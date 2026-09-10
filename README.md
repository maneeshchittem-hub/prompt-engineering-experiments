# Prompt Engineering Experiments

## Introduction

As part of my Generative AI internship, I worked on a prompt engineering task to understand how different prompts can change the output of an AI model.

For this task, I used Google AI Studio and Gemini to test different prompting techniques.

I worked on three experiments:

1. Zero-shot vs Few-shot prompting
2. Direct prompting vs Step-by-step prompting
3. Structured JSON output

---

## Experiment 1: Zero-Shot vs Few-Shot Prompting

### What I did

For this experiment, I used a simple sentiment classification task.

The model had to classify customer reviews as:

- Positive
- Negative
- Neutral

First, I tested the reviews without giving any examples. This is called zero-shot prompting.

After that, I gave the model a few examples showing which reviews were Positive, Negative, and Neutral. This is called few-shot prompting.

### Zero-Shot Result

I tested 5 reviews.

The model correctly classified 4 out of 5 reviews.

Accuracy: 80%

One interesting result was that the model classified a neutral review as Negative. This showed that the model can sometimes make mistakes when there are no examples to guide it.

### Few-Shot Result

For few-shot prompting, I provided three examples before asking the model to classify the new reviews.

The examples helped the model understand what I expected for each category.

### What I learned

I learned that giving examples in the prompt can make the model's responses more consistent, especially when the task can have some ambiguity.

---

## Experiment 2: Direct Prompt vs Step-by-Step Prompt

### What I did

For this experiment, I used a small mathematical problem involving notebooks, pens, and change.

I tested the problem in two ways.

First, I directly asked the model to solve the problem.

Then, I used another prompt asking the model to think through the problem step by step.

### Problem

A shop sells notebooks for ₹40 each and pens for ₹15 each.

Maneesh buys 5 notebooks and 4 pens and pays ₹500.

The correct change is ₹240.

### Direct Prompt

The direct prompt asked the model to solve the problem and give the answer.

### Step-by-Step Prompt

The second prompt asked the model to solve the problem step by step.

This made the calculation easier to understand because the model showed the different parts of the calculation.

### What I learned

Both approaches can work for simple problems.

However, step-by-step prompting can be useful for problems that have multiple calculations because it makes the solution easier to follow and check.

---

## Experiment 3: Structured JSON Output

### What I did

In this experiment, I asked the model to extract information from customer transaction messages.

The information I needed was:

- Name
- Date
- Amount

I wanted the model to return the information in JSON format.

### JSON Format

```json
{
  "name": "string",
  "date": "string",
  "amount": 0
}