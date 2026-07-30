# 三角洲行动 · 攻略中心（菜单式）

一个纯前端的《三角洲行动》攻略网页，打开即见「攻略目录」（类似外卖点单），点进去查看具体内容；内含高价值物品图鉴。

## 🔗 在线访问

**https://jingsiwangshi.github.io/delta-force-guide/**

- 手机 / 电脑浏览器直接打开即可，无需安装任何东西。
- 顶部有搜索框，可快速过滤攻略；左上角「⌂ 目录」随时返回首页。

## 📑 站点包含的板块

1. 游戏概览
2. 模式详解（全面战场 / 危险行动 / 战役）
3. 干员图鉴
4. 武器与改枪
5. 地图攻略
6. 战术技巧
7. 撤离生存指南
8. 高价值物品图鉴（含 AI 风格化示意图）
9. 新手误区
10. 常见问题 FAQ

## 🗂 本地文件结构

```
.
├── index.html            # 主入口（菜单式单页应用）
└── assets/
    ├── hero.mp4          # 首页背景视频（AI 生成战术氛围片段）
    └── items/            # 高价值物品图鉴图片（5 张 AI 生成 + 1 张内联 SVG）
        ├── heart.png     # 非洲之心（传说）
        ├── mandel.png    # 曼德尔砖（特殊）
        ├── gold.png      # 纯金金条
        ├── watch.png     # 奢华名表
        └── keycard.png   # 门禁卡 / 情报硬盘
```

> 说明：图鉴中的物品图片为 AI 风格化示意，**非游戏实机素材**；干员技能、武器数值、地图点位会随官方版本变动，请以游戏内为准。

## 🚀 本地预览

直接用浏览器打开 `index.html` 即可（需保持 `assets/` 目录在同层级）。
若想用本地服务器：

```bash
python -m http.server 8077
# 然后访问 http://127.0.0.1:8077/
```

## 🔄 更新内容

修改本地 `index.html` / `assets/` 后，重新运行部署脚本即可发布到 GitHub Pages：

```bash
python deploy_ghpages.py <your_github_pat> delta-force-guide
```

> 部署脚本走 GitHub 官方 API（建仓库 → 上传文件 → 开启 Pages）。
> 注意：`deploy_ghpages.py` 与 `.workbuddy/` 等为本项目工作文件，部署时仅上传 `index.html` 与 `assets/`。
