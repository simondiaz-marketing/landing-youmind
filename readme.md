# De prompt a proceso — landing para YouMind

Página de presentación de **De prompt a proceso**, una guía práctica de Simón Díaz sobre cómo crear, importar y mejorar Skills en YouMind. Es un recurso educativo independiente y no un tutorial oficial de YouMind.

La landing presenta los objetivos y el contenido de la guía, muestra una plantilla de ejemplo y ofrece una sección de preguntas frecuentes. Incluye una interfaz de registro para habilitar la descarga, aunque la integración todavía está pendiente.

## Estado de la descarga

**El registro de correos y la descarga no están disponibles actualmente.** La página mantiene el formulario desactivado porque `CONFIG.leadEndpoint` está vacío. El repositorio no incluye la guía descargable en su raíz y la página, por sí sola, no registra correos ni envía emails automáticos.

Para activar la funcionalidad se necesita un servicio HTTPS propio que reciba el correo, confirme su registro y devuelva una URL HTTPS autorizada de descarga. El contrato esperado es:

- Solicitud `POST` con JSON: `{"email":"persona@ejemplo.com"}`.

- Respuesta HTTP 2xx con JSON: `{"success":true,"downloadUrl":"https://..."}`.

- El servicio debe permitir solicitudes desde el dominio donde se publique la landing.

La URL del servicio se configura en `CONFIG.leadEndpoint`, en el script al final de `index.html`. Antes de activarlo, revisá la protección de datos, la validación del lado del servidor, el almacenamiento seguro, la protección contra abuso y el control de acceso a la descarga. No incluyas credenciales ni claves privadas en el HTML.

## Tecnologías y características

- HTML, CSS y JavaScript integrados en un único archivo.

- Diseño adaptable a distintas pantallas.

- Enlaces internos, preguntas frecuentes desplegables y validación del formulario cuando la integración está configurada.

- Tipografías Inter y JetBrains Mono desde Google Fonts, con fuentes alternativas si no se pueden cargar.

- Opciones de accesibilidad como enlace para saltar al contenido, indicadores de foco y adaptación a la preferencia de movimiento reducido.

## Ver la página en tu computadora

1. Descargá o cloná el repositorio.

2. Abrí `index.html` en un navegador.

3. Para ver cambios, editá el archivo, guardalo y actualizá la página en el navegador.

No hace falta instalar dependencias para visualizar la landing. La carga de las fuentes externas requiere conexión a internet. El formulario de registro requiere JavaScript y una integración HTTPS configurada.

## Archivos principales

```plaintext
landing-youmind/
├── .agents/          # Carpeta del repositorio
├── Captura.PNG       # Imagen incluida en el repositorio
├── GUIA-EDICION.md   # Guía para editar la página
└── index.html        # Contenido, estilos y lógica de la landing
```

> **Nota:** `GUIA-EDICION.md` menciona un nombre de archivo HTML anterior. En la raíz actual del repositorio, el archivo de la página es `index.html`.

## Edición

La [guía de edición](./GUIA-EDICION.md) explica cómo modificar textos, colores, enlaces, tarjetas y preguntas frecuentes. El propio HTML también contiene comentarios que identifican las secciones.

Antes de publicar cambios, comprobá los enlaces internos, revisá la página en una pantalla pequeña y probá las preguntas frecuentes. Si el servicio de registro aún no está configurado, conservá el aviso de que el registro y la descarga no están disponibles.

## Autor

**Simón Díaz** — recurso educativo independiente sobre YouMind.