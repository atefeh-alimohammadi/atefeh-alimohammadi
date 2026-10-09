# Hi, I'm Atefeh 👋

**Computer Engineering Graduate, University of Isfahan | AI & Machine Learning**

I'm interested in how machine learning can help us understand complex data, build intelligent systems, and solve practical problems. My background spans academic research and hands-on development across deep learning, computer vision, and LLM-based applications.

Through my projects, I've explored both training models and building applications around them. I enjoy investigating how models behave, evaluating their strengths and limitations, and understanding what makes an approach work beyond its headline metrics.

I'm looking to deepen my expertise in machine learning and AI engineering, take on challenging technical problems, and build reliable AI systems grounded in thoughtful experimentation.

**Interests:** Machine Learning · Deep Learning · Computer Vision · LLMs · Computational Neuroscience

**Open to:** AI Engineer · ML Engineer · AI-focused Software Engineer

## Featured Projects

### Socia: local-first AI companion for communication patterns

A conversational companion that remembers meaningful details, surfaces recurring communication patterns, and lets the user choose which ones to work on through adaptive multi-day "Journeys".

* **Local LLM stack:** Chat, analysis and embeddings run through Ollama (`qwen2.5:7b`, `nomic-embed-text`).
* **Retrieval-augmented memory:** Conversation events are embedded and stored in PostgreSQL with pgvector. At response time, relevant memories are retrieved by cosine distance (with a similarity cutoff and recency fallback) and injected into the model prompt.
* **Structured signal extraction:** Background LLM analysis returns JSON for emotions, behaviors and entities, validated against controlled vocabularies and confidence bounds.
* **Pattern memory with provenance:** Recurring signals are consolidated into versioned pattern memories linked to their supporting evidence.
* **User-chosen Journeys:** A journey starts from a detected pattern, and each daily challenge is generated from the previous outcome (completed, skipped, difficulty feedback).
* **Safeguards:** Includes rule-based screening for self-harm-related content, an LLM consistency check with one regeneration retry, and a feedback-driven pacing policy. These are application-level safeguards, not clinical risk assessments or a substitute for professional or emergency support.
* **Pattern detection limitations:** The current application uses a count-based rule that flags a behavioral tag after three or more occurrences. The experimental Transformer in `Socia/ml` is separate from the production flow and has not replaced this rule.
* **Application stack:** FastAPI REST API with token authentication, plus a Next.js/TypeScript frontend with progress charts.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square\&logo=fastapi\&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square\&logo=postgresql\&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-336791?style=flat-square)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square\&logo=ollama\&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square\&logo=nextdotjs\&logoColor=white)

[Repository](https://github.com/YOUR_USERNAME/SOCIA_REPO)

### Recurring-pattern detection with a custom Transformer (experimental, `Socia/ml`)

Socia currently flags a pattern when a tag appears three or more times. This experiment asks whether a sequence model can tell genuine recurring patterns from reordered or too-slow event sequences.

* Built a reproducible **synthetic dataset generator**: 400 simulated users, 15 event categories, held-out pattern identities, control users, and hard negatives.
* Implemented a **PyTorch Transformer** with learned relative-time attention bias, order embeddings, Time2Vec, and attention pooling, with isolated ablation variants (V1 to V4).
* Compared against a **count-based heuristic, WINEPI-style episode mining, and density baselines**; evaluated with ablations, matched-pair stress tests, and bootstrap / McNemar tests.
* Diagnostics showed the model relied heavily on same-category recurrence timing and was only weakly order-sensitive, which motivated the later variants.
* **Status:** Experimental, trained on synthetic data only, not integrated into Socia, and not validated on real conversations.

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square\&logo=pytorch\&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square\&logo=scikitlearn\&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square\&logo=numpy\&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square\&logo=scipy\&logoColor=white)

[Code](https://github.com/YOUR_USERNAME/SOCIA_REPO/tree/main/ml)

### Personality-trait estimation from facial video (undergraduate thesis, co-authored)

Estimates apparent Big Five traits from short video clips by adapting the S2D static-to-dynamic Vision Transformer, originally built for facial expression recognition.

* Fused face-frame and facial-landmark inputs using MCP and TMA modules; initialised the static branch from AffectNet-7 weights.
* Replaced the classification head with a five-output regression head for continuous trait scores.
* Evaluated overall and per trait with MA, CCC and RMSE on a 20% held-out split: **MA 0.886, CCC 0.381**.
* Trained at 112×112 input and shallow depth because of compute limits.

**My Contributions**

This project was developed collaboratively by two team members as part of our BSc thesis. Most components, including model implementation, data handling, and experiments, were co-developed. My contributions included:

* Co-developed the model architecture and fine-tuning pipeline.
* Implemented and adapted parts of the training, validation, and testing engine.
* Helped integrate facial-frame and landmark inputs.
* Collaborated on interpreting results and writing the thesis report.

![Vision Transformer](https://img.shields.io/badge/Vision_Transformer-555555?style=flat-square)
![Computer Vision](https://img.shields.io/badge/Computer_Vision-555555?style=flat-square)

[Repository](https://github.com/YOUR_USERNAME/THESIS_REPO)

## Technical Skills

**Languages**

**Advanced:** Python · Java

**Beginner:** C · C++

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square\&logo=openjdk\&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square\&logo=c\&logoColor=black)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square\&logo=cplusplus\&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square\&logo=typescript\&logoColor=white)


**Machine Learning & Deep Learning**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square\&logo=pytorch\&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square\&logo=scikitlearn\&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square\&logo=numpy\&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square\&logo=scipy\&logoColor=white)

Transformers and attention · transfer learning · model evaluation (baselines, ablations, significance testing)

**NLP & LLM Engineering**

![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square\&logo=ollama\&logoColor=white)

Local LLM inference · embeddings and semantic search · retrieval-augmented generation · structured JSON extraction · prompt design

**Computer Vision**

Vision Transformers · facial landmarks · video-based modeling

**Backend & Databases**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square\&logo=fastapi\&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square\&logo=pydantic\&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square\&logo=sqlalchemy\&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square\&logo=postgresql\&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-336791?style=flat-square)


## Contact

[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square\&logo=gmail\&logoColor=white)](mailto:atefehalimohammadi00163@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square)](https://www.linkedin.com/in/atefe-alimohammadi-1798b2237)
