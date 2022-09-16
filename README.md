# git-first


一个知识点的第一篇文章, 尽量呈现简单, 完整, 准确的例子, 下面是80%的时间都在使用的git命令

## 安装
```
git: https://git-scm.com/downloads
vscode: https://code.visualstudio.com/download
```

## 配置
``` shell
git config --global branch.autosetuprebase always
git config --global pull.rebase true
```


## 一次完整的提交
场景: 新创建一个commit
``` bash
git add .
git commit -m "first commit"
git push origin main
```

## amend
场景: 修补上一个commit, 不会新创建commit
``` bash
git add .
git commit --amend --no-edit
git push origin main -f
```

## reset
场景1: 将最新的多个commit,合并成一个
``` bash
# git reset xxx, xxx表示某个commit的hashid
git reset xxx
git add .
git commit -m "xxx"
git push origin main -f
```

场景2: 移除某个commit之后的代码
``` bash
# git reset --hard xxx
git reset --hard xxx
git push origin main -f
```

