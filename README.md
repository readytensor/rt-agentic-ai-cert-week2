# Ready Tensor Agentic AI Certification - Week 2

This repository contains the lessons, practical code and exercises for **Week 2** of the [Agentic AI Developer Certification Program](https://app.readytensor.ai/publications/HrJ0xWtLzLNt) by Ready Tensor, covering foundational prompt engineering concepts that are essential for building effective agentic AI systems.

## What You'll Learn

- How to build **modular prompts** for better clarity and reuse
- When and how to apply **reasoning techniques** like CoT, ReAct, and Self-Ask
- Strategies for **structured output parsing**
- Principles of **function chaining** in AI workflows
- How **vector databases** enable semantic search
- Foundations of **Retrieval-Augmented Generation (RAG)**

---

## Lessons in This Repository

### 0. Getting Started: Free APIs and Local LLMs

Set up your environment with free LLM options — including cloud APIs like Groq and Google Gemini, or local models via Ollama — so you can follow the course without hitting cost barriers.

### 1a. Building Prompts for Agentic AI Systems

Learn how to design effective prompts using modular components — instruction, tone, role, constraints — and how to iteratively refine prompts for clarity and consistency.

### 1b. Prompt Engineering: Advanced Reasoning Techniques

Covers three powerful techniques — **Chain of Thought**, **ReAct**, and **Self-Ask** — and shows how to incorporate them into your modular prompt framework.

### 2. From Text to Data: Hands-On LLM Output Parsing

Explore structured output generation from LLMs using prompt formatting and model-native methods, with tools like **Pydantic** and **LangChain**.

### 3. Function Chaining for Intelligent Pipelines

Understand how breaking down tasks into smaller functions enables composable, robust AI systems, and how to structure chains for clarity and reliability.

### 4a. Vector Databases: Finding Meaning, Not Just Keywords

Get introduced to vector search and how embeddings power semantic retrieval in intelligent systems.

### 4b. Vector Databases: Building a Semantic Retrieval System

Build a working pipeline with **ChromaDB**, embeddings, and chunked documents — the foundation of modern RAG workflows.

### 5. Introduction to RAG (Retrieval Augmented Generation)

Learn why RAG outperforms fine-tuning for most real-world scenarios, and how it enables domain-specific, knowledge-grounded assistants.

## Repository Structure

```
rt-agentic-ai-cert-week2/
├── code/
│   ├── config/
│   │   ├── config.yaml          # App config with reasoning strategies
│   │   └── prompt_config.yaml   # Prompt configurations for examples
│   ├── lesson_1a_and_ab.py      # Main script for lesson 1
│   ├── lesson_2.py      # Main script for lesson 2
│   ├── paths.py                 # File path configurations
│   ├── prompt_builder.py        # Modular prompt construction functions
│   └── utils.py                 # Utility functions
├── data/
│   └── vae-publication.md       # Sample publication for exercises
├── lessons/
│   └── lesson-wk2-*             # Markdown files and visuals for each lesson
├── outputs/                     # Generated prompts and LLM responses
├── .env.template                # Environment variables template
├── requirements.txt             # Python dependencies
└── README.md
```

## Installation & Setup

1. **Clone the repository:**

   ```bash
   git clone https://github.com/readytensor/rt-agentic-ai-cert-week2.git
   cd rt-agentic-ai-cert-week2
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your API key:**

   Create a .env file in the root directory and add at least one API key. **You need at least one key** from OpenAI, Groq, or Google to run the examples.

   See [.env.example](https://github.com/readytensor/rt-agentic-ai-cert-week2/blob/main/.env.example) file for the complete template.

   ```bash
   # Choose at least one (you don't need all three)
   OPENAI_API_KEY=your-openai-key-here
   GROQ_API_KEY=your-groq-key-here
   GOOGLE_API_KEY=your-google-key-here
   ```

   **Get your free API key from:**

   - **OpenAI** (paid): [platform.openai.com/api-keys](https://platform.openai.com/api-keys)
   - **Groq** (free): [console.groq.com](https://console.groq.com)
   - **Google Gemini** (free): [makersuite.google.com](https://makersuite.google.com)

   > 💡 **No budget for APIs?** Check out our [Free API Setup Guide](lessons/lesson-wk2-l0/w2-l0-getting-started-free-apis.md) for using Groq and Google's free tiers!

4. **Run the examples:**
   ```bash
   cd code
   python lesson_1a_and_1b.py
   ```
   **Customize your experiments:** Edit the `prompt_cfg_key` variable in `lesson_1_and_2.py` (near the bottom of the script) to test different prompt configurations (e.g., `summarization_prompt_cfg1` through `summarization_prompt_cfg6`). You can also create new configurations in `config/prompt_config.yaml` to experiment with your own prompt designs.

## Key Features

- 🧩 **Modular Prompt Builder**
  Construct prompts from reusable components like role, constraints, tone, and goals.

- 🧠 **Reasoning Techniques**
  Integrate CoT, ReAct, and Self-Ask patterns into your prompts with a single config line.

- 🛠️ **Hands-On Output Parsing**
  Generate and validate structured output using both prompt-based and model-native methods.

- 🔗 **Function Chaining Framework**
  Chain modular steps to build robust, maintainable AI pipelines.

- 🔍 **Vector Search Implementation**
  Build a retrieval system using real embeddings and ChromaDB.

* 🔍 **Intro to RAG**
  Introduction to Retrieval-Augmented Generation.

## License

This project is licensed under the CC BY-NC-SA 4.0 License - see the [LICENSE](LICENSE) file for details.

## Contact

**Ready Tensor, Inc.**

- Email: contact at readytensor dot com
- Issues & Contributions: Open an issue or pull request on this repository
- Website: [Ready Tensor](https://readytensor.ai)
