# 千禧衣橱（dressup）— AI 协作说明

> 放在每个项目仓库根目录，ZCode/Codex 等工具会自动读取。每次开工前先读这份文件。

## 这是什么项目
一句话：给 Maya 做一个复刻 4399/7K7K 经典 Flash 换装体验的千禧甜美风纸娃娃换装小游戏（自由换装 + 3 章主题挑战评分）。
当前阶段：MVP

## 运行方式
- 启动命令：无构建，直接用浏览器打开 `index.html`（单 HTML 零依赖）
- 线上地址：Cloudflare Pages（见 decisions D4）；GitHub 仓库 mayaxuuu-creator/dressup

## 项目规矩
- 技术栈（不要擅自更换）：单 HTML 文件零依赖；角色与服饰全部为**内嵌 SVG 矢量**（D2，勿改用位图/生图素材）
- 改动前先读 `decisions.md`：已定决策不得重新翻案，除非 Maya 明确同意
- 评分公式与内容数据严格按 `docs/换装游戏机制文档-v2.md` 与 `docs/换装游戏内容配置包-v1.md`，改规则先改文档再改代码
- 完成一个功能块即 git commit（中文 message，说人话）
- 重代码改动完成后 → 触发跨模型审查协议（见 `~/.zcode/workspace/default/infra/cross-model-review/`）
- Maya 是完全 vibe coding：用产品语言汇报，技术取舍讲清楚影响

## 已知坑
- macOS BSD cp：源路径带尾斜杠会把目录内容摊平（见 MAYA_PROFILE 教训库）
- 单品 SVG 必须在 500×750 画布坐标系内作画，对齐责任在画布纪律，程序不做缩放位移换算

## 关联文档
- 设计文档：`docs/换装游戏机制文档-v2.md`、`docs/换装游戏内容配置包-v1.md`
- 决策日志：`decisions.md`
- Maya 偏好档案：`/Users/mayaxu/.zcode/workspace/default/MAYA_PROFILE.md`
