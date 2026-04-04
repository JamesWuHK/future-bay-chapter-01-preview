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

- `part_id`：`P04`
- `part_name`：`等待区与父亲`
- `当前状态`：`DONE WITH NOTES`
- `当前判断`：`PASS WITH NOTES / P04->P05 BRIDGE APPLIED`
- `对应总控`：
  - [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
  - [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
  - [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)

## 3. P04 修复目标

把 `P04` 从“当前能看但仍有 replacement debt”的状态，推进到真正可稳定接入 `P05` 的正式 current 口径。

这段现在最重要的，不是多炫，而是下面 4 件事必须同时成立：

1. 观众一眼能看懂这还是 `悬浮档案大厅外侧的等待区`，不是突然切去新地点。
2. `签字笔` 和 `家属安抚屏` 要先把“温柔包装的压力”落进家庭空间，而不是只当漂亮道具飘过去。
3. 父亲说的“为你好”必须在同一条等待区压力链里真正落地，不能只剩一句模糊好心话。
4. 林澄的反问要自然接住这股压力，并把整段推向 `P05` 的概率长廊，而不是像页面跳转。

换句话说，`P04` 必须把下面这条线讲顺：

`等待区 -> 签字笔 -> 安抚屏 -> 父亲保护逻辑 -> 林澄反问 -> P05`

## 4. 这一轮必须回答的问题

1. `S01-S02` 是否已经把大厅外侧等待区、签字笔和安抚屏放进同一个空间里？
2. `S03` 是否已经不只是“等待区锚点”，而是真的把父亲那句“不是逼，是怕更难改”压进现场？
3. `S04` 父亲近景是否既像本人，又把“为你好”的现实压迫感说清楚了？
4. `S05` 林澄近景是否把反问说得足够像人，而且还能把压力继续送进 `P05`？
5. `P04 -> P05` 是否已经不用靠补说明字卡才能看懂？

## 5. 镜头级修复账

| Shot | 当前类型 | 当前判断 | 本轮职责 | 通过标准 | 失败信号 |
| --- | --- | --- | --- | --- | --- |
| `CH01-P04-S01` | `entry_bridge` | `KEEP_WITH_NOTES` | 交代这里是大厅外侧等待区，而不是新页面 | 空间关系一眼能懂，而且 current 源里已经有真实可播放 clip | 如果这镜再次退回坏链、静帧假视频，或让人误会成新地点硬切，就直接算失败 |
| `CH01-P04-S02` | `pressure_build` | `KEEP_WITH_NOTES` | 先把签字笔和安抚屏拉成同一条温柔压力线 | 道具、空间、情绪落在同一处，而且 current 源里已经有真实可播放 clip | 如果这镜再次退回占位坏链，或只剩一张静态道具图撑场，就直接算失败 |
| `CH01-P04-S03` | `pressure_chain_anchor` | `KEEP_WITH_NOTES` | 不能只稳等待区锚点，必须让父亲的保护逻辑在同一条压力链里落地 | 观众能把等待区、签字笔、安抚屏和父亲短线看成一条因果 | 这条 2.04s 真 clip 已可用，但运动很轻，仍要防它被误看成“又一张静帧” |
| `CH01-P04-S04` | `father_close` | `KEEP_WITH_NOTES` | 父亲近景立住“为你好”的压力，不变脸 | 像同一个父亲，且 speaking-ready | speaking-ready 已基本成立，但压迫感还偏正面对镜解释，后续只适合 trim，不宜夸成完全通过 |
| `CH01-P04-S05` | `lin_close` | `KEEP_WITH_NOTES` | 林澄近景立住承压与不退，把反问送进下一拍 | 像同一个林澄，且能把压力送进 `P05` | 人物稳定基本成立，但真正把它接顺的是后续 bridge recovery，不是单靠这镜自己 |

## 6. 当前通过条件

只要下面 5 条同时成立，`P04` 才能从这轮修复里过门：

1. 等待区空间关系一眼能懂。
2. 签字笔和安抚屏已经把“温柔压力”落进家庭空间。
3. 观众能把 `等待区 -> 签字笔 -> 安抚屏 -> 父亲逻辑 -> 林澄反问` 看成同一条后果链。
4. 父亲与林澄近景都维持 `canonical` 识别。
5. `P04 -> P05` 的压力传递自然成立，不再依赖假视频或说明性补丁硬撑。

## 7. 当前失败条件

只要出现下面任一条，就不算通过：

1. 观众会把 `P04` 看成突然切到一个新页面。
2. 签字笔、安抚屏和父亲短线互相不接，看不出它们为什么会一起压到林澄身上。
3. 父亲或林澄在关键近景里明显像换了一个人。
4. 必须靠额外说明字卡，才能把 `P04` 接进 `P05`。
5. 修完以后虽然更热闹了，但更看不懂因果。

## 8. 当前 recovery path 与复审结论

- `S01`：`KEEP WITH NOTES`
  - `p04-s01-waiting-zone-ingress-current.mp4` 已同步成真实 current clip，不再是坏掉的软链接占位。
  - 这一拍已经能把观众带进大厅外侧等待区；后续若再升级，优先只做 same-space motion polish，不重开它的空间职责。
- `S02`：`KEEP WITH NOTES`
  - `p04-s02-sign-pen-soothing-screen-current.mp4` 已同步成真实 current clip，不再停留在缺失源视频状态。
  - 这镜已经能承担“签字笔 + 安抚屏”的温柔压力插拍，后续只适合同空间微调，不适合整镜推倒重来。
- `S03`：`KEEP WITH NOTES`
  - 真实 2.04 秒 clip 已存在，父亲和林澄在同一等待区空间内，因果比旧口径清楚。
  - 但运动量很轻，仍要防它看起来像轻微动过的双人站位图。
- `S04`：`KEEP WITH NOTES`
  - 父亲身份稳定、开口可信，当前不是主 blocker。
  - 后续更适合做 trim 和接法优化，不适合整镜重开。
- `S05`：`KEEP WITH NOTES`
  - 林澄身份稳定、情绪可接。现在这镜已经不再单独硬扛去 `P05` 的任务，而是和后续 bridge recovery 一起完成承压传递。
- `P04 -> P05`：`BRIDGE APPLIED WITH NOTES`
  - 当前 current 已插入 `chapter-01-p04-p05-consequence-bridge-v1.mp4`，把林澄近景尾部直接溶进 `D02` 的路径比较节点。
  - `P05 current` 已同步切到 `part-05-probability-corridor-delivery-v3-d02first.mp4`，不再让更抽象的 `D01` 充当 current 开门 beat。
  - `D01` 仍保留为独立资产，但不再出现在当前 official part-05 入口。
  - 这条 bridge 已经显著收紧“切到新页面”的感觉，但它仍是 `assembly-level recovery path`；如果后续拿到更强的 native same-space clip，应优先替换它。
- `P04 current`：`PASS WITH NOTES`
  - 当前 `P04` 已从“bridge required”收口为“bridge applied with notes”。
  - 这次通过的是 `current continuity`，不是宣称这一段以后永远不用再升级。

## 9. 后续观察顺序

1. 先观察这条 `assembly-level bridge` 是否已经足够稳定承担 current 入口职责。
2. 再继续做 `S03-S05` 的 trim、接法和轻度压迫感微调。
3. 如果未来拿到更强的 native same-space bridge，再替换当前 recovery path。
4. 不回头重开已经可留的 `S01/S02`。

## 10. 和页面的关系

当前预览页已经开始直接读取：

- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

因此这份修复合同当前先作为 production 主文档存在。

后续如果需要把更细的 `P04` 修复账展示到资产总览页，应该优先从这份文档或它的结构化镜像读取，而不是在页面里手写第二套说明。
