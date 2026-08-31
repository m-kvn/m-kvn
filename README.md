<!-- Profile README for m-kvn -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=soft&color=0:0D1117,50:A03D22,100:D97757&height=190&section=header&text=Kavinkumar%20M&fontSize=50&fontColor=FFFFFF&fontAlignY=38&desc=AI%20Engineer%20%C2%B7%20Autonomous%20Agents%20%C2%B7%20LLM%20Systems&descAlignY=57&descSize=17&animation=none" width="100%" alt="Kavinkumar M — AI Engineer" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&duration=2800&pause=900&color=D97757&center=true&vCenter=true&width=760&lines=AI+Engineer+%40+NeuralMetrics;Building+CHRIS+%E2%80%94+an+autonomous+premium-audit+agent;Python+%C2%B7+FastAPI+%C2%B7+Claude+API+%C2%B7+MCP+%C2%B7+AWS;Trillion-parameter+MoE+inference+on+a+4+GB+laptop" alt="AI Engineer @ NeuralMetrics · Building CHRIS · Python, FastAPI, Claude API, MCP, AWS" />
</p>

<p align="center">
  <b>AI Engineer @ NeuralMetrics</b> · Python · FastAPI · LLM systems<br/>
  Building <b>CHRIS</b>, an autonomous premium-audit agent for US commercial insurance.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/mkvn"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://huggingface.co/mkvn"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-FFD21E?style=flat-square&logoColor=black" alt="Hugging Face" /></a>
  <a href="https://doi.org/10.5281/zenodo.21856981"><img src="https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21856981-1682D4?style=flat-square" alt="Zenodo DOI" /></a>
  <a href="mailto:mkavinkumar1@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://komarev.com/ghpvc/?username=m-kvn&style=flat-square&color=D97757&label=Profile+views" alt="Profile views" />
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
| **[ssh-mcp](https://github.com/m-kvn/ssh-mcp)** | My own MCP server for remote development over SSH — files, commands, search, git, and binary-safe SFTP transfer via Paramiko. Cross-platform, Python. |
| **CHRIS** *(private, @ NeuralMetrics)* | Autonomous premium-audit agent for US commercial insurance: data validation, classification-error detection, dynamic regulatory compliance, risk-exposure analysis. |
| **[quantization-cache-amplification](https://huggingface.co/datasets/mkvn/quantization-cache-amplification)** | Codec, routing traces and benchmarks behind the MoE paper above. |

---

### Open source

- **[OpenHands](https://github.com/OpenHands/OpenHands)** (formerly OpenDevin) — [#3285](https://github.com/OpenHands/OpenHands/pull/3285) *merged*: clear history at the start of a new task.
- **[LiteLLM](https://github.com/BerriAI/litellm)** — [#10548](https://github.com/BerriAI/litellm/pull/10548) *merged*: Gemini 2.5 Pro max_tokens fix · [#17298](https://github.com/BerriAI/litellm/pull/17298): proposed Claude Code provider integration.
- **[freqtrade](https://github.com/freqtrade/freqtrade)** — merged: [#6545](https://github.com/freqtrade/freqtrade/pull/6545) partial exit using average price, [#6540](https://github.com/freqtrade/freqtrade/pull/6540), [#6432](https://github.com/freqtrade/freqtrade/pull/6432).
- **[NostalgiaForInfinity](https://github.com/iterativv/NostalgiaForInfinity)** — 7 merged PRs on leverage handling, trailing stops and backtesting.
- **[openai/codex](https://github.com/openai/codex)** — [running my own fork](https://github.com/m-kvn/codex) and taking part in issue discussions.

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

<p>
  <img src="https://cdn.simpleicons.org/anthropic/D97757" height="18" align="top" alt="Anthropic" />&nbsp;<b>Anthropic</b><br/>
  <a href="https://verify.skilljar.com/c/yvwtrnyfoki8">Building with the Claude API</a> ·
  <a href="https://verify.skilljar.com/c/8q25r73fhfib">Claude Code in Action</a> ·
  <a href="https://verify.skilljar.com/c/r7wuvekb3aa9">Model Context Protocol: Advanced Topics</a> ·
  <a href="https://verify.skilljar.com/c/ashmtpsoee6v">Introduction to agent skills</a> ·
  <a href="https://verify.skilljar.com/c/zjazzxmsn28f">Introduction to subagents</a> ·
  <a href="https://verify.skilljar.com/c/n4zc264nzxyj">Claude with Amazon Bedrock</a> ·
  <a href="https://verify.skilljar.com/c/t6r2tv6iia5x">Claude on Google Cloud</a>
</p>

<p>
  <img src="https://cdn.simpleicons.org/cisco/1BA0D7" height="18" align="top" alt="Cisco" />&nbsp;<b>Cisco</b><br/>
  <a href="https://www.credly.com/badges/7c05cc21-016a-4b37-a626-88fb131c8ea0/public_url">Python Essentials 1</a> ·
  <a href="https://www.credly.com/badges/b9c1222a-3b28-4ab5-b667-bf455e3514b0/public_url">Python Essentials 2</a>
</p>

---

### Contribution stats

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com?user=m-kvn&theme=dark&hide_border=true&border_radius=6&date_format=j%20M%5B%20Y%5D&ring=D97757&fire=D97757&currStreakLabel=D97757" />
    <source media="(prefers-color-scheme: light)" srcset="https://streak-stats.demolab.com?user=m-kvn&theme=default&hide_border=true&border_radius=6&date_format=j%20M%5B%20Y%5D&ring=D97757&fire=D97757&currStreakLabel=D97757" />
    <img width="72%" src="https://streak-stats.demolab.com?user=m-kvn&theme=default&hide_border=true&border_radius=6&date_format=j%20M%5B%20Y%5D&ring=D97757&fire=D97757&currStreakLabel=D97757" alt="Contribution streak" />
  </picture>
</p>

<a href="https://github.com/m-kvn"><img align="center" width="49%" src="./header.svg" alt="Overview" /></a>
<a href="https://github.com/m-kvn"><img align="center" width="49%" src="./iso_calendar.svg" alt="Isometric contribution calendar" /></a>

<a href="https://github.com/m-kvn"><img align="center" width="49%" src="./languages.svg" alt="Most used languages" /></a>
<a href="https://github.com/m-kvn"><img align="center" width="49%" src="./repositories.svg" alt="Repositories" /></a>

<sub>Panels regenerate daily via <a href="https://github.com/lowlighter/metrics">lowlighter/metrics</a>.</sub>

<p align="center">
  <a href="https://www.linkedin.com/in/mkvn">LinkedIn</a> ·
  <a href="https://huggingface.co/mkvn">Hugging Face</a> ·
  <a href="https://zenodo.org/records/21856981">Zenodo</a> ·
  <a href="mailto:mkavinkumar1@gmail.com">mkavinkumar1@gmail.com</a>
</p>

<img src="https://capsule-render.vercel.app/api?type=soft&color=0:D97757,50:A03D22,100:0D1117&height=110&section=footer&animation=none" width="100%" alt="" />
