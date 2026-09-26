---
name: prompt-library
description: >
  Reusable prompts from the mk7002/prompts library. Use when a user asks
  for image editing, image generation, image styling, coding, writing,
  productivity, or another task that may match a saved prompt.
---

# Prompt Library Skill

## Purpose

Use this repository as the source of truth for reusable AI prompts.

Repository:

https://github.com/mk7002/prompts

Do not embed the complete prompt library in this skill.

## How to Use

When a user's request may match a reusable prompt:

1. Identify the user's task.
2. Find the closest matching prompt in the repository.
3. Read the complete prompt file.
4. Use the content under `## Prompt` as the base instruction.
5. Read `## Notes` for limitations or usage guidance.
6. Replace placeholders using information supplied by the user.
7. If a required placeholder is missing, ask only when it materially
   affects the result. Otherwise use a documented default.
8. Adapt pronouns and wording to the user's context.
9. Perform the requested task using the adapted prompt.
10. Do not reproduce unrelated prompts or the entire library.

## Accessing Prompt Files

If the repository is available locally, read the file directly.

Otherwise fetch the raw Markdown file:

https://raw.githubusercontent.com/mk7002/prompts/main/<path>

Example:

https://raw.githubusercontent.com/mk7002/prompts/main/image/editing/remove-people.md

## Prompt Index

### Image Editing

| Task | Prompt |
|---|---|
| Remove background | `image/editing/remove-background.md` |
| Studio background | `image/editing/studio-background.md` |
| Replace background | `image/editing/background-replacement.md` |
| Clean background | `image/editing/background-cleanup.md` |
| Remove people | `image/editing/remove-people.md` |
| Remove objects | `image/editing/remove-objects.md` |
| Replace objects | `image/editing/object-replacement.md` |
| Enhance image | `image/editing/image-enhancement.md` |

### Image Generation

| Task | Prompt |
|---|---|
| Portrait | `image/generation/portraits.md` |
| Product photography | `image/generation/product-photography.md` |
| Landscape | `image/generation/landscapes.md` |
| Social media image | `image/generation/social-media.md` |

### Image Styling

| Style | Prompt |
|---|---|
| Cinematic | `image/styling/cinematic.md` |
| Photorealistic | `image/styling/realistic.md` |
| Professional | `image/styling/professional.md` |
| Artistic | `image/styling/artistic.md` |

## Examples

### Example 1

User:

> Remove the people behind me from this photo.

Use:

`image/editing/remove-people.md`

Adapt the prompt so the user is treated as the main subject.

### Example 2

User:

> Remove the background from this image.

Use:

`image/editing/remove-background.md`

If the user specifies transparent, white, or another background,
follow their requirement.

### Example 3

User:

> Make this photo look cinematic.

Use:

`image/styling/cinematic.md`

Apply the styling prompt to the existing image rather than generating
an unrelated image.

## Important Rules

- The GitHub repository is the source of truth.
- Do not invent the contents of a prompt file.
- Do not copy the entire repository into the skill.
- Do not reproduce unrelated prompts.
- Prefer an existing matching prompt over creating a new prompt.
- Adapt prompts to the user's actual request.
- If no suitable prompt exists, handle the request normally.
- If a referenced prompt cannot be accessed, state that the prompt
  source is unavailable rather than pretending to have read it.

## Maintaining the Library

When adding a new prompt:

1. Create the Markdown file in the appropriate category.
2. Follow the standard prompt file format.
3. Add it to the Prompt Index in `SKILL.md`.
4. Update the relevant category README.
5. Use an action-based filename.