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

### Others

```
git log 
git diff --name-only master #檢查目前有哪些file被更改過
git blame file_path #檢查該檔案每一行是誰寫的
```
