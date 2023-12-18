# 解决 git 仓库太大的问题

### 清理

```
cd my_git
git rm --cached .
git commit -m "remove"
git push -u origin main
rm -rf .git
```

### 重建

```
git init .
git remote add origin git@github.com:<your_name>/<repo_name>.git
git add .
git commit -m "all"
git push --set-upstream origin main --force
```

### 注意

1. 通过 ```git init``` 新建的仓库默认分支可能不是 main 而是 master 
