# Day 4 — Course Lab

**Course 5 · Fine-Tuning and LLM Alignment**
**Lab:** Fine-Tuning a Layer with LoRA — *one Hausa sentence, one full update: "abinci dadi sosai"*
*(Cohort 2 copy of the 2026-08-13 final; Colab run-through pending)*

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/aims-ai-research-foundations/Nigeria-workshop-2/blob/main/course-labs/day4/day4-course5-student.ipynb)

## About

Trace one full LoRA update on a tiny frozen layer, first by hand and then in
numpy. Starting from a frozen W ∈ R^{4×8} you run a full-fine-tune step as the
baseline, then build the rank-1 adapter ΔW = αAB, derive its gradients, take
one SGD step, and watch the adapter — not the frozen weights — learn. The
closing sections show why a merged adapter costs nothing at inference, how two
adapters share one frozen model, and what raising the rank from 1 to 2 buys.
It is the same "abinci dadi sosai" example as the morning walkthrough and the
AI-activity worksheet, carried to the end. About 60 minutes; pure numpy, no
GPU and no installs needed.

## How to work through it

- Click **Open in Colab** above to launch the notebook.
- **Before running or editing anything, save your own copy: File → Save a copy
  in Drive.** The badge opens the notebook in read-only playground mode;
  without your own copy, all your work is lost when the tab closes.
- Follow the **Predict → Run → Explain** protocol for every code cell: predict
  what will happen (shapes, numbers), run it, then explain any surprises.
- Four YOUR-CODE-HERE stubs and a checkpoint after each part walk the update
  end to end at rank 1, then again at rank 2. The closing reflection is the
  cell that matters most: when does LoRA stop being parameter-efficient?
