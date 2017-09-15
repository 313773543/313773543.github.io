---
title: How to update ruby from version 2.0.0 to 2.4.0 on Mac?
date: 2017-09-12 10:41:46
tag: [ruby,tech]
categories: dailylearning
---

## 如何将macOS上Ruby从2.0.0升级到2.4.0
### 第一步: 安装[RVM](https://rvm.io/)
```bash
\curl -sSL https://get.rvm.io | bash -s stable
```
当你安装完成（如果遇到问题请查看rvm链接），需要重启终端(terminal)方可使用rvm．可以通过如下命令查询目前rvm包含不同版本的ruby．
```bash
rvm list known
```

### 第二步：使用[RVM](https://rvm.io/)安装Ruby
使用如下命令进行新版本Ruby安装
```bash
rvm install ruby-2.4.1
```
使用如下检查Ruby版本
```bash
ruby -v
```
目前Ruby版本应该为2.0.0
### 第三步：通过RVM切换Ruby版本
通过如下命令切换Ruby版本
```bash
rvm use ruby-2.4.1
```
如果想将其设置为默认(default)版本的
```bash
rvm use ruby-2.4.1 --default
```

至此mac上的Ruby版本修改完毕．