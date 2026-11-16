# BC Auto Workspace

**让 Microsoft Dynamics 365 Business Central 工作区更整洁、更顺手，也更重视数据安全。**

[English](./README.md) | [简体中文](./README.zh-CN.md)

**本说明对应版本：** `2.10.13` · **状态：** Public Beta · **浏览器：** Microsoft Edge · **扩展平台：** Manifest V3

### [🧩 前往 Microsoft Edge Add-ons 官方商店安装](https://microsoftedge.microsoft.com/addons/detail/chadloeablnfjknlbgfhbbboefkemfae)

> **版本提醒：** 本 README 介绍 v2.10.13。若新版仍在微软审核或分阶段发布，Edge 商店当前提供的版本可能与文档版本不同。请以商店页面或已安装扩展显示的版本号为准。

BC Auto Workspace 是面向 **Microsoft Dynamics 365 Business Central 网页客户端** 的浏览器扩展。打开已保存的记录或单据时，它可根据配置尝试自动切换为 **View（查看）模式**、最大化工作区域、收起右侧 **FactBoxes（信息窗格）**。

扩展尽量通过 BC 原生界面控件完成操作；当页面状态或按钮识别不确定时，会优先跳过操作，避免影响未保存的数据。

## ✨ 核心功能

| 功能 | 说明 |
| --- | --- |
| **Auto View** | 对符合安全条件的已保存卡片/单据页面，尝试使用 BC 原生按钮从 Edit 切换至 View。 |
| **Auto Maximize** | 尝试使用 BC 原生布局按钮扩大工作区域。 |
| **Hide FactBoxes** | 尝试收起页面右侧的信息窗格。 |
| **总开关（Master Switch）** | 一键暂停或恢复自动操作，不删除已有配置。 |
| **Page ID 规则** | 内置 **36 条默认页面规则**，分别设置 View、Maximize 和 FactBoxes，也支持自定义。 |
| **自动识别页面** | 可尝试识别其他兼容页面，并支持排除清单。 |
| **站点授权** | 仅在用户明确授权的 Business Central 网站运行。 |
| **配置备份** | 支持自动保存偏好设置以及 JSON 导入、导出。 |
| **诊断工具** | 可复制多 Frame 技术诊断，设计目标是不包含业务字段值。 |

## 🚀 安装方法

### 方式一：Microsoft Edge 官方扩展商店（推荐）

1. 打开 [BC Auto Workspace 的 Microsoft Edge Add-ons 页面](https://microsoftedge.microsoft.com/addons/detail/chadloeablnfjknlbgfhbbboefkemfae)。
2. 点击 **获取（Get）**，确认 **添加扩展（Add extension）**。
3. 打开 **BC Auto Workspace → Website & Page Rules**。
4. 选择 **Authorize & Add Website**，添加并授权你的 Business Central 网站。
5. 根据需要启用 **Master Switch、Auto View、Auto Maximize、Hide FactBoxes**。

### 方式二：加载解压版（开发或测试）

1. 将可信的扩展 ZIP 解压到固定文件夹，确认里面直接包含 `manifest.json`。
2. 在 Edge 地址栏打开 `edge://extensions`，开启**开发人员模式**。
3. 点击**加载解压缩的扩展**，选择含 `manifest.json` 的文件夹。
4. 授权 BC 网站，并配置页面规则。

请勿让商店版和解压版同时操作同一个 BC 页面。升级、刷新或重新加载扩展前，请先保存业务数据并备份配置。

## ⚙️ 页面配置

规则按 **SO / PO / Item / Other** 分组。你可以单独开关每个 Page ID 的 View、Maximize、FactBoxes，设置自动识别排除项，并备份配置。

部分预设页面：

| BC 页面 | Page ID |
| --- | ---: |
| Item Card | `30` |
| Sales Order | `42` |
| Purchase Order | `50` |
| Customer Card | `21` |
| Purchase Price List | `7018` |
| Sales Price List | `7016` |

价格表页面采用 **ListPlus** 布局，可能包含嵌套 iframe。并非所有 BC 页面或定制界面都具有兼容的查看/最大化/FactBoxes 按钮。

## 📝 v2.10.13 更新内容

- 加强 **Purchase Price List（7018）** 与 **Sales Price List（7016）** 的 Edit/View 控件识别。
- 支持定位价格表顶部工具栏的圆圈铅笔按钮，包括位于表单内容根节点外的控件。
- 避免从 Item Card 打开价格表时，误识别页面结构中残留的旧 Item 按钮。
- 对多个冲突按钮、无关工具栏操作使用更谨慎的跳过策略，增加 `priceModeSearch` 诊断。
- 保留新建记录、未保存修改和用户主动进入 Edit 模式时的保护逻辑。

## 🛡️ 安全设计与权限

BC Auto Workspace 只是**界面便利工具**，不能代替 BC 权限集、AL 业务验证或审批流程来限制编辑权限。

扩展设计为**不会自动保存、过账、删除或修改业务记录**，也不会替用户确认放弃未保存数据、修改导航 URL 或自动刷新页面。识别不确定时，可能不执行操作。

Manifest V3 权限用途：

| 权限 | 用途 |
| --- | --- |
| `storage` | 保存用户设置、授权网站和页面规则。 |
| `scripting` | 在已授权 BC 页面及允许的 Frame 中运行工作区逻辑。 |
| `activeTab` | 用户操作扩展时访问当前标签页。 |
| `webNavigation` | 跟踪支持的 BC 页面与 iframe 导航。 |
| 可选 HTTP(S) 站点访问权限 | 仅在用户同意后用于配置的 Business Central 网站。 |

## 🧪 测试及限制

v2.10.13 已通过 **16/16 项本地模拟 Chromium 浏览器回归测试**，覆盖价格表工具栏、旧 Item 页面干扰、多个候选按钮、嵌套 iframe 和未保存数据保护。

**这些测试不代表已在真实 Business Central 租户完成端到端验收。** BC 界面版本、语言和自定义布局可能影响效果；建议先在非生产环境验证。

若 Auto View 不生效，请确认记录已保存、总开关与页面规则已启用、BC 网站获得授权，再通过插件的 **Copy multi-frame diagnostics** 复制不含业务字段值的技术诊断。

## ☕ 请我喝杯咖啡

如果 BC Auto Workspace 帮你节省了一些重复点击的时间，也欢迎请开发者喝杯咖啡，支持后续维护与改进。**赞赏完全自愿，不影响插件的安装或使用。**

**微信赞赏码 — Sun liuyang**（点击可查看原图）：

<p align="center">
  <a href="./assets/wechat-donate.png"><img src="./assets/wechat-donate.png" alt="Sun liuyang 微信赞赏码" width="420"></a>
</p>

感谢每一份支持，让 Business Central 的日常工作再轻松一点。💛

## 👤 开发者与许可

**开发者：** Jovi Sun  
**联系邮箱：** jsu@novencogroup.com  
**当前状态：** Public Beta

现有扩展安装包未附带明确的开源许可文件；若准备开放源码供他人复用，请在 GitHub 仓库补充 `LICENSE`，明确授权条款。

*BC Auto Workspace 是独立开发的浏览器工具，并非微软官方产品。*
