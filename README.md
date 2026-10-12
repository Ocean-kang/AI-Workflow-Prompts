# AI-Workflow-Prompts

<p align="center">
  <img src="./assets/readme/hero.svg" width="100%" alt="AI-Workflow-Prompts：可复用的科研工作流与 Prompt 模板。材料 → Prompt → 交付。">
</p>

**可复用的科研工作流与 Prompt 模板，主要用于网页版 ChatGPT。**

把论文阅读、研究调研、代码开发和科研展示整理成结构化流程，明确所需输入、执行步骤和交付结果。

## 选择工作流

按任务打开对应目录，选择适用的 Prompt：

| 任务入口 | 用途 |
| --- | --- |
| [论文阅读](./paper-reading/) | 单篇论文速读、精读与创新分析 |
| [科研流程讲解](./paper-research-process/) | 串联论文的问题、设计、证据与结论 |
| [领域论文检索](./domain-paper-search/) | 从网络检索、筛选和整理领域论文 |
| [论文集合综述](./literature-review/) | 综合已收集的论文，形成批判性综述 |
| [科研代码](./code-generation/) | 理解、生成、修改和排查科研代码 |
| [科研 PPT](./presentation-generation/) | 先生成制作规划，再按规划制作 PPTX |
| [通用模板](./templates/) | 编写或改造 Prompt、工作流与输出格式 |

## 如何使用

1. **选择 Prompt**：从上面的任务入口选择一个模板。
2. **提供材料**：在 ChatGPT 中上传论文 PDF、代码 ZIP、日志或笔记等材料，并上传 Prompt Markdown 文件或粘贴其正文。检索任务可直接提供主题，无需先上传论文。
3. **说明目标并开始**：补充本次想解决的问题，按下面两种方式之一发送请求。

将 `{PROMPT_FILE}` 换成选定的 Prompt 文件名，将 `{USER_GOAL}` 等占位符换成实际内容；没有补充要求时，删除对应行即可。

### 直接执行（Direct Mode）

适合目标和材料已明确时使用。选择直接执行版；可选项沿用模板默认值，只在缺少关键输入时澄清。

```text
请使用我上传或粘贴的 Prompt：
「{PROMPT_FILE}」
结合本次材料直接执行。

任务目标：{USER_GOAL}
补充要求（可选）：{REQUIREMENTS}
```

### 先询问再执行（Interactive Mode）

适合先澄清目标、关注点或输出要求时使用。选择 `*-interactive.md` 模板；交互版包含完整流程，可独立使用，无需同时上传直接版。

```text
请使用我上传或粘贴的交互版 Prompt：
「{PROMPT_FILE}」

初步目标：{USER_GOAL}
请先检查材料，询问必要问题。
等我明确说“开始”后再正式执行。
```

回答必要问题后，发送“开始”即可进入正式执行。

收到结果后，检查关键结论的依据，并留意未确认的信息和缺失材料带来的限制。

---

[工作流规范](./SPEC.md) · [仓库维护规则](./AGENTS.md) · [MIT 许可证](./LICENSE)
