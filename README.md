# goldmind 🪙

> A conversational LLM agent for gold (XAU) perpetual contract analysis — with a deterministic risk engine that never lets it blow up the account.

goldmind 是一个面向黄金永续合约的对话式分析 Agent。它结合实时行情、资金费率、
宏观数据与经济日历给出结构化的交易分析，并由一层**纯代码风控引擎**强制校验每条建议：
止损必须先于爆仓价触发、单笔亏损不超过风险预算、重大数据公布前禁止新开仓。

## Features
- 💬 **多轮对话分析**：追问用户意图，结合上下文给出判断
- 🛡️ **确定性风控引擎**：爆仓价、最大亏损、手续费由代码计算，不合规建议自动打回
- 📊 **结构化输出**：方向 / 杠杆 / 入场 / 止损 / 止盈 / 爆仓价 / 置信度 / 失效条件
- 🧠 **经验复盘**：每笔建议事后自动复盘，形成可检索的经验库
- 📈 **评测与回溯**：决策日志、置信度校准、对比不加杠杆持有基准
- 🔒 **只读设计**：仅使用公开行情接口，不持有任何交易权限

## Tech Stack
DeepSeek API · LangGraph · Pydantic · CCXT · Chroma · Langfuse · FastAPI

## Roadmap
- [ ] M0 行情工具与 Function Calling
- [ ] M1 风控引擎与单元测试
- [ ] M2 宏观数据与经济日历接入
- [ ] M3 决策日志与评测看板
- [ ] M4 前向验证（纸面记录 + 小额实盘）
- [ ] v2 基于决策日志的 SFT / DPO 微调实验

## Disclaimer
本项目仅用于 LLM Agent 技术研究，输出内容不构成投资建议。
杠杆交易风险极高，可能损失全部本金。
