---
name: regional-industry-policy-miner
description: Use when the user wants to decode regional industrial policy, scan a region for priority industries, or deeply assess whether a specified industry in a region is truly supported, locally advantaged, quantitatively meaningful, and carried by real enterprises. Covers NBER-style policy text decoding, regional blind scans, targeted industry deep dives, evidence libraries, enterprise mapping, listed-company status, and quantitative scale/investment/target analysis.
---

# Regional Industry Policy Miner

Use this skill for two related but different tasks:

- **Mode B: regional blind scan**: given a region, identify what industries the region is really betting on.
- **Mode A: targeted industry deep dive**: given a region + industry, judge whether that industry is truly advantaged and worth further work.

The NBER `Decoding China's Industrial Policies` method is most naturally suited to Mode B: reading many local policy texts and inferring priority industries. Mode A requires extra layers: quantitative data, enterprise verification, listed-company status, project/fund/platform investment, and target-gap analysis.

Primary objective: identify **government industrial bets and real local carrying capacity**. This skill does not make a final investment or profitability call, but should include a light commercial-quality pre-check when evidence is available.

## Core Rule

Never make a later version thinner than an earlier version. If iterating from a prior report, do **incremental fusion**:

- keep the previous source library, document scoring, policy tools, organization, intergovernmental chain, industry-code mapping, and enterprise pool;
- add new decision, enterprise, or quantitative layers into the richer prior version;
- do not create a new short version that drops earlier evidence.

## Markdown Readability Rule

Reports are often read in Obsidian or plain Markdown preview. Keep primary ranking
and judgment tables narrow:

- use Chinese column headers when writing Chinese reports;
- prefer short headers such as `政策押注`, `本地承载`, `商业闭环`, `是否深挖`;
- keep long explanations outside the table as short bullets or paragraphs;
- avoid wide English headers in top-level decision tables unless the user asks for
  machine-readable output.

## Mode B: Regional Blind Scan

Goal: answer “this region is really betting on what industries?”

Required output:

1. Source library: plans, government work reports, budget/finance, development reform, industry bureau, science bureau, park materials, signing/project news.
2. Candidate industry ranking.
3. Score each candidate by:
   - policy target strength
   - tool complexity
   - organization execution
   - local fit
   - enterprise/project carrying
   - resource commitments
   - continuity
4. For top industries, state `should_enter_mode_a: yes/no`.
5. Explain why the top industry ranks above alternatives.
6. Add a light commercial-quality pre-check: strong/mid/weak/pending.
7. Do not default to bank tactics unless the user asks.

For Chinese reports, the candidate ranking table should be compact and readable:

| 排名 | 候选产业 | 政策押注 | 本地承载 | 商业闭环 | 是否深挖 |
| --- | --- | --- | --- | --- | --- |

Put the reasoning for each row below the table instead of stuffing long sentences
into table cells.

Top industry enterprise table is mandatory. For each top industry, include 3-8 representative enterprises or project subjects:

| field | requirement |
| --- | --- |
| enterprise_name | company/project/platform name |
| role | chain owner, platform, project company, processing firm, equipment firm, resource developer, etc. |
| listed_status | listed, listed-company subsidiary, IPO/terminated, non-listed, pending verification |
| ticker_or_parent | ticker or listed parent; otherwise non-listed/pending |
| local_link | registration, base, project, park, resource, service scope |
| scale_signal | output, profit, investment, capacity, employment, acreage, generation, customers |
| verification | official, announcement, prospectus/annual report, company website, authority media, normal media, pending |
| evidence | doc_id + URL |

## Mode A: Targeted Industry Deep Dive

Goal: answer “why this industry in this region is worth looking at, and how strong it really is.”

Required structure:

1. Conclusion: strong/mid/weak support and why.
2. Policy source library: keep at least 15 sources for a formal run; 30-50 for a deep run.
3. Document decoding score table: industrial policy score, support tone, target strength, tool complexity, organization execution.
4. Policy goals, tools, conditionality, organizational arrangements, intergovernmental relationships.
5. Support timeline: earliest support evidence, duration, turning points, national/province/city/district milestones.
6. Resource flow: funds, fiscal support, industrial funds, credit, land, parks, platforms, procurement, scenarios, projects.
7. Local advantage: research base, anchor institutions, labs/universities, chain owners, enterprise density, uniqueness.
8. Cluster portrait: size, firms, listed firms, specialized SMEs, employment if available, parks, upstream/downstream, cluster type.
9. Industry-code mapping: do not rely on one code if the industry spans multiple chain links.
10. Enterprise mapping and verification.
11. Quantitative layer.
12. Light commercial-quality pre-check.
13. Risks and counterexamples.
14. Next data gaps.

## Light Commercial-Quality Pre-check

Keep this lightweight. It is a risk screen, not a final investment conclusion.
In Chinese reports, frame it as whether the industry has a real **commercial
closed loop** or is mainly **government-forced cultivation**. The question is:
can the industry sustain itself through market demand, enterprise revenue,
tax contribution, projects, customers, and repeatable transactions, or is the
visible activity mostly created by planning language, subsidies, ceremonial
signings, and招商 pressure?

Output three separate judgments:

| dimension | meaning |
| --- | --- |
| policy_bet_strength | how strongly government is pushing the industry |
| local_carrying_strength | whether local firms/projects/platforms actually carry it |
| commercial_quality_precheck | whether market demand, profitability, cycle, overcapacity, subsidy dependence, and listed-company financials look healthy |

For Chinese reports, use this compact display table:

| 产业 | 政策押注 | 本地承载 | 商业闭环 | 结论 |
| --- | --- | --- | --- | --- |

Use `strong / mid / weak / pending` plus one short reason. Examples:

- strong policy + strong carrying + mid commercial quality: real cluster, but sector cycle is down.
- strong policy + weak carrying + weak commercial quality: likely policy wish or forced cultivation.
- mid policy + strong carrying + strong commercial quality: market-led local advantage, even if policy wording is not loud.

Do not let commercial quality override the skill's main finding. State it separately from policy support.

## Quantitative Layer

Every formal targeted industry report must include a quantitative layer. At minimum seek:

- current output/revenue scale
- historical growth
- policy targets
- target-gap calculation and required CAGR/yearly increment
- enterprise count changes
- listed enterprise count
- specialized/new “little giant” count
- project/platform/fund/credit/fiscal investment amounts
- representative enterprise revenue/profit
- land/park area, employment, R&D, patents, standards, customers if available

Use this table:

| field | requirement |
| --- | --- |
| metric_name | output, enterprise count, platform investment, listed-company revenue, etc. |
| value | number and unit |
| period | year/quarter/as-of date |
| geography_or_scope | national/province/city/district/park/company/platform |
| baseline_or_target | actual, historical, policy target, estimate |
| source_quality | official statistics, formal policy, listed filing, government news, authority media, company self-claim, estimate |
| evidence | doc_id + URL |
| caveat | duplication, target not actual, non-additive, incomplete time series |

Rules:

- Separate actuals from policy targets.
- Separate platform investment, industrial fund size, fiscal subsidy, credit line, and project investment.
- If only a mechanism is found but no amount, say “amount not found”; do not invent a number.
- Do not add listed-company revenue to regional output unless the scope clearly matches.
- If a claim is qualitative only, label it `qualitative strong, quantitative weak`.

## Evidence Discipline

For each document:

1. Extract evidence.
2. Classify with NBER-style definitions.
3. Score conservatively.
4. Filter counterexamples: ordinary publicity, single-company news, infrastructure unrelated to industry, generic business-environment text.

Every important claim should have `doc_id + evidence + URL`.

## Source Priority

Use primary and near-primary sources first:

1. Official government documents and full-text policies.
2. Development reform, industry, science, commerce, finance, park, and project-signing sources.
3. Listed-company filings, prospectuses, exchange announcements, company annual reports.
4. Authoritative media and industry associations.
5. PKULaw / 北大法宝 and similar legal-policy databases as **secondary sources** for policy discovery, abstracts, hierarchy checks, and citation-chain tracing.

PKULaw/北大法宝 rule: useful for finding or confirming policy existence and level, especially when local sites are hard to search. But do not treat an abstract as a replacement for the original full text when money, land, projects, enterprises, or quantitative claims matter.

## Useful Output Filenames

For local experiments, write reports under the workspace if appropriate:

- `tmp/industrial_policy_decoder/<region>_regional_scan.md`
- `tmp/industrial_policy_decoder/<region>_<industry>_policy_decoder.md`
- `tmp/industrial_policy_decoder/<region>_<industry>_enterprise_pool.md`
