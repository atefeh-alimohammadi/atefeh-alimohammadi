# Hi, I'm Atefeh

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

### My Contributions

This project was developed collaboratively by two team members as part of our BSc thesis. Most aspects of the project were carried out jointly, with both team members contributing across model adaptation, implementation, experimentation, evaluation, and documentation.

My contributions included:

- Co-adapting an existing video-based emotion recognition architecture for personality recognition using our target dataset.
- Collaboratively developing and refining the model implementation, data pipeline, and training, validation, and testing workflows.
- Jointly conducting experiments, evaluating model performance, comparing different configurations, and analyzing results.
- Contributing to methodological decisions, debugging, and integrating facial-frame and landmark-based inputs.
- Collaboratively documenting the methodology, interpreting findings, and writing and revising the thesis report.

![Vision Transformer](https://img.shields.io/badge/Vision_Transformer-555555?style=flat-square)
![Computer Vision](https://img.shields.io/badge/Computer_Vision-555555?style=flat-square)

[Repository](https://github.com/YOUR_USERNAME/THESIS_REPO)

## Technical Skills

### Programming Languages

**Advanced:** Python · Java

**Beginner:** C · C++

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square\&logo=openjdk\&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square\&logo=c\&logoColor=black)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square\&logo=cplusplus\&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square\&logo=typescript\&logoColor=white)

### Machine Learning & Deep Learning

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square\&logo=pytorch\&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square\&logo=tensorflow\&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat-square\&logo=keras\&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square\&logo=scikitlearn\&logoColor=white)
![fastai](https://img.shields.io/badge/fastai-00A98F?style=flat-square)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square\&logo=numpy\&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square\&logo=scipy\&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square\&logo=pandas\&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-EC6B23?style=flat-square)

Classification · Regression · Transfer Learning · Feature Engineering · Hyperparameter Tuning · Model Training and Evaluation · Transformers · Attention Mechanisms

### NLP & LLM Engineering

![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square\&logo=huggingface\&logoColor=black)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square\&logo=ollama\&logoColor=white)

Text Preprocessing · Persian NLP · Sentiment Analysis · Text Classification · Speech Recognition · Word Embeddings · N-gram Language Models · Semantic Search · Retrieval-Augmented Generation (RAG) · Structured JSON Extraction · Prompt Design

### Computer Vision

![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square\&logo=opencv\&logoColor=white)
![ResNet](https://img.shields.io/badge/ResNet-555555?style=flat-square)
![Vision Transformer](https://img.shields.io/badge/Vision_Transformer-555555?style=flat-square)

Facial Landmark Features · Video-based Modeling · Image Classification · Visual Feature Fusion · CNN Architectures

### Backend & Databases

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square\&logo=fastapi\&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square\&logo=django\&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square\&logo=pydantic\&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square\&logo=sqlalchemy\&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square\&logo=postgresql\&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square\&logo=sqlite\&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-336791?style=flat-square)

SQL · Relational Database Design · REST APIs

### Frontend

![React](https://img.shields.io/badge/React-20232A?style=flat-square\&logo=react\&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square\&logo=nextdotjs\&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square\&logo=typescript\&logoColor=white)

### Data Science & Scientific Computing

![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square\&logo=jupyter\&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-0076A8?style=flat-square\&logo=mathworks\&logoColor=white)

Data Analysis · Data Preprocessing · Data Visualization · Statistical Evaluation · Computational Modeling · Information Theory

### Tools & Platforms

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square\&logo=git\&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square\&logo=github\&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square\&logo=postman\&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat-square\&logo=figma\&logoColor=white)

### Additional Skills

**Experimental Design & Model Evaluation**

* Baseline comparisons and ablation studies
* Error analysis and model diagnostics
* Classification and regression metrics
* Bootstrap analysis and McNemar's test
* Synthetic dataset generation and hard-negative construction
* Temporal sequence modeling and counterfactual evaluation

**Natural Language Processing**

* Persian text processing and part-of-speech analysis
* N-gram-based text autocomplete
* Spell checking and word cloud generation
* Text-based personality-trait estimation using CNN architectures
* Speech recognition with pretrained models

**Computational Neuroscience**

* Neural encoding and decoding
* Information theory and mutual information
* Single-neuron modeling, including Leaky Integrate-and-Fire and Hodgkin–Huxley models
* Synaptic plasticity, Hebbian learning and STDP
* Recurrent network dynamics and attractor networks

**Data & Software Development**

* Dataset construction, splitting and validation
* Relational database design and SQL query development
* Object-oriented programming and modular software development

**UI/UX Research & Design**
Figma

## Contact

[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square\&logo=gmail\&logoColor=white)](mailto:atefehalimohammadi00163@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square)](https://www.linkedin.com/in/atefe-alimohammadi-1798b2237)
