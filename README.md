
# Prompt Engineer or Prompt Generator

This project is a modular, documentation-driven prompt engineering system for generating, refining, and managing prompts. All logic and workflow are managed through structured markdown files—no code execution or build system is present. The system is designed for clarity, maintainability, and extensibility, with each major concern isolated in its own file.

## Key Concepts

- **Declarative Workflow**: All instructions, context, commands, templates, and profiles are defined in markdown or structured text files. There is no executable code; the system is configuration- and documentation-driven.
- **Single Source of Truth**: Each concern (instructions, context, commands, templates, profiles) is managed in a dedicated file or directory.
- **Cross-file Consistency**: When updating commands, templates, or context, always update related files to maintain consistency.
- **Extensible Profiles**: Agent and workflow profiles allow for rapid switching and customization of prompt engineering strategies.

## Project Structure

- `main_instruction.md`: Central JSON configuration and system instructions. Defines the workflow, user interaction steps, and restrictions.
- `context/context.md`: Domain-specific context, best practices, prompt formats, paradigms, and techniques.
- `commands/commands.md`: All available commands, their syntax, and descriptions for workflow automation.
- `profiles/`: Agent and workflow profiles for customizing prompt generation strategies (see `profiles/profile.md`).
- `templates/templates.md` & `templates/subcomponents/templates-context.md`: Prompt templates, subcomponents, and detailed prompting techniques with examples.
- `metadata.md`: System metadata, author, version, and project description.
- `changelog.md`: Tracks all significant changes and version history.
- `glossary.md`: Defines key terms and concepts for prompt engineering.
- `contributing.md`: Guidelines for contributing to the project.

## Core Workflow (from `main_instruction.md`)

1. **Task Selection**: Choose the prompt task (Create, Enhance, Modify, Custom, Agent, or /auto). The system supports both shortcut keys and free-form mapping.
2. **Format Selection**: Select the desired prompt format (plain text, JSON, YAML, markdown, etc.), or use `/auto` for automatic selection.
3. **Technique Selection**: Choose prompt engineering techniques (e.g., Zero-shot, Few-shot, Chain-of-Thought, etc.), or `/auto`.
4. **Paradigm Selection**: Select the paradigm (Agent-based, Reasoning-based, Symbolic/GOFAI, etc.), or `/auto`.
5. **Save/Commit**: Use `/save` or `/commit` to persist your workflow state for the current chat session.
6. **Iterative Improvement**: The system supports feedback-driven refinement and multiple-choice feedback collection.
7. **Documentation**: All prompt choices and results are output in code blocks for clarity and traceability.

## Context & Best Practices (from `context/context.md`)

- Use the latest, most capable models for best results.
- Place instructions at the beginning of prompts and use clear separators.
- Be specific and detailed about context, outcome, format, and style.
- Articulate output format through examples.
- Start with zero-shot, then few-shot, then fine-tune if needed.
- Reduce imprecise descriptions and always specify what to do instead of what not to do.
- Use leading words for code generation and provide explicit format requirements.

### Supported Formats

- XML, JSON, YAML, Markdown, Table (Markdown Table), CSV, INI

### Supported Paradigms

- Agent-based, Reasoning-based, Symbolic (Classic/GOFAI)

### Prompt Engineering Techniques

- Zero-shot, Few-shot, Chain-of-Thought, Meta Prompting, Self-Consistency, Generate Knowledge, Prompt Chaining, Tree of Thoughts, Retrieval Augmented Generation, Automatic Reasoning and Tool-use, Automatic Prompt Engineer, Active-Prompt, Directional Stimulus Prompting, Program-Aided Language Models, ReAct, Reflexion, Multimodal CoT, Graph Prompting, and more (see templates and context for details).

## Commands (from `commands/commands.md`)

The system supports a rich set of commands for managing prompts, templates, context, profiles, and workflow. Key commands include:

- `/save` or `/commit`: Save current workflow state for the session.
- `/create`, `/modify`, `/delete`: Manage prompts, templates, commands, or context entries.
- `/validate`: Check structure and content for correctness.
- `/auto`: Let the system choose the best options.
- `/init`, `/start`, `/help`: Display commands, agent info, and help.
- `/templates`, `/context`, `/glossary`, `/metadata`, `/reference`, `/format`, `/paradigm`, `/agent`, `/examples`, `/readme`, `/update`, `/history`, `/profile`, `/show_changelog`, `/list_commands`, `/search [keyword]`, `/about`, `/version`.

See `commands/commands.md` for the full list and descriptions.

## Profiles (from `profiles/profile.md`)

Profiles define reusable configurations for agent behavior and prompt generation. Each profile specifies task, format, technique, and paradigm, supporting both auto and explicit settings. Example profiles:

- `agent_basic_auto`: All steps set to auto.
- `create_zero_shot_json`: Create task, JSON format, Zero-shot technique, Reasoning-based paradigm.
- `enhance_few_shot_markdown`: Enhance task, Markdown format, Few-shot technique, Agent-based paradigm.

See `profiles/profile.md` for more.

## Templates & Subcomponents

Templates define reusable prompt structures and techniques. Subcomponents provide detailed examples and advanced prompting strategies. See `templates/templates.md` and `templates/subcomponents/templates-context.md` for:

- Prompting techniques (Zero-shot, Few-shot, CoT, etc.)
- Format examples (JSON, YAML, Markdown, etc.)
- Paradigm and technique options

## Glossary

See `glossary.md` for definitions of key terms: Agent, Command, Context, Instruction, Template, Metadata, Changelog, Single Source of Truth, Cross-file Consistency, Prompt, Prompt Engineering, Format, Few-shot Prompting, Zero-shot Prompting, Chain-of-Thought, and more.

## Versioning & Changelog

All significant changes are tracked in `changelog.md`. Use this file to review project history and updates.

## Contributing

See `contributing.md` for guidelines on contributing to the project.

---


---

## Demo Implementation

Try the live Custom GPT version on OpenAI:

[Prompt Engineer / Prompt Generator (Custom GPT Demo)](https://chatgpt.com/g/g-6793426c310481918c97dee7c62ab764-prompt-engineer-prompt-generator)

For more details, see the referenced markdown files above. This README is a high-level entry point; always consult the individual files for specifics and updates.
