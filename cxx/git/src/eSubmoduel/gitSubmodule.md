# git submodule

随着项目会越来越多，常常需要提取一个公共的类库提供给多个项目使用，两者是一个依赖另一个的关系。



## CRUD

### create

``` bash
git submodule add <仓库地址> <本地路径> # clone 仓库地址作为submodule到本地。
git submodule add ssh://git@10.2.237.56:23/dennis/sub.git lib
# 添加成功后，在父仓库根目录自动增加了.gitmodule文件。
# .git/config文件会追加 [submodule "lib"]。内容为 url = ssh://git@10.2.237.56:23/dennis/sub.git

git submodule init
git submodule update 

```



``` ini
[submodule "my_proj"]
	path = proj
	url = https://github.com/abc/my_proj
```



### read

``` bash
git submodule foreach git pull
cd .. & git commit # 更新commit id
```

### update

先改子项目，再更新父项目。
 git submodule update --init --recursive 

### clone



``` bash

git clone --recurse-submodules <main_project_url>  # 获取主项目和所有子项目源码

git submodule init
git submodule update
git submodule update -- arepos # 可以指定路径更新仓库，空仓库会执行git clone

```



### delete

``` bash

rm -rf sm_path  # 删除子模块目录及源码
vim .gitmodules # 删除项目目录下.gitmodules文件中子模块相关条目
vim .git/config # 删除配置项中子模块相关条目
rm .git/module/* # 删除模块下的子模块目录，每个子模块对应一个目录
git rm --cached 子模块名称 # 清理错误
```
``` bash
SYNOPSIS
git submodule [--quiet] add [<options>] [--] <repository> [<path>]
git submodule [--quiet] status [--cached] [--recursive] [--] [<path>…?]
git submodule [--quiet] init [--] [<path>…?]
git submodule [--quiet] deinit [-f|--force] (--all|[--] <path>…?)
git submodule [--quiet] update [<options>] [--] [<path>…?]
git submodule [--quiet] summary [<options>] [--] [<path>…?]
git submodule [--quiet] foreach [--recursive] <command>
git submodule [--quiet] sync [--recursive] [--] [<path>…?]
git submodule [--quiet] absorbgitdirs [--] [<path>…?]
```

