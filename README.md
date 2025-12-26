# 病毒性肝炎學習系統 (Viral Hepatitis Learning System - VHLS)

> 一個系統化、模組化且可擴展的手冊，旨在幫助掌握病毒性肝炎 (Viral Hepatitis) 知識。

## 🎯 願景 (Vision)
本倉庫被設計為一個「活的筆記 (Living Book)」以及為醫學生、研究人員和醫療保健專業人士打造的結構化學習環境。透過使用模組化的 Markdown 方式，它可以輕鬆進行更新、社區貢獻，並與外部工具（如 Anki 或測驗引擎）整合。

## 📂 項目結構 (Project Structure)
```text
.
├── README.md               # 項目概覽與入口點
├── SYLLABUS.md             # 系統化學習路徑 (Learning Roadmap)
├── modules/                # 核心知識模組 (Core Knowledge Modules)
│   ├── 01_intro_comparison.md
│   ├── 12_ai_diagnostics_research.md
│   └── ...
├── data/                   # 用於自動化的結構化數據 (JSON/YAML)
│   ├── flashcards/
│   └── quizzes/
└── assets/                 # 圖表、圖表和媒體資源
```

## 🚀 開始學習 (Getting Started)
1. 從 [SYLLABUS.md](SYLLABUS.md) 開始，了解學習路徑。
2. 閱讀 [模組 01：導論與比較 (Module 01: Introduction & Comparison)](modules/01_intro_comparison.md) 獲取高層次概覽。
3. 使用大綱 (Syllabus) 中的複選框追蹤你的進度。

## 🛠️ 如何擴展 (How to Extend)
- **新增模組**：在 `modules/` 中建立一個新的 `.md` 文件，並在 `SYLLABUS.md` 中建立連結。
- **新增測驗數據**：按照建立的 Schema 在 `data/quizzes/` 中新增 JSON 文件。
- **改進內容**：歡迎提交基於證據 (Evidence-based) 的更新 Pull Requests。

---
*免責聲明：這是一個教育資源。在進行醫療決策時，請務必諮詢臨床指南（如 AASLD, EASL）。*
