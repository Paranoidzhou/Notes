# Git操作总结

-  a：Git注册.并配置GiT账户信息。

-  b：安装GiT 64位，

- ​     安装TortoiseGit-2.5.0.0-64bit、TortoiseGitLanguage_2.5。

- c：在GIt云服务器创建一个Demo库，然后Clone到本地。

- d：初始化生成git管理版本库，然后创建一个文件，将文件提交，推送。

- ​      推送需要复制云服务器的url地址，提交不等于立马上载到服务器，必须要推送。

  > 提交要点递归、提交也可以选择是否立即推送

  > 注意点：提交服务器，必须目录下带.git文件夹（可视为本地仓库），如果不带可能会报错，需要拉取一下云服务器的配置文件，方可推送。

- 第五步： 创建并同步本地文件（在master上完成） 、然后6、上传到远程仓库 。

  > 创建本地文件同步需要先clone云服务器。





一些Git常用操作命令：

- git clone URL                                                              //将远程库克隆到本地，然后再做修改 
- mkdir learngit                                                           //或者也可以直接创建文件夹然后再推送到远程 
- git init                                                                         //初始化生成git管理版本库 
- git add  + 文件名                                                       //将一个文件添加到仓库 
- git commit -m "每次修改的说明内容"                    //一次性提交前面所有的add操作，并添加每次操作的说明 
- git status                                                                    //查看当前有没有未提交的修改 
- git remote add origin URL                                      //关联到远程库 
- git push -u origin master                                        //把本地库的内容推送到远程库. 
- git push                                                                      //没有其他追踪分支时可以简写成这样  



操作本地分支：

- git branch dev                                                            //在本地创建新分支 
- git checkout dev                                                        //切换到本地的dev分支 
- git checkout -b dev                                                    //创建和切换一步完成
-  git branch                                                                  //查看本地所有分支 
- git branch -d dev                                                       //删除本地的dev分支
-  git log                                                                          //查看log，按q退出log模式 
- git rm 文件名(包括路径)                                              //从git中删除指定文件 



操作远程分支：

- git pull                                                                            //从其他的版本库（既可以是远程的也可以是本地的）将代码更新到本地，让本地代码与服务器代码同步 

  

- git branch -r                                                                   //查看远程分支 

  

- git branch test --> git push origin test                       //新建本地分支，然后推送到远程，相当于在远程新建了test分支，多人开发在分支上操作可以用这个方法 

  

- git push origin :test                                                    //删除远程tsst分支，冒号前面的空格不能少，原理是把一个空分支push到server上，相当于删除该分支

  

-  git push origin --delete test                                      //删除远程tsst分支 

  

- git branch –set-upstream dev origin/dev                //指定本地dev分支与远程origin/dev分支的链接，将其链接起来 