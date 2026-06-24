# git_01: Git 基础实操

## 任务

请修改本目录下的：

```text
answer.md
```

在每一道题下面的 `bash` 代码块中填写对应 Git 命令。不要删除题号、标题或代码块。

## 考察内容

本节课主要考察：

1. 使用 `git clone` 克隆课程仓库。
2. 使用 `git checkout -b` 或等价命令创建并切换分支。
3. 使用 `git add` 暂存指定文件。
4. 使用 `git commit` 创建提交。
5. 使用 `git push` 推送自己的分支。

## 分支要求

分支名必须是：

```text
student/<你的 GitHub 用户名>/git_01
```

例如 GitHub 用户名是 `alice`，分支名就是：

```text
student/alice/git_01
```

## 提交要求

commit message 必须包含：

```text
finish git_01
```

建议命令：

```bash
git add lessons/git_01/answer.md
git commit -m "finish git_01"
git push origin student/<你的 GitHub 用户名>/git_01
```

## 修改范围

只能修改：

```text
lessons/git_01/
```

不要修改：

```text
.github/
grader/
data/
```

## 自动评审

你 push 到 GitHub 后，本仓库会自动通知 grader 仓库评分。评分脚本会读取：

```text
lessons/git_01/answer.md
```

并检查 5 个 `bash` 代码块是否符合要求。

只有全部检查正确，系统才会在反馈 Issue 中显示 Odoo 课程完成密钥。

## 反馈位置

评分结果会出现在本仓库 Issues 中，标题格式为：

```text
[Feedback] <你的 GitHub 用户名> git_01
```

每次提交都会在同一个 Issue 中追加一条新评论。请根据评论中的错误提示修改后重新提交。

## 远程分支会被删除

评分完成后，系统会删除 GitHub 上的远程分支，但不会删除你的本地分支。

如果你要重新提交，继续在本地分支修改并 push 即可：

```bash
git add lessons/git_01/answer.md
git commit -m "finish git_01"
git push origin student/<你的 GitHub 用户名>/git_01
```
