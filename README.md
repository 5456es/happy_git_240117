# happy_git_240117
Git learning use 



---

## 1.17 简单总结

https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners

#### 本地

- **git init** : initialize the git repo

- 一开始的分支默认为master

- git checkout -b <new-branch-name>： 用来创建新分支

- git add . 将内容加入缓冲区   git commit -m 'xxx' 提交

- remote代表了存储于本地的，关于远程仓库的内容。 remote下面可以有多个远程仓库，一般默认的使用origin。

  - 此处-u代表了upstream绑定

  ```
  git remote add origin https://github.com/cubeton/mynewrepository.git
  git push -u origin master
  ```

- git fetch只把远程更新内容记录在remote中，pull则在记录后还进行merge。

```
git checkout -b local-branch-name origin/remote-branch-name

这个命令创建了一个新的本地分支 local-branch-name 并切换到该分支。与此同时，它会将这个新建分支与远程分支 origin/remote-branch-name 关联起来。

这种关联是通过在新建分支上设置一个 "upstream" 或者 "tracking" 的关系来实现的。这意味着在以后的 git pull 操作时，Git 会自动将远程分支的更新合并到本地分支中。你可以简单地运行 git pull，而不需要显式指定远程和分支，因为关联关系已经被设置。

所以，运行上述命令后，你可以方便地在新建分支上进行开发，并通过 git pull 来获取和合并远程分支的更新。

```

