# Day 19 — Prompt Engineering for Reliable LLM Outputs

A practical Prompt Engineering experiment focused on improving the reliability, consistency, and grounded behavior of Large Language Model (LLM) responses.

## 📌 Project Overview

As part of my **60 Days AI/ML Challenge**, I explored how different prompt engineering techniques can influence LLM output quality.

The experiment uses a **RAG Question Answering** task and evaluates multiple prompting strategies using the Gemini API.

## 🎯 Objectives

- Understand the impact of prompt engineering on LLM responses
- Establish a baseline prompt
- Test different prompt engineering techniques
- Evaluate response quality using a 1–5 scoring framework
- Improve output consistency through structured prompts
- Reduce unsupported or hallucinated responses
- Test whether the model follows grounding instructions

## 🧠 Prompt Techniques Tested

### 1. Baseline Prompt
A simple instruction asking the model to answer the given question accurately.

### 2. Role Assignment
The model is assigned the role of an expert AI/ML educator.

### 3. Output Format Specification
The model is given an explicit response structure to improve consistency.

### 4. Reasoning-Based Prompting
The model is instructed to analyze the question carefully before producing the final answer.

### 5. Few-Shot Prompting
Examples of questions and answers are provided before asking the target question.

### 6. Negative Constraints
Explicit rules are provided to prevent irrelevant information, unsupported claims, unnecessary jargon, and repetition.

## 📊 Evaluation Framework

Each generated response is evaluated using a **1–5 scale** across:

| Metric | Description |
|---|---|
| Accuracy | How factually correct is the response? |
| Relevance | How directly does it answer the question? |
| Format Consistency | How clear, concise, and well-structured is the response? |

The overall score is calculated from the three evaluation dimensions.

## 🛡️ Grounding & Hallucination Control

A dedicated grounding prompt was created with the following principle:

> Use only the information provided in the context.

If the required information is not present, the model is instructed to clearly state that there is not enough information in the provided context.

### Out-of-Context Testing

Five questions outside the provided context were designed to test whether the model would refuse to answer instead of relying on external knowledge.

One successful test demonstrated the expected grounded behavior:

```text
I don't have enough information in the provided context to answer this question.
