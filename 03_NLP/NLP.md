
# 🗣️ NLP 入門筆記：自然語言處理基礎

這份筆記整理我自學 NLP（自然語言處理）的重點觀念，包含詞表示、常見模型與應用。適合用來建立語言處理的基本理解。

---

## 🌍 什麼是 NLP？

NLP（Natural Language Processing）是讓電腦「理解人類語言」的技術。常見應用包括：

- 情感分析（判斷好評還是負評）
- 聊天機器人（如 ChatGPT）
- 文本分類（判斷新聞主題）
- 自動翻譯、摘要

---

## 🧱 文本 → 數值：詞的表示方法

電腦不能直接理解文字，所以第一步是把字詞轉成向量（數字形式）

### 1. One-Hot Encoding
- 每個詞變成一個獨立維度的向量
- 缺點：維度高、無法表示語意相似性

### 2. Bag of Words（詞袋模型）
- 看文章中出現了哪些詞，忽略順序
- 搭配 TF-IDF 可以加強重要詞彙的影響力

### 3. Word Embedding（詞向量）
- 讓語意相似的詞距離更近
- 代表模型：Word2Vec、GloVe、FastText

📷 示例圖：
![Word Embedding](https://jalammar.github.io/images/word2vec/word2vec-negative-sampling.png)

---

## 🛠️ NLP 任務常見模型

| 任務 | 模型 | 說明 |
|------|------|------|
| 文本分類 | Naive Bayes / RNN / BERT | 例：垃圾郵件 vs 一般信 |
| 情感分析 | LSTM / BERT | 判斷評論是正面還是負面 |
| 命名實體辨識（NER） | BiLSTM / CRF / Transformer | 抓出人名、地點等關鍵詞 |
| 文本生成 | GPT / LSTM | 自動產生句子、摘要 |

---

## 🧠 Transformer 架構（現代 NLP 基礎）

Transformer 是目前 NLP 最常用的架構，用於 BERT、GPT 等模型。

### ✅ 特點
- 改用「注意力機制」(Self-Attention)
- 可以同時處理整個句子，而非一個字一個字輸入

📷 架構圖（簡化）：
![Transformer]([https://jalammar.github.io/images/t/transformer_diagram.png](https://www.google.com/url?sa=i&url=https%3A%2F%2Fyololab.net%2F2023%2F07%2F31%2Ftransformer%2F&psig=AOvVaw0L7mvgDtWO9maNPQnUAJQB&ust=1746601925118000&source=images&cd=vfe&opi=89978449&ved=0CBQQjRxqFwoTCICLpqyljo0DFQAAAAAdAAAAABAJ))

---

## 🔤 預訓練語言模型：BERT vs GPT

| 模型 | 架構 | 任務 | 特點 |
|------|------|------|------|
| BERT | Transformer (Encoder) | 掃描理解文本（雙向） | 適合分類、句子配對 |
| GPT | Transformer (Decoder) | 自動產生文字（單向） | 適合生成、對話任務 |

BERT 是雙向讀句子（理解），GPT 是從左到右讀（生成）。這也是它們的任務分工基礎。

---

## 🧪 我的實作方向（將補充）

- BERT 中文情感分類
- GPT-2 文本生成
- TF-IDF + Naive Bayes 新聞分類

---

## 📚 推薦學習資源

- [The Illustrated Transformer - Jalammar](https://jalammar.github.io/illustrated-transformer/)
- [CS224n - Stanford NLP 課程](https://web.stanford.edu/class/cs224n/)
- [Hugging Face Transformers 教學](https://huggingface.co/transformers/)
- [BERT 中文簡介](https://zhuanlan.zhihu.com/p/43284939)

---

📌 此筆記為人工智慧雙主修申請的一部分，將持續更新更多 NLP 模型與實作細節。
