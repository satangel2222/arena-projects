# arena-projects

每个项目 = **一个子文件夹 + `projects.json` 里一行**。

```
arena-projects/
├── index.html          ← 画廊页（读取 projects.json 渲染）
├── projects.json       ← 项目清单
├── _template-project.json
└── <project-id>/
    └── index.html      ← 该项目的入口，线上地址 https://<user>.github.io/arena-projects/<project-id>/
```

## 新增一个项目
1. 把项目文件夹拷进来（必须含 `index.html`）
2. 复制 `_template-project.json`，填好，粘进 `projects.json` 数组
3. push

## 删除一个项目
1. 删掉 `<project-id>/` 整个文件夹
2. 从 `projects.json` 删掉那一行
3. push —— 该路径立刻 404，其它项目不受影响

> 注意：删项目 = 删文件，**不需要 `delete_repo` 权限**，也不会碰仓库本身。
