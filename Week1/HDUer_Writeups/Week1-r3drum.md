### Classic Childhood Game

题目告知为本地前端游戏，存档数据都在本地

通过浏览器的developer tools工具查看Application中的Local Storage，发现存档参数

通过更改攻击力，生命值，钥匙数量和道具数量轻松通关

hgame{fUnnyJavascript&FunnyM0taG4me}

### Sign in

aGdhbWV7V2VsY29tZV9Ub19IR0FNRTIwMjMhfQ==直接base64解码

hgame{Welcome_To_HGAME2023!}

### Become A Member

首先提示需要以Cute-Bunny身份，通过burpsuite抓包修改User-Agent为Cute-Bunny

又提示需要code为Vidar，将http请求头中添加Cookie: code=Vidar

需要通过bunnybunnybunny.com访问，将请求头中添加Referer: bunnybunnybunny.com

需要内网访问，添加X-Forwarded-For: 127.0.0.1

hgame{H0w_ArE_Y0u_T0day?}

### Show Me Your Beauty

抓包修改为.php然后发送

访问上传的.php木马，使用蚁剑连接

hgame{Unsave_F1L5_SYS7em_UPL0ad!}

### Guess Who I Am

通过脚本答题

from requests import *
import json

answer = {'21级 / 不会Re / 不会美工 / 活在梦里 / 喜欢做不会的事情 / ◼◻粉': 'ba1van4',
          '21级 / 非常菜的密码手 / 很懒的摸鱼爱好者，有点呆，想学点别的但是一直开摆': 'yolande',
          '21级 / 日常自闭的Re手': 't0hka', '21级 / 菜鸡pwn手 / 又菜又爱摆': 'h4kuy4',
          '21级web / cat../../../../f*': 'kabuto',
          '21级 / 爱好歪脖 / 究极咸鱼一条 / 热爱幻想 / 喜欢窥屏水群': 'R1esbyfe',
          '21级 / 喜欢肝原神的密码手': 'tr0uble', '21级 / 入门级crypto': 'Roam',
          '20级 / 摆烂网管 / DN42爱好者': 'Potat0', '20级 / 歪脖手 / 想学运维 / 发呆业务爱好者': 'Summer',
          '20级 / 已退休不再参与大多数赛事 / 不好好学习，生活中就会多出许多魔法和奇迹': 'chuj',
          '20级会长 / re / 不会pwn': '4nsw3r', '20级 / 可能是IOT的MISC手 / 可能是美工 / 废物晚期': '4ctue',
          '20级 / Re手 / 菜': '0wl', '20级 / web / 想学iot': 'At0m', '20级 / Crypto / 摸鱼学代师': 'ChenMoFeiJin',
          '20级 / WEB / 菜的抠脚 / 想学GO': 'Klrin', '20级 / Web / 还在努力': 'ek1ng',
          '20级 / Crypto&Block (70.030, 0.970, 1.40%)Chain / Plz V me 50 eth': 'latt1ce',
          '*级 / 被拐卖来接盘的格子 / 不可以乱涂乱画哦': 'Ac4ae0',
          '19级 / 不会web / 半吊子运维 / 今天您漏油了吗': 'Akira', '19级 / 摸鱼美工 / 学习图形学、渲染ing': 'qz',
          '19级 / 脖子笔直歪脖手': 'Liki4', '19级 / &lt;/p&gt;&lt;p&gt;Web': '0x4qE', '19级 / 骨瘦如柴的胖手': 'xi4oyu',
          '19级 / bin底层选手': 'R3n0', '19级 / 不会re / dl萌新 / 太弱小了，没有力量 / 想学游戏': 'm140',
          '19级 / 普通的binary爱好者。': 'Mezone', '19级 / 游戏开发 / 🐟粉': 'd1gg12',
          '19级 / 半个全栈 / 安卓摸🐟 / P 社玩家 / 🍆粉': 'Trotsky', '19级 / 挖坑不填的web选手': 'Gamison',
          '19级会长 / DL爱好者 / web苦手': 'Tinmix', '19级 / Re手，我手呢？': 'RT',
          '18 级 / 完全不会安全 / 一个做设计的鸽子美工 / 天天画表情包': 'wenzhuan',
          '18级 / 莫得灵魂的开发 / 茄粉 / 作豚 /  米厨': 'Cosmos',
          '18 级 / Bin / Win / 电竞缺乏视力 / 开发太菜 / 只会 C / CSGO 白给选手': 'Y',
          '18级 / 会点开发的退休web手 / 想学挖洞 / 混吃等死': 'Annevi',
          '18 级 / 求大佬带我IoT入门 / web太难了只能做做misc维持生计 / 摸🐟': 'logong', '18 级 / Web / 车万': 'Kevin',
          '18级 / 会一丢丢crypto / 摸鱼': 'LurkNoi', '18级会长 / 二进制安全 /  干拉': '幼稚园',
          '18级 / 游戏引擎开发 / 尚有梦想的game maker': 'lostflower', '18 级 / Web 底层选手': 'Roc826',
          '18 级 / Web / 真·菜到超乎想象 / 拼死学（mo）习（yu）中': 'Seadom',
          '18级 / 懂点Web & Misc / 懂点运维 / 正在懂游戏引擎 / 我们联合！': 'ObjectNotFound',
          '18 级 / 不擅长 Web / 擅长摸鱼 / 摸鱼！': 'Moesang',
          '18级 / 囊地鼠饲养员 / 写了一个叫 Cardinal 的平台': 'E99p1ant', '18 级 / Java / 会除我佬': 'Michael',
          '18级 / 编译器工程师 伪 / 半吊子PL- 静态分析方向': 'matrixtang', '18级 / 不可以摸🐠哦': 'r4u',
          '18级 / 并不会web / 端茶送水选手': '357', '17 级 / Web 安全爱好者 / 半个程序员 / 没有女朋友': 'Li4n0',
          '17级 / Focus on Java Security': '迟原静', '17 级 / 自称 Bin 手实际啥都不会 / 二次元安全': 'Ch1p',
          '17 级 / Web': 'f1rry', '17 级 / 业余开发 / 专业摸鱼': 'mian',
          '17级 / 摸鱼ctfer / 依旧在尝试入门bin / 菜鸡研究生+1': 'ACce1er4t0r',
          '17级 / 二战人 / 老二次元 / 兴趣驱动生活': 'MiGo',
          '17级 / RedTeam (8.260, 0.180, 2.23%)er / 字节跳动安全工程师': 'BrownFly',
          '17级/ Key厨 / 腾讯玄武倒水的': 'Aris', '17级 / 游戏厂打工仔 / 来深圳找我快活': 'hsiaoxychen',
          '17级 / web / 东南读研': 'Lou00', '16 级 / 立志学术的统计er / R / 为楼上的脱单事业做出了贡献': 'Junier',
          '16 级会长 / Web 后端 / 会一点点 Web 安全 / 会一丢丢二进制': 'bigmud',
          '16 级 / Java 福娃 / 上班 996 / 下班 669': 'NeverMoes', '16 级 / Web Developer': 'Sora',
          '16 级 / 可能会运维 / 摸鱼选手': 'fantasyqt', '16 级 / Rev / Windows / Freelancer': 'vvv_347',
          '16 级 / Bin / 被迫研狗': 'veritas501', '16 级 / Web 🐱 / 现于长亭科技实习': 'LuckyCat',
          '16 级 / Java 开发攻城狮 / 996 选手 / 濒临猝死': 'Ash', '16 级 / Web 前端 / 美工 / 阿里云搬砖': 'Cyris',
          '16 级 / Web 前端 / 水母一小只 / 程序员鼓励师 / Cy 来组饥荒！': 'Acaleph',
          '16级 / 大果子 / 毕业1年仍在寻找vidar娘接盘侠': 'b0lv42', '16 级 / 蟒蛇饲养员 / 高数小王子': 'ngc7293',
          '16 级 / Web / 菜鸡第一人': 'ckj123', '16级 / 前web手、现pwn手 / 菜鸡研究生 / scu': 'cru5h',
          '16 级 / Bin 打杂 / 他们说菜都是假的，我是真的': 'xiaoyao52110', '15 级网安协会会长 / Web 安全': 'Undefinedv',
          '逆向 / 二进制安全': 'Spine', '二进制 CGC 入门水准 / 半吊子爬虫与反爬虫': 'Tata',
          'Web 安全 / 长亭科技安服部门 / TSRC 2015 年年度英雄榜第八、2016 年年度英雄榜第十三': 'Airbasic',
          '15 级 / 什么都不会的开发 / 打什么都菜': 'jibo',
          '15 级 Vidar 会长 / 送分型逆向选手 / 13 段剑纯 / 差点没毕业 / 阿斯巴甜有点甜': 'Processor',
          '15 级 / 挖不到洞 / 打不动 CTF / 内网渗透不了 / 工具写不出': 'HeartSky',
          '15 级 / 删库跑路熟练工 / 没事儿拍个照 / 企鹅': 'Minygd', '15 级 / 已入 Python 神教': 'Yotubird',
          '15 级 / Web 🐶 / 汪汪汪': 'c014',
          '14 级 HDUISA 会长 / 二进制安全 / 曾被 NULL、TD、蓝莲花等拉去凑人数 / 差点没毕业 / 长亭安研': 'Explorer',
          '14 级 HDUISA 副会长 / 二次元 / 拼多多 (94.090, -1.430, -1.50%)安全工程师': 'Aklis',
          '14 级网安协会会长 / HDUISA 成员 / Web 安全 / Freebuf 安全社区特约作者 / FSI2015Freebuf 特邀嘉宾': 'Sysorem',
          '13 级 / 知道创宇 404 安全研究员 / 现在 Nu1L 划划水 / IoT、Web、二进制漏洞，密码学，区块链都看得懂一点，但啥也不会': 'Hcamael',
          '14 级 / Web 🐶 / 杭电江流儿 / 自走棋主教守门员': 'LoRexxar', '14 级网安协会副会长 / Web 安全': 'A1ex',
          '14 级网安协会副会长 / 无线安全': 'Ahlaman',
          'Web 安全 / 安全工程师 / 半吊子开发 / 半吊子安全研究': 'lightless',
          '13 级 HDUISA 会长 / Web 安全 / 华为安全部门 / 二进制安全，fuzz，符号执行方向研究': 'Edward_L',
          '13 级菜鸡 / 大数据打杂': '逆风',
          '什么都不会 / 咸鱼研究生 / <del>安恒</del>、<del>长亭</del> / SJTU': '陈斩仙',
          '渗透 / 人工智能 / 北师大博士在读': 'Eric'}

cookie = {
    ""
    "Cookie": "session=MTY3MzQ1MzEzNHxEdi1CQkFFQ180SUFBUkFCRUFBQU9fLUNBQUlHYzNSeWFXNW5EQTBBQzJOb1lXeHNaVzVuWlVsa0EybHVkQVFDQUNBR2MzUnlhVzVuREFnQUJuTnZiSFpsWkFOcGJuUUVBZ0FBfKvr-MqsuuExcS-RJ1luQ6P_IeV_rzX1ntEcX5CbMVkE"
}
while 1:
    m = get("http://week-1.hgame.lwsec.cn:32696/api/getQuestion", headers=cookie)
    print(m.text)
    json_obj = json.loads(m.text)
    q = json_obj['message']
    try:
        n = post("http://week-1.hgame.lwsec.cn:31772/api/verifyAnswer", data={'id': answer[q]}, headers=cookie)
        print(n.text)
        cookie['Cookie'] = "session=" + n.cookies.values()[0]
        k = get("http://week-1.hgame.lwsec.cn:32696/api/getScore", headers=cookie)
        print(eval(k.text))
        if eval(k.text)['message'] == 100:
            print(k.cookies)
    except KeyError:
        print(q)
        n = post("http://week-1.hgame.lwsec.cn:32696/api/verifyAnswer", data={'id': input()}, headers=cookie)
        print(n.text)
        cookie['Cookie'] = "session=" + n.cookies.values()[0]
        k = get("http://week-1.hgame.lwsec.cn:31772/api/getScore", headers=cookie)
        print(eval(k.text))
        if eval(k.text)['message'] == 100:
            print(k.cookies)