# YC-VR — 词汇复习网站（部署仓库）

> 高中英语词汇复习 Web 应用，纯前端，GitHub Pages 托管。
>
> **在线访问：https://cattiewish.github.io/YCVR-web/**

---

## 功能板块

- **课标3K**：高中课标附录词汇的选词填空与词义匹配（2400+ 题），支持全随机与按首字母定向出题
- **每周积累**：以每周词汇复习材料为单位的选词填空与词义匹配，支持多选周期定向出题，附复习材料在线浏览
- **随机挑战**：混合题型限时 60 秒，90% 正确率解锁小游戏
- **Gaming English**：游戏主题英语阅读（筹备中）

## 技术说明

- 纯 HTML/CSS/JS，无框架、无构建、无后端
- `index.html` 按需 `fetch()` 加载 `data/` 目录的 JSON 数据
- 本仓库是**部署仓库**：内容来自主工作仓库的 `docs/` 目录，经 `git subtree push` 同步，推送即部署；请勿直接在本仓库修改

## 数据说明

- 课标 3K 题库/词库按首字母拆分为 `data/cloze_*.json` 与 `data/pools_*.json`
- 每周积累按周拆分：`weekly_index.json` + `pools_weekly_XXXX.json` + `cloze_weekly_XXXX.json` + `weekly_XXXX.md`
- 词汇以美式拼写为准，干扰项由前端从词池动态抽取，不预生成
