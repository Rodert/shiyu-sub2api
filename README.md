# shiyu-sub2api
仕宇的 sub2api 教程

## 这是什么

一个「场景化」的 sub2api 教程仓库：左侧边栏按场景分栏（例如与 `ccswitch` 的整合），每个场景下面用 Step 页面把过程写成可复现的操作步骤。

## 本地预览

```bash
python3 -m pip install -U mkdocs-material
python3 -m mkdocs serve
```


## 写新教程（推荐流程）

1. 在 `docs/scenarios/<tool>/` 新建目录与页面（参考 `docs/scenarios/ccswitch/`）
2. 在 `mkdocs.yml` 的 `nav:` 里把侧边栏加上对应条目

## 发布到 GitHub Pages

仓库已包含 GitHub Actions 工作流（见 `.github/workflows/pages.yml`）。

你需要在 GitHub 仓库设置里启用：

- Settings → Pages → Source 选择 **GitHub Actions**

之后 push 到 `main` 会自动构建并部署站点。

## 用 Cloudflare Pages 部署（可选）

也可以用 Cloudflare Pages 托管静态站点：

- Build command：`python3 -m pip install -U pip mkdocs-material && python3 -m mkdocs build --strict`
- Output directory：`site`

详见文档页：`docs/deployment/cloudflare-pages.md`
