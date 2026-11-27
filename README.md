# Knowledge Capture

A reusable knowledge capture workflow for software development, powered by AI coding agents.

## Purpose

AI coding agents can help <your-path>s complete tasks faster, but completing a task does not always mean understanding the underlying concepts or technical decisions.

This repository provides a workflow for identifying meaningful learning opportunities during software development and turning them into reusable technical learning notes.

The goal is to build a long-term technical knowledge base based on practical development experience.

The knowledge base may include:

- Technical concepts and explanations
- Implementation approaches and design decisions
- Problem-solving experiences
- Troubleshooting guides
- Reusable development knowledge

The generated articles are stored separately in an Obsidian Vault or another knowledge base. This repository manages the workflow, Skills, and templates used to create them.

## Goals

- Identify meaningful learning opportunities during development.
- Turn practical development experience into technical learning articles.
- Explain underlying concepts, implementation details, and design trade-offs.
- Build reusable knowledge across different projects.
- Improve understanding through practical examples and review questions.

## How It Works

The workflow is designed to run alongside normal software development.

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

1. **Identify:** Evaluate whether a completed task contains meaningful technical learning value.
2. **Recommend:** Suggest relevant topics and explain why they are worth documenting.
3. **Review:** Check existing notes for related or duplicate content when the Obsidian Vault is accessible.
4. **Approve:** Wait for the user to approve the proposed topics.
5. **Generate:** Create articles based on actual implementation, development discussions, and reliable technical references.
6. **Review:** Allow the user to review and revise generated content.
7. **Publish:** Obtain separate approval before saving articles to the Obsidian Vault.

Not every development task needs an article. Avoid documenting trivial changes or routine work.

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

## Repository Components

| Component | Responsibility |
|---|---|
| `AGENTS.md` | Defines the knowledge capture workflow, rules, and approval requirements. |
| `skills/` | Contains external and custom Skills used by the workflow. |
| `templates/` | Provides reusable templates for learning notes. |
| `references/` | Defines writing standards and additional guidance. |
| `README.md` | Explains the repository and how to use it. |

## Skills

This repository uses a combination of external Skills and custom Skills.

### External Skills

These Skills are downloaded from existing GitHub repositories.

| Skill | Source | Purpose |
|---|---|---|
| `technical-documentation` | [dsebastien/technical-documentation-skill](https://github.com/dsebastien/technical-documentation-skill) | Writing, reviewing, and improving technical documentation. |
| `plain-language` | [arjunprabhulal/agent-skills](https://github.com/arjunprabhulal/agent-skills/tree/main/skills/docs/plain-language) | Improving clarity and readability while preserving technical accuracy. |
| `obsidian-markdown` | [obsidianmd/obsidian-skills](https://github.com/obsidianmd/obsidian-skills) | Working with Obsidian Markdown, properties, wikilinks, embeds, and callouts. |

### Custom Skills

These Skills are created specifically for this repository's workflow.

| Skill | Purpose |
|---|---|
| `obsidian-publishing` | Preparing and publishing approved learning notes to the Obsidian Vault. |

### Finding and Adding Skills

You can discover additional Skills from:

- [skills.sh](https://skills.sh/) — Search for existing Agent Skills.
- [GitHub](https://github.com/) — Find repositories containing `SKILL.md` files.

Before adding an external Skill:

1. Review its `SKILL.md` and understand its purpose.
2. Check its license and attribution requirements.
3. Check whether it fits this repository's workflow.
4. Preserve its original author and source information.
5. Review and maintain any modifications made to the original Skill.

Only add Skills that provide useful capabilities for this workflow.

## Getting Started

### Prerequisites

- [OpenCode](https://opencode.ai/)
- Git
- An Obsidian Vault (optional, but required for direct publishing)

### 1. Clone the Repository

Clone this repository to a location outside your development projects.

```bash
git clone <repository-url> ~/<your-path>/knowledge-capture
```

The repository is intended to be shared across multiple projects. You do not need to copy its Skills into individual project directories.

### 2. Configure OpenCode

Open your OpenCode configuration file:

- macOS / Linux: `~/.config/opencode/opencode.json`
- Windows: `%USERPROFILE%\.config\opencode\opencode.json`

Add the repository's Skill directory and `AGENTS.md` to the configuration:

```json
{
  "$schema": "https://opencode.ai/config.json",
  "skills": [
    "~/<your-path>/knowledge-capture/skills"
  ],
  "instructions": [
    "~/<your-path>/knowledge-capture/AGENTS.md"
  ]
}
```

Adjust the paths if you cloned the repository to a different location.

This configuration allows OpenCode to discover the Skills and load the repository instructions without copying them into each project or installing the Skills in the global skills directory.

See the [OpenCode Skills documentation](https://opencode.ai/docs/skills/) and [Configuration documentation](https://opencode.ai/docs/config/) for details.

### 3. Configure the Obsidian Vault

Set the destination Vault path in the `obsidian-publishing` Skill.

For example:

```text
/Users/your-username/Documents/Obsidian/
```

The Vault path should be configured in one place rather than repeated across different project instructions.

Do not publish notes until the user has reviewed and approved them.

## How to Use

Once configured, use OpenCode normally while working on your development projects.

The knowledge capture workflow should be considered when a meaningful development task is completed.

### Example Prompts

**Evaluate a completed task**

```text
Review the work completed in this task.

Identify any meaningful technical learning opportunities
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

Learning articles should follow these principles:

- Use clear and simple English suitable for a non-native English speaker.
- Prefer common words and relatively short sentences.
- Explain unfamiliar technical terms.
- Use practical examples to explain abstract concepts.
- Explain why and how, not only what.
- Discuss relevant alternatives, trade-offs, and limitations.
- Clearly distinguish actual implementation from general technical knowledge.
- Avoid unnecessary repetition and unrelated content.
- Preserve technical accuracy.

See [`references/writing-guidelines.md`](references/writing-guidelines.md) for the full writing standards.

## Design Principles

- **Learning over documentation:** Capture knowledge that improves understanding, not every development activity.
- **User ownership:** The user controls article topics, scope, content, and publishing.
- **Practical knowledge:** Base articles on real development experience.
- **Reusable knowledge:** Focus on concepts that can be applied across projects.
- **No automatic publishing:** Always obtain approval before generating or publishing notes.
- **Maintainability:** Keep Skills, templates, and guidelines reusable and easy to update.