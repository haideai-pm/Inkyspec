# 🖋️ InkySpec

> **The ink that binds Business and AI.​**  
> 一个为 AI 时代设计的、轻量化且业务导向的规格驱动引擎。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

---

## 🌟 什么是 InkySpec？

在 AI 编程（Agentic Workflow）普及的今天，我们发现传统的开发流程正面临巨大挑战：
- **程序员审美污染**：需求文档（Spec）充满了技术术语，业务方（产品、客服、运营）看不懂。
- **文档即废纸**：规格说明书写完就死，AI 编写代码时依然在“瞎猜”意图。
- **流程臃肿**：为了规范而规范，繁琐的变更流程扼杀了 AI 的开发效率。

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
│   ├── project.yaml      # 项目灵魂：背景、技术栈、AI 生成规则
│   ├── specs/            # 现状库：01-首次咨询, 03-申请退款... (业务方查阅处)
│   ├── changes/          # 变更中：正在进行的 Feature 或 Bugfix (研发干活处)
│   └── archive/          # 历史墙：已合并的变更记录 (考古追溯处)
└── .claude/skills/       # AI 技能集成 (让 AI 读懂并执行上述文档)
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

## 🛠️ 快速开始 (Coming Soon)

目前项目正处于早期孵化阶段。我们正在完善核心 Skill 指令集。

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
