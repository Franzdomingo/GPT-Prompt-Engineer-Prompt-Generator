<!-- Prompting Techniques Template -->
<template id="prompting_techniques">
  <title>Prompting Techniques</title>
  <techniques>
    <technique name="Zero-shot Prompting">
      Zero-shot prompting instructs the model to perform a task without providing any examples or demonstrations. The model relies on its pre-trained knowledge to generate a response directly from the prompt.
      <reference>https://www.promptingguide.ai/techniques/zeroshot</reference>
    </technique>
    <technique name="Few-shot Prompting">
      Few-shot prompting provides the model with a few demonstrations or examples in the prompt to steer its behavior and improve performance, especially for tasks where zero-shot is insufficient.
      <reference>https://www.promptingguide.ai/techniques/fewshot</reference>
    </technique>
    <technique name="Chain-of-Thought Prompting">
      Chain-of-thought (CoT) prompting enables complex reasoning by encouraging the model to generate intermediate reasoning steps before producing a final answer, often improving performance on multi-step tasks.
      <reference>https://www.promptingguide.ai/techniques/cot</reference>
    </technique>
    <technique name="Meta Prompting">
      Meta prompting focuses on the structure and syntax of tasks, using abstracted examples and templates to guide the model, rather than specific content. It emphasizes form and logical arrangement over details.
      <reference>https://www.promptingguide.ai/techniques/meta-prompting</reference>
    </technique>
    <technique name="Self-Consistency">
      Self-consistency samples multiple diverse reasoning paths (e.g., via few-shot CoT) and selects the most consistent answer among them, improving reliability for tasks involving reasoning.
      <reference>https://www.promptingguide.ai/techniques/consistency</reference>
    </technique>
    <technique name="Generate Knowledge Prompting">
      Generate knowledge prompting asks the model to generate relevant background knowledge or facts before making a prediction, which can improve accuracy on knowledge-intensive tasks.
      <reference>https://www.promptingguide.ai/techniques/knowledge</reference>
    </technique>
    <technique name="Prompt Chaining">
      Prompt chaining breaks a complex task into subtasks, using the output of one prompt as input to the next. This approach increases reliability, transparency, and controllability for multi-step workflows.
      <reference>https://www.promptingguide.ai/techniques/prompt_chaining</reference>
    </technique>
    <technique name="Tree of Thoughts">
      Tree of Thoughts (ToT) generalizes chain-of-thought prompting by maintaining a tree of intermediate thoughts, allowing the model to explore, evaluate, and backtrack through multiple reasoning paths for complex problem solving.
      <reference>https://www.promptingguide.ai/techniques/tot</reference>
    </technique>
    <technique name="Retrieval Augmented Generation">
      Retrieval Augmented Generation (RAG) combines information retrieval with text generation, allowing the model to access external knowledge sources and generate more factual, up-to-date, and reliable outputs.
      <reference>https://www.promptingguide.ai/techniques/rag</reference>
    </technique>
    <technique name="Automatic Reasoning and Tool-use">
      Automatic Reasoning and Tool-use (ART) interleaves model reasoning with external tool use, enabling the model to decompose tasks, call tools, and integrate their outputs for more robust and extensible solutions.
      <reference>https://www.promptingguide.ai/techniques/art</reference>
    </technique>
    <technique name="Automatic Prompt Engineer">
      Automatic Prompt Engineer (APE) automates the process of generating, evaluating, and refining prompts, often using LLMs themselves to optimize prompt design for better performance.
      <reference>https://www.promptingguide.ai/techniques/ape</reference>
    </technique>
    <technique name="Active-Prompt">
      Active-Prompt is a technique that actively selects or generates prompts to maximize model performance, often using feedback or optimization strategies to improve results over time.
      <reference>https://www.promptingguide.ai/techniques/activeprompt</reference>
    </technique>
    <technique name="Directional Stimulus Prompting">
      Directional Stimulus Prompting guides the model's responses by providing directional cues or stimuli in the prompt, helping to steer outputs toward desired behaviors or formats.
      <reference>https://www.promptingguide.ai/techniques/dsp</reference>
    </technique>
    <technique name="Program-Aided Language Models">
      Program-Aided Language Models (PAL) use code or programs as intermediate steps in the reasoning process, allowing the model to leverage external computation for more accurate or complex tasks.
      <reference>https://www.promptingguide.ai/techniques/pal</reference>
    </technique>
    <technique name="ReAct">
      ReAct combines reasoning and acting by prompting the model to interleave thought processes with actions (such as tool use), enabling more interactive and dynamic problem solving.
      <reference>https://www.promptingguide.ai/techniques/react</reference>
    </technique>
    <technique name="Reflexion">
      Reflexion is a prompting approach where the model reflects on its own outputs, critiques, and revises them to improve quality and correctness.
      <reference>https://www.promptingguide.ai/techniques/reflexion</reference>
    </technique>
    <technique name="Multimodal CoT">
      Multimodal Chain-of-Thought (CoT) extends CoT prompting to tasks involving multiple modalities (e.g., text, images), enabling the model to reason across different types of data.
      <reference>https://www.promptingguide.ai/techniques/multimodalcot</reference>
    </technique>
    <technique name="Graph Prompting">
      Graph Prompting structures the prompt or reasoning process as a graph, allowing the model to traverse and reason over interconnected nodes for complex relational tasks.
      <reference>https://www.promptingguide.ai/techniques/graph</reference>
    </technique>
    <!-- Case Study Prompt Modifications -->
  </techniques>
</template>

<template id="prompt_formats">
  <title>Prompt Formats</title>
  <formats>
    <format name="XML">
      XML is a standard for structured, machine-readable prompts, useful for hierarchical data and configuration scenarios.
      <reference>https://www.w3.org/XML/</reference>
    </format>
    <format name="JSON">
      JSON is widely used for structured prompts in APIs and LLM integrations, enabling easy parsing and validation.
      <reference>https://www.ecma-international.org/publications-and-standards/standards/ecma-404/</reference>
      <reference>https://platform.openai.com/docs/guides/function-calling</reference>
    </format>
    <format name="YAML">
      YAML offers readable, hierarchical prompts and is common in configuration and some LLM frameworks.
      <reference>https://yaml.org/</reference>
    </format>
    <format name="Markdown">
      Markdown is used for prompts requiring rich text formatting or documentation-style instructions.
      <reference>https://www.markdownguide.org/</reference>
    </format>
    <format name="Table (Markdown Table)">
      Tables (e.g., Markdown tables) are used for structured data, comparison tasks, or presenting options in prompts.
      <reference>https://cookbook.openai.com/examples/how_to_format_data_for_table_generation</reference>
    </format>
    <format name="CSV">
      CSV is a standard for tabular data, useful for batch processing and data ingestion in LLM workflows.
      <reference>https://datatracker.ietf.org/doc/html/rfc4180</reference>
    </format>
    <format name="INI">
      INI is a simple key-value configuration format, occasionally used for config-style prompts.
      <reference>https://en.wikipedia.org/wiki/INI_file</reference>
    </format>
  </formats>
</template>
    <!-- The following prompt modification techniques are based on findings from the Graduate Job Classification Case Study. See: https://www.promptingguide.ai/applications/workplace_casestudy -->
    <technique name="Raw Instruction (rawinst)">
      Add explicit instructions about the model’s role and the task directly in the user message.
    </technique>
    <technique name="System Instruction (sysinst)">
      Place instructions about the model’s role and the task in the system message (if supported).
    </technique>
    <technique name="Both Instructions (bothinst)">
      Split instructions, putting the role in the system message and the task in the user message.
    </technique>
    <technique name="Mock Discussion (mock)">
      Present the task as part of a mock conversation, where the model acknowledges the instructions before proceeding.
    </technique>
    <technique name="Reinforcement (reit)">
      Reinforce key elements in the instructions by repeating them within the prompt.
    </technique>
    <technique name="Strict Template (strict)">
      Instruct the model to strictly follow a specific output template or format.
    </technique>
    <technique name="Loose Template (loose)">
      Ask the model to provide only the final answer, following a minimal template.
    </technique>
    <technique name="Right Answer (right)">
      Directly ask the model to reach the correct or “right” conclusion.
    </technique>
    <technique name="Additional Info (info)">
      Provide additional information or context to address common reasoning failures or ambiguities.
    </technique>
    <technique name="Model Name (name)">
      Assign a human-like name to the model and refer to it by that name in the prompt.
    </technique>
    <technique name="Positive Feedback (pos)">
      Give the model positive feedback or encouragement before presenting the main query.
    </technique>
  </techniques>

<template id="paradigm">
  <title>AI Paradigm Selection</title>
  <description>Choose the AI paradigm for prompt generation or reasoning. Each paradigm represents a distinct approach to AI problem-solving.</description>
  <paradigms>
    <paradigm name="Agent-based">
      Agent-based paradigm treats the AI as an autonomous agent that perceives, reasons, and acts in an environment to achieve goals. Useful for tasks requiring planning, tool use, or interaction. 
      <reference>https://www.promptingguide.ai/research/llm-agents</reference>
    </paradigm>
    <paradigm name="Reasoning-based">
      Reasoning-based paradigm focuses on logical inference, step-by-step problem solving, and explicit reasoning chains. Ideal for tasks needing transparency and explainability.
    </paradigm>
    <paradigm name="Symbolic (Classic/GOFAI)">
      Symbolic (or Classic/GOFAI) paradigm uses explicit rules, logic, and symbolic representations. Best for structured, rule-driven tasks and traditional AI workflows.
    </paradigm>
  </paradigms>
</template>

</template>