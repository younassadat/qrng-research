# QRNG Research

> Investigating quantum random number generation (QRNG) vs classical pseudorandom number generation (PRNG) for procedural game world generation.

![Status](https://img.shields.io/badge/status-in%20progress-F5A623?style=flat-square)
![Field](https://img.shields.io/badge/field-quantum%20computing-6929C4?style=flat-square)
![Type](https://img.shields.io/badge/type-independent%20research-3776AB?style=flat-square)

---

## Research Question

Can quantum random number generation produce meaningfully different — and potentially richer — procedural game worlds compared to classical pseudorandom algorithms?

---

## Background

Procedural generation is the backbone of modern open-world games. Every terrain, dungeon, and ecosystem is seeded by a random number generator. But classical PRNGs are deterministic — given the same seed, they always produce the same output. They simulate randomness; they don't generate it.

Quantum random number generators, by contrast, derive randomness from genuinely non-deterministic quantum phenomena — photon arrival times, vacuum fluctuations, radioactive decay. The randomness is real, not computed.

The question is whether this distinction matters practically — and whether it produces measurably different or more complex procedural outputs.

---

## Hypothesis

QRNG-seeded procedural generation will produce statistically distinct outputs from PRNG-seeded generation, with differences detectable in distribution analysis, entropy measurements, and visual complexity of generated worlds.

---

## Methodology

### Phase 1 — Statistical Analysis
- Source quantum random numbers from public QRNG APIs (ANU Quantum Random Numbers, NIST Randomness Beacon)
- Compare against classical PRNGs: Mersenne Twister, LCG, PCG
- Run standard randomness test suites: NIST SP 800-22, Dieharder, TestU01
- Measure entropy, autocorrelation, and distribution uniformity

### Phase 2 — Procedural Generation Implementation
- Build a controlled procedural terrain generator in Python
- Seed identical generation algorithms with QRNG vs PRNG sources
- Generate sample world maps, dungeon layouts, ecosystem distributions

### Phase 3 — Comparative Analysis
- Visual complexity comparison
- Structural pattern analysis
- Statistical distribution of generated features
- Blind evaluation — can human observers tell the difference?

---

## Tools & Resources

- **Python** — NumPy, SciPy, Matplotlib
- **QRNG Sources** — ANU QRNG API, NIST Randomness Beacon
- **Randomness Testing** — NIST SP 800-22 test suite, Dieharder
- **Procedural Generation** — custom Python implementation, Perlin noise
- **Visualization** — Matplotlib, Pygame (for world rendering)

---

## Repository Structure (Planned)

```
qrng-research/
├── data/
│   ├── qrng_samples/          # Raw quantum random number datasets
│   └── prng_samples/          # Classical PRNG outputs for comparison
├── analysis/
│   ├── statistical_tests.py   # NIST & Dieharder test implementations
│   ├── entropy_analysis.py    # Entropy and distribution analysis
│   └── visualization.py       # Plots and comparative charts
├── procedural/
│   ├── terrain_generator.py   # Controlled terrain generation engine
│   └── world_renderer.py      # Visual output of generated worlds
├── results/
│   └── findings.md            # Running notes and findings
└── paper/
    └── draft.md               # Research paper draft
```

---

## Current Status

| Phase | Status |
|---|---|
| Literature review | 🔄 In progress |
| Statistical framework design | 🔄 In progress |
| QRNG data collection | ⏳ Upcoming |
| Procedural generator build | ⏳ Upcoming |
| Comparative analysis | ⏳ Upcoming |
| Paper draft | ⏳ Upcoming |

---

## Expected Outcomes

- A structured comparison of QRNG vs PRNG output quality for procedural systems
- Python tooling for QRNG-seeded procedural generation
- A publishable research paper or whitepaper on findings
- Open dataset of QRNG vs PRNG samples for procedural generation benchmarking

---

## References

- Jennewein, T. & Achleitner, G. — *A fast and compact quantum random number generator*
- NIST SP 800-22 — *A Statistical Test Suite for Random and Pseudorandom Number Generators*
- Perlin, K. — *An Image Synthesizer* (1985) — foundational procedural noise
- ANU Quantum Random Numbers Server — qrng.anu.edu.au

---

*Independent research by [Younas Sadat](https://github.com/younassadat) · Islamabad, Pakistan*
