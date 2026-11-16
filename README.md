# BC Auto Workspace

**A safer, cleaner workspace for Microsoft Dynamics 365 Business Central.**

[English](./README.md) | [简体中文](./README.zh-CN.md)

**Documented version:** `2.10.13` · **Status:** Public Beta · **Browser:** Microsoft Edge · **Extension platform:** Manifest V3

### [🧩 Install from Microsoft Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/chadloeablnfjknlbgfhbbboefkemfae)

> **Version note:** This README documents v2.10.13. The version available in the Edge Add-ons store may differ while an update is undergoing certification or rollout. Check the store listing or your installed extension to confirm its version.

BC Auto Workspace helps organize the **Microsoft Dynamics 365 Business Central web client** when you open existing records and documents. It can switch eligible saved pages to **View mode**, expand the working area, and collapse **FactBoxes** through Business Central's own controls.

The extension prioritizes preserving unsaved work. When it cannot confidently identify a control or page state, it is designed to skip the action instead of guessing.

## ✨ Features

| Feature | What it does |
| --- | --- |
| **Auto View** | Attempts to switch eligible, previously saved record/document pages from Edit to View using the native BC mode control. |
| **Auto Maximize** | Attempts to expand the current page using BC's native workspace control. |
| **Hide FactBoxes** | Attempts to collapse the right-side information pane. |
| **Master Switch** | Pauses or resumes automation without deleting saved settings. |
| **Page Rules** | Includes **36 preset Page ID rules**, with separate View, Maximize, and FactBoxes settings; custom rules are supported. |
| **Auto Detection** | Attempts to recognize additional compatible BC pages, with configurable exclusions. |
| **Site Authorization** | Runs only on Business Central websites that you explicitly authorize. |
| **Settings Backup** | Saves preferences and supports JSON import/export. |
| **Diagnostics** | Provides multi-frame technical diagnostics designed to omit business field values. |

## 🚀 Installation

### Option A — Microsoft Edge Add-ons (recommended)

1. Open the [official BC Auto Workspace listing on Microsoft Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/chadloeablnfjknlbgfhbbboefkemfae).
2. Select **Get** and confirm **Add extension**.
3. Open **BC Auto Workspace → Website & Page Rules**.
4. Choose **Authorize & Add Website** for your Business Central web client, then approve the requested site access.
5. Enable the **Master Switch** and configure **Auto View**, **Auto Maximize**, and **Hide FactBoxes** as desired.

### Option B — Load an unpacked build (development/testing)

1. Extract a trusted extension package into a permanent local folder containing `manifest.json`.
2. In Edge, open `edge://extensions` and enable **Developer mode**.
3. Choose **Load unpacked** and select the folder containing `manifest.json`.
4. Authorize your Business Central website and configure the page rules.

Do not run both the store build and an unpacked build against the same BC page. Back up your settings and save any unfinished BC work before upgrading or reloading an extension.

## ⚙️ Configuration and page support

The settings organize page rules into **SO / PO / Item / Other** groups. You can configure each supported page separately, exclude pages from auto-detection, and export/import your preferences.

Some preset examples:

| Business Central page | Page ID |
| --- | ---: |
| Item Card | `30` |
| Sales Order | `42` |
| Purchase Order | `50` |
| Customer Card | `21` |
| Purchase Price List | `7018` |
| Sales Price List | `7016` |

The price-list pages use a **ListPlus** layout and may include nested frames. Not every BC page or customized interface exposes compatible View/Maximize/FactBoxes controls.

## 📝 What's new in v2.10.13

- Improved **Purchase Price List (7018)** and **Sales Price List (7016)** mode-button detection.
- Added targeted recognition of circled pencil controls in a page's upper toolbar, including controls outside the form content root.
- Reduced interference from old **Item Card** controls left in the DOM when a price list opens from an item.
- Added safer handling of ambiguous or unrelated toolbar actions, with additional `priceModeSearch` diagnostics.
- Preserved existing controls for unsaved changes, new records, and deliberate manual editing.

## 🛡️ Safety and permissions

BC Auto Workspace is a **UI convenience tool**, not an editing permission or access-control system. Use BC permission sets, validation, and approval workflows to enforce business rules.

The extension is designed **not** to save, post, delete, or change business records automatically, confirm discard dialogs, alter navigation URLs, or reload pages. It may skip actions where it cannot establish a safe state.

Its Manifest V3 permissions have these purposes:

| Permission | Purpose |
| --- | --- |
| `storage` | Save preferences, authorized-site configuration, and page rules. |
| `scripting` | Run the workspace logic on authorized BC pages and permitted frames. |
| `activeTab` | Work with the active tab when you interact with the extension. |
| `webNavigation` | Track supported BC page and frame navigation. |
| Optional HTTP(S) site access | Requested with your consent for configured Business Central websites. |

## 🧪 Testing and known limitations

**v2.10.13 passed 16/16 local synthetic Chromium browser regression cases**, including price-list toolbar behavior, old Item Card overlays, ambiguous controls, nested frames, and unsaved-work protection.

These tests **do not** constitute end-to-end validation in a real Business Central tenant. UI customization, localization, and tenant/browser differences can affect the results. Test in a non-production environment before broad deployment.

If Auto View does not work, confirm that the record is saved, the page rule and Master Switch are enabled, and the website is authorized. Use **Copy multi-frame diagnostics** in the popup to capture technical status without copying business field values.

## ☕ Buy me a coffee

If BC Auto Workspace saves you time, you're welcome to support its continued development with a coffee. **Support is entirely optional** and is not required to use the extension.

**WeChat appreciation code — Sun liuyang** (click for the full-size image):

<p align="center">
  <a href="./assets/wechat-donate.png"><img src="./assets/wechat-donate.png" alt="WeChat appreciation QR code for Sun liuyang" width="420"></a>
</p>

Thank you for supporting small tools that make everyday Business Central work a little easier. 💛

## 👤 Developer and license

**Developer:** Jovi Sun  
**Status:** Public Beta

No explicit open-source license is included in the supplied extension package. If this repository is intended for open-source reuse, add a `LICENSE` file specifying the terms.

*BC Auto Workspace is an independent browser utility and is not an official Microsoft product.*
