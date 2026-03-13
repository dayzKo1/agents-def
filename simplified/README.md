# 简化版 Agents 配置

精简版 OpenCode 多智能体配置，5 个核心角色，适合小型团队快速上手。

## Agent 角色

| Agent ID  | 角色         | 模式     | 职责                           |
|-----------|--------------|----------|--------------------------------|
| `pm`      | 项目经理     | primary  | 协调团队、拆解任务、把控进度   |
| `dev`     | 开发工程师   | subagent | 实现功能、编写代码、修复 bug   |
| `dev-2`   | 开发工程师   | subagent | 协作开发（并行任务）           |
| `architect`| 架构师      | subagent | 技术选型、架构设计、代码审查   |
| `qa`      | 测试工程师   | subagent | 测试用例、自动化测试、质量把关 |

## 使用方法

1. 复制 `opencode.json` 到 `~/.config/opencode/` 或项目根目录
2. 在 `provider` 中配置你的模型服务商和 API Key
3. 运行 `opencode` 启动，默认进入 `pm` 角色

## 配置要点

- **两个开发角色**：`dev` 和 `dev-2` 可并行处理不同模块
- **无运维角色**：适合 DevOps 自理或云服务托管的团队
- **模型配置**：将 `provider-id/model-id` 替换为实际值