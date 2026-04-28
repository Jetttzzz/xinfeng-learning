# Git进阶学习笔记

## 模块一：冲突解决

### 冲突标记理解
- `<<<<<<< HEAD` - 当前分支内容开始
- `=======` - 分隔线
- `>>>>>>> branch-name` - 合并分支内容结束

### 冲突解决步骤
1. `git status` 查看冲突文件
2. 打开冲突文件，找到冲突标记
3. 手动编辑，保留需要的内容
4. 删除冲突标记
5. `git add <file>` 标记为已解决
6. `git commit` 完成合并

### 本次冲突解决
- main分支修改：main分支的内容
- conflict-branch修改：conflict-branch分支的内容
- 最终保留：合并了两边的修改

---

## 模块二：git log/diff 查看历史和差异


### git log 常用命令

### git log 常用格式

| 命令 | 说明 |
|------|------|
| `git log` | 完整历史 |
| `git log --oneline` | 简洁单行 |
| `git log -n` | 最近n条 |
| `git log --graph` | 图形化分支 |
| `git log --author="name"` | 按作者筛选 |
| `git log --since="2024-01-01"` | 按时间筛选 |

### git diff 常用命令

| 命令 | 说明 |
|------|------|
| `git diff` | 工作区 vs 暂存区 |
| `git diff --staged` | 暂存区 vs 最新提交 |
| `git diff HEAD` | 工作区 vs 最新提交 |
| `git diff commit1 commit2` | 两个提交比较 |
| `git diff --stat` | 统计变更 |

---

## 模块三：git revert/reset 回滚操作

这是一个错误的提交，需要回滚
