# 使用指南

本页介绍如何在本项目中编写和维护文档。

## 1. 目录结构

```text
my-docs/
├── docs/                  # 存放 Markdown 文档
│   ├── index.md           # 主页
│   ├── about.md           # 关于页面
│   ├── guide.md           # 使用指南（本页）
│   └── api.md             # API 参考
├── .github/
│   └── workflows/
│       └── deploy.yml     # 自动化部署工作流配置
├── mkdocs.yml             # MkDocs 配置文件
└── README.md              # 项目说明
```

## 2. 新增页面

1. 在 `docs/` 目录下新建一个 `.md` 文件，例如 `notes.md`
2. 在 `mkdocs.yml` 的 `nav` 中添加导航项：

```yaml
nav:
  - 主页: index.md
  - 使用指南: guide.md
  - API 参考: api.md
  - 笔记: notes.md
  - 关于: about.md
```

## 3. 常用 Markdown 语法

| 语法 | 效果 |
| --- | --- |
| `# 标题` | 一级标题 |
| `**加粗**` | **加粗** |
| `*斜体*` | *斜体* |
| `` `代码` `` | 行内代码 |
| `- 列表` | 无序列表 |

代码块示例：

```python
def hello():
    print("Hello, MkDocs!")
```

## 4. 本地预览

```bash
pip install mkdocs
mkdocs serve
```

然后在浏览器打开 <http://127.0.0.1:8000> 实时预览。

## 5. 发布

推送到 `main` 分支后，GitHub Actions 会自动完成构建和部署，无需手动操作。
