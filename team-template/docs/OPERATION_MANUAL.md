# 操作手冊

這份手冊只講你實際要怎麼操作這套 RA / CRA / PM / SA / SD / PG 團隊。

## 目標

新專案時，你只需要：

1. 把需求文件放進 `/mnt/d/AIProject/Workspaces/<project-name>/docs/references/project_idea/requirements.md`
2. 對 Codex CLI 主 agent 下指令

既有專案增修時，你只需要：

1. 先用 CRA 對談整理增修需求，或直接準備 `change-request.md`
2. 對 Codex CLI 主 agent 下 PM change kickoff 指令

之後由 PM agent 自己：

- 讀需求
- 必要時委派 CRA agent 釐清既有專案增修需求
- 委派 SA agent
- 委派 SD agent
- 收斂結果
- 建立 `/mnt/d/AIProject/Workspaces/<project-name>/`
- 產出系統文件

## 標準目錄

### 新專案

- 輸入：`/mnt/d/AIProject/Workspaces/<project-name>/docs/references/project_idea/requirements.md`
- 輸出：`/mnt/d/AIProject/Workspaces/<project-name>/`

輸出資料夾通常包含：

- `system-spec.md`
- `ui-proposal.md`
- `api-spec.md`
- `domain-model.md`
- `implementation-plan.md`
- `open-questions.md`

### 既有專案增修

- 輸入：`/mnt/d/AIProject/Workspaces/<project-name>/change-requests/CR-###/change-request.md`
- 輸出：`/mnt/d/AIProject/Workspaces/<project-name>/change-requests/CR-###/`

增修資料夾通常包含：

- `change-request.md`
- `impact-analysis.md`
- `implementation-plan.md`

## 新專案操作步驟

1. 建立專案參考資料夾 `/mnt/d/AIProject/Workspaces/<project-name>/docs/references/project_idea/`。
2. 在該資料夾放入 `requirements.md`。
3. 打開 [pm-kickoff-template.md](/mnt/d/AIProject/MultiAgent/team-template/examples/commands/pm-kickoff-template.md)。
4. 把裡面的 `<project-name>` 換成你的專案名稱。
5. 把整段文字貼給 Codex CLI 主 agent。
6. 等 PM 團隊完成討論與文件輸出。
7. 到 `/mnt/d/AIProject/Workspaces/<project-name>/` 查看成果。

## 既有專案增修操作步驟

1. 若增修需求還不清楚，打開 [cra-dialogue-template.md](/mnt/d/AIProject/MultiAgent/team-template/examples/commands/cra-dialogue-template.md)。
2. 把整段文字貼給 Codex CLI 主 agent，讓 CRA 跟你對談。
3. CRA 會將結果寫入 `/mnt/d/AIProject/Workspaces/<project-name>/change-requests/CR-###/change-request.md`。
4. 打開 [pm-change-kickoff-template.md](/mnt/d/AIProject/MultiAgent/team-template/examples/commands/pm-change-kickoff-template.md)。
5. 把裡面的 `<project-name>` 與 `<CR-###>` 換成你的專案名稱與變更編號。
6. 把整段文字貼給 Codex CLI 主 agent。
7. 等 PM 團隊完成影響分析與實作計畫。
8. 到 `/mnt/d/AIProject/Workspaces/<project-name>/change-requests/CR-###/` 查看成果。

## 你不用做的事

- 不用分別和 SA / SD 對話
- 不用在增修需求模糊時自己整理完整規格，CRA 會先幫你問清楚
- 不用手動建立 `/mnt/d/AIProject/Workspaces/<project-name>/`
- 不用自己整理 system spec

## 新專案簡單案例

### 案例名稱

`leave-request-system`

### 需求檔位置

`/mnt/d/AIProject/Workspaces/leave-request-system/docs/references/project_idea/requirements.md`

### 你要貼給 Codex 的指令

```md
請你擔任 PM agent。

需求文件在：
`/mnt/d/AIProject/Workspaces/leave-request-system/docs/references/project_idea/requirements.md`

請你依照以下方式執行：

1. 先閱讀需求文件。
2. 主動委派 SA agent 分析：
   - business rules
   - workflow rules
   - edge cases
   - acceptance considerations
3. 主動委派 SD agent 分析：
   - system modules
   - domain model
   - data model
   - API spec
   - technical risks
   - UI 建議所需的系統互動流程
4. 收斂 SA 與 SD 的討論結果。
5. 若 `/mnt/d/AIProject/Workspaces/leave-request-system/` 不存在，請自行建立。
6. 將結果寫入以下文件：
   - `/mnt/d/AIProject/Workspaces/leave-request-system/system-spec.md`
   - `/mnt/d/AIProject/Workspaces/leave-request-system/ui-proposal.md`
   - `/mnt/d/AIProject/Workspaces/leave-request-system/api-spec.md`
   - `/mnt/d/AIProject/Workspaces/leave-request-system/domain-model.md`
   - `/mnt/d/AIProject/Workspaces/leave-request-system/implementation-plan.md`
   - `/mnt/d/AIProject/Workspaces/leave-request-system/open-questions.md`

請不要把工作回丟給我，也不要要求我分別和 SA / SD 對話。
若資訊不足，請先由 PM 與 SA / SD 討論，再把未決事項整理到 `/mnt/d/AIProject/Workspaces/leave-request-system/open-questions.md`。
```

### 完成後你去哪裡看

看這個資料夾：

`/mnt/d/AIProject/Workspaces/leave-request-system/`

你會看到：

- [system-spec.md](/mnt/d/AIProject/Workspaces/leave-request-system/system-spec.md)
- [ui-proposal.md](/mnt/d/AIProject/Workspaces/leave-request-system/ui-proposal.md)
- [api-spec.md](/mnt/d/AIProject/Workspaces/leave-request-system/api-spec.md)
- [domain-model.md](/mnt/d/AIProject/Workspaces/leave-request-system/domain-model.md)
- [implementation-plan.md](/mnt/d/AIProject/Workspaces/leave-request-system/implementation-plan.md)
- [open-questions.md](/mnt/d/AIProject/Workspaces/leave-request-system/open-questions.md)

## 既有專案增修簡單案例

### 案例名稱

`ClawTaskViewer`

### CRA 先整理變更需求

先貼上：

```text
team-template/examples/commands/cra-dialogue-template.md
```

CRA 完成後會產生類似：

```text
/mnt/d/AIProject/Workspaces/ClawTaskViewer/change-requests/CR-001/change-request.md
```

### PM 接手分析變更

再貼上：

```text
team-template/examples/commands/pm-change-kickoff-template.md
```

並將：

```text
<project-name> = ClawTaskViewer
<CR-###> = CR-001
```

PM 完成後會產生：

```text
/mnt/d/AIProject/Workspaces/ClawTaskViewer/change-requests/CR-001/impact-analysis.md
/mnt/d/AIProject/Workspaces/ClawTaskViewer/change-requests/CR-001/implementation-plan.md
```

## 一句話版本

新專案：把需求放進 `/mnt/d/AIProject/Workspaces/<project-name>/docs/references/project_idea/requirements.md`，再把 PM kickoff 指令貼給 Codex。

既有專案增修：先用 CRA 產出 `change-request.md`，再用 PM change kickoff 產出影響分析與實作計畫。
