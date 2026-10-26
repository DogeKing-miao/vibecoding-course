# git_01 answer

请在每一道题下面的 `bash` 代码块中填写你认为正确的 Git 命令。

评分脚本后续会读取本文件内容进行评分。请不要删除或修改题号、标题和代码块。

实际提交作业时使用自己的 Fork 和用户名，操作步骤见课程 README。

## Q1: clone 课程仓库

假设课程仓库地址是：

```text
https://github.com/Shergould/vibecoding-course.git
```

请写出把该仓库 clone 到本地的命令。

```bash
git clone https://github.com/Shergould/vibecoding-course.git
```

## Q2: 创建自己的 git_01 分支

假设你的 GitHub 用户名是 `alice`。

请写出创建并切换到如下分支的命令：

```text
student/alice/git_01
```

```bash
git checkout -b student/alice/git_01
```

## Q3: 暂存 answer.md

请写出把当前文件 `lessons/git_01/answer.md` 加入暂存区的命令。

```bash
git add lessons/git_01/answer.md
```

## Q4: 提交 git_01 作业

请写出创建 commit 的命令。

要求 commit message 包含：

```text
finish git_01
```

```bash
git commit -m "finish git_01"
```

## Q5: 推送自己的分支

假设当前分支是：

```text
student/alice/git_01
```

请写出把该分支推送到远程 `origin` 的命令。

```bash
git push origin student/alice/git_01
```
