### git

- git config --global user.email "wangjin@gbtrnd.com"

- git config --global user.name "wangjin"

-  git init

- touch readme.txt  然后修改

- git add readme.txt      （git add .  一次添加所有修改文件）

- git commit -m "wrote a readme file"

- git diff readme.txt   或者 git diff HEAD -- readme.txt   #查看工作区readme.txt和版本库里面最新版本的区别 

- git status       #掌握仓库当前的状态 

- git log           #查看提交的历史版本记录  ，HEAD指向的是当前版本

- git reset --hard HEAD^     #回退到上一个版本

- git reset --hard HEAD~100   #往上回退100个版本

- git reset --hard 1094a          #回退到指定版本 ，1094a 是git log输出的commit中的版本号，不用写全，只写前几位就行；如果commit中的版本号忘记了， git reflog用来记录你的每一次命令 

- git reset HEAD readme.txt    #（修改文件，并且add了 ）丢弃缓存区的修改    

- git checkout -- readme.txt    #（就是直接修改文件，但还没add）丢弃工作区的修改时   

- git add test.txt      #手动删除test.txt后，使用git add test.txt ,会在缓存区中删除该文件  

- git commit -m "remove test.txt"     #之前从版本库中删除该文件后，并且把它提交了git checkout -- test.txt

- git checkout -- test.txt     #在工作区误删了test.txt后，可用该命令从缓存区中恢复文件

- git remote add origin git@github.com:pogeba/learngit.git     #添加远程库

-   git remote -v                   #查看远程库信息 

-  git remote rm origin          #如果添加的时候地址写错了，可以用该命令删除远程库 git push -u origin master

- git push -u origin master  #把当前分支`master`推送到远程 ，-u 把本地的`master`分支和远程的`master`分支关联起来 ，这样以后直接用 git push origin master就行

- ```
  git checkout -b dev   #-b参数表示创建dev分支并切换至dev分支
  git branch dev        #创建分支
  git checkout dev      #切换分支
  git branch -a         #查看当前所有分支
  git merge dev        #把dev分支合并到当前分支上
  git branch -d dev     #删除dev 分支
  ```

- git clone -b gpsd_ros git@172.17.4.8:avper/apa.git     #克隆远程库的指定分支gpsd_ros

-   git reset --hard origin/branch_name      #git 本地改动了，不保留，直接拉取线上最新代码


-   git checkout commit_id                #回退到远程commit_id版本的代码


  

## 