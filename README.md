# My Docs

基于 **MkDocs + GitHub Actions + GitHub Pages** 的个人文档站。

## 目录结构

```text
my-docs/
├── docs/                  # 存放 Markdown 文档
│   ├── index.md           # 主页
│   ├── about.md           # 关于页面
│   ├── guide.md           # 使用指南
│   └── api.md             # API 参考
├── .github/
│   └── workflows/
│       └── deploy.yml     # 自动化部署工作流配置
├── mkdocs.yml             # MkDocs 配置文件
└── README.md              # 项目说明（本文件）
```

## 使用方法

### 本地预览

```bash
pip install mkdocs
mkdocs serve
```

浏览器访问 <http://127.0.0.1:8000>。

### 自动部署

推送到 `main` 分支后，GitHub Actions 自动构建并发布到 GitHub Pages。
