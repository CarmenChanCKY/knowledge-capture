# Technical Writing Guidelines

This document defines the content standards and teaching principles for technical learning articles.

The goal is to help readers understand technical concepts, learn from practical development experience, and apply the knowledge in other projects.

## 1. Content Requirements

Base articles on actual implementation, codebase, development discussions, and reliable technical references where appropriate.

Depending on the topic, explain:

- Underlying technical concepts and how they work.
- Why a particular approach was chosen.
- Important implementation details.
- Design decisions and their trade-offs.
- Relevant alternatives.
- Practical examples.
- Important edge cases and common mistakes.

Do not include information simply to make an article longer. Focus on knowledge that helps readers understand the topic.

### Distinguish Implementation from General Knowledge

Clearly distinguish between:

- **Actual Implementation:** What was actually implemented or experienced in a particular project.
- **General Technical Knowledge:** Related concepts, technical explanations, and established practices.

Do not present general technical knowledge as something that was actually implemented.

Do not generalize a project-specific solution into a universal best practice.

Clearly identify assumptions, uncertainties, and context-dependent recommendations.

## 2. Article Structure and Depth

Adapt the article structure and depth to the topic.

Common knowledge categories include:

- **Technical Concepts:** Explain technical principles, how they work, and why they matter.
- **Practical Experience:** Document implementation approaches, challenges, investigation methods, and solutions.
- **Design Decisions:** Explain architectural choices, alternatives, constraints, and trade-offs.
- **Troubleshooting:** Explain symptoms, root causes, investigation methods, and solutions.

These categories are guidelines, not mandatory templates. A topic may cover multiple categories.

### Recommended Teaching Flow

When appropriate, organize explanations in this order:

1. **Context:** Introduce the problem, concept, or scenario.
2. **Concept:** Explain the underlying technical principles.
3. **How It Works:** Describe the relevant process or mechanism.
4. **Practical Application:** Show how the concept is used.
5. **Design Considerations:** Discuss alternatives, trade-offs, and limitations.
6. **Common Issues:** Cover relevant edge cases and mistakes.

Not every article needs all these sections. Choose the structure that best supports understanding.

## 3. Explain Technical Concepts

When introducing an unfamiliar concept:

- Explain what it is.
- Explain what problem it solves or why it exists.
- Explain how it works.
- Explain when and why it is useful.
- Connect it to practical development scenarios.

Explain concepts before introducing complex implementation details when those concepts are necessary to understand the example.

Avoid explanations that only describe what a piece of code does. Explain the underlying reasoning and behavior.

## 4. Use Practical Examples

Use examples to make abstract concepts easier to understand.

Good examples should:

- Demonstrate the concept being explained.
- Be relevant to real development scenarios.
- Include enough context to understand what is happening.
- Show expected input and output when useful.
- Avoid introducing unrelated concepts.

### Code Examples

When including code:

- Keep examples focused on the concept being explained.
- Include only relevant code.
- Explain important parts of the code.
- Use realistic names and values.
- Clearly distinguish simplified examples from actual project code.
- Avoid large code blocks when a smaller example is sufficient.

## 5. Explain Design Decisions and Trade-offs

When documenting an implementation or design decision, explain:

- What approach was chosen.
- Why it was chosen.
- What alternatives were considered.
- What advantages and disadvantages the approach has.
- What limitations or conditions may affect the decision.

Explain the context in which an approach makes sense.

Do not describe an implementation choice as universally correct when it depends on project requirements, constraints, or trade-offs.

## 6. Cover Important Edge Cases and Limitations

Include edge cases when they affect correctness, reliability, security, performance, or maintainability.

Examples include:

- Invalid or missing input.
- Unexpected data formats.
- Network failures and timeouts.
- Concurrent requests.
- Duplicate operations.
- Permission and authentication failures.
- Resource cleanup and error handling.

Also explain relevant limitations, such as:

- Performance considerations.
- Security implications.
- Scalability concerns.
- Compatibility requirements.
- Operational complexity.
- Dependencies on specific technologies or configurations.

Focus on cases relevant to the topic. Do not list every theoretical possibility.

## 7. Organize Articles for Easy Reading

- Use descriptive headings that explain what each section covers.
- Keep each section focused on one main idea.
- Use lists for related items or steps.
- Use tables when comparing multiple options.
- Use code blocks for code and command examples.
- Use diagrams when they provide a clearer explanation than text.
- Avoid repeating the same explanation in multiple sections.

Each section should build on knowledge introduced earlier.

## 8. Technical Accuracy and References

Ensure technical explanations are accurate and supported by reliable information.

When necessary, verify important technical claims against reliable sources.

Prefer:

- Official documentation.
- Technical specifications and standards.
- Well-maintained project documentation.
- Reputable technical articles.

When explaining external APIs, framework behavior, technical standards, or information that may change over time, include relevant references where appropriate.

Also:

- Distinguish confirmed behavior from assumptions or interpretations.
- Mention relevant technology versions when behavior depends on them.
- Do not present outdated or version-specific behavior as universally applicable.
- If information cannot be verified, clearly state the uncertainty.
- Do not claim that information has been verified against documentation unless it has actually been checked.

Link directly to useful sources where possible.

Do not add references merely to make an article look authoritative.

## 9. Active Recall

Include review questions when they can improve understanding.

Questions should:

- Test understanding rather than memorization.
- Encourage readers to explain concepts in their own words.
- Include practical scenarios where useful.
- Cover important trade-offs and edge cases.

Questions should help identify gaps in understanding.

Do not force review questions into every article.

## 10. Final Content Review

Before considering an article complete, check:

- Is the main topic and purpose clear?
- Are the technical explanations accurate?
- Does the article explain why and how, rather than only what?
- Are actual implementation details clearly distinguished from general knowledge?
- Are examples relevant and understandable?
- Are important trade-offs and limitations covered?
- Are assumptions and uncertainties clearly identified?
- Is there unnecessary repetition or unrelated content?
- Can readers apply the knowledge in another situation?

An article does not need to cover everything. It should cover the knowledge necessary to understand its topic properly.