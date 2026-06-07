# 🖋️ InkySpec

> **The ink that binds Business and AI.​**  
> 一个为 AI 时代设计的、轻量化且业务导向的规格驱动引擎。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

---

## 🌟 什么是 InkySpec？

在 AI 编程（Agentic Workflow）普及的今天，我们发现传统的开发流程正面临巨大挑战：
- **技术驱动**：需求文档（Spec）充满了技术术语，业务方（产品、客服、运营）看不懂。
- **文档即废纸**：规格说明书写完就死，AI 编写代码时依然在“瞎猜”意图。
- **流程臃肿**：为了规范而规范，繁琐的变更流程，扼杀了 AI 的开发效率，削弱了新晋AI开发者对规范的共识。

**InkySpec 重新定义了这一切。​** 我们抛弃了复杂的工程教条，用“像墨水书写一样自然”的逻辑，建立起业务方、研发、AI 三方都能读懂的共识。

---

## 🚀 核心特性

- 📂 **业务旅程主导 (Journey-First)​**：目录按业务场景（如：`03-申请退款`）而非代码模块组织，所有人一眼看懂。
- 🤖 **AI 规划原生 (AI-Native)​**：Spec 不是给人看的存档，而是 AI Skill 的直接输入，驱动 AI 自动拆解任务并实现。
- 📄 **极简三件套 (Minimalist)​**：只有 `Project (项目背景)`、`Spec (行为契约)` 和 `Task (任务清单)`。
- 🧹 **轻量归档 (Clean History)​**：历史变更自动归档，保持主规格库永远是系统现状的“唯一真理”。

---

## 🏗️ 目录结构

InkySpec 强制要求一种极其简洁且符合直觉的目录结构：

```text
project-root/
├── inkyspec/
│   ├── project.yaml                                # 项目说明书(AI 注入)：背景、技术栈、AI 生成规则
│   ├── specs/                                      # 当前规格库：01-首次咨询, 03-申请退款... (业务方也可以查阅)
│   │   ├── 01-首次咨询/
│   │   │   ├── spec.md
│   │   │   └── design.md
│   │   │   └── task.md                            # 可选
│   │   └── 90-平台能力/
│   │       ├── 91-模型路由/spec.md
│   │       ├── 92-工具风险分级/spec.md
│   │       └── 93-会话存储/spec.md
│   ├── changes/                                    # 变更中：正在进行的 Feature 或 Bugfix (研发干活处)
│   │   └── 2026-06-01-加退款短信通知/
│   │       ├── spec.md
│   │       ├── design.md                           # 可选
│   │       └── task.md
│   └── archive/                                    # 历史归档：已合并的变更记录 (考古追溯处)
│       └── 2026-05-01-初始客服流程/
│           ├── change-record.md
│           └── task.md
└── .claude/                                        # AI 技能集成 (让 AI 读懂并执行上述文档)
    └── skills/
        ├── inkyspec-propose/SKILL.md
        ├── inkyspec-apply/SKILL.md
        └── inkyspec-archive/SKILL.md
```

---

## 📝 核心理念

### 1. 业务命名，而非技术命名
不使用 `refund-logic-v2`，而是使用 `03-申请退款`。
### 2. 行为契约，而非实现细节
Spec 描述 `Given/When/Then` 的业务逻辑，不涉及类名、数据库表名或 SQL。
### 3. 一次变更，一份文档
在 `changes/` 目录下，一份 `spec.md` 包含了提案、设计和规格变更，一份 `task.md` 负责任务拆解。

---
## 🎬 规范起源

我们一直相信人是由兴趣而驱动，复杂繁琐的规范只会让开发人员增加维护成本，阻碍更多同行入场，规范不是铁律，不是法律，开发者即使稍有违背，也不影响项目开发，在不同公司中，也会存在不同规范，只是组织内部的一种方式，正如有的开发者用react ，有的开发者喜欢vue，不同的开发者使用不同的开发语言。

进入ai coding 的时代，各行业各岗位的开发者涌入开发圈，他们利用vibe coding开发自己的产品，提升自己的工作效率，随着深入，会开始寻找更高效的开发方式。

但是过去的规范，多数由工程师发起，出发点是技术人员能读懂，对于新入场的新进Ai coding 开发者，学习成本太高，他们可能是产品经理，设计师、运营、行政，财务、自由职业者……

这批由vibe coding为出发点的入场者，没有进行太多的编程培训，他们使用sdd（规范驱动开发） 多数是为了方便，因为vibe coding对代码管理和质量控制不太友好。

由此可见，学习传统的规范，会更容易放弃，直接结果就他们选择会让ai随机编写，但优质的代码需要一定的规范约束。

在使用openspec 的过程中，我们翻阅手册，查看了仓库，发现有大量的spec塞在一个change 里，而众多archive归档又塞在change里，层层嵌套，一个普通的文件目录中，打开竟然有众多文件，且无序号，只靠时间进行排序。

作为一个新晋ai开发者，感到非常难学习，在过去的产品设计生涯中，一直认为简单易用是产品的宗旨，而不是要求用户自己削成适合的形状，去适应产品的使用。

在引入openspec 的时候，每个llm生成的结果目录不一样，将新旧规范混合在一起，需要进行多次校正或提示词强制指定，原本只是为了提高开发而学习sdd，但现在反而增加了开发成本，为此编写一个适合自己的规范，以协调自己的开发。

我们会保证文档仓库的简洁，参考苹果的设计哲学，简单易用，不为规范而强制规范，我们达成共识，降低入门门槛，不增加开发者学习负担，

---

## 🛠️ 快速开始 (Coming Soon)

目前项目正处于早期孵化阶段。我们正在完善核心 Skill 指令集，文档模板等。

### 愿景
我们希望构建一个轻量级，上手难度超低，业务方，需求方，程序员都能看得懂，能清晰表达业务需求，AI快速实现，离开CLI也可以构建的规范，InkySpec 负责连接共识。

---

## 🤝 参与贡献

我们欢迎任何关于“如何让 Spec 更易读”、“如何让 AI 更好理解业务”的讨论。

1. **Fork** 本仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的变更 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个 **Pull Request**

---

## 📄 开源协议

本项目采用 [MIT](LICENSE) 协议。
