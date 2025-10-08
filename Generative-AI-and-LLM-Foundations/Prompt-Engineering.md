# Lesson: Prompt Engineering

### What Is a Prompt?

A **prompt** is the input or initial text provided to a **large language model (LLM)**.  
**Prompt engineering** is the process of *iteratively refining* a prompt for the purpose of eliciting a particular style or quality of response.  
Text prompts are the primary way users interact with large language models.

---

## How LLMs Respond to Prompts

Until now, we’ve seen that LLMs attempt to produce the **next token or next series of words** that are most likely to follow from the previous text.

For example, if we give a prompt such as:

> “Four score and seven years ago…”

The model recognizes this as part of the **Gettysburg Address** by Abraham Lincoln (1863) and attempts to *complete* the text based on learned patterns.

This demonstrates that completion-based LLMs are trained to **predict the next word** rather than directly perform the user’s intended task.

---

## Challenges with Completion LLMs

Completion LLMs are trained on massive datasets of internet text.  
This means they **predict what text comes next**, not necessarily what the user *wants them to do*.

As a result:
- You cannot give direct instructions or ask explicit questions to a pure completion model.
- You must instead **formulate a prompt** whose natural continuation is your desired output.

This is not always easy or effective — which is why **instruction tuning** is used.

---

## Instruction Tuning

**Instruction tuning** is a critical step in aligning an LLM to perform desired tasks.  
It involves fine-tuning a pre-trained LLM on a set of **instructions paired with desired outputs**.

For example, in Meta’s *LLaMA 2* paper:

- The **LLaMA 2 foundation models** were trained on **2 trillion tokens**.  
- **LLaMA 2 Chat**, a variant for conversations, was **additionally fine-tuned** on about **28,000 prompt–response pairs**.

### Reinforcement Learning from Human Feedback (RLHF)

A key concept in instruction tuning is **Reinforcement Learning from Human Feedback (RLHF)**.

- Human annotators write prompts and compare model outputs.
- Their feedback trains a **reward model** to learn human preferences.
- The model is then further fine-tuned to **align its behavior** with these preferences.

In short, **RLHF** helps models follow instructions and generate human-aligned responses instead of merely predicting text continuations.

---

## Successful Prompting Strategies

Prompt engineering can be challenging, but there are several **effective strategies** that improve model behavior for specific tasks.

We will look at two foundational ones:

1. **In-Context Learning (Few-Shot Prompting)**
2. **Chain-of-Thought Prompting**

---

### 1. In-Context Learning and Few-Shot Prompting

**In-Context Learning** means conditioning the model with examples or demonstrations of the task it should perform.

It’s important to note that this isn’t “learning” in the traditional sense — the model parameters don’t change.  
Instead, it’s temporary conditioning based on **examples in the prompt**.

#### Few-Shot Prompting

In **k-shot prompting**, we explicitly provide *k examples* of the desired task.

- **0-shot** → No examples  
- **1-shot** → One example  
- **2-shot** → Two examples  
- **k-shot** → k examples

#### Example (Three-Shot Prompting)

> **Task:** Translate this text from English to French  
>
> - cheese → fromage  
> - car → voiture  
> - apple → pomme  
>
> **Prompt:** translate *book*

The model, having seen the examples, correctly outputs:

> **Output:** livre

Research shows that **few-shot prompting** generally produces *better results* than zero-shot prompting.

---

### 2. Chain-of-Thought Prompting

For **complex or multi-step tasks**, we can prompt the model to *think through* intermediate steps — just as humans would when solving problems.

This is called **Chain-of-Thought (CoT) prompting**.

It encourages the model to describe its reasoning or calculation before giving the final answer.

#### Example

> **Prompt:**  
> Roger starts with 5 tennis balls. He buys 2 more cans of tennis balls. Each can has 3 tennis balls.  
> How many total tennis balls does he have?

**Response (with reasoning):**

> Roger starts with 5.  
> 2 cans × 3 = 6.  
> 5 + 6 = 11.  
> **Answer: 11 tennis balls.**

Now another example:

> The cafeteria had 20 bananas. They used 10 to make pancakes and purchased 8 more. How many bananas do they have now?

**Response (chain-of-thought):**

> Start with 20.  
> Used 10 → 10 remain.  
> Bought 8 more → 10 + 8 = 18.  
> **Answer: 18 bananas.**

Without chain-of-thought reasoning, models often make simple arithmetic or logical errors.  
This technique greatly improves **accuracy and reasoning transparency**.

---

## Hallucination in LLMs

Another important topic is **hallucination**.

### What Is a Hallucination?

A hallucination occurs when a model generates **non-factual or ungrounded text** — i.e., text not supported by its training data.

Hallucinations may:
- Contain **factually incorrect** statements.
- Sound **fluent and convincing**, even though they are wrong.

#### Example

> “In the United States, people gradually adopted the practice of driving on the left side of the road.”

This is **factually incorrect** (the U.S. drives on the *right*) — a clear hallucination.

---

### Why Hallucinations Matter

Hallucinations can be subtle and hard to detect.  
Even when text is fluent and grammatically perfect, it may still be **incorrect**.

Researchers are actively working on methods to:
- **Detect** hallucinations  
- **Measure** groundedness (how factual outputs are)
- **Reduce** hallucination rates through retrieval-augmented methods

Currently, **no technique guarantees zero hallucinations**, though retrieval-augmented systems perform better than standard zero-shot LLMs.

---

## Summary

In this lesson, we covered:

- The definition of **prompts** and **prompt engineering**
- The challenges of **completion-based LLMs**
- **Instruction tuning** and **RLHF**
- Two major prompting strategies:
  - **In-Context Learning** and **Few-Shot Prompting**
  - **Chain-of-Thought Prompting**
- The issue of **LLM hallucination** and ongoing research to mitigate it

Prompt engineering is an evolving field that combines creativity, logic, and experimentation to make LLMs more reliable and aligned with human intent.
