# TubiTV API接口


- [首页接口](#home)
- [电影](#list)
- [详情](#details)
- [搜索](#search)



<h2 id="home">首页</h2>

url：`https://uapi.adrise.tv/matrix/homescreen?app_id=tubitv&platform=android`

__拼接参数__：

- `app_id`：可选参数
- `platform`：平台，必选参数[amazon, android, androidtv, appletv, chromecast, comcast, cox, google, googletv, ios, ipad, iphone, ironsource, lg, opera, other, ps3, ps4, roku, samsung, sony, web, xbox, xboxone, xbox_one, tivo, yahoo, vizio, enseo, comcasthosp, telstra, echoshow]
- `device_id`:
- `limit`:
- `page_enabled`:`true` or `false`
- `user_id`:
- `expand`:


__示例__：
[https://uapi.adrise.tv/matrix/homescreen?platform=android](https://uapi.adrise.tv/matrix/homescreen?platform=android)

__json示例__：

```json

```



<h2 id="list">电影</h2>

url：`http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billCategory`

__拼接参数__：

- `format`：返回数据类型，可选择json，xml
- `calback`：callback


__示例__：
[http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billCategory](http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billCategory)

__json示例__：

```json

```



<h2 id="details">详情</h2>

url：`http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billCategory`

__拼接参数__：

- `format`：返回数据类型，可选择json，xml
- `calback`：callback


__示例__：
[http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billCategory](http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billCategory)

__json示例__：

```json

```



<h2 id="search">搜索</h2>

url：`http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billCategory`

__拼接参数__：

- `format`：返回数据类型，可选择json，xml
- `calback`：callback


__示例__：
[http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billCategory](http://tingapi.ting.baidu.com/v1/restserver/ting?method=baidu.ting.billboard.billCategory)

__json示例__：

```json

```