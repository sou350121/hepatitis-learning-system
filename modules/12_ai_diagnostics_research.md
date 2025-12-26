# 模組 12：肝炎診斷中的 AI 與機器學習 (Module 12: AI & Machine Learning in Hepatitis Diagnosis)

> **參考文獻 (Reference)**：*Indonesian Journal of Computer Science*, Vol. 13, No. 3, 2024. ISSN: 2549-7286.

## 1. 簡介 (Introduction)
現代肝臟病學正日益利用機器學習 (Machine Learning, ML) 來提高肝炎診斷的準確性、速度和成本效益。透過分析臨床和實驗室發現（如年齡、性別、膽紅素 Bilirubin、白蛋白 Albumin 等），ML 模型可以預測疾病的存在、嚴重程度以及患者的預後 (Outcomes)。

---

## 2. 核心演算法與方法論 (Core Algorithms & Methodology)

| 演算法 (Algorithm) | 描述 (Description) | 性能亮點 (Performance Highlights) |
| :--- | :--- | :--- |
| **隨機森林 (Random Forest, RF)** | 一種結合多棵決策樹的集成方法 (Ensemble Method)。能很好地處理複雜的交互作用。 | 在某些 UCI 數據集中達到 **99.9% 準確率**；在埃及 HCV 研究中為 94.06%。 |
| **貝氏分類器 (Naive Bayes, NB)** | 基於貝氏定理 (Bayes' Theorem) 的機率模型。簡單且易於擴展，適用於實時診斷。 | 達到約 90% 的準確率；對於早期患者分層 (Stratification) 非常有效。 |
| **K-近鄰演算法 (K-Nearest Neighbors, KNN)** | 根據特徵向量的相似性進行分類。 | 準確率介於 89.43% 到 98.1%，取決於 'K' 的取值。 |
| **支持向量機 (Support Vector Machines, SVM)** | 使用核函數 (Kernel Functions, 如 Gaussian/Linear) 在高維空間中有效運作。 | Gaussian RBF 核函數達到 **99.55% 準確率**。 |
| **人工神經網路 (Artificial Neural Networks, ANN)** | 模仿生物神經處理過程。 | 高性能，準確率約 96%，且均方誤差 (Mean Square Error) 極小。 |

---

## 3. 關鍵優化技術 (Key Optimization Techniques)
為了達到高準確率 (90%+)，研究人員採用了幾個關鍵的預處理和優化步驟：

### A. 特徵選擇 (Feature Selection)
*   **順序前向選擇 (Sequential Forward Selection, SFS)**：識別最相關的診斷特徵（例如特定的血液標記物）。
*   **排名搜索與資訊增益 (Ranker Search & Info-Gain)**：降低維度，專注於最具影響力的數據點。

### B. 數據不平衡與缺失值 (Data Imbalance & Missing Values)
*   **SMOTE (Synthetic Minority Over-sampling Technique)**：平衡數據集，解決感染病例遠少於健康病例的問題。
*   **均值/眾數插補 (Mean/Mode Imputation)**：填充缺失的臨床數據，確保模型的穩健性 (Robustness)。

### C. 超參數優化 (Hyperparameter Optimization)
*   **粒子群優化 (Particle Swarm Optimization, PSO)**：用於尋找 KNN 中的最佳 'K' 值，使準確率提升約 2%。
*   **隨機搜索 (Random Search)**：調整神經網路參數，使其性能超越預設設定。

---

## 4. 臨床意義 (Clinical Significance)
*   **早期檢測 (Early Detection)**：ML 允許在嚴重症狀出現之前識別肝炎階段。
*   **個性化治療 (Personalized Treatment)**：透過揭示關鍵診斷特徵，這些模型幫助醫生選擇量身定制的干預策略。
*   **擴展性 (Scalability)**：高通量 (High-throughput) 診斷工具使在資源有限的環境中進行篩查成為可能。

---

[回到大綱 (Back to Syllabus)](../SYLLABUS.md)

---

## 🌟 給小白的 AI 演算法大白話指南 (Layperson's Guide)

如果把「診斷肝炎」比喻成一場**醫生會診**，這五種演算法就像五位風格迥異的專家：

### 1. 隨機森林 (Random Forest, RF) —— 「專家陪審團」
*   **怎麼運作**：想像你有 100 個醫生，每個醫生都只看病人的一小部分症狀（比如 A 醫生看年齡，B 醫生看膽紅素）。最後，這 100 個醫生投票，票數最多的診斷結果就是最終答案。
*   **為什麼厲害**：因為它是「群眾的智慧」。就算其中一兩個醫生看走眼，整體的準確度（最高達 99.9%）依然非常穩健。

### 2. 貝氏分類器 (Naive Bayes, NB) —— 「算命大師（機率派）」
*   **怎麼運作**：它會根據歷史數據算機率。比如：「歷史上，眼白發黃且 ALT 數值高的人，有 90% 是肝炎」。它會把所有症狀出現的機率乘起來，算出你是肝炎的「勝算」有多少。
*   **為什麼厲害**：它反應極快，適合處理大量數據，雖然它假設各個症狀之間互不相關（這點很「天真/Naive」），但在現實中往往出奇地準。

### 3. K-近鄰演算法 (K-Nearest Neighbors, KNN) —— 「物以類聚」
*   **怎麼運作**：這就是「看你的朋友是誰，就知道你是誰」。AI 會把所有病人的數據畫在一個地圖上。當一個新病人進來時，AI 看他身邊最近的 K 個（比如 5 個）「鄰居」是誰。如果鄰居大都是肝炎患者，那這個病人極大機率也是。
*   **為什麼厲害**：非常直觀，不需要複雜的訓練過程，只要數據夠多，它就能像老中醫一樣憑「既視感」診斷。

### 4. 支持向量機 (Support Vector Machines, SVM) —— 「楚河漢界」
*   **怎麼運作**：它是一位「畫線高手」。它試圖在健康的人和生病的人之間，畫出一條最寬、最明顯的「分界線」。如果有人的數據落在線的左邊就是健康，右邊就是生病。
*   **為什麼厲害**：它非常擅長處理「非黑即白」的分類問題，特別是在數據維度非常複雜（比如同時考慮幾十種血液指標）時，它能找到那條最完美的界線。

### 5. 人工神經網路 (Artificial Neural Networks, ANN) —— 「超級大腦」
*   **怎麼運作**：它模仿人類大腦神經元的連接方式。數據會經過一層又一層的「神經元」處理，每一層都會捕捉一些肉眼看不見的細微特徵（比如年齡和某種蛋白質指標的微妙比例）。
*   **為什麼厲害**：它是目前 AI 的主流，擅長處理極其複雜、人類醫生也難以總結規律的隱藏特徵，準確率極高。
