# Ajay Surya Senthilrajan

AI/GenAI engineer in Bengaluru, with experience in document intelligence and
retrieval at Redica Systems and legal-document ML at Zolvit (formerly Vakilsearch).

**I build independent testing and evidence for agent controls.**

| Project | Question it answers | State on 8 October 2026 |
|---|---|---|
| [actseal](https://github.com/ajaysurya1221/actseal) | Does a frozen action policy meet its declared risk and coverage limits? | [1.0.1 on PyPI](https://pypi.org/project/actseal/1.0.1/); separate finite-benchmark audit: INCONCLUSIVE; offline replay uses its archived producer |
| [agent-reliability-ci](https://github.com/ajaysurya1221/agent-reliability-ci) | Did an agent change reduce reliability under tool/MCP faults, and what failed? | [Evidence release 2026-10-06](https://github.com/ajaysurya1221/agent-reliability-ci/releases/tag/evidence-2026-10-06): planner, technical report, 18 decisions re-derived byte for byte |
| [frontier-scout](https://github.com/ajaysurya1221/frontier-scout) | Did an agent PR stay within the scope declared on its base branch? | [2.2.0 on PyPI](https://pypi.org/project/frontier-scout/2.2.0/); repairs the verifier defects published for 2.1.0 |
| [dorian](https://github.com/ajaysurya1221/dorian) | Does the code still satisfy its recorded, executable claims? | [1.4.0 on PyPI](https://pypi.org/project/dorian-vwp/) as `dorian-vwp` |
| [evalopt-graph](https://github.com/ajaysurya1221/evalopt-graph) | Do the supplied gates, claims and evidence satisfy an acceptance policy? | [0.1.0 on PyPI](https://pypi.org/project/evalopt-graph/) |

**Try the synthetic demo.** Requires macOS/Linux and uv; use a new `./actseal-demo`
directory. The first command may download Python and the package.

```bash
uvx --python 3.12 actseal demo --out ./actseal-demo      # exits 0: BLOCK for the bad run, PASS for the fixed run
uvx --offline --python 3.12 actseal replay ./actseal-demo/bad/evidence   # exits 1 with the reason
```

Or start with [ARCI's offline demo](https://github.com/ajaysurya1221/agent-reliability-ci#try-the-offline-demo):
in its seeded retry example, removing a retry changes success from 192/200
to 132/200; the gate reports BLOCK and the reduced failure replays offline
([recorded results](https://github.com/ajaysurya1221/agent-reliability-ci/blob/evidence-2026-10-06/docs/results/retry-demo-n200.md)).

**What the audits say, not what the READMEs promise.** actseal's
[8 October audit](https://github.com/ajaysurya1221/actseal/blob/main/docs/results/jev-audit-2026-10-08/README.md)
of a live decision model is published with its verdict, its sealed inputs and
the exact producer needed to replay it. On a fixed Banking77 benchmark, the
policy acted on 580 of 639 verification cases; 24 actions disagreed with
benchmark labels. The risk CP interval [0.0250, 0.0639] crosses the 0.05
limit: INCONCLUSIVE. This is demo-scope evidence; replay uses the archived
producer.
frontier-scout's [defect matrix](https://github.com/ajaysurya1221/frontier-scout/blob/main/docs/evaluation/verifier-2026-10-06.md)
lists the bypasses its own earlier release accepted, with the regression
tests that now reject them.

**How these were built.** I use AI coding assistants as pair-programmers
and record that assistance in commit trailers. I can walk through the
problem framing, verification semantics, statistical decision rules, threat
models and tests on a call.

[LinkedIn](https://www.linkedin.com/in/ajay-surya-senthilrajan/) ·
[Email](mailto:ajaysuryasenthilrajan@gmail.com)
