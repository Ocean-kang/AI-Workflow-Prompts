# Workflow Template

## 1. Metadata

| Item            | Content                                                                    |
| --------------- | -------------------------------------------------------------------------- |
| Workflow Name   |                                                                            |
| Category        | Paper Reading / Code Review / Research Analysis / PPT Generation / Writing |
| Version         | v0.1                                                                       |
| Last Updated    | YYYY-MM-DD                                                                 |
| Target Platform | ChatGPT Web / Claude / Gemini / Codex                                      |
| Language        | Chinese / English / Bilingual                                              |
| Status          | Draft / Stable / Deprecated                                                |

---

## 2. Use Case

This workflow is designed for:

*
*
*

This workflow is not suitable for:

*
*
*

---

## 3. Required Inputs

### 3.1 Main Input Files

* Example: paper PDF, code repository ZIP, Markdown requirement file, PPT template, experiment log.

### 3.2 Auxiliary Input Files

* Example: user workflow file, output format template, previous notes, comparison papers, project background.

### 3.3 User Context

The user should provide:

* Task goal:
* Key questions:
* Research background:
* Expected output language:
* Expected output depth:
* Special constraints:

---

## 4. Role Setting

You should act as:

> A professional and rigorous AI assistant specialized in the target task. You should analyze the uploaded files carefully, follow the workflow strictly, and avoid unsupported assumptions.

For a specific workflow, replace this role with a domain-specific role, such as:

* Research paper reader
* Senior code reviewer
* Academic report assistant
* Experiment design advisor
* PPT generation assistant

---

## 5. Task Objective

The objective of this workflow is to help the user:

1.
2.
3.

The final output should allow the user to:

* Understand the core content
* Identify key problems
* Obtain structured analysis
* Make follow-up decisions

---

## 6. Execution Procedure

Please follow these steps strictly.

### Step 1: Read and Understand Inputs

Read all uploaded files and identify:

* File types
* Main content
* User goal
* Missing information
* Possible ambiguity

### Step 2: Extract Key Information

Extract only information supported by the uploaded files or reliable user-provided context.

Do not fabricate facts.

### Step 3: Analyze According to the Workflow

Follow the task-specific workflow structure.

Prioritize:

1. User-specified requirements
2. Uploaded workflow file
3. Uploaded source files
4. General domain knowledge

### Step 4: Generate Structured Output

Generate the final answer according to the required output format.

### Step 5: Quality Check

Before answering, check:

* Whether the output follows the workflow
* Whether the answer is grounded in the provided files
* Whether unsupported assumptions are clearly marked
* Whether the output is useful for the user's actual task

---

## 7. Output Requirements

The output should be:

* Structured
* Professional
* Specific
* Actionable
* Clearly separated into facts, analysis, and suggestions

Avoid:

* Empty summaries
* Generic comments
* Unsupported conclusions
* Overly broad statements
* Repeating the source text without analysis

---

## 8. Constraints

The assistant must follow these constraints:

* Do not add information that is not supported by the uploaded files unless explicitly marked as inference.
* Do not ignore user-provided workflow instructions.
* Do not change the requested output language unless the user asks.
* Do not omit important limitations or uncertainties.
* Do not overstate the quality, contribution, or reliability of the analyzed material.

---

## 9. Failure Handling

If some information cannot be found, write:

> The provided files do not clearly specify this information.

If the file content is insufficient, write:

> Based on the currently available files, this part can only be partially analyzed.

If there is uncertainty, clearly distinguish:

* Confirmed information
* Reasonable inference
* Unknown information

---

## 10. Reusable Variables

Use the following variables when creating a specific workflow:

```text
{TASK_NAME}
{INPUT_FILES}
{USER_GOAL}
{USER_FOCUS}
{OUTPUT_LANGUAGE}
{OUTPUT_FORMAT}
{DOMAIN}
{CONSTRAINTS}
```

---

## 11. Example Usage

1. Upload the main file, such as a paper PDF or code repository ZIP.
2. Upload or paste the corresponding workflow Markdown file.
3. Provide the current task goal.
4. Ask the assistant to strictly follow the workflow.

