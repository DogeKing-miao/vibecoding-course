# Vibe Coding Course

这是 Vibe Coding 课程代码仓库。学生只需要在本仓库完成作业并 push，系统会自动通知 grader 仓库评分，并把结果反馈到本仓库的 Issue。

## 当前开放课程

```text
git_01
```

`git_01` 用于考察 Git 基础操作。你需要在：

```text
lessons/git_01/answer.md
```

中填写 5 道 Git 命令题。

## 第一次提交

请把下面示例中的 `alice` 替换成你的 GitHub 用户名。

```bash
git clone https://github.com/Shergould/vibecoding-course.git
cd vibecoding-course
git checkout -b student/alice/git_01
```

然后修改：

```text
lessons/git_01/answer.md
```

修改完成后提交并 push：

```bash
git add lessons/git_01/answer.md
git commit -m "finish git_01"
git push origin student/alice/git_01
```

## 自动评审流程

你 push 到 `student/**` 分支后，本仓库会自动通知 grader 仓库评分：

```text
学生 push student/alice/git_01
  -> course 仓库触发 notify-grader workflow
  -> grader 仓库开始评分
  -> grader 在本仓库 Issue 中追加反馈
  -> grader 删除远程学生分支
```

通常反馈会在较短时间内出现。如果没有立刻出现，可以稍等一会儿后刷新 Issues 页面。

## 查看反馈

评分完成后，系统会在本仓库创建或更新一个反馈 Issue：

```text
[Feedback] <你的 GitHub 用户名> git_01
```

例如：

```text
[Feedback] alice git_01
```

每次提交都会在同一个 Issue 下面追加一条新评论，评论中会显示：

1. 第几次提交。
2. 本次得分。
3. 已通过的检查项。
4. 需要修改的题目或规则。
5. 如果全部正确，会显示 Odoo 课程完成密钥。

## 重新提交

评分完成后，系统会删除 GitHub 上的远程分支：

```text
origin/student/<你的 GitHub 用户名>/git_01
```

这不会删除你电脑上的本地分支。你可以继续在本地分支上修改，然后重新 push，注意保持同一课程多次提交本地分支名一致即可：

```bash
git add lessons/git_01/answer.md
git commit -m "finish git_01"
git push origin student/alice/git_01
```

远程分支会重新创建，系统会把这次 push 记录为下一次提交，并继续在同一个反馈 Issue 中追加评论。

## 同步 main

如果老师更新了 `main` 分支，建议先同步再继续做题，因此建议每次做题前先进行同步：

```bash
git fetch origin
git merge origin/main
```

如果出现冲突，请先解决冲突，再继续提交。

## 重要规则

- 分支名必须是 `student/<你的 GitHub 用户名>/git_01`。
- commit message 必须包含 `finish git_01`。
- 只修改 `lessons/git_01/` 目录。
- 不要修改 `.github/`、`grader/`、`data/` 等系统目录。
- 不要删除或修改 `answer.md` 中的题号、标题和代码块结构。
- 只有 5 道题全部正确时，反馈 Issue 中才会显示 Odoo 完成密钥。
