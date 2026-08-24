# 贡献指南

感谢你愿意为 `ai-shopping-assistant-skill` 做贡献！🎉

## 报告 Bug / 提需求

- 用 [Issue](https://github.com/jade888jgj/ai-shopping-assistant-skill/issues) 反馈，尽量附上：复现步骤、预期行为、实际行为、环境（浏览器 / Claude Code 版本）。
- 提需求请说明使用场景和期望效果。

## 提交代码（Pull Request）

1. Fork 本仓库，克隆到本地。
2. 新建分支：`git checkout -b feat/你的功能` 或 `fix/你的修复`。
3. 修改并自测。
4. 提交：`git commit -m "feat: 描述"`（参考 [Conventional Commits](https://www.conventionalcommits.org/)）。
5. 推送并开 PR，描述改动目的和影响范围。

## 代码约定

- **SKILL.md**：保持 5 步流水线结构清晰；核心原则不可删改（安全优先、不编价格、不替用户拍板）；新增步骤要说明「停不停、停什么」。
- **index.html**：静态模范模板，单文件、零依赖、双击可开。新增品类示范时，仿照「降噪耳机」的 5 步结构（需求深挖 / 产品筛选 / 深度对比 / 渠道比价 / 报告生成）复制一份即可。
- 改动后请在 `CHANGELOG.md` 追加记录。

## 行为准则

- 友好、尊重、就事论事。
- 本项目的红线：**不编价格、不替用户拍板、不碰用户密码/私有数据**。任何违背这三条的行为都不会被接受。

## 许可

提交代码即表示你同意按 [MIT License](LICENSE) 授权。
