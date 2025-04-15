# AI写作团队 - 信息管理系统

**版本:** 1.0
**日期:** {{当前日期}}

## 1. 目录结构

使用以下结构来组织所有团队资产：

```
AI_Writing_Team/
├── Agents/                     # 每个作家AI智能体的档案
│   └── Agent_{名称}_Profile.md
├── Projects/                   # 所有写作项目的根目录
│   └── {项目名称}/             # 特定项目的目录
│       ├── Project_Brief.md      # 项目的主要简报
│       ├── Tasks/                # 已分配的任务
│       │   └── Task_Assignment_{作家AI名称}_{任务ID}.md
│       ├── Submissions/          # 作家AI提交的草稿
│       │   └── Submission_{作家AI名称}_{任务ID}.md
│       ├── Feedback/             # 对提交稿件的反馈
│       │   └── Feedback_{作家AI名称}_{任务ID}_{修订号}.md
│       └── Output/               # 最终整合的输出
│           └── Final_Output_{项目名称}_{版本号}.md
├── System/                     # 核心系统文件
│   ├── Workflow.md             # 工作流程
│   ├── Information_Management.md (本文档)
│   ├── Context_Recovery.md     # 上下文恢复指南
│   ├── User_Manual.md          # 用户手册
│   └── Templates/              # 标准文档模板
│       ├── Agent_Profile_Template.md
│       ├── Project_Brief_Template.md
│       ├── Task_Assignment_Template.md
│       ├── Submission_Template.md
│       ├── Feedback_Template.md
│       └── Log_Entry_Template.md
└── Logs/                       # 系统范围的日志
    └── Activity_Log.md
```

## 2. 命名约定

*   **文件夹:** 使用 `PascalCase` 或描述性名称 (例如, `我的小说项目`)。
*   **文件:** 使用 `PascalCase`，并用下划线 `_` 分隔，包含相关标识符。
    *   `{文件类型}_{标识符}_{版本/日期/AI名称/等}.md`
*   **标识符:**
    *   `{项目名称}`: 写作项目的唯一名称。
    *   `{作家AI名称}`: 作家AI智能体的唯一标识符 (例如, `猫腻风格`).
    *   `{任务ID}`: 项目内特定任务的唯一ID (例如, `第一章草稿`). 可以是序列号或描述性的。
    *   `{修订号}`: 反馈文件的修订编号 (例如, `Rev1`)。
    *   `{版本号}`: 最终输出的版本号 (例如, `v1.0`)。
*   **日期:** 适用时使用 `YYYY-MM-DD` 格式。
*   **任务ID:** 在项目内应保持唯一。建议使用类别和序列的组合，例如 `大纲-01`, `第一章-草稿1`, `角色背景-主角`。

## 3. 元数据 (文件内部)

每个Markdown文件应以YAML front matter块（可选，但推荐用于未来自动化）或包含关键元数据的清晰标题部分开头：

**标题示例:**

```markdown
--- (可选的 YAML Front Matter)
Project: 我的小说项目
TaskID: 第一章-草稿1
Agent: 猫腻风格
Version: 1.0
Date: {{当前日期}}
Status: 已提交
---

**文件类型:** 提交稿
**项目:** 我的小说项目
**任务 ID:** 第一章-草稿1
**作家AI:** 猫腻风格
**提交日期:** {{当前日期}}
**状态:** 已提交

--- (正文内容从这里开始)
```

关键元数据包括:
*   `文件类型`: (例如, 简报, 任务, 提交稿, 反馈, 档案)
*   `项目`: 项目名称
*   `任务 ID`: 关联的任务ID (如果适用)
*   `作家AI`: 分配的/提交的作家AI (如果适用)
*   `日期`: 创建/提交/反馈日期
*   `版本/修订`: 适用的版本或修订号
*   `状态`: (例如, 已分配, 进行中, 已提交, 需修改, 已批准, 已完成)

## 4. 日志记录

`Logs/` 目录中的 `Activity_Log.md` 文件将记录关键事件：
*   项目创建
*   任务分配
*   收到提交稿
*   提供反馈
*   生成输出
*   作家AI添加/更新

条目应遵循 `Log_Entry_Template.md` 模板格式。 