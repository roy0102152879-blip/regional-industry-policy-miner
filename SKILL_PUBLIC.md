# Regional Industry Policy Miner - Public Skill

Use this public skill when you want to decode regional industrial policy, scan a region for priority industries, or assess whether a specified industry in a region is truly supported and carried by real local actors.

## Modes

### Mode B: Regional Blind Scan

Use when the input is a region.

Goal: identify what industries the region is really betting on.

Required output:

1. Source library.
2. Candidate industry ranking.
3. Score each candidate by policy strength, tool complexity, organization execution, local fit, enterprise/project carrying, resource commitment, and continuity.
4. For each top industry, state whether it should enter a targeted deep dive.
5. Explain why the top industry ranks above alternatives.
6. Add representative enterprises or project subjects.
7. Add a light commercial-quality pre-check.

### Mode A: Targeted Industry Deep Dive

Use when the input is a region + industry.

Goal: judge whether this industry is truly worth looking at locally.

Required output:

1. Conclusion: strong/mid/weak policy support.
2. Policy source library.
3. Document scoring table.
4. Policy goals, tools, conditions, organization, and intergovernmental relationships.
5. Support timeline.
6. Resource flow: funds, fiscal support, land, parks, platforms, procurement, scenarios, projects.
7. Local advantage and cluster portrait.
8. Industry-code mapping.
9. Enterprise mapping and verification.
10. Quantitative layer.
11. Light commercial-quality pre-check.
12. Risks and data gaps.

## Incremental Fusion Rule

If you iterate from a prior report, do not make the new version thinner. Keep the old source library, scoring, tools, organization, enterprise mapping, and quantitative evidence; add new layers into the richer version.

## Enterprise Mapping

For each top industry, include representative enterprises or project subjects:

| field | requirement |
| --- | --- |
| enterprise_name | company, project company, platform, or park entity |
| role | chain owner, platform, project company, processing firm, equipment firm, resource developer |
| listed_status | listed, listed-company subsidiary, IPO/terminated, non-listed, pending |
| ticker_or_parent | ticker or listed parent |
| local_link | registration, base, project, park, resource, service scope |
| scale_signal | output, profit, investment, capacity, employment, acreage, generation, customers |
| verification | official, announcement, annual report, company website, authority media, normal media, pending |
| evidence | doc_id + URL |

## Quantitative Layer

For a formal targeted industry report, seek:

- current output or revenue scale
- historical growth
- policy targets
- target gap and rough CAGR or annual increment
- enterprise count and listed-enterprise count
- specialized/new "little giant" count if available
- project/platform/fund/credit/fiscal investment amounts
- representative enterprise revenue and profit
- land, park area, employment, R&D, patents, standards, customers if available

Separate actuals from targets. Separate platform investment, industrial funds, fiscal subsidies, credit lines, and project investments. If only a mechanism is found but no amount, say so.

## Light Commercial-Quality Pre-check

This is a risk screen, not a final investment conclusion.

Output three separate judgments:

| dimension | meaning |
| --- | --- |
| policy_bet_strength | how strongly the government is pushing |
| local_carrying_strength | whether local firms/projects/platforms actually carry it |
| commercial_quality_precheck | whether demand, profitability, cycle, overcapacity, subsidy dependence, and financials look healthy |

Use `strong / mid / weak / pending` plus one short reason.

## Evidence Discipline

For each important document:

1. Extract evidence.
2. Classify it.
3. Score conservatively.
4. Filter counterexamples such as ordinary publicity, single-company news, unrelated infrastructure, and generic business-environment language.

Every important claim should have `doc_id + evidence + URL`.

