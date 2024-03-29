# TestGit
Just for test git project and what happen will be.  
Record some command or url.  

## Command
Record some command.  

### git stash

```Shell Session
git stash save 'stash 1'
git stash list
git pull
git stash pop 'stash@{0}'
```
>[Pull後被覆蓋？](https://ithelp.ithome.com.tw/articles/10188789)

### git pull origin master

`git pull origin master --rebase`
>[Git: 四種將分支與主線同步的方法](https://cythilya.github.io/2018/06/19/git-merge-branch-into-master/)

##### Undoing a git pull --rebase.
`git checkout -b after-commit HEAD@{1} # or the commit you want to recover`
>[Undoing a git pull --rebase](https://stackoverflow.com/questions/2213235/undoing-a-git-pull-rebase)

### git rebase
```
git rebase --skip => 作 git rebase 時，如果發生 conflict，選擇放棄 {branch_name_2} 的 patch 

git rebase --abort => 作 git rebase 時，如果發生 conflict，選擇回到原本的 branch 並放棄此 rebase 及其修改 

git rebase -i reference~# => 在本機端，透過編輯器 (vi) 重新挑選、排列、修改、分離、結合…，在 reference~# 之後的所有 commit 內容 
```
>[git 指令 ](http://silverwind1982.pixnet.net/blog/post/286048390-git-%E6%8C%87%E4%BB%A4)

### git tree graph
```
git log --graph --oneline --all
git log --graph --pretty=oneline --abbrev-commit
```
>[Unable to show a Git tree in terminal](https://stackoverflow.com/questions/1064361/unable-to-show-a-git-tree-in-terminal)  
>[Git 基礎 - 檢視提交的歷史記錄](https://git-scm.com/book/zh-tw/v2/Git-%E5%9F%BA%E7%A4%8E-%E6%AA%A2%E8%A6%96%E6%8F%90%E4%BA%A4%E7%9A%84%E6%AD%B7%E5%8F%B2%E8%A8%98%E9%8C%84)

### git archive
```
git diff --name-status $(git merge-base master HEAD) HEAD | awk '{ if ($1 != "D") printf("\"%s\"\n", substr($0,3)) }' | xargs git archive --format=zip -o output.zip HEAD --
```

>[Git. How to create archive with files, that have been changed?](https://stackoverflow.com/questions/7226009/git-how-to-create-archive-with-files-that-have-been-changed)


### Others

```
git log

git merge-base master HEAD
git diff --name-only master #檢查目前有哪些file被更改過
git diff --name-status master #類似以上
git diff --name-only HEAD $(git merge-base master HEAD)

git show [xxxx] --name-only #查看該commit有哪些file被更改過
git blame file_path #檢查該檔案每一行是誰寫的

git cherry -v #查看未傳送到remote的提交描述/說明
git log master ^origin/master #查看未傳送到remote的提交詳情
```
