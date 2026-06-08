# 区域产业政策挖掘器 / Regional Industry Policy Miner

一个用于解码中国地方产业政策信号的轻量研究框架。

它帮助你回答一个很实际的问题：

> 一个地方政府到底在押注哪些产业？这些产业是政策口号，还是已经有企业、项目、园区、资金和平台在承接？

本项目借鉴了 NBER working paper *Decoding China's Industrial Policies* 中“用结构化方式阅读政策文本”的思路，但不是该论文的官方复现，也不声称能够预测投资收益。它更像一个公开资料研究工作流：把地方规划、政府工作报告、项目新闻、企业证据、上市公司材料和公开数据放到同一张证据表里，区分政策热度、地方承载能力和初步商业质量。

## 适合谁

- 做区域产业研究、地方招商研究、产业链研究的人
- 想判断某个城市、区县、园区真正支持什么产业的人
- 银行、券商、咨询、投资研究、产业园区相关从业者
- 希望把“政策很多、但不知道重点在哪”变成结构化证据的人

## 它能做什么

这个框架会把三个经常混在一起的问题拆开：

1. **政策押注强度**：地方政府是否在规划、项目、基金、土地、平台、组织机制中持续支持这个产业？
2. **地方承载能力**：当地是否真的有企业、上市公司、项目公司、园区、平台、科研机构在承接？
3. **商业质量预检查**：是否初步具备市场需求、盈利能力、景气周期优势？是否存在产能过剩、补贴依赖、同质化竞争等风险？

它主要支持两类工作流：

- **区域盲扫**：输入一个地区，识别该地区真正押注的重点产业。
- **指定产业深挖**：输入“地区 + 产业”，判断该产业在当地的政策支持、地方优势、企业承载和量化规模是否扎实。

## 它不是什么

这不是：

- 投资建议系统
- 股票推荐框架
- 完整商业尽调替代品
- NBER 论文的官方复现
- 中国全部产业政策数据库

它的定位是：用结构化证据减少“只看政策标题和宣传稿”的浅层分析。

## 快速开始

公开工作流说明见 [`SKILL_PUBLIC.md`](SKILL_PUBLIC.md)。

如果你想做一个区域盲扫，可以这样提问：

```text
Use regional-industry-policy-miner to scan [地区] and identify the industries that the local government is really betting on.
```

也可以直接用中文：

```text
使用 regional-industry-policy-miner 扫描 [地区]，判断当地政府真正押注的产业，并区分政策热度、地方承载和商业质量预检查。
```

如果你想深挖一个指定产业：

```text
使用 regional-industry-policy-miner 分析 [地区] + [产业]。请分别保留政策来源库、企业映射、量化层、风险与反例、商业质量预检查。
```

## 核心原则

不要把下面几件事混为一谈：

- 政策热度
- 地方产业优势
- 真实企业承载
- 商业质量

一个地方可能高调宣传某个产业，但本地企业、项目和资金承接很弱；也可能某个产业政策表述不算最响，但企业基础更扎实、市场化优势更明显。这个框架的目的，就是把这些差异显性化。

## 输出结果通常包括

- 政策来源库：规划、政府工作报告、预算财政、发改/工信/科技/商务/园区材料、项目签约新闻等
- 候选产业排序：哪些产业最像地方政府真正押注的方向
- 政策解码表：目标强度、政策工具、组织执行、央地/省市区关系
- 企业和项目映射：代表性企业、上市状态、项目角色、规模信号、证据来源
- 量化层：产值、投资额、企业数量、政策目标、目标缺口、CAGR 或年度增量
- 商业质量预检查：市场需求、盈利、周期、过剩、补贴依赖等初步风险
- 反例和证据缺口：避免把普通宣传稿误判成强政策支持

## 仓库结构

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

## English Summary

Regional Industry Policy Miner is a lightweight framework for decoding local industrial policy signals in China and identifying government-backed industry bets.

It is inspired by the policy-text structuring ideas in the NBER working paper *Decoding China's Industrial Policies*, but it is not an official replication of that paper and does not make investment-return predictions.

The framework separates three questions:

1. **Government policy bet**: Is the local government repeatedly supporting an industry through plans, projects, funds, land, platforms, and organizational mechanisms?
2. **Local carrying capacity**: Are there real firms, listed companies, project companies, parks, platforms, or research institutions carrying the industry locally?
3. **Commercial-quality pre-check**: Is there preliminary evidence of market demand, profitability, healthy cycles, or risks such as overcapacity and subsidy dependence?

It supports two workflows:

- **Regional blind scan**: start from a region and identify priority industries.
- **Targeted industry deep dive**: start from a region plus industry and assess policy support, local fit, enterprise carrying, quantitative scale, and evidence gaps.

For the public workflow guide, see [`SKILL_PUBLIC.md`](SKILL_PUBLIC.md).

## License

This public version is released for learning, research, and non-commercial use. See [`LICENSE`](LICENSE).
