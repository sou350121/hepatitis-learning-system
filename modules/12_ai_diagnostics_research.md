# Module 12: AI & Machine Learning in Hepatitis Diagnosis

> **Reference**: *Indonesian Journal of Computer Science*, Vol. 13, No. 3, 2024. ISSN: 2549-7286.

## 1. Introduction
Modern hepatology is increasingly leveraging Machine Learning (ML) to improve the accuracy, speed, and cost-effectiveness of hepatitis diagnosis. By analyzing clinical and laboratory findings (like age, gender, bilirubin, albumin, etc.), ML models can predict disease presence, severity, and patient outcomes.

---

## 2. Core Algorithms & Methodology

| Algorithm | Description | Performance Highlights |
| :--- | :--- | :--- |
| **Random Forest (RF)** | An ensemble method combining multiple decision trees. Handles complex interactions well. | Achieved **99.9% accuracy** in some UCI datasets; 94.06% in Egyptian HCV studies. |
| **Naive Bayes (NB)** | Probabilistic model based on Bayes' Theorem. Simple and scalable for real-time diagnostics. | Achieved ~90% accuracy; effective for early patient stratification. |
| **K-Nearest Neighbors (KNN)** | Classifies based on the similarity of feature vectors. | Accuracy varies (89.43% to 98.1%) depending on the value of 'K'. |
| **Support Vector Machines (SVM)** | Effective in high-dimensional spaces using kernel functions (Gaussian/Linear). | Gaussian RBF kernel reached **99.55% accuracy**. |
| **Artificial Neural Networks (ANN)** | Mimics biological neural processing. | High performance with ~96% accuracy and minimal Mean Square Error. |

---

## 3. Key Optimization Techniques
To reach high accuracy (90%+), researchers employ several critical preprocessing and optimization steps:

### A. Feature Selection
*   **Sequential Forward Selection (SFS)**: Identifies the most relevant diagnostic traits (e.g., specific blood markers).
*   **Ranker Search & Info-Gain**: Reduces dimensionality to focus on the most impactful data points.

### B. Data Imbalance & Missing Values
*   **SMOTE (Synthetic Minority Over-sampling Technique)**: Balances datasets where infected cases are much fewer than healthy cases.
*   **Mean/Mode Imputation**: Filling in missing clinical data to ensure model robustness.

### C. Hyperparameter Optimization
*   **Particle Swarm Optimization (PSO)**: Used to find the optimal 'K' in KNN, improving accuracy by ~2%.
*   **Random Search**: Tuning neural network parameters to boost performance beyond default settings.

---

## 4. Clinical Significance
*   **Early Detection**: ML allows for identification of hepatitis stages before severe symptoms manifest.
*   **Personalized Treatment**: By uncovering key diagnostic traits, these models help doctors choose tailored intervention strategies.
*   **Scalability**: High-throughput diagnostic tools enable screening in resource-limited environments.

---
[Back to Syllabus](../SYLLABUS.md)

---

## 🌟 給小白的 AI 演算法大白話指南

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

