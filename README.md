# Mirai-bot
 基于Mirai框架的QQbot（个人用）

# 基于Mirai框架的QQ机器人玩法不完全总结    

--------------------------------
前两天本来打算去GitHub找一个QQ的改进版应用实现群聊分组功能，结果一个没找到，找到个CSGO的QQ自动战绩播报。       

于是就开始部署复现，搞半天发现问题总出现在requests后loads的json数据中，报错信息为TypeError: 'NoneType' object is not subscriptable     

转头去找战绩查询的API，发现完美好像取消了网页端战绩查询入口，剩下能想的办法就是下载移动端APP尝试，不过不确定原作者用的是ANDROID还是IOS。总之，以后如果有空，我会尝试找出战绩的JSON格式。     

OK,CSGO这个战绩播报算是栽了，但是也看到了很多优秀的Mirai项目以及社区，下面就是我从不同开源项目组合成多功能机器人的过程:smirk:      


# 环境配置   
python 3.10（最新）    
Java （我用的openjdk18）好像可以在Mirai首次运行时自动下载jdk   


# Mirai开发框架安装    
[Mirai官方](https://github.com/mamoe/mirai)    
[Mirai下载链接](https://github.com/iTXTech/mcl-installer/releases)      

运行mcl.cmd文件，在窗口按步骤安装    
关闭窗口，将生成的“mirai-api-http-v1.12.0.mirai.jar”文件移动到plugins文件夹中    
再次运行mcl.cmd，可以查看操作帮助，加入自动登录等功能     

*自动登录功能可以在控制台操作，也可以直接打开condig\Console\Autologin.yml在其中修改*     

（将“host: 0.0.0.0“中的”0.0.0.0”更改为“127.0.0.1这条找不到，暂时不影响使用）     

-----记住（authkey）vertifykey，有些插件会要用------    

最终文件夹中大致如下：     
![K)_T3U9$S20$7D 5KTQI2K0](https://user-images.githubusercontent.com/92584983/180748469-3acd1bff-66ab-4181-b85a-d91519a7ebb8.png)     

其中config文件夹是通常修改设置的地方，一般运行一次cmd之后才会生成            
![N6 6W@SB4O{N588SOZ%WFF8](https://user-images.githubusercontent.com/92584983/180748664-89fb84f6-109a-41b0-b98c-797f29b66bd6.png)       


## 插件一：随机色图插件（suijisetu）    
[下载地址](https://github.com/Ycituss/suijisetu)     
下载.jar文件，扔进plugins文件夹中，运行一次cmd后可以在yml文件中编辑戳一戳后的回复，以及反击概率等等   

目前这款插件最不稳定，不知是和P站连接问题还是腾讯对某些图片屏蔽问题    
![T_GFN{5B`JM9P UGRF4XKTW](https://user-images.githubusercontent.com/92584983/180754568-ec5510ab-0fa5-4ec9-93d1-bc092e11a67f.png)     




## 插件二：steamhelper    
[下载地址](https://github.com/EvolvedGhost/Steamhelper)     
下载.jar文件，扔进plugins文件夹中，运行后以/sh开头运行指令    

![)(P14X{0{7XZS4DSBA F@U](https://user-images.githubusercontent.com/92584983/180748938-59593e3a-b3e1-4e43-9eec-4649e22c3558.png)       
![~_WQ}R$O%WRJ_P(0A_AKQ4J](https://user-images.githubusercontent.com/92584983/180749027-29443fc8-6d6c-4a12-9cef-9beef93da58b.png)      



## 插件三：KFC疯狂星期四推送    
[下载地址](https://github.com/KuriYama-mirai524/KFC-creazy-Thursday/releases/tag/v0.0.1)      
解压后打开Windows文件夹中的KFC.exe直接运行    
注意！！提前修改data.json中的key以及qq等数据，并在Mirai登录成功后再运行     


## 插件四：Plum多功能    
[Plum版本下载地址](https://pan.baidu.com/s/1rOrHGDJtorWP3yeAuWDzpA
)(提取码: 7777)      
[项目地址](https://gitee.com/K85/plum)     

稳定功能：早安晚安，智能点歌，一言，动漫壁纸    
暂未可用：智能唱歌，智能聊天    
![1~0SC$HR7MDMV1JK)B(M7LC](https://user-images.githubusercontent.com/92584983/180749081-28662f34-5350-462c-a8e0-f4378bfd5b6c.png)     
![Q1UE046JKCMC@)%EN3V}4BK](https://user-images.githubusercontent.com/92584983/180749112-52274724-dfd5-490c-acd6-c78fd4c19612.png)       



## 插件五：新闻播报    
[下载地址](https://github.com/LinHeLurking/mirai-news-reporter)     
可以播送今日新闻和今日番剧       


# 看到几个有意思的QQBOT   
[哔哩哔哩成分姬](https://github.com/LXY1226/BiliFansBot)     
[QQLight机器人](https://github.com/QPromise/qqRobot)     
[沙雕多功能机器人](https://github.com/remiliacn/qqBot)较为专业，各种娱乐，视频网站，炒股等等     

## 最后，附上看到的一篇很好的制作简单机器人的文章，本文也从中有所借鉴    
==========
[see more](https://www.bilibili.com/read/cv14188183?spm_id_from=333.999.0.0)    
==========
# 具体部署过程就是这些，祝你玩的开心！          
