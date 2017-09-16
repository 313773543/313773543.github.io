---
title: How to squash multiple commits into one?
date: 2017-09-13 17:26:32
tag: [git,linux,tech,squash]
categories: [Paranoid, Web]
---

### 如何合并多个commit到一个commit呢？[参考][http://www.jianshu.com/p/964de879904a]

#### 第一步:  找到需要合并的commit前面的一个

  使用命令git log找到需要合并的所有commit前面的那个commit，记下前六个字符．如下图想合并前两个commit,则查找得到2629fb.

![A snapshot of it](/img/gitLog003.png)

#### 第二步：编辑之前的commit

  使用如下命令编辑之前的commit

```bash
git rebase -i 2629fb
```

结果如下图所示．

![A snapshot of it](/img/gitRebase003.png)

#### 第三步：编辑git rebase打开的文件

  修改上一步打开的文件编辑页面，将第一个pick行后面行的pick改为squash．pick意味着使用此commit,squash意味着将从commit与上面的commit合并．如下图所示（超过两行的同理）．

![A snapshot of it](/img/gitRebaseModify003.png)

#### 第四步：修改commit的评论信息

  保存上一步的编辑文件页面，就会打开一个重新编辑commit评论信息的编辑文件页面．修改评论信息，保存即可应用此次修改．

![A snapshot of it](/img/gitRebaseModifyComment003.png)





[http://www.jianshu.com/p/964de879904a]: http://www.jianshu.com/p/964de879904a