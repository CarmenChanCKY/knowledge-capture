# AGENTS.md

## Purpose

This repository manages the workflow for capturing, organizing, and maintaining technical knowledge gained during software development.

The goal is to build a long-term, reusable technical knowledge base based on practical development experience.

The knowledge base may include:
- Technical concepts and explanations
- Implementation approaches and design decisions
- Problem-solving experiences
- Troubleshooting guides
- Reusable development knowledge

## 1. Knowledge Capture

Consider whether a completed development task contains meaningful learning value.

Evaluate learning opportunities after completing meaningful development tasks or resolving non-trivial technical problems.

Do not interrupt ongoing development work to suggest notes unless the user explicitly requests knowledge capture.

Prioritize:
- New concepts or unfamiliar technologies
- Non-trivial implementation details
- Interesting problem-solving approaches
- Important design decisions and trade-offs
- Knowledge that can be reused across projects

Do not suggest notes for trivial changes, routine edits, or tasks with little learning value.

### Recommendation Workflow

When meaningful learning opportunities are identified:

1. Briefly explain what knowledge could be captured.
2. Suggest specific article topics.
3. Explain why each topic is worth documenting.
4. Check existing notes for related or duplicate content when the Obsidian Vault is accessible.
5. Recommend creating a new note or improving an existing note.
6. Wait for the user's approval before generating or modifying any notes.

If no meaningful learning opportunity is identified, continue the normal development workflow without suggesting notes.

Never automatically generate or publish articles.

## 2. Learning Note Generation

Generate learning notes only after the user approves the proposed topic.

Follow the content requirements and article standards defined in:
- `references/writing-guidelines.md`
- `skills/technical-documentation/SKILL.md`
- `skills/plain-language/SKILL.md`

Base articles on the actual implementation, codebase, and development discussion.

Focus on explaining concepts, reasoning, and practical applications rather than simply summarizing code.

Clearly distinguish actual project implementation from general technical knowledge.

Never invent implementation details, design decisions, or development experiences.

Identify assumptions, uncertainties, and context-dependent recommendations where relevant.

## 3. Knowledge Reuse and Maintenance

Treat the knowledge base as a growing collection of interconnected knowledge, not a collection of independent articles.

When the Obsidian Vault is accessible:
- Check existing notes for related concepts before suggesting new articles.
- Prefer extending or improving existing notes over creating duplicates.
- Link related notes when they provide useful context.
- Identify opportunities to connect related concepts.
- Keep notes self-contained while avoiding unnecessary repetition.

If the Vault is unavailable, do not assume its contents or claim that duplicate notes have been checked.

Never modify existing notes without user approval.

## 4. Obsidian Publishing

Use the approved template in `templates/learning-note.md`.

Follow Obsidian-compatible Markdown syntax.

### Publishing Requirements

- Use meaningful titles, tags, and properties where appropriate.
- Save notes only to the user-approved Obsidian Vault location.
- Preserve existing notes and their content.
- Allow the user to review and revise generated articles before publishing.

Do not overwrite, delete, or publish notes without explicit user approval.

## 5. Skills

Use the appropriate Skill when performing its corresponding task.

| Skill | Responsibility |
|---|---|
| `technical-documentation` | Generate and improve technical learning articles. |
| `plain-language` | Improve clarity, readability, and accessibility without losing technical accuracy. |
| `obsidian-publishing` | Format and publish notes into the Obsidian Vault. |

Load the relevant `SKILL.md` before using a Skill.

- Load `technical-documentation` and `plain-language` when generating or revising learning articles.
- Load `obsidian-publishing` when preparing or publishing notes for Obsidian.

Load only the Skills required for the current task.

## 6. User Ownership and Approval

The user owns the learning process and the final knowledge base.

Follow these rules:

- The user has final control over article topics, scope, content, and publishing.
- Never generate notes without approval of the proposed topic.
- Approval applies only to the specific topic and scope that was proposed.
- Obtain further approval before significantly changing an approved article's scope.
- Approval to generate a note does not authorize publishing it.
- Obtain separate approval before saving or publishing a note to the Obsidian Vault.
- Never modify or delete existing notes without explicit approval.
- Do not assume the user understands a concept simply because an article has been generated.
- Explain unfamiliar concepts when asked.

## General Principles

- Prioritize learning value over article quantity.
- Prefer depth and clarity over unnecessary length.
- Capture reusable knowledge rather than project-specific details.
- Base learning notes on real development experience.
- Avoid duplicate content and unnecessary documentation.
- Keep the workflow simple and maintainable.