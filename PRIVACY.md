# Privacy Policy / 隐私政策

**Product / 产品：** BC Auto Workspace  
**Publisher / 发布者：** Jovi Sun (independent developer / 个人独立开发者)  
**Effective date / 生效日期：** To be updated at official publication / 正式上架时填写  
**Contact / 联系：** GitHub Issues or the official Edge Add-ons support contact / GitHub Issues 或 Edge 商店公开联系方式

## English

### Scope

BC Auto Workspace operates on Microsoft Dynamics 365 Business Central
websites that the user explicitly adds and authorizes.

To perform the requested functions, it processes locally:
page URLs and routing context, Page IDs, visible Card/List controls,
layout state, and temporary record identity needed to avoid unsafe
operations.

### Locally stored information

The extension stores user-selected website rules, Page IDs, enabled/disabled
switches, auto-detection settings, and advanced compatibility preferences
in the browser's local extension storage (`chrome.storage.local`).

It may temporarily process page content in memory when identifying
interface controls. It does not use this information to build an external
user profile.

### Network and external services

This free version contains no developer-operated account system,
payment collection, advertising or analytics SDK, or remote license
verification service. Its extension code does **not upload Business
Central business record contents to the developer**.

Microsoft Edge and Business Central may process data as part of their
own normal services, under their respective privacy terms.

### Permissions and controls

`storage` saves preferences; `scripting` interacts with BC controls
on user-authorized sites; `webNavigation` handles navigation and frames;
`activeTab` supports the currently selected tab. The optional HTTP/HTTPS
site permissions allow the user to approve their specific BC website,
including on-premises installations.

Users can pause automation via the master switch, change individual
settings, remove authorized sites, or uninstall the extension.

### Updates

The policy will be updated before future account, analytics, payment,
or remote-license features—if any—are introduced.

## 简体中文

### 适用范围

BC Auto Workspace 只在用户主动添加并授权的 Microsoft Dynamics 365
Business Central 网站上运行。

为完成页面自动操作，插件会在浏览器本地处理页面 URL 与路由状态、
Page ID、可见的 Card/List 界面控件、布局状态，以及必要的临时
记录识别信息。

### 本地保存的信息

插件使用浏览器本地扩展存储（`chrome.storage.local`）保存用户设置的
BC 网站、Page ID 规则、总开关、独立功能设置、自动识别设置和高级兼容配置。

插件可能在运行期间临时读取相关页面界面状态，以便识别控件，
但不会用这些内容建立云端用户档案。

### 网络和第三方服务

当前免费版没有开发者运营的账户系统、付款收集、广告或分析 SDK，
也没有远程 License 验证服务器。**插件代码不会向开发者上传
Business Central 的业务记录内容。**

Edge 浏览器和 Business Central 自身的正常服务遵循各自的隐私政策。

### 权限和用户控制

`storage` 用于保存本地偏好；`scripting` 用于处理用户授权 BC 网站的
界面控件；`webNavigation` 用于识别导航与 iframe；`activeTab`
用于当前活动页面。HTTP/HTTPS 可选站点权限仅用于用户主动授权
自己使用的 BC 网站，包括本地部署环境。

用户可以通过总开关暂停自动操作、修改独立功能选项、移除网站授权，
或直接卸载扩展。

### 政策更新

如未来新增账户、分析、支付或远程授权功能，将在启用前更新本隐私说明。

---

**Note / 提醒：** The publisher should verify the accuracy of this policy
against the final submitted extension and add a real effective date and
contact channel before publishing.  
发布前请核实本政策与最终 Edge 版本完全一致，补充真实生效日期及联系方式。
