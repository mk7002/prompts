---
name: prompt-library
description: Reusable prompts for image editing (remove background, people, or objects; replace or clean up backgrounds; enhance photos), image generation, and image styling. Use when the user asks to edit, generate, or restyle an image, or for any task that may match a saved prompt in this library.
---

# Prompt Library Skill

## Purpose

Use this prompt library as the source of truth for reusable AI prompts. Instead of writing a new prompt from scratch, find the matching prompt below, adapt it to the user's request, and use it.

Repository: https://github.com/mk7002/prompts

## How to Use

When a user asks for a task that may have a reusable prompt:

1. Pick the most relevant prompt from the **Prompt Index** below.
2. Read that prompt file:
   - If the file is available locally (next to this `SKILL.md`), read it from there.
   - Otherwise, fetch its raw URL: `https://raw.githubusercontent.com/mk7002/prompts/main/<path>`
3. Take the text under `## Prompt` as the base instruction and check `## Notes` for tips and limitations.
4. Fill in any `[bracketed placeholders]` using the user's request. If a placeholder is required and the user hasn't said, choose a sensible default and mention it.
5. Adapt the wording to the user's context. For example, say "me" and "my" when the user is the subject of their own photo.
6. Carry out the task with the adapted prompt. If you can edit or generate images, apply the prompt to the user's image. Otherwise, give the user the final prompt to paste into their image tool.
7. Use only the prompt that is needed. Do not reproduce unrelated prompts or the whole library.

If no prompt fits the request, say so and help the user directly.

## Prompt Index

### Image editing — `image/editing/`

| Task | File |
|---|---|
| Remove the background (transparent, white, or plain color) | `image/editing/remove-background.md` |
| Replace the background with a studio backdrop (portraits, headshots) | `image/editing/studio-background.md` |
| Replace the background with a new scene or location | `image/editing/background-replacement.md` |
| Clean up clutter or distractions in the background | `image/editing/background-cleanup.md` |
| Remove unwanted people | `image/editing/remove-people.md` |
| Remove unwanted objects | `image/editing/remove-objects.md` |
| Replace one object with another | `image/editing/object-replacement.md` |
| Enhance quality (sharpness, exposure, noise) | `image/editing/image-enhancement.md` |

### Image generation — `image/generation/`

| Task | File |
|---|---|
| Generate a portrait of a person | `image/generation/portraits.md` |
| Generate product photography | `image/generation/product-photography.md` |
| Generate a landscape or scenery | `image/generation/landscapes.md` |
| Generate a social media image or thumbnail | `image/generation/social-media.md` |

### Image styling — `image/styling/`

Styles can be combined with a generation prompt or applied to an existing image.

| Style | File |
|---|---|
| Cinematic / film look | `image/styling/cinematic.md` |
| Photorealistic | `image/styling/realistic.md` |
| Professional / corporate | `image/styling/professional.md` |
| Artistic (painting, illustration, sketch) | `image/styling/artistic.md` |

### Coming soon

`coding/`, `writing/`, and `productivity/` have no prompts yet.

## Prompt File Format

Each prompt file contains:

- YAML frontmatter with `title`, `category` (matching the folder path, e.g. `image/editing`), `type`, `model`, and `tags`
- A `#` title heading
- `## Description`
- `## Prompt`
- `## Use Cases`
- `## Notes`

## Examples

**User:** "Remove the background from this photo."
Use `image/editing/remove-background.md`. If the user doesn't say what should replace the background, use pure white and mention that transparent is also possible.

**User:** "Remove the people behind me in this photo."
Use `image/editing/remove-people.md` and refer to the user as "me" when describing the main subject.

**User:** "Put a soft beige studio background behind me for my LinkedIn photo."
Use `image/editing/studio-background.md` and fill in the placeholders: `[color]` → beige, `[gradient / solid backdrop]` → gradient.

## Important

- The repository is the prompt library. This skill only explains how to find and use it.
- If a prompt file cannot be read, either locally or from its raw URL, tell the user the prompt source is unavailable. Do not invent the prompt's contents.
- When a prompt is added to the library, add it to the Prompt Index above.
