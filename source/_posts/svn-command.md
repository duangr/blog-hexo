---
title: SVN常用命令
date: 2016-07-12 09:58:53
tags:
- svn
---
# 前言
记录svn命令行的常用命令.

# 功能场景
在没有图形化工具的条件下使用SVN.

# 具体案例

* 迁出
svn checkout (co) path

* 更新
svn update (up) -r m PATH

* 添加
svn add file
svn status |awk '{if($1 == "?"){print $2}}'|xargs svn add

* 删除
svn delete (del,remove,rm) PATH

* 提交
svn commit (ci) -m "log msg" [--no-unlock] PATH

* 加解锁
svn lock -m "lock msg" [--force] PATH
svn unlock PATH

* 查看状态
svn status PATH
```
?：不在svn的控制中；
M：内容被修改；
C：发生冲突；
A：预定加入到版本库；
K：被锁定
```

* 查看状态
svn status -v path
第一列保持相同，第二列显示工作版本号，第三和第四列显示最后一次修改的版本号和修改人

* 查看日志
svn log PATH

* 查看文件详细信息
svn info PATH

* 对比
svn diff PATH (修改文件与基础版本比较)
svn diff -r m:n PATH (版本m与版本n比较)

* 合并
svn merge -r m:n PATH (将版本m到版本n之间的差异合并到当前文件)

* 还原
svn revert PATH

* 解决冲突
svn resolved PATH (移除冲突标识)

# 参考资料
