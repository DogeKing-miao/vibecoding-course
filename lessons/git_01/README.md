# git_01：Git 基础实操

## 任务

修改 `lessons/git_01/answer.md`，在每道题下面的 `bash` 代码块中填写 Git 命令，保留题号、标题和恰好 5 个答案代码块。

题目考察 clone、创建分支、add、commit 和 push。**按题目给定条件填写答案**：Q1 使用题设中的课程原仓库地址，Q2 和 Q5 使用假设用户名 `alice`。下面的实际提交流程则使用你自己的账号。

## 提交作业

完整步骤见 [课程提交说明](../../README.md)。首次提交需要先 Fork 课程仓库到自己的 GitHub 个人账号，再 clone 自己的 Fork。

实际分支必须为 `student/<你的 GitHub 用户名>/git_01`。例如，你的用户名是 `alice`：

```bash
git switch -c student/alice/git_01
# 完成答案后：
git add lessons/git_01/answer.md
git commit -m "finish git_01"
git push -u origin student/alice/git_01
```

请替换实际命令中的 `alice`。`origin` 必须指向自己的 Fork，不能推送到老师的原仓库。

在 GitHub 创建普通 PR：从你 Fork 的作业分支提交到 `Shergould/vibecoding-course` 的 `main`。无需协作者权限，也无需合并 PR。

## 修改范围和评分

- 只修改 `lessons/git_01/`，必须修改 `lessons/git_01/answer.md`。
- 不得修改 `.github/`、`grader/`、`data/` 或其他课程文件。
- 最新提交信息必须包含 `finish git_01`。
- 分支用户名、Fork 所有者和 PR 作者必须一致。

系统会在创建 PR 或其分支收到新提交后评分；草稿 PR 暂不评分，点击 **Ready for review** 后开始。定时扫描会补充处理漏掉的通知，运行可能排队。

评分检查提交的 Git 状态和答案文本。

## 查看反馈与订正

反馈在你的 PR 的 **Conversation** 评论区中，不再创建独立反馈 Issue。全部检查通过后，评论会显示 Odoo 完成密钥。

系统保留学生分支和 PR。在原分支修改后再次提交：

```bash
git add lessons/git_01/answer.md
git commit -m "finish git_01"
git push
```

保持原 PR 打开，新提交会自动进入评分。同一个 PR 的同一个提交不重复计分。
