# HGAME 2022 Week1 writeup by DullJZ

[TOC]

## REVERSE

### test your IDA

![](https://cdn.jsdelivr.net/gh/DullJZ/MyPicture@master/20230112173741.png)

## WEB

### Become A Member

1. 设置UA为Cute-Bunny
2. 提示code为Vidar，查看header发现set-cookie为code=guest，在请求中添加对应cookie![](https://cdn.jsdelivr.net/gh/DullJZ/MyPicture@master/20230112174441.png)
3. 根据提示添加referer为bunnybunnybunny.com
4. 提示需要修改为本地请求，设置X-Forwarded-For为127.0.0.1![](https://cdn.jsdelivr.net/gh/DullJZ/MyPicture@master/20230112174701.png)
5. 拿到账号密码，在body中已json格式填写即可![image-20230112174910342](C:\Users\admin\AppData\Roaming\Typora\typora-user-images\image-20230112174910342.png)

### Guess Who I Am

![](https://cdn.jsdelivr.net/gh/DullJZ/MyPicture@master/20230112175026.png)

F12分析得知主要为三个请求：`getQuestion` `verifyAnswer` `getScore`

题目对应的答案在HTML代码的注释中给出了相应链接

编写相应python脚本：

```python
import json
import requests
import warnings
import time


def search_id(message: str) -> str:
    i = 0
    while 1:
        if member[i]['intro'] == message:
            found = True
            return member[i]['id']
        else:
            i += 1


warnings.filterwarnings('ignore')

GET_QU_URL = 'http://week-1.hgame.lwsec.cn:31495/api/getQuestion'
VERIFY_URL = 'http://week-1.hgame.lwsec.cn:31495/api/verifyAnswer'
GET_SCORE_URL = 'http://week-1.hgame.lwsec.cn:31495/api/getScore'

# 转换为字典的列表，具体信息省略500行......
member = [{
    "id": "ba1van4",
    "intro": "21级 / 不会Re / 不会美工 / 活在梦里 / 喜欢做不会的事情 / ◼◻粉",
    "avatar": "https://thirdqq.qlogo.cn/g?b=sdk&k=kSt5er0OQMXROy28nzTia0A&s=640",
    "url": "https://ba1van4.icu"}, {
    "id": "yolande",
    "intro": "21级 / 非常菜的密码手 / 很懒的摸鱼爱好者，有点呆，想学点别的但是一直开摆",
    "avatar": "https://thirdqq.qlogo.cn/g?b=sdk&k=rY328VIqDc7lNtujYic8JxA&s=640",
    "url": "https://y01and3.github.io/"
}, {
    "id": "t0hka",
    "intro": "21级 / 日常自闭的Re手",
    "avatar": "https://thirdqq.qlogo.cn/g?b=sdk&k=EYNwm1PQe8o5OcghFb4zfw&s=640",
    "url": "https://blog.t0hka.top/"
}, {
    "id": "Eric",
    "intro": "渗透 / 人工智能 / 北师大博士在读",
    "url": "https://3riccc.github.io"
}
]
# 注意到浏览器的Cookie设置
Cookie = 'session=MTY3MzQ0NzEyMXxEdi1CQkFFQ180SUFBUkFCRUFBQU9fLUNBQUlHYzNSeWFXNW5EQWdBQm5OdmJIWmxaQU5wYm5RRUFnQUVCbk4wY21sdVp3d05BQXRqYUdGc2JHVnVaMlZKWkFOcGJuUUVBZ0FzfPTK9lbAJsugaZX85RfxBTS66IhhAnxwv9h1SxqK7k0v'
session = requests.Session()
while 1:
    r = session.get(GET_QU_URL, headers={'Cookie': Cookie})
    data = json.loads(r.text)
    print(r.text)
    r1 = session.post(VERIFY_URL, data={'id': search_id(data['message'])}, headers={'Cookie': Cookie})
    print(r1.text)
    # 刚开始没注意到Cookie的更新，导致全部都是同一个题目
    Cookie = r1.headers['Set-Cookie']
    r2 = session.get(GET_SCORE_URL, headers={'Cookie': Cookie})
    print(r2.text)
    time.sleep(0.1)
    if r1.text != r'{"message":"Correct answer!"}':
        print(r1.text)
        print(Cookie)
        break

```



## MISC

## CRYPTO

## IoT