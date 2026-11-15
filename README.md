# BC Auto Workspace

**A cleaner, more predictable workspace for Microsoft Dynamics 365 Business Central.**

[English](#english) · [简体中文](#简体中文)

> **Public Beta · Full-featured free release · No account or license key required**  
> An independent Microsoft Edge extension by **Jovi Sun**.  
> **Documentation-only repository:** the extension's source code is not published here.

---

## English

### Overview

**BC Auto Workspace** is a Microsoft Edge browser extension designed to make everyday work in **Microsoft Dynamics 365 Business Central (BC)** more convenient.

When an existing Card or Document page can be recognized safely, the extension attempts to switch it to **View mode**, expand the workspace, and collapse the **FactBox** pane according to your preferences.

It is designed to reduce repetitive interface clicks—not to replace Business Central security controls.

### Key features

- **Auto View:** Attempt to open eligible, existing Cards and Documents in View mode when the page state can be safely determined.
- **Auto maximize:** Use Business Central's existing controls to switch to a wider workspace layout.
- **Hide FactBoxes:** Collapse the right-hand FactBox pane when a safe, supported control is found.
- **32 preset Page ID rules:** Includes commonly used Card, Document, and production-order pages.
- **Unlimited custom Page IDs:** Customize rules for additional standard or customized BC pages.
- **Automatic page detection:** Supports compatible Cards opened from Lists and supported, authorized iframe contexts.
- **Master ON/OFF switch:** Pause or resume all automatic actions without deleting your saved page rules.
- **Online and on-premises:** Configure and authorize your own Business Central website.

### Designed with safety in mind

BC Auto Workspace is cautious about unsaved and new records. It is designed **not to**:

- Automatically save, post, release, delete, or change business records.
- Automatically refresh a Business Central page or rewrite its URL to force View mode.
- Dismiss unsaved-changes or leave-page confirmation dialogs.
- Override a user's deliberate choice to edit an existing record.

If an interface control cannot be identified reliably, the extension may skip the action.

**Important:** View mode is a user-interface convenience, **not a permission or access-control mechanism**. Editing rights remain governed by Business Central permissions, business rules, and approvals.

### Free-first release policy

The plan is to provide **all existing functionality free for the first 12 months starting on the date of the extension's first public release on Microsoft Edge Add-ons**.

- No credit card or payment information.
- No registration, license key, subscription, or trial application.
- No three-Page-ID cap or 72-hour trial timer.
- The current version does **not automatically expire or lock itself** at the end of the first year.

After that period, the developer may evaluate whether optional paid features or enterprise services are worthwhile, based on real usage and maintenance costs. **No pricing or conversion to a paid version has been decided.** Material changes will be communicated in advance.

**First public Edge Add-ons release date:** _To be announced after publication._

### Installation

**Recommended:** Install from the official **Microsoft Edge Add-ons** listing. The verified store link will be added here after publication.

After installation:

1. Open the extension's **Options / Settings** page.
2. Add your Business Central website and grant the requested site permission.
3. Choose your Auto View, maximize, FactBox and Page ID preferences.
4. Open an existing BC Card or Document to try the workflow.

For best results, start with non-production or demo records when evaluating a new extension.

**Current interface language:** Primarily Simplified Chinese. An English interface is under consideration.

### Privacy

The extension processes Business Central interface state on sites you explicitly authorize and saves preferences locally in your browser.

The current public-beta version has **no developer-operated account server, payment collection, analytics SDK, advertisement SDK, or remote license-check service**. Its extension code does not upload BC record contents to the developer.

See [Privacy Policy](PRIVACY.md) for the full explanation.

### Support and feedback

Bug reports and compatibility feedback are welcome through **GitHub Issues** once this repository is published. Please do not post real BC tenant addresses, confidential records, customer details, or access credentials.

This is an independently maintained project offered on a **best-effort** basis. No 24/7 help desk, guaranteed SLA, or custom enterprise development is included.

See [Support](SUPPORT.md) and [Release Notes](CHANGELOG.md).

### Source code and rights

This GitHub repository contains **product information and documentation only**. It does **not** provide the browser extension source code, downloadable extension binaries, or an open-source software license.

The extension is distributed through the official Edge Add-ons channel under the license terms included with its distribution package. Publishing documentation here grants **no additional rights** to repackage, imitate, or redistribute the extension beyond those terms.

BC Auto Workspace is an independent third-party project and is **not affiliated with, sponsored by, or endorsed by Microsoft**. Microsoft, Microsoft Edge, Dynamics 365, and Business Central are trademarks of their respective owners.

**© 2026 Jovi Sun. All rights reserved, to the extent of the publisher's established rights.**

---

## 简体中文

### 产品介绍

**BC Auto Workspace** 是一款专为 **Microsoft Dynamics 365 Business Central（BC）** 网页客户端设计的 **Microsoft Edge 浏览器扩展**。

在能够安全识别已有 Card / Document 页面状态时，扩展会根据用户设置尝试自动切换到 **View 查看模式**、扩大工作区，并收起右侧 **FactBoxes** 信息面板。

它的目标是减少日常重复点击，提高操作便利性，**并非代替 BC 的后台权限管理**。

### 主要功能

- **Auto View：** 对可安全识别的已有 Card / Document 页面，尝试自动切换至 View。
- **Auto maximize：** 使用 BC 原生按钮，尝试切换至更宽的工作区布局。
- **Hide FactBoxes：** 在控件状态明确时，尝试收起右侧信息面板。
- **32 个预设 Page ID：** 包含常见业务 Card、Document 和生产工单相关页面。
- **无限自定义 Page ID：** 支持按需添加、修改标准页面和定制页面规则。
- **自动识别页面：** 兼容从 List 打开的部分 Card，以及获得授权的 iframe 场景。
- **插件总开关：** 一键暂停或恢复自动操作，不清除保存的网站与页面规则。
- **BC Online / On-Premises：** 用户自行添加并授权需要使用的 BC 网站。

### 注重业务操作安全

插件设计上不会：

- 自动保存、过账、发布、删除或修改业务记录。
- 为了切换 View 而自动刷新 BC 页面或强制修改 URL。
- 自动确认放弃未保存更改、离开页面等提示。
- 覆盖用户主动进入 Edit 编辑模式的操作意图。

如果页面控件无法可靠识别，插件可能选择跳过操作。

**重要：** View 是界面便利功能，不是权限控制。真正的业务权限仍需要通过 Business Central 权限集、业务规则或审批实现。

### 首年免费计划

计划从插件**首次在 Microsoft Edge Add-ons 商店公开上架之日**起，连续 **12 个月免费开放全部现有功能**。

- 无需信用卡或支付资料。
- 无需注册账号、输入 License Key 或购买订阅。
- 没有免费版 3 个 Page ID 限制。
- 没有 72 小时试用计时器。
- **当前版本没有一年后自动锁定、自动收费的机制。**

第一年结束后，开发者会结合真实用户需求、兼容性问题和维护投入，评估是否推出可选的收费功能或企业服务。**目前没有确定收费计划和价格**，重大变化会提前公布。

**首次公开上架日期：** _正式上架后更新。_

### 安装方法

建议通过官方 **Microsoft Edge Add-ons 扩展商店** 安装。上架通过后，会在这里补充真实的商店链接。

安装后：

1. 打开插件的 **Options / 设置** 页面。
2. 添加并授权你使用的 Business Central 网站。
3. 配置 Auto View、最大化、FactBoxes 和 Page ID 规则。
4. 在已有 BC Card / Document 页面中验证效果。

首次使用建议先在测试环境或演示数据中体验。

**当前界面语言：** 主要为简体中文，英文界面将在未来评估。

### 隐私保护

扩展只在用户明确授权的 BC 网站中处理相关界面状态，并将配置保存在浏览器本地。

当前免费版本**没有开发者运营的账户服务器、付款收集、分析 SDK、广告 SDK 或远程 License 验证服务**，插件代码不会向开发者上传 BC 业务记录内容。

详细说明见 [隐私政策](PRIVACY.md)。

### 用户支持与反馈

欢迎通过本仓库的 **GitHub Issues** 提交问题和兼容性反馈。请勿在公开反馈中粘贴真实 BC 租户地址、客户信息、订单数据、密码或访问凭证。

这是由个人独立维护的项目，采用**尽力维护**方式，不提供 7×24 小时服务、固定响应时限或企业级 SLA。

参见 [支持说明](SUPPORT.md) 和 [更新记录](CHANGELOG.md)。

### 源代码与版权

这个 GitHub 仓库**仅公开产品介绍和相关文档**，不公开插件源代码、不提供插件安装包，也不通过该仓库授予开源软件许可证。

插件通过微软官方 Edge 商店分发，实际软件使用和再分发权益以该安装包附带的授权条款为准。公开产品文档**不会额外授予**复制、重新打包或发行插件的权利。

BC Auto Workspace 是独立第三方产品，**并非微软官方产品，也未获得微软赞助或背书**。相关商标归各自权利人所有。

**© 2026 Jovi Sun。保留依法享有的全部权利。**
