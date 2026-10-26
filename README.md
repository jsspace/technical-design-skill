# Technical Design Skill

一个把需求、现有文档或代码上下文整理成**技术方案 HTML** 的 Codex skill。当前是第一版，写作方法来自用户提供的《如何写好技术文档》，并针对技术方案评审补充了选型、落地和验证环节。

## 安装

将本仓库克隆到 Codex skills 目录：

```bash
git clone https://github.com/jsspace/technical-design-skill.git ~/.codex/skills/technical-design-skill
```

克隆后重新开启 Codex 会话，让 skill 被发现。也可以在当前仓库中直接阅读 `SKILL.md` 并按其说明生成文档。

## 使用

给出方案主题和已有资料，例如：

> 使用 $technical-design-skill，根据 `requirements.md` 和当前仓库，为订单服务的异步化改造写一版技术方案，输出 `docs/order-async-design.html`。读者是后端和运维评审人。

如果已有旧版 HTML，可要求“根据 `old-design.html` 修订并输出新的技术方案 HTML”。生成的 HTML 应能离线打开，包含清晰的目录、论证、实施和验证内容。资料不全时，文档会显式标注假设与待确认事项。

## 仓库内容

- [`SKILL.md`](SKILL.md)：Codex 执行说明。
- [`references/writing-principles.md`](references/writing-principles.md)：从原始文档提炼的写作与图表原则。
- [`assets/technical-design-template.html`](assets/technical-design-template.html)：可按实际方案裁剪的独立 HTML 起始模板。

原始 Word 文档和其中的截图不随仓库发布。
