# 参与指南

这个仓库只有一个用途：让你把“给别人的仓库提交一次改动并被合并”的完整流程亲手走一遍。下面是全部步骤，每一步在《Git 零基础入门教程》的《实战三：参与开源项目 + 课程总结》里都有展开讲解。

## 你要做的

1. **Fork**：点仓库页右上角的 Fork，把这个仓库复制到你自己的账号下。
2. **克隆你的 Fork**：`git clone https://github.com/你的用户名/git-practice.git`，然后 `cd git-practice`。
3. **加上 upstream**：`git remote add upstream https://github.com/Cranes249i/git-practice.git`，再 `git fetch upstream`。
4. **开一条分支**：`git switch -c 修正错别字`（分支名可以自己起）。不要直接在 main 上改。
5. **改一处**：把 README.md 第 3 行的“说名”改成“说明”。只改这一处，不要顺手重排别的内容。
6. **提交并推到你的 Fork**：`git add README.md`、`git commit -m "修正 README 里的错别字：说名→说明"`、`git push -u origin 修正错别字`。
7. **向这里开 PR**：回到 GitHub，点 Compare & pull request；确认 base repository 是 `Cranes249i/git-practice`、head repository 是你的 Fork。描述里写三件事：改了什么、为什么、怎么验证。
8. **等待审查并回应**：课程方会在 PR 里留意见，通常会请你把名字加进 README 的“参与者”一节。在同一条分支上改、提交、`git push`，PR 会自动更新，不要开新的 PR。
9. **被合并之后**：`git switch main`、`git fetch upstream`、`git merge upstream/main`、`git push`，再删掉工作分支：`git push origin --delete 修正错别字`、`git branch -d 修正错别字`。

## 可选：用 PR 关闭一个 Issue

先到 Issues 里开一个 Issue（比如“把我的名字加进 README 的参与者一节”），记下编号；然后在提交说明或 PR 描述里写一行 `Fixes #编号`。PR 合并后，这个 Issue 会被自动关闭。

## 几条约定

- 改动小而明确：一个 PR 只做练习内容里的事。
- 提交说明和 PR 描述用中文即可，写清“改了什么、为什么、怎么验证”。
- 审查意见是练习的一部分，不是挑错；按意见改完再推就好。
- 任何人都可以开 Issue 和 PR；这里没有会被弄坏的东西。

## 给课程方的维护说明

- 每合并一个练习 PR 后，把 README.md 第 3 行的“说明”改回“说名”，下一位读者才有东西可改；“参与者”一节里的名字保留。
- 审查时统一用 Request changes 请读者补第 2 条（如果还没做），再 Approve，并用 Merge commit 合并。