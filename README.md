# Travel Planner Skill

[中文](#中文) | [English](#english)

## 中文

一个适用于支持 Agent Skills 的 AI Agent 的分阶段休闲旅行规划 Skill。它不会一次性堆出完整攻略，而是通过数字选项逐步协助用户确定目的地、预算、路线、同行成员、酒店和每日行程。

### 主要能力

- 根据时间、偏好和出发地推荐目的地
- 估算经济、舒适和品质三档预算
- 对比多种可执行路线
- 在推荐酒店前确认同行人数、成人/儿童与性别构成、同住关系和房间需求
- 根据路线优化酒店组合，减少换酒店和无效步行
- 生成行程总览，并按需展开每日交通、门票、餐饮和预约信息
- 对航班、酒店、签证、开放时间和票务等时效信息进行联网核实
- 针对儿童、老人和行动不便旅客调整节奏

### 安装

使用 Git 克隆到你所使用的 Agent 的 Skills 目录。不同 Agent 的目录位置可能不同，请以对应平台的文档为准。

例如，在 Codex 中可使用：

```powershell
git clone https://github.com/zhongzhibin1874-sketch/travel-planner-skill.git `
  "$HOME\.codex\skills\travel-planner"
```

如果目标目录已经存在，请先选择其他目录，或备份后再替换。安装完成后，重新启动对应 Agent 或新建对话，使 Skill 被重新发现。

### 使用示例

可以直接提出旅行需求：

```text
帮我做个旅游计划。
```

```text
我想去旅游。
```

```text
帮我规划一次 7 天的日本亲子旅行。
```

```text
国庆从上海出发，想找一个适合老人、步行不要太多的目的地。
```

也可以在支持显式 Skill 调用的 Agent 中输入：

```text
用 $travel-planner 帮我比较成都、重庆和贵阳的预算与路线。
```

Skill 会从当前缺失的决策开始，并通过数字选项逐步推进。即使只说“想去旅游”，它也会从最少的必要问题开始。用户可以随时直接输入新的目的地、预算或偏好。

### 工作流程

1. 旅行意图与目的地候选
2. 预算预期与签证范围
3. 路线方案对比
4. 同行成员与订房需求确认
5. 酒店组合优化
6. 行程总览与可展开的每日细节

### 隐私

公开版本不包含作者的家庭成员、证件或默认出发地等个人资料。旅行者信息仅从当前对话中获取，不应写入 `SKILL.md`。

### 项目结构

```text
travel-planner/
├── SKILL.md
├── README.md
└── agents/
    └── openai.yaml
```

### 许可证

本仓库目前尚未添加开源许可证。在许可证添加之前，默认保留全部权利。

## English

A staged leisure travel-planning skill for AI agents that support Agent Skills. It guides users through destination selection, budget expectations, route comparison, traveler and room confirmation, hotel optimization, and detailed daily itineraries without overwhelming them with a full plan at once.

### Features

- Destination recommendations based on timing, preferences, and departure city
- Economy, comfort, and premium budget estimates
- Practical route comparisons
- Mandatory traveler composition and room-requirement confirmation before hotel recommendations
- Hotel combinations optimized for location and fewer transfers
- Expandable daily transport, ticket, dining, and reservation details
- Current-source verification for flights, hotels, visas, opening hours, and tickets
- Accessibility-aware planning for children, elderly travelers, and mobility needs

### Installation

Clone the repository into the Skills directory used by your agent. The exact location depends on the platform.

For example, with Codex:

```powershell
git clone https://github.com/zhongzhibin1874-sketch/travel-planner-skill.git `
  "$HOME\.codex\skills\travel-planner"
```

Restart the agent or begin a new conversation after installation so the skill can be discovered.

### Example

```text
Help me plan a trip.
```

```text
I want to travel.
```

```text
Use $travel-planner to plan a relaxed seven-day family trip to Japan.
```

### License

No open-source license has been added yet. All rights are reserved until a license is provided.
