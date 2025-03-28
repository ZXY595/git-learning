# git-learning

Let's learn git!

* 任务1：署名

1. 给github账户添加ssh key：由于github的最新规定，给项目推送提交现在推荐ssh认证，步骤如下：[本地生成ssh key](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)，[将生成的ssh key添加到github](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)。
2. 克隆仓库：将项目仓库以ssh形式拷贝到本地
3. 本地修改：在本地修改ASSIGNEES.txt，把自己的昵称加邮箱加入
4. 本地暂存修改：以送快递为例，暂存修改就是先把你的修改放在快递箱子里，但是不封装箱子和贴快递信息，这有助于你有选择性地送出你最希望送出的修改，在本地仓库根目录输入命令：

   ```bash
   git add .
   ```

   其中 "." 表示暂存当前目录下的所有修改
5. 本地提交：本地提交就是给当前暂存区的修改加上封条和快递信息（提交信息），在提交之后，暂存区的修改会和提交信息等一起成为一次提交，提交之后只能通过回溯（之后再说）才能回到提交之前的状态，这里特别说明是本地提交，是因为此时提交（快递）只是堆积在本地（家里），在推送提交之前，别人是不知道你有提交的，所以你也可以本地多次提交，最后一起推送出去，在本地仓库根目录输入命令：

   ```bash
   git commit -m "xxx"
   ```

   其中 "-m" 表示message, 即提交信息，"xxx" 就是你的提交（快递）的信息
6. 推送提交：在本地仓库根目录输入命令：

   ```bash
   git push
   ```

   应该会返回错误，因为你对main分支没有修改权限
7. 查看最近的提交日志，得到commit-hash（前 7 位）

   ```bash
   git log --oneline
   ```
8. 根据最近的提交创建并切换分支

   ```bash
   git branch "分支名" <commit-hash>
   git push
   ```
9. 创建pull request (pr)

---

* 任务2：issue
