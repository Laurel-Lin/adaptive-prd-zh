# adaptive-prd-zh

面向中文产品工作的自适应 PRD Codex Skill。它会根据需求规模、材料成熟度和协作范围，自动选择合适的文档深度，避免每次手动套模板。

## 支持的工作模式

- **需求简报**：用于探索阶段、一页对齐和立项判断。
- **精简迭代**：用于已有产品的小范围页面、交互或规则调整。
- **标准 PRD**：用于需要完整目标、范围、规则、指标与验收的新功能或中型项目。
- **治理型 PRD**：用于多团队、强依赖、合规、安全或平台级变更。
- **评审与读者测试**：用于检查现有 PRD 的一致性、完整性和可理解性。

## 设计原则

- 基于原始材料，不补造用户数据、时间、负责人或确认状态。
- 区分事实、推断、待确认项和材料冲突。
- 只加载当前场景需要的参考文件，不机械生成空章节。
- 关注产品结果、规则、反馈和验收，避免替研发决定内部实现。
- 用户已有模板、团队规范和明确指令始终优先。

## 安装

将本仓库复制到 Codex 的个人 Skills 目录：

```bash
git clone https://github.com/Laurel-Lin/adaptive-prd-zh.git ~/.codex/skills/adaptive-prd-zh
```

安装后可在合适的 PRD 工作场景中自动触发，也可以显式指定 `$adaptive-prd-zh`。

## 目录

```text
adaptive-prd-zh/
├── SKILL.md
├── agents/openai.yaml
├── references/
├── NOTICE.md
└── LICENSE
```

具体方法参考及许可边界见 [NOTICE.md](NOTICE.md)。本项目原创内容采用 [MIT License](LICENSE)。
