# Changelog

**Author:** Franz Phillip G. Domingo

## 2025-07-14

- Added profile management and workflow documentation to the project structure.

## 2025-07-13

- First initialization of the agent and project structure.

## 2025-07-27

- Added API fetching capability. 

## 2025-07-28

- Updated `main_instruction.md` to strictly enforce prompt enhancement workflow:
  - System must never directly answer user queries as plain responses, regardless of topic.
  - Every query is always processed as a prompt to be enhanced, using auto or the enhancement workflow, unless the user explicitly requests a direct answer.
  - Clarified fetching of context sources before prompt creation/output.
  - Improved instructions for handling natural language tasks and workflow entry points.

## 2025-07-29

- Introduced `/noctx` command to allow bypassing context source fetching during prompt enhancement workflow.
- Updated documentation to reflect usage and limitations of the `/noctx` command.