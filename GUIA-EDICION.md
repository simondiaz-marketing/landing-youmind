# Guía para editar la página

Esta guía está pensada para hacer cambios sencillos en [De prompt a proceso — landing.html](./De%20prompt%20a%20proceso%20%E2%80%94%20landing.html), aunque no tengas experiencia con HTML.

## Antes de empezar

1. Abre la carpeta del proyecto en Visual Studio Code.
2. Abre `De prompt a proceso — landing.html`.
3. Guarda una copia antes de hacer cambios importantes: en VS Code puedes usar **Archivo > Guardar como…**.
4. Busca los comentarios que empiezan y terminan con `<!--` y `-->`. Explican qué hace cada sección. Estos comentarios no aparecen en la página publicada.
5. Después de guardar, abre el archivo HTML en el navegador y actualiza la página para ver los cambios.

## Cómo reconocer el contenido

- El texto que ves entre etiquetas como `<p> ... </p>` es un párrafo.
- `<h1>`, `<h2>` y `<h3>` son títulos de distintos niveles.
- `<a href="..."> ... </a>` es un enlace o botón.
- `<section> ... </section>` agrupa una parte de la página.
- `<br>` fuerza un salto de línea dentro de un texto.
- El texto entre `<` y `>` describe el elemento. Procura no borrarlo si solo quieres cambiar las palabras.

Por ejemplo, para cambiar el título principal, busca `De prompt` dentro de la sección **Portada** y cambia solo las palabras entre las etiquetas `<h1>` y `</h1>`. Conserva las etiquetas y el `id="hero-title"`.

## Dónde hacer los cambios más comunes

| Quiero cambiar… | Busca esta sección o texto |
| --- | --- |
| Título y textos principales | **Portada** (`hero`), cerca del comienzo del `<body>` |
| Nombre o marca | `SIMÓN DÍAZ` o `SD`, en el encabezado y el pie |
| Beneficios | **Sección 02**, dentro de cada tarjeta (`benefit-card`) |
| Temas de la guía | **Sección 03**, en la lista `content-list` |
| Plantilla de muestra | **Sección 04**, dentro del bloque `<pre class="template">` |
| Textos de registro y descarga | Sección `id="descarga"` |
| Preguntas y respuestas | Sección **Preguntas frecuentes**; cada pregunta está en `<summary>` |
| Enlace de YouTube | Busca `youtube.com` en el pie de página |
| Título de la pestaña y descripción | Al principio, dentro de `<head>`: `<title>` y `meta name="description"` |
| Colores y apariencia | Bloques `<style>`; los colores principales están al principio en `:root` |

Puedes buscar un texto con **Ctrl+F** (Windows) o **Cmd+F** (Mac). Para cambiar una frase, reemplaza solo esa frase y no las etiquetas que la rodean.

## Cambiar colores y espacios

Los estilos están en bloques `<style>`. Las variables del inicio, dentro de `:root`, guardan colores que se reutilizan en toda la página; por ejemplo, `--purple` es el color morado principal. Cambiar una variable actualiza los elementos que la usan.

Al final de varios bloques encontrarás reglas `@media`. Estas ajustan el diseño para pantallas más pequeñas. Si solo quieres cambiar un color o un tamaño sencillo, edita una regla existente y revisa la página tanto en una ventana amplia como en una estrecha.

## Cambiar enlaces

- Para cambiar el destino de un botón o enlace, edita el valor de `href="..."`.
- Los destinos que empiezan con `#` llevan a una sección de esta misma página. Por ejemplo, `href="#descarga"` lleva al elemento que tiene `id="descarga"`.
- Si cambias el `id` de una sección, actualiza también todos los `href` que apuntan a ese identificador.
- Los enlaces a otras páginas usan una dirección completa, como el enlace de YouTube del pie.

## Añadir o quitar una tarjeta o pregunta

Las tarjetas de beneficios se encuentran dentro de `benefit-grid`. Cada bloque `<article class="benefit-card"> ... </article>` es una tarjeta. Puedes copiar una tarjeta completa, pegarla junto a las otras y sustituir su número, título y descripción.

En las preguntas frecuentes, cada bloque `<details> ... </details>` contiene una pregunta (`<summary>`) y su respuesta (`<p>`). Para añadir otra, copia un bloque entero y cambia su texto.

Al copiar bloques, comprueba que cada etiqueta de apertura tenga su etiqueta de cierre correspondiente. Si no estás seguro, es más seguro editar el texto existente que añadir o borrar etiquetas.

## Importante: el formulario de descarga

El formulario está **desactivado hasta que se configure una integración de servidor**. La página no registra correos ni entrega la guía por sí sola. En el código, `leadEndpoint` está vacío a propósito; mientras siga así, se muestra el aviso de que la integración no está disponible.

Para activar esta función hace falta un servicio HTTPS que:

1. Reciba una solicitud `POST` con un objeto JSON como `{"email":"persona@ejemplo.com"}`.
2. Registre el correo de forma segura y permita solicitudes desde el dominio donde se publicará la página.
3. Solo después de confirmar el registro, responda con JSON que incluya `{"success":true,"downloadUrl":"https://..."}`.
4. Entregue una URL HTTPS autorizada para descargar la guía.

La dirección de ese servicio se configura en `CONFIG`, en el script del final del HTML. No pongas contraseñas, claves privadas ni credenciales dentro del HTML: cualquier visitante puede ver el código de una página web. La integración también requiere revisar privacidad, protección contra abuso y control de acceso a la descarga. El código actual no envía correos automáticos.

No cambies los identificadores del formulario —por ejemplo `lead-form`, `form-fields`, `email` e `integration-notice`— salvo que también se actualicen las referencias correspondientes en JavaScript. Si no cuentas con el servicio de servidor, deja el formulario desactivado y conserva el aviso visible.

## Revisión antes de publicar

- Comprueba que los textos nuevos se lean bien y no hayan quedado etiquetas visibles.
- Prueba los botones y enlaces internos, especialmente los que llevan a `#descarga` y `#contenido-guia`.
- Revisa la página en un teléfono o en una ventana estrecha.
- Confirma que las preguntas frecuentes se abren y cierran.
- Si no está configurado el servicio de registro, asegúrate de que el aviso del formulario siga visible y no prometas una descarga que aún no funciona.
