{
  "chatgpt": "https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api",
  "instructions": [
    {
      "title": "Use the latest model",
      "description": "For best results, use the latest, most capable models. Newer models tend to be easier to prompt engineer. Note differences when prompting reasoning models versus GPT models."
    },
    {
      "title": "Put instructions at the beginning of the prompt and use ### or \"\"\" to separate the instruction and context",
      "less_effective_example": "Summarize the text below as a bullet point list of the most important points.\n\n{text input here}",
      "better_example": "Summarize the text below as a bullet point list of the most important points.\n\nText: \"\"\"\n{text input here}\n\"\"\""
    },
    {
      "title": "Be specific, descriptive and as detailed as possible about the desired context, outcome, length, format, style, etc",
      "description": "Specify the context, desired outcome, length, format, style, etc.",
      "less_effective_example": "Write a poem about OpenAI.",
      "better_example": "Write a short inspiring poem about OpenAI, focusing on the recent DALL-E product launch (DALL-E is a text to image ML model) in the style of a {famous poet}."
    },
    {
      "title": "Articulate the desired output format through examples",
      "description": "Show specific format requirements, making outputs easier to parse.",
      "less_effective_example": "Extract the entities mentioned in the text below. Extract the following 4 entity types: company names, people names, specific topics and themes.\n\nText: {text}",
      "better_example": "Extract the important entities mentioned in the text below. First extract all company names, then extract all people names, then extract specific topics which fit the content and finally extract general overarching themes\n\nDesired format:\nCompany names: <comma_separated_list_of_company_names>\nPeople names: -||-\nSpecific topics: -||-\nGeneral themes: -||-\n\nText: {text}"
    },
    {
      "title": "Start with zero-shot, then few-shot, if neither works, then fine-tune",
      "steps": [
        {
          "type": "Zero-shot",
          "example": "Extract keywords from the below text.\n\nText: {text}\n\nKeywords:"
        },
        {
          "type": "Few-shot",
          "example": "Extract keywords from the corresponding texts below.\n\nText 1: Stripe provides APIs that web developers can use to integrate payment processing into their websites and mobile applications.\nKeywords 1: Stripe, payment processing, APIs, web developers, websites, mobile applications\n##\nText 2: OpenAI has trained cutting-edge language models that are very good at understanding and generating text. Our API provides access to these models and can be used to solve virtually any task that involves processing language.\nKeywords 2: OpenAI, language models, text processing, API.\n##\nText 3: {text}\nKeywords 3:"
        },
        {
          "type": "Fine-tune",
          "note": "See fine-tune best practices here."
        }
      ]
    },
    {
      "title": "Reduce “fluffy” and imprecise descriptions",
      "less_effective_example": "The description for this product should be fairly short, a few sentences only, and not too much more.",
      "better_example": "Use a 3 to 5 sentence paragraph to describe this product."
    },
    {
      "title": "Instead of just saying what not to do, say what to do instead",
      "less_effective_example": "The following is a conversation between an Agent and a Customer. DO NOT ASK USERNAME OR PASSWORD. DO NOT REPEAT.\n\nCustomer: I can’t log in to my account.\nAgent:",
      "better_example": "The following is a conversation between an Agent and a Customer. The agent will attempt to diagnose the problem and suggest a solution, whilst refraining from asking any questions related to PII. Instead of asking for PII, such as username or password, refer the user to the help article www.samplewebsite.com/help/faq\n\nCustomer: I can’t log in to my account.\nAgent:"
    },
    {
      "title": "Code Generation Specific - Use “leading words” to nudge the model toward a particular pattern",
      "description": "Provide hints like 'import' for Python or 'SELECT' for SQL.",
      "less_effective_example": "# Write a simple python function that\n# 1. Ask me for a number in mile\n# 2. It converts miles to kilometers",
      "better_example": "# Write a simple python function that\n# 1. Ask me for a number in mile\n# 2. It converts miles to kilometers"
    }
  ],
  "formats": [
    {
      "name": "XML",
      "description": "Standard for structured, machine-readable prompts, useful for hierarchical data and configuration.",
      "reference": "https://www.w3.org/XML/"
    },
    {
      "name": "JSON",
      "description": "Widely used for structured prompts in APIs and LLM integrations, enabling easy parsing and validation.",
      "reference": "https://www.ecma-international.org/publications-and-standards/standards/ecma-404/"
    },
    {
      "name": "YAML",
      "description": "Readable, hierarchical prompts, common in configuration and some LLM frameworks.",
      "reference": "https://yaml.org/"
    },
    {
      "name": "Markdown",
      "description": "Used for prompts requiring rich text formatting or documentation-style instructions.",
      "reference": "https://www.markdownguide.org/"
    },
    {
      "name": "Table (Markdown Table)",
      "description": "Used for structured data, comparison tasks, or presenting options in prompts.",
      "reference": "https://cookbook.openai.com/examples/how_to_format_data_for_table_generation"
    },
    {
      "name": "CSV",
      "description": "Standard for tabular data, useful for batch processing and data ingestion in LLM workflows.",
      "reference": "https://datatracker.ietf.org/doc/html/rfc4180"
    },
    {
      "name": "INI",
      "description": "Simple key-value configuration format, occasionally used for config-style prompts.",
      "reference": "https://en.wikipedia.org/wiki/INI_file"
    }
  ],
  "case_study_prompt_modifications": {
  },
  "paradigms": [
    {
      "name": "Agent-based",
      "description": "Treats the AI as an autonomous agent that perceives, reasons, and acts in an environment to achieve goals. Useful for planning, tool use, or interaction.",
      "reference": "https://www.promptingguide.ai/research/llm-agents"
    },
    {
      "name": "Reasoning-based",
      "description": "Focuses on logical inference, step-by-step problem solving, and explicit reasoning chains. Ideal for tasks needing transparency and explainability."
    },
    {
      "name": "Symbolic (Classic/GOFAI)",
      "description": "Uses explicit rules, logic, and symbolic representations. Best for structured, rule-driven tasks and traditional AI workflows."
    }
  ]
    "description": "The following prompt modification techniques are based on findings from the Graduate Job Classification Case Study. See: https://www.promptingguide.ai/applications/workplace_casestudy",
    "techniques": [
      "Raw Instruction (rawinst): Add explicit instructions about the model’s role and the task directly in the user message.",
      "System Instruction (sysinst): Place instructions about the model’s role and the task in the system message (if supported).",
      "Both Instructions (bothinst): Split instructions, putting the role in the system message and the task in the user message.",
      "Mock Discussion (mock): Present the task as part of a mock conversation, where the model acknowledges the instructions before proceeding.",
      "Reinforcement (reit): Reinforce key elements in the instructions by repeating them within the prompt.",
      "Strict Template (strict): Instruct the model to strictly follow a specific output template or format.",
      "Loose Template (loose): Ask the model to provide only the final answer, following a minimal template.",
      "Right Answer (right): Directly ask the model to reach the correct or 'right' conclusion.",
      "Additional Info (info): Provide additional information or context to address common reasoning failures or ambiguities.",
      "Model Name (name): Assign a human-like name to the model and refer to it by that name in the prompt.",
      "Positive Feedback (pos): Give the model positive feedback or encouragement before presenting the main query."
    ]
  }
}


