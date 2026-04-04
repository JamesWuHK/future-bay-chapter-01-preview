# Chapter 01 Workflow Remediation To-Do

## 1. 文档用途

这份清单用于承接 `2026-04-04` 这轮 chapter-01 workflow 逐门质量检查后的整改动作。

它不是新的平行规则文档，而是当前唯一正式的 `整改待办 + 进度回写` 入口。后续凡是本轮整改涉及的状态更新，都先回写这里，再同步到对应主文件。

## 2. 当前判断

- 当前最强环节：`W0 语义冻结`、`W1 导演室调度`
- 当前中段环节：`W2 分镜执行稿`、`W4 首帧生成`、`W5 图像质量门`、`W8 视频生成`、`W9 视频质量门`、`W10 剪辑装配`
- 当前最弱环节：`W3 参考锁定`、`W7 视频导演与 audio contract`、`W11 交付更新与归档`
- 当前最大的系统性问题：`上游文稿链已经较新，下游状态控制层和资产总览页口径没有完全同步，大文件里的旧命名和旧总述还在拖 current 后腿`

## 3. 整改原则

- 只维护一个整改主清单，不重复新建“第二版待办”
- 先修状态源，再修展示层
- 先关 active lane，再做泛化 polish
- 所有 `DONE` 都必须对应到主文件回写，不能只停留在口头说明

## 4. 优先级总表

| ID | 优先级 | 对应 workflow | 整改项 | 主文件 | 当前状态 | 完成标准 |
| --- | --- | --- | --- | --- | --- | --- |
| T01 | P0 | `W11` | 重建 current 口径，补 `asset-manifest.json` 的总表说明 | `production/asset-manifest.json` | `DONE WITH NOTES` | manifest 能独立回答每个 part 当前做到哪一步 |
| T02 | P0 | `W8-W10` | 对齐 active lane 与 current master 口径 | `production/video-loop-state.json`、`production/version-log.md` | `IN PROGRESS` | `loop-state` 和 `version-log` 顶部 current 结论不打架 |
| T03 | P0 | `W3` | 写清 `回响` 的出镜 gate 和限制 | `visual/character-lock-pack.md`、`content/actors/actor-casting-dossier.html` | `DONE WITH NOTES` | 回响要么只保留非清晰主体存在，要么补完可见锁定后再入视频主线 |
| T04 | P0 | `W0-W7` | 更新 prompt 基线，让语言、对白、角色说话方式与最新主稿一致 | `visual/prompt-bible.md` | `DONE` | prompt bible 明确 10-12 岁语言约束、去 AI 腔规则、角色说话区分 |
| T05 | P1 | `W11` | 让资产总览页只吃 current 可信状态源 | 资产总览 HTML 页面 | `DONE WITH NOTES` | 页面不再自己拼状态，而是忠实展示 current |
| T06 | P1 | `W7` | 单独拉清 `P04` 的修复账，并把等待区压力链写死到 current 合同里 | `production/video-loop-state.json`、`production/current-part-repair-contracts.md`、`story/storyboard-script.md`、`production/shot-list.md` | `IN PROGRESS` | `P04` 哪些是真视频、哪些是桥接、哪些仍欠替换写清楚，而且 `等待区 -> 签字笔 -> 安抚屏 -> 父亲逻辑 -> 林澄反问` 的单线后果已经写进修复合同，并反向同步到 storyboard / shot list |

## 5. 当前回合执行记录

### 2026-04-04 / Round 1

- `DONE WITH NOTES`：`T01` 已把 `asset-manifest.json` 重建为 current 状态总表，不再沿用早期失真的逐资产 `todo` 列表
- `DONE WITH NOTES`：`T03` 已写死 `回响` 的出镜 gate；演员总册当前口径已一致，无需本回合重复改写
- `DONE`：`T04` 已更新 `prompt-bible.md` 的版本、语言底线、去 AI 腔约束与角色说话区分
- `IN PROGRESS`：`T02` 已更新 `video-loop-state.json`，把它与新的 manifest / remediation todo 口径绑上；下一步只剩 `version-log.md` 顶部 current 结论对齐
- `IN PROGRESS`：`T06` 已新增 `active_repair_contract`，并补出 `current-part-repair-contracts.md` 作为 active lane 细修入口

### 2026-04-04 / Round 2

- `DONE WITH NOTES`：`T05` 已把整改主清单和 active lane 修复合同直接挂到预览页，页面现在会展开主清单与 `P04` 修复合同，不再只展示几张状态卡片
- `DONE WITH NOTES`：`T05` 同步把资产总览页的 current 口径继续收紧到主仓状态源；以后整改先回写 source of truth，再让页面自动跟上，不再在页面手写第二套状态
- `IN PROGRESS`：`T02` 仍未闭环。当前 `loop-state`、`manifest`、预览页已经对齐，但 `version-log.md` 顶部 current 摘要还没补到同一口径前，不把它误写成 `DONE`
- `IN PROGRESS`：`T06` 继续维持为本轮 active quality lane。当前已把 `P04` 修复目标、镜头级判断和通过/失败条件收束到单一合同文档，下一步不是再加说明，而是按合同继续审 `S01-S05`
- `NEXT`：继续完成 `T02` 的 version log 对齐，再沿 `T06` 把 `P04` 的空间连续性、人物一致性和 `P04 -> P05` 承压衔接逐项过门

### 2026-04-04 / Round 3

- `IN PROGRESS`：重新对照 `script.md`、`storyboard-script.md` 和 `shot-list.md` 后，确认 `P04` 之前写得还不够狠：`CH01-P04-S03` 不能只算“等待区锚点”，它必须承担父亲保护逻辑正式落地这一拍
- `IN PROGRESS`：已把 `current-part-repair-contracts.md` 收紧为单一后果链口径：`等待区 -> 签字笔 -> 安抚屏 -> 父亲逻辑 -> 林澄反问 -> P05`
- `IN PROGRESS`：`T06` 当前的真实重点已经从“把修复账写出来”升级成“按修复账逐镜判断 KEEP / TRIM / REDO”
- `IN PROGRESS`：`T02` 仍保持未闭环状态。当前先不假装 `version-log` 已经对齐，避免页面和主控制文件再次长出两套 current 口径

### 2026-04-04 / Round 4

- `DONE WITH NOTES`：`T05` 继续收紧预览页展示边界。`P01/S02` 这类已经淘汰的旧单镜，不再以“说明卡”形式留在资产总览页面里；历史版本只保留在 GitHub commit 历史中，不再占 current 页面位置
- `DONE WITH NOTES`：`T05` 当前新增一条明确页面规则：资产总览页只展示仍在 current 单镜链上的可用资产；已经退回整段装配承接、或已经淘汰的 beat，不再单独挂出
- `IN PROGRESS`：`T02` 仍是下一条必须关掉的状态债务。当前 `preview page / manifest / loop-state` 已继续保持一致，但 `version-log.md` 顶部还没有补成同一套 current 摘要前，不把它改成 `DONE`
- `NEXT`：继续推进 `T02` 的顶部 current 摘要对齐，再回到 `T06` 按 `P04` 修复合同逐镜收口

### 2026-04-04 / Round 5

- `IN PROGRESS`：继续做 `T06` 的 source-of-truth 复审时，发现还有一处没完全跟上 current 合同：`storyboard-script.md` 里的 `CH01-P04-S03` 详细段落曾保留旧选择口径
- `IN PROGRESS`：`shot-list.md` 里也还保留 `p04-s03-waiting-zone-choice-current.mp4` 这一层旧命名。这个名字还能追到历史资产，但已经不能完整表达现在的修复合同重点
- `NEXT`：`T06` 的下一步不只是继续看片，还要把 `storyboard-script.md` 与 `shot-list.md` 的 `P04/S03` 旧口径同步改成 current 合同口径，然后再做 `KEEP / TRIM / REDO` 判断

### 2026-04-04 / Round 6

- `DONE WITH NOTES`：`storyboard-script.md` 里的 `CH01-P04-S03` 已经改成 current 合同口径，不再写成“先和谁谈”的选择入口，而是明确写成“父亲在签字笔与安抚屏同场压力里，说出保护逻辑”
- `IN PROGRESS`：`T06` 当前还剩下一条同类残留：`shot-list.md` 里的 `waiting-zone-choice` 旧命名还没同步掉；它虽然还能追到历史资产，但已经落后于 current 修复合同
- `NEXT`：继续想办法把 `shot-list.md` 的 `P04/S03` 命名与职责也同步到同一口径，然后再推进 `KEEP / TRIM / REDO` 的实质判断

### 2026-04-04 / Round 7

- `DONE WITH NOTES`：`asset-manifest.json` 已进一步收紧 current 口径，不再把 `shot-list` 笼统写成 `DONE`，而是明确标成 `DONE WITH NOTES`，并把 `P04/S03` 的旧命名残留与 `version-log` 顶部摘要未对齐一起记入 current 风险
- `DONE WITH NOTES`：`video-loop-state.json` 已补出两条同步债务标记：`version_log_top_summary = PENDING_ALIGNMENT`、`shot_list_p04_s03_contract = PENDING_ALIGNMENT`，同时把 `P04 next_action` 写成先收 `S03` 命名与职责，再继续 active lane 修复
- `IN PROGRESS`：`T02` 的问题已经从“还没确认差异”收缩成明确的一条大文件残留：`version-log.md` 顶部还停在旧总述，没有把 `current focus = P04`、`official accepted master = chapter-01-vertical-slice-master-v16-current.mp4`、`story spine = v14` 写进去
- `IN PROGRESS`：`T06` 的问题也已经从“哪里不一致”收缩成单点：`shot-list.md` 里 `CH01-P04-S03 / C10` 仍挂着 `p04-s03-waiting-zone-choice-current.mp4` 这层旧名，还没有正式改成“父亲保护逻辑落地”口径
- `NEXT`：下一步只做两件事，不再扩散：先关 `shot-list.md` 的 `P04/S03` 旧命名，再关 `version-log.md` 顶部 current 摘要

## 6. 进度标记规则

- `TODO`：还没开始
- `IN PROGRESS`：已开始改主文件，但还没闭环
- `DONE`：主文件已回写，且本清单已同步
- `DONE WITH NOTES`：已回写，但仍有后续观察项
- `BLOCKED`：被上游条件卡住

## 7. 下一步顺序

1. 继续按新合同复审 `T06 / P04`
2. 完成 `T02` 的 version log 对齐
3. 再做一次 current 口径复核
4. 最后把新结论继续同步到页面与主状态源
