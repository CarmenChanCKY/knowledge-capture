# Knowledge Capture

A reusable knowledge capture workflow for software development, powered by AI coding agents.

## Purpose

AI coding agents help developers complete tasks faster, but completing a task does not always mean understanding the underlying concepts or technical decisions.

This repository provides a reusable workflow for identifying meaningful learning opportunities during development and turning them into practical technical learning notes.

The goal is to build a long-term knowledge base containing reusable knowledge from real development experience, including:

- Technical concepts and explanations
- Implementation approaches and design decisions
- Problem-solving experiences
- Troubleshooting guides
- Reusable development knowledge

Generated articles are stored separately in an Obsidian Vault or another knowledge base. This repository manages the workflow, Skills, and templates used to create them.

## How It Works

The workflow runs alongside normal software development.

```text
Complete a Development Task
          |
          v
Identify Learning Opportunities
          |
          v
Recommend Article Topics
          |
          v
User Reviews and Approves Topics
          |
          v
Generate Learning Notes
          |
          v
User Reviews and Revises Articles
          |
          v
User Approves Publishing
          |
          v
Save to Obsidian Vault
```

### Workflow Principles

1. **Identify:** Evaluate completed tasks for meaningful technical learning opportunities. Not every task needs an article.
2. **Recommend:** Suggest worthwhile topics and explain their learning value.
3. **Review:** Check existing notes for related or duplicate content when the Vault is accessible.
4. **Approve:** Obtain user approval before generating articles.
5. **Generate:** Create articles based on actual implementation, development discussions, and reliable technical references.
6. **Publish:** Obtain separate user approval before saving articles to the knowledge base.

## Repository Structure

```text
knowledge-capture/
├── AGENTS.md
├── README.md
├── skills/
│   ├── technical-documentation/
│   │   └── SKILL.md
│   ├── plain-language/
│   │   └── SKILL.md
│   ├── obsidian-markdown/
│   │   └── SKILL.md
│   └── obsidian-publishing/
│       └── SKILL.md
├── templates/
│   └── learning-note.md
└── references/
    └── writing-guidelines.md
```

| Component | Responsibility |
|---|---|
| `AGENTS.md` | Defines workflow rules and approval requirements. |
| `skills/` | Contains external and custom Skills. |
| `templates/` | Provides reusable learning note templates. |
| `references/` | Contains writing standards and guidance. |
| `README.md` | Explains the repository and how to use it. |

## Skills

This repository combines external Skills with custom Skills.

### External Skills

The following Skills are sourced from existing GitHub repositories.

| Skill | Source | Purpose |
|---|---|---|
| `technical-documentation` | [dsebastien/technical-documentation-skill](https://github.com/dsebastien/technical-documentation-skill) | Writing and improving technical documentation. |
| `plain-language` | [arjunprabhulal/agent-skills](https://github.com/arjunprabhulal/agent-skills/tree/main/skills/docs/plain-language) | Improving clarity and readability while preserving accuracy. |
| `obsidian-markdown` | [obsidianmd/obsidian-skills](https://github.com/obsidianmd/obsidian-skills) | Working with Obsidian Markdown, properties, wikilinks, embeds, and callouts. |

### Custom Skills

| Skill | Purpose |
|---|---|
| `obsidian-publishing` | Preparing and publishing approved learning notes to the Obsidian Vault. |

### Finding and Adding Skills

Additional Skills can be discovered through:

- [skills.sh](https://skills.sh/) — Search for existing Agent Skills.
- [GitHub](https://github.com/) — Find repositories containing `SKILL.md` files.

Before adding an external Skill:

1. Review its instructions and purpose.
2. Check its license and attribution requirements.
3. Ensure it fits the workflow.
4. Preserve its original source information.
5. Review and maintain any modifications.

Only add Skills that provide useful capabilities.

## Getting Started

### Prerequisites

- [OpenCode](https://opencode.ai/)
- Git
- An Obsidian Vault (optional, but required for direct publishing)

### 1. Clone the Repository

Clone the repository outside your development projects so it can be shared across multiple projects.

```bash
git clone <repository-url> ~/tools/knowledge-capture
```

### 2. Configure OpenCode

Open your OpenCode configuration file:

- macOS / Linux: `~/.config/opencode/opencode.json`
- Windows: `%USERPROFILE%\.config\opencode\opencode.json`

Add the repository's Skill directory and `AGENTS.md`:

```json
{
  "$schema": "https://opencode.ai/config.json",
  "skills": [
    "~/tools/knowledge-capture/skills"
  ],
  "instructions": [
    "~/tools/knowledge-capture/AGENTS.md"
  ]
}
```

Adjust the paths if you cloned the repository elsewhere.

This allows OpenCode to discover the Skills and load the repository instructions without copying them into individual projects.

See the [OpenCode Skills documentation](https://opencode.ai/docs/skills/) and [Configuration documentation](https://opencode.ai/docs/config/) for details.

### 3. Configure the Obsidian Vault

Set the destination Vault path in the `obsidian-publishing` Skill.

For example:

```text
/Users/your-username/Documents/Obsidian/
```

Configure the path in one place rather than repeating it across project instructions.

Notes must be reviewed and approved before publishing.

## How to Use

Once configured, use OpenCode normally while working on your development projects.

When a meaningful task is completed, ask the agent to evaluate whether it contains useful learning opportunities.

### Example Prompts

**Evaluate a completed task**

```text
Review the work completed in this task.

Identify meaningful technical learning opportunities
and recommend topics worth documenting.

Check existing Obsidian notes if the Vault is accessible.
Do not generate any articles yet.
```

**Generate an approved learning note**

```text
Generate a learning note for the approved topic.

Follow the repository's writing guidelines and relevant Skills.

Base the article on the actual implementation and
relevant technical knowledge.

Do not publish the note yet.
```

**Prepare an article for publishing**

```text
Prepare the approved learning note for Obsidian.

Follow the Obsidian Markdown conventions and the
approved learning note template.

Show me the final content before publishing.
```

## Writing Principles

Learning articles should:

- Use clear and simple English suitable for non-native English speakers.
- Prefer common words and relatively short sentences.
- Explain unfamiliar technical terms.
- Use practical examples to explain abstract concepts.
- Explain why and how, not only what.
- Discuss relevant alternatives, trade-offs, and limitations.
- Distinguish actual implementation from general technical knowledge.
- Avoid unnecessary repetition and unrelated content.
- Preserve technical accuracy.

See [`references/writing-guidelines.md`](references/writing-guidelines.md) for detailed writing standards.