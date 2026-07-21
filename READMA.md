# 🚀 Prompt Engineering Lab

> A complete collection of Prompt Engineering experiments using Google's Gemini API.
>
> This repository serves as both a laboratory record and a quick reference guide for understanding the most important Prompt Engineering concepts used in Generative AI.



# 🧠 What is Prompt Engineering?

Prompt Engineering is the process of designing effective instructions (prompts) that guide a Large Language Model (LLM) to generate accurate, relevant, and high-quality responses.

A well-written prompt improves:

- Accuracy
- Relevance
- Consistency
- Creativity
- Reasoning Ability

Instead of changing the model, Prompt Engineering changes **how we communicate with the model**.

---

# 🤖 What is Gemini API?

Google Gemini API allows developers to interact with Google's Large Language Models using Python.

Example:

```python
from google import genai

client = genai.Client(api_key="YOUR_API_KEY")

response = client.models.generate_content(
    model="gemini-2.5-flash",
    contents="Explain Artificial Intelligence."
)

print(response.text)
```

---

# 📝 Experiment 1 — Basic Prompting

### Objective

Learn how an LLM responds to simple natural language instructions.

### Example Prompt

```text
Explain Machine Learning.
```

### Code

```python
prompt = "Explain Machine Learning."

response = client.models.generate_content(
    model="gemini-2.5-flash",
    contents=prompt
)

print(response.text)
```

---

# 📝 Experiment 2 — Prompt Refinement

### Objective

Improve response quality by making prompts more specific.

### Basic Prompt

```text
Explain AI.
```

### Refined Prompt

```text
Explain Artificial Intelligence in 100 words with one real-world example using simple English.
```

### Learning

More constraints generally produce more focused and useful responses.

---

# 📝 Experiment 3 — Zero-Shot Prompting

## What is Zero-Shot Prompting?

The model performs a task **without seeing any examples**.

It relies entirely on its pre-trained knowledge.

### Example

```text
Translate the following sentence into French.

Good Morning.
```

### Code

```python
prompt = """
Translate into French.

Good Morning.
"""
```

### Applications

- Translation
- Summarization
- Question Answering
- Content Generation

---

# 📝 Experiment 4 — One-Shot Prompting

## What is One-Shot Prompting?

The model is given **one example** before solving the actual task.

### Example

```text
English: Hello
French: Bonjour

English: Thank You
French:
```

### Code

```python
prompt = """
English: Hello
French: Bonjour

English: Thank You
French:
"""
```

### Benefits

- Better formatting
- Better consistency
- Reduced ambiguity

---

# 📝 Experiment 5 — Few-Shot Prompting

## What is Few-Shot Prompting?

The model receives **multiple examples** before answering.

Instead of learning from training, it learns from examples inside the prompt.

### Example

```text
Positive → I love this movie.

Negative → This is terrible.

Positive → Amazing acting.

Negative → Waste of time.

Classify:

The story was wonderful.
```

### Code

```python
prompt = """
Positive → I love this movie.

Negative → This is terrible.

Positive → Amazing acting.

Negative → Waste of time.

Classify:

The story was wonderful.
"""
```

### Applications

- Sentiment Analysis
- Classification
- Named Entity Recognition
- Information Extraction

---

# 📝 Experiment 6 — Role Prompting

## What is Role Prompting?

Assigning a role to the AI improves the style and quality of responses.

### Example

```text
You are a professional Data Scientist.

Explain Decision Trees.
```

### Code

```python
prompt = """
You are a professional Data Scientist.

Explain Decision Trees.
"""
```

---

# 📝 Experiment 7 — Constraint-Based Prompting

## What is Constraint Prompting?

The response must satisfy predefined rules.

### Example

```text
Summarize the article.

Rules:

• Maximum 80 words

• Use bullet points

• Mention Deep Learning
```

### Benefits

- Controlled output
- Better formatting
- Consistent answers

---

# 📝 Experiment 8 — Summarization

### Objective

Generate concise summaries from lengthy articles.

### Example

```text
Summarize the following article in 100 words.
```

### Applications

- Research Papers
- News Articles
- Reports
- Books

---

# 📝 Experiment 9 — Content Generation

Generate different types of text using prompts.

Examples

- Blog Writing
- Email Writing
- Product Description
- Story Generation
- LinkedIn Posts
- Social Media Captions

Example Prompt

```text
Write a LinkedIn post about Artificial Intelligence.
```

---

# 📝 Experiment 10 — Prompt Iteration

Prompt Iteration means improving prompts repeatedly until the desired output is obtained.

Example

Version 1

```text
Explain AI.
```

Version 2

```text
Explain AI using simple English.
```

Version 3

```text
Explain AI in less than 100 words using one real-life example.
```

Version 4

```text
Explain AI in bullet points with one analogy and one example.
```

Each iteration improves response quality.

---

# 💡 Best Practices

✔ Be specific

✔ Give context

✔ Define the role

✔ Specify output format

✔ Mention word limits

✔ Use examples when necessary

✔ Iterate and refine prompts

```

---

# 🎯 Learning Outcomes

After completing this laboratory, you will be able to:

- Understand Prompt Engineering fundamentals.
- Use the Gemini API for Generative AI tasks.
- Apply Zero-Shot, One-Shot, and Few-Shot prompting.
- Improve AI responses through prompt refinement.
- Generate structured outputs using constraints.
- Build effective prompts for real-world AI applications.

---

# 👨‍💻 Author

**Prabha Supriya B**

B.Tech in Artificial Intelligence & Machine Learning

---

# 📄 License

This project is intended for educational and academic learning purposes.
