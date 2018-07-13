# test

`2018/7/12`

---

`sudo apt`

```c
#include <stdio.h>
void main()
{
    printf("github");
}
```
# 学习内容 gitee.com/thc1234
## 一、配置环境
### 1.简单的Linux命令 (命令 -[选项] [参数] ) (PS:Linux下是区分大小写的) 
#### cd 切换目录
#### ls 显示当前目录下
#### mkdir 创建目录
#### rm 删除文件
#### ln 穿件链接
#### find 查找 （不建议使用 , locate）
#### cat 查看文件内容 (more less )
##### cat命令
主要有三大功能： 
1）一次显示整个文件:cat filename 
2）从键盘创建一个文件:cat > filename 只能创建新文件,不能编辑已有文件 
3）将几个文件合并为一个文件:cat file1 file2 > file
#### echo 输出命令
#### | 通道符 将前面输出的结果作为参数传入后者
#### 重定向 > 覆盖 >> 追加
#### cp 复制文件
#### mv 移动文件
#### wget 下载文件
#### grep 文本搜索工具
---
## 2.vim 的基本操作 
### 三种模式（正常模式，命令模式，插入模式）
#### 命令模式 aio  u返回。D删除 yy复制 p复制内容粘贴到下一行
#### emacs可以了解一下（有点麻烦，古老）
---
## 3.Node.js环境搭建
git clone https://github.com/cnpm/nvm.git 
### 安装Debian，解决依赖问题
#### apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927
#### echo "deb http://repo.mongodb.org/apt/debian 
####  wheezy/mongodb-org/3.2 main" | tee 
#### /etc/apt/sources.list.d/mongodb-org-3.2.list apt-get update
 #### apt-get install -y mongodb-org
```c
yx@debian:cd nvm
yx@debian:pwq /*查询地址，复制*/
yx@debian:vim ~/.bashrc/*进入文件修改，在最后一行：source 粘贴/nvm.sh*/
yx@debian:~/nvm$ source ~/.bashrc
yx@debian:~/nvm$ nvm
/*可以安装很多东西*/
yx@debian:nvm install 10.5.0
```
### 4.搭建Mongodb环境 https://blog.csdn.net/qq_39291929/article/details/78904549(仅供参考)
```c
yx@debian:~/nvm$ cd ~
yx@debian:~$ sudo apt-get install mongodb
/*
CTRL+b+上下键移动
    +b+d退出
db.students。insert（{“姓名”：“THC”}）
```
### mongodb的使用
```c
systemctl stop mongodb 关闭mongodb服务
systemctl disable mongodb 关闭mongodb的自启动
mongod --dbpath 你的数据库路径
mongo // 进入你的数据库
```
---
### 增删减查
```c

```


---
<!-- TOC -->

- [test](#test)
- [学习内容 gitee.com/thc1234](#学习内容-giteecomthc1234)
    - [一、配置环境](#一配置环境)
        - [1.简单的Linux命令 (命令 -[选项] [参数] ) (PS:Linux下是区分大小写的)](#1简单的linux命令-命令--选项-参数--pslinux下是区分大小写的)
            - [cd 切换目录](#cd-切换目录)
            - [ls 显示当前目录下](#ls-显示当前目录下)
            - [mkdir 创建目录](#mkdir-创建目录)
            - [rm 删除文件](#rm-删除文件)
            - [ln 穿件链接](#ln-穿件链接)
            - [find 查找 （不建议使用 , locate）](#find-查找-不建议使用--locate)
            - [cat 查看文件内容 (more less )](#cat-查看文件内容-more-less-)
                - [cat命令](#cat命令)
            - [echo 输出命令](#echo-输出命令)
            - [| 通道符 将前面输出的结果作为参数传入后者](#-通道符-将前面输出的结果作为参数传入后者)
            - [重定向 > 覆盖 >> 追加](#重定向--覆盖--追加)
            - [cp 复制文件](#cp-复制文件)
            - [mv 移动文件](#mv-移动文件)
            - [wget 下载文件](#wget-下载文件)
            - [grep 文本搜索工具](#grep-文本搜索工具)
    - [2.vim 的基本操作](#2vim-的基本操作)
        - [三种模式（正常模式，命令模式，插入模式）](#三种模式正常模式命令模式插入模式)
            - [命令模式 aio  u返回。D删除 yy复制 p复制内容粘贴到下一行](#命令模式-aio--u返回d删除-yy复制-p复制内容粘贴到下一行)
            - [emacs可以了解一下（有点麻烦，古老）](#emacs可以了解一下有点麻烦古老)
    - [3.Node.js环境搭建](#3nodejs环境搭建)
        - [安装Debian，解决依赖问题](#安装debian解决依赖问题)
            - [apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv EA312927](#apt-key-adv---keyserver-hkpkeyserverubuntucom80---recv-ea312927)
            - [echo "deb http://repo.mongodb.org/apt/debian](#echo-deb-httprepomongodborgaptdebian)
            - [wheezy/mongodb-org/3.2 main" | tee](#wheezymongodb-org32-main--tee)
            - [/etc/apt/sources.list.d/mongodb-org-3.2.list apt-get update](#etcaptsourceslistdmongodb-org-32list-apt-get-update)
        - [4.搭建Mongodb环境 https://blog.csdn.net/qq_39291929/article/details/78904549(仅供参考)](#4搭建mongodb环境-httpsblogcsdnnetqq_39291929articledetails78904549仅供参考)
        - [mongodb的使用](#mongodb的使用)
        - [增删减查](#增删减查)
    - [Day02](#day02)
        - [1.cookir复制](#1cookir复制)
        - [2.登陆http://jwc3.yangtzeu.edu.cn](#2登陆httpjwc3yangtzeueducn)
        - [3.F12开发者工具](#3f12开发者工具)
        - [4.编一个爬虫的小程序](#4编一个爬虫的小程序)
        - [数据表单](#数据表单)
            - [crtl+s不能动了按crtl+q可以继续操作](#crtls不能动了按crtlq可以继续操作)
        - [同步获取动态码](#同步获取动态码)
            - [看行号set nu](#看行号set-nu)
            - [<table class="gridtable">](#table-classgridtable)

<!-- /TOC -->

---
## Day02

### 1.cookir复制
### 2.登陆http://jwc3.yangtzeu.edu.cn
### 3.F12开发者工具
### 4.编一个爬虫的小程序
```c
[root@localhost ~]# mkdir newbie
[root@localhost ~]# cd newbie/
[root@localhost newbie]# mkdir Day02
[root@localhost newbie]# ls
Day02
[root@localhost newbie]# cd Day02/
[root@localhost Day02]# vim Spider.py
from bs4 import BeautifulSoup
import requests
import time as tm



```
---
```c

from bs4 import BeautifulSoup
import requests
import time as tm
import hashlib
import re

def get_str_sha(str):
    sha = hashlib.sha1(str)
    return sha.hexdigest( )
user_id = "201706532"
passwd = "201706532"

Header = {
        "User-Agent" : "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/67.0.3396.99 Safari/537.36",
        # "Cookie" : "semester.id=48; JSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131; adc-ck-jwxt_pools=IDALAKAK; GSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131"
}
LoginUrl = "http://jwc3.yangtzeu.edu.cn/eams/login.action"
Url = "http://jwc3.yangtzeu.edu.cn/eams/stdDetail.action"

req = requests.get(LoginUrl)
html = req.text

res = re.search("CryptoJS.SHA1\(\'(.*)\' ",html)
opasswd = res.group(1)
passwd = get_str_sha((opasswd+passwd).encode("utf-8/"))
print(passwd)

```
---
### 数据表单
#### crtl+s不能动了按crtl+q可以继续操作
```c
def get_str_sha(str):
    sha = hashlib.sha1(str)
    return sha.hexdigest( )
user_id = "201706532"
passwd = "201706532"

Header = {
        "User-Agent" : "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/67.0.3396.99 Safari/537.36",
        # "Cookie" : "semester.id=48; JSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131; adc-ck-jwxt_pools=IDALAKAK; GSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131"
}
LoginUrl = "http://jwc3.yangtzeu.edu.cn/eams/login.action"
Url = "http://jwc3.yangtzeu.edu.cn/eams/stdDetail.action"

req = requests.get(LoginUrl)
html = req.text

res = re.search("CryptoJS.SHA1\(\'(.*)\' ",html)
opasswd = res.group(1)
passwd = get_str_sha((opasswd+passwd).encode("utf-8/"))
print(passwd)

Data = {
        "username" : user_id,
        "password" : passwd,
        "encodedPassword" : "",
        "session_locale" : "zh_CN",
        }
req = requests.post(LoginUrl,data=Data)
print(req.text)

```
---
### 同步获取动态码
```c
def get_str_sha(str):
    sha = hashlib.sha1(str)
    return sha.hexdigest( )
user_id = "201706532"
passwd = "201706532"

Header = {
        "User-Agent" : "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/67.0.3396.99 Safari/537.36",
        # "Cookie" : "semester.id=48; JSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131; adc-ck-jwxt_pools=IDALAKAK; GSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131"
}
LoginUrl = "http://jwc3.yangtzeu.edu.cn/eams/login.action"
Url = "http://jwc3.yangtzeu.edu.cn/eams/stdDetail.action"
s = requests.Session()#同步获取动态码   //
req = s.get(LoginUrl)   //
html = req.text

res = re.search("CryptoJS.SHA1\(\'(.*)\' ",html)
opasswd = res.group(1)
passwd = get_str_sha((opasswd+passwd).encode("utf-8/"))
print(passwd)

Data = {
        "username" : user_id,
        "password" : passwd,
        "encodedPassword" : "",
        "session_locale" : "zh_CN",
        }
req = s.post(LoginUrl,data=Data) //
print(req.text)  /**/

```
---
```c
def get_str_sha(str):
    sha = hashlib.sha1(str)
    return sha.hexdigest( )
user_id = "201706532"
passwd = "201706532"

Header = {
        "User-Agent" : "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/67.0.3396.99 Safari/537.36",
        # "Cookie" : "semester.id=48; JSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131; adc-ck-jwxt_pools=IDALAKAK; GSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131"
}
LoginUrl = "http://jwc3.yangtzeu.edu.cn/eams/login.action"
Url = "http://jwc3.yangtzeu.edu.cn/eams/stdDetail.action"
s = requests.Session()#同步获取动态码   //
req = s.get(LoginUrl)   //
html = req.text

res = re.search("CryptoJS.SHA1\(\'(.*)\' ",html)
opasswd = res.group(1)
passwd = get_str_sha((opasswd+passwd).encode("utf-8/"))
print(passwd)

Data = {
        "username" : user_id,
        "password" : passwd,
        "encodedPassword" : "",
        "session_locale" : "zh_CN",
        }
tm.sleep(1)
req = s.post(LoginUrl,data=Data) 
print(req.text)
InfoUrl =  "http://jwc3.yangtzeu.edu.cn/eams/stdDetail.action" 
rep = s.get(InfoUrl)
html = req.text
print(html)
soup = BeautifulSoup(html,"lxml")
trs = soup.find_all("tr")
for tr in trd
```
#### 看行号set nu
---
```c

from bs4 import BeautifulSoup
import requests
import time as tm
import hashlib
import re
from pymongo import MongoClient
def get_str_sha(str):
    sha = hashlib.sha1(str)
    return sha.hexdigest( )
user_id = "201706532"
passwd = "201706532"

Header = {
        "User-Agent" : "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/67.0.3396.99 Safari/537.36",
        # "Cookie" : "semester.id=48; JSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131; adc-ck-jwxt_pools=IDALAKAK; GSESSIONID=483B103EE9F9A1DBC972F00BD66AF558.node131"
}
LoginUrl = "http://jwc3.yangtzeu.edu.cn/eams/login.action"
Url = "http://jwc3.yangtzeu.edu.cn/eams/stdDetail.action"
client = MongoClient("192.168.1.148",27017)
#client = MongoClient("locahost",27017)
db = client["mydb"]
col = db["students"]
s = requests.Session()#同步获取动态码
req = s.get(LoginUrl)
html = req.text

res = re.search("CryptoJS.SHA1\(\'(.*)\' ",html)
opasswd = res.group(1)
passwd = get_str_sha((opasswd+passwd).encode("utf-8/"))
print(passwd)

Data = {
        "username" : user_id,
        "password" : passwd,
        "encodedPassword" : "",
        "session_locale" : "zh_CN",
        }
tm.sleep(1)
req = s.post(LoginUrl,data=Data)
print(req.text)
InfoUrl =  "http://jwc3.yangtzeu.edu.cn/eams/stdDetail.action"
req = s.get(InfoUrl)
html = req.text
print(html)
soup = BeautifulSoup(html,"lxml")
trs = soup.find_all("tr")
infos = {}
keys = []
vals = []
print(trs)
for tr in trs[1:-1]:
        tds = tr.find_all("td")
        if len(tds) < 2:
                continue
        print("----------------------")
        key1 = tds[0].getText()[:-1]
        val1 = tds[1].getText()
        key2 = tds[2].getText()[:-1]/*省略姓名后面的冒号*/
        val2 = tds[3].getText()
        keys.append(key1)
        keys.append(key2)
        vals.append(val1)
        vals.append(val2)
for i in range(len(vals)-1):
        infos[keys[i]] = vals[i]
print(infos)

col.insert_one(infos)
/*注释掉的部分*/
'''
        for idx,td in enumerate(tds):
                if idx in [4]:
                        continue
                print(td.getText())
'''

```
####  <table class="gridtable">
<table class="grid">
```c
GradeUrl = "http://jwc3.yangtzeu.edu.cn/eams/teach/grade/course/person!historyCourseGrade.action?projectType=MAJOR"
req = s.get(GradeUrl)
html = req.text
print(html)
soup = BeautifulSoup(html,"lxml")
trs = soup.find_all("tr")
point = {}
print(trs)
for tr in trs[1:-1]:
        tds = tr.find_all("td")
print(point)
                

```
 EOL while scanning string literal
https://blog.csdn.net/a472770699/article/details/52530504参考
