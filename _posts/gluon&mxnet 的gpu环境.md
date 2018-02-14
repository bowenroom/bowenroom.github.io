---
layout: post
title: gluon&mxnet的gpu环境搭建
date: 2018-02-13 15:32:24.000000000 +09:00
categories: bowenroom
tags: original_tutorial
---


# gluon&mxnet 的gpu环境搭建


1. 首先来更新一下`sudo apt-get update`
2. `sudo apt-get install build-essential git` 
3. `wget https://developer.nvidia.com/compute/cuda/8.0/Prod2/local_installers/cuda_8.0.61_375.26_linux-run `(获取cuda的地址)
4. `chmod +x cuda_8.0.61_375.26_linux-run`(获取权限)

6. 本地安装一般会出现图形界面的问题,服务器则不会

7.
```shell

sudo /etc/init.d/lightdm stop
sudo /etc/init.d/lightdm status
# 别忘了搞定后重新打开

sudo /etc/init.d/lightdm restart
 ```
8.`sudo ./cuda_8.0.61_375.26_linux-run `按照步骤一步步安装驱动  
9.`nvidia-smi`看一下是否安装好nvidia驱动

10. 安装anaconda wget https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh
11. bash Anaconda 
> 补充:[最好设置git走代理 ](http://www.jianshu.com/p/5e74b1042b70)

12. 报**Missing dependencies for SOCKS support.**的错误：`pip install requests[socks]`
> 或者是
```
Unset socks proxy, in your case: 
unset all_proxy
unset ALL_PROXY
Install missing dependencies: 
pip install pysocks
Reset proxy, source .bashrc, and pip install works again with socks proxy.
```
13.需要在bashrc中配置的内容：
```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda-8.0/lib64

export PATH=/home/bowenroom/miniconda3/bin:$PATH
alias gluon='source activate gluon'
alias jp='MXNET_GLUON_REPO=https://apache-mxnet.s3.cn-north-1.amazonaws.com.cn/ jupyter notebook --NotebookApp.contents_manager_class='notedown.NotedownContentsManager'
'

```
14. 关于numpy的操作不支持gpu的操作,所有关于numpy的地方,都是用的cpu
 


