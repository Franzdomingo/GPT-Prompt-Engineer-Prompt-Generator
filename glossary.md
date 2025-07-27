# Glossary

**Agent**: The automated system (e.g., GitHub Copilot) that manages prompt engineering tasks and documentation updates.

**Command**: A defined action or instruction, described in `commands/commands.md`, that the agent can execute as part of the prompt engineering workflow.

**Context**: Domain-specific background or information, maintained in `context/context.md`, used to inform prompt generation and refinement.

**Instruction**: A directive or rule, often found in `main_instruction.md`, that guides the agent's behavior.

**Template**: A reusable prompt structure, defined in `templates/templates.md` and related files, used to standardize prompt generation.

**Metadata**: System-level information about the project, stored in `metadata.md`.

**Changelog**: A record of significant changes to the system, maintained in `changelog.md`.

**Single Source of Truth**: The practice of keeping each major concern isolated in its own markdown file for clarity and maintainability.

**Cross-file Consistency**: The requirement to update related files when changes are made to commands, templates, or context.
<!-- Glossary -->
<glossary>
  <term name="Prompt">
    <definition>A text input or instruction given to a language model to elicit a specific response or behavior.</definition>
  </term>
  <term name="Prompt Engineering">
    <definition>The practice of designing, refining, and optimizing prompts to achieve desired outputs from language models.</definition>
  </term>
  <term name="Format">
    <definition>The structural syntax (e.g., JSON, XML, YAML) used to organize and present prompts or data.</definition>
  </term>
  <term name="Template">
    <definition>A reusable pattern or example, often in a specific format, that guides the creation of prompts.</definition>
  </term>
  <term name="Few-shot Prompting">
    <definition>Providing a language model with a few examples in the prompt to guide its behavior.</definition>
  </term>
  <term name="Zero-shot Prompting">
    <definition>Prompting a language model to perform a task without providing any examples.</definition>
  </term>
  <term name="Chain-of-Thought (CoT)">
    <definition>A prompting technique that encourages the model to generate intermediate reasoning steps before producing a final answer.</definition>
  </term>
  <term name="RAG (Retrieval Augmented Generation)">
    <definition>A method that combines information retrieval with text generation to improve factual accuracy and reliability.</definition>
  </term>
  <term name="Fine-tuning">
    <definition>The process of training a pre-trained language model on additional data to specialize it for specific tasks or domains.</definition>
  </term>
</glossary>

<!-- Extended Glossary: Additional Prompt Engineering Terms -->
<glossary>
  <term name="Chain-of-Thought Prompting">
    <definition>A prompting technique that enables complex reasoning by encouraging the model to generate intermediate reasoning steps before producing a final answer.</definition>
  </term>
  <term name="Meta Prompting">
    <definition>A technique focusing on the structure and syntax of tasks, using abstracted examples and templates to guide the model, emphasizing form and logical arrangement over details.</definition>
  </term>
  <term name="Self-Consistency">
    <definition>A method that samples multiple diverse reasoning paths (e.g., via few-shot CoT) and selects the most consistent answer among them, improving reliability for reasoning tasks.</definition>
  </term>
  <term name="Generate Knowledge Prompting">
    <definition>A technique where the model is asked to generate relevant background knowledge or facts before making a prediction, improving accuracy on knowledge-intensive tasks.</definition>
  </term>
  <term name="Prompt Chaining">
    <definition>A method that breaks a complex task into subtasks, using the output of one prompt as input to the next, increasing reliability and transparency for multi-step workflows.</definition>
  </term>
  <term name="Tree of Thoughts (ToT)">
    <definition>A prompting approach that generalizes chain-of-thought by maintaining a tree of intermediate thoughts, allowing exploration and evaluation of multiple reasoning paths for complex problem solving.</definition>
  </term>
  <term name="Automatic Reasoning and Tool-use (ART)">
    <definition>A technique that interleaves model reasoning with external tool use, enabling decomposition of tasks and integration of tool outputs for robust solutions.</definition>
  </term>
  <term name="Automatic Prompt Engineer (APE)">
    <definition>A process that automates generating, evaluating, and refining prompts, often using LLMs themselves to optimize prompt design for better performance.</definition>
  </term>
  <term name="Active-Prompt">
    <definition>A prompting method that dynamically adapts prompts or instructions based on model feedback or intermediate results to improve task performance.</definition>
  </term>
  <term name="XML Prompt Format">
    <definition>A prompt format using XML syntax to structure instructions and data for language models.</definition>
  </term>
  <term name="JSON Prompt Format">
    <definition>A prompt format using JSON syntax to organize and present instructions and data for language models.</definition>
  </term>
  <term name="YAML Prompt Format">
    <definition>A prompt format using YAML syntax for structuring prompts and data for language models.</definition>
  </term>
  <term name="Markdown Prompt Format">
    <definition>A prompt format using Markdown syntax to structure instructions, context, or examples for language models.</definition>
  </term>
  <term name="Table Prompt Format">
    <definition>A prompt format using tables (often Markdown tables) to organize data or instructions for language models.</definition>
  </term>
  <term name="CSV Prompt Format">
    <definition>A prompt format using CSV (comma-separated values) to structure data for language models.</definition>
  </term>
  <term name="INI Prompt Format">
    <definition>A prompt format using INI file syntax to organize configuration-like instructions or data for language models.</definition>
  </term>
</glossary>
</glossary>
