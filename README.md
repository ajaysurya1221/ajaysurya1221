# Ajay Surya Senthilrajan

**AI & Machine Learning Engineering · Document AI, retrieval agents and evaluation**

I build document-processing systems, contribute to agentic retrieval workflows, and develop open-source tools for testing agent reliability. At Redica, I owned OCR engineering from server and model selection through resource optimization on EC2.

**Open to senior individual contributor roles across applied AI, generative AI and machine learning.** Bengaluru first, Chennai second. Available immediately.

[LinkedIn](https://www.linkedin.com/in/ajay-surya-senthilrajan/) · [Email](mailto:ajaysuryasenthilrajan@gmail.com)

## Start with two working demonstrations

### [ARCI — regression testing for AI agents](https://github.com/ajaysurya1221/agent-reliability-ci)

**Problem:** an agent change can behave differently when a tool times out or fails.

**What I built:** a Python CLI and GitHub Action for comparing agent versions on declared tasks and faults, inspecting differences and replaying recorded failures offline.

**Try it:** the seeded retry fixture checks a broken candidate and a repair. Requires macOS/Linux and [uv](https://docs.astral.sh/uv/). Initial setup downloads packages; the fixture makes no model calls.

```bash
uvx --python 3.12 --from 'agent-reliability-ci==1.0.0' arci demo --workers 4
```

The command exits **0 when the expected outcomes hold**, including the intended **BLOCK** for the broken candidate. Results apply to the tested tasks and faults; a recorded difference is not proof of root cause. [Demo details and limits](https://github.com/ajaysurya1221/agent-reliability-ci#try-the-offline-demo).

### [Actseal — evidence for a fixed action policy](https://github.com/ajaysurya1221/actseal)

**Problem:** accepting more actions can also mean accepting more actions that disagree with the labels.

**What I built:** a Python toolkit that evaluates a fixed policy on labelled cases, computes bounds on accepted-action risk and coverage, and records evidence for offline replay.

**Try it:** use a new output directory. The demo compares bad and fixed fixtures and checks their replay; no model or API key is needed.

```bash
uvx --python 3.12 --from 'actseal==1.0.1' actseal demo --out ./actseal-demo
```

The complete demo exits **0** after the expected bad-fixture **BLOCK** and fixed-fixture **PASS**. Replay checks consistency with recorded evidence; it does not authenticate responses or establish that labels are true.

[Watch the recorded fixture demonstrations](showcase/README.md) · [Engineering evidence sheet](showcase/EVIDENCE.md)

Recordings retain their original runtime versions, time compression, annotations and documented limits. They are historical demonstrations and may predate the pinned releases above.

## Engineering experience

**Redica Systems · Data Engineer II (MLE)**

I owned the OCR and document-processing workstream: server and model selection, page chunking, disk-backed intermediate results, concurrency controls and buffer cleanup for processing within EC2 memory constraints. I built page-level quality checks, controlled OCR retries, required-field validation and review signals for unreliable output.

I contributed to the wider agentic AI platform through GraphRAG and text-to-SQL retrieval workflows, MCP tools and agent memory. I worked with Product and distributed engineering teams to deliver these features through FastAPI services on AWS. Employer implementation and customer material remain private.

**Zolvit (formerly Vakilsearch) · Software Engineer - ML**

I built hybrid legal-document search, summarisation and extraction systems, and adapted open-source language models through continued pre-training and parameter-efficient fine-tuning.

**Working tools:** Python, FastAPI, AWS, PyTorch and Docker.

## Supporting projects

- [Dorian](https://github.com/ajaysurya1221/dorian): rechecks explicit code claims after changes. A claim is only as strong as its checker.
- [Frontier Scout](https://github.com/ajaysurya1221/frontier-scout): checks declared pull-request scope against base policy. Research preview.
- [Evalopt Graph](https://github.com/ajaysurya1221/evalopt-graph): applies acceptance rules to supplied evidence. Standalone feature development has ended.

These projects provide bounded testing and evidence; they do not establish production safety or customer adoption. I use AI coding assistants as pair-programmers.
