# Prompt Library Skill

## Purpose

Use this repository as the source of truth for reusable AI prompts.

Repository:
https://github.com/mk7002/prompts

## How to Use

When a user asks for a task that may have a reusable prompt:

1. Identify the appropriate prompt category.
2. Locate the most relevant prompt file in this repository.
3. Read the prompt and understand its intent.
4. Adapt the prompt to the user's specific context when necessary.
5. Use the repository prompt as the base instruction rather than inventing a completely new prompt.
6. Prefer the latest version available in the repository.
7. Do not reproduce unrelated prompts or the entire prompt library.

## Categories

- `image/editing`
- `image/generation`
- `image/styling`
- `coding`
- `writing`
- `productivity`

## Prompt File Convention

Prompts are stored as Markdown files.

Typical structure:

```text
category/
└── subcategory/
    └── task-name.md
```

For example: `image/editing/remove-people.md`.

Each prompt file contains:

- YAML frontmatter with `title`, `category` (matching the folder path, e.g. `image/editing`), `type`, `model`, and `tags`
- A `#` title heading
- `## Description`
- `## Prompt`
- `## Use Cases`
- `## Notes`

Each category folder has a `README.md` that indexes its prompts. Check it first to find the right file.

## Examples

User request:

> I want to remove unwanted people from a photo.

Find:

```text
image/editing/remove-people.md
```

Use that prompt as the base and adapt it to the user's image/context.

User request:

> Put a soft beige studio background behind me for my LinkedIn photo.

Find:

```text
image/editing/studio-background.md
```

Fill in the placeholders from the request (for example, `[color]` → beige, `[gradient / solid backdrop]` → gradient) and adapt the wording, such as referring to "me" when the user is the subject.

## Important

The GitHub repository is the prompt library. The skill provides the instructions for discovering and using the library.

Do not copy the entire repository into the skill.

If the repository cannot be accessed, explain that the prompt source is unavailable rather than inventing repository contents.
