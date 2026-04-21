# GitHub Pages 发布

这个仓库已经配置了自动部署：你把文档内容 push 到 `main`，站点会自动更新。

## 需要做什么

1. 在仓库的 GitHub 设置里启用 Pages：
   - Settings → Pages
   - Build and deployment → Source 选择 **GitHub Actions**
2. 等待 Actions 跑完，打开站点链接确认生效

## 本地构建（可选）

```bash
python3 -m pip install -U mkdocs-material
mkdocs build
```
