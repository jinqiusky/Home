# TVBoxOSC

![Build](https://shields.io/github/workflow/status/jinqiusky/Hometv1.0.0
/Test?logo=github&label=Build)
[![Channel](https://img.shields.io/badge/Follow-Telegram-blue.svg?logo=telegram)](https://t.me/TVBoxOSC)
[![Download](https://img.shields.io/github/v/release/jinqiusky/Hometv1.0.0?color=orange&logoColor=orange&label=Download&logo=DocuSign)](https://github.com/jinqiusky/Hometv1.0.0/releases/latest) 
[![Total](https://shields.io/github/downloads/jinqiusky/Hometv1.0.0/total?logo=Bookmeter&label=Counts&logoColor=yellow&color=yellow)](https://github.com/jinqiusky/Hometv1.0.0C/releases)

## Credits
This repo relies on the following third-party projects:
- [CatVodTVOfficial/TVBoxOSC](https://github.com/CatVodTVOfficial/TVBoxOSC)
- [hfr1107/Hometv1.0.0](https://github.com/q215613905/TVBoxOS) (Updated: ab16277159148d0ed7260e4ccfed9bc1682133a9)
- [mzlipro/boxce](https://github.com/mzlipro/boxce) (Updated: e02f6914653d8d9f7a844a207d3e25a29e97f71e)
# TV猫盒
## _在TV盒子里抓住了一直猫咪~o( =∩ω∩= )m_

[![N|Solid](https://raw.githubusercontent.com/kensonmiao/CatVodTVOSC/main/app/src/main/res/drawable/app_banner.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

## 功能

- 基本老猫功能
- 支持定义多JARs接口
- 可更换主界面样式 （集合式【完成】，老猫【完成】，安卓电视横屏滚动【开发中】）
- 剧集详细页长按集数或第三方播放器按钮可选择第三方播放器
- 推荐按钮

## Ver 0.7.20220722
## 额外新的参数如下

壁纸:
```javascript
{
    "wallpaper": "壁纸路径" //例子 "https://picsum.photos/1920/1080/?blur=10"
}
```

单Jar的定义方式不变，直接放路径即可:
```javascript
{
    ...
    "spider": "jar地址"
    ...
```

多Jars:
```javascript
{
    ...
    "spider": [
        { "n": "default", "v": "jar地址" }, //默认jar
        { "n": "jar1", "v": "jar1 地址" },
        { "n": "jar2", "v": "jar2 地址" }
        ...
    ],
    "sites": [
        ...
        { "key": "csp_csp1", "name": "CSP1", ..., "spider": "jar1" }, //对应spider里的n值
        { "key": "csp_csp2", "name": "CSP2", ..., "spider": "jar2" },
        { "key": "csp_csp3", "name": "CSP3", ... },  //没有spider参数的话，使用默认jar
        { "key": "csp_csp4", "name": "CSP4", ..., "spider": "jar2" },
        ...
    ],
    ...
}
```

