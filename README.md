<!-- Profile README for mkavinkumar1 -->

<h1 align="center">Kavinkumar M</h1>

<p align="center">
  <b>AI Engineer @ NeuralMetrics</b> · Python · FastAPI · LLM systems<br/>
  Building <b>CHRIS</b>, an autonomous premium-audit agent for US commercial insurance.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/mkvn"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://huggingface.co/mkvn"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-FFD21E?style=flat-square&logoColor=black" alt="Hugging Face" /></a>
  <a href="https://doi.org/10.5281/zenodo.21856981"><img src="https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21856981-1682D4?style=flat-square" alt="Zenodo DOI" /></a>
  <a href="mailto:mkavinkumar1@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

---

### About

I build AI systems that replace work people shouldn't have to do by hand.

- 6+ years shipping production Python — now building autonomous agents end to end.
- At **NeuralMetrics**: CHRIS validates audit data, detects the classification errors that move premium, adapts to compliance rules that shift by state and year, and analyzes risk exposure.
- Day-to-day: FastAPI, PostgreSQL, the Claude API, Model Context Protocol, and AWS (Lambda, Bedrock, ECS/ECR, S3, RDS).
- Interested in agent architectures, MoE inference systems, applied NLP, and InsurTech.

---

### Research

**[Quantization as Cache Amplification: Trillion-Parameter Mixture-of-Experts Inference on a Commodity Laptop](https://doi.org/10.5281/zenodo.21856981)**
📄 [Paper (Zenodo, DOI 10.5281/zenodo.21856981)](https://zenodo.org/records/21856981) · 📊 [Traces, code & artefacts (Hugging Face)](https://huggingface.co/datasets/mkvn/quantization-cache-amplification)

Weight quantization is usually sold as footprint reduction. This paper shows that for
offloaded Mixture-of-Experts inference the real lever is *cache capacity*: an LRU expert
cache hits **exactly 0%** whenever it holds fewer than the `k·L` expert slots a single
token touches — a phase transition measured on real routing traces — and quantization is
what carries a system across it.

| Result | Value |
| --- | --- |
| LRU hit rate below per-token working set | **0.0%** (all capacities tested) |
| Popularity-pinned cache @ 10% capacity | **22.9%** (vs 0.0% for LRU) |
| Frequency-conditioned allocation @ 1.51 bits | **22.02 PPL** vs 25.54 uniform (13.8% better at identical rate) |
| Sub-2-bit codec @ 2.01 bits, WikiText-2 | 12.17 PPL (bf16 reference: 8.11) |

Everything was measured on one laptop (RTX A500, 4 GB VRAM; 32 GB DRAM; consumer NVMe) —
sub-2-bit codec, raw OLMoE-1B-7B routing traces, and every measurement artefact behind the numbers.

---

### What I'm building

| Project | What it is |
| --- | --- |
| **[ssh-mcp](https://github.com/mkavinkumar1/ssh-mcp)** | My own MCP server for remote development over SSH — files, commands, search, git, and binary-safe SFTP transfer via Paramiko. Cross-platform, Python. |
| **CHRIS** *(private, @ NeuralMetrics)* | Autonomous premium-audit agent for US commercial insurance: data validation, classification-error detection, dynamic regulatory compliance, risk-exposure analysis. |
| **[quantization-cache-amplification](https://huggingface.co/datasets/mkvn/quantization-cache-amplification)** | Codec, routing traces and benchmarks behind the MoE paper above. |

---

### Open source

- **[OpenHands](https://github.com/OpenHands/OpenHands)** (formerly OpenDevin) — [#3285](https://github.com/OpenHands/OpenHands/pull/3285) *merged*: clear history at the start of a new task.
- **[LiteLLM](https://github.com/BerriAI/litellm)** — [#10548](https://github.com/BerriAI/litellm/pull/10548) *merged*: Gemini 2.5 Pro max_tokens fix · [#17298](https://github.com/BerriAI/litellm/pull/17298): proposed Claude Code provider integration.
- **[freqtrade](https://github.com/freqtrade/freqtrade)** — merged: [#6545](https://github.com/freqtrade/freqtrade/pull/6545) partial exit using average price, [#6540](https://github.com/freqtrade/freqtrade/pull/6540), [#6432](https://github.com/freqtrade/freqtrade/pull/6432).
- **[NostalgiaForInfinity](https://github.com/iterativv/NostalgiaForInfinity)** — 7 merged PRs on leverage handling, trailing stops and backtesting.
- **[openai/codex](https://github.com/openai/codex)** — [running my own fork](https://github.com/mkavinkumar1/codex) and taking part in issue discussions.

---

### Tech

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/-SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white)
![Pytest](https://img.shields.io/badge/-Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![Scrapy](https://img.shields.io/badge/-Scrapy-60A839?style=flat-square&logo=scrapy&logoColor=white)

![Claude](https://img.shields.io/badge/-Claude%20API-D97757?style=flat-square&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/-Model%20Context%20Protocol-1A1A1A?style=flat-square)
![Hugging Face](https://img.shields.io/badge/-Hugging%20Face-FFD21E?style=flat-square&logoColor=black)

![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white)

---

### Certifications

**Anthropic** — Building with the Claude API · Claude Code in Action · Model Context Protocol: Advanced Topics · Introduction to agent skills · Introduction to subagents · Claude with Amazon Bedrock · Claude on Google Cloud

**Cisco** — [Python Essentials 1](https://www.credly.com/badges/7c05cc21-016a-4b37-a626-88fb131c8ea0/public_url) · [Python Essentials 2](https://www.credly.com/badges/b9c1222a-3b28-4ab5-b667-bf455e3514b0/public_url)

---

### Contribution stats

<a href="https://github.com/mkavinkumar1"><img align="center" width="49%" src="./header.svg" alt="Overview" /></a>
<a href="https://github.com/mkavinkumar1"><img align="center" width="49%" src="./iso_calendar.svg" alt="Isometric contribution calendar" /></a>

<a href="https://github.com/mkavinkumar1"><img align="center" width="49%" src="./languages.svg" alt="Most used languages" /></a>
<a href="https://github.com/mkavinkumar1"><img align="center" width="49%" src="./repositories.svg" alt="Repositories" /></a>

<sub>Panels regenerate daily via <a href="https://github.com/lowlighter/metrics">lowlighter/metrics</a>.</sub>

<p align="center">
  <a href="https://www.linkedin.com/in/mkvn">LinkedIn</a> ·
  <a href="https://huggingface.co/mkvn">Hugging Face</a> ·
  <a href="https://zenodo.org/records/21856981">Zenodo</a> ·
  <a href="mailto:mkavinkumar1@gmail.com">mkavinkumar1@gmail.com</a>
</p>
