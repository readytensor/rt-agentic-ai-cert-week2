# Ready Tensor Agentic AI Certification - Week 2

This repository contains the practical code and exercises for **Week 2** of the Ready Tensor Agentic AI Certification program, covering foundational prompt engineering concepts that are essential for building effective agentic AI systems.

## What You'll Learn

**Lesson 1 - Modular Prompt Engineering:** Learn to build prompts systematically using reusable components (role, constraints, style, goals) rather than ad-hoc approaches.

**Lesson 2 - Advanced "Reasoning" Techniques:** Master three powerful techniques—Chain of Thought, ReAct, and Self-Ask—that dramatically improve LLM performance on complex tasks.

In this repository, you can experiment with the modular prompt builder, test different reasoning strategies, and see how systematic prompt engineering creates more reliable and effective AI interactions.

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

3. **Set up your OpenAI API key:**

   Create a .env file in the root directory and add your OpenAI API key.
   See [.env.example](https://github.com/readytensor/rt-agentic-ai-cert-week2/blob/main/.env.example) file.

   ```
   OPENAI_API_KEY=your-api-key-here
   ```

   You can get your API key from [OpenAI](https://platform.openai.com/api-keys).

   
4. **Run the examples:**
   ```bash
   cd code
   python lesson_1a_and_1b.py
   ```
   **Customize your experiments:** Edit the `prompt_cfg_key` variable in `lesson_1_and_2.py` (near the bottom of the script) to test different prompt configurations (e.g., `summarization_prompt_cfg1` through `summarization_prompt_cfg6`). You can also create new configurations in `config/prompt_config.yaml` to experiment with your own prompt designs.

## Key Features

- **Modular Prompt Builder:** Construct prompts from reusable components defined in YAML configuration
- **Reasoning Strategy Integration:** Easily swap between Chain of Thought, ReAct, and Self-Ask techniques
- **Real Examples:** See prompt engineering concepts applied to publication summarization and LinkedIn post creation
- **Output Generation:** Automatically save constructed prompts and LLM responses for comparison

## How It Works

The `prompt_builder.py` module takes YAML configurations and builds structured prompts. You can:

- Mix and match prompt components (role, constraints, style, goals)
- Add reasoning strategies with a single configuration line
- Generate prompts for different tasks using the same framework
- Compare outputs to see the impact of different prompt designs

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

**Ready Tensor, Inc.**

- Email: contact at readytensor dot com
- Issues & Contributions: Open an issue or pull request on this repository
- Website: [Ready Tensor](https://readytensor.com)
