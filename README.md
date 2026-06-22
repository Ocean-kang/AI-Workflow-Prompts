# AI-Workflow-Prompts

这是一个面向网页版 ChatGPT 使用的 Prompt / Workflow 仓库，用于整理论文阅读、领域论文检索、科研代码生成和通用工作流模板等可复用提示词。

本仓库的核心使用方式是：先在网页版 ChatGPT 中上传任务材料，例如论文 PDF、代码仓库 ZIP、实验日志、需求说明或已有笔记，再粘贴或上传本仓库中对应的 Prompt，让 ChatGPT 按照结构化工作流完成分析、检索、修改建议或输出整理。

## 核心使用方式

使用本仓库时，不建议只把 Prompt 单独发给 ChatGPT。更推荐把 Prompt 与任务文件一起使用：

1. 准备任务材料，例如论文 PDF、代码仓库、日志、截图、数据说明、阅读问题或研究背景。
2. 根据任务类型选择对应目录中的 Prompt。
3. 在网页版 ChatGPT 中上传任务材料。
4. 粘贴 Prompt 内容，或将 Prompt Markdown 文件一并上传。
5. 补充你的具体目标、关注点、输出语言、输出深度和特殊约束。
6. 要求 ChatGPT 严格按照 Prompt 中的流程执行。
7. 检查输出是否区分事实、推断和未知信息，并根据结果继续追问或迭代。

可以直接使用下面的基础提问方式：

```text
我已经上传了任务文件和对应 Prompt。请先阅读所有上传内容，然后严格按照 Prompt 中的流程执行。

我的任务目标是：{USER_GOAL}
我重点关注：{USER_FOCUS}
期望输出语言：{OUTPUT_LANGUAGE}
期望输出格式：{OUTPUT_FORMAT}
特殊约束：{CONSTRAINTS}
```

## 通用使用流程

1. 明确任务目标：先写清楚要解决什么问题、输出给谁看、结果要用于什么下一步。
2. 选择 Prompt：论文阅读用 `paper-reading/`，领域论文检索用 `domain-paper-search/`，科研代码任务用 `code-generation/`，自定义工作流用 `templates/`。
3. 准备输入材料：尽量上传原始文件，而不是只给零散描述。
4. 改写占位符：将 `{USER_GOAL}`、`{USER_FOCUS}`、`{OUTPUT_FORMAT}` 等变量替换为当前任务内容。
5. 约束输出：明确是否需要表格、分节报告、检查清单、Mermaid 图、代码 diff 或可执行步骤。
6. 检查结果：确认 ChatGPT 没有编造信息，必要时要求它标注“论文明确说明”“合理推断”“未知信息”。
7. 沉淀改进：如果某次改写具有长期复用价值，再整理回对应 Prompt 文件。

## Prompt 文件夹说明

### `paper-reading/`

用于上传论文 PDF 后，让 ChatGPT 进行系统化论文阅读、方法拆解、实验分析和研究价值判断。

适用场景：

- 精读单篇论文。
- 判断论文贡献、局限和实验可信度。
- 将论文内容转化为研究笔记、组会材料或后续实验参考。

常见输入材料：

- 论文 PDF。
- arXiv、OpenReview、会议页面或项目主页链接。
- 用户自己的研究方向、重点问题或已有阅读笔记。

使用方法：

1. 在 ChatGPT 网页版上传论文 PDF。
2. 选择并粘贴或上传以下任一 Prompt：
   - `paper-reading/gpt-paper-reading.md`
   - `paper-reading/gpt-paper-reading-old.md`
3. 补充你的研究背景、关注问题和希望输出的深度。
4. 要求 ChatGPT 优先依据论文 PDF，不确定信息必须明确标注。

两个论文阅读入口是平等展示的：

- `paper-reading/gpt-paper-reading.md`：当前版本，更强调事实来源、问题-方案-证据对应、方法机制、实验支撑和与用户研究方向的关系。
- `paper-reading/gpt-paper-reading-old.md`：旧版增强模板，结构完整，适合需要保留原有阅读框架或对比不同阅读风格时使用。

### `domain-paper-search/`

用于让 ChatGPT 围绕某个研究领域进行论文检索、筛选、分类和研究脉络整理。

适用场景：

- 调研一个方向近几年的顶会论文。
- 判断某个研究问题是否已有成熟路线。
- 找代表论文、阅读顺序、方法分类和潜在研究空白。

常见输入材料：

- 研究领域或关键词。
- 时间范围。
- 优先会议列表。
- 是否允许包含 arXiv。
- 用户自己的研究背景和重点关注问题。

使用方法：

1. 打开 `domain-paper-search/domain-paper-search.md`。
2. 将 `{DOMAIN_OR_KEYWORDS}`、`{YEAR_RANGE}`、`{TOP_CONFERENCES}`、`{ALLOW_ARXIV}`、`{USER_FOCUS}` 等占位符替换为当前需求。
3. 在 ChatGPT 网页版粘贴 Prompt，并明确要求它进行网络检索。
4. 检查输出是否核实 venue，是否把 arXiv 与正式发表论文区分开。

### `code-generation/`

用于上传科研代码仓库或关键源码后，让 ChatGPT 帮助理解代码、定位问题、设计最小修改方案并给出验证方法。

适用场景：

- 科研实验代码生成或修改。
- 训练、评估、推理流程理解。
- 报错、指标异常、配置问题或复现问题排查。
- 要求 ChatGPT 给出局部、可验证、尽量不破坏实验设置的修改建议。

常见输入材料：

- 代码仓库 ZIP 或关键文件。
- 配置文件、运行脚本、报错日志、实验背景。
- 当前问题、目标需求、不能修改的约束和期望输出格式。

使用方法：

1. 在 ChatGPT 网页版上传代码仓库或相关文件。
2. 粘贴 `code-generation/llm-research-code-generation-prompt.md`。
3. 补充 `{PROJECT_BACKGROUND}`、`{CURRENT_PROBLEMS}`、`{TARGET_REQUIREMENTS}`、`{CONSTRAINTS}` 和 `{EXPECTED_OUTPUT}`。
4. 要求 ChatGPT 先理解代码和需求，再给出修改方案；不要在需求不清时直接生成代码。

### `templates/`

用于创建新的通用 Prompt 或 Workflow，也可以作为改写现有 Prompt 的结构参考。

包含文件：

- `templates/workflow-template.md`：工作流模板，适合定义完整任务流程、输入、角色、输出、约束和失败处理。
- `templates/prompt-template.md`：通用 Prompt 模板，适合快速组织“上传文件 + 按 workflow 执行”的任务。
- `templates/output-format-template.md`：输出格式模板，适合统一报告、表格、清单或结构化结果。

适用场景：

- 当前任务没有现成 Prompt，需要新建一个。
- 需要把一次成功的临时 Prompt 整理成长期可复用模板。
- 需要统一不同任务的输入、执行步骤和输出格式。

使用方法：

1. 选择最接近需求的模板。
2. 替换其中的变量占位符。
3. 删除不适用的小节，补充任务特有的约束和失败处理。
4. 确认新 Prompt 不只服务某一次临时任务。

## Prompt 编写与改写约定

- 面向共享使用的说明文档默认使用中文。
- Prompt 应具体、结构化、可复用，避免只有宽泛要求。
- 优先包含使用场景、所需输入、角色设定、任务目标、执行流程、输出要求、约束条件和失败处理。
- 变量占位符使用清晰格式，例如 `{USER_GOAL}`、`{INPUT_MATERIAL}`、`{OUTPUT_FORMAT}`。
- 分析型任务应要求区分已确认事实、合理推断和未知信息。
- 不要在通用模板中加入缺乏依据的事实、结论或领域判断。
- 修改已有 Prompt 时，应保留原本的目标用户、任务范围和输出意图。

## 本地任务记录

`local-tasks/` 用于保存本地任务计划、执行记录和临时上下文，例如 `local-tasks/task001.md`、`local-tasks/task002.md`。

这些文件属于个人工作记录，不属于共享仓库文档，已通过 `.gitignore` 忽略。长期可共享的规则应写入 `AGENTS.md` 或 `SPEC.md`，不要只保存在本地任务文件中。

## 许可证

本仓库使用 MIT License。详细内容见 `LICENSE`。
