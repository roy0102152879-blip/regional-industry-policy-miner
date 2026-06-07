# Regional Industry Policy Miner

A lightweight framework for decoding local industrial policy signals and identifying government-backed industry bets in China.

This project is inspired by the policy-text structuring ideas in the NBER working paper *Decoding China's Industrial Policies*. It is not an official replication of that paper, and it does not claim to predict investment returns. The goal is more practical: read local policy documents, project news, enterprise evidence, and public data to understand what a local government is really supporting, whether local firms can carry it, and where the evidence is still weak.

## What It Does

The framework separates three questions that are often mixed together:

1. **Government policy bet**: Is the local government repeatedly supporting this industry through plans, projects, funds, land, platforms, and organizational mechanisms?
2. **Local carrying capacity**: Are there real firms, listed companies, project companies, parks, platforms, or research institutions carrying the industry locally?
3. **Commercial-quality pre-check**: Is there preliminary evidence of market demand, profitability, healthy cycles, or obvious risks such as overcapacity and subsidy dependence?

The framework is designed for two workflows:

- **Regional blind scan**: Start from a region and identify priority industries.
- **Targeted industry deep dive**: Start from a region + industry and assess the strength of policy support, local fit, enterprise carrying, and quantitative scale.

## What It Is Not

This is not:

- an investment recommendation system
- a stock-picking framework
- a replacement for full commercial due diligence
- an official replication of the NBER paper
- a database of all Chinese industrial policies

It is a structured research workflow for avoiding shallow policy summaries and making local industry analysis more evidence-backed.

## Repository Contents

```text
.
├── README.md
├── SKILL_PUBLIC.md
├── CITATION.md
├── LICENSE
├── docs/
│   ├── fields.md
│   ├── framework.md
│   └── source-priority.md
└── examples/
    └── jiaxing_simplified.md
```

## Quick Start

Use `SKILL_PUBLIC.md` as the public workflow guide. For a regional scan, start with:

```text
Use regional-industry-policy-miner to scan [region] and identify the industries that the local government is really betting on.
```

For a targeted industry deep dive:

```text
Use regional-industry-policy-miner to assess [region] + [industry]. Keep source library, enterprise mapping, quantitative layer, and commercial-quality pre-check separate.
```

## Core Principle

Do not confuse:

- policy heat
- local industrial advantage
- real enterprise carrying
- commercial quality

A region may loudly promote an industry that is still weak locally. Another industry may receive less policy language but have stronger firms and market-led advantages. The framework is meant to make those differences visible.

## License

This public version is released for learning, research, and non-commercial use. See `LICENSE`.

