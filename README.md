# Viral Hepatitis Learning System (VHLS)

> A systematic, modular, and extensible handbook for mastering viral hepatitis.

## 🎯 Vision
This repository is designed to be a "living book" and a structured learning environment for medical students, researchers, and healthcare professionals. By using a modular Markdown approach, it allows for easy updates, community contributions, and integration with external tools (like Anki or quiz engines).

## 📂 Project Structure
```text
.
├── README.md               # Project overview and entry point
├── SYLLABUS.md             # The systematic learning roadmap
├── modules/                # Core knowledge modules
│   ├── 01_intro_comparison.md
│   ├── 02_hepta_b_deep_dive.md
│   └── ...
├── data/                   # Structured data (JSON/YAML) for automation
│   ├── flashcards/
│   └── quizzes/
└── assets/                 # Diagrams, charts, and media
```

## 🚀 Getting Started
1. Start with the [SYLLABUS.md](SYLLABUS.md) to understand the learning path.
2. Read [Module 01: Introduction & Comparison](modules/01_intro_comparison.md) for a high-level overview.
3. Track your progress using the checkboxes in the Syllabus.

## 🛠️ How to Extend
- **Add a Module**: Create a new `.md` file in `modules/` and link it in `SYLLABUS.md`.
- **Add Quiz Data**: Add a JSON file to `data/quizzes/` following the established schema.
- **Improve Content**: Pull requests are welcome for evidence-based updates.

---
*Disclaimer: This is an educational resource. Always consult clinical guidelines (e.g., AASLD, EASL) for medical decision-making.*

