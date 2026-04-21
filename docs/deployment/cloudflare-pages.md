# Cloudflare Pages 部署

MkDocs 构建出的站点是纯静态文件（默认输出到 `site/`），非常适合 Cloudflare Pages。

## 1) 在 Cloudflare Pages 创建项目

1. 进入 Cloudflare Dashboard → Pages
2. 选择 **Connect to Git**
3. 绑定 GitHub 并选择仓库 `Rodert/shiyu-sub2api`
4. 选择要部署的分支（一般是 `main`）

## 2) Build 配置（推荐）

- **Framework preset**：None
- **Build command**：

```bash
python3 -m pip install -U pip mkdocs-material && python3 -m mkdocs build --strict
```

- **Build output directory**：`site`

## 3) 图片与视频的建议

- **图片**：直接放 `docs/assets/` 或场景目录的 `assets/`，用相对路径引用即可
- **视频**：建议外链托管后嵌入（更快、更省仓库体积）；如果一定要放 mp4，请控制体积并注意仓库历史会变大

## 4) 访问路径（可选）

如果你后续需要部署到子路径（不是根域名），再在 `mkdocs.yml` 增加 `site_url`，并按你的实际域名调整即可。
