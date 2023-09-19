# Chapter 1. 演算法介紹(Algorithm)

## 1.1.1 名詞定義
### Definition (Algorithm)
任何一個經由良好定義(well-defined)的計算步驟，包含了取得輸入並產生輸出的過程
or 
一個解決特定電腦問題的工具

- 總而言之，就是解決問題的方法。

### Definition (Problem)
一個問題的實例(Instance)包含了所有計算所需的可能的輸入(inputs)。
- 一個演算法只有在每個可能的輸入都可以在有限的時間裡完成，並且產生正確的解答時才能被稱為正確(correct)的演算法。
- 驗証答案的過程則使用驗証(Verification)用的演算法來進行。

## 1.1.2 應用場景
### Example (The Human Genome Project)
給定一個基因組:
```
S = "ACCGGTCGAGTGCGCGGAAGCCGGCCGAAGTCGTTCGGAATGCCGTTGCTCTGTAAA"
```
如何在S中找出"GGAAGC"片段？
- 這其實就是一個字串搜尋的問題。

### Example (Intenet Applications)
- 在網路上找到一個最佳(最短、負載最低, 可能會以權重的形式出現在測資裡)的路由(route)好讓資料通過。
- 使用search engine來快速的找到包含特定資訊的網頁。
- 電子商務交易通訊用到的加密公鑰、數位簽章等演算法。

### Example (Machine Learning)
透過預先標記的訊練集，讓模型學習之後可以進行對訊練集之外的資料判斷，或是進行更進一步的解讀。

### Example (Manufacturing and other commercial settings)
- 制造業或是商業上的最佳化問題，以達到最大化利益的目的。
- 廣告的效益最佳化策略

