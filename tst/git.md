## Git
#### git 命令
```
touch index.txt  //创建文件 
git status //查看状态
git add index.txt //添加index.txt 到暂存区
git add -A   //添加所有文件到暂存区
git commit -m "first" //添加备注信息到版本库  如果想进入编辑模式可以i键进入插入模式 i表示编辑 esc + :wq 退出
git log //查看版本库信息
mkdir git // 创建git文件夹
git init // 初始化git（会创建git隐藏文件夹）
echo hello >> index.txt  //在index.txt中添加写入“hello”
cat index.txt //查看index.txt
clear 清屏
```

> master --> 主分支
> 工作区（本地）--> 暂存区 -->  版本库（历史区）

#### 比较工作区和暂存区的区别
```
git diff
```

#### 比较工作区和版本库的区别
```
git diff master
```

#### 比较暂存区和版本库的区别
```
git diff --cached
```

#### 比较工作区和版本库的区别
```
git diff --master'
```


#### 从暂存区删除本次的add
```
git reset HEAD file
```

#### 回到过去版本
```
git reset --hard commit_id 7c5dfs5e(在git log中查看版本号)
git reset --herd HEAD^ //回到上一次的版本号
```

#### 查看未来版本
```
git reflog  // 由于错误操作，回到过早的版本中，无法查看其他的版本，可以通过reflog查看到。
```

#### 查看所有分支
```
git branch
```

####创建分支
```
git branch Archer  
```

####切换分支
```
git checkout Archer  
```

####创建并切换分支
```
git checkout -b Archer
```

删除分支
```
git branch -d Archer //如果当前在Archer分支中，则无法删除它，要在其它分支中才能删除它
```

合并分支版本区
```
git merge Archer //合并Archer分支提交的文件到主干（分支add、commit -m""后，主干中并没有提交的文件，要合并分支版本区）
```

连接本地仓库和远程仓库
```
git remote add origin URL //origin远程
```

## 合并分支产生冲突
-在主干的某个版本上进行分支开发，在分支上开发1.txt这个文件，在主干上也开发1.txt，此是回到主干上合并时，会产生冲突，需要我们手动解决


将项目提交到github上，需要在github上创建一个空的仓库
##添加远程仓库的连接
```
git remote add origin(名字) http://...
git remote -v  //查看所有远程连接
git remote rm 名字 //删除远程连接
```










