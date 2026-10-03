<div align="center">

# Virtual Longevity Clinic (VLC)

**The Virtual Longevity Clinic: A Multi-Agent AI Framework for Selection Intelligence beyond Prediction Models**

[![Status](https://img.shields.io/badge/status-preprint%20in%20submission-orange)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A multi-agent software framework that makes the **choose–monitor–revise** loop of person-level intervention selection explicit, recorded, and auditable — selection intelligence beyond prediction models.

[English](#english) | [中文](#中文)

</div>

---

## English

### What is the Virtual Longevity Clinic?

Prediction can estimate risk, but a person-level clinic must also **choose an option, record why it was chosen, and specify how follow-up should change the plan**. We call this auditable choose–monitor–revise process **selection intelligence**.

The Virtual Longevity Clinic (VLC) is a multi-agent AI research framework whose architecture makes five steps explicit:

| Component | Role |
| --- | --- |
| C1 — State record | Holds the measured state for one person |
| C2 — State maps | Versioned, computable knowledge maps that define coordinates, observation-mapping rules, and inference boundaries |
| C3 — Selection operator | Constructs candidate intervention options from the mapped state |
| C4 — Response check | Compares follow-up measurements against prespecified expectations and applies a fixed revision rule |
| C5 — Execution & verdict | Runs clinic roles and records software checks |

The intended cycle is **MEASURE → INFER → PLAN → REVIEW RESPONSE**, with plans stored as versioned data records rather than only narrative recommendations. The framework corresponds checkpoint-by-checkpoint to the companion steerability framework (CP1–CP5) of our position paper *World Models for Biomedicine: Prediction Is the Means, Selection Is the End*.

### Scope of what was tested — and what was not

The v1 instantiation was evaluated only on a subset of the architecture. Every capability in this repository's descriptions carries an explicit evidence level (**Designed / Instantiated / Exercised / Supported by companion preprint / Replicated across external cohorts**).

**Exercised in v1** (on prepared inputs):

- One methylation-to-module mapping (72 aging-related modules) over the 332-module atlas
- Workflow and option-list operations with 1,916 intervention entries and 798 conditional relationships
- Repeatability and deliberation arms (11 prepared cases: 10 de-identified individuals + 1 synthetic)
- Coordinator arbitration, provenance tracking, and resource metering

**Designed, not tested**: state-map selection, cross-tradition mapping, in-loop storyline coupling, shared client–professional goal setting, real intervention exposure, and a real 90-day follow-up cycle.

These counts describe **resource scope, not clinical validation**. The study evaluates an internal research prototype — software process properties, not clinical utility or patient safety.

### Headline results, at their honest strength

- **Within-case output stability**: top-ranked finding unchanged in 55/55 repeatability runs and 33/33 deliberation runs — stability, not accuracy
- **State dependence**: a data-swap probe gave donor-state top-ten coverage 0.500 vs 0.336 for the nominal case — a limited signal, not validated personalization
- **Traceability**: 29/32 supplement suggestions traceable to the supplied option list — traceability, not clinical appropriateness
- **Arbitration**: coordinator modified or rejected 47/132 specialist proposals (35.6%); all 196 final actions retained proposal provenance — documented process, not benefit
- **No deliberation advantage demonstrated**: blind judging preferred deliberation in 14/33 comparisons, the no-peeking control in 17/33, two ties
- **A preregistered positive-control gate failed**: the probe detected its target in 2/3 runs and therefore failed its 3/3 rule; the other two software checks passed
- **The five-role coverage comparison** failed to establish its prespecified superiority criterion
- **Resource cost**: one v1 round averaged ~8,916 tokens and 137 seconds (≈ RMB 0.01 at stated list prices)

### Status of this repository

- **v1 (current):** bilingual README and version statement. **No figures yet** — representative figures will be added with the preprint release.
- **Preprint:** in submission. The DOI and citation entry will be added here upon posting.
- **Later:** evaluation scripts, replay-arm tooling, and knowledge-map interfaces will be released as the paper's companion artifacts.

### Citation

Formal citation (DOI, BibTeX) will be added when the preprint is posted. Until then, please refer to the work as:

> Xiong, J. *The Virtual Longevity Clinic: A Multi-Agent AI Framework for Selection Intelligence beyond Prediction Models*. Preprint in submission, 2026.

### Links

| Resource | Link |
| --- | --- |
| SteeraMed platform | https://steeramed.com |
| DeepoMe | https://www.deepome.com |

**Companion repositories**

- [SteeraMed-Selection-Intelligence](https://github.com/DeepoMe/SteeraMed-Selection-Intelligence) — the position paper: prediction is the means, selection is the end
- [SteeraMed-RootMap](https://github.com/DeepoMe/SteeraMed-RootMap) — root-cause attribution framework (dependency map used by VLC's v1 workflow)
- [SteeraMed-bench](https://github.com/DeepoMe/SteeraMed-bench) — 332 × 1,916 drug-module benchmark (companion knowledge asset)
- [SteeraMed-MorbidMap](https://github.com/DeepoMe/SteeraMed-MorbidMap) — multi-morbidity pattern mining with LLMs
- [Good-Healthspan-Practice](https://github.com/DeepoMe/Good-Healthspan-Practice) — good-practice guide for N-of-1 evidence in longevity medicine

### License

This repository (README and future artifacts) is released under the [MIT License](LICENSE).

### Contact

- Jianghui Xiong — jianghui@deepome.com
- [DeepoMe Inc.](https://www.deepome.com)

---

## 中文

### 虚拟长寿诊所是什么？

预测可以估计风险，但面向个人的诊所还必须**选择方案、记录选择的理由、并规定随访如何改变计划**。我们把这个可审计的"选择—监测—修订"过程称为**选择智能（selection intelligence）**。

虚拟长寿诊所（VLC）是一个多智能体 AI 研究框架，其架构把五个环节显式化：C1 状态记录、C2 状态地图（版本化、可计算的知识地图：坐标、观测映射规则、推断边界）、C3 选择算子（构造候选干预方案）、C4 响应检查（对照预登记预期并执行固定修订规则）、C5 执行与裁决（运行诊所角色并记录软件检查）。

预期循环为 **MEASURE → INFER → PLAN → REVIEW RESPONSE**，方案以版本化数据记录存储，而非仅以叙述性建议存在。框架与我们立场论文《World Models for Biomedicine: Prediction Is the Means, Selection Is the End》的可驾驭性检查点（CP1–CP5）逐点对应。

### 测试范围——测了什么、没测什么

v1 实例仅评估了架构的一个子集。本仓库描述中每项能力都带有明确的证据等级（**已设计 / 已实例化 / 已演练 / 姊妹预印本支持 / 外部队列复现**）。

**v1 已演练**（基于预备输入）：一条甲基化→模块映射（72 个衰老相关模块，基于 332 模块图谱）；工作流与选项清单操作（1,916 个干预条目、798 条条件关系）；可重复性臂与协商臂（11 个预备案例：10 例脱敏个体 + 1 例合成案例）；协调器仲裁、来源追溯与资源计量。

**已设计、未测试**：状态地图选择、跨传统映射、环内故事线耦合、客户-专业人员共享目标设定、真实干预暴露、真实 90 天随访周期。

以上计数描述的是**资源范围，不是临床验证**。本研究评估的是内部研究原型——软件过程属性，而非临床效用或患者安全。

### 主要结果（按其诚实强度表述）

- **案例内输出稳定性**：首要发现在 55/55 次可重复运行与 33/33 次协商运行中不变——是稳定性，不是准确性
- **状态依赖**：数据置换探针中供体状态 top-10 覆盖 0.500 vs 名义案例 0.336——有限信号，非已验证的个体化
- **可追溯性**：32 条补剂建议中 29 条可追溯至所供选项清单——是可追溯性，非临床适当性
- **仲裁**：协调器修改或否决 47/132 条专科提案（35.6%）；全部 196 条最终动作保留提案来源——是过程记录，非获益证明
- **未证明协商优势**：盲评 33 次比较中协商 14 次、无偷看对照 17 次、2 次平局
- **预登记正控制门未通过**：探针在 2/3 次运行中检出目标，未达 3/3 规则判失败；另两项软件检查通过
- **五角色覆盖比较**未达到其预设优效标准
- **资源成本**：v1 单轮平均约 8,916 token、137 秒（按牌价约 RMB 0.01）

### 仓库状态

- **v1（当前）：** 中英文 README 与版本声明，**暂不附图**——代表性图件将随预印本发布补入。
- **预印本：** 投稿中。上线后在此补充 DOI 与正式引用条目。
- **后续：** 评估脚本、回放臂工具与知识地图接口将作为论文配套产物逐步放出。

### 引用

预印本上线后将补充正式引用（DOI、BibTeX）。此前请按以下方式指称：

> Xiong, J. *The Virtual Longevity Clinic: A Multi-Agent AI Framework for Selection Intelligence beyond Prediction Models*. Preprint in submission, 2026.

### 链接

| 资源 | 链接 |
| --- | --- |
| SteeraMed 平台 | https://steeramed.com |
| DeepoMe | https://www.deepome.com |

**姊妹仓库**

- [SteeraMed-Selection-Intelligence](https://github.com/DeepoMe/SteeraMed-Selection-Intelligence) — 立场论文：预测是手段，选择是目的
- [SteeraMed-RootMap](https://github.com/DeepoMe/SteeraMed-RootMap) — 根因归因框架（VLC v1 工作流所用依赖图）
- [SteeraMed-bench](https://github.com/DeepoMe/SteeraMed-bench) — 332 × 1,916 药物-模块基准（配套知识资产）
- [SteeraMed-MorbidMap](https://github.com/DeepoMe/SteeraMed-MorbidMap) — 大模型多病共存模式挖掘
- [Good-Healthspan-Practice](https://github.com/DeepoMe/Good-Healthspan-Practice) — 长寿医学 N-of-1 证据良好实践指南

### 许可

本仓库（README 及后续产物）以 [MIT 许可](LICENSE)发布。

### 联系方式

- 熊江辉 — jianghui@deepome.com
- [DeepoMe Inc.](https://www.deepome.com)
