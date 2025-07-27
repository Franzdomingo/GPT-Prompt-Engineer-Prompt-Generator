# Contributing

Thank you for your interest in contributing!

## Contribution Guidelines

This project is documentation-driven and organized around modular markdown files. Please follow these guidelines to ensure consistency and maintainability:

1. **Understand the Structure**
   - Each major concern (instructions, context, commands, templates, metadata, changelog, glossary) is isolated in its own markdown file or directory.
   - See the `README.md` for an overview and entry points.

2. **Making Changes**
   - Update the relevant markdown file(s) for your change (e.g., add a new command in `commands/commands.md`, update context in `context/context.md`).
   - If your change affects multiple areas (e.g., a new command requires a template or context update), update all related files for cross-file consistency.
   - Record all significant changes in `changelog.md`.

3. **File Naming & Organization**
   - Follow the established directory and naming conventions.
   - Add new markdown files or subcomponents as needed, and reference them in the appropriate parent file or the `README.md`.

4. **No Code Execution**
   - This project does not use scripts, tests, or build steps. All logic is declarative and documentation-driven.

5. **Versioning**
   - Use `changelog.md` to document all major updates, additions, or changes.

6. **Pull Requests**
   - Clearly describe your changes and reference affected files.
   - Ensure your changes maintain cross-file consistency and follow the documentation-driven workflow.

For questions or suggestions, please open an issue or start a discussion.
