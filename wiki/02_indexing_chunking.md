# 02. 離線索引階段（Indexing）— 切塊與向量化

在系統開始接受提問前，必須先把原始文件（PDF、網頁、筆記）整理並存入向量資料庫，這個預處理過程稱為 **Indexing（建立索引）**。

## 核心兩大步驟
1. **文件切塊（Chunking）**
   - **原因**：整本 PDF 太長會稀釋重點，且超過 AI 一次能閱讀的上限。
   - **Chunk Size（切塊大小）**：將長文章切成固定長度的小段落（例如每塊 500 字）。
   - **Chunk Overlap（重疊區間）**：相鄰兩塊之間保留 10%～20% 的重疊文字，避免一句話剛好被從中間切斷而失去上下文語意。
2. **向量嵌入（Embedding）**
   - 透過 Embedding 模型，把每一塊文字轉換成一串數字座標（向量）。
   - 語意相近的句子（例如「貓咪」與「小貓」），在向量空間中的距離會非常接近。

- **原始資料來源**：[raw/02_langchain_chunking.md](../raw/02_langchain_chunking.md) | [LangChain Docs](https://python.langchain.com/docs/concepts/text_splitters/)