# 05. RAG 系統評估三要素（RAG Triad）

評估一個 RAG 系統做得好不好，不能只看最後的文字通不通順，業界常使用 **RAG Triad（RAG 評估三角）** 逐一檢驗三個關鍵指標：

1. **檢索相關性（Context Relevance）**
   - 檢查「問題」與「撈出來的資料」：系統找回來的段落，是否真的跟使用者的問題有關？有沒有夾雜太多無關雜訊？
2. **答案忠實度（Faithfulness / Groundedness）**
   - 檢查「撈出來的資料」與「AI 回答」：AI 生成的答案是否 100% 忠於參考資料，沒有偷渡任何捏造的資訊（零幻覺）？
3. **回答相關性（Answer Relevance）**
   - 檢查「問題」與「AI 回答」：最終生成的答案，是否完整且直接地解決了使用者的疑惑？

- **原始資料來源**：[raw/05_ragas_evaluation.md](../raw/05_ragas_evaluation.md) | [RAGAs Docs](https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/)