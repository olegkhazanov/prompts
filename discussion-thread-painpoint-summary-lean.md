# Prompt: Summarize Pain Points from Large Discussion Dataset

## Context
You are given a CSV containing ~23,000 discussion threads.

## Goal
Identify and summarize the major recurring pain points.

## Instructions

1. Cluster similar complaints into higher-level themes.
2. Prioritize recurring issues over isolated complaints.
3. Estimate relative frequency (High / Medium / Low).
4. Extract representative signals (short paraphrased example).
5. Identify likely root causes where patterns are clear.
6. Ignore noise, edge outliers, and one-off emotional spikes.

## Output Format

### Executive Summary
Top 5–10 pain points ranked by frequency or severity.

---

### Pain Point #1: [Short Label]
Frequency: High / Medium / Low  
Summary: 1–2 sentences  
Example: Short paraphrased signal  
Root Cause (if clear): 1 sentence  
Impact: 1 sentence  

---

### Cross-Cutting Patterns
- Systemic issues
- Repeated breakdowns
- Emotional tone summary

---

## Constraints
- No hallucinated trends.
- No long narrative explanations.
- Be concise and structured.
- Optimize for signal density.
