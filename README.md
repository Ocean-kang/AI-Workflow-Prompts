# AI-Workflow-Prompts

## 仓库介绍

这是一个可复用的 AI 工作流与 Prompt 模板仓库，主要用于网页版 ChatGPT。
它把论文阅读、研究调研、科研开发和展示等任务整理成结构化工作流，
减少每次从零编写提示词的重复工作，
让任务需要什么输入、如何执行、交付什么结果更清楚。

按任务类型选择对应目录：

```text
AI-Workflow-Prompts/
├── paper-reading/              # 单篇论文速读、精读与创新分析
├── paper-research-process/     # 按科研论证流程讲解论文
├── domain-paper-search/        # 从网络检索、筛选和整理领域论文
├── literature-review/          # 综合已收集的论文，形成综述
├── code-generation/            # 理解、生成、修改和排查科研代码
├── presentation-generation/    # 科研 PPT 规划与制作
├── templates/                  # 编写或改造 Prompt 的通用模板
├── AGENTS.md                   # 仓库维护规则
├── SPEC.md                     # 工作流与文档规范
└── LICENSE                     # MIT 许可证
```

## 如何使用

1. **选择 Prompt**：根据任务选择目录，
   打开其中一个适用的 Prompt。
2. **提供材料**：在 ChatGPT 中上传论文 PDF、代码 ZIP、日志或笔记等所需材料，
   并上传选定的 Prompt Markdown 文件，或粘贴其正文。
   检索任务可直接提供主题，无需先上传论文。
3. **说明目标并开始**：补充本次想解决的问题，
   按下面两种方式之一发送请求。

下面的示例适用于各任务目录。
将 `{PROMPT_FILE}` 换成选定的 Prompt 文件名，
将 `{USER_GOAL}` 等占位符换成实际内容；
没有补充要求时，删除对应行即可。

### 直接执行（Direct Mode）

适合任务目标和所需材料已经明确时使用。
选择标明 Direct Mode 的模板；
可选项沿用模板默认值，只在缺少关键输入时澄清。

```text
请按我上传或粘贴的 Prompt「{PROMPT_FILE}」直接执行，结合本次提供的材料完成任务。

任务目标：{USER_GOAL}
补充要求（可选）：{REQUIREMENTS}
```

### 先询问再执行（Interactive Mode）

适合需要先澄清目标、关注点或输出要求时使用。
选择 `*-interactive.md` 模板；
交互版已包含完整流程，可独立使用，无需同时上传直接版。

```text
请按我上传或粘贴的交互版 Prompt「{PROMPT_FILE}」开展任务。

初步目标：{USER_GOAL}
请先检查材料并询问必要问题，等我明确说“开始”后再正式执行。
```

回答必要问题后，发送“开始”即可进入正式执行。

收到结果后，检查关键结论的依据，
并留意未确认的信息和缺失材料带来的限制。
