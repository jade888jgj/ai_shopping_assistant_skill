<p align="center">
  <h1 align="center">🛒 ai-shopping-assistant-skill</h1>
  <p align="center">一站式 AI 购物决策助手 —— 帮你从「想买」走到「敢买」</p>
</p>

<p align="center">
  <a href="#license"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT"></a>
  <a href="https://github.com/jade888jgj/ai-shopping-assistant-skill"><img src="https://img.shields.io/badge/version-1.0.0-brightgreen.svg" alt="Version"></a>
</p>

---

## 这是什么

一个「选择困难症」克星。你只需要说一句「我想买个降噪耳机，预算 2000」，它会按 **5 步流水线** 从需求一路跑到最终报告：

```
①需求深挖 → ②产品筛选 → ③深度对比 → ④渠道比价 → ⑤报告生成
```

每一步该停下来问你的时候会停，不该问的一口气往下跑。

## 核心原则

| 原则 | 说明 |
|---|---|
| 🛡️ **安全 > 性价比 > 便利** | 任何品类安全第一权重 |
| 🙋 **不替用户拍板** | 给推荐 + 理由 + 风险，最终决策在用户 |
| 🔍 **太完美反而假** | 零差评/好评千篇一律 → 先怀疑刷评 |
| 🚫 **不编价格** | 搜不到就直说，绝不估价冒充；提醒核对到手价 |
| ⏸️ **该停就停** | 需要输入才停，能推断的一口气跑 |

## 5 步流水线详解

| 步骤 | 做什么 | 关键点 |
|---|---|---|
| ① 需求深挖 | 问清「谁用 · 放哪儿 · 多久一次 · 预算 · 痛点」，补你没想到的 | 不急着推产品；保健品/跟风款先做成本拷问 |
| ② 产品筛选 | 搜 → 筛不靠谱的 → 打分排名 → 单独挖差评 | 太完美反而假（疑似刷评降权） |
| ③ 深度对比 | 6 维度面对面拆解，每个维度给明确优胜方 | 质量/功能/质价比/口碑/售后/设计；按场景给唯一方向 |
| ④ 渠道比价 | 京东/天猫/拼多多/淘宝同款比价 | 搜不到就直说、不编价；提醒打开 App 核对 |
| ⑤ 报告生成 | 推荐哪个、备选哪个、为什么 | 写明白、不甩「都可以」 |

## 三个文件，三种用法

| 文件 | 是什么 | 用法 |
|---|---|---|
| [`SKILL.md`](SKILL.md) | **Claude Code 技能**（真实执行） | 放进 Claude Code，说「我想买 X」就真跑，能联网搜索/抓取/读图 |
| [`demo.html`](demo.html) | **分页式流程演示**（点「下一步」翻页） | 双击用浏览器打开，一页一步走完 5 步流程 |
| [`index.html`](index.html) | **一页式模范回答**（下滑看全） | 双击用浏览器打开，看「买降噪耳机」完整回答长什么样 |

> 💡 **区别**：`SKILL.md` 是「说明书」，由 Claude Code 执行，能真抓京东、被拦平台请你截图读图，价格更真；`demo.html` 和 `index.html` 是两种不同版式的静态示范页（分页式 vs 一页式），都不接 API、纯前端演示流程。

---

## 快速开始

### 用法 A：看流程演示（零门槛）

- **分页式**：双击 [`demo.html`](demo.html)，点「下一步」一页一步走完 5 步流程（开始页还能改输入）。
- **一页式**：双击 [`index.html`](index.html)，下滑看「买降噪耳机」完整 5 步模范回答。

### 用法 B：真实跑任意品类（Claude Code）

1. 把 `SKILL.md` 复制到：
   ```
   .claude/skills/ai-shopping-assistant-skill/SKILL.md
   ```
2. 对 Claude 说：**「我想买个降噪耳机，预算 2000」**，它按 5 步从头跑到尾，该停就问。

> 依赖 `shopping-compare-skill-main` 作为底层引擎（可选，环境里没有也能独立跑）。

---

## 目录结构

```
.
├── SKILL.md          # Claude Code 技能定义（核心，5 步流水线）
├── demo.html         # 分页式流程演示（点「下一步」翻页）
├── index.html        # 一页式模范回答模板（下滑看全）
├── README.md         # 本文件
├── LICENSE           # MIT 许可
├── CONTRIBUTING.md   # 贡献指南
├── CHANGELOG.md      # 版本历史
└── .gitignore
```

## 原理说明

- **SKILL.md 是「说明书」**：定义 5 步流程和操作规范，由 Claude Code 执行。执行时用 Claude Code 已登录的模型 + 内置工具（联网搜索、浏览器抓取、多模态读图），**不需要额外 API Key**。
- **demo.html / index.html 是「演示」**：静态 HTML，把 5 步流程用「降噪耳机」这一具体品类完整示范出来，纯前端零依赖。`demo.html` 是分页式（点下一步翻页），`index.html` 是一页式（下滑看全），方便你对照改造成自己的页面或直接作为设计稿参考。

## 免责声明

- 本项目只做**信息收集与分析**，不下单、不加购、不评论、不碰密码框。
- 电商实时到手价受登录、优惠券、地区等因素影响，**以 App 实际到手价为准**。
- 商品安全信息来自公开渠道，仅供决策参考，不构成购买建议。

## 贡献

欢迎提 Issue / PR。详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## License

[MIT](LICENSE) © 2026
