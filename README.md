# BetterChrome

> **Language:** [English](#) | [简体中文](#)

---

## Introduction

BetterChrome aims to enhance Google Chrome by adding new features without modifying the Chromium core. This approach allows us to retain Google Sync services and minimize development overhead. While custom Chromium builds might offer flexibility, they come with significant challenges like high server costs and complex updates. Similarly, customized browsers like Edge or 360 Extreme Browser provide unique features but often lock users into their ecosystems. BetterChrome focuses on adding these useful features directly to Chrome through extensions and userscripts, despite the restrictions imposed by Google.

### Future Plans
1. **Compact UI Layout Similar to Safari:**
   Chrome's address bar, bookmark bar, and tab bar take up too much vertical space. A compact, combined layout like Safari's would be ideal. Unfortunately, this may not be achievable solely through extensions due to Chrome's limitations.
![image](https://github.com/user-attachments/assets/869222f0-a2f6-475c-b2e9-562837096bad)
On 13"/11" notebooks it's a great vertical space save
2. **Live Text and Real-Time OCR/Translation:**
   Inspired by Safari's Live Text feature, this would enable real-time text recognition and translation on images. For reference, see the author's prototype project leveraging macOS's built-in OCR:
   [ChromeLivetext](https://github.com/louishino/ChromeLivetext)
![image](https://github.com/user-attachments/assets/679f51e1-0280-4c04-b881-e29b3c95a90d)
0. **Enhance Bookmark Bar Logic: Open Bookmarks and Address Bar Searches in New Tabs by Default**
   In most cases, when we open a bookmarked webpage from the bookmark bar or perform a search using the address bar, we prefer these actions to open in a new tab rather than overwrite the current one. This helps preserve the original page and avoids accidental content loss.
   However, Chrome still doesn’t offer a default option for opening bookmarks or address bar searches in new tabs.
   To address this, we’ve implemented this functionality using BetterTouchTool. The solution leverages macOS APIs to detect mouse pointer hover information. Under specific conditions, the left mouse button is remapped to act as the middle button—making it especially convenient for users without a middle mouse button or those who’d rather not hold the Command key.
   The specific condition is:
hovered_element_details CONTAINS "AXRoleDescription: \"Bookmark Button\""

3. **Customizable Visual Styles (Boost Feature from Arc Browser):**
   A visual CSS customization feature to adjust website appearances. For example, users could modify overly decorative fonts or busy background colors to suit their preferences.
![image](https://github.com/user-attachments/assets/0dd25334-7046-47b0-afa7-cf1bf08ad132)

4. **Disable "Exit Full Screen" Reminder:**
   Chrome's mandatory "Press ESC to exit full screen" prompt can be intrusive. A feature to display this warning only once would greatly improve the experience.

---

## 项目介绍

BetterChrome 旨在为 Google Chrome 添加新功能，而不是基于 Chromium 进行定制开发。通过这种方式，我们可以保留谷歌同步服务并减少开发成本。尽管魔改 Chromium 内核灵活性更高，但会带来高昂的服务器维护费用和复杂的更新流程。同样，像 Edge 或 360 极速浏览器这样的定制版 Chrome 虽然功能独特，但往往将用户绑定到特定的生态系统。BetterChrome 专注于通过扩展插件和油猴脚本为原版 Chrome 添加实用功能，即使受到谷歌的诸多限制。

### 未来计划
1. **紧凑式 UI 布局（类似 Safari）：**
   Chrome 的地址栏、书签栏和标签栏占用了太多垂直空间。我们希望实现类似 Safari 的紧凑布局，将地址栏和标签栏合并，但由于 Chrome 的限制，仅靠扩展可能无法完成。
![image](https://github.com/user-attachments/assets/869222f0-a2f6-475c-b2e9-562837096bad)
On 13"/11" notebooks it's a great vertical space save
2. **实时文本识别与翻译功能：**
   受 Safari 的 Live Text 功能启发，计划实现实时文本 OCR 识别与翻译功能。以下是作者基于 macOS 自带 OCR 开发的原型项目：
   [ChromeLivetext](https://github.com/louishino/ChromeLivetext)
   [ChromeLivetext](https://github.com/louishino/ChromeLivetext)
![image](https://github.com/user-attachments/assets/679f51e1-0280-4c04-b881-e29b3c95a90d)
0. **改进书签栏逻辑：默认点击书签在新标签页打开,默认在新标签页打开地址框搜索的内容**
   在大多数情况下，我们打开书签栏内的收藏网页或通过地址栏搜索内容时，会希望在新标签页中打开，而不是直接覆盖当前网页。这样可以保留原有网页，避免内容丢失。然而，Chrome 至今未提供默认在新标签页打开书签和地址栏搜索结果的选项。
   因此，我们通过 BetterTouchTool 实现了这个功能，其原理是利用 macOS 提供的 API 来检测鼠标指针的悬停信息。在满足特定条件的情况下，将鼠标左键映射为中键（对于没有中键或不想按下 Command 键的用户特别友好）。
   具体条件如下：
   hovered_element_details CONTAINS "AXRoleDescription: \"书签按钮\""
4. **可视化样式自定义功能（借鉴 Arc 浏览器的 Boost 功能）：**
   用户可以通过可视化工具自定义网页的 CSS 样式。例如，更改过于花哨的字体或繁杂的背景颜色，以优化阅读体验。
![image](https://github.com/user-attachments/assets/0dd25334-7046-47b0-afa7-cf1bf08ad132)
5. **关闭全屏提醒：**
   每次切换到全屏模式时，Chrome 都会强制显示“按 ESC 退出全屏”的提示。虽然这是一个安全提醒，但谷歌未提供仅显示一次的选项，这让人感到非常烦恼。

---

Let’s work together to make Chrome even better!

