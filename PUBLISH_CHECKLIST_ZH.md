# GitHub 说明型仓库发布清单

## GitHub

- [ ] 创建公开仓库，例如 `BC-Auto-Workspace`，只上传本 ZIP 内的 Markdown 文档。
- [ ] 不上传 `.js`、`.html`、`.css`、`manifest.json`、测试代码或扩展安装 ZIP。
- [ ] 不在 GitHub Releases 提供插件包；统一引导到官方 Edge Add-ons。
- [ ] 设置 About Description：`Business Central workspace helper for Microsoft Edge | BC 页面自动优化工具`
- [ ] 勾选 Issues；如不想收到 PR，可以关闭/限制贡献入口。
- [ ] Edge 上架后，替换 README 的“Coming soon / 审核后更新”为真实官方商店链接。
- [ ] 补充经过脱敏的演示截图（如果希望展示产品界面）。
- [ ] 检查文档不会泄露真实 BC 租户、雇主邮箱、客户、订单等信息。
- [ ] 加入正式生效日期、合法拥有的支持邮箱或其他联系途径。
- [ ] 发布前确认源码、图标、文案和商标的实际权属。

## Microsoft Edge Add-ons

- [ ] 另行上传真正的插件运行 ZIP，**不是**这个 GitHub 介绍 ZIP。
- [ ] 按微软审核要求提交可审核的插件代码包，不能使用禁止的代码混淆手段。
- [ ] 使用本 GitHub 仓库公开的 `PRIVACY.md` HTTPS URL 作为候选隐私政策链接。
- [ ] 在 Partner Center 填写当前版本功能、权限和数据处理信息。
- [ ] 核查 Edge 分发包附带的 LICENSE 与仓库 `RIGHTS.md` 一致。
- [ ] 上架批准后记录首次公开日期，作为“首年免费”起算日。
- [ ] 上架前先在非生产 BC 测试环境人工验证主要功能。

## 授权权益提醒

这个 GitHub 仓库没有代码，不需要附加 MIT、GPL 或 PolyForm
源码许可证；否则容易让用户误以为整个插件已经在 GitHub 开源。

**但此前单独准备的 Edge 包已经含 PolyForm Shield 1.0.0。**
它允许在非竞争用途下部分修改与分发，保护力度不同于更严格的专有 EULA。
如果你要改变授权策略，应在 Edge 正式上传前统一确定软件许可。
