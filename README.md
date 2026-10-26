# Vibe Coding Course

这是 Vibe Coding 课程仓库。学生通过 **Fork + Pull Request（PR）** 提交作业，评分器会在 PR 下反馈成绩。无需成为本仓库协作者，也无需配置 Token 或启用自己 Fork 中的 Actions。

当前开放课程：`git_01`。请填写 `lessons/git_01/answer.md` 中的 5 道 Git 命令题。

## 第一次提交

1. 登录 GitHub，打开 [课程仓库](https://github.com/Shergould/vibecoding-course)，点击 **Fork**，将副本创建到自己的个人账号下。
2. 把以下实际操作命令中的 `alice` 替换成自己的 GitHub 用户名：

```bash
git clone https://github.com/alice/vibecoding-course.git
cd vibecoding-course
git remote add upstream https://github.com/Shergould/vibecoding-course.git
git switch -c student/alice/git_01
```

3. 填写 `lessons/git_01/answer.md`，然后提交到自己的 Fork：

```bash
git add lessons/git_01/answer.md
git commit -m "finish git_01"
git push -u origin student/alice/git_01
```

4. 在 GitHub 打开自己的 Fork，点击 **Compare & pull request**。也可以在课程原仓库的 **Pull requests → New pull request → compare across forks** 创建 PR，确认：

| 选项                        | 内容                           |
| --------------------------- | ------------------------------ |
| base repository（目标仓库） | `Shergould/vibecoding-course`  |
| base（目标分支）            | `main`                         |
| head repository（来源仓库） | `你的用户名/vibecoding-course` |
| compare（来源分支）         | `student/你的用户名/git_01`    |

5. 标题建议填写 `git_01: 你的用户名`，点击 **Create pull request**。请提交普通 PR；草稿 PR 要点击 **Ready for review** 后才会评分。

**答案题目与实际操作要区分：** `answer.md` 是命令知识题，其中 Q1 给定原仓库地址，Q2、Q5 假设用户名是 `alice`，请按题设作答；实际提交时则使用自己的 Fork 地址和本人用户名。

## 自动评审和反馈

```text
创建 PR / 更新 PR 分支 / 重新打开 PR / 草稿转为待评审
  → 课程仓库通知 grader
  → grader 读取本次提交并评分
  → 成绩保存在 grader 仓库，反馈评论发布到该 PR
```

只在本地 commit，或只 push 到 Fork 但没有创建 PR，不会进入评分流程。无需老师合并 PR。

打开自己的 PR，在 **Conversation** 中查看评分评论，包括提交 SHA、尝试次数、得分、通过项和需要修改的内容。全部通过后，会显示 Odoo 课程完成密钥。公共仓库中的反馈评论对其他人也可见。

评分由 GitHub Actions 排队执行，不保证立即出结果；系统还有每 5 分钟配置一次的补偿扫描，实际调度可能延迟。同一个 PR 的同一个提交不会重复计分。短时间连续推送时，系统优先处理最新版本，不保证为被覆盖的中间版本分别评分。

## 订正和重新提交

**系统不会删除你的分支，也不会自动关闭或合并 PR。** 保持 PR 打开，在原分支继续修改：

```bash
git add lessons/git_01/answer.md
git commit -m "finish git_01"
git push
```

新提交会自动更新同一个 PR 并触发评分，不需要重复创建 PR。关闭 PR 后停止接收新作业评分，重新打开可以恢复。

## 同步老师的更新

`origin` 是自己的 Fork，`upstream` 是老师的课程仓库。需要同步老师更新时，在自己的作业分支执行：

```bash
git fetch upstream
git merge upstream/main
```

如有冲突，先解决冲突，再修改作业、创建包含 `finish git_01` 的提交并 push。

## 作业规则

- 来源必须是本人个人账号下的课程 Fork；分支为 `student/<本人 GitHub 用户名>/git_01`。
- PR 作者、Fork 所有者和分支中的用户名必须一致（用户名大小写不影响身份校验）。
- 最新作业 commit message 必须包含 `finish git_01`。
- 只能修改 `lessons/git_01/`，必须修改 `lessons/git_01/answer.md`。
- 不要修改 `.github/`、`grader/`、`data/` 等系统文件。
- 保留题号、标题以及恰好 5 个 `bash` 答案代码块。
