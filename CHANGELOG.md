# 更新日志

本项目遵循 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/) 格式，版本号遵循 [SemVer](https://semver.org/lang/zh-CN/)。

## [Unreleased]

### 变更
- `index.html` 由「多模型 API 驱动版」改为「静态模范回答模板」（降噪耳机完整 5 步示范），移除 API Key 依赖和本地代理 `server.py`。

### 新增
- `demo.html`：分页式流程演示页（点「下一步」一页一步走完 5 步，开始页可改输入）。

### 计划中
- 支持导出 PDF / Markdown 报告文件
- 更多品类模范模板（手机 / 家电 / 保健品等）

## [1.0.0] - 2026-08-13

### 新增
- 完整的 5 步流水线：需求深挖 → 产品筛选 → 深度对比 → 渠道比价 → 报告生成。
- `SKILL.md`：Claude Code 技能定义（自包含，含登录检测 / 平台拦截 fallback / 购买链接分级 / Sources 分层）。
- `index.html`：网页版助手，多服务商 API 驱动、流式输出、6 维度对比可视化。
- 多服务商支持：Claude、DeepSeek、OpenAI、通义千问、Moonshot Kimi、智谱 GLM、自定义 OpenAI 兼容端点。
- 核心原则内置：安全优先、不编价格、不替用户拍板、太完美反而假（反刷评）。
- 开源配套：MIT License、README、CONTRIBUTING、CHANGELOG、.gitignore。

### 变更
- 技能命名由 `shopping-assistant` 改为 `ai-shopping-assistant-skill`。
- 网页版模型选择改为「可折叠覆盖」，默认用服务商推荐模型。

### 说明
- 本项目的 5 步流程是对 `shopping-compare-skill-main` 的重新编排与强化，向其致谢。
