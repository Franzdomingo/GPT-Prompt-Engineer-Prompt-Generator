<commands>
  <command name="/save | /commit">
    <description>Save the current set of selected choices (task type, format, techniques, paradigm, etc.) for future use or reference within this chat conversation with the agent. Use this command to persist your workflow state and easily resume or reuse your configuration. Note: Saving is only valid for the current chat session and will not persist across new conversations. '/commit' is an alternative name for this action.</description>
  </command>
  <command name="/create">
    <description>Create a new prompt, template, or context entry. Specify the type and details to generate new content or configuration.</description>
  </command>
  <command name="/modify">
    <description>Modify an existing prompt, template, command, or context entry. Provide the target and the changes to apply updates.</description>
  </command>
  <!-- Suggested additional commands for enhanced workflow: -->
  <command name="/delete">
    <description>Delete a prompt, template, command, or context entry by specifying its name or identifier.</description>
  </command>
  <command name="/validate">
    <description>Validate the structure and content of prompts, templates, or context entries to ensure correctness and consistency.</description>
  </command>
  <command name="/auto">
    <description>Let the system automatically select the best format, techniques, and paradigm for prompt engineering. Use this command as an option wherever format, techniques, or paradigm selection is required.</description>
  </command>
  <command name="/init | /start">
    <description>Displays all commands and a brief description of the agent.</description>
  </command>
  <command name="/templates">
    <description>Display all templates.</description>
  </command>
  <command name="/context">
    <description>Display the current domain-specific context and background information.</description>
  </command>
  <command name="/help">
    <description>Show all available commands with descriptions. Use this command to get a comprehensive help message, including usage examples and tips for interacting with the system. The help output should summarize each command, its purpose, and any special usage notes.</description>
  </command>
  <command name="/list_commands">
    <description>List all defined commands.</description>
  </command>
  <command name="/show_changelog">
    <description>Display recent changes from changelog.md.</description>
  </command>
  <command name="/glossary">
    <description>Show glossary terms and definitions.</description>
  </command>
  <command name="/contribute">
    <description>Display contribution guidelines.</description>
  </command>
  <command name="/metadata">
    <description>Show system metadata and version info.</description>
  </command>
  <command name="/reference">
    <description>Show cross-file references and relationships.</description>
  </command>
  <command name="/format">
    <description>Display all supported prompt formats (e.g., JSON, XML, YAML, Markdown, Table, CSV, INI) and their references. Use /auto to let the system choose the best format automatically except for paradigm</description>
  </command>
  <command name="/about">
    <description>Show a summary of the system’s purpose and architecture.</description>
  </command>
  <command name="/version">
    <description>Display the current version and last update date.</description>
  </command>
  <command name="/paradigm">
    <description>Choose the AI paradigm for prompt generation or reasoning. Options: Agent-based, Reasoning-based, Symbolic (Classic/GOFAI). Use /auto to let the system choose the best paradigm automatically.</description>
  </command>
  <command name="/agent">
    <description>Specify an agent-specific action. When using this command, you will be prompted to clarify whether your request is an "agent instruction" (to change agent behavior or configuration) or a "task" (to assign a job for the agent to perform).</description>
  </command>
  <command name="/search [keyword]">
    <description>Search for a keyword across all documentation files.</description>
  </command>
  <command name="/examples">
    <description>List example prompts or template usages.</description>
  </command>
  <command name="/readme">
    <description>Show the README summary and entry points.</description>
  </command>
  <command name="/update">
    <description>Show the latest update instructions or workflow steps for extending the system.</description>
  </command>
  <command name="/history">
    <description>Show a brief history of major changes (from changelog.md).</description>
  </command>
</commands>
  <command name="/profile">
    <description>List all available profiles, choose a profile to load, or create a new profile. Use this command to manage agent and workflow profiles for prompt engineering tasks.</description>
  </command>
</commands>

