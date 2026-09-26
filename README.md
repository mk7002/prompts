# Prompt Library

A reusable collection of AI prompts for image editing, image generation, coding, writing, productivity, and more. Designed to work as a standalone prompt library or as the source for an AI skill.

## Categories

- [Image](./image/)
- [Coding](./coding/)
- [Writing](./writing/)
- [Productivity](./productivity/)

## How to add a prompt

Create a Markdown file in the appropriate category folder, starting from one of the templates:

- [Generic prompt](./templates/generic-prompt.md)
- [Image editing prompt](./templates/image-editing-template.md)
- [Coding prompt](./templates/coding-prompt-template.md)

Set the frontmatter `category` to the folder path (for example `image/editing`) and add the prompt to the category's README. See [CONTRIBUTING.md](./CONTRIBUTING.md).

Prefer action-based filenames such as:

- `remove-objects.md`
- `background-cleanup.md`
- `generate-portrait.md`
- `review-flutter-code.md`
- `rewrite-email.md`

## Using as an AI Skill

This repository can also be used as the prompt source for an AI skill.

See [SKILL.md](./SKILL.md) for the skill instructions. The skill points to this repository instead of embedding the complete prompt library, allowing the prompts to be maintained independently.

Repository: https://github.com/mk7002/prompts
