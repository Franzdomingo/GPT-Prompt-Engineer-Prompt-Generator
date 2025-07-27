<?xml version="1.0" encoding="UTF-8"?>
<profiles>
  <profile name="agent_basic_auto">
    <param>task=auto</param>
    <param>format=auto</param>
    <param>technique=auto</param>
    <param>paradigm=auto</param>
  </profile>
  <profile name="agent_instruction_auto">
    <param>task=Agent</param>
    <param>instruction=auto</param>
    <param>format=auto</param>
    <param>technique=auto</param>
    <param>paradigm=auto</param>
  </profile>
  <profile name="create_zero_shot_json">
    <param>task=Create</param>
    <param>format=JSON</param>
    <param>technique=Zero-shot Prompting</param>
    <param>paradigm=Reasoning-based</param>
  </profile>
  <profile name="enhance_few_shot_markdown">
    <param>task=Enhance</param>
    <param>format=Markdown</param>
    <param>technique=Few-shot Prompting</param>
    <param>paradigm=Agent-based</param>
  </profile>
  <profile name="modify_chain_of_thought_yaml">
    <param>task=Modify</param>
    <param>format=YAML</param>
    <param>technique=Chain-of-Thought Prompting</param>
    <param>paradigm=Reasoning-based</param>
  </profile>
  <profile name="custom_rag_csv">
    <param>task=Custom</param>
    <param>format=CSV</param>
    <param>technique=Retrieval Augmented Generation</param>
    <param>paradigm=Agent-based</param>
  </profile>
  <profile name="agent_strict_template_xml">
    <param>task=Agent</param>
    <param>format=XML</param>
    <param>technique=Strict Template</param>
    <param>paradigm=Symbolic (Classic/GOFAI)</param>
  </profile>
  <profile name="agent_reflexion_ini">
    <param>task=Agent</param>
    <param>format=INI</param>
    <param>technique=Reflexion</param>
    <param>paradigm=Reasoning-based</param>
  </profile>
  <profile name="agent_react_table">
    <param>task=Agent</param>
    <param>format=Table (Markdown Table)</param>
    <param>technique=ReAct</param>
    <param>paradigm=Agent-based</param>
  </profile>
  <profile name="agent_meta_prompting_json">
    <param>task=Agent</param>
    <param>format=JSON</param>
    <param>technique=Meta Prompting</param>
    <param>paradigm=Reasoning-based</param>
  </profile>
  <profile name="agent_raw_basic_classics">
    <param>task=Agent</param>
    <param>format=Text</param>
    <param>technique=Raw Prompting</param>
    <param>paradigm=Classic</param>
  </profile>
</profiles>
