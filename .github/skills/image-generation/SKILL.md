---
name: image-generation
description: Create and edit high-quality images for articles, websites, social posts, marketing, and SEO content using an available image-generation tool. Use when a user explicitly asks for a new image or an edit to an existing image.
---

# Image Generation Skill

## Purpose
Plan, generate, review, and revise visual assets for general content and SEO workflows. This skill is **not** specific to games or any brand.

## When to use
- The user asks to create an image, illustration, infographic, hero image, thumbnail, social graphic, or product visual.
- The user asks to edit an existing image: remove/replace an object, adjust composition, change style, extend a background, or add readable text.
- Do **not** generate an image when the user only wants ideas, a written prompt, a file download, or an existing unmodified reference image.

## Required capability
This file contains workflow instructions, **not** an image model, API key, or executable image generator. Use an image-generation/editing tool actually available in the current environment. Never claim an image was generated when no image tool executed. Never invent image URLs or output files.

## Workflow
1. **Interpret the request:** determine intended subject, output channel, target audience, style, required text, aspect ratio, and any reference images. Follow user-provided constraints; when unspecified, choose reasonable defaults.
2. **Set composition:** prioritize one clear subject, purposeful hierarchy, consistent lighting, suitable whitespace, and visual clarity at typical display sizes.
3. **Prepare the generation prompt:** specify subject, environment, camera/composition, palette, typography (if required), aspect ratio, and constraints. Avoid unwanted logos, watermarks, artifacts, and illegible text.
4. **Generate or edit:** call the available image tool. For edits, use the supplied source image and preserve unchanged elements as requested. If no tool is available, provide a usable prompt and state the limitation.
5. **Review:** check fidelity to the user request, text accuracy, anatomy/geometry, contrast, cropping, and visual consistency. Correct defects through a follow-up edit when supported.
6. **Deliver:** show or link only verified generated assets. Briefly identify choices or limitations only when useful.

## SEO and accessibility
- Match the image to the actual subject of the page; do not make misleading visual claims.
- Recommend descriptive file names using lowercase hyphen-separated words (e.g. `minimalist-home-office-hero.webp`).
- Supply concise, literal alt text that describes the visible image. Avoid keyword stuffing.
- Optimize export dimensions/compression based on placement when supported; preserve legibility.
- Do not embed text that would be better presented as selectable HTML content unless the design calls for it.

## Prompt template
```text
Create a [type of image] featuring [main subject] for [placement/audience].
Style: [visual style, palette, mood].
Composition: [framing, perspective, background, negative space].
Text in image: [exact wording, or "none"].
Aspect ratio: [e.g. 16:9, 1:1, 4:5].
Must include: [requirements].
Avoid: [watermark, irrelevant logos, visual errors, unwanted elements].
```

## Editing template
```text
Edit the attached image. Change only [specific element(s)] to [desired result].
Preserve [elements that must remain unchanged].
Match existing perspective, shadows, color balance, and resolution.
Output aspect ratio: [ratio].
```

## Guardrails
- Respect copyright, image rights, privacy, and the applicable tool's safety policy.
- Do not imply a repository file automatically installs a skill into ChatGPT or activates image generation.
- Never store API keys or user secrets in this repository.
