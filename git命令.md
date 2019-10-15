### git命令

--------------------------------------

1. git clone 你的仓库地址         [复制远程仓库至本地 ] 
2. git clone 你的仓库地址 你的仓库别名        
3. git log         [查看仓库的提交信息]  
4. git log -p    [查看所有的具体改动]
5. git log --stat  [查看文件改变]
6. git status        [查看当前仓库的状态，哪些未被标记，哪些未被提交]
7. git add 文件路径/文件名         [添加未被追踪的文件至追踪暂存区中]
8. git add .      [将全部改动添加到暂存区]
9. git reset head 文件名/文件路径        [将暂存区中的追踪文件改成不追踪]
10. git commit -m'提交日志说明'         [添加暂存区的文件至本地仓库中]
11. git push              [将本地仓库的commit提交至远程仓库]
12. git branch 分支名称          [创建一个本地分支]
13. git checkout 分支名称             [切换至某个分支]
14. git checkout -b 分支名称       [创建并切换至某个分支]
15. git branch -d 分支名称       [删除某个分支,必须要切换至其他分支,才能删除当前分支]
16. git branch -D 分支名称         [强制删除某个分支]
17. git push origin -d 分支名称     [删除某个远程分支]
18. git push origin 分支名称        [将本地分支推送至服务器仓库]
19. git push origin 分支名称 -f          [忽略冲突,强制push至远端分支]
20. git merge 分支名称     [将分支合并至当前分支上]
21. git merge --abort      [取消分支合并]
22. git show          [查看当前commit的内容]
23. git show SHA-1          [查看具体的某个SHA-1码的改动]
24. git diff --cached/--staged      [查看所有的add,如果你立即输入 `git commit`，你将会提交什么 ]
25. git rebase  目标基础点      [将当前的父commit点改成目标基础点的commit]
26. git commit --amend        [修改上一次的commit,并生成新的commit]
27. git rebase -i SHA-1    [修改某个commit,之后需要使用git rebase --continue]
28. git reset --hard         [撤销最新的修改]
29. git revert HEAD^     [撤销上次的提交]
30. git stash -u        get checkout master    git checkout 分支名  git stash pop  [保存当前分支的状态,切换回其他分支做工作,再切换回来,进行恢复]
31. git checkout c08de9a          git checkout -b branch1    [找回被删除的分支,并创建]
32. git log 分支1..分支2     [查看分支2比分支1多提交了什么]
33. git log 分支1...分支2    [查看分支1与分支2的不同]

34. git config --global --unset credential.helper 重置密码
35. git本地推送至git
    * git init
    * git add -A
    * git commit -m'init'
    * git remote add origin git仓库地址
    * git push -u origin master
36.  git remote set-url origin 新ssh/https地址 将当前的地址替换为新地址

