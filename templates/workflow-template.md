# Workflow Template

## 1. Workflow Name

在这里填写该 workflow 的名称。

示例：

* Paper Reading Workflow
* Code Review Workflow
* Research Feasibility Analysis Workflow
* PPT Generation Workflow

---

## 2. Use Case

说明这个 workflow 适合解决什么问题。

本 workflow 适用于：

*
*
*

不适用于：

*
*
*

---

## 3. Input Files

说明使用该 workflow 时需要上传或提供哪些输入。

需要的输入包括：

1. 主输入文件：

   * 例如：论文 PDF、代码仓库 ZIP、实验报告、Markdown 文档

2. 辅助输入文件：

   * 例如：任务说明、输出格式模板、已有总结、参考资料

3. 用户补充信息：

   * 例如：研究方向、关注问题、已有代码环境、目标会议、输出语言

---

## 4. Role Setting

你需要扮演以下角色：

> 在这里描述 ChatGPT 应该具备的角色能力。

示例：

你是一个严谨的科研助手，擅长阅读论文、分析方法贡献、拆解实验设计，并能结合用户的研究方向给出可执行建议。

---

## 5. Task Objective

你的任务目标是：

1.
2.
3.

最终需要帮助用户得到：

*
*
*

---

## 6. Execution Steps

请严格按照以下步骤执行：

### Step 1: Understand the Input

先阅读所有输入文件，明确文件内容、任务目标和用户关注点。

### Step 2: Extract Key Information

从输入中提取核心信息，不要添加无依据内容。

### Step 3: Analyze According to the Workflow

按照本 workflow 的结构进行分析。

### Step 4: Generate the Final Output

按照指定格式输出完整结果。

### Step 5: Quality Check

输出前检查以下内容：

* 是否遗漏关键输入信息
* 是否存在无依据推断
* 是否满足用户指定格式
* 是否明确区分事实、分析和建议

---

## 7. Output Format

请按照以下格式输出：

```md
# 标题

## 1. 背景与任务目标

## 2. 核心内容总结

## 3. 关键分析

## 4. 结论

## 5. 后续建议
```

---

## 8. Constraints

必须遵守以下要求：

* 不要添加输入文件中不存在的事实性内容
* 不要跳过 workflow 中要求的步骤
* 不要只做表面总结，需要进行结构化分析
* 不确定的地方必须明确说明
* 输出应当专业、严谨、清晰

---

## 9. Custom Variables

使用时可以替换以下变量：

```text
{TASK_NAME}：任务名称
{INPUT_FILE_TYPE}：输入文件类型
{OUTPUT_LANGUAGE}：输出语言
{USER_FOCUS}：用户重点关注的问题
{OUTPUT_FORMAT}：输出格式要求
```

---

## 10. Example Usage

使用方式：

1. 上传需要分析的文件
2. 上传或复制本 workflow
3. 补充当前任务目标
4. 要求 ChatGPT 严格按照 workflow 执行
