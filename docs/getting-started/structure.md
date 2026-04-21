# 约定与目录结构

这套仓库按「场景」来组织教程，方便你扩展维护。

## 推荐结构

```text
.
├─ mkdocs.yml
└─ docs/
   ├─ index.md
   ├─ assets/
   ├─ getting-started/
   ├─ scenarios/
   │  └─ ccswitch/
   ├─ deployment/
   └─ faq/
```

## 场景写法（建议模板）

每个场景一个目录，至少包含：

- `index.md`：这个场景要解决什么问题、适用人群、前置条件
- `step-01-*.md` ～ `step-0n-*.md`：可执行步骤（每页尽量只做一件事）
- `troubleshooting.md`：现象 → 原因 → 解决

## 资源文件（图片/视频）

- **图片**：推荐放 `docs/assets/`，也可以放在场景目录下的 `assets/`（便于场景自包含）
- **视频**：推荐外链（平台/对象存储/Release），文档里嵌入；不建议直接把大文件放进仓库
