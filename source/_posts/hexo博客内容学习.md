---
title: hexo博客内容学习
date: 2022-09-15 01:55:20
categories:
- hexo
tags:
- hexo
---
# hexo博客创建总结
首先我这边使用的操作系统是 *Centos9*
### 第一步 git、Node.js 的安装
    yum -y install git
    yum install -y nodejs
    npm install -g hexo-cli
### 第二步 创建blog文件夹 初始化hexo
这里我选用的位置是/root 

    mkdir blog
    hexo init blog
### 第三步 安装依赖
    cd blog/
    npm install
    hexo g
    hexo server
### 第四步 利用github创建仓库
    New repository --> create repository
### 第五步 生成SSH密钥
    git config --global user.name "yourname"
    git config --global user.email "youremail"
    ssh-keygen -t rsa -C "youremail"
    #在这里会得到一个.pub的文件，cat它
*在SSH and GPG keys里面填写*
### 第六步 更改  _config.yml 文件
     deploy:
          type: git
          repo: github仓库SSH地址，复制过来就行
          branch: master
### 第七步 上传
    hexo clean
    hexo g
    hexo d
    
    