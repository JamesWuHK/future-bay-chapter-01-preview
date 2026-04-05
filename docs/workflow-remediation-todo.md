# Chapter 01 Workflow Remediation To-Do

## 1. 文档用途

这份清单用于承接 `2026-04-04` 这轮 chapter-01 workflow 逐门质量检查后的整改动作。

它不是新的平行规则文档，而是当前唯一正式的 `整改待办 + 进度回写` 入口。后续凡是本轮整改涉及的状态更新，都先回写这里，再同步到对应主文件。

## 2. 当前判断

- 当前最强环节：`W0 语义冻结`、`W1 导演室调度`
- 当前中段环节：`W2 分镜执行稿`、`W4 首帧生成`、`W5 图像质量门`、`W8 视频生成`、`W9 视频质量门`、`W10 剪辑装配`
- 当前最弱环节：`W3 参考锁定`、`W7 视频导演与 audio contract`、`W11 交付更新与归档`
- 当前最大的系统性问题：`上游文稿链经常比成片链更快更新；如果不明确写出哪些已经进了 part / story spine / master、哪些只是 docs-only，就很容易把“页面变新了”误判成“总装也修完了”`

## 3. 整改原则

- 只维护一个整改主清单，不重复新建“第二版待办”
- 先修状态源，再修展示层
- 先关 active lane，再做泛化 polish
- 所有 `DONE` 都必须对应到主文件回写，不能只停留在口头说明
- 任何修正如果还没进 `part delivery -> story spine -> master current`，只能标成 `DOCS ONLY / NOT COUNTED`，不算总装完成

## 4. 优先级总表

| ID | 优先级 | 对应 workflow | 整改项 | 主文件 | 当前状态 | 完成标准 |
| --- | --- | --- | --- | --- | --- | --- |
| T01 | P0 | `W11` | 重建 current 口径，补 `asset-manifest.json` 的总表说明 | `production/asset-manifest.json` | `DONE WITH NOTES` | manifest 能独立回答每个 part 当前做到哪一步 |
| T02 | P0 | `W8-W10` | 对齐 active lane 与 current master 口径 | `production/video-loop-state.json`、`production/version-log.md` | `DONE WITH NOTES` | `loop-state` 和 `version-log` 顶部 current 结论不打架 |
| T03 | P0 | `W3` | 写清 `回响` 的出镜 gate 和限制 | `visual/character-lock-pack.md`、`content/actors/actor-casting-dossier.html` | `DONE WITH NOTES` | 回响要么只保留非清晰主体存在，要么补完可见锁定后再入视频主线 |
| T04 | P0 | `W0-W7` | 更新 prompt 基线，让语言、对白、角色说话方式与最新主稿一致 | `visual/prompt-bible.md` | `DONE` | prompt bible 明确 10-12 岁语言约束、去 AI 腔规则、角色说话区分 |
| T05 | P1 | `W11` | 让资产总览页只吃 current 可信状态源 | 资产总览 HTML 页面 | `DONE WITH NOTES` | 页面不再自己拼状态，而是忠实展示 current |
| T06 | P1 | `W7-W10` | 单独拉清 `P04` 的修复账，并把等待区压力链写死到 current 合同里 | `production/video-loop-state.json`、`production/current-part-repair-contracts.md`、`story/storyboard-script.md`、`production/shot-list.md` | `DONE WITH NOTES` | `P04` 哪些是真视频、哪些仍是静帧债务、哪些可以 `KEEP / TRIM / REDO` 写清楚，而且 `等待区 -> 签字笔 -> 安抚屏 -> 父亲逻辑 -> 林澄反问 -> P05` 的后果链已经过 clip-level 复审 |
| T07 | P0 | `W10-W11` | 收口 `P06 / E01` 的亮走廊 reset，并把 trimmed ingress 传导到 part、story spine、master、preview current | `production/video-loop-state.json`、`production/asset-manifest.json`、`production/current-part-repair-contracts.md`、`production/version-log.md`、预览页 current 镜像 | `DONE WITH NOTES` | `P06` 开头不再先亮一下再变暗，且 `part-06 current / story spine / master / preview` 都切到同一套 `trimmed-ingress` 口径 |
| T08 | P0 | `W0-W2` | 继续做 chapter-01 真人说话口径整改，清掉孩子听不懂的 AI 腔、文件腔和跳出故事的生硬规则词，并继续把这批改动传导到成片链 | `story/master-episode-script.md`、`story/script.md`、`story/storyboard-script.md`、`audio/voice-script.md`、受影响的 `part delivery` 装配 | `DONE WITH NOTES` | 角色说话能一耳朵分开，10 岁孩子能听懂；受影响改动至少要进对应 `part delivery`，并继续传到当前完整故事入口与 review master；否则只算文稿修正 |
| T09 | P0 | `W11` | 收口 chapter-01 的对外交付入口口径，明确哪条是完整故事 current，哪条只是 review master | `production/asset-manifest.json`、`production/video-loop-state.json`、`production/version-log.md`、资产总览 HTML 页面 | `DONE WITH NOTES` | 页面顶部和状态源都能明确告诉人：当前 `story spine current` 才是完整故事入口，当前 `vertical slice master` 只是 review master |
| T10 | P1 | `W0-W11` | 收口“文稿承诺 vs current 实现”边界，把趣味层、产品稿、上屏文案和资产总览页统一到同一套 current / 后补口径 | `story/script.md`、`story/storyboard-script.md`、`product/product-script.md`、`product/episode-onscreen-copy.md`、`production/shot-list.md`、`production/asset-manifest.json`、`production/video-loop-state.json`、资产总览 HTML 页面 | `DONE WITH NOTES / DOCS ONLY` | 页面和主文档都能一眼看出：哪些趣味层已经进 current，哪些仍是后补，不再把候选资产误写成“已上线”；但这项本身不自动算总装推进 |
| T11 | P0 | `W10-W11` | 审计“文稿 / 页面修正是否真的进了总装”，未进的一律降级成 `DOCS ONLY / NOT COUNTED`，并把最关键的 viewer-visible 修正继续推进到 `part -> story spine -> master` | `production/workflow-remediation-todo.md`、`production/video-loop-state.json`、`production/asset-manifest.json`、`production/version-log.md`、资产总览 HTML 页面、受影响的 `part delivery / assembly` | `IN PROGRESS` | 每条被宣称“已修”的项，都能回答它已进了哪个 `part delivery / story spine / master`；答不出来就降级，答得出来才算有效 |

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

### 2026-04-04 / Round 8

- `DONE WITH NOTES`：公开预览仓已经同步补齐 4 份 current 镜像文件：`docs/workflow-remediation-todo.md`、`docs/current-part-repair-contracts.md`、`data/asset-manifest.json`、`data/video-loop-state.json`。这一步先把“公开页面读不到私有主仓 raw”这个结构问题收成可修的单点
- `IN PROGRESS`：`T05` 现在还剩最后一层页面路由债务。预览页 `index.html` 虽然已经有正文镜像机制，但 workflow 状态和整改区还在直连私有主仓 raw / cdn 地址；下一步必须把这些读取入口改到预览仓本地镜像
- `IN PROGRESS`：`T02` 与 `T06` 的主债务没有变，依然是 `version-log` 顶部摘要未对齐、`shot-list` 的 `P04/S03` 旧命名未收掉
- `NEXT`：下一步顺序继续保持单线：先把预览页 workflow 读取切到公开镜像，再关 `shot-list.md` 的 `P04/S03` 旧命名，最后关 `version-log.md` 顶部 current 摘要

### 2026-04-04 / Round 9

- `DONE WITH NOTES`：预览页 [index.html](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md) 对 workflow 状态、整改清单和 `P04` 修复合同的读取路线已经切到预览仓公开镜像，不再优先依赖私有主仓 raw 地址。现在这页在公开访问时，至少能稳定读到 `data/asset-manifest.json`、`data/video-loop-state.json`、`docs/workflow-remediation-todo.md` 和 `docs/current-part-repair-contracts.md`
- `DONE WITH NOTES`：`T05` 这条页面结构债务现在已经从“公开页经常读不到 source of truth”收缩成“只要镜像按节奏同步，页面就能稳定显示最新 current”。后续观察重点不再是路由，而是镜像同步是否及时
- `IN PROGRESS`：当前剩下的核心质量债务只剩两条：`T06` 的 `shot-list.md / P04-S03 waiting-zone-choice` 旧命名，以及 `T02` 的 `version-log.md` 顶部 current 摘要
- `NEXT`：下一步顺序再收窄一次：先关 `shot-list.md` 的 `P04/S03` 旧命名，再关 `version-log.md` 顶部 current 摘要，然后做一次整页 current 口径复核

### 2026-04-04 / Round 10

- `DONE WITH NOTES`：`shot-list.md` 已把 `CH01-P04-S03 / C10` 从旧的“先走向谁”选择口径，收口成“父亲保护逻辑在等待区压力链里落地”；`waiting-zone-choice` 不再作为 current 合同描述残留在主 shot list。
- `DONE WITH NOTES`：`version-log.md` 顶部 current 摘要已补齐 `active lane = P04`、`official master = chapter-01-vertical-slice-master-v16-current.mp4`、`story spine = v14`，`T02` 从状态不一致收成已对齐。
- `DONE WITH NOTES`：`asset-manifest.json`、`video-loop-state.json` 与公开预览镜像已同步去掉这两条旧同步债务。当前 source of truth 不再卡在旧命名和旧摘要。
- `NEXT`：下一步回到真正的 production 质量复审：继续按 `P04` 修复合同逐镜做 `KEEP / TRIM / REDO`，再复核 `P04 -> P05` 的承压衔接。

### 2026-04-04 / Round 11

- `IN PROGRESS`：已完成 `P04` 的第一轮 clip-level 复审。真实结论比文稿层更严格：`S01`、`S02` 还不能算真 clip 过门，当前仓库里的 current clip 实际仍指向缺失源视频，成片里更像静帧 hold。
- `DONE WITH NOTES`：`S03-S05` 已拿到可继续留在线上的判断，其中 `S03` 可作为压力链锚点保留，`S04/S05` 的人物稳定和 speaking-ready 也基本成立。
- `IN PROGRESS`：`P04 -> P05` 仍没有真正过门。现有 cut 还带明显“切到新页面”的跳段感，下一步要补 same-space consequence bridge 或重组入口顺序。
- `NEXT`：重新把 `T06` 维持为 active quality lane，优先解决 `S01/S02` 的真 clip 债务，再处理 `P04 -> P05` 的 bridge。

### 2026-04-04 / Round 12

- `DONE WITH NOTES`：主仓 `P04 / S01-S02` 的 current clip 坏链已经就地修成真实二进制文件，不再是指向缺失源视频的软链接占位。
- `DONE WITH NOTES`：这一轮顺手把 `P04` 的 current 口径重新收紧成单点债务：`S01-S05` 继续保留 `KEEP WITH NOTES`，不再把已经可播的 same-space clip 误写成 `REDO REQUIRED`。
- `IN PROGRESS`：`T06` 现在只剩一个真正 blocker：`P04 -> P05` 的 same-space consequence bridge 还没补上，现有 cut 仍有明显“切到新页面”的跳段感。
- `NEXT`：下一步只做两件事：先补 `P04 -> P05` 的 bridge，再做 `S03-S05` 的 trim 和接法优化；不再回头重开已经可用的 `S01/S02`。

### 2026-04-04 / Round 13

- `DONE WITH NOTES`：`T06` 已把 `P04 -> P05` 的 same-space consequence bridge 通过 `chapter-01-p04-p05-consequence-bridge-v1.mp4` 落到 official current。
- `DONE WITH NOTES`：`P05 current` 已同步切到 `part-05-probability-corridor-delivery-v3-d02first.mp4`，`D01` 继续保留为独立资产，但不再作为 current 开门 beat。
- `DONE WITH NOTES`：`official master` 已升级到 `chapter-01-vertical-slice-master-v17-current.mp4`，`story spine` 已升级到 `v15`，预览页应与这套 current 口径保持一致。
- `NEXT`：回到 chapter-level 质量复审，优先继续看 `P06` 的 `READABILITY REOPENED` 和整章 continuity notes；如果没有新 blocker，就保持当前 current 稳定，不再回退 `P04/P05`。

### 2026-04-04 / Round 14

- `DONE WITH NOTES`：`T07` 已把 `P06 / E01` 开头那一拍更亮、更空的走廊 reset 通过 trim recovery 收掉，新的 `part-06 current` 已切到 `part-06-dark-layer-interface-delivery-v6-trimmed-ingress.mp4`。
- `DONE WITH NOTES`：`story spine current` 已升级到 `chapter-01-story-spine-preview-v16.mp4`，`master current` 已升级到 `chapter-01-vertical-slice-master-v18-current.mp4`，这次修复没有停在单条 clip，而是已经传导到 chapter 级入口。
- `DONE WITH NOTES`：`video-loop-state.json`、`asset-manifest.json` 与 `current-part-repair-contracts.md` 已把 active lane 从 `P04` 切到 `P06`，不再拿已经收口的 `P04` 继续冒充当前正在修的主位。
- `DONE WITH NOTES`：顺手把 `asset-manifest.json / video-loop-state.json` 的 part delivery 指针统一按 `current/deliveries` 真实 symlink 回填，修掉了像 `P01` 还停在旧 `v17`、但 current 其实已经是 `v30` 这种状态源滞后。
- `IN PROGRESS`：下一步继续按同一条 production loop 复审 `P05 -> P06 -> P07`。如果还有问题，优先继续走 `trim / bridge / reorder`，不整段重开。

### 2026-04-04 / Round 15

- `IN PROGRESS`：新增 `T08`，把这轮“一个正常大人都听不顺”的对白问题正式落进主整改清单，不再只靠对话口头提醒。
- `DONE WITH NOTES`：已先收掉最容易跳戏的一批词：`新主位`、`底层母样本`、`原样事实`、`只把我当个例子放在那儿` 等，改成更口语、更像人在现场会说的话。
- `IN PROGRESS`：`story / storyboard / voice` 三条文稿链正在继续对齐角色口气。当前先关掉最明显的 AI 腔和文件腔，再继续往下做逐场人物区分复审。
- `NEXT`：把这轮对白修订同步到公开镜像，再继续按 `P05 -> P06 -> P07` 的 production review 看有没有新的 viewer-blocking 问题。

### 2026-04-04 / Round 16

- `DONE WITH NOTES`：新增 `T09`，把 chapter-01 的对外交付入口口径正式收口。当前 source of truth 和资产总览页已经明确区分：
  - `story spine v16` = 当前完整故事入口
  - `vertical slice master v18` = 当前 review master
- `DONE WITH NOTES`：`asset-manifest.json`、`video-loop-state.json`、`version-log.md` 和主资产页已同步写明：不能再把 `vertical slice master` 冒充成完整故事唯一入口。
- `IN PROGRESS`：`T08` 继续保留未闭环状态。当前能确认的是：最新人话化对白已经回写 `master / script / storyboard / voice` 文稿链，但现有 `part delivery` 不会自动吃这些更新，所以还不能宣称“台词都已经完全修进最终成片”。
- `IN PROGRESS`：当前对白传导的主要观察位先盯 `P01 / P09 / P10 / P11`。这些段落最容易让文稿链与成片链重新长出两套口径。
- `NEXT`：继续按 active lane 复审 `P05 -> P06 -> P07`，同时把 `T08` 从文稿层往成片层继续推进；修完一段，就同步写回 source of truth 和公开预览。

### 2026-04-04 / Round 17

- `DONE WITH NOTES`：已按 `T08` 继续逐场复审 `P05 -> P06 -> P07`，重点收掉了几类还像“主题代言词”的句子：
  - `林澄` 不再总用抽象判断句解释自己，而是更直接地说“我真正会的东西被挤成一小条”这类能看见、能感觉到的话。
  - `回响` 继续收成“先说能做什么、再说代价”的口气，不绕、不装聪明。
  - `风声婆婆` 去掉了 `资源模型喜欢的房间`、`发亮的风线`、`不爱排队` 这类不够像真人说话的句子，改成更像她会现场说出来的话。
- `DONE WITH NOTES`：这轮已回写 [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)、[script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)、[storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)、[voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)。
- `IN PROGRESS`：`T08` 仍未闭环。当前只是把 `P05-P07` 的文稿链继续收得更像人话，成片链还没有因为这些文稿变化自动换掉旧台词音轨。
- `NEXT`：继续把 `T08` 从 `P05-P07` 往受影响更大的 `P09 / P10 / P11` 成片传导位推进；同时保持 active lane 仍先盯 `P05 -> P06 -> P07` continuity，不让对白整改和中段 continuity 各跑一套。

### 2026-04-04 / Round 18

- `DONE WITH NOTES`：已把 `T08` 从文稿链继续推到 `P01 / P09 / P10 / P11` 的装配链。当前已重渲：
  - `part-01-future-bay-task-dock-delivery-v30.mp4`
  - `part-09-evidence-freeze-team-split-delivery-v2.mp4`
  - `part-10-free-echo-platform-delivery-v4.mp4`
  - `part-11-midnight-choice-return-delivery-v3.mp4`
- `DONE WITH NOTES`：`story spine v16` 与 `vertical slice master v18-current` 已重新装配，chapter 级 current 入口现在也吃到了这轮 `P01 / P09 / P10 / P11` 的人话化 overlay 传导，不再只停在单条 part 上。
- `DONE WITH NOTES`：已补抓 `P05 -> P06`、`P06 -> P07` 的 transition contact sheet 复审。当前判断：
  - `P05 -> P06`：`PASS WITH NOTES`，`trimmed-ingress` 后已经能读成异常风声把人推入暗层入口。
  - `P06 -> P07`：`PASS WITH NOTES`，仍带一点 stylized handoff，但 wave motif、空间形状和旧训练痕迹还能读成同一条追索继续，不判成 viewer-blocking 跳页。
- `IN PROGRESS`：`T08` 依然不能改成 `DONE`。这轮主要传导的是 overlay / assembly 文案；已有同步音轨的旧对白还没有全部重做，尤其不能误报成“chapter-01 所有成片台词都已经彻底换新”。
- `NEXT`：继续保持 active lane 在 `P06` continuity 观察位，同时把 `T08` 的后续精力转到“哪些剩余段落还是 baked audio 决定口径”，只做真实闭环，不做口头完成。

### 2026-04-04 / Round 19

- `DONE WITH NOTES`：在 `T08` 的逐场复审里，又抓到 `P03 / 悬浮档案大厅` 一处典型 staging 歧义：
  - 林澄那句“你也是来劝我……”单独抽出来时，指向不够清楚
  - 父亲“我不是逼她”容易听成在对空气自言自语
  - 小队成员实际没进画，但旧生产链里还残留过像同场发言的读法
- `DONE WITH NOTES`：已把这处问题同步修到 `master / script / storyboard / voice / shot-list` 五条链：
  - 林澄现在明确是 `看向玩家` 说话
  - 父亲现在明确是 `转向玩家` 解释
  - 闻夏耳麦判断改成更口语的 `他是在卡时间，不让我们把话说完`
  - `shot-list` 也补上“这句必须一听就知道是对谁说”的执行要求
- `IN PROGRESS`：这次修复已经回写 source of truth，但只要还有旧同步音轨没换掉，`T08` 仍继续保持 `IN PROGRESS`，不把文稿修正误报成成片链全部闭环。

### 2026-04-05 / Round 20

- `DONE WITH NOTES`：继续按 `T08 + continuity` 交叉复审时，抓到 `P07 / 沉默练习室` 还有一处 production 输入打架：
  - `storyboard` 的 beat 表把 `S03` 写成了 `林澄极短反应`
  - 但详细分镜又把它写成 `风声婆婆看向你`
  - `shot-list` 实际 current 口径则一直是 `旧录音 / 声像承载体先进入`
- `DONE WITH NOTES`：已把 `script / storyboard / voice` 收回同一口径：
  - `P07/S03` 先是风声婆婆的 `旧录音 / 承载体` 开口，不是假装完整真人现身
  - `script.md` 里的 `她说完，又眯起眼` 已改成 `旧录音停了一拍`，避免主稿继续暗示真人已在场
  - `storyboard-script.md` 已把 `S03` 的演员、类型、画面职责改回和 `shot-list` 一致
- `IN PROGRESS`：`T08` 继续保持未闭环。当前这轮修掉的是 source-of-truth 自己互相打架的问题，还不是重新烤进所有现有视频音轨。

### 2026-04-05 / Round 21

- `DONE WITH NOTES`：继续复审 `P07 -> P08` 时，又抓到一处会误导执行的口径漂移：
  - `shot-list / storyboard` 把 `P08` 设计成 `UI-first + 07 一句短线压实立场`
  - 但 `script.md` 里 07 还在说更长、更抽象的硬规则腔
  - `audio/voice-script.md` 甚至额外长出 `我也曾经有一条没被公开的路` 这类别处没承接的新设定
- `DONE WITH NOTES`：已把 `P08` 收回和 current 执行链一致的版本：
  - 07 在 `P08` 先只说短而硬的一层：`一个孩子的愿望 / 一整座城的分配`
  - 孩子的回应也改得更直：`你们先决定了，哪条路连看都不该看`
  - `audio/voice-script.md` 删掉了未被别的主文件接住的 07 个人往事设定
  - `shot-list.md` 补了一条执行提醒：`P08/S03` 不在这里临时新增 07 的个人往事 lore
- `IN PROGRESS`：`T08` 仍未闭环。这次修掉的是 `P08` 的文稿链漂移，不代表对应成片音轨已经全部换新。

### 2026-04-05 / Round 22

- `DONE WITH NOTES`：继续往 `P09 -> P10` 查时，又抓到一批典型的“文件腔残留”：
  - `shot-list` 里 `P09/S03` 还挂着 `请不要把经过推断的便利，包装成未经加工的事实`
  - `audio/voice-script.md` 和 `episode-onscreen-copy.md` 里还留着 `更容易提交的版本`
  - `audio/voice-script.md` 的 `P10` 仍有多处 `回响整理协议` 作为发言者标签
- `DONE WITH NOTES`：已把这一批统一收回更像人会说的话的版本：
  - 07 的冻结台词统一改成：`后来补上的东西，不能当最早那份证据。`
  - 林澄那句统一改成：`你们是不是也开始想把我改成一个更好交上去的样子？`
  - `P10` 音频里的发言者标签改回 `回响`
  - `episode-onscreen-copy.md` 的相关按钮和提示也同步去掉了过重的 `整理协议` 文件腔
- `DONE WITH NOTES`：这次不只改了文稿，还把 `P09/S03` 的 3 份 `qingyun-vidu` prompt 模板一起同步成新台词，避免后续重生视频时又把旧句子生回来。
- `IN PROGRESS`：`T08` 依然保持未闭环。当前修的是文稿、装配文案和生成提示的一致性，不代表旧成片音轨已经全部重录完。

### 2026-04-05 / Round 23

- `DONE WITH NOTES`：继续扫 `shot-list` 的旧口径残留时，又抓到 `底层母样本` 还留在当前生产链里：
  - `P03` 的 07 台词说明还在写 `底层母样本`
  - `P09` 的权限冻结清单还在写 `底层母样本调取权限`
- `DONE WITH NOTES`：已把这两处一起收回故事内口径：
  - 改成 `更底下那层原始记录`
  - 改成 `更底下最早记录调取权限`
- `IN PROGRESS`：`T08` 继续保持未闭环。当前这步修的是 production 输入残留，避免旧世界外词重新流回 UI、对白或 prompt。

### 2026-04-05 / Round 24

- `DONE WITH NOTES`：继续按 `T08` 收 `P10 / P11` 时，又抓到一串结果层的文件腔还挂在主链上：
  - `资格通过`、`提案`、`公开权申诉`、`观察名单`、`责任记录`
  - 这些词一进高潮和回航，角色就会突然不像人在现场说话，孩子也很难一耳朵听明白
- `DONE WITH NOTES`：已把 `master / script / storyboard / voice / shot-list / episode-onscreen-copy / product-script` 一起收回更像人话的 current 口径：
  - `回响` 统一改成 `按这里的规矩，我不能替任何人点这个头`
  - `P10/P11` 的系统结果改成 `第四路径今晚暂时挂出 / 这不是默认推荐 / 以后再碰这种事你们会被看得更紧`
  - `守望者` 的结尾句收掉了 `有没有资格先看见完整的自己`，统一改成 `能不能先把完整的自己看清`
- `DONE WITH NOTES`：这轮还顺手修掉了一个结构性 continuity 错位：
  - `storyboard-script.md` 的 beat 表里 `P11/S02 = 林澄结尾陈词`、`P11/S03 = 系统结果`
  - 但详细分镜段落一直把林澄那句误写成了 `CH01-P11-S03`
  - 现在已改回 `S02 = 林澄结尾陈词`，并补出真正的 `S03` 结果公告段，避免后续再按错镜号生成
- `IN PROGRESS`：`T08` 仍不改成 `DONE`。当前闭环的是 source-of-truth、UI 文案和执行链口径；已有 baked audio 的旧成片并不会因为文稿改了就自动全部换新。

### 2026-04-05 / Round 25

- `DONE WITH NOTES`：按用户刚指出的两个长期残留 bug，已把 `P01` 从 current clip 链往 chapter 级入口做了一次热修：
  - `S04` 的旧 `别站队 / 先别下结论` baked line 已从 current 退下，改成和最新主稿一致的直白口径
  - `S07` 不再误用工作台错片，也不再把 `S04` 的半句话漏进启航镜头
- `DONE WITH NOTES`：`S07` 当前已改成真正的 `team-launch bridge` 读法：
  - 前半拍先回到固定小队同场画面
  - 后半拍再接航线点亮与出发
  - 至少不再出现“只剩航线、看不出队伍已经一起出发”的 current 误读
- `DONE WITH NOTES`：这次修复已经同步重装：
  - `part-01-future-bay-task-dock-delivery-v31.mp4`
  - `chapter-01-story-spine-preview-v17.mp4`
  - `chapter-01-vertical-slice-master-v19-current.mp4`
- `IN PROGRESS`：`T08` 仍继续保持未闭环。当前修掉的是 `P01` 两个 viewer-blocking bug 和对应装配链，不代表 chapter-01 所有旧同步音轨都已经全部重做完。

### 2026-04-05 / Round 26

- `DONE WITH NOTES`：新增并完成 `T10`。这轮不再只盯对白本身，而是继续核对“分镜脚本 / 趣味增强 / 产品稿 / 上屏文案 / 资产总览页”有没有把候选层误写成 current 已实现。
- `DONE WITH NOTES`：已把 [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)、[storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)、[product-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/product-script.md)、[episode-onscreen-copy.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/episode-onscreen-copy.md) 一起收回同一套边界：
  - 哪些趣味层已经进 current
  - 哪些只保留在后补候选
  - 哪些当前不进主线承诺
- `DONE WITH NOTES`：`shot-list.md` 已去掉指向不存在的 `story/fun-assets.md` 假引用，改回现有主文档入口，避免执行链再被无效来源带偏。
- `DONE WITH NOTES`：资产总览页已扩展成同时展示 `整集总脚本 / 分场剧本 / 分镜脚本 / 产品脚本 / 上屏文案` 五份当前镜像，并在页面上直接写明 current / 后补边界。
- `IN PROGRESS`：`T08` 仍未闭环。这轮修的是文稿链与页面口径，不代表所有 baked audio 都已换完。

### 2026-04-05 / Round 27

- `DONE WITH NOTES`：继续按 `T08 + T10` 交叉复审时，又抓到一批还挂在页面可见层的旧词：
  - `主位`
  - `点头`
  - `扛下`
  - `不予开放`
  - `原始性风险`
- `DONE WITH NOTES`：这轮已把这批词从 [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)、[script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)、[product-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/product-script.md)、[episode-onscreen-copy.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/episode-onscreen-copy.md)、[shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)、[asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json) 和资产总览页一起收掉，统一改成更直接、更像人会说的话。
- `DONE WITH NOTES`：这轮还把资产总览页的“最新组装版”卡片标签从 `文件` 收回成 `入口`，并补齐 `product-script.md / episode-onscreen-copy.md` 的公开镜像，避免页面一边说“读最新主稿”，一边实际缺正文入口。
- `DONE WITH NOTES`：`video-loop-state.json`、`asset-manifest.json` 与 [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md) 已同步记下这轮“页面可见口径继续收口”的状态，不再只改页面不改状态源。
- `DONE WITH NOTES / DOCS ONLY`：回看这轮时，必须明确降级口径：它修掉的是文稿链、页面层和公开镜像层的旧口径，但当时没有新的 `part delivery / story spine / master`，所以不算总装推进。
- `IN PROGRESS`：`T08` 继续保持未闭环。当前还不能因为页面和文稿说顺了，就误报“所有旧同步音轨都已经全部换新”。

### 2026-04-05 / Round 28

- `DONE WITH NOTES`：开始执行 `T11` 的“总装有效性”审计后，先把验收标准收紧成一条硬规则：任何修正如果还没进 `part delivery -> story spine -> master`，一律只算 `DOCS ONLY / NOT COUNTED`。
- `DONE WITH NOTES`：这轮先挑出一个最明确还能直接进总装的 viewer-visible 问题来闭环：
  - `P11` 结果层还挂着明显偏文件腔的可见 overlay
  - 已把它改成更直接的人话，并真实重装成 `part-11-midnight-choice-return-delivery-v4.mp4`
  - 然后继续重装到 `chapter-01-story-spine-preview-v18.mp4`
  - 再继续重装到 `chapter-01-vertical-slice-master-v20-current.mp4`
- `DONE WITH NOTES`：`v1.19 / v1.20` 现在统一改口为 `docs-only truth sync`，不再拿它们冒充“总装又往前推了一轮”。
- `IN PROGRESS`：`T11` 还没闭环。当前只先把 `P11` 一处明确的可见问题推进进总装；其余还停在文稿、页面或公开镜像层的改动，还要继续逐项审、逐项传。

### 2026-04-05 / Round 29

- `DONE WITH NOTES`：继续按 `T11` 往下追时，又抓到 `P10 / 自由回响台` 还留着一层真正会被观众看到的可见问题：
  - `S02` 的整理区标题和提示还带着明显的文件 / UI 腔
  - `S03` 还在说过重的 `高概率 / 低概率` 抽象句，和主稿也没有完全对齐
  - `S04` 的公开陈词虽然方向对了，但措辞还能再收得更直、更像人在现场说话
- `DONE WITH NOTES`：这轮不是只改脚本，而是把修复真推到了总装链里：
  - 重渲 `part-10-free-echo-platform-delivery-v5.mp4`
  - 继续重装 `chapter-01-story-spine-preview-v19.mp4`
  - 再继续重装 `chapter-01-vertical-slice-master-v21-current.mp4`
- `DONE WITH NOTES`：`P10` 现在的 current 口径已经收成更直接的人话：
  - `回响台 / 先把想说的话摆明白`
  - `这条路不是没有。可现在不能先放到大家前面。`
  - `这座城可以先给建议，但不能替还没看清的孩子先把路关掉。`
- `DONE WITH NOTES`：这轮已同步回写状态源和资产总览页，明确它是 `assembly-valid` 进展，不再停在“页面看起来更新了”的层面。
- `IN PROGRESS`：`T11` 仍不改成 `DONE`。当前只是把 `P10` 这处明确的 viewer-visible 问题也推进进了总装；接下来还要继续按主线回到 `P05 -> P06 -> P07` continuity 观察，并继续审其余还停在 `docs-only` 的对白传导债务。

### 2026-04-05 / Round 30

- `DONE WITH NOTES`：继续按主质检流程回到 `P05 -> P06 -> P07` 时，确认当前最该修的不是再开模型，而是把 `P05` 尾部那拍旧的正面定住 pose 收掉。
- `DONE WITH NOTES`：这轮采用的是 `editor-level trim`，不是整段重开：
  - `P05 current` 改成 `D02-first + D04 tail trim`
  - 不再让 `P05` 停在“林澄站住给你看”的旧姿态
  - 让 cut 更像被异常风往下一层拽走，再去接 `P06`
- `DONE WITH NOTES`：这次修复已经真实推进进总装链：
  - `part-05-probability-corridor-delivery-v4-d02first-tailtrim.mp4`
  - `chapter-01-story-spine-preview-v20.mp4`
  - `chapter-01-vertical-slice-master-v22-current.mp4`
- `DONE WITH NOTES`：当前判断继续保持保守：
  - `P05 -> P06` 现在已经不再停在旧的正面定住 pose，上下文读起来更像后果推进
  - `P06 -> P07` 继续维持 `PASS WITH NOTES`
  - 中段 still stylized，但现在不再把它误报成必须马上重开模型的新 blocker
- `IN PROGRESS`：`T08 / T11` 仍未闭环。这轮修掉的是一处真实进总装的 continuity 问题，不代表所有旧同步音轨对白都已经全部换新。

### 2026-04-05 / Round 31

- `DONE WITH NOTES`：继续按 `T11` 审“哪些页面可见修正还没真的进总装”时，抓到 `P09` 的冻结提示虽然文稿链已经改顺，但 `part current` 里那层字还像回执单，不够像人会当场说出来的话。
- `DONE WITH NOTES`：这轮没有重开整段，而是直接把 `P09` current 收成更清楚的人话版：
  - `part-09-evidence-freeze-team-split-delivery-v3-overlaycleanup.mp4`
  - `回响台提醒：这些先别当最早那份`
  - `后来补上的这些，今晚先不能拿去当前排法。`
  - `你们还能继续去回响台开口。`
  - `可你们手里现在能用的证据，已经比刚才少了。`
- `DONE WITH NOTES`：这次真正进总装的是：
  - `part-09-evidence-freeze-team-split-delivery-v3-overlaycleanup.mp4`
  - `chapter-01-story-spine-preview-v21.mp4`
- `DONE WITH NOTES`：`review master` 当前已刷新到 `chapter-01-vertical-slice-master-v23-current.mp4`，但这里明确写清边界：
  - 它本身仍是 vertical-slice subset
  - 它不含 `P09`
  - 所以这次 `P09` 是否真的修顺，应该以 `story spine v21` 为准，不再误报成“也已经进了 review subset”
- `IN PROGRESS`：`T08 / T11` 仍未闭环。这轮闭环的是 `P09` 一处真实 viewer-visible 的装配文案问题；其余还被旧同步音轨卡住的对白位，仍要继续按 `part -> full-story current` 的顺序往下传。

### 2026-04-05 / Round 32

- `DONE WITH NOTES / DOCS ONLY`：继续按 `T08` 往下扫时，又抓到一组你已经明确不要的口气残留还挂在主文稿和上屏文案里：
  - `点头`
  - `先排先后`
  - `第四路径今晚会先挂出去`
- `DONE WITH NOTES / DOCS ONLY`：已把这组句子从 `master-episode-script.md`、`audio/voice-script.md`、`episode-onscreen-copy.md` 一起收回更口语的版本：
  - `你要是肯让我补……`
  - `档案城可以先顾大多数，但不能把少数孩子的路直接藏起来。`
  - `第四路径今晚会先亮出来。`
  - `再来叫我服气。`
- `DONE WITH NOTES / DOCS ONLY`：这轮只算 source-of-truth 和页面正文清理，不算总装推进；以后如果这几句真的进了新的 part / full-story current，再另记成 assembly-valid 进展。

### 2026-04-05 / Round 33

- `DONE WITH NOTES / DOCS ONLY`：继续扫资产总览页会直接读到的正文镜像时，又抓到一整层还偏“项目术语”的词还挂在 `storyboard / product / onscreen / voice` 里：
  - `最优路径`
  - `失败率预测模型`
  - `公开申请`
  - `观察期申请`
- `DONE WITH NOTES / DOCS ONLY`：已把这层说法收回更像时间档案城里的人会说的话：
  - `为什么总有一条路被先推到前面`
  - `这座城怎么分力气`
  - `哪种走法更容易摔跟头`
  - `请把第四路径亮给更多人看`
  - `先把第四路径留下来继续看`
- `DONE WITH NOTES / DOCS ONLY`：这轮仍只算 page-visible docs 清理，不算总装推进；但它会直接改善资产总览页里展开正文时的阅读体验，不再一边说“已经去文件腔”，一边还把旧词挂给人看。

### 2026-04-05 / Round 34

- `DONE WITH NOTES`：继续按 active lane 复审 `P06 -> P07` 时，没有直接重开模型，而是先做了低成本 editor 测试：
  - `1 秒` 头切几乎没改善
  - 但 `3.2 秒` 头切后，`P06` 末尾的桌面波形可以更直接接到 `P07` 的旧档案桌面
- `DONE WITH NOTES`：这轮把这刀 trim 真正推进进了完整故事 current：
  - `part-07-silent-practice-room-delivery-v3-headtrim.mp4`
  - `chapter-01-story-spine-preview-v22.mp4`
- `DONE WITH NOTES`：这次明确只影响完整故事入口，不误报 review subset：
  - `story spine current` 已升级到 `v22`
  - `review master` 继续保持 `v23-current`
  - `master` 这轮不变，因为它本来就不含 `P07`
- `IN PROGRESS`：`T08 / T11` 仍未闭环。这轮闭环的是 `P06 -> P07` 一处真实 continuity trim，不代表剩余旧同步音轨对白都已经换新。

### 2026-04-05 / Round 35

- `DONE WITH NOTES`：继续按 active lane 补抓 `P05 tail -> P06 head` 和 `P06 tail -> P07 head` 的 contact-sheet 复审。当前判断：
  - `P05 -> P06`：仍带一点从人物反应切到第一人称暗层入口的 stylized handoff，但旧版那种“先亮一下、再像新页面重开”的问题已经没有重新出现。
  - `P06 -> P07`：`P07 v3 head trim` 继续成立，桌面波形和旧档案桌面的接法目前仍能读成同一条追索后果。
- `DONE WITH NOTES / DOCS ONLY`：这轮没有新增 assembly 变更，只是把“当前没有新的 viewer-blocking 问题、先不再追加 trim / bridge”这条判断写回 source of truth，避免下一轮接手又从旧 blocker 重新猜起。
- `IN PROGRESS`：`T08` 仍未闭环。当前开始补探可复用的自动转写检查路，但本机没有现成 Whisper；Gemini 探针也还没拿到稳定返回，所以暂时还不能把“哪些旧音轨仍卡着口径”自动批量捞出来。

### 2026-04-05 / Round 36

- `DONE WITH NOTES / DOCS ONLY`：已在仓库外用 `/tmp/ch01-audio-qc-venv + faster-whisper` 打通本地 rough audio audit 路，不再只靠主观听感猜“哪条旧同步音轨还没跟上当前文稿”。
- `DONE WITH NOTES / DOCS ONLY`：这轮粗转写先收出一条更可执行的结论：
  - `P05` 当前只听到一记很短的“等等，这风声”，先记可疑但不单独判 blocker。
  - `P06` 当前没抓到可辨识对白。
  - `P07 / P11` 当前音轨大体还算顺，先不重开。
  - `P09 / P10` 仍能听到旧 baked-audio 口径，已经成为 `T08` 眼下最明确的声音债务。

- `DONE WITH NOTES / DOCS ONLY`：顺着这条检查，又抓到 `P10 / S03` 的所有正式重生模板还残留旧句 `如果高概率已经证明答案，你凭什么让城市承担低概率代价？`。这轮已把它统一改回和 current 一致的短线：`这条路不是没有。可现在不能先放到大家前面。`
- `IN PROGRESS`：`T08 / T11` 仍未闭环。这轮只完成了“找准旧音轨债务 + 清掉上游再生源头”，还没有新增 `part delivery / story spine / master`，所以必须继续记成 `DOCS ONLY / NOT COUNTED`。

### 2026-04-05 / Round 37

- `DONE WITH NOTES`：已把 `P09 / S03` 和 `P10 / S03` 的 speaking clip 真正重生进 current 短线，不再只停在模板清理：
  - `shot-ch01-p09-s03-evidence-freeze-intervention-viduq3-s2v-v3.mp4`
  - `shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.mp4`
- `DONE WITH NOTES`：已用仓库外 `/tmp/ch01-audio-qc-venv + faster-whisper` 复核 source clip 与 part-level current：
  - `P09 / S03` 现在能读到：`后来补上的东西 / 不能当最早那份证据`
  - `P10 / S03` 现在能读到 current 短线骨架：`这条路不是没有 / 可现在不能先放到大家前面`
- `DONE WITH NOTES`：已把这轮真实音轨修复继续传到总装链，而不是停在 source clip：
  - 重渲 `part-09-evidence-freeze-team-split-delivery-v3-overlaycleanup.mp4`
  - 重渲 `part-10-free-echo-platform-delivery-v5.mp4`
  - 重装 `chapter-01-story-spine-preview-v23.mp4`
  - 重装 `chapter-01-vertical-slice-master-v24-current.mp4`
  - `chapter-01-story-spine-preview-current.mp4` 与 `chapter-01-master-current.mp4` 已同步切到新版本
- `DONE WITH NOTES`：`T08` 这轮终于不再只是 `DOCS ONLY`。之前最明确的 `P09 / P10 baked-audio` 债务，已经真修进 `source clip -> part -> story spine -> master`。
- `IN PROGRESS`：`T11` 继续保持未闭环。当前只是把最明确的一组“页面和文稿先变了、成片却还没跟上”的债务关掉；后续仍要继续按同一套规则审 active lane 和新发现的问题，不能因为这一轮成了就把整章误报成“全部完成”。

### 2026-04-05 / Round 38

- `DONE WITH NOTES / DOCS ONLY`：继续按 `T11` 复核 `P05 -> P06 -> P07` 时，用 current 粗转写抽到了 `P07` 的真实口径：当前成片里，风声婆婆先落一句 `你听不见，不一定是因为它不存在`，后面还会补一句 `也可能是你前面太吵了`。
- `DONE WITH NOTES / DOCS ONLY`：顺着这条抽检，反查出 source-of-truth 仍有一组 `P07` 自己打架的残留：
  - `storyboard-script.md` 的详细段落还把 `S03` 写成双句旧版
  - `shot-list.md` 的 `E07` 细节也还留着双句合并写法
  - `audio/voice-script.md` 的 `Scene 07` 还停在更长的旧独白，没有明确写清 current 正片先只保哪两句
- `DONE WITH NOTES / DOCS ONLY`：这轮已把 `script / storyboard / voice / shot-list` 收回同一套 current 口径：
  - `P07/S03` 先只落第一句短线
  - `P07/S04` 再补第二句短线，并把后半段继续留给风名标签、短风声和林澄反应
- `IN PROGRESS`：这次没有新增 `part / story spine / master` 重装，所以不能把它误报成新的总装推进；它的价值在于关掉了一组会误导后续生产、也会让页面和成片口径重新长歪的 source-of-truth 漂移。

### 2026-04-05 / Round 39

- `DONE WITH NOTES`：继续按 `T11` 回到 `P06` 时，确认这里不该再只做 docs-only 降级，而是要把真正卡住的断点补进成片链：
  - `P06 / E03` 文稿里一直承诺有系统确认
  - `P06 / E04` 文稿里一直承诺有婆婆旧录音短线
  - 但旧 current part 还是 atmosphere-only，形成了“文稿有声、成片无声”的真实断点
- `DONE WITH NOTES`：这轮已把这个断点真实补进总装，而不是只改说明文字：
  - 重写 [render_chapter01_part6_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part6_delivery.sh)
  - 重渲 [part-06-dark-layer-interface-delivery-v7-voiceclosure.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-06-dark-layer-interface-delivery-v7-voiceclosure.mp4)
  - 继续重装 [chapter-01-story-spine-preview-v24.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v24.mp4)
  - 再继续重装 [chapter-01-vertical-slice-master-v25-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v25-current.mp4)
- `DONE WITH NOTES`：这次补的不只是离屏声音，还额外加了轻量 viewer-visible 锚点：
  - `E03` 现在会把 `隐藏路径已恢复 / 风暴听译者` 轻轻挂出来
  - `E04` 现在会把 `风声婆婆旧录音：别只听最大声的那条。` 轻轻挂出来
  - 这样就算孩子没一下子全听清，也不会错过关键意思
- `DONE WITH NOTES`：仓库外 rough STT 这轮给出的结论也一起回写清楚了：
  - 它能确认 `P06` 现在已经不是纯静音氛围位，而是有新的人声层
  - 但它对本地 macOS 中文 TTS 的逐字识别不稳定，所以这轮不把机器逐字稿当唯一验收
  - 当前这类短线，先以真实装配链闭环和可见锚点同步为准
- `IN PROGRESS`：`T11` 仍不改成 `DONE`。这轮闭环的是 `P06 / E03-E04` 的真实音画断点，不代表 `P05 -> P06 -> P07` 的 continuity 长观察已经结束。

### 2026-04-05 / Round 40

- `DONE WITH NOTES`：继续按 `T11` 往下收时，没有把这轮停在“`P06` 已经有声了”这一层，而是继续把它收成更清楚、更像孩子一遍能听懂的 current 版本：
  - `E03` 当前短线收成：`第四条路回来了。这条路叫风暴听译者。`
  - `E04` 当前短线收成：`别只听最大声那条。`
- `DONE WITH NOTES`：这轮真实重装的不只是 source clip，而是整条 current 链：
  - 重渲 [part-06-dark-layer-interface-delivery-v8-voiceclarity.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-06-dark-layer-interface-delivery-v8-voiceclarity.mp4)
  - 继续重装 [chapter-01-story-spine-preview-v25.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v25.mp4)
  - 再继续重装 [chapter-01-vertical-slice-master-v26-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v26-current.mp4)
- `DONE WITH NOTES`：顺着这条热修，又抓到一组 source-of-truth 自己打架的残留，并一起清掉了：
  - `storyboard-script.md` 的 `P06/S04` 详细段落还留着旧句 `别只听最大声的那条`
  - `shot-list.md` 的 `P06/E03-E04` 执行表和详细说明里，还并存着旧句和新句
  - 这轮已把 `storyboard / shot-list / voice` 三条链统一成 current 口径，避免后续再把旧句生回来
- `DONE WITH NOTES`：仓库外 rough STT 这轮抽检结果，比上一版更能抓住 `P06` 的关键句骨架：
  - `P06`：`第四條路回來了,這條路叫風暴停`
  - `P06`：`別之聽最大聲納條`
  - `P07`：`你聽不見,不一定是因為他不存在 / 也可能是因為你前面太吵了`
  - 它逐字仍不完美，但已经足够说明 `P06` 这两句 current 更容易被机器和人一起接住
- `IN PROGRESS`：`T11` 仍不改成 `DONE`。这轮闭环的是 `P06` 的清晰度热修和 source-of-truth 同步，不代表 `P05 -> P06 -> P07` 的 continuity 长观察已经结束。

### 2026-04-05 / Round 41

- `DONE WITH NOTES`：继续按 active lane 复审 `P05 -> P06` 的 contact-sheet 后，又抓到一个真正还会掉气的 viewer-visible 问题：
  - `P05` 尾部虽然已经不再停在旧的正面定住 pose
  - 但还多留了半拍“人又重新站稳”的感觉
  - 这会让 `P05 -> P06` 比应该有的样子更像先收住一下，再切新页面
- `DONE WITH NOTES`：这轮仍然没有重开模型，而是继续走更省、更准的 `editor-level trim`：
  - `part-05 current` 继续收成 `part-05-probability-corridor-delivery-v5-d02first-tailtrim2.mp4`
  - `D04` 时长从 `2.400000s` 收到 `2.166667s`
  - 音频尾 fade 也一起前收，避免那半拍重新站稳又被听感托长
- `DONE WITH NOTES`：这次修复已经继续推进进总装链，不是只停在局部 clip：
  - `chapter-01-story-spine-preview-v26.mp4`
  - `chapter-01-vertical-slice-master-v27-current.mp4`
  - `part-05-current / chapter-01-story-spine-preview-current / chapter-01-master-current` 已同步切到新版本
- `DONE WITH NOTES`：这轮 source-of-truth 也一起落账，不再让页面口径慢半拍：
  - `video-loop-state.json`
  - `asset-manifest.json`
  - `current-part-repair-contracts.md`
  - `version-log.md`
  - 资产总览页与公开镜像应继续保持这套 `v26 / v27-current` 口径
- `IN PROGRESS`：`T11` 仍不改成 `DONE`。当前只是把 `P05 -> P06` 的 continuity 再收紧一刀；下一步还要继续按同一条主质检流程观察 `P05 v5 tailtrim2 + P06 v8 voiceclarity + P07 v3 head trim` 这条链有没有新的 trim / bridge 需求。

### 2026-04-05 / Round 42

- `DONE WITH NOTES / DOCS ONLY`：这轮没有再盲目开修，而是先按 `T11` 的真实闭环标准做了一次针对性抽检：
  - 重新看了 `P05 v5 -> P06 v8` 和 `P06 v8 -> P07 v3` 的 transition strip
  - 当前没有抓到新的 viewer-blocking 跳页
  - 所以 active lane 继续保持 `PASS WITH NOTES`，不因为“总得再改点什么”就硬做无效 trim
- `DONE WITH NOTES / DOCS ONLY`：顺着用户前面点名的“文稿链往成片链传导”继续做 rough STT 抽检：
  - `P09` 当前仍能抓到：`后来补上的东西，不能当最早那份证据`
  - `P10` 当前仍能抓到：`这条路不是没有。可现在不能先放到大家前面`
  - `P11` 当前仍保留“我不想还没看见，就先被删掉”这层核心意思
  - 这三段目前没有重新掉回旧 baked-audio 口径
- `DONE WITH NOTES / DOCS ONLY`：`P01` 这轮单独做了更窄的复核，因为全段 rough STT 曾误抓到 `见习建造者`：
  - 在更短的 `S05` 片段里，没有再次抓到这个旧词
  - 当前更像是粗转写把 `灰银任务` 听岔成了别的词
  - 在没有更强证据前，先不把 `P01` 误判成 reopened blocker
- `IN PROGRESS`：`T11` 继续保持未闭环。当前这轮的结论是“`P01 / P09 / P10 / P11` 暂时没有新增 reopen blocker”，不是“这些段落以后都不用再看”。

### 2026-04-05 / Round 43

- `DONE WITH NOTES`：按 `T11` 继续查 viewer-visible 问题时，又抓到一个必须就地修的真 bug：
  - `P09 / E13` 的源 clip 里还露着英文伪 UI
  - 第一眼会先看到 `Evidence Permission Panel...` 这类旧字样
  - 这已经和当前中文 world-in 口径直接打架
- `DONE WITH NOTES`：这轮没有误把它推回模型重开，而是直接做 assembly-level localized overlay recovery：
  - 更新 [render_chapter01_part9_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part9_delivery.sh)
  - 重渲 [part-09-evidence-freeze-team-split-delivery-v4-localized-ui.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-09-evidence-freeze-team-split-delivery-v4-localized-ui.mp4)
  - `E13` 现在会先被中文世界内卡片接住，不再让英文伪 UI 抢第一眼
- `DONE WITH NOTES`：这次修复已经继续传导到完整故事入口，不只停在 part：
  - `part-09 current`
  - [chapter-01-story-spine-preview-v27.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v27.mp4)
  - 公开预览 current 镜像也已同步切到新的 full-story current
- `DONE WITH NOTES`：这轮没有动 `review master`，并且要明确写死原因：
  - [chapter-01-vertical-slice-master-v27-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v27-current.mp4) 本来就不含 `P09`
  - 所以这次 `P09` 是否收顺，应该以 `story spine v27` 为准，不再误报成“master 也已更新”
- `DONE WITH NOTES`：source-of-truth 和页面口径已同步回写：
  - [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
  - [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
  - [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)
  - 资产总览页与公开镜像
- `IN PROGRESS`：`T11` 仍不改成 `DONE`。这轮闭环的是一个真实 viewer-visible 的 `P09` 画面 bug；active lane 仍回到 `P05 -> P06 -> P07` continuity 主线继续观察。

### 2026-04-05 / Round 44

- `DONE WITH NOTES / DOCS ONLY`：继续按 active lane 复查 `P05 -> P06 -> P07` 的生产复现链时，又抓到一个流程质量缺口：
  - `video-loop-state.json` 里把 `P07` 的 accepted delivery 指到 `scripts/production/render_chapter01_part7_delivery.sh`
  - 但仓库里这个脚本其实不存在
  - 也就是说这段 current 虽然能看，但复现链是断的
- `DONE WITH NOTES / DOCS ONLY`：这轮先不误报成新的总装推进，而是把复现链补齐：
  - 新增 [render_chapter01_part7_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part7_delivery.sh)
  - 逻辑明确写死：从 `part-07-silent-practice-room-delivery-v2.mp4` 做 `3.2s` 头切，输出 `part-07-silent-practice-room-delivery-v3-headtrim.mp4`
  - 这一步修的是 workflow reproducibility，不是新模型生成
- `DONE WITH NOTES / DOCS ONLY`：已经做过临时复现验证，不是只写脚本不验：
  - 临时复现输出时长 `9.989002s`
  - 与当前正式 `part-07 v3 headtrim` 一致
  - 临时复现版和正式版做逐帧 PSNR 对比，平均值约 `47.24dB`，说明当前脚本已经足够贴近现有 accepted delivery
- `DONE WITH NOTES / DOCS ONLY`：顺手把 `P07 v3` 的正式 metadata 也补齐了 `script` 字段，避免以后再出现“状态源写着有脚本、metadata 却追不到脚本”的断链。
- `DONE WITH NOTES / DOCS ONLY`：这轮又补做了一次 active lane 的低成本节奏复查：
  - `P06` 尾部和 `P07` 头部都能测到较长安静段
  - 但继续做帧相似度抽查后，暂时还不足以证明它们是在重复停同一股桌面信息
  - 所以这轮先不误开新的 `trim / reorder`，active lane 继续维持 `PASS WITH NOTES`
- `IN PROGRESS`：`T11` 仍不改成 `DONE`。这轮闭环的是 active lane 上一个流程复现缺口，不是新的 `part -> story spine -> master` 画面推进；下一步继续回到 `P05 -> P06 -> P07` 的 viewer-visible continuity 复审。

### 2026-04-05 / Round 45

- `DONE WITH NOTES`：继续按 active lane 复审 `P06 -> P07` 的 viewer-visible continuity 时，确认上一轮刚补齐复现链的 `P07 v3 head trim` 其实裁过了：
  - 开场几乎立刻就落到旧档案桌面
  - `S01` 原本该有的沉默练习室暖房间入口被吃掉太多
  - 这会让 `P06 -> P07` 更像“又切到另一张桌面信息页”，而不是顺着第四路径走进旧练习室
- `DONE WITH NOTES`：这轮没有误开模型重生，而是继续走更省、更准的 assembly-level trim recovery：
  - 更新 [render_chapter01_part7_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part7_delivery.sh)
  - 把头切从 `3.2s` 改成 `2.4s`
  - 正式重渲 [part-07-silent-practice-room-delivery-v4-warm-ingress.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-07-silent-practice-room-delivery-v4-warm-ingress.mp4)
  - 让 `P07` 先保留一小段暖房间入口，再落到旧档案桌面
- `DONE WITH NOTES`：这次修复已经真实推进进当前完整故事入口，不是只停在单条 part：
  - `part-07 current` 已切到 `v4 warm-ingress`
  - 完整故事入口已升级到 [chapter-01-story-spine-preview-v28.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v28.mp4)
  - 公开预览 current 镜像也应同步切到新的 full-story current
- `DONE WITH NOTES`：这轮要明确写死一个边界，避免再误报：
  - `review master` 继续保持 [chapter-01-vertical-slice-master-v27-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v27-current.mp4)
  - 原因不是漏同步，而是它本来就不含 `P07`
  - 所以这轮闭环的是 `part -> story spine -> preview current`，不是 `master` 更新
- `DONE WITH NOTES`：source-of-truth 和页面口径已同步回写：
  - [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
  - [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
  - [current-part-repair-contracts.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/current-part-repair-contracts.md)
  - [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)
  - 资产总览页与公开镜像
- `IN PROGRESS`：`T11` 仍不改成 `DONE`。这轮闭环的是一个真实进了总装链的 `P07` continuity 修复；active lane 还是回到 `P05 -> P06 -> P07` 主线继续观察，不误报成“全章收完”。

### 2026-04-05 / Round 46

- `DONE WITH NOTES / DOCS ONLY`：继续按 `T11` 审当前工作链时，先把一个差点被误判成 source-of-truth 缺失的问题查清了：
  - `P08` 的 `delivery script / metadata / current clips / current shots` 在主仓 `HEAD` 里其实都在
  - 问题出在当前临时 `sparse worktree` 没把这批文件 hydrate 出来
  - 所以这不是“仓库没资产”，而是“本地工作树漏检文件”
- `DONE WITH NOTES / DOCS ONLY`：已把 [render_chapter01_part8_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part8_delivery.sh) 补成可安全旁路验证的版本：
  - 新增 `TMP_DIR_OVERRIDE`
  - 新增 `FINAL_VIDEO_OVERRIDE`
  - 新增 `FINAL_META_OVERRIDE`
  - 后续再做 `P08` 可复现性验证时，不会再误写正式 `part-08 current`
- `DONE WITH NOTES / DOCS ONLY`：已完成一次 `P08` 重放验证结论收口：
  - 当前 accepted delivery 仍能从 `E09 + E10 + E11 + E12` 这条链重装
  - 抽样关键帧校验一致，说明视觉装配链可重放
  - 整文件 MD5 不同，当前判断主要来自脚本里的合成底噪床每次会重新生成，因此这一步只算 `structurally reproducible`，不算 `byte-identical`
  - 这轮不新增 `part / story spine / master`
  - 因此只能记为 `process-valid reproducibility check`，不算总装推进
- `IN PROGRESS`：`T11` 继续保持未闭环。当前先关掉的是“本地工作树漏检 -> 误判仓库缺资产”这类流程噪音；下一步仍先回到 active lane 的 `P05 -> P06 -> P07` continuity 观察，再补看 `P07 -> P08 / P09 -> P10` 的 viewer-visible handoff，不把 process fix 冒充成内容修复。

### 2026-04-05 / Round 47

- `DONE WITH NOTES`：继续按 `T11` 的 viewer-visible continuity 复审往下看时，这轮终于抓到一处值得真进总装、而且能用剪辑解决的问题：
  - `P07 -> P08` 的问题不在“规则投影室不该存在”
  - 而在 `P08 / E09` 的空白规则厅建立略久，容易把 `P07` 的暖房间余波读成“切了一个新模块”
- `DONE WITH NOTES`：这轮先做了两个 editor-level 试片：
  - `0.6s` 头切几乎没改善
  - `1.0s` 头切能明显把空白建立收短，同时还保留足够的规则厅建立位
- `DONE WITH NOTES`：因此这轮正式采用 `1.0s` 的 `TRIM_HEAD` recovery，而不是重开模型：
  - 新增 [part-08-rule-projection-room-delivery-v2-headtrim.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-08-rule-projection-room-delivery-v2-headtrim.mp4)
  - 对应 metadata：
    [part-08-rule-projection-room-delivery-v2-headtrim.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-08-rule-projection-room-delivery-v2-headtrim.metadata.json)
  - [render_chapter01_part8_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part8_delivery.sh) 也已切到 current recovery 口径
- `DONE WITH NOTES`：这次修复已经真实推进进完整故事入口：
  - `part-08 current` 已切到 `v2 headtrim`
  - 完整故事入口已升级到 [chapter-01-story-spine-preview-v29.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v29.mp4)
  - `review master` 继续不变，因为它本来就不含 `P08`
- `DONE WITH NOTES`：同一轮也顺手把 `P09 -> P10` 再复审了一遍：
  - 当前更像必要的公共空间建立，而不是同类“空白建立过长”
  - `P10 / F01` 仍在 `3-4s` 的 shot contract 范围内
  - 所以这轮不为了“想再顺一点”去硬动 `P10`
- `IN PROGRESS`：`T11` 继续保持未闭环。当前只是又关掉了一处真实进了 `part -> story spine -> preview current` 的 continuity bug；active lane 仍回到 `P05 -> P06 -> P07` 主线继续观察。

## 6. 进度标记规则

- `TODO`：还没开始
- `IN PROGRESS`：已开始改主文件，但还没闭环
- `DONE`：主文件已回写，且本清单已同步
- `DONE WITH NOTES`：已回写，但仍有后续观察项
- `BLOCKED`：被上游条件卡住

## 7. 下一步顺序

1. 继续观察 `P05 v5 tailtrim2 + P06 v8 voiceclarity + P07 v4 warm ingress` 这组 continuity recovery 是否已经足够稳，必要时只做更细的 `trim / bridge / reorder`
2. 保持复审 `P05 -> P06 -> P07` 的中段 continuity，但当前先按 `PASS WITH NOTES` 口径继续推进，不把 stylized handoff 误判成新 blocker
3. `T11` 的下一步继续盘点还有哪些 viewer-visible 修正仍停在 `docs / page / mirror` 层，按 `part -> story spine -> master` 的顺序逐项传导；`P06`、`P09 / P10` 这几组已从“静音 / 旧音轨”开放债务里出队
4. 继续使用这条已打通的本地 rough STT 路，做后续 speaking shot 的低成本抽检；但像本地中文 TTS 这种短线，不再把机器逐字稿当唯一验收
5. 把新的 current judgement 持续同步到 `video-loop-state.json`、`asset-manifest.json`、预览页镜像与 GitHub Pages；当前完整故事入口口径应保持 `story spine v29`
