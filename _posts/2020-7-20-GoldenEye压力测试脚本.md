---
title: GoldenEye压力测试脚本
layout: post
comments: true
toc: true
---
玩压力测试的朋友肯定都知道，测试机器防御用的一款工具，下面说的这款 GoldenEye是一款Layer 7拒绝服务测试工具，采用Python语言开发。这是一款HTTP DoS测试工具，可帮助研究人员对目标项目进行安全测试。

参数帮助
-u：指定需要使用的user-agent列表文件（默认随机生成）；
-w：指定并行worker数量（默认50）；
-s：指定并行socket数量（默认30）；
-m：指定使用的HTTP方法，“get“、”post“或”random“（默认get）；
-d：启用调试模式（默认false）；
-n：关闭SSL证书验证功能（默认true）；
-h：查看帮助信息

使用帮助

首先你需要一台抗投诉服务器或者是发包机
推荐使用git克隆整个项目到服务器
第一步跳转到脚本所在目录
cd /GoldenEye
第二步为脚本添加执行权限
chmod +x goldeneye.py
第三步脚本的使用帮助指令
./goldeneye.py -h
压测指令为
./goldeneye.py http://xxx.com -w 1000 -s 500

GoldenEye项目地址：https://github.com/jseidl/GoldenEye