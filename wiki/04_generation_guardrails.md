# 04. 增強生成階段（Generation）— Prompt 組裝與防幻覺

撈出 Top-K 參考資料後，系統會在幕後把「系統指令 + 參考資料 + 使用者問題」組裝成一個完整的 Prompt，交給 LLM 進行 **Generation（生成）**。

## 防幻覺三大護欄（Guardrails）
為了避免 AI 拿到資料後還是忍不住自行腦補，Prompt 必須加入嚴格約束：
1. **嚴格依據資料**：明確指示「請僅根據下方提供的參考資料回答問題」。
2. **允許拒答機制**：規定「若資料中沒有提及答案，請直接回答『現有資料無法回答』，嚴禁自行推測」。
3. **強制標註來源（Citation）**：要求 AI 在每一句回答後方附上參考資料編號（例如 `[1]`），方便使用者查證真偽。

- **原始資料來源**：[raw/04_anthropic_prompting.md](../raw/04_anthropic_prompting.md) | [Anthropic Docs](https://docs.anthropic.com/en/docs/test-and-evaluate/strengthen-guardrails/reduce-hallucinations)