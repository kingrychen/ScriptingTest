从柳星  https://github.com/S1ngS1ng/ScriptingTest.git fork 之后
以我余虹君为例子  https://github.com/yuhjun/ScriptingTest.git
1. git clone 余虹君
2. 进入bower.json 所在项目 打开git bash  使用bower install 安装包文件
3. 同步柳星改过的GIT  参考 http://www.tuicool.com/articles/6vayqen

Github上fork之后如何保持同步(Windows环境)

1. `git remote -v`
2. `git remote add upstream 柳星`
结果：
origin: https://github.com/yuhjun/ScriptingTest.git (fetch)
origin: https://github.com/yuhjun/ScriptingTest.git (push)
upstream: https://github.com/S1ngS1ng/ScriptingTest.git (fetch)
upstream: https://github.com/S1ngS1ng/ScriptingTest.git (push)
3. `git fetch upstream`
4. `git checkout master`

-----
使用git rebase是有条件的, 你的本地仓库要“足够干净”. 可以用git status命令查看当前改动:
`git status`
结果:
On branch master
Your branch is ahead of 'origin/master' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working directory clean

`git pull --rebase upstream master`
结果：
From https://github.com/S1ngS1ng/ScriptingTest
 \* branch   master  ->  FETCH_HEAD
Current branch master is up to date.

至此我的本地项目已经于原作者项目同步了

同步完成后 推送到自己的Github上:
`git push origin master`