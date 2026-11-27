---
name: obsidian-publishing
description: Prepare and publish approved learning notes to the user's Obsidian Vault. Use when saving, updating, or organizing technical learning notes in Obsidian.
---

# Obsidian Publishing

## Purpose

This Skill defines how to prepare and publish approved technical learning notes to the user's Obsidian Vault.

It ensures that learning notes follow Obsidian-compatible Markdown conventions, use consistent metadata, and are saved to the correct location without accidentally overwriting existing notes.

## 1. Obsidian Configuration

### Vault Path

```text
~/Documents/ObsidianVault/
```

### Learning Notes Directory

```text
Knowledge/
```

All learning notes must be saved inside the `Knowledge/` directory under the configured Vault.

The resulting path should follow this structure:

```text
~/Documents/ObsidianVault/
└── Knowledge/
    ├── Redis Token Bucket Rate Limiting.md
    └── Node.js Event Loop.md
```

Do not save learning notes outside this directory unless the user explicitly requests a different location.

## 2. Publishing Workflow

Follow these steps when publishing a learning note:

1. Confirm that the user has approved the article for publishing.
2. Prepare the article using the approved learning note template.
3. Check that the content uses valid Markdown and Obsidian-compatible syntax.
4. Add the required YAML frontmatter.
5. Generate a descriptive filename using a human-readable title.
6. Check whether a file with the same name already exists.
7. Save the note to the configured Learning Notes Directory.
8. Confirm that the file was created successfully.

Do not skip the user's publishing approval.

Approval to generate an article does not automatically authorize publishing it.

## 3. Publishing Rules

### File Format

- Save all learning notes as Markdown (`.md`).
- Use UTF-8 encoding.
- Use descriptive, human-readable filenames.
- Use normal title capitalization and spaces between words.
- Keep filenames consistent with the article title.
- Avoid unnecessary special characters in filenames.

Example:

```text
Redis Token Bucket Rate Limiting.md
```

### YAML Frontmatter

Every published learning note must include YAML frontmatter.

Use the following format:

```yaml
---
title: "Redis Token Bucket Rate Limiting"
date: 2026-11-27
tags:
  - redis
  - rate-limiting
  - algorithm
---
```

Frontmatter requirements:

- `title`: A clear and descriptive article title.
- `date`: The date the note is published, using `YYYY-MM-DD`.
- `tags`: Relevant tags that help organize and discover notes.

Use existing tag conventions when available. Avoid creating unnecessary or duplicate tags.

Do not add properties that are not useful for the note.

### Title and Heading Consistency

- Use a human-readable title in YAML frontmatter.
- The H1 heading should match the YAML title.
- The filename should match the title, with `.md` as the file extension.
- Do not use kebab-case filenames unless explicitly requested.
- Avoid duplicate titles within the same Vault when possible.

Example:

Filename:

```text
Redis Token Bucket Rate Limiting.md
```

Frontmatter:

```yaml
---
title: "Redis Token Bucket Rate Limiting"
date: 2026-11-27
tags:
  - redis
  - rate-limiting
---
```

Article heading:

```markdown
# Redis Token Bucket Rate Limiting
```

## 4. Existing Notes and File Safety

Before creating a note:

- Check whether a file with the same filename already exists.
- Do not overwrite existing files.
- Do not delete or rename existing notes.
- Do not modify existing notes unless the user explicitly approves the changes.

If a file with the same name already exists:

1. Read the existing note when access is available.
2. Determine whether it covers the same topic.
3. Report the conflict to the user.
4. Ask whether to update the existing note or create a separate note with a different filename.

Never silently create duplicate notes or overwrite existing content.

## 5. Obsidian Markdown Conventions

Use Obsidian-compatible Markdown.

Where appropriate:

- Use `[[Internal Links]]` to link related notes.
- Use aliases when a link needs a more readable display name.
- Use Obsidian callouts for useful tips, warnings, or important information.
- Use standard Markdown headings, lists, tables, and code blocks.
- Use meaningful tags and YAML properties.

Do not add wikilinks or callouts simply for decoration. Only use them when they improve navigation or understanding.

Follow the `obsidian-markdown` Skill for detailed Obsidian syntax and formatting conventions.

## 6. Publishing Verification

After saving a note:

- Confirm that the file exists at the expected path.
- Confirm that the file contains the complete article.
- Confirm that the YAML frontmatter is present and correctly formatted.
- Confirm that the filename matches the article title.
- Report the final file path to the user.

If file creation or verification fails, explain the problem clearly.

Never claim that a note has been published successfully without verifying the file.

## 7. Important Restrictions

- Only publish articles approved by the user.
- Never overwrite existing notes without explicit approval.
- Never delete existing notes.
- Never change the configured Vault path or Learning Notes Directory without user approval.
- Do not publish draft articles unless the user explicitly approves them.
- Preserve the approved article's content and scope during publishing.