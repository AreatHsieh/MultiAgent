# MultiAgent

`MultiAgent` 只保存 agent 流程、prompt、template、文件與範例，不承擔正式專案工作區。

## 目前結構

```text
MultiAgent/
  team-template/
    prompts/
    workflow/
    templates/
    examples/
    docs/
```

## 放置規則

- 正式專案實作放在 `/mnt/d/AIProject/Workspaces/<project-name>/`。
- 搬遷前資料、舊需求與歷史輸出放在 `/mnt/d/AIProject/Archives/`。
- 不要在 `MultiAgent` 底下建立正式專案 repo。
- 不要把 build output、測試資料或正式專案產物放進 `team-template`。

## 主要入口

- `team-template/`: PM-led agent team 的流程範本。
- `team-template/docs/`: 操作說明與歷史說明文件。
- `team-template/examples/commands/`: 可複製使用的指令範本。
