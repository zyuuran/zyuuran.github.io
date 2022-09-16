---
title: 1_python基础
date: 2022-09-15 20:24:33
categories:
- python
tags:
- python
---
# <font color = blue >python基础</font>
## 变量/字符串
### 变量
    = : 赋值      把右边的值赋给左边
    类型 : str,int,bool……
    
    a = 4 #不需要先定义类型再赋值
    b = 5
    t = a
    a = b
    b = t
    print(a,b) # result 5 4
### 字符串 加法/乘法
    print("I"+" Love"+" Python") #result I Love Python
    print("python"*3) #result pythonpythonpython
### 切片/索引
    a = 'xxxxx'
    a[0] : 第一个元素
    a{x][0<=x<正无限) : 第1到(x-1)个元素
    a[-1] : 最后一个元素
    
| |1|2|3|4|5|6|7|8|9|10|
|----|----|----|----|----|----|----|----|----|----|----|
|a[+]|0|1|2|3|4|5|6|7|8|9|
|a[-]|-10|-9|-8|-7|-6|-5|-4|-3|-2|-1|
### 方法
    .split('x') : 通过x分割
    .repalce('x','y') : 把x替换成y
    .strip() : 去除字符串两边指定的字符
    .format() :
            a = "I love {}".format(‘Python’)
            print(a) # result I love Python
## 函数/控制语句
### 函数
    def 函数名 (参数1，参数2…):  
        return '结果‘
    
    def c_number(number):
        h_number = number.replace(number[3:7]),'*'*4)
        print(h_number)
    c_number('18888888888')
    # result 188****8888
### 判断
    if 条件:
        do
     else:
         do
         
    if 条件:
        do
    elif 条件:
        do
    else:
        do
        
    def c_login():
        passwd = input('password')
        if passwd == '123456':
            print('login ok')
        else:
            print(''password)
    c_login() 
### 循环
    for 元素 in 集合 :
        do
    
    for i in (1,11):
        print(i) #result 12345678910

    while 条件:
        do
        
    i = 0
    sum = 0
    while i < 199:
        i = i + 1
        sum = sum + i
    print(sum) #result 5050
## 数据结构
### 列表
    name = ['w1','w2''w3']
    age = [12,13,14]
    for name,age in zip(name,age):
        print(name,age)
    #result
    w1 12
    w2 13
    w3 14
### 字典
    u_info{
        'name':'w1',
        'age':'12',
        'sex':'man'
    }
    print u_info['name']
    # result w1
### 元组/集合
    tuple =（1，2，3） #只能看不能改
    
    list = ['w1','w2','w3']
    set = set(list)
    print(set)
    #result {'w1','w2'}
## 文件操作
### 打开文件
    open(name[, mode[, buffering]]) #name必填 其它可选
    f = open('/root/hexo/_config.yml')
### 读写文件
    [root@192 hexo]# cat test.txt
    test doc
    [root@192 hexo]# python
    Python 3.9.13 (main, Jul 25 2022, 00:00:00)
    [GCC 11.3.1 20220421 (Red Hat 11.3.1-2)] on linux
    Type "help", "copyright", "credits" or "license" for more information.
    >>> f = open('/root/hexo/test.txt','r')
    >>> content = f.read()
    >>> print(content)
    test doc
    
|值|描述
|----|----|
|'r'|读模式|
|'w'|写模式|
|'a'|追加模式|
|'b'|二进制模式（可添加到其他模式使用）|
|'+'|读写模式（可添加到其他模式使用）|
### 关闭文件
    f.close
## 面向对象
### 类
类：具有相同属性和方法的对象集合

    class b:
        c = ['f','w','p']
    m = b()
    y = b()
    print(m)
    print(b)
    #rresult : 
    ['f','m','b'] 
    ['f','m','b'] 
### 实例属性
    class b:
        c = ['f','w','p']
    m = b()
    m.other= 'ba' #实例
    print(m.other)
    #result ba
### 实例方法
    clss b:
        c = ['f','w','p']
        def u(self,time):
            print('{}m'.format(time*100))
    m = b()  #调用b()
    m.u(10)  #b().U(10)
    #result 1000m
    
    _init_() 方法 创造实列时，不需要引用自动运行
### 类的继承
子类继承父类，子类包含父类的所以属性
    
    class b():
        c = ['f','w','p']
        def _init_(self):
            self.other = 'basket'
        def u(self,time):
            print('{}m'.format(time*100))
    class S_b(b): #s_b()&&b() 只能运行可以自动运行的
        def cost(self,hour):
            print('{}k'.format(hour*2))
    b = s_b() # S_b()
    print(b.other)
    b.cost(2) #s_b().cost(2)&&b().cost(2)
##### <font color = 'blue'>本文档到此处就结束了，虽然没啥文字解析，但是我感觉看这些代码应该差不多能理解了</blue>