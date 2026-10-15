# 关于本站

- 文档工具：MkDocs
- 自动部署：GitHub Actions
- 托管平台：GitHub Pages

## 工作原理

```text
编写 Markdown → git push → GitHub Actions 构建 → 发布到 GitHub Pages
```

1. 在 `docs/` 目录下编写 Markdown 文档
2. 推送到仓库的 `main` 分支
3. GitHub Actions 工作流（`.github/workflows/deploy.yml`）自动执行 `mkdocs gh-deploy`
4. 构建产物发布到 `gh-pages` 分支，由 GitHub Pages 对外提供访问
