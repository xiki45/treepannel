# TreePannel - 树状导航站

一个轻量级的个人导航站，使用纯静态 HTML + JSON 数据驱动，支持多级树状折叠浏览。

## 在线访问

https://treepannel.vercel.app

## 结构

```
├── index.html   # 导航页面（纯 HTML/CSS/JS，无框架依赖）
└── tree.json    # 导航数据（嵌套 JSON，支持无限层级）
```

## 数据格式

`tree.json` 为嵌套数组结构，每个节点包含 `name`、可选的 `url` 和可选的 `children`：

```json
[
  {
    "name": "分类名",
    "children": [
      { "name": "站点名", "url": "https://example.com" }
    ]
  }
]
```

没有 `url` 的节点会渲染为可折叠的文件夹，有 `url` 的渲染为可点击的链接。

## 更新导航

编辑 `tree.json` 后推送到 main 分支，Vercel 会自动重新部署。

## 部署

通过 GitHub 仓库关联 Vercel 自动部署，无需构建步骤。
