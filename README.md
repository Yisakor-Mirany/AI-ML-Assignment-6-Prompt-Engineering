# AI-ML Assignment 6 – Prompt Engineering

**Name:** Yisakor Mirany  
**Course:** AI / Machine Learning  
**Assignment:** Prompt Engineering & LLM Task Optimization  

---

## Project Overview

The goal of this assignment is to demonstrate the practical impact of prompt engineering
on the performance of a Large Language Model (LLM). The project evaluates how different
prompt engineering techniques improve output quality for the same task and input.

The selected task for this experiment is **structured data extraction** from unstructured
text, a common real-world enterprise use case.

All experiments were conducted using a Jupyter Notebook to ensure transparency,
repeatability, and clear comparison between prompt strategies.

---

## LLM Used

- **Model:** OpenAI ChatGPT (pre-trained Large Language Model)
- **Environment:** Jupyter Notebook
- **Input Type:** Unstructured customer transaction text
- **Output Type:** Structured JSON

---

## Task Description

The LLM is required to extract the following structured fields from a block of
unstructured customer order text:

- Customer Name  
- Product  
- Price (USD)  
- Order Number  
- Order Date  
- Delivery Date  

The same input text is used across all prompt experiments to isolate the impact of
prompt engineering alone.

---

## Constant Input Text

The following input text was used for all prompt tests:


---

## Prompt Engineering Techniques Tested

Five prompt versions were evaluated:

1. **Baseline Prompt** – Minimal instruction with no guidance or constraints.
2. **Technique 1: Role Prompting** – Assigning the model a professional role.
3. **Technique 2: Output Formatting Constraints** – Enforcing a strict JSON schema.
4. **Technique 3: Chain-of-Thought Prompting** – Instructing the model to reason step by step.
5. **Final Optimized Prompt** – Combination of the most effective techniques.

---

## Prompt Comparison Summary

| Prompt Version | Technique Used | Score (1–10) | Observation |
|---------------|--------------|--------------|-------------|
| Baseline Prompt | None | 3 | Output was unstructured and not machine-readable |
| Technique 1 | Role Prompting | 6 | Improved understanding but poor format control |
| Technique 2 | Output Formatting | 9 | Reliable structured JSON output |
| Technique 3 | Chain-of-Thought | 9.5 | Higher accuracy and fewer missing fields |
| Final Prompt | Combined Techniques | 10 | Production-ready, consistent output |

---

## Technique Explanations

### Baseline Prompt
The baseline prompt provided minimal instruction (“Extract the data from the text”).
This resulted in vague, inconsistent output that lacked structure and could not be
used programmatically.

### Role Prompting
By instructing the model to act as a Senior Data Analyst, the output showed improved
understanding of relevant fields but still lacked strict formatting.

### Output Formatting Constraints
Providing an explicit JSON schema significantly improved consistency, accuracy, and
machine-readability, making the output suitable for real applications.

### Chain-of-Thought Prompting
Encouraging step-by-step reasoning further improved accuracy and reduced omissions,
especially in multi-field extraction tasks.

### Final Optimized Prompt
The final prompt combines role prompting, strict output formatting, and structured
reasoning, resulting in the highest-quality output.

---

## Key Lesson Learned

This experiment demonstrates that prompt engineering has a significant impact on
LLM performance. While baseline prompts produce unreliable and inconsistent results,
adding role context, explicit output constraints, and structured reasoning dramatically
improves accuracy, consistency, and usability.

Well-engineered prompts are essential for enterprise, security-sensitive, and
production-grade LLM applications.

---

## Repository Contents

- `prompt_engineering.ipynb` – Jupyter Notebook containing all prompt experiments
- `README.md` – Project documentation
- `requirements.txt` – Python dependencies

---

## Conclusion

Prompt engineering is not a cosmetic improvement but a core component of effective
LLM usage. This project highlights how deliberate prompt design can transform an
LLM from a general conversational tool into a reliable system for structured,
real-world tasks.
