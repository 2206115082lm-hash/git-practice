# git-practice

Git 练习仓库，用于记录和实验 Git 的常用工作流。

## 目录结构

```
.
├── README.md      # 本文件
└── .gitignore     # 忽略规则
```

## 常用命令速查

### 初始化与提交

```bash
git init                      # 初始化仓库
git add <file>                # 暂存指定文件
git add .                     # 暂存所有变更
git commit -m "message"       # 提交
git status                    # 查看当前状态
git log --oneline --graph     # 查看提交历史
```

### 分支

```bash
git branch                    # 列出本地分支
git switch -c feature/x       # 新建并切换到 feature/x
git switch main               # 切回 main
git merge feature/x           # 合并 feature/x 到当前分支
git branch -d feature/x       # 删除已合并的分支
```

### 远程协作

```bash
git remote -v                 # 查看远程地址
git push -u origin main       # 首次推送并建立追踪关系
git push                      # 后续推送
git pull --rebase             # 拉取并变基
git fetch --prune             # 拉取并清理已删除的远程分支
```

### 撤销与回退

```bash
git restore <file>            # 丢弃工作区改动
git restore --staged <file>   # 取消暂存
git commit --amend            # 修改最近一次提交
git reset --soft HEAD~1       # 撤销最近一次提交，保留改动
git revert <commit>           # 生成一次反向提交（安全回退）
```

## 提交信息规范

采用 Conventional Commits：

| 前缀 | 含义 |
| --- | --- |
| `feat:` | 新功能 |
| `fix:` | 修复缺陷 |
| `docs:` | 文档变更 |
| `refactor:` | 重构 |
| `chore:` | 构建/工具链调整 |

示例：`feat: add branch cleanup script`

## 许可证

未指定。
