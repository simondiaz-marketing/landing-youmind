---
name: landing-page
description: Plan, write, design, or build a focused landing page for a product, service, lead magnet, event, waitlist, app, or other single-offer campaign. Covers conversion strategy, copy, visual design, implementation, and validation.
---

# Landing pages

A landing page serves one main audience, one offer, and one primary action. Use this skill for focused campaign pages, not for multi-purpose homepages unless the user identifies a single page goal.

Follow the requested level of work. If the user asks for analysis or a plan, do not edit files. If they ask to implement, build and integrate the page in the current project.

## 0. Work from a brief, references, and real assets

Treat the landing-page task as a reference-driven creation workflow, not as a request to produce an interchangeable template:

- Gather the objective, intended audience, offer, primary CTA, conversion definition, brand identity, existing copy, screenshots, links, and real product or resource assets.
- Keep the brief, design references, page copy, source assets, and implementation decisions connected throughout the work.
- If a screenshot or existing page is supplied, reproduce its structure, visual hierarchy, proportions, spacing, typography, and color logic. Improve accessibility or broken behavior where needed, but do not silently redesign it.
- If materials are incomplete, ask only for decisions that materially affect the offer or implementation. Do not invent a brand, product facts, proof, prices, guarantees, testimonials, or external integrations.
- Do not infer a YouMind project, file system, framework, API, or lead-storage implementation from this skill. Detect or ask for the user's actual environment.
- Preserve real resources and previews. Use genuine product screenshots, documents, diagrams, or project-native representations rather than invented mockups.

## 1. Inspect context and identify the goal

- Inspect the workspace before asking questions. Look for project instructions, existing pages and code, brand identity, campaign or product research, resources, assets, and configured integrations.
- If the workspace is new or has no relevant materials, use the requested stack and details. Ask only for material choices that cannot be inferred safely; do not invent brand assets, proof, or product facts.
- Treat user-provided materials as the source of truth for the offer and brand. Use external research for current or changeable claims, prefer official sources, and distinguish verified facts from assumptions.
- Identify the audience, problem, offer, promised outcome, traffic source and context, primary CTA, and what counts as a successful conversion.
- Carry forward decisions already made by the user. Avoid repeated questions.
- Determine whether the user wants a plan, a visual implementation, a functional implementation, or an editable review handoff.

## 1.1 Shape the page before styling it

Before writing CSS or generating assets:

1. Define the single page goal and main CTA.
2. State what the visitor should understand within the first screen.
3. Map the page sequence and the job of every section.
4. Choose only sections that reduce uncertainty or support the conversion.
5. Identify the real evidence that can be shown: the resource itself, a process diagram, a genuine preview, or verified facts.
6. Define the intended desktop, tablet, and mobile reading order.
7. Separate editable copy, styles, content data, and assets when the project structure allows it.
8. Choose the delivery format before implementation: maintainable project files or a portable standalone export. Follow the existing project structure when present; keep a single-file export self-contained unless the user prefers a package with separate assets.

Do not add a proof, FAQ, form, process, testimonial, or extra CTA section only to make the page feel fuller. Keep the first screen and the final conversion aligned.

## 2. Choose the conversion path

Select the path that matches the actual offer. Do not add a form or email gate to every landing page.

- **Lead magnet or free resource:** define whether access is gated, what information is collected, what happens after submission, and how the resource is delivered. Keep fields to the minimum requested. Do not promise email delivery, subscriptions, privacy practices, or follow-up messages unless they are configured and accurately described.
- **Product or paid service:** make the purchase or contact path clear. Use only verified prices, terms, guarantees, and product claims.
- **Demo, consultation, or booking:** use the configured booking or contact flow. Do not imply a reservation is confirmed unless the integration confirms it.
- **Waitlist, event, app, or open download:** use the real signup, registration, install, or download destination. Do not add lead capture unless requested or necessary to the agreed conversion.

For forms, reuse an existing integration when available. If none exists, agree on the endpoint and storage before implementation. A local file or development server is only a local prototype, not production lead storage. Never show a success state unless the action actually succeeds; preserve entered values and explain errors.

For lead-gated resources:

- Collect the minimum information required.
- Confirm whether the download is released by registration or by a direct verified resource link.
- Explain in interface copy exactly whether an email will be sent.
- Never promise email delivery, privacy compliance, or follow-up unless the implementation and legal copy support those claims.
- Preserve the visitor's input after submission errors.
- Prevent duplicate submissions while a request is pending.
- Show success only after registration succeeds, then reveal the real download.

If no integration exists, implement a clearly marked integration placeholder or a prototype that explicitly fails without saving data. Do not claim a lead was recorded. Keep the rest of the page usable, and do not promise immediate access or make a disabled email form the primary CTA. Link directly to the real resource if that is the agreed path and the file exists; otherwise state clearly that access is not available yet.

## 3. Shape the page and write the copy

- Make the offer, intended audience, value, and primary action clear in the first screen.
- Match the message to the traffic source and what visitors already know, when that context is available.
- Write benefit-first, specific copy. Tie claims to available evidence; do not invent statistics, outcomes, testimonials, logos, endorsements, guarantees, or product capabilities.
- Choose a structure that serves the offer. A page may use a hero, problem and solution, benefits, process, proof, objection handling, FAQ, and final CTA, but do not add sections just to follow a template.
- Use genuine previews from the actual resource or product. Do not turn an independent resource into an official product endorsement.
- Keep one primary CTA. Secondary links may exist when useful, but should not compete with the main conversion.
- Use risk-reversal language only when the trial, cancellation, refund, or guarantee is real and documented.
- Keep copy concise enough to scan. The first screen should explain what it is, for whom it is useful, the promised outcome, and the next action.

## 4. Create and integrate visual assets

Plan visuals by their purpose, not by filling every section with decoration. A useful page may need a hero visual, a simple process diagram, and a genuine preview of the offer.

- Inspect brand references and preserve required colors, typography, contrast, and visual tone.
- Use the image-generation tool for requested photographic or illustrative raster assets when available. Specify composition, use case, palette, and avoid-list; keep generated text out of images unless exact text is required.
- If image generation is unavailable, explain the limitation and continue with project-native SVG/CSS where suitable. Do not silently substitute unrelated stock imagery or switch to an unrequested CLI/API workflow.
- Build diagrams with SVG or other project-native assets. Base previews on the actual product or resource, not invented sample pages. Verify the source asset is present before calling a preview real; label illustrative material honestly.
- Store referenced assets in the project. Add descriptive alt text, and accessible titles or descriptions for informative SVGs.
- Optimize crop, intrinsic dimensions, and mobile layout intentionally.
- Prefer clear visual hierarchy over excessive decoration: one dominant image or composition, a restrained accent, consistent borders, structured grids, and generous whitespace.
- Use screenshots or native mockups only when they represent real behavior or real resource content.
- Avoid gradients, neon effects, stock people, particles, cyberpunk motifs, and unrelated 3D objects unless a supplied reference explicitly calls for them.
- Make the output easy to review and revise: keep section boundaries clear and make copy, images, CTAs, and links straightforward to locate and replace.

## 5. Implement accessibly and validate

- Follow the existing stack and conventions. For a static project without a framework, use a small HTML/CSS/JS implementation. Avoid unnecessary dependencies.
- Keep code formatted and readable rather than minified. Put styles in the document head or the project's stylesheet, not between page sections in the body.
- When styles are separate or reused, scope landing-page selectors to a page root or use a consistent prefix so generic rules do not unintentionally affect the host site. Keep theme values such as colors and typography easy to customize with CSS variables.
- Use JavaScript only for requested behavior; do not add scripts merely for decoration. Keep simple behavior small, and separate substantial scripts from HTML when the project structure supports it. Essential content and navigation must remain available if JavaScript fails.
- Keep the implementation limited to the landing page and its agreed conversion path. Do not add campaigns, analytics, or automated follow-up unless requested.
- Make the page responsive across desktop, tablet, and mobile. Preserve readable type sizes, comfortable line lengths, and touch-friendly controls.
- Use semantic structure, sufficient contrast, visible focus, keyboard-accessible controls, and properly associated form labels. Respect `prefers-reduced-motion`; keep essential content available if scripts or animation fail.
- Add page title, description, social metadata, and internal links when appropriate to the goal and traffic source.
- Decide whether the page should be indexed based on whether the offer is evergreen and matches search intent. Use `noindex` only when appropriate, such as a private or time-limited campaign.
- Run the smallest relevant build, test, or validation command. Verify links, downloads, form behavior, and responsive layout; use available browser validation when practical.
- Test at narrow widths down to at least 320 px and confirm that there is no unintended horizontal overflow.
- Verify invalid, pending, successful, and failed form states where a form is present.
- When scripts fail or the animation environment is unavailable, keep essential copy and controls visible and usable.
- Keep motion subtle and short. Scroll reveals must never hide final content or block interaction.

## 5.1 Editable and shareable handoff

When the target environment supports live editing or publishing:

- Organize the page into clear sections or components.
- Keep copy and data easy to edit independently of layout.
- When the user requests beginner-friendly code or identifies a beginner as the editor, add concise comments in the user's language to explain each file, major section, safe-to-edit content, theme variables, and important script configuration. Use the correct comment syntax for each file (HTML `<!-- -->`, CSS `/* */`, JavaScript `//` or `/* */`). Do not comment every line or explain obvious syntax. Keep the formatting readable; comments are not a substitute for clear structure.
- If a beginner will maintain multiple files, provide a short edit guide when requested. Map common changes to the right file and explain which linked IDs, class names, or configuration values should not be changed casually.
- Preserve a direct route to preview, refine, share, publish, or download the output.
- Use natural, element-level review language in handoff examples only if the target environment supports it.
- Do not claim a page is shareable or published unless the environment and integration confirm that state.
- If exporting HTML, verify that relative assets, fonts, styles, scripts, links, and downloads work in the exported package. For static hosting, confirm the entry file is in the configured publish directory and test both the deployed root URL and the direct HTML route when available.

## 6. Hand off clearly

- For planning, return a decision-complete page outline, recommended layout, draft copy, CTA, conversion path, and relevant SEO recommendation. List only unresolved decisions that genuinely block progress.
- For implementation, summarize what was built and identify the local files.
- Explain where form submissions go, how resources are delivered, and which production integrations remain unconfigured.
- Identify any visual asset or integration still pending. Never describe a prototype as production-ready.
- Provide the exact command or workflow used to run, build, preview, or publish the result.
- Distinguish a local prototype from persistent production storage.

## Acceptance checklist

- The first screen communicates the offer, intended audience, value, and primary CTA.
- The CTA leads to the agreed conversion path; secondary actions do not obscure it.
- Copy and visuals reflect actual project materials; claims and social proof are supported.
- Forms, booking links, purchases, and downloads work as described. Success is shown only after successful completion, and errors do not silently discard input.
- Lead capture is used only when agreed. Email delivery and follow-up are claimed only when configured.
- The selected file structure fits the project or export target; styles are scoped, readable, and easy to customize. Beginner-facing code has useful comments and an edit guide when requested.
- Previews and claims are backed by available project materials, and CTA copy matches the actual integration and resource availability.
- The page is readable and usable on mobile, with no unintended horizontal overflow.
- Controls work by keyboard, forms have labels, contrast and focus are sufficient, and motion respects reduced-motion preferences.
- SEO and indexing choices fit the page's purpose.
- The result remains easy to review and revise: sections, copy, assets, CTAs, and integrations are clear and replaceable.
