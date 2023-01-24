# HGAME 2023 Week2 writeup by lc622

[TOC]

## Web

### Git Leakage

一道Git泄露的题目，先用工具扫描一下后台目录。发现确实是有.git文件。

于是用GitHack工具，执行GitHack脚本，把文件下载到文件中，找到包含flag文件。

![image-20230113003129653](L:\桌面\HGAME 2023\Week2\web\image-20230113003129653.png)

![image-20230113003239570](L:\桌面\HGAME 2023\Week2\web\image-20230113003239570.png)

