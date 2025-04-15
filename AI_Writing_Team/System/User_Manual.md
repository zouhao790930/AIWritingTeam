# AI写作团队 - 用户手册

**版本:** 1.0
**日期:** {{当前日期}}

欢迎使用AI写作团队！本手册将指导您如何与Leader AI（领导AI）及整个团队协作，以完成您的写作项目。

## 1. 团队结构与沟通方式

*   **核心角色:** 您（用户）、Leader AI（领导AI）、Writer AI Agents（作家AI智能体）。
*   **领导AI职责:** 理解您的需求、分配任务给合适的作家AI、审阅稿件、整合内容、交付最终输出、管理项目流程。
*   **作家AI职责:** 根据分配的任务和自身的风格特点执行写作。
*   **沟通媒介:** **所有沟通都通过Markdown文件进行**。您需要创建、编辑或查阅指定目录下的 `.md` 文件来与团队互动。

## 2. 核心系统文件（请先熟悉）

位于 `AI_Writing_Team/System/` 目录下：

*   `Workflow.md`: 描述了标准的项目操作流程。
*   `Information_Management.md`: 定义了目录结构、文件命名规范和元数据标准。
*   `Context_Recovery.md`: 提供了在会话中断后如何恢复工作状态的指南和提示词模板。
*   `User_Manual.md`: 本手册。

## 3. 发起一个新项目

1.  **创建项目目录:** 在 `AI_Writing_Team/Projects/` 下创建一个新的项目文件夹，例如 `AI_Writing_Team/Projects/我的新小说/`。
2.  **创建项目简报:** 在新建的项目文件夹内，复制 `AI_Writing_Team/System/Templates/Project_Brief_Template.md` 并重命名为 `Project_Brief.md`。
3.  **填写项目简报:** 打开 `Project_Brief.md`，根据模板提示，尽可能详细地填写项目目标、风格要求（可以选择哪个作家AI或描述新需求）、目标受众、关键元素、篇幅、截止日期等信息。
4.  **通知Leader AI:** 向Leader AI发送消息，明确告知新的项目简报已创建，并提供文件路径：`AI_Writing_Team/Projects/我的新小说/Project_Brief.md`。

## 4. 项目执行与互动

*   **任务分配:** Leader AI会分析简报，并在项目目录的 `Tasks/` 子目录下创建任务分配文件 (`Task_Assignment_*.md`)。
*   **查看进度:** 您可以通过检查项目目录下的 `Tasks/`, `Submissions/`, `Feedback/` 子目录中的文件，以及 `AI_Writing_Team/Logs/Activity_Log.md` 来跟踪项目进展。
*   **审阅提交稿:** Leader AI审阅作家AI提交的稿件（位于 `Submissions/` 目录）后，会进行整合或要求修改。
*   **提供反馈:** 如果Leader AI或您认为某部分稿件需要修改，可以通过创建反馈文件 (`Feedback_*.md` in `Feedback/`) 或直接向Leader AI说明需要修改的内容和原因。Leader AI会负责将反馈传达给相应的作家AI。
*   **接收最终稿:** Leader AI完成整合和审阅后，会在项目目录的 `Output/` 子目录下生成最终稿 (`Final_Output_*.md`)，并通知您。

## 5. 管理作家AI智能体

*   **查看档案:** 每个作家AI的风格和能力定义在 `AI_Writing_Team/Agents/Agent_{名称}_Profile.md` 文件中。
*   **添加新作家AI:**
    1.  准备好新作家AI的风格提示词。
    2.  使用 `AI_Writing_Team/System/Templates/Agent_Profile_Template.md` 在 `Agents/` 目录下创建一个新的档案文件，例如 `Agent_新风格作家_Profile.md`。
    3.  将风格提示词填入档案文件中。
    4.  通知Leader AI有新的作家AI档案已添加，并提供文件路径。

## 6. 处理会话中断

如果与Leader AI的会话中断，请参照 `AI_Writing_Team/System/Context_Recovery.md` 中的说明和提示词模板来恢复会话和项目状态。

## 7. 文件模板

所有标准文档的模板位于 `AI_Writing_Team/System/Templates/` 目录下。请在创建新文档时使用相应的模板。

## 8. 日志

`AI_Writing_Team/Logs/Activity_Log.md` 文件记录了团队活动的关键步骤，便于追踪和审计。

---

如有任何疑问，请随时向Leader AI提问。 