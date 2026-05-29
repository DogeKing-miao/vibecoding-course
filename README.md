# Vibe Coding Course

这是 Vibe Coding 课程的学生代码仓库。

## 仓库职责

本仓库用于：

1. 存放课程任务说明和学生需要完成的代码文件。
2. 让学生在自己的分支上完成每节课实操。
3. 作为自动评审系统读取学生提交结果的来源。
4. 让学生在本仓库查看评审反馈，例如 commit status 或反馈 Issue。

本仓库不负责保存最终成绩，不保存评分密钥，也不保存隐藏测试。

## 当前阶段

当前只测试一个 lesson：

```text
git_01
```

该 lesson 用于测试学生对 Git 基础操作的掌握情况。

## 学生分支规则

每个学生需要创建自己的分支：

```text
student/<github_username>/git_01
```

示例：

```text
student/alice/git_01
student/bob/git_01
```

## 学生操作流程

学生需要执行类似流程：

```bash
git clone https://github.com/Shergould/vibecoding-course.git
cd vibecoding-course
git checkout -b student/alice/git_01
# 按课程要求完成 git_01 任务
git add .
git commit -m "finish git_01"
git push origin student/alice/git_01
```

其中：

- `alice` 替换成学生自己的 GitHub 用户名。
- commit message 必须包含 `finish git_01`。
- 学生只能在自己的分支上提交。

## git_01 评审目标

第一版自动评审不检查学生本地实际敲过哪些 Git 命令，而是检查学生最终提交出来的 Git 状态是否符合要求。

评审内容包括：

1. 分支名是否符合 `student/<github_username>/git_01`。
2. 是否提交了指定 lesson 的内容。
3. 是否没有修改禁止修改的系统文件。
4. commit message 是否包含 `finish git_01`。
5. 任务文件是否填写了有效内容。

## 结果反馈

评审由另一个仓库 `vibecoding-grader` 完成。

学生不需要向 `vibecoding-grader` 提交内容。

评审结果会尽量反馈回本仓库，例如：

1. 学生 commit 页面中的 passed/failed 状态。
2. 本仓库中的反馈 Issue。

## 与 Odoo 的关系

Odoo 在线学习页面只放本仓库链接和操作说明。

Odoo 不负责：

1. 接收学生代码。
2. 执行自动评审。
3. 保存成绩。
4. 校验密钥。

第一阶段的核心链路是：

```text
Odoo 课程页面
  -> 学生进入本 GitHub 仓库
  -> 学生创建自己的分支并提交
  -> vibecoding-grader 自动评审
  -> 评审结果反馈回本仓库
```

