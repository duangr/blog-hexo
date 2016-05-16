----
title: git guide
----

## 配置

### 全局配置

查看
```
less ~/.gitconfig
```
修改
```
git config --global user.name "duangr"
git config --global user.email "duangr@qq.com"
```


常用别名

```
git config --global alias.st status
git config --global alias.ci commit
git config --global alias.co checkout
git config --global alias.br branch
```
### 局部配置

查看
```
less .git/config
```

修改
```
git config user.name "duangr"
git config user.email duangr@qq.com
```

### 会话配置
