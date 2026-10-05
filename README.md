# Ajay Surya Senthilrajan

AI/GenAI engineer in Bengaluru. Day job: document intelligence and retrieval agents
(OCR at 3,000+ pages, GraphRAG, text-to-SQL, MCP, agent memory) at Redica Systems.
Before that, four years of legal-document ML at Zolvit.

## The accountability layer for AI coding agents

Coding agents ship PRs faster than humans can review them. These tools make an agent's
work checkable in CI without trusting the agent's own summary:

| Tool | What it verifies | One number |
|---|---|---|
| [dorian](https://github.com/ajaysurya1221/dorian) | The agent's *claims* about a change, sealed and re-checked on every commit | P/R 0.93 on a 240-pair benchmark, 11.6× fewer false alarms than path-watching |
| [frontier-scout](https://github.com/ajaysurya1221/frontier-scout) | The agent's PR stayed within *approved scope*, fail-closed, with optional Sigstore-attested evidence | 188 tests passed (PR #74), mypy strict core |
| [agent-reliability-ci](https://github.com/ajaysurya1221/agent-reliability-ci) | The agent's *reliability* under injected tool/MCP faults, with honest statistics | 200 trials per arm, Clopper-Pearson/Newcombe bounds; 437 tests collected (2026-09-30 audit) |
| [evalopt-graph](https://github.com/ajaysurya1221/evalopt-graph) | Whether the *evidence* satisfies an explicit acceptance policy, replayably | Zero runtime dependencies, 411 tests passed (2026-09-30 audit); CI across 5 Python versions and 3 OSes |

- [Calibration audit](https://github.com/ajaysurya1221/agent-reliability-ci/tree/main/docs/results/jev-calibration): 26,140 sealed requests; ECE 0.024 on CLINC150 and 0.084 on Banking77; all seven pre-registered expectations met.
- [Decision layer](https://github.com/ajaysurya1221/frontier-scout/tree/main/docs/evaluation/decision-model): on a 324-command labelled set against the dogfood policy, dangerous static allows fell from 25 → 0 (11 denied, 14 sent to approval); AUROC ≥ 0.999 on each risk question: destructive actions, secret exposure and privilege escalation.

Start with dorian's 30-second demo or arci's five-minute path.

**How these were built.** I use Claude Code and Codex as pair-programmers and record it in
commit trailers; the problem framing, verification semantics, statistical decision rules,
threat models and test design are mine, and I can walk through any of them on a call.

## Elsewhere
LinkedIn: linkedin.com/in/ajay-surya-senthilrajan · Email: ajaysuryasenthilrajan@gmail.com
