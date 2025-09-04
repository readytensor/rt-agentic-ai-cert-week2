![AAIDC-wk2-l0-free-apis.jpeg](AAIDC-wk2-l0-free-apis.jpeg)

<!-- RT_DIVIDER -->

---

[🏠 Home - All Lessons](https://app.readytensor.ai/hubs/ready_tensor_certifications)

[⬅️ Previous - Agents Vs. Workflows](https://app.readytensor.ai/publications/Xq3L2HSWLPou)
[➡️ Next - Building Prompts](https://app.readytensor.ai/publications/36Hu3DC3TLdu)

---

<!-- RT_DIVIDER -->

# TL;DR

This lesson shows you how to get started with agentic AI using free LLM options for learning, experimentation, and prototyping. You'll explore APIs from providers like Groq and Google Gemini, or run local models with Ollama—no payments or subscriptions required to follow along. Whether you use Llama, Gemini, or OpenAI models, you have flexible options to support your learning journey.

---

<!-- RT_DIVIDER -->

# Getting Ready: Free LLM Options for This Course

In this course, you’ll be using tools like **LangChain** and **LangGraph** to build intelligent, goal-driven AI systems. Many lessons include examples that use OpenAI’s API — a popular option, but one that typically requires a paid subscription.

**Good news:** you can complete this course **without needing to pay for API access**.

We’ve intentionally designed the curriculum with **low usage requirements**, so learners can follow along without hitting paywalls. All major projects and hands-on lessons can be completed using **free-tier API keys** or **local models** that run entirely on your machine.

In this lesson, you’ll learn about two ways to get started without spending anything:

1.  **Use Free API Access**
    Providers like **Groq** and **Google Gemini** offer generous free usage quotas for high-quality LLMs. Some of these even support OpenAI models, so you can stick with familiar prompts while avoiding upfront costs.

2.  **Run Local Models with Ollama**
    If you have a machine with a decent GPU, you can use **Ollama** to download and run open-source models like **Llama 3**, **Mistral**, or **Code Llama** right on your computer. This option gives you full control and zero API limits — perfect for hands-on learners who want to explore under the hood.

We’ll walk you through how to set up each of these options and explain the tradeoffs — from speed and quality to installation complexity and system requirements.

<!-- RT_DIVIDER -->

:::info{title="Effortless LLM Switching With LangChain"}

LangChain makes switching between providers seamless, whether you're using Groq, Gemini, OpenAI, or a local model with Ollama. With just a small config change, you can follow the course without rewriting your code or adjusting your prompts — giving you the freedom to choose what works best for you.

:::

---

<!-- RT_DIVIDER -->

# Option 1: Use a Free Cloud API

You don’t need to run large language models on your own machine to follow this course. Providers like **Groq** and **Google Gemini** offer **free API access** to high-quality models — no credit card or subscription required.

These cloud APIs are:

- Easy to set up
- Well-supported by LangChain
- Fast enough for real-time use
- Free to use (within generous usage and rate limits)

Let’s start with Groq.

---

<!-- RT_DIVIDER -->

## Groq: Fast, Free Access to Open-Source LLMs

**Groq** is an AI infrastructure provider offering free API access to powerful open-source models like Llama 3 and Mixtral, all hosted on their ultra-fast **Language Processing Units (LPUs)**.

You get real-time responses from capable open models — perfect for learning and prototyping.

> ⚠️ Note: Groq’s free tier includes **rate limits and daily caps**. These limits are generous enough for this course, but if you're sending lots of requests, you may occasionally need to wait.

---

<!-- RT_DIVIDER -->

### Advantages of Using Groq

- ✅ **Free to use (within limits)** — no credit card required
- ✅ **Fast responses** — LPUs make requests snappy
- ✅ **Developer-friendly** — limits support learning and prototyping
- ✅ **OpenAI-style interface** — easy prompt reuse
- ✅ **LangChain ready** — works out of the box with this course setup

---

<!-- RT_DIVIDER -->

### How to Set Up and Use Groq

 <h3> Step 1: Sign Up and Get Your Groq API Key </h3>
 
 1. Go to [https://console.groq.com](https://console.groq.com)
 2. Sign up (no payment info required)
 3. In the dashboard, go to **API Keys**
 4. Click **Create API Key**
 5. Copy your key (starts with `gsk_...`)
 
 ---
 
 <h3> Step 2: Add Your API Key to the Environment </h3>
 
 ```bash
 # Option 1: Add to a .env file
 GROQ_API_KEY=your_key_here
 
 # Option 2: Export it directly in your terminal
 export GROQ_API_KEY=your_key_here
 ```
 
 ---
 
 <h3> Step 3: Install the LangChain–Groq Package </h3>
 
 Install Groq's LangChain integration:
 
 ```bash
 pip install langchain_groq
 ```
 
 ---
 
 <h3> Step 4: Run a Simple Test Script </h3>
 
 Try this simple test script:
 
 ```python
 from langchain_groq import ChatGroq
 
 llm = ChatGroq(model="llama3-8b-8192")
 response = llm.invoke("What is agentic AI?")
 print(response)
 ```
 
 If you see a response in your terminal, you’re good to go.
 
 > 🧪 Try swapping the prompt to something like `"Explain vector databases in one paragraph."`
 > Or test something fun like `"Write a haiku about AI agents."`
 
 ---

<!-- RT_DIVIDER -->

### Video Walkthrough: Setup and Use Groq’s Free API 🎥

In this video, you’ll learn how to set up Groq’s free API key and load it into your local development environment using both export and `.env` file methods.

By the end of this video, you’ll be ready to run your own LangChain-powered applications using Groq’s Llama 3 models — no billing or cloud configuration needed.

:::youtube[Use Groq’s Free API for Local LLM Projects]{#Y6M8Nehwo0U}

---

<!-- RT_DIVIDER -->

## Gemini: Access Google’s LLMs Through a Free Developer Tier

**Gemini** is Google’s suite of powerful large language models — and you can access them via **Gemini API**, using a developer key that you generate through **Google AI Studio**.

You don’t need to enter payment information to get started. The API offers a **free tier** designed for testing, development, and learning — making it a great fit for coursework and experimentation.

> ⚠️ Google’s free tier includes usage limits and rate caps. These are typically generous enough for this course, but they are not meant for production use. If you hit a limit, you can wait for it to reset — or upgrade later if needed.

---

### Advantages of Using Gemini

- ✅ **No billing required to start** — generate an API key instantly with your Google account
- ✅ **Developer-friendly limits** — enough for lessons, prototyping, and experimentation
- ✅ **Good performance on reasoning and coding tasks**
- ✅ **Supports multimodal input** (text, images, etc.)
- ✅ **Works seamlessly with LangChain**

---

### How to Set Up and Use Gemini

 <h4> Step 1: Create Your API Key </h4>
 
 1. Go to [https://makersuite.google.com](https://makersuite.google.com)
 2. Sign in with your Google account
 3. Click **Get API Key**
 4. Choose **Create API Key in new project**
 5. Copy your key — it will look like `AIza...`
 
 ---
 
 <h4> Step 2: Add the Key to Your Environment </h4>
 
 ```bash
 # Option 1: Add to a .env file
 GOOGLE_API_KEY=your_key_here
 
 # Option 2: Export it in your terminal
 export GOOGLE_API_KEY=your_key_here
 ```
 
 ---
 
 <h4> Step 3: Install the Required Package </h4>
 
 ```bash
 pip install langchain-google-genai
 ```
 
 ---
 
 <h4> Step 4: Test Your Setup </h4>
 
 Try this minimal script:
 
 ```python
 from langchain_google_genai import ChatGoogleGenerativeAI
 
 llm = ChatGoogleGenerativeAI(
     model="gemini-2.5-flash",
     temperature=0,
     max_tokens=None,
     timeout=None,
     max_retries=2,
     # other params...
 )
 response = llm.invoke("Explain prompt engineering in simple terms.")
 print(response)
 ```
 
 You should see a clean response — ready to go, with no billing setup.
 
 > 🧪 Tip: Try switching the prompt to `"Give me a metaphor for vector embeddings"` or `"What's a beginner-friendly explanation of LangChain?"`
 
 ---

<!-- RT_DIVIDER -->

### Use Google Gemini’s Free API in Your Projects 🎥

In this video, you’ll learn how to create and configure a Gemini API key using Google AI Studio. You’ll integrate the key into your environment (via `.env` file or terminal) and send your first request — all in under 5 minutes.

:::youtube[Use Google Gemini’s Free API in Your Projects]{#-epXsWJbggA}

---

<!-- RT_DIVIDER -->

# Option 2: Run a Local LLM with Ollama

Don’t want to depend on cloud APIs at all? **Ollama** lets you run powerful LLMs like **Llama 3**, **Mistral**, and **Code Llama** locally — with no API keys, no rate limits, and no internet required once models are downloaded.

This is a great option if:

- You want full control over the models you're using
- You’re interested in exploring open models
- You have a machine with enough resources (RAM and GPU)

> ⚠️ Running local models requires decent hardware — especially if you're using larger models. We recommend starting with smaller variants like `llama3-8b-8192` if you’re unsure.

---

## Advantages of Using Ollama

- ✅ **No API calls or rate limits** — everything runs locally
- ✅ **Fully offline** after initial model download
- ✅ **Free and open-source** — no subscriptions or tokens needed
- ✅ **Great for privacy-conscious development and experimentation**
- ✅ **LangChain-compatible** with minimal setup

---

<!-- RT_DIVIDER -->

## What Your System Needs

Going local with Ollama gives you full control and unlimited usage — but it also demands serious memory. Here’s how to figure out if your hardware can handle it.

---

 <h3> Memory Rule (Assuming FP32) </h3>
 
 Let’s assume you’re running the model using standard **FP32** precision — that means each parameter (or weight) uses **4 bytes** of memory.
 
 > **Memory required (in GB)** =
 > `Model size in billions × 4`
 
 💡 Here, “model size” refers to the **number of parameters** (also called weights), typically expressed in billions (e.g., 7B, 13B, 70B).
 
 So for example:
 
 * A **7B** model in **FP32** requires `7 × 4 = 28 GB`
 * A **13B** model in **FP32** requires `13 × 4 = 52 GB`
 
 Most laptop GPUs can’t handle this — but don’t worry, there’s a trick.
 
 ---
 
 <h3> But You Can Use Less: Enter Quantization </h3>
 
 Most models don’t need full 32-bit precision to run effectively. You can use **quantization** — a technique that stores each parameter in fewer bits.
 
 This significantly reduces memory usage while keeping model quality high enough for most tasks.
 
 | Precision Type | Bytes per Parameter | Notes                       |
 | -------------- | ------------------- | --------------------------- |
 | FP32           | 4                   | Full precision              |
 | FP16           | 2                   | Common for inference        |
 | Q8             | 1                   | 8-bit quantization          |
 | Q4             | 0.5                 | 4-bit quantization (common) |
 
 
 :::tip{title="Info"}
 💡 Note: Lower precision (like FP16, Q8, Q4) is commonly used for inference to save memory, while training usually requires higher precision like FP32 or FP16 to maintain accuracy and stability.
 :::
 
 ---
 
 <h3> Memory Formula with Quantization </h3>
 
 > **Memory required (in GB)** =
 > `Model size in billions × bytes per parameter`
 
 **Examples:**
 
 * A **7B** model in **Q4** → `7 × 0.5 = 3.5 GB`
 * A **13B** model in **FP16** → `13 × 2 = 26 GB`
 
 That’s why tools like **Ollama** can run quantized models on machines with as little as 8–16 GB of GPU memory.
 
 ---
 
 <h3> Memory Requirements by Model Size </h3>
 
 | Model Size | FP32 (4 bytes) | FP16 (2 bytes) | Q8 (1 byte) | Q4 (0.5 byte) |
 | ---------- | -------------- | -------------- | ----------- | ------------- |
 | 1B         | 4 GB           | 2 GB           | 1 GB        | 0.5 GB        |
 | 3B         | 12 GB          | 6 GB           | 3 GB        | 1.5 GB        |
 | 7B         | 28 GB          | 14 GB          | 7 GB        | 3.5 GB        |
 | 8B         | 32 GB          | 16 GB          | 8 GB        | 4 GB          |
 | 13B        | 52 GB          | 26 GB          | 13 GB       | 6.5 GB        |
 | 20B        | 80 GB          | 40 GB          | 20 GB       | 10 GB         |
 | 30B        | 120 GB         | 60 GB          | 30 GB       | 15 GB         |
 | 65B        | 260 GB         | 130 GB         | 65 GB       | 32.5 GB       |
 | 70B        | 280 GB         | 140 GB         | 70 GB       | 35 GB         |
 | 120B        | 480 GB         | 240 GB         | 120 GB       | 60 GB         |
 
 ---
 
 <h3> Reality Check: Don't Forget Overhead </h3>
 
 The values above only account for **model weights**. But during inference, your system also needs memory for:
 
 * **Activations** (intermediate outputs at each layer)
 * **Input tokens**
 * **Temporary buffers**
 
 A safe rule of thumb:
 
 > Add **20–50% extra memory** on top of the base estimate to avoid out-of-memory errors.
 
 ---
 
 <h3> What Will Run on a Laptop GPU? </h3>
 
 * **8 GB GPU** → you’ll likely need to stick with **1B–3B models** in **Q4**
 * **16 GB GPU** → you might be able to run a **7B model** in **Q4 or Q8**
 * **32 GB+ GPU** → capable of running **13B+ models**, especially in FP16
 
 > 🔧 For comparison: An **NVIDIA A100 (40 GB variant)** can run a **13B model in FP16** or a **30B model in Q4**. To run **70B models**, you'd need **multiple high-end GPUs** or advanced memory management.
 
 ---

<!-- RT_DIVIDER -->

## How to Set Up and Use Ollama

 <h3> Step 1: Install Ollama </h3>
 
 Go to [https://ollama.com](https://ollama.com) and download the installer for your system (macOS, Windows, or Linux).
 
 Follow the instructions to complete installation.
 
 ---
 
 <h3> Step 2: Download a Model </h3>
 
 Once installed, open your terminal and run:
 
 ```bash
 # Recommended starting point
 ollama pull llama3-8b-8192
 ```
 
 Other available models include:
 
 ```bash
 ollama pull mistral
 ollama pull codellama
 ```
 
 These will download and prepare the models for local use.
 
 ---
 
 <h3> Step 3: Install the LangChain Integration </h3>
 
 Install the Ollama LangChain wrapper:
 
 ```bash
 pip install langchain-ollama
 ```
 
 ---
 
 <h3> Step 4: Run a Local LLM Test </h3>
 
 Here’s a minimal example:
 
 ```python
 from langchain_community.chat_models import ChatOllama
 
 llm = ChatOllama(model="llama3-8b-8192")
 response = llm.invoke("Summarize how local models work.")
 print(response)
 ```
 
 This will invoke the LLM running on your machine and return a response — no cloud involved.
 
 > 🧪 Try a fun test prompt like: `"Explain agentic AI like you're a movie trailer narrator."`
 
 ---

<!-- RT_DIVIDER -->

# When to Use Which Option

Not sure which path to pick? Here’s the good news: **they all work** — and you can switch at any time.

If you want something fast and cloud-hosted, start with **Groq** or **Gemini**. Prefer full control or want to work offline? Try **Ollama**. You’re not locked in — LangChain makes it easy to change providers without rewriting your code.

|           | **Groq**           | **Gemini**        | **Ollama**            |
| --------- | ------------------ | ----------------- | --------------------- |
| Setup     | Easy cloud setup   | Easy cloud setup  | Requires install      |
| Speed     | Very fast          | Fast              | Varies by hardware    |
| Cost      | Free tier          | Free tier         | Fully free (local)    |
| Limits    | Rate caps apply    | Rate caps apply   | No rate limits        |
| Offline?  | ❌                 | ❌                | ✅                    |
| Great for | Prototyping, speed | Reasoning, coding | Privacy, full control |

There’s no single “best” choice — just pick what fits your system and comfort level. You can always switch later.

---

<!-- RT_DIVIDER -->

:::info{title="Info"}

# OpenAI's GPT-OSS Models: Now Available for Local Use

OpenAI recently released open-source versions of their models, known as **GPT-OSS**. These include two models like **gpt-oss-20b** and **gpt-oss-120b** that you can now run locally using Ollama.

**What makes GPT-OSS special:**

- **Fully open-weight** - you can download and modify them freely
- **High performance** - built on OpenAI's latest architecture
- **Local deployment** - run them on your own hardware with Ollama

**Using GPT-OSS with Ollama:**

```bash
# Download the 20B model (requires ~16GB RAM)
ollama pull gpt-oss:20b

# Or the larger 120B model (requires ~60GB RAM)
ollama pull gpt-oss:120b
```

**Reality check:** While these models offer cutting-edge capabilities, they require substantial hardware resources that are likely beyond most learning setups. The 20B model needs around 16GB of RAM, and the 120B model needs approximately 60GB - making cloud APIs more practical for most users in this course.

However, if you have access to high-end workstations or servers, these models represent an exciting opportunity to run OpenAI-quality models completely locally and privately.
:::

---

<!-- RT_DIVIDER -->

# Final Notes

You’re now ready to start your journey building with agentic AI — no cost barriers, no complicated setup.

As you work through the lessons and projects, any of these LLM options will work. You can stick with one, or try more than one to see what fits your style.

Most importantly, you can learn and experiment **without burning through tokens or money** — it’s easy to stay within the free tiers or run models locally.

And if you ever get stuck, we’re just a message away on [Discord](https://discord.com/invite/EsVfxNdUTR).

---

**Next up:** we’ll kick off your hands-on journey with prompt engineering — the core skill behind making LLMs useful, flexible, and goal-driven. Now that your setup is ready, it’s time to start building.

<!-- RT_DIVIDER -->

---

[🏠 Home - All Lessons](https://app.readytensor.ai/hubs/ready_tensor_certifications)

[⬅️ Previous - Agents Vs. Workflows](https://app.readytensor.ai/publications/Xq3L2HSWLPou)
[➡️ Next - Building Prompts](https://app.readytensor.ai/publications/36Hu3DC3TLdu)

---
