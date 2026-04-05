# Current Part Repair Contracts

## 1. 文档用途

这份文档只做一件事：承接 chapter-01 当前 `active lane` 的修复合同。

它不替代：

- `video-loop-state.json` 的总控状态
- `shot-list.md` 的全片 production 结构
- `flow-vertical-slice-pack.md` 的阶段记录

它只负责把“当前正在修哪一段、为什么修、怎么判通过、什么情况直接算失败”写清楚。

以后 active lane 变了，就直接更新这份文档，不再把修复条件散落写在页面、对话和零碎备注里。

## 2. 当前 active lane

- `part_id`：`P06`
- `part_name`：`暗层接口`
- `当前状态`：`DONE WITH NOTES`
- `当前判断`：`PASS WITH NOTES / E01 TRIMMED INGRESS + E03_E04_VOICE_CLARITY_LANDED + P05 TAIL TRIM REFINED + P07 HEAD TRIM LANDED`
- `对应总控`：
  - [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
  - [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
  - [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)

## 3. P06 修复目标

把这条中段承接继续收口成同一条后果链：`P05` 结尾不再停在旧的正面定住 pose，而是停在异常风把林澄往下一层带走的听风位；`P06` 入口继续保持暗层入口状态。

这段现在最重要的，不是多炫，而是下面 4 件事必须同时成立：

1. `P05` 结尾不再停在旧的正面定住 pose，观众会更像顺着异常风继续往下走。
2. `P05` 结尾的异常风声一出来，观众就会顺着它进暗层，而不是先被一条更亮的空走廊打断。
3. `E01` 第一秒就要让人知道，我们已经走进更暗、更贴近暗层的入口状态了。
4. `E02-E04` 还得继续讲顺：`对波形 -> 找门 -> 录风声`，不能因为 trim 了开头，或因为这一轮补了声音，后面反而变乱。
5. `P06 -> P07` 还要像后果推进，而不是“暗层刚看明白，又切到一个新页面”。

换句话说，`P06` 必须把下面这条线讲顺：

`P05 风异常 -> 暗层入口 -> 波形解读 -> 第四路径显现 -> 风声记录 -> P07 旧训练痕迹`

## 4. 这一轮必须回答的问题

1. `P05` 结尾是否已经不再停在旧的正面定住 pose？
2. `E01` 开头是否已经不再先闪回更亮、更空的走廊？
3. trim 之后，`E01` 是否更像直接被风声带进暗层，而不是更跳？
4. `E02-E04` 的读法是否仍然清楚，没有因为入口被裁而断气？
5. `P06 -> P07` 是否还像追索继续推进，而不是新的页面切换？

## 5. 镜头级修复账

| Shot | 当前类型 | 当前判断 | 本轮职责 | 通过标准 | 失败信号 |
| --- | --- | --- | --- | --- | --- |
| `CH01-P06-S01` | `dark_layer_ingress` | `TRIM_APPLIED_WITH_NOTES` | 去掉开头那一拍更亮、更空的走廊 reset，让 `P05` 的风异常直接把人推入暗层 | 第一秒就进入更暗的入口状态，而且 current 源里已经换成 trimmed clip | 如果开头仍先亮一下，或 trim 后更跳，就直接算失败 |
| `CH01-P06-S02` | `waveform_puzzle` | `KEEP_WITH_NOTES` | 把“要先听懂风声”这层动作讲清 | 观众能看懂这是追线索，不是随手切一个特效面板 | 如果 trim 完入口后，这镜突然像另起一段，就要重新复审 |
| `CH01-P06-S03` | `hidden_path_reveal` | `KEEP_WITH_NOTES` | 把第四路径显现这件事立住，继续承担中段核心 reveal | 观众能把它看成前一拍追索的结果 | 如果它看起来像突然公布新答案，就不算过门 |
| `CH01-P06-S04` | `wind_listener_interface` | `KEEP_WITH_NOTES` | 把“记录风声”这件事落地，并把后果继续送向 `P07` | 观众能明白这是继续追索，不是结算结束 | 如果到这里又像切出一页新模块，就要回退复审 |

## 6. 当前通过条件

只要下面 4 条同时成立，`P06` 才能从这轮修复里过门：

1. `P05` 结尾不再停在旧的正面定住 pose。
2. `P05` 尾部异常风声之后，不再先看到一条更亮的空走廊 reset。
3. `E01` 第一秒就能把人带进暗层入口。
4. `E02-E04` 仍保持 `对波形 -> 找门 -> 录风声` 的单线追索关系。
5. `P06 -> P07` 继续像后果推进，而不是断页。

## 7. 当前失败条件

只要出现下面任一条，就不算通过：

1. `P05` 结尾仍停在旧的正面定住 pose。
2. `P06` 开头仍然先亮一下，再慢慢变暗。
3. trim 之后，镜头头部虽然更短了，但跳切感更重。
4. `E02-E04` 因为入口被裁而变得更难懂。
5. `P06 -> P07` 又重新看起来像换页面。
6. 修完以后虽然更暗了，但故事线反而更难跟。

## 8. 当前 recovery path 与复审结论

- `E01`：`TRIM APPLIED WITH NOTES`
  - `p06-s01-dark-layer-ingress-current.mp4` 已切到 trimmed ingress 版，不再先回到更亮、更空的走廊。
  - 这次修的是 `assembly/editor-level trim recovery`，不是整段重开模型。
- `E02`：`KEEP WITH NOTES`
  - 波形解读职责仍成立，当前不因为入口 trim 回退。
- `E03`：`KEEP WITH NOTES`
  - 第四路径 reveal 仍是这段中间最重要的锚点；这轮已把系统短线收成“第四条路回来了。这条路叫风暴听译者。”，并配好轻字幕锚点，不再只是静音氛围位。
- `E04`：`KEEP WITH NOTES`
  - 风声婆婆录音接口仍承担“把追索继续推进出去”的职责；这轮已把旧录音短线收成“别只听最大声那条。”，并配上轻字幕锚点，当前先观察它和 `P07` 的接法。
- `P05 -> P06`：`P05 TAIL TRIM REFINED + VOICECLARITY APPLIED`
  - 当前 `part-05 current` 已同步切到 `part-05-probability-corridor-delivery-v5-d02first-tailtrim2.mp4`。
  - 当前 `part-06 current` 已同步切到 `part-06-dark-layer-interface-delivery-v8-voiceclarity.mp4`。
  - `story spine current` 已同步切到 `chapter-01-story-spine-preview-v26.mp4`。
  - `master current` 已同步切到 `chapter-01-vertical-slice-master-v27-current.mp4`。
  - 这次通过的是“把旧的正面定住 pose、亮走廊 reset，以及 `E03/E04` 的静音断点一起收掉”，并继续把两句短线收成更清楚的人话；本地 rough STT 也已经能更稳定抓到 `第四条路回来了` 和 `别只听最大声那条` 的骨架。
  - 这轮又继续把 `P05` 尾部多留的半拍“重新站稳”泄气感收掉，让 cut 更停在被异常风带偏、还没回稳的点。
  - 后续又继续用 `P07 v3 head trim` 把 `P06` 的桌面波形更直接接进 `P07` 的旧档案桌面。
  - 这不是宣称这段以后永远不用再升级，只是当前 same-space handoff 又往前收了一刀。
- `Round 35 / contact-sheet 复审`
  - 继续抽看 `P05 tail -> P06 head` 和 `P06 tail -> P07 head` 后，当前判断不变：
  - `P05 -> P06` 仍带一点从人物反应切到第一人称暗层入口的风格化跳接，但已经不再像旧版那样先亮一下再重开页面。
  - `P06 -> P07` 当前这刀 `head trim` 继续成立，桌面波形和旧档案桌面还能读成同一条追索后果。
  - 这轮不再追加新的 `trim / bridge`，先继续按 `PASS WITH NOTES` 观察，不把 still-stylized handoff 误判成新 blocker。

## 9. 后续观察顺序

1. 先观察这次 `P05 v5 tailtrim2 + P06 v8 voiceclarity + P07 v3 head trim` 是否已经足够稳定承担 current 入口职责。
2. 再继续审 `P05 -> P06 -> P07` 的连续性，必要时只走 `trim / bridge / reorder`。
3. 如果未来拿到更强 native same-space ingress，再替换当前 recovery path。
4. 不回头重开已经可留的 `E02-E04`。

## 10. 和页面的关系

当前预览页已经开始直接读取：

- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

因此这份修复合同当前先作为 production 主文档存在。

后续如果需要把更细的 `P06` 修复账展示到资产总览页，应该优先从这份文档或它的结构化镜像读取，而不是在页面里手写第二套说明。
