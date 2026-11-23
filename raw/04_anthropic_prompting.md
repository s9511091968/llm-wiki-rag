# Source 04: Anthropic Documentation — Reduce Hallucinations
- **Source**: Anthropic Prompt Engineering Guide
- **URL**: https://docs.anthropic.com/en/docs/test-and-evaluate/strengthen-guardrails/reduce-hallucinations
- **Raw Notes**:
  - Even with retrieved context, LLMs may still rely on prior training knowledge or extrapolate beyond the text.
  - Guardrail techniques:
    1. Explicitly instruct the model to ONLY use the provided reference context.
    2. Give the model permission to say "I don't know" or "現有資料無法回答" when the answer is not in the context.
    3. Require sentence-level citations referencing the source chunk ID.