# Multi-Agent-LLaMA-Sentiment-Analysis-System
**Overview**

This project implements a three-agent LLaMA-based ensemble system for sentiment classification. Each agent independently analyzes review text and predicts one of three labels: Positive, Negative, or Neutral. The final sentiment is determined using a majority voting aggregation strategy to improve robustness and consistency.

The system also includes an evaluation component to compare predictions against true labels and measure model performance.

**Architecture**
1. Multi-Agent Design

Three independent LLaMA-based agents

Each agent processes the same input review

Structured prompts ensure consistent label-only outputs

2. Aggregation Strategy

Majority voting across the three agents

Reduces single-model bias

Improves stability of predictions

3. Evaluation Component

Compares aggregated predictions with ground-truth labels

Computes accuracy (and optionally other metrics such as precision/recall)

**Prompt Design**

Prompts are carefully engineered to:

Clearly define the task (sentiment classification)

Restrict output to one of three labels

Reduce verbosity and ambiguity

Improve response consistency across agents

This structured prompting ensures reliable outputs suitable for aggregation.

**Workflow**

Load dataset containing reviews and true sentiment labels

Send each review to all three LLaMA agents

Collect individual predictions

Aggregate using majority voting

Evaluate predictions against true labels

**Key Features**

Multi-agent LLM architecture

Ensemble-style prediction aggregation

Structured prompt engineering

Evaluation pipeline

Modular and extensible design

**Results**

The ensemble approach improves classification robustness compared to relying on a single agent, demonstrating the effectiveness of multi-agent LLM systems in NLP tasks.

