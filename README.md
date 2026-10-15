# Awesome World Models

世界模型与具身智能论文阅读清单，围绕 **State、Action、Reward / Value、Integration** 四个视角，整理状态表征、动作条件预测、任务评价、规划与策略学习相关工作。

本清单收录 **142 条文献**，包含论文、综述、理论研究、评测基准与官方研究介绍。保留英文标题与原始链接，使用中文概括研究内容和核心方法。

## Contents

- [阅读说明](#reading-guide)
- [Surveys & Perspectives · 综述与观点](#surveys)
- [Foundations · 基础工作](#foundations)
- [State · 状态表征与预测](#state)
- [Action · 动作与控制](#action)
- [Reward / Value · 奖励与价值](#reward-value)
- [Integration · 系统集成与评测](#integration)
- [来源与整理说明](#sources)
- [Contributing](#contributing)

<a id="reading-guide"></a>
## 阅读说明

每篇文献只收录一次，按来源中首次出现的正文章节组织；条目中的 **讨论视角** 保留跨章节关联。分类用于导航，不表示文章仅属于该方向，也不表示所有条目都是完整的世界模型系统。

| 讨论视角 | 关注的问题 | 来源中涉及的文献数 |
| --- | --- | ---: |
| State | 状态中保留了什么信息，如何预测环境演化？ | 51 |
| Action | 动作如何表示、影响预测并对应实际执行？ | 35 |
| Reward / Value | 如何评价任务进展、预测奖励和估计价值？ | 41 |
| Integration | 预测如何进入规划、策略学习与执行反馈？ | 21 |

上述计数允许同一文献跨视角重复，排除来源中的 Table 2 总览引用；不能相加作为独立文献总数。下文编号沿用来源，便于交叉查找。

方法简介来自所提供文献总表及其综述整理，尚未逐篇独立复核原论文。“稿内未展开”不代表方法没有相应能力；文献出现在某个诊断或失败机制小节，也不等于原论文已实验证实该失败。

<a id="surveys"></a>
## Surveys & Perspectives · 综述与观点

### 综述与研究视角

<a id="paper-1"></a>
**[1] Is Sora a World Simulator?** · 2024 · 综述

[Is Sora a World Simulator? A Comprehensive Survey on General World Models and Beyond](https://arxiv.org/abs/2405.03520)

- **研究内容：** 梳理通用世界模型与视频模拟的发展
- **核心方法 / 输入输出：** 综述文献，不适用模型输入输出
- **讨论视角：** 引言 · 来源章节：§1.1, §1.2

<a id="paper-2"></a>
**[2] Understanding World or Predicting Future?** · 2024 · 综述

[Understanding World or Predicting Future? A Comprehensive Survey of World Models](https://arxiv.org/abs/2411.14499)

- **研究内容：** 从表征与未来预测组织世界模型研究
- **核心方法 / 输入输出：** 综述文献，不适用模型输入输出
- **讨论视角：** 引言 · 来源章节：§1.1, §1.2

<a id="paper-3"></a>
**[3] World Models for Embodied AI** · 2025 · 综述

[A Comprehensive Survey on World Models for Embodied AI](https://arxiv.org/abs/2510.16732)

- **研究内容：** 梳理世界模型在具身智能中的功能
- **核心方法 / 输入输出：** 综述文献，不适用模型输入输出
- **讨论视角：** 引言 · 来源章节：§1.1, §1.2

<a id="paper-4"></a>
**[4] World Model for Robot Learning** · 2026 · 综述

[World Model for Robot Learning: A Comprehensive Survey](https://arxiv.org/abs/2605.00080)

- **研究内容：** 梳理世界模型与机器人策略的联系
- **核心方法 / 输入输出：** 综述文献，不适用模型输入输出
- **讨论视角：** 引言 · 来源章节：§1.1, §1.2

<a id="paper-5"></a>
**[5] 3D and 4D World Modeling** · 2025 · 综述

[3D and 4D World Modeling: A Survey](https://arxiv.org/abs/2509.07996)

- **研究内容：** 梳理空间与时空场景表示
- **核心方法 / 输入输出：** 综述文献，不适用模型输入输出
- **讨论视角：** 引言 · 来源章节：§1.1, §1.2

<a id="paper-6"></a>
**[6] World Action Models: The Next Frontier** · 2026 · 综述/观点

[World Action Models: The Next Frontier in Embodied AI](https://arxiv.org/abs/2605.12090)

- **研究内容：** 讨论世界预测与动作生成的结合
- **核心方法 / 输入输出：** 研究方向综述，不适用单一模型接口
- **讨论视角：** 引言 · 来源章节：§1.1

<a id="paper-7"></a>
**[7] World Action Models: A Survey** · 2026 · 综述

[World Action Models: A Survey](https://arxiv.org/abs/2606.20781)

- **研究内容：** 整理世界动作模型
- **核心方法 / 输入输出：** 综述文献，不适用模型输入输出
- **讨论视角：** 引言 · 来源章节：§1.1, §1.2

<a id="paper-8"></a>
**[8] Latent State Design under Sufficiency Constraints** · 2026 · 理论/观点

[Latent State Design for World Models under Sufficiency Constraints](https://arxiv.org/abs/2605.01694)

- **研究内容：** 讨论潜在状态是否保留智能体所需信息
- **核心方法 / 输入输出：** 状态充分性问题；稿内未展开具体模型
- **讨论视角：** 引言 · 来源章节：§1.1, §1.2

<a id="paper-9"></a>
**[9] Decision-Making-Centric Position** · 2026 · 评测/观点

[How Should World Models Be Evaluated for Embodied Decision- Making? A Decision-Making-Centric Position](https://arxiv.org/abs/2606.15032)

- **研究内容：** 强调世界模型评测应支撑决策能力主张
- **核心方法 / 输入输出：** 评测原则；非单一预测模型
- **讨论视角：** 引言 · 来源章节：§1.1, §1.2

<a id="foundations"></a>
## Foundations · 基础工作

### 基础工作

<a id="paper-10"></a>
**[10] World Models** · 2018 · 世界模型与控制

[World Models](https://arxiv.org/abs/1803.10122)

- **研究内容：** 组合视觉压缩、循环动力学与控制器
- **核心方法 / 输入输出：** 图像/历史 → 潜在状态、时间预测与控制
- **讨论视角：** 背景 · Reward / Value · 来源章节：§2.1, §5.2.1

<a id="paper-11"></a>
**[11] PlaNet** · 2018 · 世界模型与规划

[Learning Latent Dynamics for Planning from Pixels](https://arxiv.org/abs/1811.04551)

- **研究内容：** 从图像学习潜在动力学并在线规划
- **核心方法 / 输入输出：** 图像历史、候选动作 → 潜在轨迹与奖励
- **讨论视角：** 背景 · Reward / Value · Integration · 来源章节：§2.1, §5.1.2, §6.1.1

<a id="paper-12"></a>
**[12] Dreamer** · 2019 · 世界模型与策略学习

[Dream to Control: Learning Behaviors by Latent Imagination](https://arxiv.org/abs/1912.01603)

- **研究内容：** 在潜在想象中学习行为
- **核心方法 / 输入输出：** 观测、动作 → 潜在轨迹、观测/奖励；另学策略和价值
- **讨论视角：** 背景 · Reward / Value · Integration · 来源章节：§2.1, §5.1.2, §5.1.3, §6.1.2

<a id="paper-13"></a>
**[13] MuZero** · 2019 · 世界模型与搜索

[Mastering Atari, Go, Chess and Shogi by Planning with a Learned Model](https://arxiv.org/abs/1911.08265)

- **研究内容：** 学习搜索需要的量而不重建完整观测
- **核心方法 / 输入输出：** 历史、候选动作 → 潜在转移、奖励、价值与策略预测
- **讨论视角：** 背景 · Reward / Value · 来源章节：§2.1, §5.1.3, §5.1.4

<a id="state"></a>
## State · 状态表征与预测

### 空间环境建模

<a id="paper-26"></a>
**[26] Pathdreamer** · 2021 · 空间世界模型

[Pathdreamer: A World Model for Indoor Navigation](https://arxiv.org/abs/2105.08756)

- **研究内容：** 用历史三维信息补全查询视点的场景
- **核心方法 / 输入输出：** 历史观测、目标视点 → 视点相关场景内容
- **讨论视角：** State · 来源章节：§3.1.1

<a id="paper-27"></a>
**[27] GSN** · 2021 · 空间场景生成

[Unconstrained Scene Generation with Locally Conditioned Radiance Fields](https://arxiv.org/abs/2104.00670)

- **研究内容：** 用局部潜在布局与辐射场生成可渲染场景
- **核心方法 / 输入输出：** 局部潜变量/稀疏观测、视点 → 场景及新视图
- **讨论视角：** State · 来源章节：§3.1.1

<a id="paper-28"></a>
**[28] SE3DS** · 2022 · 空间场景生成

[Simple and Effective Synthesis of Indoor 3D Scenes](https://arxiv.org/abs/2204.02960)

- **研究内容：** 组合点云重投影与 RGB-D 补全扩展场景
- **核心方法 / 输入输出：** 已有 RGB-D、查询视点 → 新 RGB-D 与扩展场景
- **讨论视角：** State · 来源章节：§3.1.1, §3.2.2, §3.2.3

<a id="paper-29"></a>
**[29] SceneDreamer** · 2023 · 空间场景生成

[SceneDreamer: Unbounded 3D Scene Generation from 2D Image Collections](https://arxiv.org/abs/2302.01330)

- **研究内容：** 用高度场和语义布局生成无界三维景观
- **核心方法 / 输入输出：** 二维图像集合用于学习 → 可渲染三维景观
- **讨论视角：** State · 来源章节：§3.1.1, §3.2.1

<a id="paper-30"></a>
**[30] WonderJourney** · 2023 · 空间场景扩展

[WonderJourney: Going from Anywhere to Everywhere](https://arxiv.org/abs/2312.03884)

- **研究内容：** 以语义、深度与投影连接连续生成场景
- **核心方法 / 输入输出：** 初始场景/语义 → 连续场景视图
- **讨论视角：** State · 来源章节：§3.1.1

<a id="paper-31"></a>
**[31] WonderWorld** · 2024 · 空间场景生成

[WonderWorld: Interactive 3D Scene Generation from a Single Image](https://arxiv.org/abs/2406.09394)

- **研究内容：** 从单图构造和扩展交互浏览的三维场景
- **核心方法 / 输入输出：** 单张图像 → 可交互浏览三维场景
- **讨论视角：** State · 来源章节：§3.1.1

<a id="paper-32"></a>
**[32] WorldMem** · 2025 · 带记忆的世界模拟

[WorldMem: Long-term Consistent World Simulation with Memory](https://arxiv.org/abs/2504.12369)

- **研究内容：** 按位姿和时间检索历史帧以保持重访一致性
- **核心方法 / 输入输出：** 帧历史、位姿、时间 → 一致场景模拟
- **讨论视角：** State · 来源章节：§3.1.1, §3.2.2, §3.2.3

### 几何、语义与状态构建

<a id="paper-33"></a>
**[33] StereoScene / BRGScene** · 2023 · 几何感知

[Bridging Stereo Geometry and BEV Representation with Reliable Mutual Interaction for Semantic Scene Completion](https://arxiv.org/abs/2303.13959)

- **研究内容：** 融合双目几何与 BEV 语义补全场景
- **核心方法 / 输入输出：** 双目图像 → 语义场景占据
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-34"></a>
**[34] VPD** · 2023 · 几何感知

[One at a Time: Progressive Multi-step Volumetric Probability Learning for Reliable 3D Scene Perception](https://arxiv.org/abs/2306.12681)

- **研究内容：** 逐步细化体素概率以改善三维感知
- **核心方法 / 输入输出：** 观测 → 渐进细化的体积概率/三维场景
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-35"></a>
**[35] HTCL** · 2024 · 几何感知

[Hierarchical Temporal Context Learning for Camera-based Semantic Scene Completion](https://arxiv.org/abs/2407.02077)

- **研究内容：** 对齐跨帧上下文以恢复场景几何
- **核心方法 / 输入输出：** 多帧相机观测 → 语义场景补全
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-36"></a>
**[36] Hi-SOP** · 2024 · 几何感知

[Hierarchical Context Alignment with Disentangled Geometric and Temporal Modeling for Semantic Occupancy Prediction](https://arxiv.org/abs/2412.08243)

- **研究内容：** 分开几何与时间对齐以改善占据预测
- **核心方法 / 输入输出：** 观测、深度置信度、相机位姿 → 语义占据
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-37"></a>
**[37] Robust Scale-Aware Stereo Matching** · 2021 · 几何感知

[Robust Scale-Aware Stereo Matching Network](https://ieeexplore.ieee.org/document/9547779/)

- **研究内容：** 融合多尺度视差估计
- **核心方法 / 输入输出：** 双目图像 → 视差
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-38"></a>
**[38] StereoDiffuer** · 2026 · 几何感知

[StereoDiffuer: Diffusion-based Progressive Geometry Modeling with Saliency Attention Perception for Stereo Matching](https://arxiv.org/abs/2608.21710)

- **研究内容：** 用显著性与置信度逐步修正边界和细结构视差
- **核心方法 / 输入输出：** 双目图像 → 视差/几何
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-39"></a>
**[39] Hybrid-depth** · 2025 · 几何感知

[Hybrid-grained Feature Aggregation with Coarse-to-fine Language Guidance for Self-supervised Monocular Depth Estimation](https://arxiv.org/abs/2510.09320)

- **研究内容：** 结合语义与局部空间特征估计深度
- **核心方法 / 输入输出：** 单目图像、语言引导 → 深度
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-40"></a>
**[40] Light of Normals** · 2025 · 几何感知

[Light of Normals: Unified Feature Representation for Universal Photometric Stereo](https://arxiv.org/abs/2506.18882)

- **研究内容：** 分离光照因素并保留表面法线细节
- **核心方法 / 输入输出：** 光度立体观测 → 表面法线
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-41"></a>
**[41] DKT** · 2025 · 几何感知

[Diffusion Knows Transparency: Repurposing Video Diffusion for Transparent Object Depth and Normal Estimation](https://arxiv.org/abs/2512.23705)

- **研究内容：** 以视频扩散恢复透明/反光物体深度和法线
- **核心方法 / 输入输出：** 视频观测 → 时间一致的深度与法线
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-42"></a>
**[42] NaviNeRF** · 2023 · 表征/三维重建

[NaviNeRF: NeRF-based 3D Representation Disentanglement by Latent Semantic Navigation](https://arxiv.org/abs/2304.11342)

- **研究内容：** 在生成辐射场中寻找可解释潜在因素
- **核心方法 / 输入输出：** 辐射场潜变量 → 可解释方向与三维渲染
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-43"></a>
**[43] NaviNeRF++** · 2025 · 表征/三维重建

[NaviNeRF++: Towards Interpretable 3D Reconstruction via Unsupervised Disentangled Representation Learning](https://doi.org/10.1109/TPAMI.2025.3601145)

- **研究内容：** 结合感知解耦与语言识别解释三维因素
- **核心方法 / 输入输出：** 三维表示 → 解耦且可命名的因素
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-44"></a>
**[44] CL-Dis** · 2024 · 表征学习

[Closed-Loop Unsupervised Representation Disentanglement withβ-VAE Distillation and Diffusion Probabilistic Feedback](https://arxiv.org/abs/2402.02346)

- **研究内容：** 用 VAE 蒸馏和扩散反馈改进无监督解耦
- **核心方法 / 输入输出：** 视觉表征 → 解耦潜变量
- **讨论视角：** State · 来源章节：§3.1.2

<a id="paper-45"></a>
**[45] LangSurf** · 2024 · 三维场景理解

[LangSurf: Language-Embedded Surface Gaussians for 3D Scene Understanding](https://arxiv.org/abs/2412.17635)

- **研究内容：** 把语言特征准确落到物体表面
- **核心方法 / 输入输出：** 视觉/语言特征 → 带语言信息的表面高斯表示
- **讨论视角：** State · 来源章节：§3.1.2

### 占据表示与度量几何

<a id="paper-18"></a>
**[18] UniScene** · 2024 · 场景生成平台

[UniScene: Unified Occupancy-centric Driving Scene Generation](https://arxiv.org/abs/2412.05435)

- **研究内容：** 用共享 occupancy 约束视频与 LiDAR 场景一致
- **核心方法 / 输入输出：** 场景布局 → 语义占据 → 视频与 LiDAR
- **讨论视角：** State · 来源章节：§3.1.3

<a id="paper-19"></a>
**[19] UniScenev2** · 2025 · 数据集与场景生成

[Scaling Up Occupancy-centric Driving Scene Generation: Dataset and Method](https://arxiv.org/abs/2510.22973)

- **研究内容：** 扩展占据生成的空间覆盖、时间预测与传感器建模
- **核心方法 / 输入输出：** 占据/点图条件 → 扩展场景、预测与传感器数据
- **讨论视角：** State · 来源章节：§3.1.3

<a id="paper-20"></a>
**[20] OccScene** · 2024 · 感知与场景生成

[OccScene: Semantic Occupancy-based Cross-task Mutual Learning for 3D Scene Generation](https://arxiv.org/abs/2412.11183)

- **研究内容：** 让 occupancy 感知与扩散生成相互学习
- **核心方法 / 输入输出：** 场景信息 → 语义占据与生成场景；双向对齐
- **讨论视角：** State · 来源章节：§3.1.3

<a id="paper-46"></a>
**[46] DiST-4D** · 2025 · 四维场景生成

[DiST-4D: Disentangled Spatiotemporal Diffusion with Metric Depth for 4D Driving Scene Generation](https://arxiv.org/abs/2503.15208)

- **研究内容：** 用度量深度连接时间预测与新视点合成
- **核心方法 / 输入输出：** 场景观测、度量深度/视点 → 时空场景生成
- **讨论视角：** State · 来源章节：§3.1.3

<a id="paper-47"></a>
**[47] MuDG** · 2025 · 三维场景重建

[MuDG: Taming Multi-modal Diffusion with Gaussian Splatting for Urban Scene Reconstruction](https://arxiv.org/abs/2503.10604)

- **研究内容：** 融合 LiDAR 与视觉几何先验改善偏离采集轨迹的重建
- **核心方法 / 输入输出：** LiDAR、视觉先验 → Gaussian 场景与新视图
- **讨论视角：** State · 来源章节：§3.1.3

<a id="paper-48"></a>
**[48] Appearance Codes + Bilateral Grids** · 2025 · 三维场景重建

[Unifying Appearance Codes and Bilateral Grids for Driving Scene Gaussian Splatting](https://arxiv.org/abs/2506.05280)

- **研究内容：** 用外观码与局部颜色校正减少光度不一致伪影
- **核心方法 / 输入输出：** 驾驶场景观测 → Gaussian 重建与渲染
- **讨论视角：** State · 来源章节：§3.1.3

### 时序演化预测

<a id="paper-16"></a>
**[16] DINO-WM** · 2024 · 特征世界模型

[DINO-WM: World Models on Pre-trained Visual Features enable Zeroshot Planning](https://arxiv.org/abs/2411.04983)

- **研究内容：** 在冻结的 DINOv2 空间特征上学习动态与规划
- **核心方法 / 输入输出：** 图像历史、动作 → 未来空间 patch 特征
- **讨论视角：** State · Reward / Value · 来源章节：§3.1.4, §3.1.5, §5.2.1

<a id="paper-49"></a>
**[49] VideoGPT** · 2021 · 视频生成

[VideoGPT: Video Generation using VQ-VAE and Transformers](https://arxiv.org/abs/2104.10157)

- **研究内容：** 压缩时空视频 token 并自回归建模
- **核心方法 / 输入输出：** 视频 → 离散时空潜变量 → 生成视频
- **讨论视角：** State · 来源章节：§3.1.4

<a id="paper-50"></a>
**[50] TECO** · 2022 · 视频预测

[Temporally Consistent Transformers for Video Generation](https://arxiv.org/abs/2210.02396)

- **研究内容：** 用紧凑潜在动态保留更长历史
- **核心方法 / 输入输出：** 视频历史 → 后续视频/潜在动态
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.3

<a id="paper-51"></a>
**[51] Sora 官方研究介绍** · 2024 · 官方研究报告

[Video generation models as world simulators](https://openai.com/index/video-generation-models-as-world-simulators/)

- **研究内容：** 展示时空 patch 视频生成及定性能力和限制
- **核心方法 / 输入输出：** 生成条件 → 视频；稿内未展开完整接口
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.2

<a id="paper-52"></a>
**[52] Cosmos** · 2025 · 基础模型平台

[Cosmos World Foundation Model Platform for Physical AI](https://arxiv.org/abs/2501.03575)

- **研究内容：** 提供视觉 tokenizer 与视频预测等组件
- **核心方法 / 输入输出：** 视觉/生成条件 → 视频表示与预测
- **讨论视角：** State · 来源章节：§3.1.4

<a id="paper-53"></a>
**[53] Drive-WM** · 2023 · 驾驶视频模型与规划

[Driving into the Future: Multiview Visual Forecasting and Planning with World Model for Autonomous Driving](https://arxiv.org/abs/2311.17918)

- **研究内容：** 联合时间和视点建模并用未来评分支持规划
- **核心方法 / 输入输出：** 驾驶观测与候选未来条件 → 多视点视频及规划评分
- **讨论视角：** State · Reward / Value · 来源章节：§3.1.4, §3.2.2, §5.1.2

<a id="paper-54"></a>
**[54] DrivingWorld** · 2024 · 驾驶视频模型

[DrivingWorld: Constructing World Model for Autonomous Driving via Video GPT](https://arxiv.org/abs/2412.19505)

- **研究内容：** 分离帧间时间建模与帧内 token 处理
- **核心方法 / 输入输出：** 驾驶视频历史 → 长序列预测
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.3

<a id="paper-55"></a>
**[55] iVideoGPT** · 2024 · 交互视频世界模型

[iVideoGPT: Interactive VideoGPTs are Scalable World Models](https://arxiv.org/abs/2405.15223)

- **研究内容：** 用上下文压缩分开静态场景与后续变化
- **核心方法 / 输入输出：** 视觉历史、交互条件 → 后续视频 token
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.1

<a id="paper-56"></a>
**[56] IRIS** · 2022 · 视频世界模型与策略

[Transformers are Sample-Efficient World Models](https://arxiv.org/abs/2209.00588)

- **研究内容：** 用自回归 Transformer 预测离散视觉 token
- **核心方法 / 输入输出：** 视觉 token/交互历史 → 未来视觉 token
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.1

<a id="paper-57"></a>
**[57] DIAMOND** · 2024 · 视频世界模型与策略

[Diffusion for World Modeling: Visual Details Matter in Atari](https://arxiv.org/abs/2405.12399)

- **研究内容：** 用扩散预测视觉观测，关注细节与递归稳定性
- **核心方法 / 输入输出：** 交互观测历史 → 未来视觉观测
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.3

<a id="paper-58"></a>
**[58] LeWorldModel / LeWM** · 2026 · 特征世界模型

[LeWorldModel: Stable End-to-End Joint-Embedding Predictive Architecture from Pixels](https://arxiv.org/abs/2603.19312)

- **研究内容：** 联合训练视觉编码器与预测器，以正则避免塌缩
- **核心方法 / 输入输出：** 图像历史 H、动作 a → 下一状态特征；不以像素重建为核心
- **讨论视角：** State · 来源章节：§3.1.4, §3.1.5, §3.2.1

<a id="paper-59"></a>
**[59] Copilot4D** · 2023 · 结构化世界模型

[Copilot4D: Learning Unsupervised World Models for Autonomous Driving via Discrete Diffusion](https://arxiv.org/abs/2311.01017)

- **研究内容：** 对 LiDAR 离散表示做时空扩散以预测点云
- **核心方法 / 输入输出：** LiDAR 观测历史 → 未来点云
- **讨论视角：** State · 来源章节：§3.1.4

<a id="paper-60"></a>
**[60] OccWorld** · 2023 · 结构化世界模型

[OccWorld: Learning a 3D Occupancy World Model for Autonomous Driving](https://arxiv.org/abs/2311.16038)

- **研究内容：** 以三维占据 token 联合预测场景和自车轨迹
- **核心方法 / 输入输出：** 语义占据历史 → 未来占据＋自车轨迹
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.1

<a id="paper-61"></a>
**[61] C-SWM** · 2019 · 对象世界模型

[Contrastive Learning of Structured World Models](https://arxiv.org/abs/1911.12247)

- **研究内容：** 以对象潜在状态和关系图建模转移
- **核心方法 / 输入输出：** 视觉对象状态 → 关系图上的状态转移
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.1, §3.2.2

<a id="paper-62"></a>
**[62] SlotFormer** · 2022 · 对象动态模型

[SlotFormer: Unsupervised Visual Dynamics Simulation with Object-Centric Models](https://arxiv.org/abs/2210.05861)

- **研究内容：** 预测时间对齐的对象 slot 及其关系变化
- **核心方法 / 输入输出：** 对象 slot 历史 → 未来对象 slot
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.3

<a id="paper-63"></a>
**[63] GNS** · 2020 · 粒子物理模拟器

[Learning to Simulate Complex Physics with Graph Networks](https://arxiv.org/abs/2002.09405)

- **研究内容：** 以粒子邻域图和消息传递学习物理状态更新
- **核心方法 / 输入输出：** 粒子历史/材料信息等 → 粒子状态更新
- **讨论视角：** State · 来源章节：§3.1.4, §3.2.2, §3.2.3

### 特征空间预测

<a id="paper-17"></a>
**[17] V-JEPA 2** · 2025 · 表征学习与世界模型

[V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning](https://arxiv.org/abs/2506.09985)

- **研究内容：** 分开无动作视频预训练和动作条件规划适配
- **核心方法 / 输入输出：** 视频 → 特征；适配模型以动作预测未来特征
- **讨论视角：** State · Reward / Value · 来源章节：§3.1.5, §5.2.1

<a id="paper-64"></a>
**[64] V-JEPA** · 2024 · 视频表征学习

[Revisiting Feature Prediction for Learning Visual Representations from Video](https://arxiv.org/abs/2404.08471)

- **研究内容：** 通过预测遮挡区域特征学习视频表示
- **核心方法 / 输入输出：** 可见视频上下文 → 被遮挡目标特征
- **讨论视角：** State · 来源章节：§3.1.5

<a id="paper-65"></a>
**[65] V-JEPA 2.1** · 2026 · 视频表征学习

[V-JEPA 2.1: Unlocking Dense Features in Video Self-Supervised Learning](https://arxiv.org/abs/2603.14482)

- **研究内容：** 加强密集特征和中间层预测监督
- **核心方法 / 输入输出：** 视频 → 密集视觉特征
- **讨论视角：** State · 来源章节：§3.1.5

### 信息丢失与状态混叠

<a id="paper-66"></a>
**[66] Denoised MDPs** · 2022 · 任务相关表征

[Denoised MDPs: Learning World Models Better Than the World Itself](https://arxiv.org/abs/2206.15477)

- **研究内容：** 按可控性与奖励相关性分解潜在因素
- **核心方法 / 输入输出：** 交互数据 → 分离可控/奖励相关因素的潜在状态
- **讨论视角：** State · Reward / Value · 来源章节：§3.2.1, §5.2.1, §5.2.3

### 结构与物理一致性

<a id="paper-67"></a>
**[67] Physical Law Perspective** · 2024 · 诊断/评测研究

[How Far is Video Generation from World Model: A Physical Law Perspective](https://arxiv.org/abs/2411.02385)

- **研究内容：** 区分分布内、参数外推与组合物理泛化
- **核心方法 / 输入输出：** 受控运动/碰撞场景 → 视频模型物理评测
- **讨论视角：** State · 来源章节：§3.2.2

### 长时预测与历史记忆

<a id="paper-68"></a>
**[68] Lipschitz Continuity in MBRL** · 2018 · 理论

[Lipschitz continuity in model-based reinforcement learning](https://proceedings.mlr.press/v80/asadi18a.html)

- **研究内容：** 分析动力学敏感度与多步预测误差传播
- **核心方法 / 输入输出：** 模型误差与连续性假设 → 误差界
- **讨论视角：** State · 来源章节：§3.2.3

### 诊断与评测

<a id="paper-69"></a>
**[69] Stability Under Scrutiny** · 2025 · 基准/诊断研究

[Stability Under Scrutiny: Benchmarking Representation Paradigms for Online HD Mapping](https://arxiv.org/abs/2510.10660)

- **研究内容：** 分别测在线地图的存在、定位与形状稳定性
- **核心方法 / 输入输出：** 在线地图预测 → 时间稳定性评测
- **讨论视角：** State · 来源章节：§3.3

<a id="paper-70"></a>
**[70] TAPTRv2** · 2024 · 跟踪/诊断工具

[TAPTRv2: Attention-based Position Update Improves Tracking Any Point](https://arxiv.org/abs/2407.16291)

- **研究内容：** 分离位置更新与内容表示以跟踪点
- **核心方法 / 输入输出：** 视频、查询点 → 点轨迹
- **讨论视角：** State · 来源章节：§3.3

<a id="paper-71"></a>
**[71] Imagined Rollouts are Kinematic, Not Dynamic** · 2026 · 诊断研究

[Imagined Rollouts are Kinematic, Not Dynamic: A Diagnosis of Long-Horizon World-Model Failure](https://arxiv.org/abs/2607.05966)

- **研究内容：** 以运动学一致性与摩擦干预诊断特定 DreamerV3
- **核心方法 / 输入输出：** 指定 checkpoint 的 walker-walk rollout → 动力学诊断
- **讨论视角：** State · 来源章节：§3.3

<a id="action"></a>
## Action · 动作与控制

### 动作表示与控制适配

<a id="paper-72"></a>
**[72] Playable Video Generation** · 2021 · 潜在动作视频模型

[Playable Video Generation](https://arxiv.org/abs/2101.12195)

- **研究内容：** 从重建中学可由用户选择的离散控制
- **核心方法 / 输入输出：** 视频 → 潜在动作；潜在控制 → 后续帧
- **讨论视角：** Action · 来源章节：§4.1.1

<a id="paper-73"></a>
**[73] Genie** · 2024 · 潜在动作世界模型

[Genie: Generative Interactive Environments](https://arxiv.org/abs/2402.15391)

- **研究内容：** 从无动作标注视频学习交互环境
- **核心方法 / 输入输出：** 视频 → tokenizer/潜在动作；控制 → 后续帧
- **讨论视角：** Action · 来源章节：§4.1.1, §4.2.2

<a id="paper-74"></a>
**[74] Latent Action World Models in the Wild** · 2026 · 潜在动作世界模型

[Learning Latent Action World Models In The Wild](https://arxiv.org/abs/2601.05230)

- **研究内容：** 从异质真实视频学习受约束的连续潜在动作
- **核心方法 / 输入输出：** 视频变化 → 连续潜在动作与预测
- **讨论视角：** Action · 来源章节：§4.1.1

<a id="paper-75"></a>
**[75] Olaf-World** · 2026 · 潜在动作世界模型

[Olaf- World: Orienting Latent Actions for Video World Modeling](https://arxiv.org/abs/2602.10104)

- **研究内容：** 用冻结视频特征差约束跨情境动作语义
- **核心方法 / 输入输出：** 视觉转移/视频特征差 → 对齐的潜在动作
- **讨论视角：** Action · 来源章节：§4.1.1, §4.2.1

<a id="paper-76"></a>
**[76] MuCoLA** · 2026 · 潜在动作学习

[Multi-view consistent latent action learning for world modeling and control](https://proceedings.mlr.press/v306/wan26f.html)

- **研究内容：** 用同步多视点自蒸馏减少视角影响
- **核心方法 / 输入输出：** 同步多视点视频 → 一致潜在动作
- **讨论视角：** Action · 来源章节：§4.1.1, §4.2.1

<a id="paper-77"></a>
**[77] AdaWorld** · 2025 · 潜在动作世界模型

[AdaWorld: Learning adaptable world models with latent actions](https://proceedings.mlr.press/v267/gao25u.html)

- **研究内容：** 预训练潜在动作后用少量交互适配新控制
- **核心方法 / 输入输出：** 视频预训练＋目标交互 → 可适配控制世界模型
- **讨论视角：** Action · 来源章节：§4.1.1, §4.2.1

<a id="paper-78"></a>
**[78] DreamDojo** · 2026 · 机器人世界模型

[DreamDojo: A Generalist Robot World Model from Large-Scale Human Videos](https://arxiv.org/abs/2602.06949)

- **研究内容：** 人类视频潜在控制预训练后适配机器人数据
- **核心方法 / 输入输出：** 人类视频/机器人数据 → 机器人未来模拟
- **讨论视角：** Action · Reward / Value · 来源章节：§4.1.1, §4.2.1, §5.2.2

<a id="paper-79"></a>
**[79] LAPO** · 2023 · 策略学习

[Learning to Act without Actions](https://arxiv.org/abs/2312.10812)

- **研究内容：** 从视频恢复潜在动作并适配可执行控制
- **核心方法 / 输入输出：** 视频、少量动作标签/奖励 → 策略
- **讨论视角：** Action · 来源章节：§4.1.1

### 动作条件响应建模

<a id="paper-80"></a>
**[80] Action-Conditional Video Prediction** · 2015 · 动作条件视频模型

[Action-Conditional Video Prediction using Deep Networks in Atari Games](https://arxiv.org/abs/1507.08750)

- **研究内容：** 将动作依赖变换插入视觉预测
- **核心方法 / 输入输出：** Atari 图像、动作 → 未来帧
- **讨论视角：** Action · 来源章节：§4.1.2

<a id="paper-81"></a>
**[81] DriveGAN** · 2021 · 可控驾驶模拟

[DriveGAN: Towards a Controllable High-Quality Neural Simulation](https://arxiv.org/abs/2104.15060)

- **研究内容：** 分离车辆操控与场景属性编辑
- **核心方法 / 输入输出：** 驾驶控制、场景属性条件 → 视频
- **讨论视角：** Action · 来源章节：§4.1.2

<a id="paper-82"></a>
**[82] AVID** · 2024 · 动作适配方法

[AVID: Adapting Video Diffusion Models to World Models](https://arxiv.org/abs/2410.12822)

- **研究内容：** 用 adapter 与 mask 把视频扩散模型适配为世界模型
- **核心方法 / 输入输出：** 视觉历史、动作适配信号 → 后续视频
- **讨论视角：** Action · 来源章节：§4.1.2

<a id="paper-83"></a>
**[83] Vid2World** · 2025 · 动作条件视频模型

[Vid2World: Crafting Video Diffusion Models to Interactive World Models](https://arxiv.org/abs/2505.14357)

- **研究内容：** 自回归适配与动作 guidance 加强交互响应
- **核心方法 / 输入输出：** 视觉历史、动作 → 后续视频
- **讨论视角：** Action · 来源章节：§4.1.2, §4.2.1, §4.2.2

<a id="paper-84"></a>
**[84] UniSim** · 2023 · 动作条件模拟器

[Learning Interactive Real-World Simulators](https://arxiv.org/abs/2310.06114)

- **研究内容：** 结合异质数据模拟高层指令与低层控制效果
- **核心方法 / 输入输出：** 历史、高层指令/低层控制 → 未来视频
- **讨论视角：** Action · 来源章节：§4.1.2

<a id="paper-85"></a>
**[85] IRASim** · 2024 · 动作条件视频模型

[IRASim: A Fine-Grained World Model for Robot Manipulation](https://arxiv.org/abs/2406.14540)

- **研究内容：** 以逐帧条件对齐命令与生成帧
- **核心方法 / 输入输出：** 机器人动作序列 → 对齐的未来帧
- **讨论视角：** Action · 来源章节：§4.1.2, §4.2.1

<a id="paper-86"></a>
**[86] Ctrl-World** · 2025 · 动作条件视频模型

[Ctrl-World: A Controllable Generative World Model for Robot Manipulation](https://arxiv.org/abs/2510.10125)

- **研究内容：** 结合逐帧动作、多视图和位姿记忆检索
- **核心方法 / 输入输出：** 动作、历史、位姿 → 多视图机器人视频
- **讨论视角：** Action · Reward / Value · 来源章节：§4.1.2, §5.1.1, §5.2.2

<a id="paper-87"></a>
**[87] Vista** · 2024 · 驾驶世界模型

[Vista: A Generalizable Driving World Model with High Fidelity and Versatile Controllability](https://arxiv.org/abs/2405.17398)

- **研究内容：** 支持多种驾驶控制条件的未来模拟
- **核心方法 / 输入输出：** 指令/目标点/轨迹/转向/速度 → 驾驶视频
- **讨论视角：** Action · 来源章节：§4.1.2

<a id="paper-88"></a>
**[88] GAIA-2** · 2025 · 驾驶世界模型

[GAIA-2: A Controllable Multi- View Generative World Model for Autonomous Driving](https://arxiv.org/abs/2503.20523)

- **研究内容：** 以结构化条件控制多相机生成
- **核心方法 / 输入输出：** 自车动态、其他交通参与者配置 → 多视图视频
- **讨论视角：** Action · 来源章节：§4.1.2

<a id="paper-89"></a>
**[89] GEM** · 2024 · 可控视频世界模型

[GEM: A Generalizable Ego-Vision Multimodal World Model for Fine-Grained Ego-Motion, Object Dynamics, and Scene Composition Control](https://arxiv.org/abs/2412.11198)

- **研究内容：** 分别控制自运动、物体动态与场景组成
- **核心方法 / 输入输出：** 自车轨迹、稀疏特征、人体姿态 → 视频
- **讨论视角：** Action · 来源章节：§4.1.2

<a id="paper-90"></a>
**[90] Navigation World Models** · 2024 · 导航世界模型

[Navigation World Models](https://arxiv.org/abs/2412.03572)

- **研究内容：** 模拟导航动作的未来观测供轨迹比较
- **核心方法 / 输入输出：** 导航历史、动作 → 未来观测
- **讨论视角：** Action · 来源章节：§4.1.2

<a id="paper-91"></a>
**[91] Hunyuan-GameCraft** · 2025 · 交互游戏视频模型

[Hunyuan-GameCraft: High-dynamic Interactive Game Video Generation with Hybrid History Condition](https://arxiv.org/abs/2506.17201)

- **研究内容：** 将键鼠输入映射到相机表示并保留历史
- **核心方法 / 输入输出：** 键盘/鼠标、历史 → 游戏视频
- **讨论视角：** Action · 来源章节：§4.1.2

<a id="paper-92"></a>
**[92] Matrix-Game 2.0** · 2025 · 交互游戏视频模型

[Matrix-game 2.0: An open-source, real-time, and streaming interactive world model](https://arxiv.org/abs/2508.13009)

- **研究内容：** 逐帧注入动作并用少步扩散支持流式生成
- **核心方法 / 输入输出：** 历史、逐帧动作 → 流式视频
- **讨论视角：** Action · 来源章节：§4.1.2

### 稀疏控制与稠密几何

<a id="paper-21"></a>
**[21] ORV** · 2025 · 动作条件视频模型

[ORV: 4D Occupancycentric Robot Video Generation](https://arxiv.org/abs/2506.03079)

- **研究内容：** 用动作通路和 4D occupancy 联合约束机器人视频
- **核心方法 / 输入输出：** 分块 7-DoF 动作、占据渲染 → 视频
- **讨论视角：** Action · 来源章节：§4.1.3

<a id="paper-22"></a>
**[22] KVLR** · 2026 · 动作条件视频模型

[From Articulated Kinematics to Routed Visual Control for Action-Conditioned Surgical Video Generation](https://arxiv.org/abs/2605.08712)

- **研究内容：** 将关节运动学提升为图像对齐控制场并分层路由
- **核心方法 / 输入输出：** 机器人运动学 → 语义/深度/运动控制场 → 手术视频
- **讨论视角：** Action · 来源章节：§4.1.3

<a id="paper-24"></a>
**[24] OmniNWM** · 2025 · 集成世界模型

[OmniNWM: Omniscient Driving Navigation World Models](https://arxiv.org/abs/2510.18313)

- **研究内容：** 连接全景生成、轨迹控制和占据奖励
- **核心方法 / 输入输出：** 轨迹控制 → RGB/语义/深度/占据与结构化评分
- **讨论视角：** Action · Reward / Value · Integration · 来源章节：§4.1.3, §5.3, §6.1.2

<a id="paper-93"></a>
**[93] PointWorld** · 2026 · 三维动作条件世界模型

[PointWorld: Scaling 3D World Models for In- The-Wild Robotic Manipulation](https://arxiv.org/abs/2601.03782)

- **研究内容：** 在共同 3D 点流空间表示动作与环境运动
- **核心方法 / 输入输出：** RGB-D、3D 动作点流 → 环境点流
- **讨论视角：** Action · Reward / Value · 来源章节：§4.1.3, §5.2.1

<a id="paper-94"></a>
**[94] PAM** · 2026 · 可控视频/数据生成

[PAM: A Pose-Appearance-Motion Engine for Simto-Real HOI Video Generation](https://arxiv.org/abs/2603.22193)

- **研究内容：** 协调姿态、外观、运动生成人物与物体交互视频
- **核心方法 / 输入输出：** 深度/分割/关键点/姿态 → HOI 视频
- **讨论视角：** Action · 来源章节：§4.1.3

<a id="paper-95"></a>
**[95] Light-X** · 2025 · 可控四维渲染

[Light-X: Generative 4D Video Rendering with Camera and Illumination Control](https://arxiv.org/abs/2512.05115)

- **研究内容：** 分开相机轨迹与照明控制
- **核心方法 / 输入输出：** 动态点云、相机与光照条件 → 视频
- **讨论视角：** Action · 来源章节：§4.1.3

### 动作生成与未来预测的联合建模

<a id="paper-96"></a>
**[96] Unified World Models** · 2025 · 联合视频动作模型

[Unified World Models: Coupling Video and Action Diffusion for Pretraining on Large Robotic Datasets](https://arxiv.org/abs/2504.02792)

- **研究内容：** 共享 Transformer 耦合视频与动作扩散
- **核心方法 / 输入输出：** 视频/动作的不同条件组合 → 视频或动作
- **讨论视角：** Action · 来源章节：§4.1.4

<a id="paper-97"></a>
**[97] WorldVLA** · 2025 · 联合视频动作模型

[WorldVLA: Towards Autoregressive Action World Model](https://arxiv.org/abs/2506.21539)

- **研究内容：** 以自回归方式结合动作生成和未来图像预测
- **核心方法 / 输入输出：** 观测/任务上下文 → 动作与未来图像
- **讨论视角：** Action · 来源章节：§4.1.4, §4.2.3

<a id="paper-98"></a>
**[98] Motus** · 2025 · 联合视频动作模型

[Motus: A Unified Latent Action World Model](https://arxiv.org/abs/2512.13030)

- **研究内容：** 组合理解、视频和动作专家及多模态生成
- **核心方法 / 输入输出：** 多模态条件 → 视频/动作；光流潜在动作用于预训练
- **讨论视角：** Action · 来源章节：§4.1.4

<a id="paper-99"></a>
**[99] VideoVLA** · 2025 · 联合视频动作模型

[VideoVLA: Video Generators Can Be Generalizable Robot Manipulators](https://arxiv.org/abs/2512.06963)

- **研究内容：** 从图像与语言共同生成机器人行为和预期结果
- **核心方法 / 输入输出：** 图像、语言指令 → 动作序列＋未来视觉结果
- **讨论视角：** Action · 来源章节：§4.1.4, §4.2.3

<a id="paper-100"></a>
**[100] DreamZero** · 2026 · 联合视频动作模型

[World Action Models are Zero-shot Policies](https://arxiv.org/abs/2602.15922)

- **研究内容：** 视频扩散骨干联合学习异质机器人数据中的行为
- **核心方法 / 输入输出：** 机器人上下文 → 视频与动作
- **讨论视角：** Action · 来源章节：§4.1.4

<a id="paper-101"></a>
**[101] ViPRA** · 2025 · 视频预测驱动策略

[ViPRA: Video Prediction for Robot Actions](https://arxiv.org/abs/2511.07732)

- **研究内容：** 先预测未来与运动潜在动作，再解码机器人控制
- **核心方法 / 输入输出：** 视频/语言 → 未来观测、潜在动作 → 控制序列
- **讨论视角：** Action · 来源章节：§4.1.4, §4.2.3

### 动作响应与策略评测

<a id="paper-102"></a>
**[102] WorldGym** · 2025 · 策略评测系统

[WorldGym: World Model as An Environment for Policy Evaluation](https://arxiv.org/abs/2506.00613)

- **研究内容：** 用世界模型 rollout 和 VLM 判断估计策略表现
- **核心方法 / 输入输出：** 策略 rollout → 生成视频 → 成功评估
- **讨论视角：** Action · Reward / Value · 来源章节：§4.2.2, §5.1.1, §5.2.2, §5.2.3

### 预测与执行的一致性

<a id="paper-103"></a>
**[103] SuSIE** · 2023 · 视觉子目标与策略

[Zero-Shot Robotic Manipulation with Pretrained Image-Editing Diffusion Models](https://arxiv.org/abs/2310.10639)

- **研究内容：** 图像编辑模型生成子目标供低层策略执行
- **核心方法 / 输入输出：** 当前图像/目标 → 子目标图像 → 策略控制
- **讨论视角：** Action · 来源章节：§4.2.3

<a id="reward-value"></a>
## Reward / Value · 奖励与价值

### 任务评估

<a id="paper-104"></a>
**[104] Reward as An Agent** · 2026 · 任务评估器

[Reward as An Agent for Embodied World Models](https://arxiv.org/abs/2606.19990)

- **研究内容：** 以任务完成与物理合理性评估生成行为
- **核心方法 / 输入输出：** 生成轨迹、任务 → 评估反馈
- **讨论视角：** Reward / Value · 来源章节：§5.1.1, §5.2.1

<a id="paper-105"></a>
**[105] World-Gymnast** · 2026 · 模型内策略训练

[World-Gymnast: Training Robots with Reinforcement Learning in a World Model](https://arxiv.org/abs/2602.02454)

- **研究内容：** 以 VLM 奖励优化视频世界模型中的 VLA
- **核心方法 / 输入输出：** 模型生成 rollout、VLM 反馈 → 更新策略
- **讨论视角：** Reward / Value · 来源章节：§5.1.1

<a id="paper-106"></a>
**[106] World Model Self-Distillation** · 2026 · 任务条件世界模型训练

[World Model Self-Distillation: Training World Models to Solve General Tasks](https://arxiv.org/abs/2606.12072)

- **研究内容：** 用蒸馏、VLM 反馈与物理约束改善任务生成
- **核心方法 / 输入输出：** 短任务指令 → 任务视频；反馈优化生成器
- **讨论视角：** Reward / Value · 来源章节：§5.1.1, §5.2.1

### 奖励建模

<a id="paper-14"></a>
**[14] DreamerV3** · 2023 · 世界模型与策略学习

[Mastering Diverse Domains through World Models](https://arxiv.org/abs/2301.04104)

- **研究内容：** 用统一训练支持多任务域的想象式学习
- **核心方法 / 输入输出：** 观测、动作 → 潜在轨迹、观测/奖励/延续信号
- **讨论视角：** Reward / Value · 来源章节：§5.1.2, §5.1.3

<a id="paper-107"></a>
**[107] Drive-OccWorld** · 2024 · 占据预测与规划

[Driving in the Occupancy World: Vision-Centric 4D Occupancy Forecasting and Planning via World Models for Autonomous Driving](https://arxiv.org/abs/2408.14197)

- **研究内容：** 用预测占据及其成本评估驾驶轨迹
- **核心方法 / 输入输出：** 观测/占据预测、候选轨迹 → 几何成本与规划
- **讨论视角：** Reward / Value · 来源章节：§5.1.2, §5.3

<a id="paper-108"></a>
**[108] Think2Drive** · 2024 · 驾驶世界模型与强化学习

[Think2Drive: Efficient Reinforcement Learning by Thinking in Latent World Model for Quasi-Realistic Autonomous Driving (in CARLA-v2)](https://arxiv.org/abs/2402.16720)

- **研究内容：** 在潜在世界模型中学习驾驶奖励与策略
- **核心方法 / 输入输出：** 驾驶交互 → 潜在预测、奖励和策略
- **讨论视角：** Reward / Value · 来源章节：§5.1.2

<a id="paper-109"></a>
**[109] DayDreamer** · 2022 · 机器人世界模型与强化学习

[DayDreamer: World Models for Physical Robot Learning](https://arxiv.org/abs/2206.14176)

- **研究内容：** 将实体机器人奖励预测用于想象行为学习
- **核心方法 / 输入输出：** 机器人观测/动作 → 状态与奖励；学习行为
- **讨论视角：** Reward / Value · 来源章节：§5.1.2

<a id="paper-110"></a>
**[110] DreamerV2** · 2020 · 世界模型与策略学习

[Mastering Atari with Discrete World Models](https://arxiv.org/abs/2010.02193)

- **研究内容：** 以离散潜在状态进行想象式行为学习
- **核心方法 / 输入输出：** 观测、动作 → 潜在轨迹与奖励
- **讨论视角：** Reward / Value · 来源章节：§5.1.2

<a id="paper-111"></a>
**[111] HarmonyDream** · 2023 · 世界模型训练

[HarmonyDream: Task Harmonization Inside World Models](https://arxiv.org/abs/2310.00344)

- **研究内容：** 平衡观测与奖励学习的损失权重
- **核心方法 / 输入输出：** 交互数据 → 更平衡的观测/转移/奖励学习
- **讨论视角：** Reward / Value · 来源章节：§5.1.2, §5.2.1, §5.2.2

<a id="paper-112"></a>
**[112] DeepMDP** · 2019 · 表征学习与理论

[DeepMDP: Learning Continuous Latent Space Models for Representation Learning](https://arxiv.org/abs/1906.02736)

- **研究内容：** 通过奖励与转移预测研究价值保留条件
- **核心方法 / 输入输出：** 状态、动作、奖励 → 潜在模型与价值误差关系
- **讨论视角：** Reward / Value · 来源章节：§5.1.2, §5.2.2

### 价值预测与价值感知学习

<a id="paper-15"></a>
**[15] TD-MPC2** · 2023 · 世界模型与规划

[TD-MPC2: Scalable, Robust World Models for Continuous Control](https://arxiv.org/abs/2310.16828)

- **研究内容：** 以短潜在轨迹和终端价值做连续控制
- **核心方法 / 输入输出：** 状态/观测、动作 → 任务潜在转移、奖励与价值
- **讨论视角：** Reward / Value · 来源章节：§5.1.3, §5.1.4

<a id="paper-113"></a>
**[113] Value Prediction Network** · 2017 · 任务导向模型与规划

[Value Prediction Network](https://arxiv.org/abs/1707.03497)

- **研究内容：** 学习用于前瞻搜索的抽象动力学与价值
- **核心方法 / 输入输出：** 状态/动作 → 奖励、折扣与价值
- **讨论视角：** Reward / Value · 来源章节：§5.1.3

<a id="paper-114"></a>
**[114] EfficientZero** · 2021 · 世界模型与搜索

[Mastering Atari Games with Limited Data](https://arxiv.org/abs/2111.00210)

- **研究内容：** 结合奖励前缀、叶价值和旧策略数据校正
- **核心方法 / 输入输出：** 有限交互 → 搜索所需模型与价值目标
- **讨论视角：** Reward / Value · 来源章节：§5.1.3, §5.2.3

<a id="paper-115"></a>
**[115] EfficientZero V2** · 2024 · 世界模型与搜索

[EfficientZero V2: Mastering Discrete and Continuous Control with Limited Data](https://arxiv.org/abs/2403.00564)

- **研究内容：** 用搜索产生更适合演化策略的价值目标
- **核心方法 / 输入输出：** 离散/连续控制数据 → 搜索与价值学习
- **讨论视角：** Reward / Value · 来源章节：§5.1.3, §5.2.3

<a id="paper-116"></a>
**[116] TD-MPC** · 2022 · 世界模型与规划

[Temporal Difference Learning for Model Predictive Control](https://arxiv.org/abs/2203.04955)

- **研究内容：** 用短轨迹累计奖励加终端价值选择控制
- **核心方法 / 输入输出：** 状态/观测、动作 → 潜在转移、奖励与终端价值
- **讨论视角：** Reward / Value · Integration · 来源章节：§5.1.3, §5.1.4, §6.1.1

<a id="paper-117"></a>
**[117] Cosmos Policy** · 2026 · 视频模型策略与规划

[Cosmos Policy: Fine-Tuning Video Models for Visuomotor Control and Planning](https://arxiv.org/abs/2601.16163)

- **研究内容：** 结合未来状态和价值预测评估候选动作
- **核心方法 / 输入输出：** 视觉上下文 → 动作、未来状态与价值预测
- **讨论视角：** Reward / Value · 来源章节：§5.1.3, §5.2.3

<a id="paper-118"></a>
**[118] Value Equivalence** · 2020 · 理论

[The Value Equivalence Principle for Model-Based Reinforcement Learning](https://arxiv.org/abs/2011.03506)

- **研究内容：** 以指定策略和函数集上的 Bellman 更新一致定义模型
- **核心方法 / 输入输出：** 环境、策略/函数集合 → 价值等价条件
- **讨论视角：** Reward / Value · 来源章节：§5.1.3, §5.2.1, §5.2.3

<a id="paper-119"></a>
**[119] Proper Value Equivalence** · 2021 · 理论

[Proper Value Equivalence](https://arxiv.org/abs/2106.10316)

- **研究内容：** 以保持策略价值刻画规划相关模型
- **核心方法 / 输入输出：** 模型与策略族 → 策略价值保持条件
- **讨论视角：** Reward / Value · 来源章节：§5.1.3, §5.2.3

<a id="paper-120"></a>
**[120] Calibrated VAML** · 2025 · 理论与模型学习

[Calibrated valueaware model learning with probabilistic environment models](https://proceedings.mlr.press/v267/voelcker25a.html)

- **研究内容：** 校准概率模型的价值敏感学习目标
- **核心方法 / 输入输出：** 概率转移/价值信息 → 校准模型学习目标
- **讨论视角：** Reward / Value · 来源章节：§5.1.3, §5.2.2

<a id="paper-121"></a>
**[121] ROMI** · 2026 · 离线模型强化学习

[Model-based Offline RL via Robust Value-Aware Model Learning with Implicitly Differentiable Adaptive Weighting](https://arxiv.org/abs/2603.08118)

- **研究内容：** 以保守价值目标和自适应权重训练模型
- **核心方法 / 输入输出：** 离线转移数据 → 动力学/价值联合学习
- **讨论视角：** Reward / Value · 来源章节：§5.1.3, §5.2.2

### 任务导向的模型学习

<a id="paper-23"></a>
**[23] VAML** · 2017 · 理论与模型学习

[Value-Aware Loss Function for Model-based Reinforcement Learning](https://proceedings.mlr.press/v54/farahmand17a.html)

- **研究内容：** 按下游价值函数衡量转移模型误差
- **核心方法 / 输入输出：** 转移与价值函数信息 → 价值敏感的模型学习损失
- **讨论视角：** Reward / Value · 来源章节：§5.1.4

<a id="paper-122"></a>
**[122] VaGraM** · 2022 · 价值敏感模型学习

[Value Gradient weighted Model-Based Reinforcement Learning](https://arxiv.org/abs/2204.01464)

- **研究内容：** 用价值梯度给状态预测误差加权
- **核心方法 / 输入输出：** 转移误差、价值梯度 → 加权模型目标
- **讨论视角：** Reward / Value · 来源章节：§5.1.4

<a id="paper-123"></a>
**[123] Newt** · 2025 · 多任务世界模型与控制

[Learning Massively Multitask World Models for Continuous Control](https://arxiv.org/abs/2511.19584)

- **研究内容：** 以语言条件、多任务演示和在线交互扩大覆盖
- **核心方法 / 输入输出：** 语言任务、交互数据 → 多任务世界模型/控制
- **讨论视角：** Reward / Value · 来源章节：§5.1.4

### 目标对齐

<a id="paper-124"></a>
**[124] Visual Foresight** · 2018 · 视觉预测与规划

[Visual Foresight: Model-Based Deep Reinforcement Learning for Vision-Based Robotic Control](https://arxiv.org/abs/1812.00568)

- **研究内容：** 通过预测未来和视觉目标选择机器人行为
- **核心方法 / 输入输出：** 视觉历史、候选控制 → 未来图像与目标评分
- **讨论视角：** Reward / Value · 来源章节：§5.2.1

### 奖励与价值估计

<a id="paper-125"></a>
**[125] What Model Does MuZero Learn?** · 2023 · 诊断研究

[What model does MuZero learn?](https://arxiv.org/abs/2306.00840)

- **研究内容：** 测模型累计奖励误差及对行为策略的依赖
- **核心方法 / 输入输出：** MuZero、动作序列/策略 → 奖励预测误差分析
- **讨论视角：** Reward / Value · 来源章节：§5.2.2, §5.2.3

<a id="paper-126"></a>
**[126] COMBO** · 2021 · 离线模型强化学习

[COMBO: Conservative Offline Model-Based Policy Optimization](https://arxiv.org/abs/2102.08363)

- **研究内容：** 用保守价值学习抑制模型外推的过度乐观
- **核心方法 / 输入输出：** 离线数据与模型样本 → 保守价值/策略
- **讨论视角：** Reward / Value · Integration · 来源章节：§5.2.2, §6.2.1

### 任务与策略分布变化

<a id="paper-127"></a>
**[127] MBPO** · 2019 · 模型强化学习

[When to Trust Your Model: Model-Based Policy Optimization](https://arxiv.org/abs/1906.08253)

- **研究内容：** 从真实状态分支短 rollout 限制模型误差与策略漂移
- **核心方法 / 输入输出：** 真实状态、模型 rollout → 策略更新
- **讨论视角：** Reward / Value · Integration · 来源章节：§5.2.3, §6.2.1

### 诊断与评测

<a id="paper-128"></a>
**[128] RoboScape-R** · 2025 · 交互训练环境

[RoboScape-R: Unified Reward-Observation World Models for Generalizable Robotics Training via RL](https://arxiv.org/abs/2512.03556)

- **研究内容：** 联合观测与奖励建模并明确目标和终止信号
- **核心方法 / 输入输出：** 目标观测/交互 → 观测、奖励与终止反馈
- **讨论视角：** Reward / Value · 来源章节：§5.3

<a id="integration"></a>
## Integration · 系统集成与评测

### 真实观测反馈下的规划

<a id="paper-129"></a>
**[129] PETS** · 2018 · 概率动力学与规划

[Deep Reinforcement Learning in a Handful of Trials using Probabilistic Dynamics Models](https://arxiv.org/abs/1805.12114)

- **研究内容：** 用概率集成和轨迹采样传播规划不确定性
- **核心方法 / 输入输出：** 状态、候选动作 → 概率轨迹与控制选择
- **讨论视角：** Integration · 来源章节：§6.1.1

<a id="paper-130"></a>
**[130] Puppeteer** · 2024 · 分层控制系统

[Hierarchical World Models as Visual Whole-Body Humanoid Controllers](https://arxiv.org/abs/2405.18418)

- **研究内容：** 结合高层视觉控制与低层人形控制器
- **核心方法 / 输入输出：** 视觉 → 高层命令 → 低层控制
- **讨论视角：** Integration · 来源章节：§6.1.1

### 学习到的模拟器内的策略交互

<a id="paper-131"></a>
**[131] Dreamer 4** · 2025 · 世界模型内策略学习

[Training Agents Inside of Scalable World Models](https://arxiv.org/abs/2509.24527)

- **研究内容：** 在可交互预测模型中从离线数据学习 Minecraft 行为
- **核心方法 / 输入输出：** 离线交互数据 → 动作条件模拟与行为学习
- **讨论视角：** Integration · 来源章节：§6.1.2

<a id="paper-132"></a>
**[132] World-Env** · 2025 · 模型内策略训练

[World-Env: Leveraging World Model as a Virtual Environment for VLA Post-Training](https://arxiv.org/abs/2509.24948)

- **研究内容：** 固定世界模型构建 VLA 后训练交互回合
- **核心方法 / 输入输出：** 策略动作 → 模拟观测、完成/终止反馈
- **讨论视角：** Integration · 来源章节：§6.1.2

<a id="paper-133"></a>
**[133] RISE** · 2026 · 模型辅助策略学习

[RISE: Self-Improving Robot Policy with Compositional World Model](https://arxiv.org/abs/2602.11075)

- **研究内容：** 以短模型扩展和进度价值构造动作块优势
- **核心方法 / 输入输出：** 离线状态、短 rollout、价值 → 策略更新
- **讨论视角：** Integration · 来源章节：§6.1.2

<a id="paper-134"></a>
**[134] ReSim** · 2025 · 驾驶模拟与策略评测

[ReSim: Reliable World Simulation for Autonomous Driving](https://arxiv.org/abs/2506.09981)

- **研究内容：** 结合预测模拟与 Video2Reward 进行策略评估选择
- **核心方法 / 输入输出：** 预测驾驶视频 → 奖励/策略评估
- **讨论视角：** Integration · 来源章节：§6.1.2

### 执行数据驱动的模型与策略更新

<a id="paper-25"></a>
**[25] GigaBrain-0.5M\*** · 2026 · 集成策略系统

[GigaBrain-0.5M\*: a VLA That Learns From World Model-Based Reinforcement Learning](https://arxiv.org/abs/2602.12099)

- **研究内容：** 用预测未来与价值指导策略并结合真实纠正数据
- **核心方法 / 输入输出：** 未来状态/价值信号 → 策略学习；真实 rollout 更新系统
- **讨论视角：** Integration · 来源章节：§6.1.3

<a id="paper-135"></a>
**[135] World-VLA-Loop** · 2026 · 模型策略闭环训练

[World- VLA-Loop: Closed-Loop Learning of Video World Model and VLA Policy](https://arxiv.org/abs/2602.06508)

- **研究内容：** 以目标环境新轨迹共同改进模型与策略
- **核心方法 / 输入输出：** 真实交互轨迹 → 世界模型和 VLA 更新
- **讨论视角：** Integration · 来源章节：§6.1.3

<a id="paper-136"></a>
**[136] WoVR** · 2026 · 模型策略闭环训练

[WoVR: World Models as Reliable Simulators for Post-Training VLA Policies with RL](https://arxiv.org/abs/2602.13977)

- **研究内容：** 以真实目标环境数据提高模型内策略后训练可靠性
- **核心方法 / 输入输出：** 目标环境轨迹、模拟交互 → 模型/策略改进
- **讨论视角：** Integration · 来源章节：§6.1.3

<a id="paper-137"></a>
**[137] WAM-RL** · 2026 · 模型策略闭环训练

[WAM-RL: World-Action Model Reinforcement Learning with Reconstruction Rewards and Online Video SFT](https://arxiv.org/abs/2606.17906)

- **研究内容：** 结合执行一致性、重建奖励和在线视频更新
- **核心方法 / 输入输出：** 执行结果与视频 → actor/世界模型更新
- **讨论视角：** Integration · 来源章节：§6.1.3

### 生成模型作为数据引擎

<a id="paper-138"></a>
**[138] OnePoseViaGen** · 2025 · 生成数据与感知

[One View, Many Worlds: Single-Image to 3D Object Meets Generative Domain Randomization for One-Shot 6D Pose Estimation](https://arxiv.org/abs/2509.07978)

- **研究内容：** 以单图三维生成和域随机化训练姿态估计
- **核心方法 / 输入输出：** 单图 → 三维对象/合成数据 → 6D 姿态估计
- **讨论视角：** Integration · 来源章节：§6.1.4

### 模型利用、保守学习与分布偏移

<a id="paper-139"></a>
**[139] MOPO** · 2020 · 离线模型强化学习

[MOPO: Model-based Offline Policy Optimization](https://arxiv.org/abs/2005.13239)

- **研究内容：** 用模型不确定性惩罚限制离线策略外推
- **核心方法 / 输入输出：** 离线数据、模型预测 → 惩罚奖励与策略优化
- **讨论视角：** Integration · 来源章节：§6.2.1

### 失败发现与功能评测

<a id="paper-140"></a>
**[140] Challenger** · 2025 · 对抗场景生成/测试

[Challenger: Affordable Adversarial Driving Video Generation](https://arxiv.org/abs/2505.15880)

- **研究内容：** 搜索有效对抗驾驶轨迹并渲染多视图压力测试
- **核心方法 / 输入输出：** 对抗轨迹/场景 → 驾驶视频与策略测试
- **讨论视角：** Integration · 来源章节：§6.3

<a id="paper-141"></a>
**[141] BasinLens** · 2026 · 失败发现方法

[Where World Models Break: Natural-Input Failure Discovery](https://arxiv.org/abs/2608.22421)

- **研究内容：** 在有限查询预算下寻找可复现的自然输入失败区域
- **核心方法 / 输入输出：** 有效输入变化、模型查询 → 失败案例与复现检验
- **讨论视角：** Integration · 来源章节：§6.3

<a id="paper-142"></a>
**[142] WorldArena** · 2026 · 评测基准

[WorldArena: A Unified Benchmark for Evaluating Perception and Functional Utility of Embodied World Models](https://arxiv.org/abs/2602.08971)

- **研究内容：** 同时评价感知质量与具身功能效用
- **核心方法 / 输入输出：** 生成结果/任务测试 → 多维评测
- **讨论视角：** Integration · 来源章节：§6.3

<a id="sources"></a>
## 来源与整理说明

- 内容来源：`World_Models_Survey (6)` 配套的“世界模型综述 全文献总表”（2026-10-14 版）。
- 来源标注的文献截止日期：2026-10-08；本 README 整理日期：2026-10-15。
- 文献编号、标题、链接、研究内容、方法简介与跨章节关系均来自所提供页面；未收录原稿引用上下文及本地文件路径。
- 年份依据来源的参考文献文本整理，不统一视为正式发表年份。GNS、DreamerV2、Value Equivalence、MOPO 的页面年份误取了 arXiv 编号前四位，此处按原参考文献均修正为 2020。
- 论文链接沿用来源，未在此次格式整理中逐条联网核验。

<a id="contributing"></a>
## Contributing

欢迎补充相关论文、纠正文献信息或完善方法简介。提交时请提供完整标题、年份、原论文或官方项目链接、建议分类，以及简短的研究内容与方法说明。涉及能力、局限或失败机制的描述，请附原文或实验依据。
