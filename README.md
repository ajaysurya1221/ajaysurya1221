# Ajay Surya Senthilrajan

**AI / GenAI engineer · Document intelligence, retrieval agents and evaluation**

At **Redica Systems**, as **Data Engineer II (MLE)**, I build document-intelligence and retrieval-agent capabilities. My work includes OCR for documents of **3,000+ pages**, GraphRAG, text-to-SQL, MCP tools and agent memory. I deliver LLM features across retrieval design, prompting, evaluation, FastAPI services and AWS deployment, working with Product and distributed engineering teams.

Previously, as **Software Engineer – ML** at **Zolvit (formerly Vakilsearch)**, I built hybrid legal-document search, summarisation and extraction systems, and adapted open-source language models through continued pre-training and parameter-efficient fine-tuning.

**Working tools:** Python, FastAPI, AWS, PyTorch and Docker.

**Seeking Senior AI / GenAI Engineer and Senior Machine Learning Engineer roles.** Bengaluru preferred; Chennai also considered. Available to join immediately.

[LinkedIn](https://www.linkedin.com/in/ajay-surya-senthilrajan/) · [Email](mailto:ajaysuryasenthilrajan@gmail.com)

## Public engineering

I build independent testing and evidence tools for agent controls. Start with **ARCI** to see an experiment, a regression decision, failure diagnosis and offline replay in one runnable fixture.

| Project | What it does | Published version |
|---|---|---|
| [ARCI](https://github.com/ajaysurya1221/agent-reliability-ci) | Runs predeclared baseline/candidate experiments under tool faults, applies non-inferiority gates and replays recorded failures. | [0.8.0](https://pypi.org/project/agent-reliability-ci/0.8.0/) |
| [Actseal](https://github.com/ajaysurya1221/actseal) | Tests a frozen categorical action policy against labelled cases, bounds accepted-action risk and coverage, and replays the evidence. | [1.0.1](https://pypi.org/project/actseal/1.0.1/) |
| [Dorian](https://github.com/ajaysurya1221/dorian) | Turns explicit code claims into executable checks and revalidates them after changes. | [1.4.1](https://pypi.org/project/dorian-vwp/1.4.1/) |
| [Frontier Scout](https://github.com/ajaysurya1221/frontier-scout) | Checks declared PR scope against base-commit policy and compiles policy into Claude Code permissions and hooks. Research preview. | [2.2.0](https://pypi.org/project/frontier-scout/2.2.0/) |
| [Evalopt Graph](https://github.com/ajaysurya1221/evalopt-graph) | Evaluates supplied gates, claims and evidence against acceptance policy. Standalone feature development has ended; the kernel and research record remain available. | [0.1.1](https://pypi.org/project/evalopt-graph/0.1.1/) |

## Run the ARCI retry demo

Requires macOS/Linux and [uv](https://docs.astral.sh/uv/). First setup may download Python and packages; the seeded fixture makes no model calls.

```bash
uvx --python 3.12 --from 'agent-reliability-ci==0.8.0' arci demo --workers 4
```

The demo removes a retry, checks the regression, reduces the injected fault set, replays the failure and checks a repair. It exits **0 when the expected outcomes hold**, including the intended **BLOCK** for the broken candidate. [Read the fixture and its limits](https://github.com/ajaysurya1221/agent-reliability-ci#try-the-offline-demo).

The projects' fixture and benchmark results have defined scopes; they do not establish production safety or customer adoption. Each repository documents its trust boundaries and limitations. I use AI coding assistants as pair-programmers and record that assistance in commit trailers.
