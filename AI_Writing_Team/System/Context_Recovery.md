# AI写作团队 - 上下文恢复指南

**版本:** 1.0
**日期:** {{当前日期}}

## 1. 目的

本文档旨在提供在AI会话中断（例如，由于上下文长度限制、系统重启或意外关闭）后，恢复Leader AI（领导AI）和整个写作项目工作状态的标准流程和必要提示词。

## 2. 恢复流程

1.  **识别中断点:** 确定中断发生时正在进行的具体项目和任务。
    *   检查 `AI_Writing_Team/Logs/Activity_Log.md` 获取最新活动记录。
    *   检查相关项目目录 (`AI_Writing_Team/Projects/{项目名称}/`) 下的 `Tasks/`, `Submissions/`, `Feedback/` 子目录，查看文件状态和时间戳。

2.  **准备恢复提示词:** 根据中断点和需要恢复的任务，准备相应的提示词（见第3节）。

3.  **重启Leader AI会话:** 开启一个新的与Leader AI的会话。

4.  **提供恢复提示词:** 将准备好的恢复提示词提供给Leader AI。

5.  **验证状态:** Leader AI将根据提示词读取相关文件（如项目简报、任务分配、日志等），重建其内部状态，并确认当前的项目进度和下一步行动。

6.  **继续工作:** 一旦Leader AI确认状态已恢复，即可继续按照 `Workflow.md` 中的流程进行。

## 3. 恢复提示词模板 (提供给Leader AI)

请根据实际情况修改和组合以下模板。

**通用启动提示词:**

```
你是AI写作团队的Leader AI。我们的协作基于以下核心系统文件，请先熟悉它们：
1. 工作流程: `AI_Writing_Team/System/Workflow.md`
2. 信息管理: `AI_Writing_Team/System/Information_Management.md`
3. 用户手册: `AI_Writing_Team/System/User_Manual.md`
4. 作家AI档案位于: `AI_Writing_Team/Agents/`
5. 项目文件位于: `AI_Writing_Team/Projects/`
6. 系统日志位于: `AI_Writing_Team/Logs/Activity_Log.md`

请确认你已理解这些文件定义的结构和流程。
```

**恢复特定项目提示词:**

```
我们需要恢复对项目 `{项目名称}` 的工作。

1.  请读取项目简报: `AI_Writing_Team/Projects/{项目名称}/Project_Brief.md`。
2.  请检查最新的任务状态，浏览以下目录中的文件：
    *   `AI_Writing_Team/Projects/{项目名称}/Tasks/`
    *   `AI_Writing_Team/Projects/{项目名称}/Submissions/`
    *   `AI_Writing_Team/Projects/{项目名称}/Feedback/`
3.  请查阅最新的相关日志条目: `AI_Writing_Team/Logs/Activity_Log.md` (搜索与 `{项目名称}` 相关的条目)。

根据这些信息，请总结项目 `{项目名称}` 当前的整体状态，以及需要立即处理的下一步任务是什么（例如，分配新任务、审阅提交稿、等待用户反馈等）？
```

**恢复特定任务提示词 (如果中断发生在某个具体任务的处理过程中):**

```
我们需要恢复对项目 `{项目名称}` 中任务 `{任务ID}` 的处理。

1.  请读取相关的任务分配文件: `AI_Writing_Team/Projects/{项目名称}/Tasks/Task_Assignment_{作家AI名称}_{任务ID}.md`
2.  (如果适用) 请读取相关的提交稿文件: `AI_Writing_Team/Projects/{项目名称}/Submissions/Submission_{作家AI名称}_{任务ID}.md`
3.  (如果适用) 请读取相关的反馈文件: `AI_Writing_Team/Projects/{项目名称}/Feedback/Feedback_{作家AI名称}_{任务ID}_{修订号}.md`

我们上次中断时正在 [描述中断前的具体操作，例如：正在审阅提交稿 / 准备分配任务 / 等待作家AI修改]。请基于文件内容，确认任务 `{任务ID}` 的当前状态，并告诉我接下来应该做什么。
```

## 4. 注意事项

*   **文件是关键:** 由于所有状态都存储在文件中，确保文件是最新的至关重要。
*   **清晰的日志:** 保持 `Activity_Log.md` 的清晰和及时更新，有助于快速定位中断点。
*   **逐步恢复:** 如果不确定中断点，可以先使用通用启动提示词，然后逐步聚焦到具体项目和任务。 