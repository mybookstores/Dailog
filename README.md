# Dailog · 日报工具

一个精致、零依赖的日常工作日报管理工具，单文件即可运行，数据完全本地存储。

[![Online](https://img.shields.io/badge/在线使用-mybookstores.github.io/Dailog-brightgreen)](https://mybookstores.github.io/Dailog/) ![HTML5](https://img.shields.io/badge/单文件-HTML5-orange) ![localStorage](https://img.shields.io/badge/数据-localStorage-blue) ![Chart.js](https://img.shields.io/badge/图表-Chart.js-purple)

---

## ✨ 功能亮点

| 模块 | 说明 |
|------|------|
| **✏️ 填写日报** | 结构化填写「今日完成 / 明日计划 / 风险阻塞 / 想法讨论」，支持标签分类 |
| **📋 历史时间线** | 按时间倒序展示所有日报，卡片式布局，一目了然 |
| **📊 周报总览** | 本周完成趋势柱状图（Chart.js）、每日填报状态网格、核心指标统计 |
| **📤 导出** | 实时 Markdown 预览，一键下载 `.md` 文件或复制到剪贴板 |
| **💾 草稿保存** | 手动保存草稿，刷新不丢失；提交后自动清除 |
| **🔁 昨日预填** | 新建日报时自动填入昨日内容（项目 + 明日计划），减少重复输入 |
| **🔥 连续记录** | Hero 区域展示连续填报天数、总日报数、总完成项数 |

---

## 🚀 在线使用

**直接访问 GitHub Pages：**
👉 https://mybookstores.github.io/Dailog/

或下载 `index.html` 到本地，双击用浏览器打开即可（无需服务器）。

> ⚠️ 注意：`Inter` 字体通过 Google Fonts CDN 加载，完全离线使用时会 fallback 到系统字体，不影响功能。

---

## 📁 项目结构

```
.
├── index.html            # 主文件（单文件，含 HTML/CSS/JS）
├── README.md              # 本文档
└── .workbuddy/            # WorkBuddy 项目数据（可忽略）
```

---

## 🛠️ 技术栈

- **前端**：原生 HTML5 + CSS3 + JavaScript（ES6+），零框架依赖
- **图表**：[Chart.js 4.4.7](https://www.chartjs.org/)（CDN 引入）
- **字体**：Inter（Google Fonts CDN）
- **存储**：localStorage，key 为 `wb_daily_v6`（草稿 `wb_draft_v6`）
- **风格**：冷淡精致风，CSS 变量驱动，支持 Retina 高清渲染

---

## 📖 使用说明

### 填写日报
1. 选择所属项目（risk-model-context / riskai / riskgraph / riskgaia / 其他）
2. 在四个板块中填写内容，每项一行
3. 点击标签进行归类（开发 / 测试 / 联调 / 部署 / 文档 / 会议 / Code Review / 其他）
4. 「保存草稿」暂存，「提交日报」写入本地数据

### 查看历史
- 切换到「历史」标签页，所有日报以时间线卡片展示
- 支持查看「今日完成 / 明日计划 / 风险阻塞 / 想法讨论」及标签

### 周报总览
- 统计本周完成任务数、涉及项目数、有想法的天数、有阻塞的天数
- 柱状图展示每日完成趋势，今日柱高亮
- 每周网格直观显示填报状态（实心 = 已填报，空心 = 未填报）

### 导出
- 切换到「导出」标签页，自动生成 Markdown 格式预览
- 点击「导出 .md」下载文件，或「复制」到剪贴板

---

## 🔧 自定义

### 修改项目选项
编辑 HTML 中 `id="project-select"` 的 `<select>` 元素。

### 修改标签选项
编辑 `id="tag-pills"` 下的 `<span class="tag">` 元素。

### 清除所有数据
在浏览器控制台执行：
```js
localStorage.removeItem('wb_daily_v6')
localStorage.removeItem('wb_draft_v6')
location.reload()
```

---

## 📦 本地开发

```bash
# 克隆仓库
git clone https://github.com/mybookstores/Dailog.git
cd Dailog

# 本地预览（解决 CDN 字体加载问题）
npx serve .
```

---

## 📝 License

MIT License — 自由使用、修改和分发。

---

## 🙋 关于

由 [陈静茹](https://github.com/chenjingru) 开发，用于日常工作中高效记录和管理日报。

如有问题或建议，欢迎提 Issue ✨
