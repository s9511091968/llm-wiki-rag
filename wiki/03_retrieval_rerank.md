# 03. 線上檢索階段（Retrieval）— 語意搜尋與重排序

當使用者在介面上輸入問題（Query）時，系統會即時啟動 **Retrieval（檢索）**，從資料庫中精準撈出最相關的參考片段。

## 檢索進階三部曲
1. **向量語意搜尋（Vector Search）**
   - 將使用者的問題也轉成向量，計算與資料庫向量的「餘弦相似度」。即使字面不同（如「怎麼退貨」與「退款流程」），也能靠語意找到。
2. **混合檢索（Hybrid Search）**
   - 結合「傳統關鍵字搜尋（BM25）」與「向量語意搜尋」。既能精準比對產品型號、專有名詞，又能理解同義詞語意。
3. **重排序（Reranking）**
   - 先寬鬆撈出前 20 筆候選資料，再用更精細的 Reranker 模型重新打分排序，只把最準確的前 3 筆（Top-3）交給 LLM，避免雜訊干擾。

- **原始資料來源**：[raw/03_pinecone_retrieval.md](../raw/03_pinecone_retrieval.md) | [Pinecone Learn](https://www.pinecone.io/learn/retrieval-augmented-generation/)