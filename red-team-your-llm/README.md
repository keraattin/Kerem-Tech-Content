# Red team your LLM

> The open-source LLM scanner from NVIDIA — 150+ attack probes, 24+ vulnerability categories, 12 generator backends, 5 min to first finding.

A walkthrough of [garak](https://github.com/NVIDIA/garak), NVIDIA's open-source
LLM vulnerability scanner. From install to your first probe-driven report.

**PDF:** [garak_carousel.pdf](garak_carousel.pdf)
**Instagram:** [@kerem.tech post](https://www.instagram.com/p/DYUR1WBDI-N)

## What's inside

- **Foundation (slides 1–3)** — what garak is, architecture, install
- **10 probe families (slides 4–13)** — the attacks that matter most
- **Operations (slides 14–16)** — generators, filtering, reports

## 10 probes covered

`encoding` · `promptinject` · `dan` · `divergence` · `leakreplay` ·
`packagehallucination` · `malwaregen` · `xss` · `goodside` · `ansiescape`

## References

- garak: <https://github.com/NVIDIA/garak> (Apache 2.0)
- NVIDIA AI Red Team

## Who it's for

ML engineers shipping LLM-powered features, AI red teamers, and security
researchers evaluating model-level risks before production rollout.
