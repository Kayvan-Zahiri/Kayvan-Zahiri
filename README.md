# Hi, I'm Kayvan 👋

**Speech and ML engineer** in San Francisco. M.S. Data Science & AI, University of San Francisco, 2026.
**Open to full-time roles** in speech, ML, or infrastructure.

Most of my recent work lives in other people's repositories: **36 pull requests merged into third-party production projects, 59 more in review.**

🌐 [Portfolio](https://kayvan-zahiri.github.io/Portfolio/) · 💼 [LinkedIn](https://www.linkedin.com/in/kayvan-zahiri/) · 📫 kzahiri@dons.usfca.edu

---

## Open source

**Merged**

- **[OpenAI Whisper #2836](https://github.com/openai/whisper/pull/2836)** — the English text normalizer rewrote the `1` inside `3.1` and `1%`, silently deleting the percent sign. It ran on both sides of every WER comparison, so the scores never moved and nothing flagged it. Merged by a Whisper paper author.
- **[Google SentencePiece #1320](https://github.com/google/sentencepiece/pull/1320)** — `and` returns its operand, not a bool, so on an empty batch the `return_bytes` flag became `[]` instead of `False` and reached the binding as a list where a bool was expected. Every other `return_type` gave `[]`; `offset_mapping` raised `TypeError`. Merged by Taku Kudo, who wrote SentencePiece.
- **[torchmetrics #3455](https://github.com/Lightning-AI/torchmetrics/pull/3455)** — PESQ raised on any sample the backend could not score, taking the whole batch down with it; those samples now return `nan` and the rest of the batch survives.
- **[Meta FAISS](https://github.com/facebookresearch/faiss/commit/b4c66ba)** — `index_factory` round-trips dropped the storage index for HNSW, so rebuilding from the returned string gave you a different index.
- **[uv #21144](https://github.com/astral-sh/uv/pull/21144) and [#21146](https://github.com/astral-sh/uv/pull/21146)** — both merged by Astral's co-founder.
- **[Hugging Face Transformers #47888](https://github.com/huggingface/transformers/pull/47888)** — the ASR pipeline destroyed stereo audio in channels-last layout.
- **[librosa #2087](https://github.com/librosa/librosa/pull/2087)** — merged by the library's creator.
- **Python SDKs:** [Deepgram #767](https://github.com/deepgram/deepgram-python-sdk/pull/767), [ElevenLabs #858](https://github.com/elevenlabs/elevenlabs-python/pull/858), [AssemblyAI #234](https://github.com/AssemblyAI/assemblyai-python-sdk/pull/234).

**In review:** [ONNX Runtime](https://github.com/microsoft/onnxruntime/pull/32376), [NVIDIA NeMo](https://github.com/NVIDIA-NeMo/Speech/pull/16200), [PyTorch Audio](https://github.com/pytorch/audio/pull/4227), [SciPy](https://github.com/scipy/scipy/pull/25923), [scikit-learn](https://github.com/scikit-learn/scikit-learn/pull/34716), and the [Anthropic Python SDK](https://github.com/anthropics/anthropic-sdk-python/pull/1906).

---

## Projects

**[asr-age-gap](https://github.com/Kayvan-Zahiri/asr-age-gap) — who voice systems leave out**
Whisper transcribes older speakers *more* accurately, not less. The failure is elsewhere: at a fixed 700ms endpoint threshold, speakers in their sixties are read as finished mid-sentence 19.7% of the time against 8.0% in their twenties, because they take about twice as many internal pauses. Word error rate cannot see it. A semantic turn model halves the gap.
`Whisper` · `Common Voice` · `speaker-bootstrapped CIs`

**[state-of-ats-2026](https://github.com/Kayvan-Zahiri/state-of-ats-2026) — which ATS each large employer uses**
Open dataset covering 738 large employers, 704 verified against the live careers-portal apply host, 551 with a recorded evidence host you can check yourself. MIT licensed, free keyless API.

**[ResumeAI](https://withresumeai.com) — ATS resume optimizer**
Full-stack AI product I founded and built solo: compatibility scoring, bullet rewriting, cover letters, PDF/DOCX export, Chrome extension. Active users across 7+ countries.
`Next.js` · `TypeScript` · `Supabase` · `Claude API` · `Stripe`

**[ParkCast SF](https://github.com/Brandonminer333/ml-ops-final-project-team-ParkCast-SF) — end-to-end MLOps**
Parking-occupancy API serving 12.7K SF blocks at 8.98 MAE / 0.73 R². Automated retraining with a champion-challenger gate that blocks silent regressions before deploy.
`FastAPI` · `LightGBM` · `Docker` · `Cloud Run` · `MLflow`

→ More on my [portfolio site](https://kayvan-zahiri.github.io/Portfolio/).

---

## Tech

**Languages:** Python · TypeScript · Java · C · SQL
**AI/ML:** PyTorch · Whisper · LiveKit · scikit-learn · LLM fine-tuning · RAG · model evaluation
**Data:** PySpark · Pandas · NumPy · Dagster · dlt/dbt · Airflow
**Infra:** AWS · GCP · Docker · MLflow · GitHub Actions

---

## Experience

**AI Engineer, Asurion** (through June 2026) — real-time voice AI: Whisper fine-tuning and low-latency LiveKit pipelines in production.
Previously **Spotly Jobs** (dlt/dbt + Dagster ETL) and **Outlier AI** (RLHF training and LLM evaluation).

🏅 AWS Certified Cloud Practitioner · Google Cloud Digital Leader
