---
name: adaptive-prd-zh
description: Create, restructure, shorten, or review Chinese product requirements documents by routing the task to a brief, lean iteration, standard PRD, governed delivery, or reader-test workflow. Trigger on requests such as 写PRD、整理需求文档、精简PRD、评审PRD、检查需求是否完整、根据原型或会议材料写需求、发布前读者测试, or when the appropriate PRD depth is unclear. Use notes, prototypes, research, review comments, and existing documents as sources. Do not use for BRDs, technical design documents, architecture specifications, or implementation plans unless the user explicitly asks to convert their product-facing content into a PRD.
---

# 自适应中文 PRD

根据需求规模、材料成熟度、协作范围和用户目标选择合适的 PRD 深度。不要让用户记忆模板或手动选择其他 Skill；除非用户明确指定模式，否则自动路由。

## 共同底线

1. 以用户提供的原文、原型、数据和评审结论为事实来源，不补造用户数据、指标、时间、负责人、技术结论或确认状态。
2. 区分已确认事实、合理推断、待确认项和材料冲突。推断必须说明依据，不写成已确认结论。
3. 用户提供的模板、组织规范和明确范围优先于本 Skill 的默认结构。
4. PRD 定义用户场景、产品规则、可见反馈、限制和验收结果。除非技术约束直接影响产品结果，否则不替研发决定接口、数据库、缓存、对象结构、前后端分工或迁移脚本。
5. 保留能提供事实、规则、依据、决策和未决项的信息；删除重复、套话和不产生新信息的文字。

开始任务时阅读 [共享写作规则](references/shared-writing-rules.md) 和 [模式路由](references/mode-router.md)，然后只加载所选模式对应的参考文件。

## 执行流程

1. 阅读所有可用材料，记录来源、时间、版本及相互冲突之处。
2. 根据模式路由选择一个主模式。信息不足时先完成不依赖缺失信息的部分，再集中提出少量会改变范围或方案的问题。
3. 读取该模式的参考文件并执行。必要时可以组合“评审/读者测试”与任一写作模式，但不要同时套用多个写作模板。
4. 交付前检查事实状态、范围、名称、数量、默认状态、异常、验收和历史数据影响是否一致。
5. 有明确文件交付要求时遵从要求；否则，较完整的产物默认保存为 Markdown，命名为 `{产品或功能名}_PRD_{版本或日期}.md`。短简报可以直接在对话中给出。

## 模式与参考文件

| 模式 | 何时使用 | 读取文件 |
|---|---|---|
| 需求简报 | 仍在探索、材料少、只需一页对齐或决定是否进入 PRD | [简报与精简迭代](references/brief-and-lean.md) |
| 精简迭代 | 存量产品、已有原型、小范围页面或规则调整、单团队交付 | [简报与精简迭代](references/brief-and-lean.md) |
| 标准 PRD | 新功能或中型项目，需要问题、用户、范围、指标、详细规则和验收 | [标准 PRD](references/standard-prd.md) |
| 治理型 PRD | 多团队、强依赖、合规/安全/平台变更、需要版本和追溯治理 | [治理型 PRD](references/governed-prd.md) |
| 评审/读者测试 | 已有 PRD 需要检查、精简、补漏或发布前独立理解测试 | [评审与读者测试](references/review-and-reader-test.md) |

## 输出约束

- 不显示“已确认”标签也可以，但正文不能把待确认或推断写成事实；待确认项必须可被读者找到。
- 不机械生成空章节。某项内容不适用时省略；若该缺失本身影响评审，说明“不适用”及原因。
- 不因模板要求虚构基线、目标值、发布日期、责任人、市场规模或竞品信息。未知值使用 `待确认`。
- 评审任务默认先报告问题，不在用户只要求审查时擅自重写原文。
- 用户明确要求“先讨论、先确认结构、确认后再写”时，只完成分析和建议，不提前生成最终 PRD。

## 交付前最低检查

- 每个结论能回到原始材料、明确推断或待确认项。
- 问题、目标、范围和详细功能之间没有明显断裂。
- 复杂功能具有可观察、可判定的验收结果。
- 原型、文字、字段、数量、名称和状态没有未说明的冲突。
- 已说明旧数据、旧配置和历史内容是否受影响。
- 没有把内部实现建议写成已确认的产品要求。

行为验证场景见 [评测场景](references/evaluation-scenarios.md)。
