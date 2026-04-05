# Version Log

## 1. 基本信息

- 项目：`AI未来通识课（K12）`
- 章节：`chapter-01-time-archive-city`
- 标题：`不被预测的人生`
- 负责人：`Codex / 项目团队`
- 当前阶段：`连续剧化样板 + P05-P07 continuity 观察 + quality-gate preview pass + P09-P10 handoff merge recovery + W11 总装有效性审计`
- 当前稳定版本：`v1.36`
- 当前 active lane：`P06`
- 当前完整故事入口：`chapter-01-story-spine-preview-v32.mp4`
- 当前 review master：`chapter-01-vertical-slice-master-v28-current.mp4`
- 当前判断：`当前 active lane 仍是 P06 continuity 观察位。P05 -> P06 -> P07 继续维持 PASS WITH NOTES；这轮先把 `quality-gate-state.json` 收成可执行的 public-preview gate，再把 `P09 -> P10` 在完整故事入口里还像“翻页”的硬切，收成 `P09 + P10 overlap merge`，并继续推进到 `story spine v32`。review master 仍保持 `v28-current`，因为它本来就不含 `P08 / P09`。`

## 2. 阶段版本总览

| 日期 | 版本 | 阶段 | 核心变化 | 是否冻结 |
| --- | --- | --- | --- | --- |
| 2026-04-05 | v1.36 | W11 / quality-gate preview pass + P09-P10 handoff merge 传导 | 把 `quality-gate-state` 从“默认整排拦死”收成可执行的 public-preview gate，再把 `P09 -> P10` 在完整故事入口里还像翻页的硬切，收成 `P09 + P10 overlap merge handoff`，并继续推进到 `story spine v32`；`review master` 不变，因为它不含 `P08 / P09` | 否 |
| 2026-04-05 | v1.35 | W11 / P07-P08 handoff merge recovery 传导 | 复审确认 `P07 -> P08` 在完整故事入口里仍像“开了新页面”，于是保持 `part-07 current / part-08 current` 不变，只在 assembly 层新增 `P07 + P08 overlap merge handoff`，把完整故事入口收成 `story spine v31`；`review master` 不变，因为它不含 `P08` | 否 |
| 2026-04-05 | v1.34 | W11 / P11 G02 english-leak recovery 传导 | 抓到 `P11 / G02` close-up 两侧会露出来的英文漂浮文档，于是直接做 assembly-level world-in 浮卡遮罩 recovery，把 `part-11 current` 收成 `v5`，并继续重渲 `story spine v30 / master v28-current` | 否 |
| 2026-04-05 | v1.33 | W11 / P08 head-trim recovery 传导 | contact-sheet 复审确认 `P07 -> P08` 的真正问题是 `P08 / E09` 空白建立略久，于是把 `part-08 current` 收成 `v2 headtrim`，并继续重渲 `story spine v29`；`review master` 不变，因为它不含 `P08` | 否 |
| 2026-04-05 | v1.32 | W11 / P07 warm-ingress recovery 传导 | contact-sheet 复审确认 `P07 v3 head trim` 把沉默练习室入口裁过了，于是改成保留暖房间入口的 `part-07 v4 warm-ingress`，并继续重渲 `story spine v28`；`review master` 不变，因为它不含 `P07` | 否 |
| 2026-04-05 | v1.31 | W11 / P09 localized-ui recovery 传导 | 抓到 `P09 / E13` 源 clip 里还露着英文伪 UI，于是直接做 assembly-level localized overlay recovery，把 `part-09 current` 收成 `v4 localized-ui`，并继续重渲 `story spine v27`；`review master` 不变，因为它不含 `P09` | 否 |
| 2026-04-05 | v1.30 | W11 / P05 tail-trim refine 传导 | 继续按 contact-sheet 复审 `P05 -> P06`，抓到 `P05` 尾部仍多留了半拍“重新站稳”的泄气感，于是把 `part-05 current` 再收成 `v5 tailtrim2`，并继续重渲 `story spine v26 / master v27-current` | 否 |
| 2026-04-05 | v1.29 | W11 / P06 E03-E04 清晰度热修 | 把 `P06 / E03-E04` 从已闭环的 `v7` 继续收成更清楚、更像孩子一遍能听懂的 `part-06 v8 voiceclarity`，再继续重渲 `story spine v25 / master v26-current`；本地 rough STT 已能更稳定抓到 `第四条路回来了 / 别只听最大声那条` 的骨架 | 否 |
| 2026-04-05 | v1.28 | W11 / P06 E03-E04 有声闭环 | 把 `P06 / E03` 的系统确认和 `P06 / E04` 的风声婆婆旧录音短线，真实补进 `part-06 v7`，再继续重渲 `story spine v24 / master v25-current`，关掉“文稿承诺有声、成片还是静音氛围位”的断点 | 否 |
| 2026-04-05 | v1.27 | W11 / P09-P10 baked-audio 真闭环 | 把 `P09/S03` 与 `P10/S03` 的 speaking clip 重生为 current 短线，并继续重渲 `part-09 v3 / part-10 v5 / story spine v23 / master v24-current`；仓库外 rough STT 已复核旧 baked-audio 债从 current 清掉 | 否 |
| 2026-04-05 | v1.26 | T08 / 本地 rough STT 复审与 P10 上游模板清理 | 打通仓库外 `faster-whisper` 粗转写检查路，确认 `P09 / P10` 仍有旧 baked-audio 债务，并把 `P10/S03` 的旧“高概率 / 低概率”重生模板统一改成 current 短线；本轮没有新的 `part / story spine / master`，只算 docs-only | 否 |
| 2026-04-05 | v1.25 | W11 / P07 head-trim continuity 传导 | 把 `P07` 开头更像新页面建立位的走廊 lead-in 收成 `v3 head trim`，让 `P06` 的桌面波形更直接接到 `P07` 的旧档案桌面，并真实推进到 `part-07 v3 / story spine v22` | 否 |
| 2026-04-05 | v1.24 | W11 / P09 overlay cleanup 传导 | 把 `P09` 冻结提示里还像回执单的可见文案收成更直接的人话，并真实推进到 `part-09 v3 / story spine v21`；`review master` 刷新到 `v23-current`，但继续明确只当 vertical-slice subset | 否 |
| 2026-04-05 | v1.23 | W11 / P05-P06 continuity tail-trim 传导 | 不重开模型，直接把 `P05 current` 做成 editor-level tail trim，去掉旧的正面定住 pose，并真实重装到 `part-05 v4 / story spine v20 / master v22-current` | 否 |
| 2026-04-05 | v1.22 | W11 / P10 viewer-visible 文案传导 | 把 `P10` 自由回响台里仍会被观众直接看到的文件 / UI 腔继续收口成更直接的人话，并真实重装到 `part-10 v5 / story spine v19 / master v21-current` | 否 |
| 2026-04-05 | v1.21 | W11 / 总装有效性审计 + P11 结果层传导 | 把“没进 `part delivery -> story spine -> master` 不算完成”写回状态源，并把 `P11` 结果层的可见文件腔真正推进到 `part-11 v4 / story spine v18 / master v20-current` | 否 |
| 2026-04-05 | v1.20 | T10 / 页面可见口径继续收口 | 收掉主入口和五份主文稿里剩余的 `主位 / 点头 / 扛下 / 不予开放` 等旧词，并补齐 `product-script.md / episode-onscreen-copy.md` 的公开镜像；但这一轮没有新的 `part delivery / story spine / master`，只算 docs/page sync，不计总装推进 | 否 |
| 2026-04-05 | v1.19 | T10 / 文稿兑现边界收口 | 把 `分镜脚本 / 趣味增强 / 产品稿 / 上屏文案 / 资产总览页` 的 current / 后补边界统一写清，并把资产总览页扩展成五份主文稿镜像入口；但这一轮没有新的 `part delivery / story spine / master`，只算 docs/page truth sync | 否 |
| 2026-04-05 | v1.18 | T08 / P01 current hotfix 传导 | 修掉 `P01/S04` 旧 baked line 与 `P01/S07` 错片/半句串镜问题，重装 `part-01 v31 / story spine v17 / master v19-current`，让开场 hotfix 真正传导到 chapter 级入口 | 否 |
| 2026-04-04 | v1.17 | T08 / 装配传导与 continuity 快检 | 把 `P01 / P09 / P10 / P11` 的 current delivery 重新渲染到更口语、更世界内的装配文案口径，并同步重装 `story spine v16 / master v18-current`；同时完成 `P05 -> P06 -> P07` transition contact-sheet 复审，当前判为 `PASS WITH NOTES` | 否 |
| 2026-04-04 | v1.16 | T08 / P05-P07 对白复审继续推进 | 继续收 `P05 -> P06 -> P07` 的角色口气同质化和不够像人话的句子，回写主稿、分场、分镜、配音台本与整改清单，并同步到线上预览镜像 | 否 |
| 2026-04-04 | v1.15 | W11 交付入口纠偏与对白传导状态落账 | 明确 `story spine v16` 才是当前 `P01-P12` 完整故事入口，`vertical slice master v18` 只保留作 review master；同步把“最新人话化对白尚未全部传导到成片音轨”写入 current 状态源和资产总览页 | 否 |
| 2026-04-04 | v1.14 | P06 ingress trim recovery 落地 | 把 `P06 / E01` 开头那一拍更亮、更空的走廊 reset 通过 trim recovery 收掉，并同步重装 `part-06 current v6 / master v18 / story spine v16 / preview current` 同一口径 | 否 |
| 2026-04-04 | v1.13 | P04-P05 bridge recovery 落地 | 把 `P04 -> P05` 的 consequence bridge 正式装进 `official current`，同步把 `P05 current` 切到 `D02-first` recovery 入口，并回写 `master v17 / story spine v15 / preview current` 同一口径 | 否 |
| 2026-04-03 | v1.12 | P02-P07 编号对齐与追索链收口 | 把 `script.md` 前半段重新对齐为 canonical 场次顺序，明确 `Scene 02` 只负责入港门槛、`Scene 03` 单独承担大厅对峙，并把 `P06` 的 `异常风声 -> 对波形 -> 找门 -> 第四路径 reveal` 收成单线动作；同步补入 `Scene 11 / P12` 的极简收束，并回写 `storyboard-script.md` 问题台账 | 否 |
| 2026-04-03 | v1.11 | P06-P07 入口桥接收口 | 在 `第四路径 reveal` 后补入 `沉默练习室` 旧训练记录，明确 `P07` 不是突然切到新房间，而是顺着第四路径留下的旧线索继续追进去；同步回写 `master-episode-script.md`、`script.md` 与 `storyboard-script.md` | 否 |
| 2026-04-03 | v1.10 | P11 后果层减压与双拍收口 | 把 `Scene 10 / P11` 从“签署结果 + 回航立案一口气结算”拆成“先落今晚后果，再落回航后果”的双拍口径，并同步回写 `master-episode-script.md`、`script.md` 与 `storyboard-script.md` | 否 |
| 2026-04-03 | v1.09 | P08 时间线收口与 P09-P10 桥接修复 | 修正 `script.md` 中 `Scene 08` 的倒计时冲突，把 `系统的理由` 与 `证据失效` 拉回 canonical 顺序，并把“私下补件来不及，只剩回响台公开窗口还能继续争”同步回写到 `master-episode-script.md`、`script.md` 与 `storyboard-script.md` | 否 |
| 2026-04-03 | v1.08 | 逐场可读性问题台账回写 | 把 chapter-01 从 `Scene 01 / P01` 到 `Scene 11 / P12` 的铺垫不足、信息跳跃、时间线冲突与桥接缺口，逐场回写到 `storyboard-script.md`，形成后续逐个修复的唯一问题台账 | 否 |
| 2026-04-03 | v1.07 | P03 人话版 current 同步 | 把 `P03 v6 / story spine v37-full / chapter master v33-current` 回写到主 HTML、loop 状态、版本日志与预览页，清掉旧 `v36 / v32 / P03 v4` 口径 | 否 |
| 2026-03-19 | v0.1 | 内容与 demo 骨架 | 建立章节主稿、产品脚本、分镜、配音、demo 流程与首批制作清单 | 是 |
| 2026-03-19 | v0.2 | AIGC 产线准备 | 建立 prompt bible、asset manifest、版本日志与制作模板层 | 是 |
| 2026-03-20 | v0.3 | 叙事升级与制作对齐 | 把第四路径改成“困难可能性”，同步脚本、UI、上屏文案、分镜与配音口径 | 否 |
| 2026-03-20 | v0.4 | 连续剧化升级 | 确立未来湾固定团队主位、新增证据失效与责任签署机制、点亮“系统看起来很体贴，其实在替人决定人生”这条长线阴影 | 否 |
| 2026-03-20 | v0.5 | 数据与生产模板补位 | 对齐 JSON、asset manifest、prototype 资产清单与第二轮关键 API 请求模板 | 否 |
| 2026-03-20 | v0.6 | 生产编号收口 | 对齐连续剧版 `S / C / UI` 编号，补固定团队模板与新高潮链 UI 请求，删除旧编号重复模板 | 否 |
| 2026-03-21 | v0.7 | Flow 试片落地 | 新增 Flow 纵切试片包，收口 chapter-01 的低成本视频验证入口 | 否 |
| 2026-03-21 | v0.8 | 主稿重写与角色锁定 | 重写整集总脚本，落实连续剧化改进，并新增可用于生图锁角色的定妆包 | 否 |
| 2026-03-22 | v0.9 | 分镜执行稿升级 | 把 `shot-list.md` 的 C-G 段补齐为 production-ready 字段，回绑场景、角色与生成路由 | 否 |
| 2026-03-22 | v0.10 | 首轮视频执行包补位 | 新增 4 个 shot keyframe 请求模板，并把 Flow 第一优先批补成可直接试跑的 clip 执行单 | 否 |
| 2026-03-23 | v0.11 | P01 分镜重拆 | 按主剧本重拆未来湾开场 beat，修正 canonical shot 逻辑与成片映射边界 | 否 |
| 2026-03-24 | v0.12 | P01 音频交付补强 | 把 P01 从单一占位音轨升级为多角色试音 + 任务音效层的可试听交付版 | 否 |
| 2026-03-24 | v0.13 | P01 正式试音替换 | 把 P01 从本地占位试音升级为神经语音正式试音包，并重做桥接与启航声场 | 否 |
| 2026-03-24 | v0.14 | P01 编辑母带收口 | 把 P01 从“多人试音展示版”收成对白更少、混音更稳的正式开场母带 | 否 |
| 2026-03-24 | v0.15 | P02 纸片验证落地 | 把紧急入港校验段推进成可审节奏的 paper cut 成片与可复用装配脚本 | 否 |
| 2026-03-24 | v0.16 | P02 主交付链建立 | 把 P02 从 paper cut 节奏验证推进到已有稳定主装配文件的状态 | 否 |
| 2026-03-24 | v0.17 | P01 口型与尾段气氛修正 | 把 P01 收成当前唯一主交付入口，并同步统一展示层编号口径 | 否 |
| 2026-03-24 | v0.18 | P01 开场导演复盘 | 明确当前主交付只承担气质验证，不能替代正式连续剧开场，并锁定唯一下一步为 7-beat 重装配 | 否 |
| 2026-03-24 | v0.19 | P01 canonical story-clear 重装配 | 补出 `S04/S06` 关键首帧，并交付按 `CH01-P01-S01-S07` 讲清故事的 `v9` 主装配 | 否 |
| 2026-03-25 | v0.20 | P01 同步镜头升级 | 把 `S03/S04/S06/S07` 从纸片承接升级为同步音视频镜头，并交付 `v10` 主装配 | 否 |
| 2026-03-25 | v0.21 | P01 开场声场修正 | 在保留同步对白镜头链的前提下，把 `S01/S02` 的未来湾环境声与信号唤醒层补回到 `v11` 主装配 | 否 |
| 2026-03-25 | v0.22 | P01 可读性与截断修正 | 进一步加强开头声场，补出 `S02` 高对比灰银任务牌，并把 `S04` 放回完整时长，交付 `v12` 主装配 | 否 |
| 2026-03-25 | v0.23 | P01 林澄台词收口 | 重生 `S06` 同步镜头，改用更短的林澄台词并交付 `v13` 主装配，解决“话没说完就被截断”的源 clip 问题 | 否 |
| 2026-03-25 | v0.24 | P02/P03 wan2.6-r2v workflow 实战 | 明确 `B04` 的 R2V 试片不能进主线，并把 `C01` 推进成第一条可继续扩展的大厅建立镜头 | 否 |
| 2026-03-25 | v0.25 | P03 identity-first workflow 校正 | 明确 `C01` 旧 `R2V` 分支不进主线，改用 `scene-state keyframe + actor_refs -> short I2V -> QC -> 必要时裁切` 的主路线 | 否 |
| 2026-03-26 | v0.27 | P03 正式交付收口 | 把 `P03` 收成 `delivery v1` 主文件，并同步更新主 HTML 资产页为正式审片入口 | 否 |
| 2026-03-27 | v0.29 | P05 导演室收口 | 完成 `P05` 的导演室拆镜与 keyframe 优先级判断，把 loop 下一步从“待审”推进到“先做 D01，再做 D04” | 否 |
| 2026-03-27 | v0.30 | P05 青云图像链验证 | 用 `qingyuntop` 验证 `P05/W4` 的替代首帧链，确认 `D01` 已可出图，`D04` 仍受多图配额/路由约束 | 否 |
| 2026-03-28 | v0.31 | P05 story-first 粗资产推进 | 不再把高清大图当眼前瓶颈，先把 `D01 v1 + D04 v7 + S-04` 收成可跑通流程的 rough pack，推进到低成本节奏验证 | 否 |
| 2026-03-28 | v0.32 | P05 D02 UI 粗验证 | 为 `D02` 补出同空间 `路径切换 + 价值勾选` overlay，并回写主资产页与 loop 下一步 | 否 |
| 2026-03-28 | v0.33 | Chapter01 持续 loop 驱动器 | 补出可持续运行的 loop driver，修正 current preview 入口，并把 stable current hub 与 chapter-01 的唯一下一步绑定 | 否 |
| 2026-03-28 | v0.34 | P05 rough preview 落地 | 把 `D01 + D02 overlay + D04 v7` 装成 `part-05` 的可审 paper cut 预览，并把 loop 下一步收口到“先审 preview” | 否 |
| 2026-03-28 | v0.35 | P05 W6 通过并进入 W7 | 完成 `P05` rough preview 自审，把 `纸片剪辑验证` 判成 `PASS WITH NOTES`，主线进入视频与 audio contract 收口 | 否 |
| 2026-03-28 | v0.36 | P06 导演室与 shot contract 收口 | 把 `P06` 从待接棒状态推进到 `W3` 参考锁定前夜，锁定 `E01-E04` 的职责、声音顺序与唯一下一步 | 否 |
| 2026-03-28 | v0.37 | P06 首轮首帧与 paper cut 落地 | 生成 `E01-E04` 首帧并装配 `part-06` rough preview，把 `P06` 从 `W3` 推进到 `W6 PASS WITH NOTES` | 否 |
| 2026-03-28 | v0.38 | P06 交付收口并切换到 P10 | 把 `E03` 收成当前可用 rescue clip、装出 `part-06 delivery v1`，并把 active part 正式交给 `P10` | 否 |
| 2026-03-28 | v0.39 | P10 导演室与 shot contract 收口 | 把自由回响台辩论收口成 `F01 空间建立 + F02 UI-first + F03 唯一优先短 clip + F04 UI-first` 的可执行口径 | 否 |
| 2026-03-28 | v0.40 | P10 首轮首帧与 paper cut 落地 | 生成 `F01` 与 `F03` 首帧、装配 `part-10` low-cost paper cut，并把 loop 下一步推进到 `W7` 的 `F03` 正式短 clip | 否 |
| 2026-03-28 | v0.41 | P10 W7 正式视频模板与首轮提交 | 为 `F03` 补齐正式视频模板并真实发起 `vidu / veo` 提交，明确当前阻塞是 provider 级，而不是镜头合同失败 | 否 |
| 2026-03-28 | v0.42 | P10 story-first 交付收口并切换到 P11 | 用 `F03 rescue clip` 收成 `part-10 delivery v1`，把 P10 提升为 `accepted_with_notes`，并把 active part 正式切到 `P11` | 否 |
| 2026-03-28 | v0.43 | P11 导演室收口并推进到 W2 | 收紧午夜前选择与回航段的导演判断，明确 `G02` 为唯一优先正式人物视频位，active part 继续推进到 `P11 / W2` | 否 |
| 2026-03-28 | v0.44 | P11 首帧与 rough preview 落地 | 生成 `G01/G02` 首帧并装配 `part-11` paper cut，让 P11 从 `W2` 推进到 `W7 / PASS WITH NOTES` | 否 |
| 2026-03-28 | v0.45 | P11 G02 多 provider 正式提交收口 | 真实轮转 `qingyun` 下的 `vidu / wan / hailuo / kling` 提交家族，确认当前阻塞位并补齐 DashScope 直连模板 | 否 |
| 2026-03-29 | v0.46 | P11 G02 自动提交 loop 落地 | 把 `G02` 收成可执行提交循环脚本，并用一轮真实执行把 `missing key / 429 / 500` 分型收口到 machine-readable 状态 | 否 |
| 2026-03-29 | v0.47 | P11 正式 clip 过门并交付 | 接收 `G02 / viduq3` 成功 clip、完成 `W9` 轻量 QC，并收成 `part-11 delivery v1`，让主线正式切到 `P12` | 否 |
| 2026-03-29 | v0.48 | P12 导演室与单镜收束合同 | 把旧版 4 镜导师总结压缩为 `G05` 单镜收束，并把主线推进到 `W3` 的 mentor-space 参考锁定 | 否 |
| 2026-03-29 | v0.49 | P12 mentor-space 落图与 route rollback | 收到 `S-09 mentor-space v2` accepted clean plate，并把漂移的可见导师首帧回退为 `voice-first` 路线，主线推进到 `W6` | 否 |
| 2026-03-29 | v0.50 | P12 voice-first 预览落地 | 基于 accepted clean plate 装出 `part-12` 低成本语音预览，确认当前可以进入 `W7` 的正式 audio contract 收口 | 否 |
| 2026-03-29 | v0.51 | P12 正式交付收口并完成 chapter loop | 把 `voice-first preview v2` 提升为 `part-12 delivery v1`，同步 audio contract 与主资产页，并让 chapter-01 首版视频主线全部进入 `accepted_with_notes` | 否 |
| 2026-03-30 | v0.52 | Chapter-01 vertical slice master 装配 | 新增章节级 master 装配脚本，串联 current hub 的 9 条 accepted parts，形成 `171.34s` 可审 spine，并明确展示版下一步只收 `P01/P12` 时长与 `P03/P06/P10` 的高价值 backlog | 否 |
| 2026-03-30 | v0.53 | P03 relation paper cut 补强 | 用大厅三角、林澄近景和 07 压迫位装出 `P03` 低成本关系预览，专门验证 `C02/C04` 的人物关系可读性，不替代 current delivery | 否 |
| 2026-03-30 | v0.54 | Chapter-01 master v2 P03 override 对照 | 用 `P03 relation paper cut` 替换 current `P03` 重新装出章节级 master，对照判断这次关系补强是否值得继续推进到 delivery v2 | 否 |
| 2026-03-30 | v0.55 | P03 delivery v2 提升并回写 current | 把已验证的 relation-led 低成本重装配正式提升为 `P03` current delivery，完成 loop 状态、主 HTML 与 current 指针回写 | 否 |
| 2026-03-30 | v0.56 | Chapter-01 master current 对齐到 P03 v2 | 基于最新 current parts 重渲章节级 master，并补出稳定的 `chapter-01-master-current.mp4` 入口，避免继续混用旧版 P03 spine | 否 |
| 2026-03-30 | v0.57 | P10 F03 Qingyun rotation 二轮收紧 | 把第二轮重试结果写回主线，确认当前 15 模型池仍无稳定通过项，rotation 现在是恢复 harness 而不是已可用轮换池 | 否 |
| 2026-03-30 | v0.58 | P10 F03 新家族补测 | 新接入 `veo / sora / grok-video` 6 条家族并完成真实补测，把 tested pool 扩到 21，并确认当前仍无稳定通过项 | 否 |
| 2026-03-30 | v0.59 | P10 F03 veo 家族近亲补测 | 继续顺着 `veo3.1-fast` 的非 401 信号补测近亲，把 tested pool 扩到 26，并收出 `veo3.1-pro = 502` 的新观察位 | 否 |
| 2026-03-30 | v0.60 | P10 F03 veo3.1 变体补测 | 继续补测 `components` 与下划线别名，把 tested pool 扩到 30，并确认这些变体当前全部回到 401 | 否 |
| 2026-03-30 | v0.61 | P10 F03 正式 clip 过门并回写主 spine | 接收新 key 下的 `viduq3-turbo` 成功 clip，替换旧 `F03 rescue clip`，并同步重渲 `part-10 delivery` 与 chapter master current | 否 |
| 2026-03-31 | v0.62 | P07-P09 故事补桥预览 | 新增 `P07-P09 middle bridge paper cut` 与 `chapter-01 story spine preview`，专门验证补回中段承重后，章节是否从预告片感转向完整故事感 | 否 |
| 2026-03-31 | v0.63 | P07-P09 故事补桥 v2 | 在 preview 基础上继续补 `P06 -> P07`、`P07 -> P08`、`P09 -> P10` 三处结构桥，并重出 `story spine preview v2` | 否 |
| 2026-03-31 | v0.64 | P07-P09 正式 shot contract 回写 | 把 `P07-P09` 正式补回 `shot-list.md`，形成 `E05-E17` 与 `N05A-N05D` 执行链，并把下一步收口到关键首帧与正式 clip 升级 | 否 |
| 2026-03-31 | v0.65 | P07-P09 关键首帧落地 | 生成 `E05/E09/E13/E17` 的当前首帧，并把结果挂到 `current/shots`、`current/images` 与主 HTML | 否 |
| 2026-03-31 | v0.66 | P07-P09 首轮正式 clip 与 story spine v3 | 接收 `E05 / E09 / E13` 的 `viduq3-turbo` 正式短 clip，生成 `bridge v3` 与 `chapter-01 story spine preview v3`，并把 `P07-P09` 重新纳入视频 loop 主线 | 否 |
| 2026-03-31 | v0.67 | P07 E06 真实物件痕迹 clip | 把 `E06` 从缺失位推进成 `qwen-image-max + viduq3-turbo` 的真实短 clip，挂入 `current/shots`、`current/clips` 与主 HTML，让 `P07` 开始具备“有人真实活过”的中段承重 | 否 |
| 2026-03-31 | v0.68 | P07 E07 旧录音承载体 clip | 把 `E07` 从“待想办法处理台词”的风险位推进成 `carrier-first` 的真实短 clip，先锁住风声婆婆短线的视觉承载体，再把下一步收口到 `E07` 短句音频与 `E08` 停留段 | 否 |
| 2026-03-31 | v0.69 | P07 独立交付收口并切换到 P08 | 补齐 `E08` 真实 listening clip、正式落盘 `E07` 短句音频，并装出 `part-07-silent-practice-room-delivery-v1.mp4`；`P07` 进入 `accepted_with_notes`，loop 焦点正式切到 `P08` | 否 |
| 2026-03-31 | v0.70 | P08 独立交付收口并切换到 P09 | 补齐 `E11` 序列员 07 立场 speaking clip，并用 `E09 + E10 + E11 + E12` 装出 `part-08-rule-projection-room-delivery-v1.mp4`；`P08` 进入 `accepted_with_notes`，loop 焦点正式切到 `P09` | 否 |
| 2026-03-31 | v0.71 | P09 正式交付 + chapter story spine v4 | 把 `P09` 从“还缺冻结质疑与团队分裂”推进成独立可交付 part，并把 `P07/P08/P09` 正式插回整章，形成当前最完整的故事观看口径 | 否 |
| 2026-03-31 | v0.72 | P06 假视频债务清理完成并切到 P05 | 把 `P06 / E01-E04` 全部推进为真实 `qingyun / viduq3` 短 clip，收成 `part-06-dark-layer-interface-delivery-v4.mp4`，同步修正 loop 状态、主 HTML 与 backlog 优先级，并把 active part 切到 `P05 / D02` | 否 |
| 2026-03-31 | v0.73 | P05 D02 真实 clip 过门并切到 P02 | 把 `D02` 从 `scene still + overlay` 升级为真实 `viduq3-turbo` 路径比较 clip，重装 `part-05-probability-corridor-delivery-v2.mp4`，同步 current 指针、loop 状态与 backlog 优先级，并把 active part 切到 `P02 / B01-B04` | 否 |
| 2026-03-31 | v0.74 | P02 双 clip 过门并切到 P11 | 把 `B01 / B04` 都升级为真实 `viduq3-turbo` 短 clip，重装 `part-02-emergency-entry-check-delivery-v2.mp4`，同步 current 指针、loop 状态与 backlog 队列，并把 active part 切到 `P11 / G01-G04` | 否 |
| 2026-03-31 | v0.75 | P11 双 bridge clip 过门并切到 P12 | 把 `G03 / G04` 都升级为真实 `viduq3-turbo` 桥接 clip，重装 `part-11-midnight-choice-return-delivery-v2.mp4`，同步 chapter story spine、loop 状态与主 HTML，并把 active part 切到 `P12 / G05` | 否 |
| 2026-03-31 | v0.76 | P09 E15 人物连续性修复并回写 current | 修复 `E15` 上游首帧漂移，改用 `qwen-image-max-2025-12-30` 生成新的 `07` 锁定 keyframe，再用 `viduq3-turbo / start-end2video` 收成 `E15 v3` 与 `part-09-evidence-freeze-team-split-delivery-v2.mp4`，同步 current 指针、loop 状态、flow 与主 HTML，同时保持 active part 继续为 `P12` | 否 |
| 2026-03-31 | v0.77 | P12 弱投影 opening clip 接回尾声主线 | 把 `P12` 从纯 `voice-first clean plate` 升级为“真实 `viduq3 start-end2video` opening clip + voice-led world-in hold”的 `delivery v2`，并用 clean-plate 顶部补片救回 provider 偷塞文字的 opening clip，随后同步 current 指针、loop 状态、flow 与主 HTML | 否 |
| 2026-03-31 | v0.78 | P12 clean retry 收口并切回 P10 | 把 `P12` 的 current opening clip 从本地遮字救援版切到无后期遮字的 `clean retry` 版本，重渲 `delivery v3` 与 `chapter master v6-current`，同步 current 指针、loop 状态、flow 与主 HTML，并把下一条 active lane 切回 `P10` | 否 |
| 2026-03-31 | v0.79 | P10 F01 真实建立镜接回高潮主线 | 把 `P10/F01` 从 still-motion 建立位升级为真实 `viduq3-turbo` 公共空间建立 clip，重渲 `part-10 delivery v2` 与 `chapter master v7-current`，同步 current 指针、loop 状态、flow 与主 HTML，并把 `P10` backlog 收缩到 `F02/F04` | 否 |
| 2026-03-31 | v0.80 | P10 F02/F04 动态 carrier 接回高潮中段 | 把 `F02/F04` 从同一张母图的静态 zoompan 底座升级为真实 `viduq3-turbo` same-space carrier，重渲 `part-10 delivery v3` 与 `chapter master v8-current`，同步 current 指针、loop 状态、flow 与主 HTML，并把 `P10` 的主问题从“假视频债务”收缩为“中段节奏与 UI-first 可读性复审” | 否 |
| 2026-04-01 | v0.81 | chapter-01 故事结构复审与 canonical 互动链收束 | 重新审 chapter-01 的整集主稿、互动稿、分镜和 shot list，明确儿童可理解的背景交代、5 个高压互动锚点、`P10 -> P11` 双拍高潮摆位、第一集默认 `human_vs_agent` 辩论模式，以及玩家与队友在回响台中的职责关系，并同步回写主 HTML | 否 |
| 2026-04-01 | v0.82 | chapter-01 结构复审一致性收口 | 收掉分镜和产品稿中残留的旧辩论口径，明确多模式只是产品层预留，第一集只走 `human_vs_agent`；同步把本轮 to do 完成状态与剩余唯一风险更新到主交付 HTML | 否 |
| 2026-04-01 | v0.83 | P10->P11 双拍高潮编辑复审 | 按 `editor + directors-room` 联合复审当前 `P10/P11/master` 成片，确认问题已从“文档没写清”收缩为“F04 -> G01 缺一拍 consequence bridge”，并把 `TRIM / BRIDGE / KEEP` 级结论回写到 flow、version log 和主交付 HTML | 否 |
| 2026-04-01 | v0.84 | P10->P11 consequence bridge 落地并切回 P01 | 把 `P10/F04` 尾部收短、在 `P11` 开头插入低成本 consequence bridge 并收短 `G01`，重装 `P10 v4 / P11 v3 / chapter master v9 / story spine v5`，修正 current 指针后把 active lane 切回 `P01` | 否 |
| 2026-04-01 | v0.85 | P01 开场静尾 trim 收口并同步章节入口 | 先不重开开场模型，按 `editor` 结论把 `S06 v2` 静尾从装配层收短，重装 `P01 v14`，同时把 `chapter master` 升到 `v10-current`、`story spine` 升到 `v6`，并同步 current 指针、loop 状态、flow 与主 HTML | 否 |
| 2026-04-01 | v0.86 | P01 守望者交班尾部收口并继续保留 active lane | 继续按 `editor + directors-room` 审开场，确认 `S04 KEEP / S05 TRIM_TAIL / S07 KEEP`，把 `S05` 从 `4.0s` 收到 `3.4s`，重装 `P01 v15 / chapter master v11-current / story spine v7`，并同步 current 指针、loop 状态、flow 与主 HTML | 否 |
| 2026-04-02 | v0.87 | P01 前段假视频债务收紧并修复 current 状态漂移 | 先修 `video-loop-state.json` 失效与 current 口径漂移，再把 `P01` 前两拍从装配层收短，重装 `P01 v16 / chapter master v13-current / story spine v9`，并把开场假视频债务从笼统 `A01-A03` 收束为更真实的 `A01-A02` 主债务 | 否 |
| 2026-04-02 | v0.88 | P06->P07 consequence bridge 落地并切到 P07 可读性修复 | 新增 assembly-level `P06 -> P07` consequence bridge，重渲 `story spine v10` 并切回 current，把 `P05/P06/P07` 的问题从“页面切换感”收缩为“暗部亮度与可辨识度”，同步回写 loop、flow 与主 HTML | 否 |
| 2026-04-02 | v0.89 | P07 开场可读性提亮并同步完整故事预览 | 对 `P07` 前三拍做轻度 assembly-level readability lift，重装 `part-07 delivery v2`，再重渲带 bridge 的 `story spine v11`，把 active technical fix 前移到 `P08` 的暗部可读性复审 | 否 |
| 2026-04-02 | v0.90 | P12 尾声从假视频 hold 收成明确离场卡片 | 复审确认 `P08/P09` 不属同类暗部失败后，把 `P12` 从“真实 opening clip + voice-led hold”升级为“真实 clean retry opening clip + 明确 world-in mentor question card”，重装 `P12 v4 / chapter master v14-current / story spine v12`，并把假视频主债务收缩到 `P01 A01-A02 + P03 C02` | 否 |
| 2026-04-02 | v0.91 | P01 前两拍改成显式 intro cards，不再伪装成运动镜头 | 把 `A01/A02` 从 still-motion linger 重写为 dock intro / grey-silver request cards，重装 `P01 v17 / chapter master v15-current / story spine v13`，并把“照片加滤镜冒充视频”类主债务继续收缩到 `P03 C02` | 否 |
| 2026-04-02 | v0.92 | P03/C02 真实青云 clip 回写 current，清掉最后一条同类假视频主债务 | 把历史已验证的 `Qingyun / viduq3 / start-end2video` `P03/C02` probe 提升为 accepted current clip，重装 `P03 v4 / chapter master v16-current / story spine v14`，并把 accepted current 里的同类 fake-video 主债务正式收口 | 否 |
| 2026-04-03 | v0.93 | P01/S01 港区水面动态修复并贯通整章 current | 放弃弱水面 `A01` 路线，改用系统里已有的 `A02` 港区真 clip 重建 `S01`，重装 `P01 v19 / story spine v22-full / chapter master v18-current`，并把修复同步回总览页与预览入口 | 否 |
| 2026-04-03 | v0.94 | 全片故事可读性总修总表回写 source of truth | 把“故事看不懂”的系统性问题按 `P01-P12` 全部回写到 `storyboard-script.md`、`shot-list.md` 与主总览页，统一 current 口径、明确每段必须讲清什么、当前误读风险和下一步唯一修复动作 | 否 |
| 2026-04-03 | v0.95 | P01/S01 恢复原始 A01 构图并接回真实水动 | 把 `S01` 从单一 `A02` 路线升级成 `A01+A02` 混合开场，重装 `P01 v20 / story spine v23-full / chapter master v19-current`，并把“原图保留 + 真实水动”同步回总览页与 current 入口 | 否 |
| 2026-04-03 | v0.96 | P04 waiting-zone 真替换贯通整章 current | 把 `P04 / S01-S05` 里剩余的 still-motion 与较弱 speaking 位升级为真实青云 clip，重装 `P04 v2 / story spine v24-full / chapter master v20-current`，并把 current 指针、loop 状态与总览页同步切到新口径 | 否 |
| 2026-04-03 | v0.97 | P01/S03-S04 读懂度提示版 current 贯通整章入口 | 在保留真实 clip 的前提下，把 `P01 / S03` 阿潮集结指令和 `P01 / S04` 固定小队分工做成更直白的提示版 current，重装 `P01 v20 / story spine v25-full / chapter master v21-current`，并把 loop 状态与总览页同步切到新版本号 | 否 |
| 2026-04-03 | v0.98 | P01/S06 青云真 clip 贯通整章 current | 新增并落地 `Qingyun / viduq3` 的 `P01 / S06` 林澄争议切片真 clip，重装 `P01 v21 / story spine v26-full / chapter master v22-current`，同步 current 指针、loop 状态、总览页与预览入口 | 否 |
| 2026-04-03 | v0.99 | P01/S03-S04 直白台词真 clip 贯通整章 current | 把 `P01 / S03-S04` 从“提示版 current”继续升级成新的直白台词真 clip，重装 `P01 v22 / story spine v27-full / chapter master v23-current`，同步 current 指针、loop 状态、总览页与预览入口，并把 active lane 收束到 `S05-S07` | 否 |
| 2026-04-03 | v1.00 | P01/S05 身份交班澄清贯通整章 current | 把 `P01 / S05` 从“见习建造者”这一句观众听不懂的交班位，升级成直接点明“你就是未来湾固定小队的新主位”的 current 版本，重装 `P01 v23 / story spine v28-full / chapter master v24-current`，同步 current 指针、loop 状态、总览页与预览入口，并把 active lane 收缩到 `S06-S07` | 否 |
| 2026-04-03 | v1.01 | P01/S06-S07 读懂度修复贯通整章 current | 把 `P01 / S06` 改成第一次看就能懂的直白顺序版争议切片，并把 `P01 / S07` 明确成“已经接单，现在去时间档案城，先拿临时观察许可”的启航 current，重装 `P01 v24 / story spine v29-full / chapter master v25-current`，同步 current 指针、loop 状态、总览页与预览入口，并把 active lane 收缩到 `P01 -> P02` 承接复审 | 否 |
| 2026-04-03 | v1.02 | P02 临时观察许可门槛澄清贯通整章 current | 把 `P02 / B01/B04` 从“靠音轨和上下文才能懂”的入口段，升级成直接把制度门槛烧进真 clip 的 current 版本，重装 `P02 v3 / story spine v30-full / chapter master v26-current`，同步 current 指针、loop 状态、总览页与预览入口，并把 active lane 转到 `P03` 的人物站位复审 | 否 |
| 2026-04-03 | v1.03 | P02 后果说人话版贯通整章 current | 把 `P02 / B01/B04` 继续升级成第一次看就能懂的人话版 current，直接写出“现在只能进去看、进去问，还不能替她改结果”和“如果今晚帮不了林澄申诉成功，她的人生就会按 93% 匹配的路被锁定”，重装 `P02 v5 / story spine v31-full / chapter master v27-current`，同步 current 指针、loop 状态、总览页与预览入口，并把 active lane 继续保持在 `P03` 的人物站位复审 | 否 |
| 2026-04-03 | v1.04 | P01 S05-S07 去出戏与整队出发澄清贯通整章 current | 把 `P01 / S05` 里的制作说明从成片中拿掉，改成世界内责任表达；同时把 `S06` 补成“林澄为什么卡住”的完整处境链，把 `S07` 改成一眼能看懂“未来湾固定小队已经整队出发”的 current 版本，重装 `P01 v25 / story spine v32-full / chapter master v28-current`，同步 current 指针、loop 状态、总览页与预览入口，并继续保持 active lane 在 `P03` 的人物站位复审 | 否 |
| 2026-04-03 | v1.05 | P03 script-first 重开 | 不再继续在 `P03` 上做表面装配微修，而是按用户要求回退到主稿重写：把 `谁不肯签 / 谁在劝她签 / 谁在按程序推进 / 今晚来不及会失去什么` 锁成单线因果，并同步重写 `script.md`、`master-episode-script.md`、`storyboard-script.md`、`shot-list.md`、`voice-script.md` 与 `video-loop-state.json` | 否 |
| 2026-04-03 | v1.06 | P01 S05 截断根因修复并重发整章 current | 复核确认 `P01 / S05` 的源 clip 实长为 `5.01s`，旧装配脚本却只保留 `3.4s`，所以守望者交班会像“说到灰银任务就没了”。本轮把 `P01` 重装到 `v26`，再低磁盘修复 `story spine v34-full / chapter master v30-current`，同步补回 metadata 与总览页版本说明，确保顶部整章入口、`P01 current` 和 `master current` 都吃到这次真实修复 | 否 |

## 3. 详细版本记录

## Version `v1.36`

- 日期：`2026-04-05`
- 阶段：`W11 / quality-gate preview pass + P09-P10 handoff merge 传导`
- 目标：先把 `quality-gate-state` 从“任何重渲都会被整排 delivery_ready=false 拦死”收成可执行的 public-preview gate，再把 `P09 -> P10` 在完整故事入口里还像“翻到新页面”的硬切收成 assembly-level overlap merge

### 主要产出

- [quality-gate-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/quality-gate-state.json)
- [validate_chapter01_quality_gate.py](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/validate_chapter01_quality_gate.py)
- [render_chapter01_p09_p10_handoff_merge.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_p09_p10_handoff_merge.sh)
- [render_chapter01_story_spine_preview.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_story_spine_preview.sh)
- [chapter-01-p09-p10-handoff-merge-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-p09-p10-handoff-merge-v1.mp4)
- [chapter-01-p09-p10-handoff-merge-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-p09-p10-handoff-merge-v1.metadata.json)
- [chapter-01-story-spine-preview-v32.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v32.mp4)
- [chapter-01-story-spine-preview-v32.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v32.metadata.json)

### 核心变化

- 这轮先没有直接继续拼新总装，而是先把 `T12` 的第一版硬门修正成可执行口径：
  - `story_spine_current` 现在先承担 `public preview` 的结构化放行门
  - 它要求 `semantic / continuity / directors-room / shot contract / reference lock / clip QC / assembly QC / delivery sync` 这些核心步骤必须是真正 `PASSED`
  - `first_frame / image_qc / paper_cut / audio_contract` 这些 strict-backfill 证据如果还没补齐，就继续保留成下一层债务，不再假装已经全过
- 这轮也顺手修掉了一个实际会让 merge 失真的脚本 bug：
  - 旧 merge 脚本按 `format duration` 算 `xfade offset`
  - 但 `P09` 的 `audio duration` 长于 `video stream duration`
  - 结果淡化点会落到视频流结尾之后，第二段实际上接不进来
  - 现在已统一改成按第一条视频流时长计算 offset
- 在 gate 可执行、merge 逻辑也修正之后，这轮真正推进进完整故事入口的是：
  - `P07 -> P08 overlap merge handoff`
  - `P09 -> P10 overlap merge handoff`
  - `story spine current = v32`

### 当前结论

- 这轮真正闭环的，不只是又多了一条 merge clip，而是：
  - `quality-gate preview current` 现在已经能真实通过
  - `P09 -> P10` 的 viewer-visible hard cut 已经继续推进到完整故事入口
  - `chapter-01-story-spine-preview-current.mp4` 已切到 `v32`
- `T11` 仍不改成 `DONE`。当前只是又关掉了一处真实进了完整故事入口的 continuity bug，并把 gate 规则从空壳收成可执行；`P05 -> P06 -> P07` 的 strict-backfill 和 `P10 -> P11` 的后续复审仍继续。

## Version `v1.35`

- 日期：`2026-04-05`
- 阶段：`W11 / P07-P08 handoff merge recovery 传导`
- 目标：继续按 viewer-visible continuity 复审完整故事入口，不重开 `P08` 模型，也不把 `P07` 尾巴重复塞回 part 级 current，只把 `P07 -> P08` 那刀还像“新页面”的硬切收成 assembly-level overlap merge

### 主要产出

- [render_chapter01_p07_p08_handoff_merge.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_p07_p08_handoff_merge.sh)
- [render_chapter01_story_spine_preview.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_story_spine_preview.sh)
- [chapter-01-p07-p08-handoff-merge-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-p07-p08-handoff-merge-v1.mp4)
- [chapter-01-p07-p08-handoff-merge-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-p07-p08-handoff-merge-v1.metadata.json)
- [chapter-01-story-spine-preview-v31.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v31.mp4)
- [chapter-01-story-spine-preview-v31.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v31.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮不是继续抽象讨论“P07 -> P08 有没有点跳”，而是直接回看片证据后确认：
  - `P07` 结尾的暖色旧桌面还在
  - `P08` 开头虽然已经做过 `headtrim`
  - 但放回完整故事入口里，暖桌面还是会硬切到白色规则厅，观感更像“开了新页面”
- 因此这轮不回退到重开 `P08` 模型，而是选择更符合装配层职责的 recovery：
  - 保持 `part-07 current` 和 `part-08 current` 不变
  - 新增 `chapter-01-p07-p08-handoff-merge-v1.mp4`
  - 用 `0.35s` 的 video/audio overlap merge，把暖桌面轻溶到规则厅
- 这次修复当前先真实推进到完整故事入口：
  - `story spine current` 已切到 `chapter-01-story-spine-preview-v31.mp4`
  - `review master` 继续保持 `chapter-01-vertical-slice-master-v28-current.mp4` 不变，因为它本来就不含 `P08`

### 当前结论

- 这轮真正闭环的是：`P07 -> P08` 那处还像“新页面”的 hard cut，已经被收成完整故事入口里的 `overlap merge handoff`。
- `part-07 current` 和 `part-08 current` 这轮都不重开；当前 fix 的职责是 full-story assembly continuity，不是假装 part 级内部都需要一起重做。
- `T11` 仍不改成 `DONE`。当前只是又关掉了一处真实推进进完整故事入口的 viewer-visible continuity bug；active lane 仍继续回到 `P05 -> P06 -> P07` 主线观察。

## Version `v1.33`

- 日期：`2026-04-05`
- 阶段：`W11 / P08 head-trim recovery 传导`
- 目标：继续按 viewer-visible continuity 复审 `P07 -> P08`，不重开模型，只把 `P08 / E09` 那段会把规则投影室读成“新模块加载”的空白建立位收短

### 主要产出

- [render_chapter01_part8_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part8_delivery.sh)
- [part-08-rule-projection-room-delivery-v2-headtrim.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-08-rule-projection-room-delivery-v2-headtrim.mp4)
- [part-08-rule-projection-room-delivery-v2-headtrim.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-08-rule-projection-room-delivery-v2-headtrim.metadata.json)
- [chapter-01-story-spine-preview-v29.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v29.mp4)
- [chapter-01-story-spine-preview-v29.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v29.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮先没有盲动，而是继续按 `editor` 方式复审 `P07 -> P08` 和 `P09 -> P10`：
  - `P07 -> P08` 的 viewer-visible 问题，不在结构本身，而在 `P08 / E09` 的空白规则厅建立略久
  - `P09 -> P10` 目前更像必要的公共空间建立，不属同类“空白建立过长”
- 这轮先做了两个 `P08` 头切试片：
  - `0.6s` 改善不明显
  - `1.0s` 能把空白建立收短，同时还保留足够的规则厅建立位
- 因此这轮正式采用 `1.0s` 的 `TRIM_HEAD` recovery，而不是重开模型：
  - `part-08 current` 收成 `part-08-rule-projection-room-delivery-v2-headtrim.mp4`
  - 规则厅仍保留短建立，再接模型 overlay 和序列员 07 的立场短句
  - `P07` 的暖房间余波能更顺地落到制度压力里，不再更像“新模块加载”
- 这次修复已经真实推进进完整故事入口：
  - `part-08 current` 已切到 `v2 headtrim`
  - 完整故事入口升级到 `chapter-01-story-spine-preview-v29.mp4`
  - `review master` 继续保持 `chapter-01-vertical-slice-master-v27-current.mp4` 不变，因为它本来就不含 `P08`

### 当前结论

- 这轮真正闭环的是：`P07 -> P08` 那处会把规则投影室读成“新页面 / 新模块”的空白建立过长问题，已经真修进 `part -> story spine -> preview current`。
- `P10 / F01` 这轮复审后先保持不动。它仍在 `3-4s` 的 shot contract 范围内，不值得为了“想再顺一点”去误开新 trim。
- `T11` 仍不改成 `DONE`。当前只是又关掉了一处真实进了总装链的 continuity bug；active lane 还是回到 `P05 -> P06 -> P07` 主线继续观察。

## Version `v1.32`

- 日期：`2026-04-05`
- 阶段：`W11 / P07 warm-ingress recovery 传导`
- 目标：继续按 `P06 -> P07` 的 continuity 复审 current，不重开模型，只把 `P07 v3` 那刀裁过头的开场入口收回来，让观众先知道我们走进了沉默练习室，再落到旧档案桌面

### 主要产出

- [render_chapter01_part7_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part7_delivery.sh)
- [part-07-silent-practice-room-delivery-v4-warm-ingress.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-07-silent-practice-room-delivery-v4-warm-ingress.mp4)
- [chapter-01-story-spine-preview-v28.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v28.mp4)
- [current-part-repair-contracts.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/current-part-repair-contracts.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮抓到的不是“想再优化一下”的小意见，而是一个已经会影响剧情读法的 continuity 问题：
  - `P07 v3 head trim` 开得太狠
  - 开场几乎立刻就落到旧档案桌面
  - `S01` 原本该承担的“走进沉默练习室、气氛先慢下来”那一拍被裁掉太多
- 这轮没有误把问题推回模型重开，而是继续走更省、更准的 `editor-level trim recovery`：
  - 在 `render_chapter01_part7_delivery.sh` 里把头切从 `3.2s` 改成 `2.4s`
  - `part-07 current` 收成 `part-07-silent-practice-room-delivery-v4-warm-ingress.mp4`
  - 先保留一小段暖房间入口，再落到旧档案桌面
- 这次修复已经真实推进进当前完整故事入口：
  - `part-07 current` 切到 `v4 warm-ingress`
  - 完整故事入口升级到 `chapter-01-story-spine-preview-v28.mp4`
  - `review master` 维持 `chapter-01-vertical-slice-master-v27-current.mp4` 不变，因为它本来就不含 `P07`

### 当前结论

- 这轮真正闭环的是：`P07` 开场那处会把“走进练习室”读成“直接又切一张桌面信息页”的过裁问题，已经真修进 `part -> story spine -> preview current`。
- `T11` 仍不改成 `DONE`。当前只是又关掉了一处真实进了总装链的 continuity bug；active lane 还是回到 `P05 -> P06 -> P07` 主线继续观察。

## Version `v1.31`

- 日期：`2026-04-05`
- 阶段：`W11 / P09 localized-ui recovery 传导`
- 目标：不重开模型，直接把 `P09 / E13` 里还会抢第一眼的英文伪 UI 收掉，让这一拍重新回到中文 world-in 口径

### 主要产出

- [render_chapter01_part9_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part9_delivery.sh)
- [part-09-evidence-freeze-team-split-delivery-v4-localized-ui.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-09-evidence-freeze-team-split-delivery-v4-localized-ui.mp4)
- [chapter-01-story-spine-preview-v27.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v27.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮抓到的是一个真实 viewer-visible 问题，不是文稿洁癖：
  - `P09 / E13` 源 clip 里还露着英文伪 UI
  - 第一眼会先看到 `Evidence Permission Panel...` 这类旧字样
  - 这已经和 current 的中文 world-in 口径直接打架
- 这轮没有误把问题推回模型重开，而是直接走更省、更准的 assembly-level recovery：
  - 在 `render_chapter01_part9_delivery.sh` 里给 `E13` 补了中文 world-in overlay
  - `part-09 current` 收成 `part-09-evidence-freeze-team-split-delivery-v4-localized-ui.mp4`
  - 英文伪 UI 不再作为第一可读层抢镜
- 这次修复已经真实推进进当前完整故事入口：
  - `part-09 current` 切到 `v4 localized-ui`
  - 完整故事入口升级到 `chapter-01-story-spine-preview-v27.mp4`
  - `review master` 维持 `chapter-01-vertical-slice-master-v27-current.mp4` 不变，因为它本来就不含 `P09`

### 当前结论

- 这轮真正闭环的是：`P09 / E13` 那个还会把观众拉出戏的英文伪 UI，已经真修进 `part -> story spine`。
- `T11` 仍不改成 `DONE`。当前只是又关掉了一处真实 viewer-visible 画面 bug；active lane 还是回到 `P05 -> P06 -> P07` continuity 主线继续观察。

## Version `v1.30`

- 日期：`2026-04-05`
- 阶段：`W11 / P05 tail-trim refine 传导`
- 目标：继续按 `P05 -> P06` 的 contact-sheet 复审 current continuity，不重开模型，只把 `P05` 尾部那半拍重新站稳的泄气感再收掉，让 cut 更像被异常风直接带进暗层

### 主要产出

- [render_chapter01_part5_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part5_delivery.sh)
- [part-05-probability-corridor-delivery-v5-d02first-tailtrim2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-05-probability-corridor-delivery-v5-d02first-tailtrim2.mp4)
- [chapter-01-story-spine-preview-v26.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v26.mp4)
- [chapter-01-vertical-slice-master-v27-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v27-current.mp4)
- [current-part-repair-contracts.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/current-part-repair-contracts.md)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮不是再开新模型，而是继续沿 `editor-level trim` 往前收：
  - `D04` 从 `2.400000s` 收到 `2.166667s`
  - cut 不再多留那半拍“人又站稳了”的感觉
  - 结尾更停在林澄被异常风带偏、还没回稳的点
- 这次修复已经真实推进到总装链，而不是停在局部 clip：
  - `part-05 current` 切到 `part-05-probability-corridor-delivery-v5-d02first-tailtrim2.mp4`
  - 完整故事入口升级到 `chapter-01-story-spine-preview-v26.mp4`
  - review master 升级到 `chapter-01-vertical-slice-master-v27-current.mp4`
- 这轮判断依然保持保守：
  - `P05 -> P06` 现在比 `v4 tail trim` 更像后果推进
  - 但它仍属于 `PASS WITH NOTES`，不是说这一段以后不用再看
  - active lane 继续留在 `P06 continuity`，下一步还是复审 `P05 -> P06 -> P07`

### 当前结论

- 这轮真正闭环的是：`P05` 尾部那处还会泄气的半拍，已经不只在审片备注里指出，而是已经真修进 `part -> story spine -> master`。
- `T11` 仍不改成 `DONE`。当前只是把 `P05 -> P06` 这条链再收紧了一刀；chapter-01 依然整体 `PASS WITH NOTES`，后面还要继续按同一套 workflow 审 active lane 的 continuity 和剩余 viewer-visible 问题。

## Version `v1.29`

- 日期：`2026-04-05`
- 阶段：`W11 / P06 E03-E04 清晰度热修`
- 目标：不只让 `P06` 有声音，而是把已经闭环的两句短线继续收成更清楚、更像孩子一遍能听懂的人话，同时把 source-of-truth 里残留的旧句一起清干净

### 主要产出

- [render_chapter01_part6_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part6_delivery.sh)
- [part-06-dark-layer-interface-delivery-v8-voiceclarity.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-06-dark-layer-interface-delivery-v8-voiceclarity.mp4)
- [chapter-01-story-spine-preview-v25.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v25.mp4)
- [chapter-01-vertical-slice-master-v26-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v26-current.mp4)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮不是重新发明 `P06` 说什么，而是把已经闭环的两句短线收得更清楚：
  - `E03` 当前收成：`第四条路回来了。这条路叫风暴听译者。`
  - `E04` 当前收成：`别只听最大声那条。`
- 这次不只改了 part 输出，还顺手把 source-of-truth 里会误导后续生产的旧句一起清掉：
  - `storyboard-script.md` 的 `P06/S04` 详细段落已改成 current 句子
  - `shot-list.md` 的 `P06/E03-E04` 执行表和详细镜头说明已改成 current 句子
  - `voice-script.md` 的 `part-06 current` 说明已同步到 `v8`
- 这次修复已经继续传导到 chapter 级 current：
  - 完整故事入口升级到 `story spine v25`
  - review master 升级到 `v26-current`
  - `part-06-current / chapter-01-story-spine-preview-current / chapter-01-master-current` 已同步切到新版本
- 仓库外 `faster-whisper` 粗转写这轮仍只当辅助抽检，不当唯一验收：
  - `P06` 当前可抓到：`第四條路回來了,這條路叫風暴停`
  - `P06` 当前可抓到：`別之聽最大聲納條`
  - `P07` 当前仍可抓到：`你聽不見,不一定是因為他不存在 / 也可能是因為你前面太吵了`
  - 逐字仍不完美，但已经足够说明 `P06` 这两句骨架比上一版更容易被机器和人一起接住

### 当前结论

- 这轮真正闭环的是：`P06` 不只“终于有声了”，而且 current 短线已经进一步收成更清楚的人话。
- `T11` 仍不改成 `DONE`。chapter-01 还是 `PASS WITH NOTES`，因为 active lane 仍在 `P05 -> P06 -> P07` continuity 长观察，不是因为这轮热修还没进总装。
- 这轮下一步最该做的是：继续按主质检流程复审 `P05 -> P06 -> P07` 的 viewer-visible continuity，并继续把发现的新问题按 `part -> story spine -> master` 的顺序就地修掉。

## Version `v1.28`

- 日期：`2026-04-05`
- 阶段：`W11 / P06 E03-E04 有声闭环`
- 目标：不再让 `P06` 保留“文稿里已经承诺有系统确认和旧录音短线，但 current part 里还是静音氛围位”的断点，而是把这两拍真的推进到 `part -> story spine -> master`

### 主要产出

- [render_chapter01_part6_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part6_delivery.sh)
- [part-06-dark-layer-interface-delivery-v7-voiceclosure.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-06-dark-layer-interface-delivery-v7-voiceclosure.mp4)
- [chapter-01-story-spine-preview-v24.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v24.mp4)
- [chapter-01-vertical-slice-master-v25-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v25-current.mp4)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮先把 `P06` 的根因断点补上了：
  - `E03` 现在真实落系统确认：`隐藏路径已恢复：风暴听译者。`
  - `E04` 现在真实落婆婆旧录音短线：`别只听最大声的那条。`
  - 两拍都一起进了 `part-06 v7`
- 这次不是只补声音层，还顺手做了轻量 viewer-visible 锚点：
  - `E03` 增加路径恢复文字锚点
  - `E04` 增加旧录音短句锚点
  - 这样孩子第一次看就算没完全听清，也不会错过关键意思
- 这次修复已经继续传导到 chapter 级 current：
  - 完整故事入口升级到 `story spine v24`
  - review master 升级到 `v25-current`
  - `part-06-current / chapter-01-story-spine-preview-current / chapter-01-master-current` 已同步切到新版本
- 仓库外 rough STT 这轮只承担了“确认有人声层已经进 current”的辅助作用：
  - 它对本地 macOS 中文 TTS 的逐字识别不稳定
  - 所以这轮不把机器逐字稿当唯一验收，而以真实装配链闭环和可见锚点同步为准

### 当前结论

- 这轮真正闭环的是：`P06` 不再是“文稿承诺有声、成片还是静音氛围位”的断点。
- `T11` 依然不改成 `DONE`。chapter-01 还是 `PASS WITH NOTES`，因为 active lane 仍在 `P05 -> P06 -> P07` continuity 长观察，不是因为 `P06` 这一拍还没推进到总装。
- 这轮下一步最该做的是：继续按主质检流程复审 `P05 -> P06 -> P07` 的 viewer-visible continuity，并继续把发现的新问题按 `part -> story spine -> master` 的顺序就地修掉。

## Version `v1.27`

- 日期：`2026-04-05`
- 阶段：`W11 / P09-P10 baked-audio 真闭环`
- 目标：不再把 `P09 / P10` 的旧 speaking audio 债务停在“模板已经改了、页面也写了、但成片还没跟上”的中间态，而是把它们真正推进到 `source clip -> part -> story spine -> master`

### 主要产出

- [shot-ch01-p09-s03-evidence-freeze-intervention-viduq3-s2v-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p09-s03-evidence-freeze-intervention-viduq3-s2v-v3.mp4)
- [shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.mp4)
- [part-09-evidence-freeze-team-split-delivery-v3-overlaycleanup.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-09-evidence-freeze-team-split-delivery-v3-overlaycleanup.mp4)
- [part-10-free-echo-platform-delivery-v5.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v5.mp4)
- [chapter-01-story-spine-preview-v23.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v23.mp4)
- [chapter-01-vertical-slice-master-v24-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v24-current.mp4)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮不再只停在 `P10/S03` 上游模板清理，而是把两条最明确的 speaking debt 真的重生了：
  - `P09 / S03` 现在能在 source clip 与 part-level current 里读到：`后来补上的东西 / 不能当最早那份证据`
  - `P10 / S03` 现在能在 source clip 与 part-level current 里读到 current 短线骨架：`这条路不是没有 / 可现在不能先放到大家前面`
- 这次不是 docs-only：
  - `part-09 v3` 已重渲
  - `part-10 v5` 已重渲
  - 完整故事入口已重装到 `story spine v23`
  - review master 已重装到 `v24-current`
  - 两条 current hub 也已同步切到新版本
- 仓库外 `faster-whisper` 粗转写这轮不再只承担“定位债务”，而是真正承担了“闭环后验收”：
  - source clip 复核通过
  - part-level current 复核通过
  - 因此 `P09 / P10` 这组最明确的旧 baked-audio 债，不再继续停留在 current 主链里

### 当前结论

- 这轮真正闭环的是：`T08` 里最明确、最 viewer-visible 的 speaking debt，已经完成 `source clip -> part -> story spine -> master` 真传导，不再只是页面和文稿先变了。
- 这轮依然保留的边界是：chapter-01 还不能误报成“全部完成”。active lane 仍回到 `P05 -> P06 -> P07` continuity 观察，`T11` 也还要继续审计后续发现的问题有没有真进总装。
- 这轮下一步最该做的是：继续按同一条规则做主线质检循环，发现 viewer-visible 问题就地修复，再继续复审，不让“source of truth 已修、当前入口却没跟上”的情况再长回来。

## Version `v1.26`

- 日期：`2026-04-05`
- 阶段：`T08 / 本地 rough STT 复审与 P10 上游模板清理`
- 目标：不给“哪些旧同步音轨还在拖 current 后腿”继续停在猜测层，而是先用低成本本地粗转写把债务定位清楚，再把最容易反复长回来的 `P10/S03` 旧模板统一清掉

### 主要产出

- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮先把仓库外的 `faster-whisper` 粗转写检查路跑通了，终于能低成本核对“哪些旧同步音轨还在拖 current 后腿”，不再只靠主观听感来回猜。
- 当前 rough STT 先给出一条足够能指导下一步生产的判断：
  - `P05` 只听到一记很短的风声反应，先记观察位。
  - `P06` 没抓到可辨识对白。
  - `P07 / P11` 当前音轨大体还算顺，先不重开。
  - `P09 / P10` 仍能听到旧 baked-audio 口径，已经成为 `T08` 眼下最明确的声音债务。
- 顺着这条检查，确认 `P10 / S03` 的 30 份正式重生模板还都残留旧句 `如果高概率已经证明答案，你凭什么让城市承担低概率代价？`；这轮已统一改成和 current 一致的短线：`这条路不是没有。可现在不能先放到大家前面。`
- 这次没有新增 `part delivery / story spine / master`。所以它只算 source-of-truth 与上游模板清理，不算总装推进。

### 当前结论

- 这轮真正闭环的是：`T08` 终于从“知道还没全改完”推进到“已经能更准确定位哪几段旧音轨还在拖后腿”，同时把 `P10 / S03` 这条最会反复长回来的坏模板从上游统一清掉。
- 这轮继续维持的硬边界是：只要没有新的 `part -> story spine -> master`，就不能把这次清理说成成片又往前推进了一轮。
- 这轮下一步最该做的是：继续优先盯 `P09 / P10` 的 baked-audio 债务，找到能真正进 `part-level current` 的最小闭环。

## Version `v1.25`

- 日期：`2026-04-05`
- 阶段：`W11 / P07 head-trim continuity 传导`
- 目标：继续按 active lane 收 `P06 -> P07` 的 same-space handoff，不重开模型，先用 editor-level trim 判断能不能把“像换页面”的感觉再压下去

### 主要产出

- [part-07-silent-practice-room-delivery-v3-headtrim.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-07-silent-practice-room-delivery-v3-headtrim.mp4)
- [chapter-01-story-spine-preview-v22.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v22.mp4)
- [part-07-silent-practice-room-delivery-v3-headtrim.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-07-silent-practice-room-delivery-v3-headtrim.metadata.json)
- [chapter-01-story-spine-preview-v22.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v22.metadata.json)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮没有重开 `P07` 模型，而是先用 editor 测试验证：`1 秒` 头切基本没救，`3.2 秒` 头切则能明显让 `P06` 的桌面波形更直接接进 `P07` 的旧档案桌面。
- 这次真实进链的是：`part-07 v3 head trim -> story spine v22`。
- `review master` 这轮继续保持 `v23-current`，而且这里明确写清：它本来就不含 `P07`，所以这次修补不再误报成“也已经进了 review subset”。
- `P05 v4`、`P09 v3`、`P10 v5`、`P11 v4` 这些之前已经进 current 的修补，这轮也继续保留在相应链路里，没有回弹。
- `T08 / T11` 继续保持 `IN PROGRESS`。当前闭环的是一处真实 continuity trim，不代表所有旧同步音轨对白都已经换新。

### 当前结论

- 这轮真正闭环的是：`P06 -> P07` 那处最像“新页面建立位”的开头被收掉后，完整故事入口读起来更像同一条追索后果。
- 这轮同步补清的是：`story spine current` 和 `review master` 的职责边界继续要分开写，不能因为 `v23-current` 版本号更大，就误把它当成包含 `P07` 的完整故事 current。
- 这轮还没闭环的是：`P05 -> P06 -> P07` 的长观察，以及所有还被旧同步音轨卡住的对白位。

## Version `v1.24`

- 日期：`2026-04-05`
- 阶段：`W11 / P09 overlay cleanup 传导`
- 目标：继续按“只有进总装才算有效”的硬标准推进，把 `P09` 冻结提示里还像回执单的可见文案真正推进到 `part -> full-story current`，并同时把 review subset 刷到最新 current 口径

### 主要产出

- [part-09-evidence-freeze-team-split-delivery-v3-overlaycleanup.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-09-evidence-freeze-team-split-delivery-v3-overlaycleanup.mp4)
- [chapter-01-story-spine-preview-v21.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v21.mp4)
- [chapter-01-vertical-slice-master-v23-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v23-current.mp4)
- [render_chapter01_part9_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part9_delivery.sh)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮真正新修进总装的，是 `P09` 那层 viewer-visible 冻结提示：不再像在读一张回执单，而是收成 10-12 岁孩子也能立刻听懂的人话。
- 这次真实进链的是 `part-09 v3 -> story spine v21`。以后再审 `P09`，默认先看完整故事入口，不再拿 review subset 误代替它。
- `review master` 这轮也刷新到了 `v23-current`，但这里只把边界写清楚：它继续只是 vertical-slice subset，不含 `P09`，所以不再误报“P09 这次也已经进了 review master”。
- `P05 v4`、`P10 v5`、`P11 v4` 这些之前已经进 current 的修补，这轮也继续保留在相应链路里，没有在升版本时回弹成旧口径。
- `T08 / T11` 继续保持 `IN PROGRESS`。当前闭环的是一处真实 viewer-visible 装配问题，不代表所有旧同步音轨对白都已经换新。

### 当前结论

- 这轮真正闭环的是：`P09` 一处会直接被观众看到的冻结提示，已经从 `part current` 传到当前完整故事入口。
- 这轮同步补清的是：`review master` 和 `full-story current` 不是一回事；以后再写状态，不再把不含 `P09` 的 subset 误写成 `P09` 也已进链。
- 这轮还没闭环的是：`P05 -> P06 -> P07` 的 continuity 长观察，以及所有还被旧同步音轨卡住的对白位。

## Version `v1.23`

- 日期：`2026-04-05`
- 阶段：`W11 / P05-P06 continuity tail-trim 传导`
- 目标：不重开模型，直接用 editor-level trim 把 `P05 -> P06` 最明显的 viewer-visible 断页感继续收紧，并把这次修补真实推进到 `part -> story spine -> master`

### 主要产出

- [part-05-probability-corridor-delivery-v4-d02first-tailtrim.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-05-probability-corridor-delivery-v4-d02first-tailtrim.mp4)
- [chapter-01-story-spine-preview-v20.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v20.mp4)
- [chapter-01-vertical-slice-master-v22-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v22-current.mp4)
- [render_chapter01_part5_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part5_delivery.sh)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这轮没有重开模型，而是直接把 `P05 current` 从旧的 `D02-first` recovery 再往前推一刀：只保留真正服务 continuity 的尾段，让 cut 停在异常风把林澄往下一层带走的听风位，不再停在旧的正面定住 pose。
- 这次不是只停在 `P05` 单条 part：`part-05 current` 已切到 `v4-d02first-tailtrim`，并继续重装到 `story spine v20` 与 `master v22-current`。
- `P06 -> P07` 这轮继续维持 `PASS WITH NOTES`，不把 stylized handoff 误报成新 blocker；下一步仍是继续观察更细的 trim / bridge 空间，而不是整段重开模型。
- `T08 / T11` 继续保持 `IN PROGRESS`。当前真正闭环的是这次 continuity trim 已经进了总装；旧同步音轨对白还不能假装已经全部换新。

### 当前结论

- 这轮真正闭环的是：`P05 -> P06` 最明显那处 viewer-visible 断页感，已经从 `P05 current` 继续传到 chapter 级完整故事入口与 review master。
- 这轮继续保持的硬边界是：只停在文稿、页面或公开镜像的修正，仍然不算总装完成。
- 这轮还没闭环的是：`P05 -> P06 -> P07` 的长观察，以及所有还被旧同步音轨卡住的对白位。

## Version `v1.22`

- 日期：`2026-04-05`
- 阶段：`W11 / P10 viewer-visible 文案传导`
- 目标：继续按“只有进总装才算有效”的硬标准推进，把 `P10` 自由回响台里最明确的一处 viewer-visible 文件 / UI 腔问题真正推进到 `part -> story spine -> master`

### 主要产出

- [part-10-free-echo-platform-delivery-v5.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v5.mp4)
- [chapter-01-story-spine-preview-v19.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v19.mp4)
- [chapter-01-vertical-slice-master-v21-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v21-current.mp4)
- [render_chapter01_part10_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part10_delivery.sh)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P10` 这轮继续收掉了观众一眼就会看到的文件 / UI 腔：`回响台 / 先把想说的话摆明白`、`这条路不是没有。可现在不能先放到大家前面。`、`这座城可以先给建议，但不能替还没看清的孩子先把路关掉。`
- 这次不是只停在 `P10` 单条 part：`part-10 current` 已切到 `v5`，并继续重装到 `story spine v19` 与 `master v21-current`。
- 前一轮推进进总装的 `P11 v4` 结果层口径，这轮也继续保留在新的 chapter 级入口里，没有在升版本时被重新冲回旧文案。
- `T11` 继续保持 `IN PROGRESS`。当前已经能明确说“真进了总装”的，是 `P10 v5` 这处可见文案修正；其余还停在文稿、页面或公开镜像层的项，仍只能算 `docs-only / not counted`。

### 当前结论

- 这轮真正闭环的是：`P10` 自由回响台里一处明确的 viewer-visible 文案问题，已经从 part 继续传到 chapter 级完整故事入口与 review master。
- 这轮继续维持的硬边界是：以后凡是只停在文稿、页面或公开镜像的修正，一律不算总装完成。
- 这轮还没闭环的是：`P05 -> P06 -> P07` 的 continuity 长观察，以及所有还被旧同步音轨卡住的对白位。

## Version `v1.21`

- 日期：`2026-04-05`
- 阶段：`W11 / 总装有效性审计 + P11 结果层传导`
- 目标：先把“只有进总装才算有效”写回 source of truth，再把这一轮最明确还停在可见层的 `P11` 结果公告口径真正推进到 `part -> story spine -> master`

### 主要产出

- [part-11-midnight-choice-return-delivery-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-11-midnight-choice-return-delivery-v4.mp4)
- [chapter-01-story-spine-preview-v18.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v18.mp4)
- [chapter-01-vertical-slice-master-v20-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v20-current.mp4)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P11` 结果层里还偏文件腔的可见 overlay 已改成更直接的世界内口径，不再让孩子在最后结果公告这一步突然像在看表单回执。
- 这次不是只停在 `P11` 单条 part：`part-11 current` 已切到 `v4`，并继续重装到 `story spine v18` 与 `master v20-current`。
- `v1.19-v1.20` 这两轮虽然继续收了文稿、页面和公开镜像，但因为当时没有新的 `part delivery / story spine / master`，现在统一降级回 `docs-only truth sync`，不再被描述成“总装又往前推进了一轮”。
- `T08` 仍继续保持 `IN PROGRESS`。当前真正进成片的，只是已经明确传到装配链的那部分；旧同步音轨对白还不能假装全部好了。

### 当前结论

- 这轮真正闭环的是：`P11` 结果层一处明确的 viewer-visible 口径，已经从脚本和 part 传到 chapter 级完整故事入口与 review master。
- 这轮同步收紧的是：以后凡是只停在文稿、页面或公开镜像的修正，一律不再算总装完成，只能记成 `docs-only / not counted`。
- 这轮还没闭环的是：`P05 -> P06 -> P07` 的 continuity 长观察，以及所有还被旧同步音轨卡住的对白位。

## Version `v1.20`

- 日期：`2026-04-05`
- 阶段：`T10 / 页面可见口径继续收口`
- 目标：继续按主 workflow 做“边审边改”，把当前主入口和五份主文稿里还会让人出戏的旧词继续收掉，同时补齐公开镜像缺口，确保页面读到的就是最新主稿

### 主要产出

- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [product-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/product-script.md)
- [episode-onscreen-copy.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/episode-onscreen-copy.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `master / script / product / onscreen / shot-list / 资产总览页` 这轮继续收掉了一批页面可见旧词：
  - `主位`
  - `点头`
  - `扛下`
  - `不予开放`
  - `原始性风险`
- `P01` 页面卡片、角色说明和当前入口卡上的可见描述，已经全部改到和最新主稿一致的说法，不再一边说“已经整改”，一边还挂着旧词。
- 公开镜像这轮补齐了 `product-script.md` 与 `episode-onscreen-copy.md` 两份正文入口，资产总览页现在可以和另外三份文稿一样，直接读到这两份最新主稿。
- 这轮没有误报“所有对白已经全部进成片”。`T08` 继续保持 `IN PROGRESS`，因为已有同步音轨的旧对白还没全部重做。

### 当前结论

- 这轮真正闭环的是：页面当前能看到的主入口、主文稿和状态源，已经不再一边更新、一边残留旧口径。
- 但这轮没有新的 `part delivery / story spine / master`，所以现在回看，它只能算 `docs/page truth sync`，不算总装推进。
- 这轮还没闭环的是：旧同步音轨对白的继续传导，以及 `P05 -> P06 -> P07` 的 continuity 长观察。

## Version `v1.19`

- 日期：`2026-04-05`
- 阶段：`T10 / 文稿兑现边界收口`
- 目标：继续按主 workflow 做“边审边改”，把 `分镜脚本 / 趣味增强 / 产品稿 / 上屏文案 / 资产总览页` 的 current / 后补边界统一到同一套 source of truth，不再让候选层冒充已上线

### 主要产出

- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [product-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/product-script.md)
- [episode-onscreen-copy.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/episode-onscreen-copy.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `script / storyboard / product / onscreen` 现在都明确写清了三层：
  - 哪些趣味层已经进 current
  - 哪些还只是后补候选
  - 哪些当前不进主线承诺
- `shot-list.md` 去掉了指向不存在文件的趣味资产引用，避免执行链继续被坏入口带偏。
- 资产总览页不再只展示三份剧本文稿；现在会同时展示 `整集总脚本 / 分场剧本 / 分镜脚本 / 产品脚本 / 上屏文案` 五份当前镜像。
- 这轮没有误报“全部完成”。`T08` 仍保持 `IN PROGRESS`，因为文稿链的最新口径还没有自动吃进所有旧同步音轨。

### 当前结论

- 这轮真正闭环的是：文稿链和页面展示层终于在“current 已实现 / 后补候选”这件事上说同一种话。
- 但这轮没有新的 `part delivery / story spine / master`，所以它现在也只算 `docs-only truth sync`，不算总装推进。
- 这轮还没闭环的是：所有 baked audio 的对白传导，以及 `P05 -> P06 -> P07` 的 continuity 长观察。

## Version `v1.18`

- 日期：`2026-04-05`
- 阶段：`T08 / P01 current hotfix 传导`
- 目标：先修掉用户刚指出的两个长期残留 bug，再把这次 `P01` 热修继续传导到 `part / story spine / master / 资产总览页`，同时不打断当前 `P06` continuity 主 workflow

### 主要产出

- [part-01-future-bay-task-dock-delivery-v31.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v31.mp4)
- [chapter-01-story-spine-preview-v17.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v17.mp4)
- [chapter-01-vertical-slice-master-v19-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v19-current.mp4)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)

### 核心变化

- `P01 / S04` 旧的 `别站队 / 先别下结论` baked line 已从 current 退下，改成和最新主稿一致的直白口径。
- `P01 / S07` 不再误用工作台错片，也不再把 `S04` 的半句话串进启航镜头；现在先看到固定小队同场，再接航线点亮。
- `part-01 current` 已升级到 `v31`，chapter 级 `story spine` 与 `review master` 也已经吃到这次热修，不再只有单条 clip 改对。
- active lane 仍保持在 `P06` continuity 观察位；这轮是 `P01` 的定向 hotfix，不是假装 chapter-01 所有对白问题都已一次性清空。

### 当前结论

- 这轮真正闭环的是：`P01` 两个 viewer-blocking bug 已从 current clip 一路修到 chapter 级入口。
- 这轮还没有闭环的是：`T08` 整体。已有 baked audio 的旧对白位仍需继续逐段清理，不能因为 `P01` 热修完成就误报“全片台词都好了”。

## Version `v1.17`

- 日期：`2026-04-04`
- 阶段：`T08 / 装配传导与 continuity 快检`
- 目标：把 `P01 / P09 / P10 / P11` 的人话化整改从文稿链继续推进到 current 成片入口，同时复核 `P05 -> P06 -> P07` 的中段 continuity 是否还能稳住同一条后果链

### 主要产出

- [part-01-future-bay-task-dock-delivery-v30.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v30.mp4)
- [part-09-evidence-freeze-team-split-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-09-evidence-freeze-team-split-delivery-v2.mp4)
- [part-10-free-echo-platform-delivery-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v4.mp4)
- [part-11-midnight-choice-return-delivery-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-11-midnight-choice-return-delivery-v3.mp4)
- [chapter-01-story-spine-preview-v16.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v16.mp4)
- [chapter-01-vertical-slice-master-v18-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v18-current.mp4)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- `P01 / P09 / P10 / P11` 已重新渲染，把最容易跳戏的口号腔、系统腔和备注腔先从装配层里清掉。
- `P10` 的回响台立场卡已改成更像孩子会说的话，不再把高潮写成概念海报。
- `P11` 的真实 clip 仍保留，但现在会强制叠新的世界内 overlay，不再直接把旧 baked 口径裸露给 current。
- `story spine v16` 与 `master v18-current` 已重新装配，chapter 级入口不再落后于这轮 part-level 更新。
- `P05 -> P06` 与 `P06 -> P07` 已做 transition contact-sheet 复审：
  - `P05 -> P06` 当前可判 `PASS WITH NOTES`
  - `P06 -> P07` 当前可判 `PASS WITH NOTES`
  - 目前都不升格成新的 viewer-blocking 问题

### 当前结论

- 这轮真正闭环的是：`overlay / assembly` 层的人话化传导，已经进入 part、story spine 和 review master。
- 这轮还没有闭环的是：所有带旧同步音轨的对白位。`T08` 仍必须保持 `IN PROGRESS`，不能误报成“全片台词都已经换新”。
- active lane 继续保持 `P06` continuity 观察位；下一步优先继续盯“还有哪些段落仍被 baked audio 口径卡住”，而不是重复修已经传导过的 overlay。

## Version `v1.16`

- 日期：`2026-04-04`
- 阶段：`T08 / P05-P07 对白复审继续推进`
- 目标：继续按 `workflow-remediation-todo.md / T08` 逐场复审 `P05 -> P06 -> P07` 的对白，把还在同质化、还像主题说明、还不够像人会当场说出来的话继续收掉

### 主要产出

- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- `林澄` 在 `P05` 不再像在替主题总结，而是更直接地说“我真正会的东西被挤成一小条”这种孩子能立刻听懂的话。
- `序列员 07` 在 `P06` 的反方解释继续收短，保留冷静和立场，但不再说成抽象制度话。
- `回响` 在 `P06/P09` 继续压成“能做什么 / 会快多少 / 代价是什么”的口气，不再有说明书味。
- `风声婆婆` 在 `P06/P07` 去掉了几句看上去有画面、听起来却不像真人会说的话，改成更贴地、更像她本人现场会说出口的表达。
- 这轮仍是文稿链推进，不是假装已经把这些新对白全部烤进现有 `part delivery` 音轨。

### 当前判断

- `T08`：`IN PROGRESS`
  - `P05-P07` 文稿链已经继续收紧。
  - 成片链仍需继续传导。
- `active lane`：`P06 / PASS WITH NOTES`
  - 当前还是先盯 `P05 -> P06 -> P07` continuity，不让对白整改脱离主 workflow 单跑。

### 下一步

- 继续把 `T08` 从 `P05-P07` 文稿链往 `P09 / P10 / P11` 和已有 part-level delivery 传导
- 继续结合中段 continuity 复审，不让角色口气和镜头节奏互相打架

## Version `v1.15`

- 日期：`2026-04-04`
- 阶段：`W11 交付入口纠偏与对白传导状态落账`
- 目标：停止把 `vertical slice master v18` 继续写成 chapter-01 的唯一完整交付入口，同时把“最新人话化对白已经进文稿链、但还没完全烤进成片音轨”这条质量债务正式写回 source of truth 和资产总览页

### 主要产出

- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)
- [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 明确区分了两条 chapter 级入口：
  - `chapter-01-story-spine-preview-v16.mp4`
    - 当前完整故事入口
    - 覆盖 `P01-P12`
    - 时长约 `205.33s`
  - `chapter-01-vertical-slice-master-v18-current.mp4`
    - 当前 review master
    - 只承担 chapter 级 vertical-slice 审片职责
    - 时长约 `157.84s`
- 这轮没有重渲新的 chapter 级 mp4，修的是 `W11` 的交付口径和状态源，避免资产页继续把 review master 冒充成完整故事唯一入口。
- 同步把“最新人话化对白已经回写 `master / script / storyboard / voice` 文稿链，但还没自动传导到所有 part-level delivery 音轨”这条债务正式写进 `asset-manifest.json`、`video-loop-state.json`、`workflow-remediation-todo.md` 和主 HTML。
- 资产总览页顶部现在会同时展示：
  - 当前完整故事入口
  - 当前 review master
  - active lane
  - 对白传导状态

### 当前判断

- `W11`：`DONE WITH NOTES`
  - 对外入口口径已经纠正。
  - 但“文稿已改、成片未完全跟上”这条债务还没结束。
- `T08 对白整改`：`IN PROGRESS`
  - 文稿层已经推进。
  - 成片层仍需继续传导，尤其是 `P01 / P09 / P10 / P11`。

### 下一步

- 继续按 active lane 复审 `P05 -> P06 -> P07` 的 continuity
- 继续把最新对白整改传导到受影响的 part-level delivery 与 chapter current
- 保持“修完就同步 source of truth + 资产页 + 公开预览”这条工作流

## Version `v1.14`

- 日期：`2026-04-04`
- 阶段：`P06 ingress trim recovery 落地`
- 目标：把 `P06 / E01` 从“开头先回到更亮、更空的走廊，再慢慢变暗”的 reset 感，收口成真正承接 `P05` 风异常的连续入口，并把修复同步传导到 `part -> story spine -> master -> preview current`

### 主要产出

- [shot-ch01-p06-s01-dark-layer-ingress-viduq3-i2v-v2-trimmed.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p06-s01-dark-layer-ingress-viduq3-i2v-v2-trimmed.mp4)
- [part-06-dark-layer-interface-delivery-v6-trimmed-ingress.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-06-dark-layer-interface-delivery-v6-trimmed-ingress.mp4)
- [chapter-01-story-spine-preview-v16.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v16.mp4)
- [chapter-01-vertical-slice-master-v18-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v18-current.mp4)
- [render_chapter01_part6_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part6_delivery.sh)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [current-part-repair-contracts.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/current-part-repair-contracts.md)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)

### 核心变化

- `P06` 的问题这次没有继续停在“READABILITY REOPENED”口头判断，而是直接用 `trim recovery` 去掉 `E01` 开头那一拍更亮、更空的走廊 reset。
- 这次修的是 `assembly/editor-level reset`，不是整段重开模型，因此 `E02-E04` 全部保留在线，只把入口第一秒收紧到更像顺着风声进入暗层。
- `part-06 current` 已切到 `delivery v6-trimmed-ingress`，`story spine current` 已切到 `v16`，`chapter master current` 已切到 `v18`。
- 这轮 review 还顺手把 `asset-manifest.json / video-loop-state.json` 的 part delivery 指针按 `current/deliveries` 全量对齐，修掉了 `P01` 还停在旧 `v17`、但 current 实际已经是 `v30` 这种 source-of-truth 滞后。
- active lane 也已经从 `P04` 正式切到 `P06`，后续质量复审不再拿已经收口的 `P04` 继续冒充当前在修的主位。

### 当前判断

- `P06 / E01`：`PASS WITH NOTES`
  - 亮走廊 reset 已被收掉，入口明显更贴近 `P05` 的异常风声 handoff。
  - 但 `P05 -> P06 -> P07` 仍要继续观察是否还需要更细的 `trim / bridge / reorder`。
- `chapter current entry`：`PASS WITH NOTES`
  - 这次修复已经传导到 `part-06 current / story spine v16 / master v18 / preview current`，不再只是单条 clip 层面的局部结论。

### 下一步

- 继续按 current loop 复审 `P05 -> P06 -> P07` 的 continuity
- 如果还有问题，优先继续走 `trim / bridge / reorder`
- 没有新的 viewer-blocking 问题前，不回退到整段模型重开

## Version `v1.13`

- 日期：`2026-04-04`
- 阶段：`P04-P05 bridge recovery 落地`
- 目标：把已经本地复审通过的 `P04 -> P05` 承压 bridge 正式落到 current，不再让 source of truth 和公开预览页继续停在“bridge required”的旧口径

### 主要产出

- [chapter-01-p04-p05-consequence-bridge-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-p04-p05-consequence-bridge-v1.mp4)
- [part-05-probability-corridor-delivery-v3-d02first.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-05-probability-corridor-delivery-v3-d02first.mp4)
- [chapter-01-vertical-slice-master-v17-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v17-current.mp4)
- [chapter-01-story-spine-preview-v15.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v15.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [current-part-repair-contracts.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/current-part-repair-contracts.md)
- [workflow-remediation-todo.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/workflow-remediation-todo.md)

### 核心变化

- 不再让 `P04` 停在“只剩一个 blocker 但还没落 current”的状态，而是把这条承压 bridge 真正装进 official current。
- `P05 current` 不再从更抽象的 `D01` 打开，而是改成 `D02-first` recovery 结构，让 `林澄近景 -> 路径比较节点 -> 风异常反应` 读起来更像同一条后果。
- `D01` 没有被删除；它继续保留为独立资产，但不再作为 current `part-05` 的开门 beat。
- `official master` 已切到 `chapter-01-vertical-slice-master-v17-current.mp4`，`story spine` 已切到 `v15`。
- 这次通过的是 `assembly-level recovery path`，不是宣称以后不需要更强的 native same-space bridge。

### 当前判断

- `P04 -> P05`：`PASS WITH NOTES`
  - 跳页感已明显收紧，当前官方入口不再继续停在“bridge required”。
  - 但 bridge 仍属于 recovery path，未来如果拿到更强 native clip，应优先替换。
- `chapter current entry`：`PASS WITH NOTES`
  - 主仓 current、preview current、`master v17`、`story spine v15` 和 `part-05 current v3-d02first` 应该保持同一口径。

### 下一步

- 回到 chapter-level 质量复审
- 优先继续看 `P06` 的 `READABILITY REOPENED` 和中段 continuity notes
- 保持“发现问题就地修复，再同步 current / preview / source of truth”这条工作流

## Version `v1.07`

- 日期：`2026-04-03`
- 阶段：`P03 人话版 current 同步与预览回写`
- 目标：把已经真实渲染完成的 `P03 v6`、`story spine v37-full`、`chapter master v33-current` 回写到 source of truth 和预览页，不再让总览继续显示旧的 `v36 / v32 / P03 v4`

### 主要产出

- [render_chapter01_part3_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part3_delivery.sh)
- [part-03-archive-hall-pressure-delivery-v6.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-03-archive-hall-pressure-delivery-v6.mp4)
- [chapter-01-story-spine-preview-v37-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v37-full.mp4)
- [chapter-01-vertical-slice-master-v33-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v33-current.mp4)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)

### 核心变化

- `P03 current` 不再停留在旧 `v4/v5` 口径，而是正式切到 `delivery v6`。
- 这轮 `P03` 的变化不是只换一个版本号，而是把大厅里最难懂的几句改成更直白的人话顺序：
  - 林澄先问系统为什么认定她只能走那条 `93%` 的路
  - 父亲更早站出来表明自己在帮女儿争一次申诉机会
  - `序列员 07` 更早报出“今晚归档由我负责”的程序身份
  - `闻夏` 明确点破真正正在输掉的是时间
- 顶部整章入口已切到 `story spine v37-full`，并且不只吃到 `P01 v28 / P02 v5`，也继续吃到新的 `P03 v6`。
- 隐藏的统一审片入口已切到 `chapter master v33-current`，保证主 HTML、current 指针和预览仓库口径一致。
- 这轮也顺手补了新的 cache-busting 版本戳，避免 GitHub Pages 继续让浏览器缓存住旧视频说明。

### 当前判断

- `P03`：`PASS WITH NOTES`
  - 现在第一次看片时，已经更容易听懂：
    - 谁在顶着不签
    - 谁在逼她赶紧签
    - 谁在按时间档案城的流程推进
    - 今晚如果拖过午夜会失去什么
- `chapter current entry`：`PASS WITH NOTES`
  - 顶部整章入口、隐藏 master 入口、`P03 current` 卡片和预览仓库都应统一显示 `v37 / v33 / v6`

### 下一步

- active lane 仍保持在 `P03`
- 优先继续修：
  - `P03`：继续把局部模糊照片感替换成更原生的真实视频表达
  - `P03 -> P04`：继续检查情绪承接是否足够顺
  - 整章：继续保持“改了就立刻进 current / HTML / preview”这条硬规则

## Version `v1.05`

- 日期：`2026-04-03`
- 阶段：`P03 script-first 重开`
- 目标：停止继续在 `P03` 上叠补表面装配，把这段最乱的故事先从剧本层重新讲清

### 主要产出

- [story/script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [story/master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [story/storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [audio/voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [production/shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [production/video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- 不再让 `P03` 继续围着“模糊画面 + 补几句说明字”打转，而是把这段的主冲突重写成清楚的 6 拍主线。
- 重新锁定 `P03` 必须先回答的 4 个问题：
  - 谁不肯签
  - 谁在劝她签
  - 谁在按程序推进
  - 如果今晚来不及会失去什么
- 把父亲前移到 `P03` 正面出场，不再等到后一段才第一次真正成立。
- 把 `序列员 07` 的第一句从抽象制度话改成先报身份、先说明“今晚归档由我负责”。
- 把调查层的职责改成必须直接摊出 `93% 路径 / 家属支持记录 / 午夜锁定后果` 三件硬事实。
- 把 `闻夏` 的作用收成一句清楚判断：现在真正输的是时间，不是气势。
- `video-loop-state.json` 已把 `P03` 当前 gate 回退到 `W2`，后续必须先过脚本和 shot contract，再重开首帧和视频。

## Version `v1.03`

- 日期：`2026-04-03`
- 阶段：`P01 -> P02 承接收口`
- 目标：把 `P02` 的制度话彻底换成第一次看就能懂的人话，并确保这次修复真正贯通到 `P02 current`、顶部整章入口、master current 与总览页

### 主要产出

- [audio/voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [production/shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [story/storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [story/master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [render_chapter01_part2_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part2_delivery.sh)
- [part-02-emergency-entry-check-delivery-v5.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-02-emergency-entry-check-delivery-v5.mp4)
- [chapter-01-story-spine-preview-v31-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v31-full.mp4)
- [chapter-01-vertical-slice-master-v27-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v27-current.mp4)

### 核心变化

- `P02 / B01` 现在不再让观众自己猜“临时观察许可”到底差在哪，而是直接烧进真 clip：
  - `现在你只能进去看、进去问，还不能替她改结果。`
  - `如果今晚帮不了林澄申诉成功，她的人生就会按 93% 匹配的路被锁定。`
- `P02 / B04` 也不再只说“校验通过”，而是继续把后果压实：
  - `你现在能进去看、进去问，也能把申诉提上去。`
  - `如果今晚申诉不成功，林澄的人生还是会按 93% 匹配的路锁定。`
- `P02 / B02-B03` 的系统规则同步去掉制度腔，改成第一次看就能懂的话：
  - `系统觉得哪条路最适合你，资源就会先往那条路走`
  - `如果今晚申诉不成功，午夜一到，那条路就会先锁定`
- 这轮不是只改文案，而是把修复直接贯通进了：
  - `part-02-current.mp4` -> `delivery v5`
  - `chapter-01-story-spine-preview-current.mp4` -> `v31-full`
  - `chapter-01-master-current.mp4` -> `v27-current`

### 当前判断

- `P02`：`PASS WITH NOTES`
  - 当前第一次看片时，更容易直接听懂这条逻辑：
    - `现在能做什么`
    - `现在还不能做什么`
    - `今晚申诉失败到底会发生什么`
- `chapter current entry`：`PASS WITH NOTES`
  - 顶部整章入口已升级到 `story spine v31-full`
  - `P02 v5`、`story spine v31-full` 和 `master v27-current` 已统一吃到这次人话版后果澄清

### 下一步

- active lane 保持在 `P03`
- 优先继续修：
  - `P03`：复审 `C01-C04` 的三方站位与顺序，避免“像几个人突然开始说话”
  - 整章：继续沿 story-first 规则复审后续 parts 的“第一次看是否看得懂”

## Version `v1.02`

- 日期：`2026-04-03`
- 阶段：`P01 -> P02 承接收口`
- 目标：把启航之后的制度门槛从“听过一遍才反应过来”推进到第一眼就能懂的 current 版本，并确保这次修复真正贯通到 `P02 current`、顶部整章入口、master current 与总览页

### 主要产出

- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [voice-first-round-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-first-round-pack.md)
- [render_chapter01_part2_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part2_delivery.sh)
- [part-02-emergency-entry-check-delivery-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-02-emergency-entry-check-delivery-v3.mp4)
- [chapter-01-story-spine-preview-v30-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v30-full.mp4)
- [chapter-01-vertical-slice-master-v26-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v26-current.mp4)

### 核心变化

- `P02 / B01` 不再只靠守望者一句音轨解释，现在直接把最关键的入口规则烧进真 clip：
  - `先别急着去见林澄`
  - `你得先拿到临时观察许可`
  - `现在能做的是进城观察，不是直接替她改结果。`
- `P02 / B04` 也不再只是“过桥去大厅”的漂亮桥接，而是明确压实当前权限边界：
  - `校验通过，可以进入争议档案现场`
  - `但你现在拿到的只是临时观察许可`
  - `下一步你才会真正见到林澄和序列员 07。`
- `P02` 的 current clip 不再是原始裸 probe，已经回写为带制度澄清 overlay 的正式 current 版本：
  - `current/clips/p02-s01-entry-approach-current.mp4`
  - `current/clips/p02-s04-entry-bridge-current.mp4`
- 这轮不是只改文档，而是把修复直接烧进了 `P02 current`，并贯通到：
  - `part-02-current.mp4` -> `delivery v3`
  - `chapter-01-story-spine-preview-current.mp4` -> `v30-full`
  - `chapter-01-master-current.mp4` -> `v26-current`

### 当前判断

- `P02`：`PASS WITH NOTES`
  - 当前第一次看片时，更容易直接接上这条逻辑：
    - `为什么还不能直接去见林澄`
    - `现在拿到的权限到底是什么`
    - `下一步为什么才会进入争议现场`
- `chapter current entry`：`PASS WITH NOTES`
  - 顶部整章入口已升级到 `story spine v30-full`
  - `P02 v3`、`story spine v30-full` 和 `master v26-current` 已统一吃到这次 `临时观察许可` 门槛澄清

### 下一步

- active lane 转到 `P03`
- 优先继续修：
  - `P03`：复审 `C01-C04` 的三方站位与顺序，避免“像几个人突然开始说话”
  - 整章：继续沿 story-first 规则复审后续 parts 的“第一次看是否看得懂”

## Version `v1.01`

- 日期：`2026-04-03`
- 阶段：`P01 开场读懂度修复继续推进`
- 目标：把 `S06/S07` 从“文档里知道该怎么解释，但视频里还没真正说清”推进到第一次看片就能懂的 current 版本，并确保这次修复真正贯通到 `P01 current`、顶部整章入口、master current 与总览页

### 主要产出

- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v24.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v24.mp4)
- [chapter-01-story-spine-preview-v29-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v29-full.mp4)
- [chapter-01-vertical-slice-master-v25-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v25-current.mp4)

### 核心变化

- `P01 / S06` 不再只靠旧 overlay 在镜头外解释。当前正式口径已直接烧进 clip：
  - `林澄还没签确认书`
  - `系统判定：93% 匹配`
  - `如果她今晚不反对，午夜后会自动锁定`
  - `她没有盯着确认书，她在听一段系统没标出来的异常风声`
- `P01 / S07` 不再只是“漂亮启航镜头”，而是明确交代：
  - `你已经接下这项灰银任务`
  - `现在立刻去时间档案城，先拿临时观察许可`
  - `守望者：从现在起，这不是观察任务。这是责任任务。`
- 这轮不是只改文档，而是把修复直接烧进了 `S06/S07 current clip`，并贯通到：
  - `part-01-current.mp4` -> `delivery v24`
  - `chapter-01-story-spine-preview-current.mp4` -> `v29-full`
  - `chapter-01-master-current.mp4` -> `v25-current`
- 同时修掉预览发布脚本的一个隐患：不再用 `git add -A` 把临时垃圾文件一起推上预览仓库

### 当前判断

- `P01`：`PASS WITH NOTES`
  - 当前第一次看片时，已经更容易直接接上这条逻辑：
    - `我是谁`
    - `林澄卡在哪`
    - `如果今晚不反对会发生什么`
    - `为什么现在就要出发`
  - 当前剩余主阻塞已从 `S06-S07` 收缩到 `P01 -> P02` 的承接：启航之后，制度门槛和临时观察许可的压力还要继续保持不断线
- `chapter current entry`：`PASS WITH NOTES`
  - 顶部整章入口已升级到 `story spine v29-full`
  - `P01 v24`、`story spine v29-full` 和 `master v25-current` 已统一吃到这次 `S06/S07` 读懂度修复

### 下一步

- active lane 继续保留在 `P01`
- 优先继续修：
  - `P01 -> P02`：复审启航后立刻进入临时观察许可的制度压力，避免“又像切页”
  - `P03+`：继续沿 story-first 规则复审后续 parts 的“第一次看是否看得懂”

## Version `v1.00`

- 日期：`2026-04-03`
- 阶段：`P01 开场读懂度修复继续推进`
- 目标：把 `S05` 的守望者交班从“称呼听着很正式，但观众不知道在叫谁”升级成第一次看就能听懂“守望者在叫你，而且你现在是什么身份”的 current 版本，并确保这次修复真正贯通到 `P01 current`、顶部整章入口、master current 与总览页

### 主要产出

- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [p01-s05-watchkeeper-handoff-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p01-s05-watchkeeper-handoff-current.mp4)
- [part-01-future-bay-task-dock-delivery-v23.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v23.mp4)
- [chapter-01-story-spine-preview-v28-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v28-full.mp4)
- [chapter-01-vertical-slice-master-v24-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v24-current.mp4)

### 核心变化

- `P01 / S05` 不再让“见习建造者”单独悬在空中。当前正式口径已改成：
  - `你，未来湾固定小队的新主位。`
  - `现在正式接下第一项灰银任务。`
- 这轮不是只改文档，而是把澄清直接烧进了 `S05 current clip`，并贯通到：
  - `part-01-current.mp4` -> `delivery v23`
  - `chapter-01-story-spine-preview-current.mp4` -> `v28-full`
  - `chapter-01-master-current.mp4` -> `v24-current`
- `render_chapter01_part1_delivery.sh` 已新增 `S05` 的直白交班 overlay，使第一次看片的人即使没先读设定，也能立刻知道守望者正在叫谁
- 总览页已同步更新：
  - `P01` 当前交付说明改为 `v23`
  - 顶部整章入口改指向 `v28-full`
  - `chapter master current` 改指向 `v24-current`
  - `S05` 分镜卡与 clip 窗口改成“身份交班澄清版”

### 当前判断

- `P01`：`PASS WITH NOTES`
  - `S05` 已不再是“知道有人在交班，但不知道他在叫谁”
  - 当前第一次看片时，更容易接上这条逻辑：
    - `S03` 谁出发
    - `S04` 先查什么
    - `S05` 谁来负责
  - 当前剩余主阻塞已收缩到 `S06-S07`：林澄争议后果与启航压力承接
- `chapter current entry`：`PASS WITH NOTES`
  - 顶部整章入口已升级到 `story spine v28-full`
  - `P01 v23`、`story spine v28-full` 和 `master v24-current` 已统一吃到这次 `S05` 身份澄清

### 下一步

- active lane 继续保留在 `P01`
- 优先继续修：
  - `S06`：把林澄争议的地点、性质、倒计时、失败后果压成第一次看就能懂的信息顺序
  - `S07`：把“接受任务”自然推进到“启航”和下一段入港压力
  - 整章：继续排查后段噪音和残余 fake-video 感，不能只修开头

## Version `v0.99`

- 日期：`2026-04-03`
- 阶段：`P01 开场读懂度修复继续推进`
- 目标：把 `S03/S04` 从“提示观众看懂”的过渡方案，升级成观众第一次听就能直接听懂的真对白 clip，并确保这次升级真正贯通到 `P01 current`、顶部整章入口、master current 与总览页

### 主要产出

- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [shot-ch01-p01-s03-achao-arrival-viduq3-v1-direct.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p01-s03-achao-arrival-viduq3-v1-direct.json)
- [shot-ch01-p01-s04-team-operating-viduq3-v1-direct.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p01-s04-team-operating-viduq3-v1-direct.json)
- [shot-ch01-p01-s03-achao-arrival-viduq3-v1-direct.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s03-achao-arrival-viduq3-v1-direct.mp4)
- [shot-ch01-p01-s04-team-operating-viduq3-v1-direct.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s04-team-operating-viduq3-v1-direct.mp4)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v22.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v22.mp4)
- [chapter-01-story-spine-preview-v27-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v27-full.mp4)
- [chapter-01-vertical-slice-master-v23-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v23-current.mp4)

### 核心变化

- `P01 / S03` 不再依赖额外说明条才能让第一次看的孩子听懂任务。阿潮当前使用的真 clip 已改成直接集结令：
  - `未来湾固定小队，火速集结。`
  - `马上去时间档案城，处理林澄任务。`
- `P01 / S04` 也不再说“先别下结论”这类会让人摸不着重点的话，而是改成更直接的证据派追问：
  - `先查清系统为什么认定，林澄只能走那条 93% 的路？`
- `render_chapter01_part1_delivery.sh` 已收口为新的直白台词优先级：
  - 优先使用新的 `viduq3` 直白对白 clip
  - 再回退青云 `wan` 直白对白分支
  - 最后才回退旧版本
- current 链已全部回写：
  - `part-01-current.mp4` -> `delivery v22`
  - `chapter-01-story-spine-preview-current.mp4` -> `v27-full`
  - `chapter-01-master-current.mp4` -> `v23-current`
- 总览页与 source-of-truth 文档已同步：
  - `storyboard-script.md / voice-script.md / shot-list.md` 已统一口径
  - `chapter-01-main-character-dossier.html` 已改成新的版本号、缓存参数和对白说明

### 当前判断

- `P01`：`PASS WITH NOTES`
  - 开头最难懂的 `S03/S04` 已不再只是“提示版 current”，而是新的真对白 clip
  - 现在第一次看这段，至少能更直接地听懂“谁出发、去哪里、处理谁、现在先查什么”
  - 当前剩余主阻塞已经收缩到 `S05-S07`：任务正式交班、林澄争议后果、启航和下一段压力承接
- `chapter current entry`：`PASS WITH NOTES`
  - 顶部整章入口已升级到 `story spine v27-full`
  - `P01 v22`、`story spine v27-full` 和 `master v23-current` 已统一吃到这次 `S03/S04` 真对白升级

### 下一步

- active lane 继续保留在 `P01`
- 优先继续修：
  - `S05`：把守望者的任务交班说成明确责任交接
  - `S06`：把林澄争议的地点、性质、后果压成第一次看就能懂的信息顺序
  - `S07`：把“接受任务”自然推进到“启航”和下一段入港压力
  - 整章：继续排查后段噪音和残余 fake-video 感，不能只修开头

## Version `v0.98`

- 日期：`2026-04-03`
- 阶段：`P01 开场读懂度修复继续推进`
- 目标：把 `S06` 从旧 `wan` 争议切片正式切到新的 `Qingyun / viduq3` 真 clip，并确保修改不是停在单镜，而是贯通到 `P01 current`、顶部整章入口和总览页

### 主要产出

- [shot-ch01-p01-s06-lin-cheng-dispute-slice-viduq3-i2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p01-s06-lin-cheng-dispute-slice-viduq3-i2v-v1.json)
- [shot-ch01-p01-s06-lin-cheng-dispute-slice-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s06-lin-cheng-dispute-slice-viduq3-i2v-v1.mp4)
- [shot-ch01-p01-s06-lin-cheng-dispute-slice-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p01-s06-lin-cheng-dispute-slice-viduq3-i2v-v1.metadata.json)
- [p01-s06-dispute-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p01-s06-dispute-current.mp4)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v21.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v21.mp4)
- [chapter-01-story-spine-preview-v26-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v26-full.mp4)
- [chapter-01-vertical-slice-master-v22-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v22-current.mp4)

### 核心变化

- 新增 `Qingyun / viduq3 / img2video` 请求模板，直接使用现有 `S06` 首帧和林澄 canonical portrait，生成新的林澄争议切片真 clip
- `render_chapter01_part1_delivery.sh` 已改成：
  - 优先使用新的 `Qingyun S06` clip
  - 仅在该文件缺失时才回退旧 `wan v2`
  - 同步把 `S06 current clip` 回写到 `current/clips`
- current 链已全部回写：
  - `part-01-current.mp4` -> `delivery v21`
  - `chapter-01-story-spine-preview-current.mp4` -> `v26-full`
  - `chapter-01-master-current.mp4` -> `v22-current`
- 总览页已同步更新：
  - 顶部唯一整章入口改指向 `v26-full`
  - `P01` 当前交付说明改为 `v21`
  - `S06` 分镜卡与 clip 窗口改成新的青云 current clip
  - 缓存参数已换，避免页面继续读旧片

### 当前判断

- `P01`：`PASS WITH NOTES`
  - `S06` 现在已经不再只是旧片尾部 trim 或说明条补丁，而是新的真实青云 clip
  - 开头现在更接近“人 -> 问题 -> 后果”的顺序
  - 但 `S05 -> S06 -> S07` 的责任交班与启航后果，仍要继续讲顺
- `chapter current entry`：`PASS WITH NOTES`
  - 顶部 current 已升级到 `story spine v26-full`
  - `P01 v21`、`story spine v26-full` 和 `master v22-current` 已统一吃到这次 `S06` 替换

### 下一步

- active lane 继续保留在 `P01`
- 优先继续修：
  - `S05` 的正式交班力度
  - `S06 -> S07` 的后果推进
  - `S07` 的启航落点与下一段入港压力承接

## Version `v0.97`

- 日期：`2026-04-03`
- 阶段：`P01 开场读懂度修复继续推进`
- 目标：不等待失效的 DashScope 密钥恢复，先把已经存在的真实 `S03/S04` clip 升成“第一次看就能懂”的提示版 current，并贯通到整章入口

### 主要产出

- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [p01-s03-achao-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p01-s03-achao-current.mp4)
- [p01-s04-team-operating-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p01-s04-team-operating-current.mp4)
- [part-01-future-bay-task-dock-delivery-v20.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v20.mp4)
- [chapter-01-story-spine-preview-v25-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v25-full.mp4)
- [chapter-01-vertical-slice-master-v21-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v21-current.mp4)

### 核心变化

- `P01 / S03` 保留真实阿潮 clip，但额外烧入了直白任务提示：
  - `阿潮｜全队集结指令`
  - `目的地：时间档案城`
  - `处理对象：灰银级人物 林澄`
- `P01 / S04` 保留真实固定小队工作态 clip，但额外烧入了队伍分工提示：
  - `祁野：查清 93% 路径证据`
  - `闻夏：抢在午夜前争时间`
  - `固定小队已经在工作，你是责任主位`
- `P01` 的 source-of-truth 文本已对齐：
  - 不再继续保留“拧着说、故作聪明”的旧口径
  - `voice-script / storyboard / shot-list / master episode script` 已统一成新的更直白表达
- current 链已全部回写：
  - `part-01-current.mp4` 继续指向 `delivery v20`
  - `chapter-01-story-spine-preview-current.mp4` -> `v25-full`
  - `chapter-01-master-current.mp4` -> `v21-current`

### 当前判断

- `P01`：`PASS WITH NOTES`
  - 开场第一段的“地点不清 / 集结对象不清 / 队友分工不清”已经从真实 clip 层开始收口
  - 但 `S05-S07` 的责任后果与林澄争议切片，仍要继续把故事因果讲得更顺
- `chapter-01 current entry`：`PASS WITH NOTES`
  - 顶部整章入口已升级到 `story spine v25-full`
  - 当前主要 residual risk 已从“开头完全看不懂”收缩为“后半程仍有对白和因果顺滑度待继续提升”

### 下一步

- active lane 继续保留在 `P01`
- 优先继续修：
  - `S05` 的责任交班力度
  - `S06` 林澄争议切片的信息顺序
  - `S07` 从接受任务到启航的后果推进

## Version `v0.96`

- 日期：`2026-04-03`
- 阶段：`P04 waiting-zone 真替换与整章 current 回写`
- 目标：把 `P04` 里仍然会被看成 still-motion 的等待区进入与签字笔物件位，连同父亲 / 林澄 speaking close-up 的更稳版本，一次性收进正式 current，并贯通到整章入口

### 主要产出

- [agents.md](/Users/wujames/Desktop/AI未来通识课（K12）/agents.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [render_chapter01_part4_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part4_delivery.sh)
- [shot-ch01-p04-s01-waiting-zone-ingress-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p04-s01-waiting-zone-ingress-viduq3-i2v-v1.mp4)
- [shot-ch01-p04-s02-sign-pen-soothing-screen-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p04-s02-sign-pen-soothing-screen-viduq3-i2v-v1.mp4)
- [shot-ch01-p04-s04-father-close-viduq3-s2v-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p04-s04-father-close-viduq3-s2v-v2.mp4)
- [shot-ch01-p04-s05-lin-close-viduq3-s2v-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p04-s05-lin-close-viduq3-s2v-v2.mp4)
- [part-04-waiting-zone-and-father-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-04-waiting-zone-and-father-delivery-v2.mp4)
- [chapter-01-story-spine-preview-v24-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v24-full.mp4)
- [chapter-01-vertical-slice-master-v20-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v20-current.mp4)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `QINGYUN_API_KEY` 当前可用外部来源已重新核实并补回项目规则：
  - 只记录本机外部 source path、shell-safe 加载方式和 `GET /v1/models = 200`
  - 不把裸密钥写回仓库
- `P04 / S01` 已从等待区静帧入口升级为真实 `viduq3` ingress clip：
  - 现在不再靠 still-motion 假装“迈入等待区”
  - 等待区气流、材质反光和轻微前进位移已由真实视频承担
- `P04 / S02` 已从物件静帧升级为真实 `viduq3` object-pressure clip：
  - 签字笔反光与安抚屏柔光脉冲现在属于真实视频层
  - overlay 只继续承担受控中文信息层，不再替底片假装运动
- `P04 / S04/S05` 已切到更稳的 `start-end2video v2`：
  - 父亲与林澄近景现在都使用更强的首尾帧锁定 speaking clip
  - `current/clips` 已同步切换到 `s2v-v2`
- current 链已全部回写：
  - `part-04-current.mp4` -> `delivery v2`
  - `chapter-01-story-spine-preview-current.mp4` -> `v24-full`
  - `chapter-01-master-current.mp4` -> `v20-current`
  - `video-loop-state.json` 已不再把 `P04` 判成 `FAKE-VIDEO REPLACEMENT REOPENED`

### 当前判断

- `P04`：`PASS WITH NOTES`
  - `S01-S05` 这轮修复已经真正落到 clip、part 和 chapter assemblies
  - 当前主要 residual risk 不再是 still-motion，而是 speaking clip 的中文对白 / 口型贴合度仍需要继续人工复审
- `chapter-01 current entry`：`PASS WITH NOTES`
  - 顶部整章入口已升级到 `story spine v24-full`
  - 但整集第一轮观看的最大阻塞已经回到 `P01 / S02-S04` 的身份 onboarding 与任务语言，而不是 `P04` 的假视频债务

### 下一步

- active lane 切回 `P01`
- 继续按 `storyboard-script.md` 和 `shot-list.md` 的全片总修表，优先清理：
  - `S02-S04` 的身份说明
  - 任务对象与紧急原因
  - 让第一次看的孩子更快知道 `我 / 林澄 / 队友 / 父亲 / 07` 分别是谁
  - 后续所有修复继续坚持 `clip -> part -> story spine/master -> HTML` 一起回写
## Version `v0.95`

- 日期：`2026-04-03`
- 阶段：`P01/S01 A01+A02 混合开场修复`
- 目标：不再让 `S01` 在“保留原始任务台前构图”和“保留真实水面动态”之间二选一，而是把原始 `A01` 和真实港区动态 `A02` 真正整合进 current，并把结果贯通到 `clip -> part -> story spine -> master -> HTML`

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [p01-s01-dock-intro-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p01-s01-dock-intro-current.mp4)
- [p01-s01-dock-intro-labeled-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p01-s01-dock-intro-labeled-current.mp4)
- [part-01-future-bay-task-dock-delivery-v20.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v20.mp4)
- [part-01-future-bay-task-dock-delivery-v20.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v20.metadata.json)
- [chapter-01-story-spine-preview-v23-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v23-full.mp4)
- [chapter-01-story-spine-preview-v23-full.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v23-full.metadata.json)
- [chapter-01-vertical-slice-master-v19-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v19-current.mp4)
- [chapter-01-vertical-slice-master-v19-current.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-vertical-slice-master-v19-current.metadata.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `S01` 不再只依赖单一路径：
  - 先用原始 `A01` 的第一人称任务台前构图立住“我已经在未来湾任务码头”
  - 再接入 `A02` 的真实港区动态水面和反射运动
- 这次不是回退到“静态图假装在动”：
  - `A01` 只承担短促 anchor frame
  - 真正的持续动态仍由 `A02` 接管
- current 链已同步更新：
  - `S01 current clip` 已改为新的 `A01+A02` 混合版本
  - `P01 current` 已切到 `delivery v20`
  - `story spine current` 已切到 `v23-full`
  - `chapter master current` 已切到 `v19-current`
- 主总览页已改成新的 source of truth：
  - 顶部整章入口改指向 `v23-full`
  - `P01/S01` 文案明确写成“保留原图 + 接回真实水动”
  - 历史资产区也补上 `A01/A02` 已重新参与 current 混合开场的说明

### 当前判断

- `P01/S01`：`PASS`
  - “原图被丢掉”与“水不动”这两个开场阻塞已在真实 clip 层同时收口
- `chapter-01 current entry`：`PASS WITH NOTES`
  - 当前顶部入口已经改成 `204.92s` 的 `story spine v23-full`
  - 但开场 `S02-S04` 的身份 onboarding 和整章后续对白可懂度仍要继续修

### 下一步

- active lane 仍保持 `P04`
- 继续按全片可读性总表修 `S02-S04` 的身份和任务语言
- 所有后续修复继续执行：
  - `clip`
  - `part delivery / current delivery`
  - `story spine / master / preview`
  三层同步回写后才算完成

## Version `v0.94`

- 日期：`2026-04-03`
- 阶段：`整集 story-first 可读性复审`
- 目标：不再靠零散对话记忆“哪里看不懂”，而是把 chapter-01 从 `P01-P12` 的故事可读性债务、clip / beat / bridge 风险、以及当前唯一修复动作正式回写到 source of truth

### 主要产出

- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 把“整集故事看不懂”的问题从抽象抱怨改成了可执行的总修框架：
  - 每一段都先回答 `我在哪里 / 谁在要什么 / 为什么现在必须推进 / 如果失败会失去什么`
  - 任何 part 只要这 4 个问题里有 2 个以上回答不清，就不准误报成“已经讲顺”
- `storyboard-script.md` 现已新增：
  - `整集故事可读性硬门`
  - `按 part 的总修结论`
  - 明确 `P01-P12` 各段的必须信息、最大误读和 clip / assembly 债务
- `shot-list.md` 现已纠正旧口径漂移：
  - 不再误报自己只覆盖 `demo / vertical slice`
  - 明确当前已经服务 `P01-P12` 的整章 current
  - 新增 `整集故事修复总表`
- 主总览页现已同步新增：
  - `整片修复总表`
  - 把 `P02-P12` 的 part 视频统一标成 `完整视频`
  - 让 `P01` 的 fully-expanded 逐镜格式和全片总修框架同时可见

### 当前判断

- `source of truth 对齐`：`PASS`
  - 当前 chapter-01 已经有一套统一的全片可读性修复口径
  - 后续 agent 不需要再从旧 vertical-slice 口径倒推当前主线
- `整集故事视频本身`：`STORY-FIRST IN PROGRESS`
  - 这次修的是“全片该怎么修”的控制面，不是误报成所有 clip 已经一次性完成
  - 当前最值得继续实打实落 clip 的 part 仍是 `P04`

### 下一步

- 继续按 current loop 先修 `P04`
- 同时带着这次总表去复审 `P02-P12` 的每段对白、bridge 和 clip 债务
- 所有后续视频修改都必须继续遵守：
  - `clip`
  - `part delivery / current delivery`
  - `story spine / master / preview`
  三层同步回写后才算完成

## Version `v0.93`

- 日期：`2026-04-03`
- 阶段：`P01/S01 水面动态修复`
- 目标：不再让 chapter-01 开头第一拍读成“海面几乎不动的假空镜”，而是把 `S01` 真正换成同空间、可见水纹与反射变化的港区动态镜头，并把修复贯通到所有 current 交付入口

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [p01-s01-dock-intro-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p01-s01-dock-intro-current.mp4)
- [p01-s01-dock-intro-labeled-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p01-s01-dock-intro-labeled-current.mp4)
- [part-01-future-bay-task-dock-delivery-v19.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v19.mp4)
- [part-01-future-bay-task-dock-delivery-v19.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v19.metadata.json)
- [chapter-01-story-spine-preview-v22-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v22-full.mp4)
- [chapter-01-story-spine-preview-v22-full.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v22-full.metadata.json)
- [chapter-01-vertical-slice-master-v18-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v18-current.mp4)
- [chapter-01-vertical-slice-master-v18-current.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-vertical-slice-master-v18-current.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 先否定了一个错误前提：
  - 系统里并没有一条“更强水面动态的旧 `A01`”
  - 旧工作台里的多个所谓历史候选，经 `shasum` 核对后与当前旧 `S01` 实为同一文件
- 这次修复改走 `same-space upgrade`，不是继续给静帧加动效：
  - 正式放弃弱水面 `A01` 路线
  - 提升系统里已有的 [shot-a02-future-bay-establishing-wan2.6-i2v-flash-v1-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-a02-future-bay-establishing-wan2.6-i2v-flash-v1-720p.mp4) 为当前 `S01` 港区底片
  - 重烧地点条 `未来湾任务码头 / 固定小队任务中枢`
- 当前链路已完整贯通：
  - `S01 current clip` 已更新为 `4.00s / 927283 bytes`
  - `P01 current` 已更新为 `delivery v19 / 27.00s`
  - `story spine current` 已更新为 `v22-full / 131.00s`
  - `chapter master current` 已更新为 `v18-current / 157.50s`

### 当前判断

- `P01/S01`：`PASS`
  - “水不动”这一条用户阻塞问题已在真实 clip 层修掉
  - 这次不是页面文案修饰，而是已进入 `clip -> part -> story spine -> master`
- `chapter-01 current entry`：`PASS WITH NOTES`
  - 开场第一拍的假感已显著下降
  - 但 `S02-S04` 的人物身份 onboarding 与对白可懂度仍要继续收清

### 下一步

- active lane 仍保持 `P04`
- `P01` 这次只收 `S01 水面动态` 这条明确债务
- 不把这次成功误报成“chapter-01 开头所有可读性问题都已经解决”

## Version `v0.92`

- 日期：`2026-04-02`
- 阶段：`P03/C02 真 clip 回写 current`
- 目标：不再把“系统里其实已经有的青云真视频”继续当成工作台遗留物，而是把它真正提升进 current 资产链，清掉 `P03/C02` 的 zoompan fallback

### 主要产出

- [render_chapter01_part3_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part3_delivery.sh)
- [shot-ch01-p03-s02-lin-cheng-question-viduq3-s2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p03-s02-lin-cheng-question-viduq3-s2v-v1.mp4)
- [shot-ch01-p03-s02-lin-cheng-question-viduq3-s2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p03-s02-lin-cheng-question-viduq3-s2v-v1.metadata.json)
- [part-03-archive-hall-pressure-delivery-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-03-archive-hall-pressure-delivery-v4.mp4)
- [part-03-archive-hall-pressure-delivery-v4.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-03-archive-hall-pressure-delivery-v4.metadata.json)
- [chapter-01-story-spine-preview-v14.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v14.mp4)
- [chapter-01-story-spine-preview-v14.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v14.metadata.json)
- [chapter-01-vertical-slice-master-v16-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v16-current.mp4)
- [chapter-01-vertical-slice-master-v16-current.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-vertical-slice-master-v16-current.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 把历史已验证的青云 `P03/C02` 真 clip 正式提升为 current 资产：
  - 来源是 `2026-03-26` 留下的 `Qingyun / viduq3 / start-end2video` probe
  - 它本来就使用了和 `P03/C02` 一致的 `start/end frame` 组合
  - 因此这次不是“拿别段视频硬塞”，而是把一直在系统里的真实可用产出正式回写到了主资产链
- `render_chapter01_part3_delivery.sh` 现已改为：
  - 先把历史 probe 提升成 [shot-ch01-p03-s02-lin-cheng-question-viduq3-s2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p03-s02-lin-cheng-question-viduq3-s2v-v1.mp4)
  - 再重装 `P03 delivery v4`
  - 让 `C02` 不再继续停留在 `zoompan fallback`
- `P03 delivery v4` 的当前结构已收口为：
  - `C01` 继续沿用已 accepted 的大厅建立锚点
  - `C02` 改为 promoted `Qingyun` 真 reaction close-up
  - `C03/C05` 明确保留为 `UI-first` 信息位
  - `C04` 改用更干净的 same-space real pressure clip
- 当前 accepted current 里的同类假视频主债务已正式收口：
  - `P01/A01-A02` 是显式 intro cards，不再伪装成运动镜头
  - `P12` 是明确的导师离场卡片，不再伪装成正式视频尾段
  - `P03/C02` 已换成真实青云 clip

### 当前判断

- `P03 delivery v4`：`PASS WITH NOTES`
  - 它已经足以替换旧 `P03 current delivery v2`
  - 这次提升的价值在于把最后一条同类 fake-video 主债务从 accepted current 里拿掉
  - 但它仍不是“visible speech 全部同步完成”的最终冻结版
- `chapter-01 master current v16`：`PASS WITH NOTES`
  - 现在已经直接吃到新的 `P03 v4`
- `story spine v14`：`STORY-FIRST IN PROGRESS`
  - 继续承担“最完整顺看”入口，但也已同步更新到新的 `P03 v4`

### 下一步

- active lane 从 `P03` 切回 `P04`
- 后续优先不再是“继续找假视频”
- 而是定向复审 `P04` 的 waiting-zone continuity、人物同步与入口承压感

## Version `v0.87`

- 日期：`2026-04-02`
- 阶段：`P01 前段假视频债务收紧`
- 目标：不假装“前面三拍全都一样假”，而是先修复 current 状态漂移与 loop 失效，再用最低风险 assembly 编辑把真正最像假视频 linger 的 `A01/A02` 收短，让开场更快进入阿潮真实入场位

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v16.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v16.mp4)
- [part-01-future-bay-task-dock-delivery-v16.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v16.metadata.json)
- [chapter-01-vertical-slice-master-v13-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v13-current.mp4)
- [chapter-01-vertical-slice-master-v13-current.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-vertical-slice-master-v13-current.metadata.json)
- [chapter-01-story-spine-preview-v9.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v9.mp4)
- [chapter-01-story-spine-preview-v9.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v9.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 先修复了 `video-loop-state.json` 的 JSON 失效问题
  - 旧文件在 `scope_note` 后缺逗号，`jq` 已无法解析
  - 这会直接破坏 chapter-01 的 loop 控制判断
- `P01` 继续按 `editor` 结论从装配层收口，而不是回头整段重跑
  - `S01` 已由 `3.4s` 收到 `2.2s`
  - `S02` 已由 `3.0s` 收到 `2.4s`
  - 这样开场会更快进入 `S03` 的阿潮真实入场位
- contact-sheet 复审后，`A03` 不再与 `A01/A02` 混算同一档假视频债务
  - `A01/A02` 仍是主债务
  - `A03` 已具备明确真实位移，只保留为开场 continuity 审片对象
- chapter 级入口已同步更新：
  - accepted master：`chapter-01-vertical-slice-master-v13-current.mp4`
    - 当前正式时长为 `160.17s`
  - 完整故事预览：`chapter-01-story-spine-preview-v9.mp4`
    - 当前正式时长为 `207.58s`

### 当前结论

- `P01`：`PASS WITH NOTES`
  - 这轮收掉的是最像“照片加滤镜冒充视频”的前段 linger
  - 但 `A01/A02` 仍属于 replacement debt，不应被误报成“已彻底解决”
- 当前更准确的开场债务口径是：
  - `A01/A02`：仍是假视频主债务
  - `A03`：不再计入同档债务
- 下一条最值得继续推进的技术问题：
  - `P05 -> P06 -> P07` bridge continuity
  - 而不是继续把 `P01` 三拍笼统混成一类问题反复描述

## Version `v0.88`

- 日期：`2026-04-02`
- 阶段：`P06->P07 consequence bridge 落地`
- 目标：不把 `P05/P06/P07` 的页面切换感继续留在抽象待办里，而是直接用 assembly-level recovery path 验证“先补 bridge 是否就能救”

### 主要产出

- [render_chapter01_p06_p07_consequence_bridge.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_p06_p07_consequence_bridge.sh)
- [chapter-01-p06-p07-consequence-bridge-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-p06-p07-consequence-bridge-v1.mp4)
- [chapter-01-p06-p07-consequence-bridge-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-p06-p07-consequence-bridge-v1.metadata.json)
- [render_chapter01_story_spine_preview.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_story_spine_preview.sh)
- [chapter-01-story-spine-preview-v10.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v10.mp4)
- [chapter-01-story-spine-preview-v10.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v10.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P06 -> P07` 的问题没有继续停在口头判断
  - 已补出一条 `2.12s` 的 consequence bridge
  - 它是 assembly-level recovery path，不是假装成新的正式 part
- `story spine current` 已切到 `v10`
  - 新版会在 `P06` 与 `P07` 之间显式插入 bridge
  - 当前正式时长为 `209.70s`
- 这一步的目的不是“桥看起来多高级”
  - 而是先把 repeated empty-space reset 从 page-switch 感收成更可解释的后果推进
- 当前 bottleneck 已经前移：
  - `P05/P06/P07` 的主问题不再是“是否必须重开”
  - 而是 `P07-P09` 暗部亮度与可辨识度

### 当前结论

- `P06 -> P07`：`PASS WITH NOTES`
  - bridge 已落地并进入 official `story spine current`
  - 但它仍属于 recovery path，不等于这条过渡已经达到最终成片最优解
- 下一条最值得继续推进的技术问题：
  - `P07-P09` 亮度与可辨识度

## Version `v0.89`

- 日期：`2026-04-02`
- 阶段：`P07 opening readability lift`
- 目标：不把 `P07-P09` 的亮度问题一股脑混写，而是先对最像“看得见但不够稳”的 `P07` 前三拍做轻度装配提亮，验证低风险 readability lift 是否值得继续沿用

### 主要产出

- [render_chapter01_part7_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part7_delivery.sh)
- [part-07-silent-practice-room-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-07-silent-practice-room-delivery-v2.mp4)
- [part-07-silent-practice-room-delivery-v2.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-07-silent-practice-room-delivery-v2.metadata.json)
- [chapter-01-story-spine-preview-v11.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v11.mp4)
- [chapter-01-story-spine-preview-v11.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v11.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P07` 不再只停留在“建议提亮”
  - `E05/E06/E07` 已做轻度 assembly-level readability lift
  - 没有改结构，也没有回头重跑模型
- `part-07 current` 已切到 `delivery v2`
  - 当前正式时长仍为 `13.17s`
- 完整故事预览已同步重渲为 `story spine v11`
  - 继续保留 `P06 -> P07` consequence bridge
  - 同时吃回 `P07 v2` 的 opening readability lift

### 当前结论

- `P07`：`PASS WITH NOTES`
  - 开头空间与物件信息更稳一点
  - 但这还不代表 `P08/P09` 已自动过门
- 下一条最值得继续推进的技术问题：
  - `P08/P09` 是否真的还需要同类暗部可读性修复

## Version `v0.90`

- 日期：`2026-04-02`
- 阶段：`P12 mentor end-card 收口`
- 目标：不再让 `P12` 的后半段继续靠同场景轻动 hold 冒充视频，而是把它明确改成 world-in 离场卡片；同时先关掉 `P08/P09` 被误挂为同类暗部问题的支线

### 主要产出

- [render_chapter01_part12_voicefirst_preview.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part12_voicefirst_preview.sh)
- [render_chapter01_part12_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part12_delivery.sh)
- [part-12-digital-mentor-voicefirst-preview-v5.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-voicefirst-preview-v5.mp4)
- [part-12-digital-mentor-delivery-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-delivery-v4.mp4)
- [chapter-01-story-spine-preview-v12.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v12.mp4)
- [chapter-01-vertical-slice-master-v14-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v14-current.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P08/P09` 的暗部支线先被正确关单
  - contact-strip 复审确认它们主要属于 `UI-first` 信息组织位
  - 当前不继续沿用 `P07` 那种 assembly-level 提亮，也不把中段 UI 段误并入“照片冒充视频”同类债务
- `P12` 后半段不再继续伪装成视频
  - 保留前半段真实 `clean retry opening clip`
  - 把后半段改为明确的 `world-in mentor question card`
  - 总时长从 `24.4s` 收到 `23.6s`
- chapter 级入口已同步吃回 `P12 v4`
  - `part-12 current` -> `delivery v4`
  - `chapter-01-master-current.mp4` -> `v14`
  - `chapter-01-story-spine-preview-current.mp4` -> `v12`

### 当前结论

- `P12 delivery v4`：`PASS WITH NOTES`
  - 它不是“新增更多真实视频”，而是把最像假视频的尾段改成了明确设计过的离场卡片
  - 这让 `P12` 退出同类 fake-video 主债务队列
- 当前 remaining fake-video replacement debt 已收束为：
  - `P01 / A01-A02`
  - `P03 / C02`
- 下一条最值得继续推进的技术问题：
  - `P01 / A01-A02` 开场 still-motion 主债务

## Version `v0.91`

- 日期：`2026-04-02`
- 阶段：`P01 faux-video opening -> explicit intro cards`
- 目标：不再让 `A01/A02` 继续伪装成运动镜头，而是把开场前两拍改成明确的信息卡，再尽快交给 `A03` 的真实入场动作

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v17.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v17.mp4)
- [part-01-future-bay-task-dock-delivery-v17.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v17.metadata.json)
- [chapter-01-story-spine-preview-v13.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v13.mp4)
- [chapter-01-vertical-slice-master-v15-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v15-current.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `A01/A02` 不再继续装成“低运动视频”
  - `A01` 现在是显式 `dock intro card`
  - `A02` 现在是显式 `grey-silver request card`
  - 两拍都更快把节奏交给 `A03` 的真实入场动作
- `P01` 时长从 `26.2s` 收到 `24.0s`
  - 不是单纯靠再 trim 一刀
  - 而是直接把最像 faux-video linger 的部分改写成明确的信息卡表达
- chapter 级入口已同步吃回 `P01 v17`
  - `part-01 current` -> `delivery v17`
  - `chapter-01-master-current.mp4` -> `v15`
  - `chapter-01-story-spine-preview-current.mp4` -> `v13`

### 当前结论

- `P01 delivery v17`：`PASS WITH NOTES`
  - 它仍不是最终真实视频开场
  - 但已经不再属于“照片加滤镜冒充视频”同类问题
- 当前 remaining fake-video replacement debt 已继续收缩到：
  - `P03 / C02`
- 下一条最值得继续推进的技术问题：
  - `P03 / C02` 真实近景替换

## Version `v0.86`

- 日期：`2026-04-01`
- 阶段：`P01 守望者交班尾部收口`
- 目标：继续用最低风险的 assembly 编辑把开场讲顺，不重开模型，只把 `S05` 从“独立 talking-head sample”收回到“任务正式压上来”的交班链条里

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v15.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v15.mp4)
- [part-01-future-bay-task-dock-delivery-v15.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v15.metadata.json)
- [chapter-01-vertical-slice-master-v11-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v11-current.mp4)
- [chapter-01-story-spine-preview-v7.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v7.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P01` 继续按 `editor + directors-room` 联合复审，而不是回头整段重生
  - 这轮结论明确锁成：`S04 KEEP / S05 TRIM_TAIL / S07 KEEP`
- `S05` 已从 `4.0s` 收到 `3.4s`
  - 当前主要收益不是“更短更快”本身
  - 而是让守望者更像把任务压到你面前，而不是单独站稳说完一整条样片台词
- `S07` 当前经过备选复审后仍维持 `KEEP`
  - 现有 `Achao visible / world-audio` 备选依旧带明显乱字 overlay
  - 因此没有被提升为 current
- `P01 current` 已升级到 `delivery v15`
  - 当前正式时长为 `28.00s`
- chapter 级入口已同步更新：
  - accepted master：`chapter-01-vertical-slice-master-v11-current.mp4`
    - 当前正式时长为 `161.96s`
  - 完整故事预览：`chapter-01-story-spine-preview-v7.mp4`
    - 当前正式时长为 `209.38s`

### 当前结论

- `P01`：`PASS WITH NOTES`
  - 当前开场后半段的 lingering 拼接感继续收缩
  - 但 active lane 仍保持在 `P01 / W10`
- 下一条唯一优先动作：
  - 再审一次 `S04 -> S05 -> S06 -> S07` 是否已经足够 story-clear
  - 只有在仍明显像 page switch 时，才允许补一条极短 dock bridge
  - 不回头重跑带乱字的 `S07` 备选

## Version `v0.85`

- 日期：`2026-04-01`
- 阶段：`P01 开场静尾 trim 收口`
- 目标：不先重开 `P01` 模型链，而是先把开场里最明显、也最安全可收的静尾 lingering 从 assembly 层拿掉，让开场更像连续任务启动，而不是多条成功 clip 的拼接

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v14.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v14.mp4)
- [part-01-future-bay-task-dock-delivery-v14.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v14.metadata.json)
- [chapter-01-vertical-slice-master-v10-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v10-current.mp4)
- [chapter-01-story-spine-preview-v6.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v6.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P01` 当前不再卡在“脚本改完却无法重复渲染”
  - 旧脚本依赖已消失的历史 `tmp/part1-delivery/*.wav`
  - 现在已改成在 `TMP_DIR` 内直接重建所需氛围与 UI 音效
- `S06 v2` 已经按 `editor` 结论从装配层收短：
  - 由 `5.0s` 收到 `4.0s`
  - 主表演与关键信息保留
  - 旧版静尾 lingering 被拿掉
- `P01 current` 已升级到 `delivery v14`
  - 当前正式时长为 `28.60s`
- chapter 级入口已同步更新：
  - accepted master：`chapter-01-vertical-slice-master-v10-current.mp4`
    - 当前正式时长为 `162.56s`
  - 完整故事预览：`chapter-01-story-spine-preview-v6.mp4`
    - 当前正式时长为 `209.98s`

### 当前结论

- `P01`：`PASS WITH NOTES`
  - 当前已经先收掉开场里最安全的一条静尾
  - 但 `S04/S05/S07` 仍保留下一轮 `bridge / same-space upgrade` 审查窗口
- active lane 继续保持：`P01`
  - 下一条唯一优先动作不再是重开 `S06`
  - 而是继续复审 `S04/S05/S07` 的可接性与升级必要性

## Version `v0.84`

- 日期：`2026-04-01`
- 阶段：`P10->P11 consequence bridge 落地`
- 目标：把上一轮已经诊断清楚的 `F04 -> G01` 断点真正收掉，让高潮双拍从“功能页切换感”推进成“公开承担 -> 后果落地”

### 主要产出

- [part-10-free-echo-platform-delivery-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v4.mp4)
- [part-11-midnight-choice-return-delivery-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-11-midnight-choice-return-delivery-v3.mp4)
- [chapter-01-vertical-slice-master-v9-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v9-current.mp4)
- [chapter-01-story-spine-preview-v5.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v5.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P10` 已从 `delivery v3` 升到 `delivery v4`：
  - `F04` 尾部 lingering 收短
  - 高潮第一拍不再像“提交完一个表单后还停太久”
  - 当前正式时长为 `15.40s`
- `P11` 已从 `delivery v2` 升到 `delivery v3`：
  - 在 `G01` 前插入一条低成本 `consequence bridge`
  - `G01` 开头与尾部收短
  - 当前更像“刚才那句话的后果现在压回来了”，而不是“新页面开始了”
  - 当前正式时长为 `15.53s`
- `part-11-current.mp4` 的 current 指针已从错误挂着的旧版 `v1` 修正到 `v3`
- chapter 级入口已同步到新主线：
  - accepted master：`chapter-01-vertical-slice-master-v9-current.mp4`
  - 完整故事预览：`chapter-01-story-spine-preview-v5.mp4`

### 当前结论

- `P10`：`PASS WITH NOTES`
- `P11`：`PASS WITH NOTES`
- `P10 -> P11` 双拍高潮：`PASS WITH NOTES`
  - 主要跳切感已从主问题降为局部 notes
  - 后续不再优先重开长辩论，而是把注意力切回 `P01` 开场假视频替换 backlog

## Version `v0.83`

- 日期：`2026-04-01`
- 阶段：`P10->P11 双拍高潮编辑复审`
- 目标：不再抽象地说“后半段还是有点跳”，而是直接按 `editor + directors-room` 审 current 成片，判断 `P10 公开冲突 -> P11 后果落地` 到底卡在什么地方

### 本轮复审对象

- [part-10-free-echo-platform-delivery-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v3.mp4)
- [part-11-midnight-choice-return-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-11-midnight-choice-return-delivery-v2.mp4)
- [chapter-01-vertical-slice-master-v8-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v8-current.mp4)

### 本轮总判断

- `P10` 内部四拍已经基本成立
- `P11` 自身也已经不再是“完全塌回静帧结果页”的状态
- 当前最关键的问题被正式收束为：
  - `F04 -> G01` 缺少一拍“公共后果压回林澄身上”的承压桥
  - 所以孩子更容易感到“从一个功能页切到另一个功能页”，而不是“公开承担之后，后果立刻落到当事人面前”

### editor 结论

- `F01`：`KEEP`
- `F02`：`KEEP`
- `F03`：`KEEP`
- `F04`：`TRIM_TAIL`
- `G01`：`TRIM_HEAD + TRIM_TAIL`
- `F04 -> G01`：`BRIDGE`

### directors-room 结论

- 高潮第二拍当前缺的不是更大的制度奇观，也不是再多一轮辩论
- 缺的是一条极短但明确的 consequence bridge：
  - 让观众感到“刚才公开说出去的话，现在已经压回林澄的人生”

### 下一条唯一优先动作

1. 先做 `F04 -> G01` 的低成本 bridge 方案
2. 若仍不够，再定向重剪：
   - `F04` 尾部收短
   - `G01` 头尾收短
3. 暂不回头重开 `F03`，也不改变 `P10 -> P11` 的 canonical 双拍摆位

## Version `v0.82`

- 日期：`2026-04-01`
- 阶段：`chapter-01 结构复审一致性收口`
- 目标：把上一轮故事复审已经得出的结论，继续压实到分镜稿、产品状态层和主交付页，避免后续再次出现“故事主线已锁，但执行文档还留着旧分支”的回摆

### 本轮完成的 targeted fix

- [x] 在 `storyboard-script.md` 中去掉 `P10/S03` 的“真人对手 / agent 对手”双主线残留
- [x] 把 `P10/S04` 的系统文案改成第一集默认的 `序列员 07 / 文明辩手` 接入口径
- [x] 在 `product-script.md` 的状态枚举处明确：`human_vs_human` 与 `group_vs_group` 只是产品扩展预留，不是 chapter-01 当前 canonical 主线
- [x] 把本轮 to do 的完成情况和剩余唯一风险同步写入主交付 HTML

### 当前一致性判断

- chapter-01 当前关于 `高潮摆位`、`辩论模式`、`玩家角色关系`、`互动锚点` 的 source of truth 已基本统一
- 现在最大的剩余风险已不再是文档互相打架，而是：
  - 当前 accepted 视频主线是否真的把 `P10 公开冲突 -> P11 后果落地` 这条双拍高潮拍顺
  - 换句话说，问题已经从“写没写清”切到“成片有没有把这条结构拍出来”

## Version `v0.81`

- 日期：`2026-04-01`
- 阶段：`chapter-01 故事结构复审与 canonical 互动链收束`
- 目标：重新检查整集剧情是否通顺、儿童观众是否好理解、背景交代是否清楚、互动问题应该摆在哪里、辩论高潮应该如何安排，以及玩家与剧中人物在辩论中的关系和流程

### 本轮总判断

- 当前这集已经不再是“完全看不懂人物从哪里来、场景从哪里来”的状态
- 但它仍存在一个结构风险：
  - 如果不把 `背景交代`、`高压互动锚点`、`P10/P11 的双拍高潮` 和 `辩论默认模式` 明确锁死，后续产品稿、分镜稿和视频装配很容易再次各讲各的
- 因此本轮不是继续补资产，而是先把故事层的 source of truth 重新压紧

### 本轮完成的 to do

- [x] 明确前 10 到 12 分钟里，孩子必须理解的 4 个背景问题
- [x] 固定整集 5 个必须亲手承担的高压互动锚点
- [x] 明确高潮不是单一一场辩论赛，而是 `P10 公开冲突 + P11 后果落地`
- [x] 固定第一集默认辩论模式为 `human_vs_agent`
- [x] 明确玩家、祁野、闻夏、回响、林澄、序列员 07 在辩论段中的职责关系

### 已回写主文件

- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [product-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/product-script.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 下一条最该继续的动作

- 不再先发散讨论更多辩论模式
- 直接进入 `editor + directors-room` 联合复审：
  - 检查当前视频主线是否已经体现 `P10 -> P11` 的双拍高潮
  - 检查 `F02 -> F03 -> F04 -> G01` 是否真的让孩子感到“我先公开回答，再把后果带回林澄面前”

## Version `v0.80`

- 日期：`2026-03-31`
- 阶段：`P10 F02/F04 动态 carrier 接回高潮中段`
- 目标：不再让 `P10` 的中段继续靠同一张 `S-07` 母图做 zoompan 假装视频，而是把 `F02/F04` 都换成真实的 same-space 动态承载，让高潮中部更像同一空间里连续发生的组织与承担

### 主要产出

- [shot-ch01-p10-s02-evidence-stance-carrier-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p10-s02-evidence-stance-carrier-viduq3-i2v-v1.mp4)
- [shot-ch01-p10-s02-evidence-stance-carrier-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p10-s02-evidence-stance-carrier-viduq3-i2v-v1.metadata.json)
- [shot-ch01-p10-s04-public-statement-carrier-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p10-s04-public-statement-carrier-viduq3-i2v-v1.mp4)
- [shot-ch01-p10-s04-public-statement-carrier-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p10-s04-public-statement-carrier-viduq3-i2v-v1.metadata.json)
- [part-10-free-echo-platform-delivery-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v3.mp4)
- [chapter-01-vertical-slice-master-v8-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v8-current.mp4)
- [shot-ch01-p10-s02-evidence-stance-carrier-viduq3-i2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s02-evidence-stance-carrier-viduq3-i2v-v1.json)
- [shot-ch01-p10-s04-public-statement-carrier-viduq3-i2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s04-public-statement-carrier-viduq3-i2v-v1.json)
- [render_chapter01_part10_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part10_delivery.sh)

### 核心变化

- `F02` 与 `F04` 都已拿到真实 `qingyun / viduq3-turbo / img2video` same-space carrier：
  - 两条 clip 都是 `5.04s`
  - 两条 clip 都是 `880x588`
  - 两条 clip 都是 `24fps`
  - 抽帧哈希持续变化，不是假视频
- `part-10 delivery` 已升级到 [part-10-free-echo-platform-delivery-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v3.mp4)：
  - `F01` 继续承担“城市正在倾听”的真实建立
  - `F02/F04` 不再是 detached 静态底图
  - `F03` 继续承担对手进入与短反问
- chapter 级 accepted 审片入口已同步重渲为 [chapter-01-vertical-slice-master-v8-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v8-current.mp4)

### 当前结论

- `P10 / F02 carrier`：`PASS WITH NOTES`
- `P10 / F04 carrier`：`PASS WITH NOTES`
- `P10 delivery v3`：`PASS WITH NOTES`
  - `P10` 当前已经摆脱 `F01-F04` 的静帧假视频债务
  - 当前 notes 收缩为：`F02/F04` 虽然已经是真实动态承载，但还需要继续复审它们的节奏和 UI-first 可读性，确认高潮中段不再像连续切功能页
- active lane 继续保持 `P10`
  - 下一条唯一优先动作是做一轮 `editor pass`，专看 `F02 -> F03 -> F04` 是否已经足够顺地把压力送进 `P11`

## Version `v0.79`

- 日期：`2026-03-31`
- 阶段：`P10 F01 真实建立镜接回高潮主线`
- 目标：不让 `P10` 继续停在“对手已经是真视频，但公共空间建立还在用静图推近”的半成品状态，而是先把 `F01` 升级成真实动态建立位，再把主装配与整章 master 一起回写

### 主要产出

- [shot-ch01-p10-s01-echo-platform-establishing-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p10-s01-echo-platform-establishing-viduq3-i2v-v1.mp4)
- [shot-ch01-p10-s01-echo-platform-establishing-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p10-s01-echo-platform-establishing-viduq3-i2v-v1.metadata.json)
- [part-10-free-echo-platform-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v2.mp4)
- [chapter-01-vertical-slice-master-v7-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v7-current.mp4)
- [shot-ch01-p10-s01-echo-platform-establishing-viduq3-i2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s01-echo-platform-establishing-viduq3-i2v-v1.json)
- [render_chapter01_part10_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part10_delivery.sh)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P10 / F01` 现在已拿到真实 `qingyun / viduq3-turbo / img2video` 建立镜：
  - `4.04s`
  - `880x588`
  - `24fps`
  - 抽帧差异明确，不是假视频
- 轻量 `W9` 复核结论：
  - 首帧承接成立
  - 没有多余人物、乱字、主持台或擂台化变形
  - 公共空间点亮与轻微前推成立，当前判定为 `PASS WITH NOTES`
- `P10` 正式交付已升级到 [part-10-free-echo-platform-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v2.mp4)
- chapter 级 accepted 审片入口已同步重渲为 [chapter-01-vertical-slice-master-v7-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v7-current.mp4)

### 当前结论

- `P10 / F01`：`PASS WITH NOTES`
  - 当前 notes 收缩到：推近略快，尾帧里城市层被压掉一些，但已足够替代旧 still-motion 建立位
- `P10 delivery v2`：`PASS WITH NOTES`
  - backlog 已从 `F01/F02/F04` 收缩到 `F02/F04`
- active lane 继续保持 `P10`
  - 下一条唯一优先动作是继续判断 `F02/F04` 是否保留 `UI-first` 边界、但换成更动态的同空间承载

## Version `v0.78`

- 日期：`2026-03-31`
- 阶段：`P12 clean retry 收口并切回 P10`
- 目标：把 `P12` 从“尾声已经成立，但 opening clip 仍带本地遮字救援痕迹”的状态再收一刀，换成无后期遮字的 clean retry current；同时把 chapter master 与 source of truth 全部对齐，并把 active lane 正式交回 `P10`

### 主要产出

- [shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v3-cleanretry.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v3-cleanretry.mp4)
- [part-12-digital-mentor-voicefirst-preview-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-voicefirst-preview-v4.mp4)
- [part-12-digital-mentor-delivery-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-delivery-v3.mp4)
- [chapter-01-vertical-slice-master-v6-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v6-current.mp4)
- [render_chapter01_part12_voicefirst_preview.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part12_voicefirst_preview.sh)
- [render_chapter01_part12_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part12_delivery.sh)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P12 / G05` current opening 已从救援遮字版切到无后期遮字的 `viduq3 / start-end2video clean retry`：
  - `4.04s`
  - `880x588`
  - `24fps`
  - 抽帧差异明确，不是假视频
- `P12` 正式交付已升级到 [part-12-digital-mentor-delivery-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-delivery-v3.mp4)：
  - `24.41s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`
- chapter 级 accepted 审片入口已重渲为 [chapter-01-vertical-slice-master-v6-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v6-current.mp4)：
  - `164.17s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`
- current 指针已同步切换：
  - `current/clips/p12-s01-digital-mentor-current.mp4 -> ...viduq3-s2v-v3-cleanretry.mp4`
  - `current/deliveries/part-12-current.mp4 -> ...delivery-v3.mp4`
  - `current/deliveries/chapter-01-master-current.mp4 -> ...master-v6-current.mp4`

### 当前结论

- `P12 / G05 opening clip`：`PASS WITH NOTES`
  - 当前 notes 已从“必须靠本地遮字补丁才能进主线”收缩为“弱投影存在感仍可继续微调”
- `P12 delivery v3`：`PASS WITH NOTES`
  - 当前问题已主要收缩到后半段 `voice-led hold` 的节奏，而不是 opening 是否还成立
- active lane 现在应切回 `P10`
  - 下一条最值得继续清理的债务重新回到 `F01/F02/F04` 的 `still-motion / UI-first` demo 感
  - `P12` 退出 active lane，保留为尾声 notes 区

## Version `v0.77`

- 日期：`2026-03-31`
- 阶段：`P12 弱投影 opening clip 接回尾声主线`
- 目标：把 `P12` 从“整段只靠 clean plate + 声音成立”的 world-in 尾声，推进成“前半段有真实动态接待感、后半段仍保留温和离场”的更正式交付；同时坚持不回到可见正脸导师长讲话

### 主要产出

- [shot-ch01-p12-s01-digital-mentor-return-v4-endframe.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p12-s01-digital-mentor-return-v4-endframe.png)
- [shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v1.mp4)
- [shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v2-salvaged.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v2-salvaged.mp4)
- [shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v2-salvaged.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v2-salvaged.metadata.json)
- [p12-g05-toptext-salvage-overlay-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/ui/p12-g05-toptext-salvage-overlay-v1.png)
- [part-12-digital-mentor-voicefirst-preview-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-voicefirst-preview-v3.mp4)
- [part-12-digital-mentor-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-delivery-v2.mp4)
- [render_chapter01_part12_voicefirst_preview.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part12_voicefirst_preview.sh)
- [render_chapter01_part12_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part12_delivery.sh)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P12 / G05` 已不再是“从头到尾只在同一张 clean plate 上等声音落下”：
  - 开头 4 秒现在由真实 `qingyun / viduq3-turbo / start-end2video` opening clip 接住
  - 后半段继续保留 world-in 的温和离场与问题 overlay，不强行把尾声拍成可见导师正脸讲课
- 这条 opening clip 的上游路线是：
  - `S-09 mentor-space clean plate`
  - 本地补出的 `v4 endframe`
  - `viduq3-turbo / start-end2video`
- provider 首轮返回的 `v1` 虽然有真实动态，但偷偷生成了禁止进入主线的可读英文大字：
  - 因此没有直接回写 current
  - 改为使用 clean-plate 顶部补片做本地救援
  - 收成 [shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v2-salvaged.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p12-s01-digital-mentor-return-viduq3-s2v-v2-salvaged.mp4)
- `G05` 当前 opening clip 的技术结果：
  - `4.04s`
  - `880x588`
  - `24fps`
  - `AAC stereo`
  - 抽帧差异明确，不是假视频
- `P12` 当前正式交付已升级到 [part-12-digital-mentor-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-delivery-v2.mp4)：
  - `24.41s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`
- current 指针已同步切换：
  - `current/deliveries/part-12-current.mp4 -> ...delivery-v2.mp4`
  - `current/clips/p12-s01-digital-mentor-current.mp4 -> ...viduq3-s2v-v2-salvaged.mp4`

### 当前结论

- `P12 / G05 opening clip`：`PASS WITH NOTES`
  - 它已经把尾声从“纯 clean plate”推进成“真实弱投影接待感”
  - 当前 notes 收缩到：这是一条经救援遮字后接回主线的 clip；如果后续还要再升格，优先换掉救援版，而不是回到长讲话人形
- `P12 delivery v2`：`PASS WITH NOTES`
  - 尾声当前已经不再主要像“声音成立了，但画面完全没开始”
  - 当前 notes 收缩到：opening clip 仍是 540p 级成功片，后半段仍保留 hold+overlay 的 story-first 痕迹
- 当前唯一优先下一步收口为：
  1. `P12` 继续保持 active lane，但已不再是纯 clean-plate 债务
  2. 若继续升级，优先补一条不需要本地遮字救援的更干净 opening clip
  3. 在 `P12` 不再明显拖后腿后，再决定是否把活跃 lane 转给 `P10`

## Version `v0.76`

- 日期：`2026-03-31`
- 阶段：`P09 E15 人物连续性修复并回写 current`
- 目标：修复 `Sequence Officer 07` 在 `P08 / E11` 与 `P09 / E15` 之间最明显的人物漂移，把问题先收束在上游首帧与单镜 continuity，而不是直接把换脸当默认路线；同时把修复结果正式写回 `P09 current`，但不抢占当前 `P12` active lane

### 主要产出

- [shot-ch01-p09-s03-evidence-freeze-intervention-v4-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p09-s03-evidence-freeze-intervention-v4-qwen-image-max.png)
- [shot-ch01-p09-s03-evidence-freeze-intervention-v4-endframe.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p09-s03-evidence-freeze-intervention-v4-endframe.png)
- [shot-ch01-p09-s03-evidence-freeze-intervention-viduq3-s2v-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p09-s03-evidence-freeze-intervention-viduq3-s2v-v3.mp4)
- [shot-ch01-p09-s03-evidence-freeze-intervention-viduq3-s2v-v3.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p09-s03-evidence-freeze-intervention-viduq3-s2v-v3.metadata.json)
- [part-09-evidence-freeze-team-split-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-09-evidence-freeze-team-split-delivery-v2.mp4)
- [render_chapter01_part9_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part9_delivery.sh)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 这次确认 `P08 / E11` 与旧 `P09 / E15 current` 的不一致，不只是视频漂移：
  - 旧 `E15` 的上游 keyframe 本身就已经偏离 canonical `07`
  - 因此不能只继续在旧首帧上追加 `img2video`
- `E15` 上游首帧现在已改为新的修复版：
  - 使用 `qingyun` 的 `images` 路线
  - 模型切到 `qwen-image-max-2025-12-30`
  - 先把 `07` 的脸型、发型、银灰制度外套和冷静压迫感重新拉回 `P08 / E11` 线程
- `E15` 当前正式 clip 已切到新的 `start-end2video` 修复路线：
  - `viduq3-turbo`
  - `start-end2video`
  - `canonical portrait + repaired keyframe + endframe`
  - 当前技术结果：
    - `4.04s`
    - `880x588`
    - `24fps`
    - `AAC stereo`
    - 抽帧差异明确，不是静图假视频
- `P09` 当前正式交付已升级到 [part-09-evidence-freeze-team-split-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-09-evidence-freeze-team-split-delivery-v2.mp4)：
  - `17.64s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`
- current 指针已同步切换：
  - `current/clips/p09-s03-evidence-freeze-current.mp4 -> ...viduq3-s2v-v3.mp4`
  - `current/deliveries/part-09-current.mp4 -> ...delivery-v2.mp4`
- loop 主线判断已同步修正：
  - `P09` 维持 `accepted_with_notes`
  - 这次修复不重开中段主线争夺
  - 当前 active part 继续保持 `P12`

### 当前结论

- `P09 / E15`：`PASS WITH NOTES`
  - 新的 `v3` continuity repair 已明显优于旧版 `current`
  - 它已经足够把 `07` 拉回和 `P08 / E11` 同一条角色线程
  - 当前 notes 收缩到：如果后续要更严苛统一，可继续把 `E11` 也抬到同一套 `identity-lock` 口径
- `P09 delivery v2`：`PASS WITH NOTES`
  - 这段现在不再被最明显的 `E15` 换人感拉断
  - `E14 / E16` 仍保留 UI-first，是后续更高一档升级位
- 当前唯一优先下一步收口为：
  1. 保持 `P12` 为唯一 active part
  2. 优先探索尾声从 `voice-first clean plate` 往“极弱存在感视频化”升级
  3. 中段 backlog 只保留 `E11` 进一步 identity-lock 收紧，以及 `E14 / E16` 的正式视频替换

## Version `v0.75`

- 日期：`2026-03-31`
- 阶段：`P11 双 bridge clip 过门并切到 P12`
- 目标：把 `P11` 里最影响结尾体感的 `G03/G04` 从静帧 / overlay 提升成真实动态桥接位，让午夜前选择与回航不再在最后一段重新塌回预告片感，然后把 active lane 顺势切到 `P12`

### 主要产出

- [shot-ch01-p11-s03-petition-status-keyframe-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p11-s03-petition-status-keyframe-v1.png)
- [shot-ch01-p11-s03-petition-status-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p11-s03-petition-status-viduq3-i2v-v1.mp4)
- [shot-ch01-p11-s03-petition-status-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p11-s03-petition-status-viduq3-i2v-v1.metadata.json)
- [shot-ch01-p11-s04-return-archive-mentor-viduq3-s2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p11-s04-return-archive-mentor-viduq3-s2v-v1.mp4)
- [shot-ch01-p11-s04-return-archive-mentor-viduq3-s2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p11-s04-return-archive-mentor-viduq3-s2v-v1.metadata.json)
- [part-11-midnight-choice-return-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-11-midnight-choice-return-delivery-v2.mp4)
- [render_chapter01_part11_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part11_delivery.sh)
- [chapter-01-story-spine-preview-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v4.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `G03` 现在已升级为真实 `qingyun / viduq3-turbo` 制度接收 clip：
  - `3.04s`
  - `880x588`
  - `24fps`
  - 抽帧差异明确，不是静图假视频
- `G04` 现在已升级为真实 `qingyun / viduq3-turbo` 回航桥接 clip：
  - `4.04s`
  - `880x588`
  - `24fps`
  - 抽帧差异明确，不是静图假视频
- `P11` 当前正式交付已升级到 [part-11-midnight-choice-return-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-11-midnight-choice-return-delivery-v2.mp4)：
  - `15.53s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`
- story spine 已同步重装，因此整章完整故事预览现在直接吃到新的 `P11 delivery v2`
- loop 主线已同步切换：
  - `P11 -> accepted_with_notes / delivery v2`
  - `P11` 不再是最高优先假视频债务
  - 下一条 active part 已切到 `P12`

### 当前结论

- `P11`：`PASS WITH NOTES`
  - 这段现在已经不再主要像“结尾又退回静帧桥”
  - notes 收缩到：`G01` 仍偏静态、`G02-G04` 仍是 `540p` 级成功片、`G04` 的导师存在感还可以再温和但更明确
- 当前唯一优先下一步收口为：
  1. 重开 `P12 / G05`
  2. 优先探索极弱存在感的视频化升级，替掉 `voice-first clean plate`
  3. 再决定是否回头定向补 `P11 / G01`

## Version `v0.74`

- 日期：`2026-03-31`
- 阶段：`P02 双 clip 过门并切到 P11`
- 目标：把 `P02` 里最关键的两个正式视频插槽真正补上，让紧急入港校验不再靠场景缩放和纸片桥推动，然后把下一条 active lane 切到终局 still-heavy 段 `P11`

### 主要产出

- [shot-b01-entry-approach-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-b01-entry-approach-viduq3-i2v-v1.mp4)
- [shot-b01-entry-approach-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-b01-entry-approach-viduq3-i2v-v1.metadata.json)
- [shot-b04-entry-bridge-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-b04-entry-bridge-viduq3-i2v-v1.mp4)
- [shot-b04-entry-bridge-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-b04-entry-bridge-viduq3-i2v-v1.metadata.json)
- [part-02-emergency-entry-check-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-02-emergency-entry-check-delivery-v2.mp4)
- [render_chapter01_part2_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part2_delivery.sh)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `B01` 现在已升级为真实 `qingyun / viduq3-turbo` 航线逼近 clip：
  - `4.04s`
  - `880x588`
  - `24fps`
  - 抽帧差异明确，不是静图假视频
- `B04` 现在已升级为真实 `qingyun / viduq3-turbo` 桥接入厅 clip：
  - `4.04s`
  - `880x588`
  - `24fps`
  - 抽帧差异明确，不是静图假视频
- `P02` 当前正式交付已升级到 [part-02-emergency-entry-check-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-02-emergency-entry-check-delivery-v2.mp4)：
  - `22.40s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`
- loop 主线已同步切换：
  - `P02 -> accepted_with_notes`
  - `P02` 不再是最高优先假视频债务
  - 下一条 active part 已切到 `P11 / G01-G04`

### 当前结论

- `P02`：`PASS WITH NOTES`
  - 这段现在已经不再主要像“纸片规则段”
  - notes 收缩到：`B01` 的制度压迫感还能再收、`B04` 的门槛桥接还可更强、`B02/B03` 继续保持 UI-first
- 当前唯一优先下一步收口为：
  1. 重开 `P11 / G01-G04`
  2. 优先把 `G03/G04` 升成真实桥接位
  3. 再判断是否需要补 `G01`

## Version `v0.73`

- 日期：`2026-03-31`
- 阶段：`P05 D02 真实 clip 过门并切到 P02`
- 目标：把 `P05` 中最明显的 `scene still + overlay` 位真正替换成真实短视频段，让概率长廊不再像“在同一张图上读说明”，并把下一条 active lane 正式交给 `P02 / B01-B04`

### 主要产出

- [shot-ch01-p05-s02-path-comparison-keyframe-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p05-s02-path-comparison-keyframe-v1.png)
- [shot-ch01-p05-s02-path-comparison-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p05-s02-path-comparison-viduq3-i2v-v1.mp4)
- [shot-ch01-p05-s02-path-comparison-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p05-s02-path-comparison-viduq3-i2v-v1.metadata.json)
- [part-05-probability-corridor-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-05-probability-corridor-delivery-v2.mp4)
- [render_chapter01_part5_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part5_delivery.sh)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `D02` 现在已经不再只是 `scene still + overlay`：
  - 通过 `S-04 + D02 overlay` 合成首帧，先锁住“同一空间中的路径比较”
  - 再用 `qingyun / viduq3-turbo / img2video` 推进成真实短 clip
- `D02` 当前技术门结果：
  - `3.04s`
  - `880x588`
  - `24fps`
  - 抽帧差异明确，不是静图假视频
- `P05` 当前正式交付已升级到 [part-05-probability-corridor-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-05-probability-corridor-delivery-v2.mp4)：
  - `9.13s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`
- loop 主线已同步切换：
  - `P05 -> accepted_with_notes`
  - `P05` 不再是最高优先假视频债务
  - 下一条 active part 已切到 `P02 / B01-B04`

### 当前结论

- `P05`：`PASS WITH NOTES`
  - 概率长廊现在已经不再主要卡在“这段是不是静态说明页”
  - notes 收缩到：`D01` 的奇观气质、`D02` 是否需要更长比较节奏、`D04` 的余光桥接感
- 当前唯一优先下一步收口为：
  1. 重开 `P02 / B01-B04`
  2. 优先补 `B01 / B04` 的正式视频插槽
  3. 再判断 `B02 / B03` 是否继续留在 UI-first

## Version `v0.72`

- 日期：`2026-03-31`
- 阶段：`P06 假视频债务清理完成并切到 P05`
- 目标：把 `P06` 从“仍靠静帧 / rescue clip 撑住结构”的 backlog 位，推进成 `E01-E04` 都为真实动态镜头的正式 part-level 交付，并把下一条 active lane 明确切到 `P05 / D02`

### 主要产出

- [shot-ch01-p06-s01-dark-layer-ingress-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p06-s01-dark-layer-ingress-viduq3-i2v-v1.mp4)
- [shot-ch01-p06-s02-waveform-puzzle-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p06-s02-waveform-puzzle-viduq3-i2v-v1.mp4)
- [shot-ch01-p06-s03-hidden-path-reveal-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p06-s03-hidden-path-reveal-viduq3-i2v-v1.mp4)
- [shot-ch01-p06-s04-wind-listener-recording-interface-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p06-s04-wind-listener-recording-interface-viduq3-i2v-v1.mp4)
- [render_chapter01_part6_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part6_delivery.sh)
- [part-06-dark-layer-interface-delivery-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-06-dark-layer-interface-delivery-v4.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P06 / E01-E04` 现在都已经有真实动态短 clip：
  - `E01 / 进入暗层`
  - `E02 / 波形解谜`
  - `E03 / 第四路径显形`
  - `E04 / 风声婆婆旧录音界面`
- `P06` 当前不再存在“只剩一条 rescue clip 顶主线”的状态：
  - `E03` 已由正式 `viduq3-turbo` clip 接管
  - `E01/E02/E04` 也不再停留在静帧晃动或纯 overlay 假视频
- [part-06-dark-layer-interface-delivery-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-06-dark-layer-interface-delivery-v4.mp4) 当前规格：
  - `14.17s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`
- loop 判断已同步更新：
  - `P06 -> accepted_with_notes`
  - `P06` 不再属于最高优先 `假视频替换债务`
  - 下一条 active part 已切到 `P05 / D02`

### 当前结论

- `P06`：`PASS WITH NOTES`
  - 这段当前已经脱离“拿静态图晃动几下冒充视频”的高风险区
  - notes 主要转为节奏、声场与 `P05 -> P06 -> P07` 连续性，而不是“这四镜是否真的存在”
- 当前唯一优先下一步收口为：
  1. 重开 `P05 / D02`
  2. 把“路径比较”从同图 UI 说明层升级成真实短视频段
  3. 然后再继续回到 `P02 / B01-B04`

## Version `v0.70`

- 日期：`2026-03-31`
- 阶段：`P08 独立交付收口并切换到 P09`
- 目标：把 `P08` 从“只有入口与单句立场”推进到真正可独立审片的制度段，然后把 active part 正式交给 `P09`

### 主要产出

- [shot-ch01-p08-s03-sequence-officer-stance-v1-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p08-s03-sequence-officer-stance-v1-qwen-image-max.png)
- [shot-ch01-p08-s03-sequence-officer-stance-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p08-s03-sequence-officer-stance-viduq3-i2v-v1.mp4)
- [part-08-rule-projection-room-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-08-rule-projection-room-delivery-v1.mp4)
- [part-08-rule-projection-room-delivery-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-08-rule-projection-room-delivery-v1.metadata.json)
- [part-08-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/deliveries/part-08-current.mp4)
- [render_chapter01_part8_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part8_delivery.sh)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- `E11 / P08-S03` 已推进成真实 speaking clip，不再只靠 `P10` 的后置对抗去替他补立场
- `P08` 当前已经形成 4 拍独立制度段：
  - `E09 / 规则室建立`
  - `E10 / 制度模型展开`
  - `E11 / 07 压实立场`
  - `E12 / 立场预回应`
- `part-08-rule-projection-room-delivery-v1.mp4` 当前规格：
  - `16.68s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`

### 当前结论

- `P08`：`PASS WITH NOTES`
  - 这段现在已经能独立审片，不再只是 `bridge v3` 里的过渡论点
  - notes 主要收缩到：`E10 / E12` 目前仍是 UI-first 低风险路线，后续可继续替换成更强正式视频位
- 当前 loop 已正式切换：
  - `P08 -> accepted_with_notes`
  - `P09 -> in_progress`
- 当前唯一优先下一步收口为：
  - 继续补 `P09 / E15 / E17`

## Version `v0.69`

- 日期：`2026-03-31`
- 阶段：`P07 独立交付收口并切换到 P08`
- 目标：把 `P07` 从“已经有三条好镜头”推进到真正可独立审片的 part-level 交付，然后把 active part 正式切给 `P08`

### 主要产出

- [shot-ch01-p07-s04-wind-tag-listening-v1-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p07-s04-wind-tag-listening-v1-qwen-image-max.png)
- [shot-ch01-p07-s04-wind-tag-listening-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p07-s04-wind-tag-listening-viduq3-i2v-v1.mp4)
- [part7-v1-wind-listener-shortline.mp3](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part7-v1-wind-listener-shortline.mp3)
- [part-07-silent-practice-room-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-07-silent-practice-room-delivery-v1.mp4)
- [part-07-silent-practice-room-delivery-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-07-silent-practice-room-delivery-v1.metadata.json)
- [part-07-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/deliveries/part-07-current.mp4)
- [render_chapter01_part7_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part7_delivery.sh)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- `E08 / P07-S04` 已推进成真实 short clip，不再把 `P07` 的停留段继续留给静态补位
- `E07` 的短句音频也已正式落盘，当前 `P07` 不再只是“承载体准备好了”
- 当前 `P07` 已形成 4 镜独立交付：
  - `E05 / 入口`
  - `E06 / 生活痕迹`
  - `E07 / 旧见证短线`
  - `E08 / 停下来听`
- `part-07-silent-practice-room-delivery-v1.mp4` 当前规格：
  - `13.17s`
  - `1152x768`
  - `30fps`
  - `AAC stereo`

### 当前结论

- `P07`：`PASS WITH NOTES`
  - 这段现在已经可独立审片，不再只是 bridge preview 的组成零件
  - notes 主要收缩到：`E08` 仍偏 scene-state 交互位，后续还可继续加强“林澄安静反应”尾拍
- 当前 loop 已正式切换：
  - `P07 -> accepted_with_notes`
  - `P08 -> in_progress`
- 当前唯一优先下一步收口为：
  - 继续补 `P08 / E11`
  - 再决定 `E10 / E12` 是否继续停留 UI-first

## Version `v0.68`

- 日期：`2026-03-31`
- 阶段：`P07 E07 旧录音承载体 clip`
- 目标：先把风声婆婆短线的视觉承载体成立，不冒然做完整说话人脸，让 `P07` 的理解入口继续往正式视频链推进

### 主要产出

- [shot-ch01-p07-s03-wind-listener-carrier-v2-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p07-s03-wind-listener-carrier-v2-qwen-image-max.png)
- [shot-ch01-p07-s03-wind-listener-carrier-v2-qwen-image-max.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/shots/shot-ch01-p07-s03-wind-listener-carrier-v2-qwen-image-max.metadata.json)
- [shot-ch01-p07-s03-wind-listener-carrier-viduq3-i2v-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p07-s03-wind-listener-carrier-viduq3-i2v-v2.mp4)
- [shot-ch01-p07-s03-wind-listener-carrier-viduq3-i2v-v2.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p07-s03-wind-listener-carrier-viduq3-i2v-v2.metadata.json)
- [p07-s03-wind-listener-carrier-current.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/shots/p07-s03-wind-listener-carrier-current.png)
- [p07-s03-wind-listener-carrier-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p07-s03-wind-listener-carrier-current.mp4)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- `E07 / P07-S03` 已经从高风险 speaking shot 回退为 `carrier-first` 路线，并拿到真实动态 clip
- 本轮实战结论也更清楚了：
  - `qwen-image-max / chat anchor` 在这镜上因 content 参数报错，不值得继续硬耗
  - `qwen-image-max / prompt-only rescue` 可以更稳地把承载体首帧先做出来
  - `viduq3-turbo / img2video` 仍可把这类无脸、低动作、短呼吸镜头推进成真实短 clip
- `E07` 轻量技术门结果：
  - `3.04s`
  - `880x588`
  - `24fps`
  - 抽帧差异明显，不是静图假视频
- 当前 `P07` 已经连续拿到：
  - `E05 / 入口`
  - `E06 / 生活痕迹`
  - `E07 / 旧见证承载体`
  三条真实短 clip

### 当前结论

- `E07 / P07-S03`：`PASS WITH NOTES`
  - 当前已经能承担“旧见证即将落下一句短线”的视觉职责
  - 但还没有把正式短句音频挂进来，因此不能误判成完整通过的 speaking beat
- 当前唯一优先下一步收口为：
  - 先补 `E07` 的短句音频合同
  - 再补 `E08`
  - 然后进入 `P07` part-level assembly

## Version `v0.67`

- 日期：`2026-03-31`
- 阶段：`P07 E06 真实物件痕迹 clip`
- 目标：不让 `P07` 继续只靠入口气氛成立，而是把“第四路径有人真的在这里长期练习过”推进成真实短 clip

### 主要产出

- [shot-ch01-p07-s02-old-practice-traces-v1-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p07-s02-old-practice-traces-v1-qwen-image-max.png)
- [shot-ch01-p07-s02-old-practice-traces-v1-qwen-image-max.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/shots/shot-ch01-p07-s02-old-practice-traces-v1-qwen-image-max.metadata.json)
- [shot-ch01-p07-s02-old-practice-traces-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p07-s02-old-practice-traces-viduq3-i2v-v1.mp4)
- [shot-ch01-p07-s02-old-practice-traces-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p07-s02-old-practice-traces-viduq3-i2v-v1.metadata.json)
- [p07-s02-old-practice-traces-current.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/shots/p07-s02-old-practice-traces-current.png)
- [p07-s02-old-practice-traces-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/clips/p07-s02-old-practice-traces-current.mp4)
- [p07-s02-old-practice-traces-current.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/current/images/p07-s02-old-practice-traces-current.json)
- [p07-s02-old-practice-traces-current.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/current/videos/p07-s02-old-practice-traces-current.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- `E06 / P07-S02` 已经从缺失位推进成真实短 clip，不再停留在“后面再补”的空槽位
- 当前路线继续验证成立：
  - `qwen-image-max` 可承担 `P07` 物件痕迹首帧
  - `viduq3-turbo / img2video` 可把这种对象焦点位推进成真实动态短片
- `E06` 轻量技术门结果：
  - `3.04s`
  - `880x588`
  - `24fps`
  - provider 附带 `AAC stereo`
- 当前抽帧 hash 与帧间均值差已确认存在明确时间变化，不是“静图晃两下”的伪视频
- `P07` 现在不再只有 `E05` 的入口气氛，而开始具备“这条路曾被人真实走过”的生活痕迹承重

### 当前结论

- `E06 / P07-S02`：`PASS WITH NOTES`
  - 已可进入 `current/clips`
  - 但仍需要和后续 `E07 / E08` 连起来判断整段呼吸与理解节奏
- 当前唯一优先下一步收口为：
  - 继续补 `E07 / E08`
  - 先把 `P07` 收成可独立成立的正式 part-level 人性理解段
  - 再进入 `P08 / E11`

## Version `v0.66`

- 日期：`2026-03-31`
- 阶段：`P07-P09 首轮正式 clip 与 story spine v3`
- 目标：不再让中段只停留在首帧与纸片桥，而是先把最关键的三条入口位真正升级成正式短 clip，再把它们塞回整章 spine 验证故事流畅度

### 主要产出

- [shot-ch01-p07-s01-silent-room-ingress-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p07-s01-silent-room-ingress-viduq3-i2v-v1.mp4)
- [shot-ch01-p08-s01-rule-projection-room-establishing-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p08-s01-rule-projection-room-establishing-viduq3-i2v-v1.mp4)
- [shot-ch01-p09-s01-evidence-auth-choice-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p09-s01-evidence-auth-choice-viduq3-i2v-v1.mp4)
- [part-07-09-middle-bridge-papercut-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-07-09-middle-bridge-papercut-v3.mp4)
- [chapter-01-story-spine-preview-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v3.mp4)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- `E05 / E09 / E13` 已经从 `current/shots` 正式推进到 `current/clips`
- 这三条 clip 都通过了轻量技术门：
  - `3.04s`
  - `880x588`
  - `24fps`
  - `AAC stereo`
- 当前判断它们不是“静图晃两下”的伪视频，而是可以承担正式入口职责的真实短 clip
- `P07-P09 middle bridge` 已推进到 `v3`
  - 不再只是纯静帧 bridge
  - 已正式接入 `E05 / E09 / E13`
- `chapter-01 story spine preview` 已推进到 `v3`
  - 当前成为这章最完整的故事流畅度预览入口
  - 但仍不替代 `chapter-01 master current`

### 当前结论

- `E05 / P07-S01`：`PASS`
- `E09 / P08-S01`：`PASS WITH NOTES`
- `E13 / P09-S01`：`PASS`
- `P07-P09 bridge v3`：`PASS WITH NOTES`
- `chapter-01 story spine preview v3`：`PASS WITH NOTES`
- 当前唯一优先下一步收口为：
  - 把 `P07` 设为当前 active part，继续补 `E06 / E07 / E08`
  - 然后推进 `P08` 的 `E11`
  - 再推进 `P09` 的 `E15 / E17`
  - 目标不再是“证明中段该不该补”，而是把 `P07-P09` 真正收成 part-level delivery

## Version `v0.65`

- 日期：`2026-03-31`
- 阶段：`P07-P09 关键首帧落地`
- 目标：既然 `P07-P09` 的正式 shot contract 已经补齐，就不再停在文档层，而是把最影响中段可视化推进的 4 个关键镜头先落成可用首帧

### 主要产出

- [shot-ch01-p07-s01-silent-room-ingress-v2-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p07-s01-silent-room-ingress-v2-qwen-image-max.png)
- [shot-ch01-p08-s01-rule-projection-room-establishing-v2-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p08-s01-rule-projection-room-establishing-v2-qwen-image-max.png)
- [shot-ch01-p09-s01-evidence-auth-choice-v3-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p09-s01-evidence-auth-choice-v3-qwen-image-max.png)
- [shot-ch01-p09-s05-team-split-v3-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p09-s05-team-split-v3-qwen-image-max.png)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 当前已经把 `P07-P09` 从“只有 bridge preview”推进到“已有 current 首帧锚点”
- 新增并挂到 `current/images/` 的模板入口：
  - `p07-s01-silent-room-current.json`
  - `p08-s01-rule-room-current.json`
  - `p09-s01-evidence-auth-current.json`
  - `p09-s05-team-split-current.json`
- 新增并挂到 `current/shots/` 的首帧入口：
  - `p07-s01-silent-room-current.png`
  - `p08-s01-rule-room-current.png`
  - `p09-s01-evidence-auth-current.png`
  - `p09-s05-team-split-current.png`
- 路由判断也更清楚了：
  - 旧本机提取的青云 key 当前已确认 `额度已用尽`
  - 用户提供的青云 key 已通过 `GET /v1/models = 200`
  - `qwen-image-max / chat` 在这组模板上出现 `content parameter length invalid / limit_requests`
  - 本轮正式通过项来自更保守的 `qwen-image-max / images` prompt-only 救援线

### 当前结论

- `E05 / P07-S01`：`PASS`
- `E09 / P08-S01`：`PASS WITH NOTES`
- `E13 / P09-S01`：`PASS`
- `E17 / P09-S05`：`PASS WITH NOTES`
- 当前唯一优先下一步收口为：
  - 先用 `E05 / E09 / E13` 进入视频导演与 clip 试生
  - `E17` 先继续收一版更克制的关系首帧，或直接做低动作群像试片

## Version `v0.64`

- 日期：`2026-03-31`
- 阶段：`P07-P09 正式 shot contract 回写`
- 目标：既然 `story spine v2` 已证明中段补桥值得保留，就不再让它停留在 preview 判断层，而是直接把 `P07-P09` 写回正式执行链，避免产线继续从 `P06` 硬跳 `P10`

### 主要产出

- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `shot-list.md` 现在已正式补回：
  - `P07 / E05-E08`
  - `P08 / E09-E12`
  - `P09 / E13-E17`
- 同时新增中段交互节点：
  - `N05A` 风名标签探索
  - `N05B` 规则模型查看
  - `N05C` 立场预回应
  - `N05D` 证据整理权限选择
- 这次回写不是为了把 preview 假装变成 accepted 视频，而是为了把导演判断转成真正可执行的 production chain
- `flow-vertical-slice-pack.md` 与主 HTML 已同步改口：
  - 故事判断仍是 `PASS WITH NOTES`
  - 但“下一步”已不再是抽象审片，而是直接推进 `E05 / E09 / E13 / E17` 的关键首帧与正式 clip 升级

### 当前结论

- 当前最重要的进展不是又多了一条 preview，而是 `P07-P09` 终于不再缺席正式执行清单
- 从现在开始，chapter-01 的中段不能再被默认当成“以后再说的 bridge backlog”
- 后续真正的唯一下一步已经收口为：
  - 先补 `E05 / E09 / E13 / E17` 的 scene-state / keyframe
  - 再进入 `P07-P09` 的正式视频替换
  - `accepted spine` 与 `current` 继续保持不变，直到中段拿到可过 gate 的正式段落

## Version `v0.61`

- 日期：`2026-03-30`
- 阶段：`P10 F03 正式 clip 过门并回写主 spine`
- 目标：既然 `P10 / F03` 已拿到第一条真实可用的正式短 clip，就不再把它停留在 archive 里当旁证，而是直接接进 `part-10 current delivery` 与 chapter master current

### 主要产出

- [shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.mp4)
- [shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.metadata.json)
- [render_chapter01_part10_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part10_delivery.sh)
- [part-10-free-echo-platform-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v1.mp4)
- [part-10-free-echo-platform-delivery-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-10-free-echo-platform-delivery-v1.metadata.json)
- [chapter-01-vertical-slice-master-v4-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v4-current.mp4)
- [chapter-01-vertical-slice-master-v4-current.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-vertical-slice-master-v4-current.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 用新注入且已通过最小鉴权的外部 Qingyun key，真实拿到 `P10 / F03` 的第一条成功正式视频：
  - `viduq3-turbo`
  - `img2video`
  - `3.04s`
  - `880x588`
  - `24fps`
  - `AAC audio`
- 当前已完成 `W9` 轻量 QC，确认：
  - 首帧承接成立
  - `序列员 07` 身份稳定，没有换脸、乱站位或多余人物
  - 这条片子不再是“图片晃几下”，而是存在明确的微动作与口型段
- `render_chapter01_part10_delivery.sh` 已不再引用旧 `F03 rescue clip`，而是直接吃进这条新的 `viduq3` 正式 clip
- `part-10 delivery v1` 的音轨也已同步改为接入 `F03` 原始短句人声，不再保留“画面里嘴在动、成片里只有提示音”的装配硬伤
- `part-10 delivery v1` 已在保留 `F01/F02/F04` 既有结构的前提下完成重渲，因此：
  - `P10` 仍是 `PASS WITH NOTES`
  - 但 notes 已从“高潮段还在用 rescue clip”收缩为“`F01/F02/F04` 仍带静帧 / UI-first 气质”
- 章节级 master 也已同步重渲为 `v4-current`，避免整章审片继续看到旧 `P10` 版本
- `video-loop-state.json` 已把 `current_focus_part` 正式切到 `P06`，因为 `P10 / F03` 的最高优先替换债务已经完成

### 当前结论

- `P10 / F03 viduq3 formal clip`：`PASS WITH NOTES`
- 当前最重要的制作判断：
  - `P10` 已不再是“没有正式动态对手”的高潮段
  - 但这不等于青云已经形成稳定模型池；更准确地说，是当前已明确拿到 `1` 个成功正式通过项，而不是“30 模型都不行”
  - loop 主线现在应把主要注意力移到 `P06` 的 `E03 rescue clip` 替换债务

## Version `v0.56`

- 日期：`2026-03-30`
- 阶段：`Chapter-01 master current 对齐到 P03 v2`
- 目标：既然 `P03 current delivery` 已切到 `v2`，章节级 spine 也必须同步到同一口径，避免内部审片继续看到旧版 `P03` 混在线里

### 主要产出

- [render_chapter01_vertical_slice_master.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_vertical_slice_master.sh)
- [chapter-01-vertical-slice-master-v3-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v3-current.mp4)
- [chapter-01-vertical-slice-master-v3-current.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-vertical-slice-master-v3-current.metadata.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 重新按当前 accepted spine 装出新的章节级 master：
  - `P01-P06`
  - `P10-P12`
  - 其中 `P03` 已自动读取新的 `delivery v2`
- 当前 master 输出规格复核为：
  - `1152x768`
  - `30fps`
  - `AAC stereo`
  - `168.02s`
- dated current 目录已补出稳定入口：
  - `current/deliveries/chapter-01-master-current.mp4`
- 主 HTML 已增加 chapter-level master current 链接，后续整章审片不再需要手翻版本号

### 当前结论

- `chapter-01 master v3 current`：`PASS WITH NOTES`
- 当前最重要的意义：
  - 它已经与最新 `P03 current delivery v2` 对齐
  - 现在可以直接用稳定入口连续审整条 vertical slice
  - 它仍然是 `story-first vertical slice master`，不是完整 demo 或最终单集封版

## Version `v0.55`

- 日期：`2026-03-30`
- 阶段：`P03 delivery v2 提升并回写 current`
- 目标：既然 `P03 relation paper cut` 已在章节级 override 审片里证明关系更清楚，就不再把它停留在“待决定对照”，而是正式收成 `P03 current delivery v2`，用最小成本提升 chapter spine 的人物关系可读性

### 主要产出

- [render_chapter01_part3_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part3_delivery.sh)
- [part-03-archive-hall-pressure-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-03-archive-hall-pressure-delivery-v2.mp4)
- [part-03-archive-hall-pressure-delivery-v2.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-03-archive-hall-pressure-delivery-v2.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `render_chapter01_part3_delivery.sh` 现在明确把 `relation paper cut v1` 收口成：
  - `part-03-archive-hall-pressure-delivery-v2.mp4`
  - 对应 metadata 同步写入 `delivery v2` 的 story-clear 说明
- `P03 delivery v2` 已通过当前统一交付规格复核：
  - `1152x768`
  - `30fps`
  - `AAC stereo`
  - `19.04s`
- 这次升级的真实含义被明确限定为：
  - 它是 `relation-led low-cost reassembly`
  - 它优先修正 `C02/C04` 的关系理解和信息顺序
  - 它不是“已经拿到更强正式 clip 的 P03 最终冻结版”
- `video-loop-state.json` 已把 `P03` accepted delivery 从 `v1` 切到 `v2`，并把 gate 回写为 `W11`
- 主 HTML 与 current 指针随后一起对齐到 `delivery v2`

### 当前结论

- `P03 delivery v2`：`PASS WITH NOTES`
- 当前最重要的制作判断：
  - 这次提升已经足够作为 `P03` 的 current 入口
  - 但后续若要继续升格，仍然只该针对 `C02/C04` 的正式 clip 做定向升级
  - `C01` 大厅锚点继续保持冻结，不重开

## Version `v0.54`

- 日期：`2026-03-30`
- 阶段：`Chapter-01 master v2 P03 override 对照`
- 目标：不只在单段里判断 `P03 relation paper cut` 有没有改善，而是把它真的放回 chapter spine，看它对整条 vertical slice 的可读性影响

### 主要产出

- [render_chapter01_vertical_slice_master.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_vertical_slice_master.sh)
- [chapter-01-vertical-slice-master-v2-p03-relation.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v2-p03-relation.mp4)
- [chapter-01-vertical-slice-master-v2-p03-relation.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-vertical-slice-master-v2-p03-relation.metadata.json)

### 核心变化

- `render_chapter01_vertical_slice_master.sh` 现在支持：
  - `MASTER_TAG`
  - `P03_SOURCE_OVERRIDE`
- 基于这个 override 口径，新生成了一条章节级对照 master：
  - 用 `part-03-archive-hall-relation-papercut-v1.mp4` 替换原来的 current `P03`
  - 其余 `P01-P06、P10-P12` 仍沿用 current delivery
- 当前对照 master 的实际输出规格为：
  - `1152x768`
  - `30fps`
  - `AAC stereo`
  - `168.02s`
- 这条对照 master 的职责被明确限制为：
  - 只用于判断 `P03` 关系补强是否值得继续推进
  - 不自动提升为新的 current hub
  - 不直接等同于 `chapter-01 vertical slice master v2` 正式主入口

### 当前结论

- `chapter-01-vertical-slice-master-v2-p03-relation`：`PASS WITH NOTES`
- 当前最有价值的判断：
  - `P03 relation paper cut` 已值得进入 chapter 级对照审片
  - 后续若人工审片确认提升明显，`P03` 应优先进入 `delivery v2` 低成本重装配讨论
  - 在这个判断完成前，不需要重开其他 parts

## Version `v0.53`

- 日期：`2026-03-30`
- 阶段：`P03 relation paper cut 补强`
- 目标：不在 `P03` 还没拿到更强正式 clip 前盲目重开 delivery，而是先用正确的人物锚点和信息顺序做一条低成本关系预览，确认当前真正缺的是关系位而不是大厅建立位

### 主要产出

- [render_chapter01_part3_relation_papercut.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part3_relation_papercut.sh)
- [part-03-archive-hall-relation-papercut-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-03-archive-hall-relation-papercut-v1.mp4)
- [part-03-archive-hall-relation-papercut-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-03-archive-hall-relation-papercut-v1.metadata.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)

### 核心变化

- 明确把 `P03` 当前最影响章节理解的短板钉死为：
  - `C02` 缺少 dedicated hall-anchored relation beat
  - `C04` 需要更明确地承担“07 先合法赢一小步”的压迫位
- 新增 `render_chapter01_part3_relation_papercut.sh`，只使用当前已通过身份门的正确资产：
  - `hall-triangle v7`
  - `Lin Cheng question keyframe v2 salvage crop`
  - `Sequence Officer pressure keyframe v1`
  - 已有调查层 / 驳回层 overlay
- 当前这条 `relation papercut` 的职责被刻意限制为：
  - 验证 `P03` 的人物关系可读性与信息顺序
  - 不假装已经拿到新的正式 visible-speech clip
  - 不替代 `part-03-archive-hall-pressure-delivery-v1.mp4` 的 current 入口
- 当前得到的直接制作结论是：
  - `P03` 的下一步依然应优先补 `C02/C04`
  - 不是回头重开 `C01`
  - 也不是继续把 `P01/S06` 的旧争议切片借给大厅段凑近景

### 当前结论

- `part-03-archive-hall-relation-papercut-v1`：`PASS WITH NOTES`
- 当前 notes：
  - 这仍是 low-cost paper cut，不是新正式交付
  - 如果后续决定升格，应该把这条预览当作 `P03 delivery v2` 的导演和编辑依据，而不是直接回写 current
- 下一步重点：
  - 先人工审这条 relation paper cut 是否明显优于当前 `P03 delivery v1` 的 `C02/C04` 关系理解
  - 若结论成立，再决定走：
    - `正式 clip 替换`
    - 或 `delivery v2` 的低成本结构重装配

## Version `v0.52`

- 日期：`2026-03-30`
- 阶段：`Chapter-01 vertical slice master 装配`
- 目标：不让 `chapter-01` 在“各 part 都有了，但还没有一条章节级 master spine 可供连续审片”的状态继续停留，而是先收出一条不改 current hub 的可审母带

### 主要产出

- [render_chapter01_vertical_slice_master.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_vertical_slice_master.sh)
- [chapter-01-vertical-slice-master-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v1.mp4)
- [chapter-01-vertical-slice-master-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-vertical-slice-master-v1.metadata.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)

### 核心变化

- 新增 `render_chapter01_vertical_slice_master.sh`，直接读取 [outputs/current-chapter-01/deliveries](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/current-chapter-01/deliveries) 的当前 accepted parts：
  - `P01-P06`
  - `P10-P12`
- 当前 master 不重做 part 内部结构、不回写 current hub，只做章节级顺接装配，输出统一规格：
  - `1152x768`
  - `30fps`
  - `AAC stereo`
  - `171.34s`
- 这次章节级连续审片也正式把当前 spine 的定位钉死：
  - 它已经是 `story-first vertical slice master`
  - 但还不能误称为“完整 demo”或“最终单集封版”
  - 当前 `P07-P09` 仍不在视频主线 scope 内
- 当前最值钱的 backlog 已从“再去把每个 part 都做得更像成片”收敛为三类：
  - `P01 / P12`：展示版可进一步收尾时长
  - `P03`：人物关系近景仍是最值得优先升级的剧情理解位
  - `P06 / P10`：后半段 rescue clip 若 provider 恢复，再定向替换，不整段重开

### 当前结论

- `chapter-01 vertical slice master v1`：`PASS WITH NOTES`
- 当前 master 的职责：
  - 给章节级连续审片与展示版收口提供稳定入口
  - 不取代 part-level source of truth
  - 不自动提升为 `outputs/current-chapter-01` 的 current 主入口
- 下一步重点：
  - 先做展示版收刀，而不是重开 chapter 主线
  - 优先顺序：`P03` 关系补强 > `P01/P12` 时长收口 > `P06/P10` rescue clip 替换窗口
  - 如后续要扩成更完整 demo，应先明确 `P07-P09` 是否进入视频主线，再决定是否重开 chapter master

## Version `v0.51`

- 日期：`2026-03-29`
- 阶段：`P12 正式交付收口并完成 chapter loop`
- 目标：不让 `chapter-01` 停在“最后一段已经成立，但仍挂着 preview / W7”的半完成状态，而是把 `P12` 真正收成首版交付，并同步回写所有 source of truth

### 主要产出

- [render_chapter01_part12_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part12_delivery.sh)
- [part12-v1-digital-mentor-contract.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part12-v1-digital-mentor-contract.aiff)
- [part-12-digital-mentor-voicefirst-preview-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-voicefirst-preview-v2.mp4)
- [part-12-digital-mentor-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-delivery-v1.mp4)
- [part-12-digital-mentor-delivery-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-12-digital-mentor-delivery-v1.metadata.json)
- [voice-first-round-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-first-round-pack.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P12` 的正式声音合同已从“仅做节奏验证”的状态推进为当前首版可交付口径：
  - voice: `zh-CN-XiaoxiaoNeural`
  - 语气：温和、平视、非课堂
  - 形态：`clean plate + voice-first + 轻问题 overlay`
- `part-12-digital-mentor-voicefirst-preview-v2.mp4` 不再只是过门试看片，而是被正式提升为 [part-12-digital-mentor-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-delivery-v1.mp4) 的首版母带。
- `video-loop-state.json` 已把 `P12` 从 `W7 / in_progress` 推进到 `W11 / accepted_with_notes`，因此 `chapter-01` 当前纳入 loop 的 `P01-P06、P10-P12` 已全部进入完成态。
- 当前明确保留的 notes：
  - `C-08` 数字导师仍未进入稳定锁形，因此首版继续坚持 `voice-first`，不假装已经拥有可用正脸导师视频
  - 如后续要升级，只允许补极弱世界内导师界面，或单独开启 `C-08` 锁形任务；不重开 `P12` 主线去盲长人形

### 当前结论

- `P12`：`accepted_with_notes / PASS WITH NOTES / W11`
- `chapter-01` 当前 loop：首版已全链路跑通
- 下一步重点：从“把每个 part 都跑出来”切换到“按 backlog 定向升级最值钱的局部位”

## Version `v0.47`

- 日期：`2026-03-29`
- 阶段：`P11 正式 clip 过门并交付`
- 目标：不让 `P11` 停在“单镜终于成功，但整段仍没有正式交付”的中间态，而是把 `G02` 的成功 clip 真正推进到 `W9 -> W10 -> W11`

### 主要产出

- [shot-ch01-p11-s02-lin-final-speech-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p11-s02-lin-final-speech-viduq3-i2v-v1.mp4)
- [shot-ch01-p11-s02-lin-final-speech-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p11-s02-lin-final-speech-viduq3-i2v-v1.metadata.json)
- [render_chapter01_part11_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part11_delivery.sh)
- [part-11-midnight-choice-return-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-11-midnight-choice-return-delivery-v1.mp4)
- [part-11-midnight-choice-return-delivery-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-11-midnight-choice-return-delivery-v1.metadata.json)
- [chapter01_loop_driver.py](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/chapter01_loop_driver.py)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `qingyun / viduq3-turbo` 已真实为 `G02` 出片，不再停留在“只知道某条 loop 存在，但主线还没吃进去”的状态
- 对 `G02` 完成了轻量 `W9` 审核：
  - 首帧承接成立，人物脸型、发型、服装和年龄感都没有明显漂移
  - 画面里没有多余人物、乱字幕或胜利式表演腔
  - 音轨已存在，足以承担当前 `story-first` 的正式人物陈词职责
- 新增 `render_chapter01_part11_delivery.sh`，把 `G01 still + G02 正式 clip + G03 UI-first + G04 bridge` 收成 `part-11-midnight-choice-return-delivery-v1.mp4`
- 顺手补齐 `chapter01_loop_driver.py --sync-current` 的 stable current hub 映射，让 `outputs/current-chapter-01/chapter-01-preview.html` 在 HTTP 预览下也能正确加载 `characters / scenes / videos / current` 目录，而不是只在本地文件语义下勉强可用
- `P11` 当前结论：
  - 已可提升为 `accepted_with_notes`
  - 当前 notes 主要集中在：`G03/G04` 仍是低成本 UI / bridge 口径，`G02` 也仍是 `540p` 成功片而非更高分辨率升级版
  - 这些 notes 不再阻塞 chapter-01 主线切到 `P12`

## Version `v0.48`

- 日期：`2026-03-29`
- 阶段：`P12 导演室与单镜收束合同`
- 目标：不让 `P12` 回到旧版“4 镜 + 60-90 秒总结”的课堂化路径，而是先把数字导师压成能接住余韵的单镜收束方案

### 主要产出

- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `P12` 的导演问题被重新定义为：
  - 不是“导师要不要再讲长一点”
  - 而是“怎样在世界内把孩子接住，再温和离场”
- 旧版 `P12 / S01-S04` 已压缩为单镜 `G05`
  - 时长改为 `18-24 秒`
  - 内部只保留 3 个 beat：接住情绪、抽出命题、留下问题
- 基于当前资产现实，`C-08` 未锁形前不直接进入清晰正脸讲话视频
  - 首版先走 `S-09 mentor-space clean plate + 柔和投影 / 半身轮廓 + 配音` 的安全路线
  - 等 `C-08` 锁定成功后，再考虑升级为 face-forward 收束镜头
- 当前结论：
  - `P12` 的 `W1-W2` 已完成
  - active part 继续保持 `P12`
  - 下一步进入 `W3`，优先锁 `S-09 mentor-space` 与导师接待位参考，不急着开贵价长视频

## Version `v0.49`

- 日期：`2026-03-29`
- 阶段：`P12 mentor-space 落图与 route rollback`
- 目标：不给 `P12` 卡在“导师人形总长歪，所以整段又停工”的状态，而是先拿到可接受的回航 clean plate，再把首版路线收回到更稳的 `voice-first`

### 主要产出

- [s-09-future-bay-return-archive-wall-mentor-space-v2-qwen-clean-plate.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/s-09-future-bay-return-archive-wall-mentor-space-v2-qwen-clean-plate.json)
- [s-09-future-bay-return-archive-wall-mentor-space-v2-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/scenes/s-09-future-bay-return-archive-wall-mentor-space-v2-qwen-image-max.png)
- [s-09-future-bay-return-archive-wall-mentor-space-v2-qwen-image-max.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/scenes/s-09-future-bay-return-archive-wall-mentor-space-v2-qwen-image-max.metadata.json)
- [shot-ch01-p12-s01-digital-mentor-return-v2-qwen-prompt-only.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-ch01-p12-s01-digital-mentor-return-v2-qwen-prompt-only.json)
- [shot-ch01-p12-s01-digital-mentor-return-v3-qwen-rescue-night.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-ch01-p12-s01-digital-mentor-return-v3-qwen-rescue-night.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `S-09 mentor-space v2` 已成为 `P12 / G05` 当前 accepted clean plate：
  - 它把“安全回航 + 导师接待位预留”成立了
  - 画面没有再长出孩子或完整导师主体，适合作为首版 scene-state 基线
- `G05` 的两条可见导师首帧尝试都没有进入主线：
  - `v2` 漂成白昼里的全身 humanoid
  - `v3` 漂成夜景里的悬浮躯干投影
- 当前由此做出明确 rollback：
  - `P12` 首版不再追可见导师人形首帧
  - 主线改走 `clean plate + voice-first + 轻问题 overlay`
  - 若后续确实需要可见导师，再单独开 `C-08` 锁形，不让 `P12` 主线继续烧错方向

## Version `v0.50`

- 日期：`2026-03-29`
- 阶段：`P12 voice-first 预览落地`
- 目标：不让 `P12` 继续停在“已经知道该走 voice-first，但没人真的把它装成可看片预览”的状态，而是先让收束节奏真实跑通

### 主要产出

- [render_chapter01_part12_voicefirst_preview.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part12_voicefirst_preview.sh)
- [part-12-digital-mentor-voicefirst-preview-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-12-digital-mentor-voicefirst-preview-v1.mp4)
- [part-12-digital-mentor-voicefirst-preview-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-12-digital-mentor-voicefirst-preview-v1.metadata.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 新增 `render_chapter01_part12_voicefirst_preview.sh`，把 `S-09 mentor-space v2 clean plate + guiding question overlay + 本机中文 TTS` 收成一条可看片的 `part-12` 低成本预览
- 当前预览的真实价值是：
  - 验证 `P12` 是否能在没有可见导师人形的前提下仍然成立“被接住 -> 抽出命题 -> 留下问题”的节奏
  - 把 chapter-01 的尾段从单张图推进到真实可审的时序资产
- 当前 notes：
  - 声音仍是本机 `Tingting` TTS，只用于节奏验证，不当作最终声音方案
  - 当前还没决定正式版是否需要极弱可见导师界面层
- 当前结论：
  - `P12` 的 `W6` 可判定为 `PASS WITH NOTES`
  - 下一步进入 `W7`，收导师总结的正式 audio contract

## Version `v0.36`

- 日期：`2026-03-28`
- 阶段：`P06 导演室与 shot contract 收口`
- 目标：不让 `P06` 卡在“知道该去暗层，但不知道先拍什么”的松散状态，而是先把换挡、解谜、第四色揭示与风声婆婆进场的边界锁死

### 主要产出

- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 正式把 `P06` 的导演问题收口为四件事：
  `E01` 负责换挡进入暗层接口，`E02` 负责异常波形与残缺切片解谜，`E03` 才第一次明确点亮第四色，`E04` 才让风声婆婆旧录音正式进场
- 把 `P06` 的声音顺序锁紧为：
  `D04` 异常风声尾音 -> `E01` 暗层低频换挡 -> `E02` 异常波形主音色 -> `E03` 系统低声确认 -> `E04` 旧录音进入
- 在 `shot-list.md` 里把 `E01-E04` 的音画合同补实，明确：
  - `E01` 不提前泄露第四色或旧录音
  - `E02` 先走 `scene-state + overlay / paper cut`，不急着跑贵价长视频
  - `E03` 才承担路径命名与第四色显形
  - `E04` 首版固定为录音界面方案，短句优先锁为 `别只听最大声的那条。`
- loop 主线已不再停在 `P06 / W1`，而是可以进入 `W3` 参考锁定：
  先用现有 `S-05`、`C-07` 与 `E03` 请求模板收参考，再决定 `E01/E04` 的首轮首帧

## Version `v0.37`

- 日期：`2026-03-28`
- 阶段：`P06 首轮首帧与 paper cut 落地`
- 目标：不给 `P06` 再停在“导演室已经收口，但还没有真正可审资产”的状态，而是把暗层段最小可读链真正装出来

### 主要产出

- [shot-ch01-p06-s01-dark-layer-ingress-v1-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p06-s01-dark-layer-ingress-v1-qwen-image-max.png)
- [shot-ch01-p06-s02-waveform-puzzle-scene-state-v1-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p06-s02-waveform-puzzle-scene-state-v1-qwen-image-max.png)
- [shot-ch01-p06-s03-hidden-path-reveal-v2-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p06-s03-hidden-path-reveal-v2-qwen-image-max.png)
- [shot-ch01-p06-s04-wind-listener-recording-interface-v2-no-tags-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p06-s04-wind-listener-recording-interface-v2-no-tags-qwen-image-max.png)
- [render_chapter01_part6_papercut.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part6_papercut.sh)
- [part-06-dark-layer-interface-papercut-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-06-dark-layer-interface-papercut-v1.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 用同一条 `qingyuntop / qwen-image-max` 图像链把 `P06` 的四个核心镜头全部补成首轮横版 keyframe，不再让暗层段停留在只有母图和口头判断的状态
- `E01` 当前判为 `PASS WITH NOTES`：已能承担进入暗层的换挡职责，但阈值感仍偏弱
- `E04 v1` 因陈列展柜感和可见标签文字直接弃用，`E04 v2` 提升为主线参考：先按“旧录音承载界面”承担风声婆婆的初次进入
- `E03` 旧模板回包慢，已用 `qwen` 救援版把第四色显形稳定落盘，避免单个慢请求拖住整个 loop
- 新增 `render_chapter01_part6_papercut.sh`，把 `E01 -> E02 -> E03 -> E04` 装成 `15.6s / 1152x768 / h264+aac` 的 rough preview
- 当前内部判断：`P06 / W6 / PASS WITH NOTES`
  已能读清“进入暗层 -> 拼接异常证据 -> 第四色显形 -> 旧录音进入”的顺序，因此下一步不再是继续堆静图，而是进入 `W7` 收视频与 audio contract

## Version `v0.38`

- 日期：`2026-03-28`
- 阶段：`P06 交付收口并切换到 P10`
- 目标：不让 `P06` 在外部 provider 限流时重新停住，而是先用可控的 story-first 资产把这一段真正收成 part-level 交付

### 主要产出

- [shot-ch01-p06-s03-hidden-path-reveal-viduq3-i2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p06-s03-hidden-path-reveal-viduq3-i2v-v1.json)
- [shot-ch01-p06-s03-hidden-path-reveal-veo-3.1-i2v-b64-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-videos/shot-ch01-p06-s03-hidden-path-reveal-veo-3.1-i2v-b64-v1.json)
- [shot-ch01-p06-s03-hidden-path-reveal-rescue-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p06-s03-hidden-path-reveal-rescue-v1.mp4)
- [render_chapter01_p06_e03_rescue_clip.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_p06_e03_rescue_clip.sh)
- [render_chapter01_part6_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part6_delivery.sh)
- [part-06-dark-layer-interface-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-06-dark-layer-interface-delivery-v1.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `E03` 的首条正式 `qingyun vidu` 提交命中 `HTTP 429`，备用 `veo-3.1` 路由命中 `HTTP 503`；当前判断这是 provider 级阻塞，不是镜头合同失败
- 不让主线停住，直接把 `E03` 收成一条受控 `rescue clip`，继续承担“第四色第一次明确成立”的职责
- 新增 `render_chapter01_part6_delivery.sh`，把 `E01 still-motion + E02 UI-first + E03 rescue clip + E04 recording-first` 装成 `part-06 delivery v1`
- 当前判断：`P06 / accepted_with_notes / delivery v1`
- `P06` 已正式交付并进入 backlog，active part 现在切到 `P10`

## Version `v0.39`

- 日期：`2026-03-28`
- 阶段：`P10 导演室与 shot contract 收口`
- 目标：不让 `P10` 一上来又掉回“整段辩论都想做成长视频”的发散状态，而是先把真正值得视频化的位收紧

### 主要产出

- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- 正式把 `P10` 的导演判断收口为：
  `F01` 负责“城市正在倾听”的空间建立，`F02` 固定 `UI-first`，`F03` 成为唯一优先正式短 clip，`F04` 固定 `UI-first`
- 在 `shot-list.md` 中为 `F01-F04` 补了音画合同，明确：
  - `F01` 不提前塞辩手、证据库或主持式口播
  - `F02/F04` 都不进入首轮长视频
  - `F03` 只承担“对手投影进入 + 一句短反问”
- 当前 loop 焦点已经稳定切到 `P10 / W1`，下一步不再是抽象讨论“辩论怎么做”，而是直接锁 `F01` 和 `F03`

## Version `v0.40`

- 日期：`2026-03-28`
- 阶段：`P10 首轮首帧与 paper cut 落地`
- 目标：不给 `P10` 再停在“导演室已经收口，但还没有真正可审画面”的状态，而是先把 `F01`、`F03` 和低成本节奏验证真正装出来

### 主要产出

- [shot-ch01-p10-s01-echo-platform-establishing-v1-qwen.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-ch01-p10-s01-echo-platform-establishing-v1-qwen.json)
- [shot-ch01-p10-s03-opponent-projection-v1-qwen-chat.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-ch01-p10-s03-opponent-projection-v1-qwen-chat.json)
- [shot-ch01-p10-s03-opponent-projection-v2-qwen-rescue.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-ch01-p10-s03-opponent-projection-v2-qwen-rescue.json)
- [shot-ch01-p10-s03-opponent-projection-v3-qwen-rescue-framed.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-ch01-p10-s03-opponent-projection-v3-qwen-rescue-framed.json)
- [shot-ch01-p10-s01-echo-platform-establishing-v1-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p10-s01-echo-platform-establishing-v1-qwen-image-max.png)
- [shot-ch01-p10-s03-opponent-projection-v3-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p10-s03-opponent-projection-v3-qwen-image-max.png)
- [render_chapter01_part10_papercut.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part10_papercut.sh)
- [part-10-free-echo-platform-papercut-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-papercut-v1.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 新增 `P10` 的正式请求模板与救援模板，明确执行口径：
  - `F01` 先用 `qwen-image-max / images` 锁回响台公共空间建立
  - `F03` 先尝试 `多参考 chat` 路线，再在额度预扣不足时立即切回 `images` 救援版，不让 active part 停住
- 实际踩实一条新的 provider 判断：
  - 原先机器里的旧 `qingyuntop` key 已在本轮命中 `额度已用尽`
  - 改用当前可鉴权的新 key 后，`F01` 与 `F03 rescue` 已能继续真实出图
  - `F03` 的 `chat + 双参考` 路线因 `pre-consumed quota` 不足未继续死磕，直接切回 `story-first rescue`
- `F01` 当前结论：`PASS WITH NOTES`
  - 已把“城市正在倾听”的公共空间建立起来
  - 仍保留一条 notes：画面更偏 `公共回响台奇观`，后续若进入正式视频首帧，可继续增强“发言位即将被启用”的近端压力
- `F03` 当前结论：`PASS WITH NOTES`
  - `v2` 过于接近制度人物定妆照，因此没有拿来当主线
  - `v3` 已把构图拉回“对手投影进入公共场域”的职责位，当前先作为 `P10` 的主线首帧救援版
- 新增 `render_chapter01_part10_papercut.sh`，把 `F01 + F02 UI + F03` 装成 `13.0s` 的低成本节奏验证视频
- `P10` 的 `W6` 当前可判定为 `PASS WITH NOTES`：
  - 现在已经能按正确顺序读清 `空间亮起 -> 组织证据与立场 -> 对手反问进入`
  - 因此 loop 下一步不再停留在 `W3/W4/W5`，而是进入 `W7`，只为 `F03` 收视频与 audio contract 并生成唯一正式短 clip

## Version `v0.41`

- 日期：`2026-03-28`
- 阶段：`P10 W7 正式视频模板与首轮提交`
- 目标：不给 `P10` 在 `paper cut` 通过后又停在“知道该生成短 clip，但没人真的提交”的状态，而是把 `F03` 的正式视频链真实发起一次

### 主要产出

- [shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo-3.1-i2v-b64-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-videos/shot-ch01-p10-s03-opponent-projection-veo-3.1-i2v-b64-v1.json)
- [shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1.metadata.json)
- [shot-ch01-p10-s03-opponent-projection-veo-3.1-i2v-b64-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p10-s03-opponent-projection-veo-3.1-i2v-b64-v1.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- `P10 / F03` 的 `W7` 不再只有抽象口径，而是已经形成两条真正可执行的正式视频模板：
  - `qingyun / viduq3-turbo / img2video`
  - `adult-safe veo-3.1 relay / image-to-video`
- 首轮真实提交结果已经踩实为 provider 级阻塞，而不是镜头合同失败：
  - `viduq3-turbo` 对 `shot-ch01-p10-s03-opponent-projection-viduq3-i2v-v1` 返回 `HTTP 429`
  - 成人 `veo-3.1` 备用 relay 对 `shot-ch01-p10-s03-opponent-projection-veo-3.1-i2v-b64-v1` 首次提交命中 `Broken pipe`
- 当前判断：
  - `F03` 的画面职责已经清楚，`W3-W6` 不是瓶颈
  - `P10` 现在真实卡在 `W7 / provider availability`
  - 因此后续不该回头重开 `F01/F02/F04`，而应继续只追 `F03` 的正式短 clip 路线

## Version `v0.42`

- 日期：`2026-03-28`
- 阶段：`P10 story-first 交付收口并切换到 P11`
- 目标：不让 `P10` 停在“正式 provider 卡住，所以整段又停工”的状态，而是先用可控 rescue 路线把公共表达高潮段收成可看片的 part-level 交付

### 主要产出

- [render_chapter01_p10_f03_rescue_clip.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_p10_f03_rescue_clip.sh)
- [shot-ch01-p10-s03-opponent-projection-rescue-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p10-s03-opponent-projection-rescue-v1.mp4)
- [shot-ch01-p10-s03-opponent-projection-rescue-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p10-s03-opponent-projection-rescue-v1.metadata.json)
- [render_chapter01_part10_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part10_delivery.sh)
- [part-10-free-echo-platform-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-10-free-echo-platform-delivery-v1.mp4)
- [part-10-free-echo-platform-delivery-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-10-free-echo-platform-delivery-v1.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 在 `vidu / veo` 两条正式视频路由都出现 provider 级阻塞后，没有回退去重写 `P10`，而是直接照 `P06/E03` 的办法补出 `F03 rescue clip`
- `F03 rescue clip` 当前职责已经成立：
  - 让“对手投影进入公共场域”真正动态化
  - 不再让 `P10` 只能靠静帧说明推进
  - 继续保留“正式 provider clip 恢复后优先替换”的升级窗口
- 新增 `render_chapter01_part10_delivery.sh`，把 `F01` 空间建立、`F02` 证据立场 UI、`F03 rescue clip`、`F04` 公开陈词提交 UI 收成 `16.0s` 的 `part-10 delivery v1`
- 当前结论：
  - `P10` 已可提升为 `accepted_with_notes`
  - 当前 notes 主要集中在：`F03` 仍是 rescue clip 而非正式 provider clip
  - 但整段已经足够支撑 chapter-01 主线继续推进到 `P11`

## Version `v0.43`

- 日期：`2026-03-28`
- 阶段：`P11 导演室收口并推进到 W2`
- 目标：不让 chapter-01 在 `P10` 收口后重新停在“P11 轮到它了，但还没人决定怎么拍”的空转状态，而是先把终局段真正收成单一主线口径

### 主要产出

- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- 正式把 `P11` 的导演判断收口为：
  - `G01` 负责把制度结果压回林澄面前
  - `G02` 成为唯一优先正式人物视频位
  - `G03` 固定 `UI-first`
  - `G04` 先作为回航桥接位，不提前展开完整数字导师总结
- 明确 `P11` 当前最重要的不是“把结尾做得更大”，而是“先把结果压回具体人生，再把孩子温和带回未来湾”
- loop 已从 `P11 / W1` 推到 `P11 / W2`
- 当前唯一下一步已经被收紧为：
  先锁 `G01` 的终局确认层与 `G02` 的林澄结尾陈词参考，不开启 `G03` 长视频

## Version `v0.44`

- 日期：`2026-03-28`
- 阶段：`P11 首帧与 rough preview 落地`
- 目标：不让 `P11` 停在“知道终局怎么拍，但还没有任何可审资产”的状态，而是先把 `G01 -> G02 -> G03 -> G04` 装成一条可审的 `story-first` 预览链

### 主要产出

- [shot-ch01-p11-s01-final-confirmation-v1-qwen.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-ch01-p11-s01-final-confirmation-v1-qwen.json)
- [shot-ch01-p11-s02-lin-final-speech-v1-qwen.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-ch01-p11-s02-lin-final-speech-v1-qwen.json)
- [shot-ch01-p11-s01-final-confirmation-v1-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p11-s01-final-confirmation-v1-qwen-image-max.png)
- [shot-ch01-p11-s02-lin-final-speech-v1-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p11-s02-lin-final-speech-v1-qwen-image-max.png)
- [render_chapter01_part11_papercut.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part11_papercut.sh)
- [part-11-midnight-choice-return-papercut-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-11-midnight-choice-return-papercut-v1.mp4)
- [part-11-midnight-choice-return-papercut-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-11-midnight-choice-return-papercut-v1.metadata.json)
- [shot-ch01-p11-s02-lin-final-speech-viduq3-i2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p11-s02-lin-final-speech-viduq3-i2v-v1.json)
- [shot-ch01-p11-s02-lin-final-speech-viduq2-i2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p11-s02-lin-final-speech-viduq2-i2v-v1.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `G01` 已真实锁成终局确认位：制度结果、确认书与林澄重新回到同一画面里，不再停在概念口径
- `G02` 已有当前主线首帧，林澄结尾陈词不必再从空白开始谈正式人物视频
- 新增 `render_chapter01_part11_papercut.sh`，把 `G01 -> G02 -> G03 UI-first -> G04` 装成 `16.8s` 的 `part-11 paper cut v1`
- 已为 `G02` 补出 `qingyun / viduq3` 主版本和 `viduq2` 救援版本请求模板，并真实提交过一次；当前两条都返回 `HTTP 429`
- 当前结论：
  - `P11` 的 `W3-W6` 已形成可审的 `story-first` 资产
  - 当前判断继续保持 `W7 / PASS WITH NOTES`
  - 唯一优先下一步已经继续收紧为：为 `G02` 切下一条正式 provider，不重复刷当前 `qingyun` 限流路由；`G03`、`G04` 不抢首轮视频资源

## Version `v0.45`

- 日期：`2026-03-28`
- 阶段：`P11 G02 多 provider 正式提交收口`
- 目标：不让 `G02` 停在“只有一条 provider 429，所以继续空转”的状态，而是把当前可切的正式提交家族都真实撞一遍，明确哪类失败值得停止、哪类入口值得保留

### 主要产出

- [shot-ch01-p11-s02-lin-final-speech-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p11-s02-lin-final-speech-wan2.6-i2v-flash-v1.json)
- [shot-ch01-p11-s02-lin-final-speech-hailuo-2.3-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p11-s02-lin-final-speech-hailuo-2.3-v1.json)
- [shot-ch01-p11-s02-lin-final-speech-kling-video-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-videos/shot-ch01-p11-s02-lin-final-speech-kling-video-v1.json)
- [shot-ch01-p11-s02-lin-final-speech-kling-video-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p11-s02-lin-final-speech-kling-video-v1.metadata.json)
- [shot-ch01-p11-s02-lin-final-speech-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p11-s02-lin-final-speech-wan2.6-i2v-flash-v1.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `qingyun / ent/v2` 当前不只是 `vidu` 限流，而是 `G02` 的 `viduq3`、`viduq2`、`wan2.6-i2v-flash`、`MiniMax-Hailuo-2.3` 四条 task-based 提交都返回 `HTTP 429`
- `qingyun / kling-video` 已真实通过 `chat/completions` 提交并返回结构化错误 metadata：`invalid_api_type`，明确这条模型不是当前脚本壳，要求 task-based channel
- `G02` 当前因此不再适合继续在 `qingyun` 同一提交层盲换模型；阻塞位已收敛为 `provider submission tier`
- 为下一次可直接接手，已补出独立 [shot-ch01-p11-s02-lin-final-speech-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p11-s02-lin-final-speech-wan2.6-i2v-flash-v1.json) 正式模板；一旦独立 DashScope key 恢复，不需要重新写模板，直接可提
- 当前结论：
  - `P11` 继续保持 `W7 / PASS WITH NOTES`
  - `G02` 的问题已明确是 provider 侧提交层，而不是镜头合同、首帧或剧情职责问题
  - 下一步不再重复刷 `qingyun` 当前提交层，优先等独立 DashScope 路由恢复后接管

## Version `v0.46`

- 日期：`2026-03-29`
- 阶段：`P11 G02 自动提交 loop 落地`
- 目标：不让 `G02` 继续依赖人工一条条重提，而是把当前正式提交矩阵固化成可重复执行的 loop，并用一轮真实执行把阻塞位收口成可接手结果

### 主要产出

- [run_chapter01_p11_g02_submission_loop.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/run_chapter01_p11_g02_submission_loop.sh)
- [shot-ch01-p11-s02-lin-final-speech-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p11-s02-lin-final-speech-wan2.6-i2v-flash-v1.json)
- [shot-ch01-p11-s02-lin-final-speech-kling-video-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p11-s02-lin-final-speech-kling-video-v1.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 新增 `run_chapter01_p11_g02_submission_loop.sh`，当前执行顺序固定为：
  - 有独立 `DASHSCOPE_API_KEY` 时，优先执行 `G02 / wan2.6-i2v-flash` 正式模板
  - 否则自动轮转 `qingyun / viduq3 -> viduq2 -> wan2.6-i2v-flash -> MiniMax-Hailuo-2.3`
  - 最后再尝试 `openai-compatible / kling-video`
- 已真实执行一轮最小 loop，当前 machine-readable 结果是：
  - `DashScope`: `missing_key`
  - `qingyun / viduq3`: `429`
  - `qingyun / viduq2`: `429`
  - `qingyun / wan2.6-i2v-flash`: `429`
  - `qingyun / MiniMax-Hailuo-2.3`: `429`
  - `qingyun / kling-video chat/completions`: `500`
- 这意味着 `G02` 当前不再缺“下一步做什么”，而是已经有了可重复执行的提交 loop；真正阻塞位被压缩成：
  - 当前机器缺独立 DashScope key
  - 当前 `qingyun` task 提交层整体限流
- 当前结论：
  - `P11` 继续保持 `W7 / PASS WITH NOTES`
  - 下一步最值得做的是：补到可用独立 DashScope key 后，直接执行 `G02 / wan2.6-i2v-flash` 正式模板或同一个 loop 脚本

## Version `v0.35`

- 日期：`2026-03-28`
- 阶段：`P05 W6 通过并进入 W7`
- 目标：不让 `P05` 卡在“预览已经有了，但没人判断能不能继续”的停滞态，把低成本节奏验证真正转化为下一门的推进依据

### 主要产出

- [part-05-probability-corridor-papercut-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-05-probability-corridor-papercut-v1.mp4)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- 对 `part-05-probability-corridor-papercut-v1.mp4` 完成内部自审，确认这条 rough preview 已经足够讲清 `P05` 的核心顺序：
  `三路径成立 -> 路径比较 -> 异常风声打断`
- 当前判断：
  - `D02` 的同空间 UI 分层已成立
  - `D04 v7` 的桥接职责已成立
  - `D01 v1` 仍有展柜感，但属于可后补的画面升级项，不再阻塞主线
- 正式把 `P05` 从 `W6 / story-first preview ready` 推进到 `W7 / PASS WITH NOTES`
- `W7` 的唯一优先下一步已收口为：
  先为 `P05` 收视频与 audio contract，明确哪些镜头保持 `UI-first / paper-cut`，哪些镜头值得进入正式 clip 生成

## Version `v0.34`

- 日期：`2026-03-28`
- 阶段：`P05 rough preview 落地`
- 目标：不再停在“P05 应该怎么做”的讨论层，直接把 `概率长廊成立 -> 路径比较 -> 异常风声打断` 装成一条可审的低成本预览

### 主要产出

- [render_chapter01_part5_papercut.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part5_papercut.sh)
- [part-05-probability-corridor-papercut-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-05-probability-corridor-papercut-v1.mp4)
- [part-05-probability-corridor-papercut-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-05-probability-corridor-papercut-v1.metadata.json)
- [p05-d02-path-comparison-overlay-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/ui/p05-d02-path-comparison-overlay-v1.png)
- [p05-d04-anomaly-subtitle-overlay-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/ui/p05-d04-anomaly-subtitle-overlay-v1.png)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- 新增 `render_chapter01_part5_papercut.sh`，把 `D01`、`D02` 同空间 UI 粗层、`D04 v7` 与最小环境音装配成 `12.6s / 1152x768 / AAC` 的可审 rough preview
- 为 `D02` 与 `D04` 分别补出可直接装配的视频用 PNG overlay，避免预览阶段依赖浏览器叠 SVG 才能成立
- 主资产页已直接展示 `part-05-probability-corridor-papercut-v1.mp4`，后续审片不再只看静帧和描述
- `P05` 当前判断已从 `STORY-FIRST IN PROGRESS` 推进到 `STORY-FIRST PREVIEW READY`
- loop 的唯一下一步已收口为：先审这条 rough preview；故事读得清就进 `W7`，不清再定向返修 `D01/D02`

## Version `v0.33`

- 日期：`2026-03-28`
- 阶段：`Chapter01 持续 loop 驱动器`
- 目标：把 chapter-01 从“有状态板”推进到“有可持续运行的 agent loop”，只要章节未完工，就能沿唯一 active part 持续往前推进

### 主要产出

- [chapter01_loop_driver.py](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/chapter01_loop_driver.py)
- [current/README.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/current/README.md)
- [agents.md](/Users/wujames/Desktop/AI未来通识课（K12）/agents.md)
- [content/chapters/chapter-01-time-archive-city/agents.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/agents.md)
- [outputs/current-chapter-01](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/current-chapter-01)
- [chapter-01-preview.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/current/chapter-01-preview.html)

### 核心变化

- 新增 `scripts/production/chapter01_loop_driver.py`，负责读取 `video-loop-state.json`、判断 chapter 是否完工、输出唯一 active part 与唯一优先下一步，并同步 `outputs/current-chapter-01`
- 明确把 loop 的持续条件固化为：只要仍存在 `next_active_part / in_progress / queued / blocked / ready` 状态，chapter-01 就视为未完工，loop 继续
- 修正 dated current 包里的 `chapter-01-preview.html` 入口链接，避免 current preview 指向自身形成坏链
- 确认 `outputs/current-chapter-01` 继续稳定指向 dated accepted current hub，让 `content/.../current/assets` 不再悬空
- 把 `chapter01_loop_driver.py --check --sync-current` 回写进项目级与 chapter 级规则，后续 agent 默认先跑这条命令再接手 active part

### 当前 loop 结论

- `Loop complete`: `NO`
- `Current focus part`: `P05`
- `Next active gate`: `W6 / 纸片剪辑验证`
- `唯一优先下一步`：
  基于 `D01 + D02 overlay + D04 v7 + S-04` 做低成本节奏验证与流程跑通，再决定哪些镜头值得回头精修

## Version `v0.32`

- 日期：`2026-03-28`
- 阶段：`P05 D02 UI 粗验证`
- 目标：不给 `D02` 另开贵价长视频路线，先用同空间 overlay 验证“路径切换与价值勾选”这一步是否成立

### 主要产出

- [p05-d02-path-comparison-overlay-v1.svg](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/ui/p05-d02-path-comparison-overlay-v1.svg)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [s-04-probability-corridor-v1-qwen-image-plus.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/scenes/s-04-probability-corridor-v1-qwen-image-plus.png)
- [shot-d01-probability-corridor-reveal-keyframe-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-d01-probability-corridor-reveal-keyframe-v1.png)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v7-qwen-prompt-only-retry.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v7-qwen-prompt-only-retry.png)

### 核心变化

- 按 `shot-list` 的 `D02` 合同，把“路径切换 + 价值勾选”收回到同一条概率长廊空间内，不再把它误做成独立答题页或单独长视频
- 新增透明 SVG overlay，用最小成本把 `底部路径切换条 + 右上价值排序面板 + 当前未来切片` 叠回 `S-04` 空间
- 主 HTML 已直接展示这张 rough UI 叠层效果，便于按“故事是否读得懂”而不是“画面是否够贵”来审当前流程
- `P05` 的下一步已进一步收口为：基于 `D01 + D02 overlay + D04 v7 + S-04` 做低成本节奏验证，再决定是否回头精修 `D01` 或正式推进 clip

## Version `v0.31`

- 日期：`2026-03-28`
- 阶段：`P05 story-first 粗资产推进`
- 目标：停止把 `P05` 卡在高清首帧精修上，先用已经能讲清故事的粗资产把流程继续往下游推进

### 主要产出

- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [shot-d01-probability-corridor-reveal-keyframe-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-d01-probability-corridor-reveal-keyframe-v1.png)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v7-qwen-prompt-only-retry.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v7-qwen-prompt-only-retry.png)
- [s-04-probability-corridor-v1-qwen-image-plus.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/scenes/s-04-probability-corridor-v1-qwen-image-plus.png)
- [shot-d01-probability-corridor-reveal-keyframe-v2-qwen-path-lanes.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-d01-probability-corridor-reveal-keyframe-v2-qwen-path-lanes.png)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v8-qwen-canonical-layered.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v8-qwen-canonical-layered.png)

### 核心变化

- 明确当前阶段目标不是“再追一轮更高清的 `P05` 首帧”，而是先把 `概率长廊成立 -> 浏览可能性 -> 异常风声打断` 这条叙事链跑通
- 把 `D01 v1` 提升为当前 rough keyframe：它仍有展柜感和后续精修空间，但已经足以承担“三条公开路径同时成立”的基础叙事职责
- 把 `D04 v7` 保持为当前 rough bridge keyframe：它不是严格参考锁脸版，但已经足以承担“林澄听见异常并把注意力推向暗层入口”的桥接职责
- 把 `D02` 明确固定为 `同空间 UI 分层` 路线，不再为它追额外高清大图，避免在交互段继续盲烧额度
- 本轮补跑的 `D01 v2` 与 `D04 v8` 已归档为对照探索资产，但当前不提升为主展示；原因是它们没有明显优于现有 rough 主线的叙事清晰度
- loop 状态已从“首帧门卡住”切到“`W6 / STORY-FIRST IN PROGRESS`”：下一步优先做低成本节奏验证，而不是继续堆更贵的图片尝试

## Version `v0.30`

- 日期：`2026-03-27`
- 阶段：`P05 青云图像链验证`
- 目标：在 `txvlogvip + GEMINI` 图像路由失效后，为 `P05/W4` 找到可继续推进的 `qingyuntop` 首帧替代链，并把阻塞点缩到可执行层

### 主要产出

- [generate_openai_images.py](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/generation/generate_openai_images.py)
- [shot-d01-probability-corridor-reveal-keyframe-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-d01-probability-corridor-reveal-keyframe-v1.png)
- [shot-d01-probability-corridor-reveal-keyframe-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/metadata/shots/shot-d01-probability-corridor-reveal-keyframe-v1.metadata.json)
- [shot-d01-probability-corridor-reveal-keyframe-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/imagen4-fast/metadata/shots/shot-d01-probability-corridor-reveal-keyframe-v1.metadata.json)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max-chat/metadata/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v1.metadata.json)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/gemini-2.5-flash-image-chat/metadata/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v1.metadata.json)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v4-qwen-prompt-only.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v4-qwen-prompt-only.png)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v4-qwen-prompt-only.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/metadata/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v4-qwen-prompt-only.metadata.json)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v5-qwen-prompt-only-canonical-push.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v5-qwen-prompt-only-canonical-push.png)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v5-qwen-prompt-only-canonical-push.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/metadata/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v5-qwen-prompt-only-canonical-push.metadata.json)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v7-qwen-prompt-only-retry.png](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v7-qwen-prompt-only-retry.png)
- [shot-ch01-p05-s04-wind-anomaly-reaction-v7-qwen-prompt-only-retry.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-images/qwen-image-max/metadata/shots/shot-ch01-p05-s04-wind-anomaly-reaction-v7-qwen-prompt-only-retry.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- 用 `qingyuntop / qwen-image-max` 经 `https://api.qingyuntop.top/v1/images/generations` 成功生成 `CH01-P05-S01 / D01` 的 `1536x1024` 首帧候选，证明 `P05` 不再完全卡死在旧图像 relay 上
- 明确 `google/imagen-4-fast` 在青云当前不是标准 `/v1/images/generations` 路由，而是任务制专用通道；后续如果要用它，必须改走对应 task endpoint，不能再按 OpenAI 图片壳盲调
- 把 `generate_openai_images.py` 补成可解析青云 `chat` 图像响应里 Markdown 包裹的 `data:image/...;base64`，避免“模型已返回图片但脚本不会落盘”的假失败
- 明确 `CH01-P05-S04 / D04` 的双参考反应镜头在 `qwen-image-max + /v1/chat/completions` 路线上当前先卡在额度预扣；换到 `gemini-2.5-flash-image` 后，路由本身已返回图片格式，但重跑时被同一把 key 的剩余额度耗尽打断
- 在 `D04` 上新增 `qwen-image-max / images` 的 prompt-only 救援链，并真实产出 `v4` 与更接近 canonical 服装口径的 `v5`
- 在限流恢复后再次重试，`gemini-2.5-flash-image` 的严格参考路线仍被上游负载挡住；但 `qwen-image-max / images` 又补出一张新的 `v7`，当前比 `v5` 更接近林澄的 canonical 年龄与服装观感
- 当前判断：`v4` 证明 `D04` 可以被当前 provider 路线快速补出；`v7` 则是现阶段更值得进入人工审图的一张救援候选
- `P05` 仍停留在 `W4 / IN_PROGRESS`，但唯一优先下一步已经更具体：先审 `D01` 的三路径区分和空间可读性；`D04` 则先以 `v7` 为救援候选进入审图，再决定是否继续追严格参考版

## Version `v0.29`

- 日期：`2026-03-27`
- 阶段：`P05 导演室收口`
- 目标：把 `P05` 从“loop 控制板里写着该先审一下”的状态，推进成真正可执行的 `W1/W2` 收口状态，并明确首轮 keyframe 顺序

### 主要产出

- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- 明确 `P05` 的真正导演目标不是“先把第四路径做出来”，而是“先让三条公开路径的诱惑力成立，再让异常风声把它打断”
- 把 `D01 / D02 / D03 / D04` 的职责重新拆开：`D01` 负责奇观建立，`D02` 负责同空间交互，`D03` 后移为趣味补强，`D04` 负责桥接到 `P06`
- 把 `D02` 从潜在的贵价长视频目标改回 `scene-state + UI 分层 + 交互` 路线，避免在交互段盲烧长视频额度
- 更新 loop 状态：`P05` 不再停留在 `QUEUED / W1`，而是进入 `W4 / IN_PROGRESS`，唯一优先下一步收口为先做 `D01` keyframe，再做 `D04` keyframe

## Version `v0.27`

- 日期：`2026-03-26`
- 阶段：`P03 正式交付收口`
- 目标：把 `P03` 从“workflow 已校正的候选镜头”推进成“可直接审片的 part-level delivery”，同时让主资产页只保留真正有长期价值的交付入口与复用资产

### 主要产出

- [render_chapter01_part3_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part3_delivery.sh)
- [part-03-archive-hall-pressure-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-03-archive-hall-pressure-delivery-v1.mp4)
- [part-03-archive-hall-pressure-delivery-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-03-archive-hall-pressure-delivery-v1.metadata.json)
- [shot-ch01-p03-s01-hall-triangle-v7-no-panel-qwen-image-2.0-pro.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p03-s01-hall-triangle-v7-no-panel-qwen-image-2.0-pro.png)
- [c03-hall-investigation-overlay-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/ui/c03-hall-investigation-overlay-v1.png)
- [c05-application-rejected-overlay-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/ui/c05-application-rejected-overlay-v1.png)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 新增 `P03` 正式主装配脚本，把 `C01-C05` 固定成 `delivery v1`：大厅建立、林澄近景、调查层、序列员 07 施压与驳回提示形成一条完整可审片链
- `P03` 当前主交付已正式收成 `1152x768 / 30fps / 22.4s / AAC stereo` 的 part-level delivery 文件，不再只停留在单镜头候选
- `C03/C05` 的 UI 层已被提升为正式复用资产；主 HTML 不再展示过程性 relay probe，而是切换为交付视频、正式首帧与正式 UI 叠层
- 当前结论明确收口为：`P03 delivery v1 = PASS WITH NOTES`，后续只定向升级 `C02/C04` 的近景关系镜头，不重开已接受的 canonical 锚点

## Version `v0.25`

- 日期：`2026-03-25`
- 阶段：`P03 identity-first workflow 校正`
- 目标：把 `CH01-P03-S01 / C01` 从“能出一个大厅视频”收束为“按正确 workflow 能稳定推进的大厅主线候选”，停止把旧 `R2V` 试片误认成可直接回写的主资产

### 主要产出

- [generate_dashscope_images.py](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/generation/generate_dashscope_images.py)
- [video-director-codex-zh/SKILL.md](/Users/wujames/.codex/skills/video-director-codex-zh/SKILL.md)
- [shot-image-generator-codex-zh/SKILL.md](/Users/wujames/.codex/skills/shot-image-generator-codex-zh/SKILL.md)
- [video-qc-codex-zh/SKILL.md](/Users/wujames/.codex/skills/video-qc-codex-zh/SKILL.md)
- [clip-study-codex-zh/SKILL.md](/Users/wujames/.codex/skills/clip-study-codex-zh/SKILL.md)
- [shot-ch01-p03-s01-hall-triangle-v7-no-panel.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-images/shot-ch01-p03-s01-hall-triangle-v7-no-panel.json)
- [shot-ch01-p03-s01-hall-establishing-wan2.6-i2v-flash-v5-short-clean-world-audio.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p03-s01-hall-establishing-wan2.6-i2v-flash-v5-short-clean-world-audio.json)
- [shot-ch01-p03-s01-hall-triangle-v7-no-panel-qwen-image-2.0-pro.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p03-s01-hall-triangle-v7-no-panel-qwen-image-2.0-pro.png)
- [shot-ch01-p03-s01-hall-establishing-wan2.6-i2v-flash-v5-short-clean-world-audio-cropped-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p03-s01-hall-establishing-wan2.6-i2v-flash-v5-short-clean-world-audio-cropped-720p.mp4)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)

### 核心变化

- 把 `qwen-image-2.0` 生图链补成真正支持 `reference_sources`，让 `actor_refs` 能直接进入镜头首帧生成，而不再只是文字承诺
- 明确把“每个清晰出镜人物都必须提交 actor photo”“没有 clip 首帧图不允许生视频”“多人物镜头默认先出 clean scene-state keyframe”写入项目规则与本地 skill
- 把 `CH01-P03-S01 / C01` 的旧 `R2V v1/v2` 正式降级为 `FAILED_GATE`；这些分支保留为试验记录，但不再作为主线候选展示
- 新生成 `hall-triangle v7 no-panel` 首帧，并在其基础上交付 `wan2.6-i2v-flash v5 short clean world audio` 裁切候选，形成当前最干净的 `P03/C01` 主线样本
- 主 HTML 展示页已切换到真实状态：`P03` 当前展示的是 `v7` keyframe + `v5 cropped` clip 的 workflow 校正成果，而不是旧 `R2V` 误判

## Version `v0.21`

- 日期：`2026-03-25`
- 阶段：`P01 开场声场修正`
- 目标：在不回退同步口型方案的前提下，修正 `P01` 开头两镜被削薄的世界音问题

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v11.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v11.mp4)
- [part-01-future-bay-task-dock-delivery-v11.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v11.metadata.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)

### 核心变化

- 保留 `v10` 已经建立的 `S03/S04/S05/S06` 镜头内同步对白路线，不再回退到后贴 TTS
- 把 `S01/S02` 从“轻底噪试听版”升级成更像正式剧集开场的未来湾港口声场，补回低频海流、空气层、码头电流与灰银信号唤醒层
- 把 `P01` 最终音轨从实际单声道修正为真实 `AAC stereo`
- 主 HTML 展示页已切换到 `v11` 主交付，后续审片默认以这一版为准

## Version `v0.22`

- 日期：`2026-03-25`
- 阶段：`P01 可读性与截断修正`
- 目标：修正用户在 `v11` 中明确指出的三处问题：开头环境音仍弱、男孩台词被切、灰银任务信息不可读

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v12.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v12.mp4)
- [part-01-future-bay-task-dock-delivery-v12.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v12.metadata.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)

### 核心变化

- 在 `S01/S02` 混音里接回项目内已存在的开场效果资产，并提高港口、空气、电流与信号层的可感知度
- 为 `S02` 增加高对比正式任务牌，明确呈现“灰银任务 / 时间档案城 正式请求接入”
- 把 `S04` 从 `4.2s` 装配截切恢复为完整 `5.0s`，避免男孩那句台词在 assembly 层被提前切掉
- 主 HTML 展示页已切换到 `v12` 主交付，后续审片默认以这一版为准

## Version `v0.23`

- 日期：`2026-03-25`
- 阶段：`P01 林澄台词收口`
- 目标：修正用户继续指出的 `S06` 林澄台词“感觉没说完就截断了”的问题

### 主要产出

- [shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v2.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v2.json)
- [shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v2-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v2-720p.mp4)
- [shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v2-720p.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v2-720p.metadata.json)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v13.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v13.mp4)
- [part-01-future-bay-task-dock-delivery-v13.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v13.metadata.json)

### 核心变化

- 确认旧 `S06 v1` 的非静音内容一直顶到 clip 末尾，问题在源视频本身，不在 assembly 时长
- 新增 `S06 v2` 请求模板，把林澄台词改成更短的同步句：`可清晰，不等于正确。`
- 重跑 `S06 v2` 后确认其尾段已留出静尾和收气空间，再替换进 `P01 v13` 主装配
- 主 HTML 展示页已切换到 `v13` 主交付，后续审片默认以这一版为准

## Version `v0.1`

- 日期：`2026-03-19`
- 阶段：`内容与 demo 骨架`
- 目标：为 chapter-01 建立从叙事到 demo 制作的完整基线

### 主要产出

- [chapter.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/chapter.md)
- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [product-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/product-script.md)
- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [prototype-flow.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/prototype-flow.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [prototype-assets-checklist.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/prototype-assets-checklist.md)

### 核心变化

- 明确 chapter-01 作为首个完整样板章节
- 明确第一人称沉浸体验与课后数字导师收束
- 建立从内容稿走向 demo 验证的首轮制作骨架

## Version `v0.2`

- 日期：`2026-03-19`
- 阶段：`AIGC 产线准备`
- 目标：把 chapter-01 从“可制作”推进到“可生成”

### 主要产出

- [prompt-bible.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/visual/prompt-bible.md)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)

### 核心变化

- 为角色、场景、镜头、UI 和声音建立统一 prompt 基线
- 为首批 P0 资产建立结构化 manifest
- 建立版本归档与模板层，避免生成过程失控

## Version `v0.3`

- 日期：`2026-03-20`
- 阶段：`叙事升级与制作对齐`
- 目标：把 chapter-01 从“成立的样板”推到“更成戏、更沉浸、更适合制作协同”的版本

### 主要产出

- [chapter.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/chapter.md)
- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [product-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/product-script.md)
- [digital-mentor.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/digital-mentor.md)
- [ui-prototype.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/ui-prototype.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [content/chapters/chapter-01-time-archive-city/product/episode-onscreen-copy.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/episode-onscreen-copy.md)

### 核心变化

- 把第四路径从“被隐藏的正确答案”改成“被隐藏的困难可能性”
- 把前半段从“先导览后危机”改成“先危机后规则”
- 把回响台升级为更有制度后果的终局装置
- 让多份生产文档进入同一版叙事逻辑

## Version `v0.4`

- 日期：`2026-03-20`
- 阶段：`连续剧化升级`
- 目标：把 chapter-01 从“强单集样板”升级为“能承担整季开篇职责的第一集”

### 主要产出

- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/script.md)
- [product-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/product-script.md)
- [digital-mentor.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/digital-mentor.md)
- [ui-prototype.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/ui-prototype.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [content/chapters/chapter-01-time-archive-city/product/episode-onscreen-copy.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/episode-onscreen-copy.md)
- [future-bay-fixed-ip-team.md](/Users/wujames/Desktop/AI未来通识课（K12）/docs/world/future-bay-fixed-ip-team.md)

### 核心变化

- 把玩家从临时协助者升级为未来湾固定团队主位
- 新增 `Part 5.5：证据失效与团队分裂`
- 把 AI 使用边界写成真实戏剧代价，而不是原则说明
- 把高潮升级成责任签署与制度后果
- 在主稿中第一次点出“系统看起来在帮你，其实在替你决定人生”
- 让林澄从单集案例角色升级为长期伙伴起点

## Version `v0.5`

- 日期：`2026-03-20`
- 阶段：`数据与生产模板补位`
- 目标：把当前稳定叙事结构同步到数据层、资产追踪层和 API 请求层

### 主要产出

- [chapter-01-time-archive-city.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/data/chapters/chapter-01-time-archive-city.json)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [first-round-generation-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/first-round-generation-pack.md)
- [prototype-assets-checklist.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/prototype-assets-checklist.md)
- [README.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/README.md)
- [s-02-emergency-entry-check.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/s-02-emergency-entry-check.json)
- [s-09-future-bay-return-archive-wall-mentor-space.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/s-09-future-bay-return-archive-wall-mentor-space.json)
- [ui-13-system-petition-status-bar.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/ui-13-system-petition-status-bar.json)
- [shot-e03-hidden-path-reveal-keyframe.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-e03-hidden-path-reveal-keyframe.json)
- [shot-f03-opponent-projection-keyframe.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-f03-opponent-projection-keyframe.json)

### 核心变化

- 把 JSON 数据层补齐到当前稳定主线
- 同步 `public_window_opened`、`resolution_tier`、`evidence_integrity` 等关键状态
- 明确 `prototype-assets-checklist`、`asset-manifest` 与 `api-requests` 的职责边界
- 为第二轮关键视觉 / UI 资产补出可直接调用的请求模板
- 当时建立的旧编号模板已在后续 `v0.6` 中按连续剧版编号重映射

## Version `v0.6`

- 日期：`2026-03-20`
- 阶段：`生产编号收口`
- 目标：把 chapter-01 当前真正要开工的资产编号、提示词基线和请求模板收成一套生产可执行口径

### 主要产出

- [prompt-bible.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/visual/prompt-bible.md)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [README.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/README.md)
- [c-04-qi-ye.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/c-04-qi-ye.json)
- [c-05-wen-xia.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/c-05-wen-xia.json)
- [c-07-wind-listener-keeper.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/c-07-wind-listener-keeper.json)
- [c-08-digital-mentor.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/c-08-digital-mentor.json)
- [s-07-free-echo-platform.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/s-07-free-echo-platform.json)
- [s-09-future-bay-return-archive-wall-mentor-space.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/s-09-future-bay-return-archive-wall-mentor-space.json)
- [ui-09-evidence-integrity-status-bar.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/ui-09-evidence-integrity-status-bar.json)
- [ui-10-team-permission-freeze-warning.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/ui-10-team-permission-freeze-warning.json)
- [ui-12-responsibility-signing-layer.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/ui-12-responsibility-signing-layer.json)
- [ui-13-system-petition-status-bar.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/ui-13-system-petition-status-bar.json)

### 核心变化

- 把 `S-07 / S-09`、`C-04-C-08`、`UI-08-UI-13` 的连续剧版编号正式同步到 `asset-manifest`
- 在 `prompt-bible` 中补齐祁野、闻夏、林澄父亲，以及证据冻结区、午夜前确认层和新高潮链 UI 的生成基线
- 删除旧的 `s-07-future-bay-exit-mentor-space.json`，避免与新编号冲突
- 为固定团队与新高潮链补出可直接试跑的角色、场景和状态 UI 请求模板

## 4. 当前冻结共识

- 玩家身份：`未来湾固定团队主位`
- 第四路径性质：`困难可能性`，不是隐藏正确答案
- 回响台性质：`表达场 + 资格校验 + 责任签署装置`
- 本集长线阴影：“系统看起来很体贴，其实在替人决定人生”
- 结果层：至少区分 `公开申诉 / 观察期接入 / 争议附件`

## 5. 当前仍开放事项

- `asset-manifest.json` 仍需继续补第二轮及之后的真实生成记录
- `api-requests/` 目前主要覆盖视觉请求，声音与更多 UI 请求模板仍可继续补
- chapter-02 尚未建立与 chapter-01 同级的稳定骨架

## Version `v0.7`

- 日期：`2026-03-21`
- 阶段：`Flow 试片落地`
- 目标：把“可以直接用 Flow 做小成本验证”这件事落成 chapter-01 的正式生产入口

### 主要产出

- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [agents.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/agents.md)
- [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)

### 核心变化

- 为 `chapter-01` 新增一份明确面向 `Google Flow` 的低成本纵切试片包
- 从现有锁定结构中挑出最值得先验证的 8 个关键视频镜头
- 为每个镜头补齐中文导演意图、英文主 prompt、运镜 prompt、负向约束和通过标准
- 把已有角色 / 场景 / keyframe 请求模板重新组织为 `Flow` 可直接搭配的参考图入口
- 明确本轮目标是验证 `团队感 / 世界感 / 中段反转 / 连续剧钩子`，而不是直接追完整成片

## Version `v0.8`

- 日期：`2026-03-21`
- 阶段：`主稿重写与角色锁定`
- 目标：把 chapter-01 从“已经有改进方向”推进到“主稿已落实改进，角色已进入定妆准备”的状态

### 主要产出

- [master-episode-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/master-episode-script.md)
- [character-lock-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/visual/character-lock-pack.md)

### 核心变化

- 重写 chapter-01 主稿，把“固定团队 + 长线阴影 + 世界层持续冒险能力”落实到整集体验
- 把玩家主位、林澄、序列员 07、祁野、闻夏的连续剧化功能重新压实
- 新增可用于人物生图锁定的 `character-lock-pack`
- 为后续场景母图、图生视频和分镜执行做准备

## Version `v0.9`

- 日期：`2026-03-22`
- 阶段：`分镜执行稿升级`
- 目标：把 chapter-01 的后半段镜头从“可读分镜”推进到“可直接衔接生图、图生视频、前端 UI 与声音制作”的执行粒度

### 主要产出

- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)

### 核心变化

- 把 `shot-list.md` 的 `C01-G05` 补齐 `source_beat / 镜头目标 / 起始帧 / 视频段提示 / 参考资产 / 生成路由 / 风险提示`
- 明确回绑 `S-03` 到 `S-09` 场景资产，以及 `C-02`、`C-03`、`C-04`、`C-05`、`C-07`、`C-08` 等角色资产
- 让悬浮档案大厅、概率长廊、暗层接口、自由回响台和终局回航都进入同一套 production 语言
- 为后续补 `api-requests`、出 keyframe、接 Flow 或其他图生视频链路建立统一镜头口径

## Version `v0.10`

- 日期：`2026-03-22`
- 阶段：`首轮视频执行包补位`
- 目标：把 chapter-01 从“已有镜头与试片方向”推进到“首轮 Flow / I2V 试跑可以直接开做”的状态

### 主要产出

- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [README.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/README.md)
- [shot-a03-grey-silver-mission-signal-keyframe.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-a03-grey-silver-mission-signal-keyframe.json)
- [shot-b03-time-archive-city-approach-keyframe.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-b03-time-archive-city-approach-keyframe.json)
- [shot-d01-probability-corridor-reveal-keyframe.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-d01-probability-corridor-reveal-keyframe.json)
- [shot-g04-return-archive-wall-keyframe.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-g04-return-archive-wall-keyframe.json)

### 核心变化

- 为 `CH01-P01` 前段信号位、`P02` 入港逼近位、`CH01-P05-S01`、`CH01-P11-S04` 新增可直接调用的 shot keyframe 模板
- 把 `SHOT-A03 / SHOT-B03 / SHOT-D01 / SHOT-G04` 这批历史模板正式纳入 `asset-manifest` 的生产追踪范围，并以 canonical 编号解释其职责
- 为 `Flow` 第一优先批新增一张可执行 clip 表，明确时长、起始帧、路由与声音策略
- 把 `FV-02 / FV-03 / FV-05 / FV-08` 从“依赖场景母图”推进到“有明确镜头首帧参考”的状态

## Version `v0.11`

- 日期：`2026-03-23`
- 阶段：`P01 分镜重拆`
- 目标：按主剧本重新拆分未来湾开场，让 canonical 分镜先服务故事理解，再服务视频装配

### 主要产出

- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)

### 核心变化

- 把 `P01` 从“港口 / 信号 / 交班 / 出发挤在一起”改成 `到场 -> 灰银信号 -> 阿潮接入 -> 固定小队运转 -> 守望者交班 -> 争议切片与责任后果 -> 接受任务启航`
- 明确阿潮和固定小队必须在开场里真实成立，而不是继续被空镜头和抽象装置替代
- 把 `CH01-P01-S06 / S07` 的职责重新切开为“争议切片 + 任务简报层”与“接受任务后的启航”，不再默许旧交付把它们压成一个信息不足的片段
- 在 `flow-vertical-slice-pack.md` 中明确：现有 `part-01-future-bay-task-dock-delivery-v1.mp4` 仍可作为 look-dev，但不再等于最新正式分镜编号

## Version `v0.12`

- 日期：`2026-03-24`
- 阶段：`P01 音频交付补强`
- 目标：把 `P01` 从“画面已可看、声音明显拖后腿”推进到“内部可交付试听”的状态

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [part-01-future-bay-task-dock-delivery-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v2.mp4)
- [part-01-future-bay-task-dock-delivery-v2.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v2.metadata.json)
- [part1-v2-watchkeeper-task.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v2-watchkeeper-task.aiff)
- [part1-v2-watchkeeper-responsibility.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v2-watchkeeper-responsibility.aiff)
- [part1-v2-achao-line.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v2-achao-line.aiff)
- [part1-v2-qiye-line.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v2-qiye-line.aiff)
- [part1-v2-wenxia-line.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v2-wenxia-line.aiff)
- [part1-v2-echo-line.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v2-echo-line.aiff)

### 核心变化

- 把 `P01` 的音轨从“单一占位感播报”升级成 `守望者 / 阿潮 / 祁野 / 闻夏 / 回响` 的多角色试音结构
- 新增 `signal pulse / ui rise / route swell / rumble bed` 等任务声场，提升任务信号、简报展开和启航段的世界内连续性
- 保留并强化 `CH01-P01-S06 -> S07` 的 `J-cut` 进入方式，让守望者的责任话语更像把画面推进出发，而不是后贴说明
- 输出一条新的 `part-01-future-bay-task-dock-delivery-v2.mp4`，并同步保存最小 metadata 与可复用 voice stems

## Version `v0.13`

- 日期：`2026-03-24`
- 阶段：`P01 正式试音替换`
- 目标：把 `P01` 从“人声和配乐仍明显像占位”推进到“可继续交付试听的后期配音版”

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [voice-first-round-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-first-round-pack.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [part-01-future-bay-task-dock-delivery-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v3.mp4)
- [part-01-future-bay-task-dock-delivery-v3.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v3.metadata.json)
- [part1-v3-watchkeeper-task-formal.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v3-watchkeeper-task-formal.aiff)
- [part1-v3-watchkeeper-responsibility-formal.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v3-watchkeeper-responsibility-formal.aiff)
- [part1-v3-achao-formal.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v3-achao-formal.aiff)
- [part1-v3-qiye-formal.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v3-qiye-formal.aiff)
- [part1-v3-wenxia-formal.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v3-wenxia-formal.aiff)
- [part1-v3-echo-formal.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v3-echo-formal.aiff)

### 核心变化

- 把 `P01` 的人声从 `macOS say` 占位试音切换成 `edge-tts` 中文神经语音，并按角色做独立后期处理
- 正式锁定一套 `守望者 / 阿潮 / 祁野 / 闻夏 / 回响` 的 `P01` 试音执行映射，避免后续每轮重猜声音
- 把任务交付段到任务简报段的桥接声场细化为 `handoff shimmer / panel bloom / card tick / ui rise`
- 把 `CH01-P01-S07` 的启航声场细化为 `launch whoosh / route swell / city draw / glass air`
- 输出新的 `part-01-future-bay-task-dock-delivery-v3.mp4`，作为当前主试听版本

## Version `v0.14`

- 日期：`2026-03-24`
- 阶段：`P01 编辑母带收口`
- 目标：把 `P01` 从“声音方向对了但人声仍过密”推进到“更像正式剧集开场的可交付母带”

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [voice-first-round-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-first-round-pack.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [part-01-future-bay-task-dock-delivery-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v4.mp4)
- [part-01-future-bay-task-dock-delivery-v4.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v4.metadata.json)
- [part1-v4-achao-approach.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v4-achao-approach.aiff)
- [part1-v4-watchkeeper-handoff.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v4-watchkeeper-handoff.aiff)
- [part1-v4-echo-brief.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v4-echo-brief.aiff)
- [part1-v4-watchkeeper-responsibility.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v4-watchkeeper-responsibility.aiff)

### 核心变化

- 把 `P01` 的开场人声从 6 条并发信息收成 4 条必要短句，减少“听感像说明会”的问题
- 把守望者、阿潮、回响的 `P01` 文稿改写成更能贴住镜头时长的交付版短句
- 在最终混音里加入 `speech ducking`，让背景环境声在发声位自动退后
- 把交付规格重新锁定为 `1152x768 / 30fps / 23.8s / AAC stereo`
- 更新主 HTML 资产页，让 `v4` 成为当前唯一主交付入口

## Version `v0.15`

- 日期：`2026-03-24`
- 阶段：`P02 纸片验证落地`
- 目标：把 `P02` 从“导演和分镜已成立，但还没可看片”推进到“能审节奏、能判断是否值得继续烧视频”的低成本验证版

### 主要产出

- [render_chapter01_part2_papercut.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part2_papercut.sh)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [part-02-emergency-entry-check-papercut-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-02-emergency-entry-check-papercut-v1.mp4)
- [part-02-emergency-entry-check-papercut-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-02-emergency-entry-check-papercut-v1.metadata.json)

### 核心变化

- 把 `P02` 的 `CH01-P02-S01-S04`（兼容别名 `B01-B04`）收成一条 `22.4s` 的 paper cut 验证成片，先验证信息顺序、准入压力和 `S-02 -> S-03` 过桥是否成立
- 用现有 `S-02 / S-03` 场景母图与后叠 UI 的方式跑通 `临时观察许可校验`，避免直接把预算烧在低价值教程视频上
- 新增 `CH01-P02-S02` 许可校验层和 `CH01-P02-S03` 限制动作层的可复用 UI 叠层，以及守望者 / 系统校验层的最小必要配音
- 为后续正式生成明确优先级：`CH01-P02-S01` 航行 clip 与 `CH01-P02-S04` 过桥 clip 优先，`CH01-P02-S02/S03` 继续保持 UI-first

## Version `v0.16`

- 日期：`2026-03-24`
- 阶段：`P02 主交付链建立`
- 目标：把 `P02` 从“已有 paper cut 节奏验证”推进到“已有稳定主装配文件，并能直接接正式 Wan clip 升级”的状态

### 主要产出

- [render_chapter01_part2_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part2_delivery.sh)
- [shot-b01-entry-approach-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-b01-entry-approach-wan2.6-i2v-flash-v1.json)
- [shot-b04-entry-bridge-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-b04-entry-bridge-wan2.6-i2v-flash-v1.json)
- [part-02-emergency-entry-check-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-02-emergency-entry-check-delivery-v1.mp4)
- [part-02-emergency-entry-check-delivery-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-02-emergency-entry-check-delivery-v1.metadata.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 为 `P02` 建立单一主装配文件 `part-02-emergency-entry-check-delivery-v1.mp4`，避免后续继续堆平行试片
- 把 `CH01-P02-S01` 与 `CH01-P02-S04` 固定为正式视频插槽，并补出对应 Wan 请求模板
- 主装配脚本支持 `真实 clip 优先、无 clip 则回退场景母图` 的稳定升级路径
- 主 HTML 资产页同步改为展示 `P02 delivery v1`，保留 `paper cut v1` 作为节奏基线而不是主入口

## Version `v0.17`

- 日期：`2026-03-24`
- 阶段：`P01 口型与尾段气氛修正`
- 目标：把 `P01` 从“结构和混音已基本成立，但仍有口型错位与尾段配乐失真”推进到真正可作为主交付的开场版本

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [part-01-future-bay-task-dock-delivery-v5.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v5.mp4)
- [part-01-future-bay-task-dock-delivery-v5.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v5.metadata.json)
- [part1-v5-watchkeeper-handoff.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v5-watchkeeper-handoff.aiff)
- [part1-v5-watchkeeper-responsibility.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v5-watchkeeper-responsibility.aiff)
- [part1-v5-achao-approach.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v5-achao-approach.aiff)
- [part1-v5-echo-brief.aiff](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/audio/part1-v5-echo-brief.aiff)

### 核心变化

- 把守望者第一句从任务交付可见位移到 `CH01-P01-S06` 任务简报段，改成剪辑上成立的 offscreen 交付
- 保留 `CH01-P01-S05` 的交付视觉，但不再让它承担无法对口型的人声表演
- 从主交付中移除 `CH01-P01-S07` 启航段的模型自动音轨，直接消除尾段偏欢快配乐
- 重新平衡 `launch / route / city` 尾段世界声场，保留启航牵引感但不再破坏制度压力气氛
- 把主 HTML 资产页同步切到 `v5` 作为当前唯一 `P01` 主入口，并统一展示层使用 `规范编号 + 历史文件别名` 的口径

## Version `v0.18`

- 日期：`2026-03-24`
- 阶段：`P01 开场导演复盘`
- 目标：明确当前 `P01` 主交付的真实能力边界，阻止后续继续把“气质样片”误判成“已经讲清楚故事的正式开场”

### 主要产出

- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [version-log.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/version-log.md)
- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v8.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v8.mp4)
- [shot-ch01-p01-s04-team-operating-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-images/shot-ch01-p01-s04-team-operating-v1.json)
- [shot-ch01-p01-s06-lin-cheng-dispute-slice-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-images/shot-ch01-p01-s06-lin-cheng-dispute-slice-v1.json)

### 核心变化

- 明确当前 `P01 v8` 只可继续作为 `teaser / assembly look-dev / 气质验证版` 使用，不再把它口头升级成“已经讲清 chapter-01 开头”的正式开场
- 明确 `CH01-P01-S04` 固定小队运转镜头仍然缺失，这是当前开头“看着有气质但仍然莫名其妙”的核心原因之一
- 明确 `CH01-P01-S06` 必须回到 `林澄争议切片 -> 任务性质 -> 责任后果` 的信息顺序，而不是继续停留在泛任务简报 UI
- 明确 `CH01-P01-S06` 与 `CH01-P01-S07` 必须继续分开，因为“知道任务是什么”和“真的决定出发”是两个不同戏剧动作
- 在 `render_chapter01_part1_delivery.sh` 顶部补写边界说明，避免后续继续把当前 `A01-A06` 历史装配链误读成 `CH01-P01-S01-S07` 已经全部落地

### 唯一优先下一步

- 先按主剧本把 `P01` 重装配成真正的 `7-beat opening assembly`
- 在新装配成立前，不再继续对当前 `v8` 做零碎声音修补或 HTML 话术升级

## Version `v0.19`

- 日期：`2026-03-24`
- 阶段：`P01 canonical story-clear 重装配`
- 目标：把 `P01` 从“已知结构不清的 teaser 交付”推进到“第一次真正按 canonical `S01-S07` 讲通故事顺序的主装配”

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [part-01-future-bay-task-dock-delivery-v9.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v9.mp4)
- [part-01-future-bay-task-dock-delivery-v9.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v9.metadata.json)
- [shot-ch01-p01-s04-team-operating-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-images/shot-ch01-p01-s04-team-operating-v1.json)
- [shot-ch01-p01-s06-lin-cheng-dispute-slice-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-images/shot-ch01-p01-s06-lin-cheng-dispute-slice-v1.json)
- [shot-ch01-p01-s04-team-operating-v1-qwen-image-2.0-pro.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p01-s04-team-operating-v1-qwen-image-2.0-pro.png)
- [shot-ch01-p01-s06-lin-cheng-dispute-slice-v1-qwen-image-2.0-pro.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p01-s06-lin-cheng-dispute-slice-v1-qwen-image-2.0-pro.png)
- [p01-s06-dispute-overlay-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/ui/p01-s06-dispute-overlay-v1.png)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 直接放弃“继续在旧 `A01-A06` 动态串上补一点声音也许就能讲清”的错误路线，改为按 `CH01-P01-S01-S07` 重新装配
- 补出 `CH01-P01-S04` 固定小队运转首帧，并把 `S03/S04` 当前先收成 `受控静帧 + 离屏对白` 的低风险验证方案
- 补出 `CH01-P01-S06` 林澄争议切片首帧，并新增 `dispute overlay`，让“林澄是谁 / 为什么今晚必须立刻去 / 失败后果是什么”第一次在开场里被清楚看见
- 把所有高风险 visible speech 从主交付中移走，统一改为 `离屏 / 无线 / 系统层`，避免继续把口型失败塞进主视频
- 把尾段 `S07` 改成受控启航静帧动化，移除模型自发英文样文字和不合气氛的尾段音乐

## Version `v0.20`

- 日期：`2026-03-25`
- 阶段：`P01 同步镜头升级`
- 目标：在 `v9` 先把故事讲清楚的基础上，把仍停留在纸片承接的关键段落推进成真正的同步音视频镜头

### 主要产出

- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [shot-ch01-p01-s03-achao-arrival-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p01-s03-achao-arrival-wan2.6-i2v-flash-v1.json)
- [shot-ch01-p01-s04-team-operating-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p01-s04-team-operating-wan2.6-i2v-flash-v1.json)
- [shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v1.json)
- [shot-ch01-p01-s07-route-ignite-wan2.6-i2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p01-s07-route-ignite-wan2.6-i2v-flash-v1.json)
- [shot-ch01-p01-s03-achao-arrival-wan2.6-i2v-flash-v1-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s03-achao-arrival-wan2.6-i2v-flash-v1-720p.mp4)
- [shot-ch01-p01-s04-team-operating-wan2.6-i2v-flash-v1-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s04-team-operating-wan2.6-i2v-flash-v1-720p.mp4)
- [shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v1-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s06-lin-cheng-dispute-slice-wan2.6-i2v-flash-v1-720p.mp4)
- [shot-ch01-p01-s07-route-ignite-wan2.6-i2v-flash-v1-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s07-route-ignite-wan2.6-i2v-flash-v1-720p.mp4)
- [part-01-future-bay-task-dock-delivery-v10.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v10.mp4)
- [part-01-future-bay-task-dock-delivery-v10.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v10.metadata.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 把 `S03` 从“纸片上的阿潮离屏播报”升级成阿潮接入的同步音视频镜头
- 把 `S04` 从“固定小队 still-motion”升级成祁野工作中发声的同步镜头，稳定团队责任感
- 把 `S06` 升级成林澄在镜头里说关键一句的同步镜头，并继续用 overlay 压住模型自发文档文字
- 把 `S07` 从静帧启航升级回真实 world-audio 启航镜头，同时保留“无人声、无配乐、无随机文字”的边界
- `P01 v10` 现在已经不再依赖手工后贴角色对白，主交付中的关键人声全部改为镜头内同步生成

## Version `v0.24`

- 日期：`2026-03-25`
- 阶段：`P02/P03 wan2.6-r2v workflow 实战`
- 目标：不再停留在“脚本已支持 R2V”，而是把 `wan2.6-r2v-flash` 放进 chapter workflow 的真实镜头里，判断它到底适合哪些 shot

### 主要产出

- [generate_dashscope_videos.py](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/generation/generate_dashscope_videos.py)
- [render_chapter01_part2_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part2_delivery.sh)
- [shot-b04-entry-bridge-wan2.6-r2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-b04-entry-bridge-wan2.6-r2v-flash-v1.json)
- [shot-b04-entry-bridge-wan2.6-r2v-flash-v2.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-b04-entry-bridge-wan2.6-r2v-flash-v2.json)
- [shot-ch01-p03-s01-hall-establishing-wan2.6-r2v-flash-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/dashscope-videos/shot-ch01-p03-s01-hall-establishing-wan2.6-r2v-flash-v1.json)
- [shot-b04-entry-bridge-wan2.6-r2v-flash-v1-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-b04-entry-bridge-wan2.6-r2v-flash-v1-720p.mp4)
- [shot-b04-entry-bridge-wan2.6-r2v-flash-v2-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-b04-entry-bridge-wan2.6-r2v-flash-v2-720p.mp4)
- [shot-ch01-p03-s01-hall-establishing-wan2.6-r2v-flash-v1-720p.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p03-s01-hall-establishing-wan2.6-r2v-flash-v1-720p.mp4)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 把 DashScope 视频生成脚本扩成真正支持 `reference_sources -> reference_urls` 的 `R2V` 路线，不再只能跑单图 `I2V`
- 用 `B04` 做了两轮 `R2V` 实战，明确验证出这类“强第一人称桥接镜头”并不适合当前 `R2V` 主线使用
- 立刻把 `render_chapter01_part2_delivery.sh` 改成 `R2V` 试片默认不回写主装配，避免失败 clip 被自动吞回 `P02`
- 改把 `R2V` 试点推进到 `CH01-P03-S01`，并成功生成 `C01` 大厅建立镜头的第一条可用候选
- 明确 chapter-01 的下一条主制作线从 `P01` 转向 `P03`，以“讲清大厅冲突入口”为优先，而不是继续在 `P01` 或 `B04` 上反复消耗

## Version `v0.26`

- 日期：`2026-03-25`
- 阶段：`OpenAI 兼容 Veo relay 横版参数验证`
- 目标：把第三方 relay 的 `veo-3.1` 调用从“能偶尔成功”推进到“明确知道什么参数和参考图组合可用”

### 主要产出

- [generate_openai_videos.py](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/generation/generate_openai_videos.py)
- [shot-ch01-p03-s04-sequence-officer-veo-3.1-i2v-b64-probe-adult-control-size-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-videos/shot-ch01-p03-s04-sequence-officer-veo-3.1-i2v-b64-probe-adult-control-size-v1.json)
- [shot-ch01-p03-s04-sequence-officer-veo-3.1-i2v-b64-probe-multi-image-size-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-videos/shot-ch01-p03-s04-sequence-officer-veo-3.1-i2v-b64-probe-multi-image-size-v1.json)
- [shot-ch01-p03-s04-sequence-officer-veo-3.1-i2v-b64-probe-adult-control-size-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p03-s04-sequence-officer-veo-3.1-i2v-b64-probe-adult-control-size-v1.mp4)
- [shot-ch01-p03-s04-sequence-officer-veo-3.1-i2v-b64-probe-multi-image-size-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p03-s04-sequence-officer-veo-3.1-i2v-b64-probe-multi-image-size-v1.mp4)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 明确验证：该第三方 relay 不应按原生 Google / `v1beta` 思路调用，主路线应按 `OpenAI 兼容格式`
- 把 `size = 1280x720` 与 `aspect_ratio = 16:9` 补进 probe 后，单图与多图 `I2V` 都能稳定输出横版 `1280x720`
- 明确踩实一条新门控：如果参考图里混入未成年角色，会触发 `PUBLIC_ERROR_MINOR_UPLOAD`；因此当前 relay 上的成人镜头 probe 必须坚持 `adult-only refs`
- 明确踩实第二条门控：`横版首帧 + 竖版角色照` 会把构图拖偏；必须改成 `horizontal keyframe + horizontal adult-only ref`
- 把失败回包也写入 metadata，避免后续调参数时再次黑箱

## Version `v0.27`

- 日期：`2026-03-27`
- 阶段：`P04 等待区与父亲 workflow 收束`
- 目标：把 `P04` 从“概念上存在但 production 不可执行”的状态，推进到真正可进参考锁定与首帧生成的主线状态

### 主要产出

- [storyboard-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/story/storyboard-script.md)
- [product-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/product/product-script.md)
- [voice-script.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/audio/voice-script.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [asset-manifest.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/asset-manifest.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)

### 核心变化

- 用导演室结论把 `P04` 从原来的 4 镜改成 5 镜：`等待区进入 -> 签字笔/安抚屏 -> 双目标成立 -> 父亲短线 -> 林澄短线`
- 把 `P04` 中误写成父亲的 `C-08` 全部改回正确角色 `C-06`，避免后续请求继续把数字导师混入等待区
- 固定连续剧线性交付顺序为 `父亲先 -> 林澄后`，同时保留产品层的顺序选择，不再让“为保分支”破坏主线叙事清晰度
- 把 Scene 04 的主线对白缩成两条可控 `visible speech` 短线，其余长句下放到交互分支或后续同步能力更稳的版本
- 在 `asset-manifest` 中正式启用 `S-11 家属等待区`，为后续 waiting-zone keyframe 与 speaking-ready 近景建立明确资产锚点

## Version `v0.28`

- 日期：`2026-03-27`
- 阶段：`P04 等待区与父亲交付收口`
- 目标：把 `P04` 从“已锁文档与 keyframe”推进到真正可审片的 part delivery，并把通过质量门的关键资产回写到主资产入口

### 主要产出

- [render_chapter01_part4_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part4_delivery.sh)
- [part-04-waiting-zone-and-father-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-04-waiting-zone-and-father-delivery-v1.mp4)
- [shot-ch01-p04-s03-waiting-zone-choice-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p04-s03-waiting-zone-choice-viduq3-i2v-v1.mp4)
- [shot-ch01-p04-s04-father-close-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p04-s04-father-close-viduq3-i2v-v1.mp4)
- [shot-ch01-p04-s05-lin-close-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p04-s05-lin-close-viduq3-i2v-v1.mp4)
- [shot-ch01-p04-s01-waiting-zone-ingress-v2-clean3.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p04-s01-waiting-zone-ingress-v2-clean3.png)
- [shot-ch01-p04-s02-sign-pen-soothing-screen-v1-imagen4.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p04-s02-sign-pen-soothing-screen-v1-imagen4.png)
- [p04-s02-soothing-screen-overlay-v1.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/ui/p04-s02-soothing-screen-overlay-v1.png)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 严格按 `P04` 的 5 镜合同推进：`S01` 先成立等待区，`S02` 再给签字笔与安抚屏温柔压迫，之后才进入 `S03-S05` 的关系和对白
- 用 `viduq3-turbo img2video` 跑通 `S03-S05` 的音视频同步 clip，并通过 `first frame / identity / audio contract` 轻量质量门
- 新增 `render_chapter01_part4_delivery.sh`，把 `S01/S02` 收成稳定画面与世界内环境声，不再把这一段做成漂浮 still-motion
- `S04` 与 `S05` 保留镜头内同步短对白，不再回退到后贴长台词路线
- 把 `P04` 主交付和通过质量门的 keyframe / clip 回写到主资产目录，同时把 loop 控制切到 `P05`

## Version `v0.36`

- 日期：`2026-03-28`
- 阶段：`P05 概率长廊 W7 收口并推入 W8`
- 目标：把 `P05` 从“rough preview 已经能看，但还没人正式拍板”推进到真正可提交生成的状态

### 主要产出

- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [shot-ch01-p05-s01-probability-corridor-reveal-viduq3-i2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p05-s01-probability-corridor-reveal-viduq3-i2v-v1.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 正式把 `P05` 的 `W7` 视频与 audio contract 写实：`D01` 负责三路径短揭示、`D02` 固定 `UI-first`、`D04` 固定为 `P05 -> P06` bridge
- 把 `P05` loop 状态从 `W7 / PASS WITH NOTES` 推到 `W8 / READY FOR GENERATION`，避免第一集在“rough preview 已通过但没人开跑”处再次停住
- 为 `D01` 新增一条真正可提交的 `qingyun / viduq3-turbo img2video` 请求模板，优先用低成本短 clip 去验证三路径奇观是否能在正式视频里成立
- 同步把主 HTML 的 `P05` 状态改成 `W8` 口径，确保资产页和 loop 控制板不再互相错位

## Version `v0.37`

- 日期：`2026-03-28`
- 阶段：`P05 D01 首条正式视频生成`
- 目标：把 `D01` 从“有请求模板”推进到“真正有一条可审的正式短 clip”，避免 `W8` 停留在纸面

### 主要产出

- [shot-ch01-p05-s01-probability-corridor-reveal-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p05-s01-probability-corridor-reveal-viduq3-i2v-v1.mp4)
- [shot-ch01-p05-s01-probability-corridor-reveal-viduq3-i2v-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p05-s01-probability-corridor-reveal-viduq3-i2v-v1.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [shot-list.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/shot-list.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 真正提交并生成了 `D01` 的首条正式 `img2video` 短 clip，不再只停在 request template
- 最小合同已成立：三路径关系可读、无人物、无第四色、无隐藏入口提前泄露
- 当前保留 notes 也被明确写回：长廊仍偏 `波浪隧道`，右侧还有 `exhibit wall` 感，因此当前判断为 `W9 / PASS WITH NOTES`
- loop 已继续向前推进到审片门，不再停在 `W8 / READY FOR GENERATION`

## Version `v0.38`

- 日期：`2026-03-28`
- 阶段：`P05 正式交付收口`
- 目标：把 `P05` 从单镜头 QC 推进到真正的 part-level 交付，并把 active part 交给 `P06`

### 主要产出

- [shot-ch01-p05-s01-probability-corridor-reveal-viduq3-i2v-v2-straight-corridor.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p05-s01-probability-corridor-reveal-viduq3-i2v-v2-straight-corridor.mp4)
- [shot-ch01-p05-s04-wind-anomaly-reaction-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p05-s04-wind-anomaly-reaction-viduq3-i2v-v1.mp4)
- [render_chapter01_part5_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part5_delivery.sh)
- [part-05-probability-corridor-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-05-probability-corridor-delivery-v1.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `D01` 的唯一救援版 `v2` 已实际生成，但没有明显优于 `v1`，因此主线保留 `D01 v1` 作为 `story-first accepted with notes`
- `D04` 已从 rough keyframe 升级成正式带人声 bridge clip，人物稳定、动作成立、且没有提前泄露暗层
- 新增 `render_chapter01_part5_delivery.sh`，把 `D01 clip + D02 UI-first + D04 clip` 装成 `P05` 的正式 part-level 交付
- `P05` 现在正式提升为 `accepted_with_notes`，active part 已切到 `P06`

## Version `v0.39`

- 日期：`2026-03-30`
- 阶段：`P10 / F03 Qingyun rotation 首轮补测`
- 目标：把 `P10 / F03` 从“只有零散模型试错”推进到“有真实轮换记录的可恢复模型池”

### 主要产出

- [run_p10_f03_qingyun_rotation.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/run_p10_f03_qingyun_rotation.sh)
- [generate_qingyun_vidu.py](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/generation/generate_qingyun_vidu.py)
- [p10-f03-new-models-failure-log.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-vidu/metadata/failures/p10-f03-new-models-failure-log.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 为 `P10 / F03` 新增并接入 11 个 Qingyun 候选模型模板，扩成 15 模型 rotation 池
- 真实使用旧 Qingyun key 对新增 11 模型做过一轮批量补测，当前通过数仍为 `0`
- 第一轮失败结果已经开始分层，可用于后续轮换策略：
- `401`：`doubao-seedance-lite-i2v`、`hailuo-2.3-fast`
- `502`：`doubao-seedance-pro-fast`、`jimeng-video-3.0`、`jimeng-4.0`、`jimeng-4.1`、`minimax/video-01`、`wan2.5-i2v-preview`、`wan2.6-i2v`
- `429`：`jimeng-4.5`、`minimax/video-01-live`
- `generate_qingyun_vidu.py` 已补上 `--continue-on-error` 与结构化 failure log，后续可以直接按 rotation 链继续筛“今天能用的模型”

## Version `v0.57`

- 日期：`2026-03-30`
- 阶段：`P10 / F03 Qingyun rotation 二轮收紧`
- 目标：把 `P10 / F03` 的第一轮“返回码分层”继续收口成更准确的生产判断，避免把 `429 / 502` 误判成已经可用的轮换候选

### 主要产出

- [p10-f03-rotation-retry1-failure-log.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-vidu/metadata/failures/p10-f03-rotation-retry1-failure-log.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 对首轮最像“有机会”的 `5` 个模型做了第二轮真实重试：
  - `jimeng-4.5`
  - `minimax/video-01-live`
  - `wan2.6-i2v`
  - `jimeng-4.0`
  - `jimeng-video-3.0`
- 第二轮结果全部回落为 `HTTP 401 Unauthorized`
- 因此第一轮里的 `429 / 502` 不再被视为当前 session 下的可优先轮换候选
- 当前更准确的结论是：`P10 / F03` 已接入并真实试过的 `15` 个 Qingyun 模型里，稳定通过数仍为 `0`
- `run_p10_f03_qingyun_rotation.sh` 与 `--continue-on-error` 现在仍然有价值，但它们当前承担的是“provider 恢复后快速复投”的恢复 harness，而不是已经筛出可用模型的生产轮换池

## Version `v0.58`

- 日期：`2026-03-30`
- 阶段：`P10 / F03 Qingyun 新家族补测`
- 目标：不给 `P10 / F03` 停在旧的 15 模型结论上，而是把 `veo / sora / grok-video` 家族也真正接进 rotation 池并做一轮最小实投

### 主要产出

- [shot-ch01-p10-s03-opponent-projection-veo2-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo2-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo2-fast-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo2-fast-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo3-fast-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo3-fast-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo3.1-fast-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo3.1-fast-v1.json)
- [shot-ch01-p10-s03-opponent-projection-sora-2-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-sora-2-v1.json)
- [shot-ch01-p10-s03-opponent-projection-grok-video-3-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-grok-video-3-v1.json)
- [run_p10_f03_qingyun_rotation.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/run_p10_f03_qingyun_rotation.sh)
- [p10-f03-new-families-failure-log.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-vidu/metadata/failures/p10-f03-new-families-failure-log.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 新接入并真实补测了 `6` 条家族：
  - `veo2`
  - `veo2-fast`
  - `veo3-fast`
  - `veo3.1-fast`
  - `sora-2`
  - `grok-video-3`
- 这轮结果为：
  - `401`：`veo2`、`veo2-fast`、`veo3-fast`、`sora-2`、`grok-video-3`
  - `429`：`veo3.1-fast`
- 因此 `P10 / F03` 当前已接入并真实测试过的 Qingyun tested pool 扩到 `21`
- 当前仍没有稳定通过项，但 `veo3.1-fast` 可保留为下一次冷却后再探的观察名单

## Version `v0.59`

- 日期：`2026-03-30`
- 阶段：`P10 / F03 veo 家族近亲补测`
- 目标：既然 `veo3.1-fast` 是上一轮唯一非 `401` 的新家族，就继续沿它的近亲往下试，而不是立刻回到明显无信号的枝杈

### 主要产出

- [shot-ch01-p10-s03-opponent-projection-veo2-pro-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo2-pro-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo3.1-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo3.1-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo3.1-pro-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo3.1-pro-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo3-pro-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo3-pro-v1.json)
- [shot-ch01-p10-s03-opponent-projection-luma-video-api-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-luma-video-api-v1.json)
- [p10-f03-veo-family-retry-failure-log.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-vidu/metadata/failures/p10-f03-veo-family-retry-failure-log.json)

### 核心变化

- 新补测的 `5` 条近亲结果为：
  - `401`：`veo2-pro`、`veo3.1`、`veo3-pro`、`luma_video_api`
  - `502`：`veo3.1-pro`
- 因此 `P10 / F03` 当前已接入并真实测试过的 Qingyun tested pool 扩到 `26`
- 当前仍没有稳定通过项，但 `veo3.1-fast = 429` 与 `veo3.1-pro = 502` 现在可以一起保留在下一次冷却后的观察名单

## Version `v0.60`

- 日期：`2026-03-30`
- 阶段：`P10 / F03 veo3.1 变体补测`
- 目标：把 `veo3.1` 线上仍可见的 `components` 与下划线别名也真正试掉，避免后面反复怀疑“是不是还漏了同一家族的别名入口”

### 主要产出

- [shot-ch01-p10-s03-opponent-projection-veo3.1-components-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo3.1-components-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo3.1-fast-components-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo3.1-fast-components-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo_3_1-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo_3_1-v1.json)
- [shot-ch01-p10-s03-opponent-projection-veo_3_1-fast-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p10-s03-opponent-projection-veo_3_1-fast-v1.json)
- [p10-f03-veo31-variant-failure-log.json](/Users/wujames/Desktop/AI未来通识课（K12）/archive/workbench-defaults/qingyun-vidu/metadata/failures/p10-f03-veo31-variant-failure-log.json)

### 核心变化

- 新补测的 `4` 条变体结果全部为 `401`：
  - `veo3.1-components`
  - `veo3.1-fast-components`
  - `veo_3_1`
  - `veo_3_1-fast`
- 因此 `P10 / F03` 当前已接入并真实测试过的 Qingyun tested pool 扩到 `30`
- 目前仍最值得保留的观察位没有变化，依旧是：
  - `veo3.1-fast = 429`
  - `veo3.1-pro = 502`

## Version `v0.62`

- 日期：`2026-03-31`
- 阶段：`P07-P09 故事补桥预览`
- 目标：不再只停留在“知道中段缺失让整章像预告片”的分析层，而是先用低成本 bridge preview 把 `P07-P09` 的因果承重补回去，并直接装进章节 spine 做 story-level 对照

### 主要产出

- [render_chapter01_part7to9_bridge_papercut.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part7to9_bridge_papercut.sh)
- [part-07-09-middle-bridge-papercut-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-07-09-middle-bridge-papercut-v1.mp4)
- [part-07-09-middle-bridge-papercut-v1.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-07-09-middle-bridge-papercut-v1.metadata.json)
- [render_chapter01_story_spine_preview.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_story_spine_preview.sh)
- [chapter-01-story-spine-preview-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v1.mp4)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 当前已新增一条不进入 `current` 的 `P07-P09` 中段 bridge preview：
  - `P07` 补回第四路径的人性承重
  - `P08` 补回 `07` 的制度公平性与公共分配压力
  - `P09` 补回证据链误包为事实后的第一次真实反噬与团队分裂
- 当前已把这条 bridge 插回章节 spine，形成 `chapter-01 story spine preview`
- 这轮新增资产的正式口径固定为：
  - `story-first preview`
  - `not accepted current`
  - `用于比较 vertical slice 与更完整故事链的差异`
- 当前 `accepted spine`、`outputs/current-chapter-01/` 与 `video-loop-state.json` 都保持不变：
  - 不把预览误写成 accepted 主线
  - 不用新 preview 污染 current 交付入口

## Version `v0.63`

- 日期：`2026-03-31`
- 阶段：`P07-P09 故事补桥 v2`
- 目标：不再只停在“知道该补哪三处桥”，而是把 `P06 -> P07`、`P07 -> P08`、`P09 -> P10` 三个结构补丁直接装进新的 preview，并重出新的章节级对照版

### 主要产出

- [render_chapter01_part7to9_bridge_papercut.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part7to9_bridge_papercut.sh)
- [part-07-09-middle-bridge-papercut-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-07-09-middle-bridge-papercut-v2.mp4)
- [part-07-09-middle-bridge-papercut-v2.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-07-09-middle-bridge-papercut-v2.metadata.json)
- [render_chapter01_story_spine_preview.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_story_spine_preview.sh)
- [chapter-01-story-spine-preview-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v2.mp4)
- [chapter-01-story-spine-preview-v2.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/chapter-01-story-spine-preview-v2.metadata.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `bridge v2` 现在直接补入了三处导演室结构修正：
  - `P06 -> P07`：用 `P06` 尾部减速桥，把“发现第四路径”先落地
  - `P07 -> P08`：用林澄侧反应位，避免两段 thesis 背靠背硬顶
  - `P09 -> P10`：用余波承接卡，让公共程序更像后果而不是模块切换
- 当前主 HTML 已切到 `v2` 预览入口，不再继续把 `v1` 当最新判断
- 当前仍保持同一口径：
  - `story-first preview`
  - `not accepted current`
  - `用于判断 P07-P09 是否值得正式纳入 production scope`

### 当前结论

- [part-07-09-middle-bridge-papercut-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-07-09-middle-bridge-papercut-v2.mp4)：`PASS WITH NOTES`
- [chapter-01-story-spine-preview-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v2.mp4)：`PASS WITH NOTES`
- 当前更准确的导演判断：
  - 这条 `v2` 已经把 chapter-01 从“像预告片一样跳着切”推进到“孩子能顺着因果跟下去”的 story spine
  - 但这种改善当前仍主要发生在 `story-first preview` 层，不等于 `P07-P09` 已完成正式戏剧视频化
- 因此下一步优先级正式收口为：
  - 重开 `P07-P09` 的正式 shot contract
  - 再推进 `P07-P09` 从 bridge preview 到正式 clip 的升级路线
  - 不再继续把主要资源先砸在 `P10/P11` 的单镜头抛光上

## Version `v0.71`

- 日期：`2026-03-31`
- 阶段：`P09 正式交付 + chapter story spine v4`
- 目标：把 `P09` 从“还缺冻结质疑与团队分裂”推进成独立可交付 part，并把 `P07/P08/P09` 正式插回整章形成当前最完整的故事观看口径

### 主要产出

- [shot-ch01-p09-s03-evidence-freeze-intervention-v2-qwen-image-max.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p09-s03-evidence-freeze-intervention-v2-qwen-image-max.png)
- [shot-ch01-p09-s03-evidence-freeze-intervention-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p09-s03-evidence-freeze-intervention-viduq3-i2v-v1.mp4)
- [shot-ch01-p09-s05-team-split-viduq3-i2v-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p09-s05-team-split-viduq3-i2v-v1.mp4)
- [render_chapter01_part9_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part9_delivery.sh)
- [part-09-evidence-freeze-team-split-delivery-v1.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-09-evidence-freeze-team-split-delivery-v1.mp4)
- [chapter-01-story-spine-preview-v4.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v4.mp4)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `E15` 已从“最痛但一直空着的制度动作位”推进成真实 speaking clip：
  - `5.04s`
  - `880x588`
  - `24fps`
  - 抽帧差异明确，不是静图假视频
- `E17` 已从 `PASS WITH NOTES` 首帧推进成真实团队分裂 clip：
  - 三人同框压力与第一人称压近已经成立
  - 当前 notes 收缩到动作还可更克制，而不是“有没有这镜”
- `P09` 现在已正式形成独立 part-level delivery：
  - `授权诱惑 -> 顺滑错觉 -> 07 冻结质疑 -> 系统冻结 -> 团队第一次真实分裂`
  - 因此 `P09` 已可进入 `accepted_with_notes`
- `chapter-01 story spine preview` 已升级到 `v4`：
  - 不再只是把 `P07-P09 bridge` 塞回整章
  - 而是直接把 `P07 / P08 / P09` 正式交付段插回 chapter
  - 当前已成为最接近“完整第 1 集故事流畅视频”的章节级预览口径
- loop 主线也已同步切换：
  - `P09 -> accepted_with_notes`
  - 下一条 active part 重新锁到 `P06`
  - 原因不是中段继续缺故事，而是用户明确要求优先清理最高优先假视频债务

## Version `v0.72`

- 日期：`2026-03-31`
- 阶段：`人物一致性 identity-lock v2`
- 目标：把“人物一致性出问题了”从抽象提醒收口成一条真实可复用的 production 路线，并验证它比“单首帧硬顶 + 事后考虑换脸”更适合作为主线

### 主要产出

- [shot-ch01-p11-s02-lin-final-speech-endframe-v2.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p11-s02-lin-final-speech-endframe-v2.png)
- [shot-ch01-p08-s03-sequence-officer-stance-endframe-v2.png](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p08-s03-sequence-officer-stance-endframe-v2.png)
- [shot-ch01-p04-s04-father-close-endframe-v2.jpg](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p04-s04-father-close-endframe-v2.jpg)
- [shot-ch01-p04-s05-lin-close-endframe-v2.jpg](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/shots/shot-ch01-p04-s05-lin-close-endframe-v2.jpg)
- [shot-ch01-p11-s02-lin-final-speech-viduq3-s2v-v2.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p11-s02-lin-final-speech-viduq3-s2v-v2.json)
- [shot-ch01-p04-s04-father-close-viduq3-s2v-v2.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p04-s04-father-close-viduq3-s2v-v2.json)
- [shot-ch01-p04-s05-lin-close-viduq3-s2v-v2.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p04-s05-lin-close-viduq3-s2v-v2.json)
- [shot-ch01-p08-s03-sequence-officer-stance-viduq3-s2v-v2.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p08-s03-sequence-officer-stance-viduq3-s2v-v2.json)
- [shot-ch01-p11-s02-lin-final-speech-viduq3-s2v-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p11-s02-lin-final-speech-viduq3-s2v-v2.mp4)
- [shot-ch01-p11-s02-lin-final-speech-viduq3-s2v-v2.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p11-s02-lin-final-speech-viduq3-s2v-v2.metadata.json)
- [shot-ch01-p04-s05-lin-close-viduq3-s2v-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p04-s05-lin-close-viduq3-s2v-v2.mp4)
- [shot-ch01-p04-s05-lin-close-viduq3-s2v-v2.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/shot-ch01-p04-s05-lin-close-viduq3-s2v-v2.metadata.json)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [flow-vertical-slice-pack.md](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/flow-vertical-slice-pack.md)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- 4 条身份敏感镜头请求模板都已补成统一口径：
  - `横版 start frame`
  - `横版 end frame`
  - `canonical actor portrait`
  - `start-end2video`
- 这次不再把“同一张首帧硬顶全程稳定”当默认方案，也不把“之后看看能不能换脸”当第一补救动作
- `P11 / G02` 已拿到一条真实 `identity-lock v2` 探针：
  - `4.04s`
  - `880x588`
  - `24fps`
  - `AAC`
  - `0s / 1s / 2s / 3s` 抽帧均不同，不是静图晃动假视频
- `P04 / S05` 也已拿到第二条真实 `identity-lock v2` 探针：
  - `3.04s`
  - `964x536`
  - `24fps`
  - `AAC`
  - `0s / 0.8s / 1.6s / 2.4s` 抽帧均不同，不是静图晃动假视频
- 当前更准确的 production judgement 是：
  - `FACE_SWAP_CANDIDATE` 依旧只保留为补救分支
  - 在仓库内没有稳定换脸产线前，最省 token 的主线仍是更强的首尾帧与演员参考控制
  - 这条主线现在已经至少在 `P11` 和 `P04` 两个不同场景的林澄近景上重复走通，不再只是单次偶发成功

### 当前结论

- [shot-ch01-p11-s02-lin-final-speech-viduq3-s2v-v2.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p11-s02-lin-final-speech-viduq3-s2v-v2.mp4)：`PASS WITH NOTES`
- 当前它的定位不是“立刻替换 `P11 current`”，而是：
  - 作为 `G02` 的更强身份稳定升级候选
  - 作为 `P04/P08/P11` 同类近景的统一模板基线
  - 作为后续减少换脸冲动、减少无效重跑的默认路线
- loop 主线继续保持：
  - `active part = P12`
  - 先处理尾声 `voice-first clean plate` 的视频化升级，不让 `P11` backlog 重新抢主线

## Version `v0.86`

- 日期：`2026-04-03`
- 阶段：`P01 S07 story-clarity rescue`
- 目标：把 `P01 / S07` 从“route-only 启航空镜 + 解释字卡”推进到真实可看的 current clip，并且同步落到 `part -> story spine -> master -> HTML`

### 主要产出

- [shot-ch01-p01-s07-team-launch-bridge-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s07-team-launch-bridge-v3.mp4)
- [part-01-future-bay-task-dock-delivery-v27.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v27.mp4)
- [chapter-01-story-spine-preview-v35-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v35-full.mp4)
- [chapter-01-vertical-slice-master-v31-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v31-current.mp4)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)
- [shot-ch01-p01-s07-team-launch-start-v1-qwen-chat-anchor.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/openai-images/shot-ch01-p01-s07-team-launch-start-v1-qwen-chat-anchor.json)
- [shot-ch01-p01-s07-team-launch-viduq3-s2v-v1.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/api-requests/qingyun-vidu/shot-ch01-p01-s07-team-launch-viduq3-s2v-v1.json)

### 核心变化

- 先按 hard rules 做了 `trim / bridge / same-space upgrade`，没有继续拿单条空镜硬说“全队已经出发”
- `S07` 当前已换成真实 bridge clip：
  - 前半用 `S04` 的真实多人同场视频交代“队友已经一起接上任务”
  - 后半接入裁掉伪文字的启航航线镜头
  - 全段现在属于真实视频，不再靠大段说明字卡承担主要叙事
- `P01` 已升级到 `delivery v27`
- `story spine current` 已切到 `v35-full`
- `chapter master current` 已切到 `v31-current`
- HTML 总览页已回写成这轮真实状态，并统一更新了 cache-busting 参数

### 当前结论

- [shot-ch01-p01-s07-team-launch-bridge-v3.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/shot-ch01-p01-s07-team-launch-bridge-v3.mp4)：`PASS WITH NOTES`
- 当前 `S07` 的准确定位不是“已经拿到理想单镜完片”，而是：
  - 一个已经落到 current 的 `team-launch bridge rescue`
  - 它比原先的 route-only 空镜更诚实，也更能让第一次看片的人看懂“不是一个人出发”
  - 但后续仍值得评估是否重生一条真正单镜成立的“队伍集结并启航”新 clip

## Version `v0.87`

- 日期：`2026-04-03`
- 阶段：`P01 S06 teammate-duty onboarding pass`
- 目标：把“整队介绍”从导演文档真正落到 current clip，并同步贯通 `part -> story spine -> master -> HTML`

### 主要产出

- [part-01-future-bay-task-dock-delivery-v28.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v28.mp4)
- [chapter-01-story-spine-preview-v36-full.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-story-spine-preview-v36-full.mp4)
- [chapter-01-vertical-slice-master-v32-current.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/chapter-01-vertical-slice-master-v32-current.mp4)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [video-loop-state.json](/Users/wujames/Desktop/AI未来通识课（K12）/content/chapters/chapter-01-time-archive-city/production/video-loop-state.json)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `S06` 不再只负责解释林澄的处境，后半已补入一层很短的 `同行成员职责`：
  - `祁野` 查 `93%` 判定
  - `闻夏` 抢公开窗口
  - `回响` 整理证据
  - `阿潮` 带队启航
  - `我` 做最后判断
- `P01` 已升级到 `delivery v28`
- `story spine current` 已切到 `v36-full`
- `chapter master current` 已切到 `v32-current`
- HTML 总览页已同步回写这轮真实变化，并更新了 `part / spine / S06 / S07` 的 cache-busting 参数

### 当前结论

- 这一轮不是理想终版的“原生团队介绍镜头”，而是一次更诚实的 current 升级：
  - 让第一次看片的人在出发前，至少先知道谁和我一起去、各自负责什么
  - 再由已经落地的 `S07 team-launch bridge` 把这层介绍兑现成“固定小队已经一起动身”
- 后续如果继续升格 `P01`，优先方向不是再加长解释字，而是把这层职责介绍从 overlay 继续升级成更原生的视频内动作

## Version `v0.88`

- 日期：`2026-04-03`
- 阶段：`P01 repeat cleanup + squad intro handoff fix`
- 目标：修掉 `P01` 在 `23-24s` 左右的重复感，并把固定小队介绍稳定落到真正可见的 `S07` 队伍镜头里

### 主要产出

- [part-01-future-bay-task-dock-delivery-v30.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v30.mp4)
- [part-01-future-bay-task-dock-delivery-v30.metadata.json](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/metadata/videos/part-01-future-bay-task-dock-delivery-v30.metadata.json)
- [render_chapter01_part1_delivery.sh](/Users/wujames/Desktop/AI未来通识课（K12）/scripts/production/render_chapter01_part1_delivery.sh)
- [chapter-01-main-character-dossier.html](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/chapter-01-main-character-dossier.html)

### 核心变化

- `S06` 不再在尾段提前重复整队职责，只负责把林澄为什么拒签讲清
- `S07` 现在明确承担固定小队介绍：
  - `祁野` 查系统判定
  - `闻夏` 抢公开窗口
  - `回响` 整理证据
  - `阿潮` 带队启航
  - `我` 做最后判断
- 这轮顺手清掉了会泄露制作过程的内部说明文案，确保 `P01 current` 保持用户可见文案口径
- `P01 current` 已切到 `delivery v30`
- HTML 主资产页已同步回写 `P01 current` 的版本、时长与本轮修正说明

### 当前结论

- [part-01-future-bay-task-dock-delivery-v30.mp4](/Users/wujames/Desktop/AI未来通识课（K12）/outputs/2026-03-22-chapter-01-dashscope-character-lock/videos/part-01-future-bay-task-dock-delivery-v30.mp4)：`PASS WITH NOTES`
- 当前这轮已经解决的不是“画面好不好看”层面，而是更基础的 `story handoff`：
  - `S06` 结束在林澄的拒签理由
  - `S07` 再进入小队成员与职责
  - 所以 `23-24s` 不再像把同一层信息重复播两次
- 后续如果还要继续升格 `P01`，优先方向仍是把 `S07` 的职责介绍继续从 overlay 升成更原生的队内动作与镜头表演
