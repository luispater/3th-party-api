# Mob API接口

- [1 天气预报](#1)
	- [1.1 城市列表查询接口](#1.1)
	- [1.2 根据城市名查询天气](#1.2)
	- [1.3 根据IP查询天气](#1.3)
	- [1.4 空气质量查询](#1.4)
	- [1.5 空气质量城市列表接口](#1.5)
- [2 生活常用](#2)
	- [2.1 手机号码查询接口](#2.1)
	- [2.2 身份证信息](#2.2)
	- [2.3 IP地址查询](#2.3)
	- [2.4 基站定位查询](#2.4)
	- [2.5 万年历查询](#2.5)
- [3 邮编查询](#3)
	- [3.1 邮编查询接口](#3.1)
	- [3.2 邮编城市列表查询接口](#3.2)
	- [3.3 邮编城市列表查询接口](#3.3)
- [4 菜谱查询](#4)
	- [4.1 菜谱分类标签查询](#4.1)
	- [4.2 按标签查询菜谱接口](#4.2)
	- [4.3 菜谱查询接口](#4.3)
- [5 微信精选](#5)
	- [5.1 微信精选分类查询](#5.1)
	- [5.2 微信精选列表查询](#5.2)
- [6 驾考题库查询](#6)
	- [6.1 科目一题库列表查询接口](#6.1)
	- [6.2 科目四题库列表查询接口](#6.2)
	- [6.3 专项题库分类查询接口](#6.3)
	- [6.4 专项练习题库查询接口](#6.4)
- [7 汽车信息查询](#7)
	- [7.1 查询所有汽车品牌](#7.1)
	- [7.2 车型查询](#7.2)
	- [7.3 查询车型详细信息](#7.3)
- [8 休闲旅游](#8)
	- [8.1 周公解梦](#8.1)
	- [8.2 婚姻匹配](#8.2)
	- [8.3 手机号测吉凶](#8.3)
	- [8.4 八字算命](#8.4)
	- [8.5 老黄历](#8.5)



续。。。

<h2 id="1">天气预报</h2>

<h3 id="1.1">城市列表查询接口</h3>


__接口地址__：`http://apicloud.mob.com/v1/weather/citys`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/weather/citys?key=1af5f5c45b9f8](http://apicloud.mob.com/v1/weather/citys?key=1af5f5c45b9f8)

__备注说明__：`天气预报支持的城市`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	

__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
province	|string|	是	|省份	||
city	|array	|是|	城市	||
district|	array	|是	|区县	||

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": [
	        {
	            "city": [
	                {
	                    "city": "合肥",
	                    "district": [
	                        {
	                            "district": "合肥"
	                        },
	                        {
	                            "district": "长丰"
	                        },
	                        {
	                            "district": "肥东"
	                        },
	                        {
	                            "district": "肥西"
	                        },
	                        {
	                            "district": "巢湖"
	                        },
	                        {
	                            "district": "庐江"
	                        }
	                    ]
	                },
	                {
	                    "city": "蚌埠",
	                    "district": [
	                        {
	                            "district": "蚌埠"
	                        },
	                        {
	                            "district": "怀远"
	                        },
	                        {
	                            "district": "固镇"
	                        },
	                        {
	                            "district": "五河"
	                        }
	                    ]
	                },
	                {
	                    "city": "芜湖",
	                    "district": [
	                        {
	                            "district": "芜湖"
	                        },
	                        {
	                            "district": "繁昌"
	                        },
	                        {
	                            "district": "芜湖县"
	                        },
	                        {
	                            "district": "南陵"
	                        },
	                        {
	                            "district": "无为"
	                        }
	                    ]
	                },
	                {
	                    "city": "淮南",
	                    "district": [
	                        {
	                            "district": "淮南"
	                        },
	                        {
	                            "district": "凤台"
	                        },
	                        {
	                            "district": "潘集"
	                        }
	                    ]
	                },
	                {
	                    "city": "马鞍山",
	                    "district": [
	                        {
	                            "district": "马鞍山"
	                        },
	                        {
	                            "district": "当涂"
	                        },
	                        {
	                            "district": "含山"
	                        },
	                        {
	                            "district": "和县"
	                        }
	                    ]
	                }
	            ]
	        }
	    ]
	}

<h3 id="1.2">根据城市名查询天气</h3>

__接口地址__：`http://apicloud.mob.com/v1/weather/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/weather/query?key=1af5f5c45b9f8&city=通州&province=北京](http://apicloud.mob.com/v1/weather/query?key=1af5f5c45b9f8&city=通州&province=北京)

__备注说明__：`仅支持国内的天气查询，具体城市可根据支持的城市列表API来查询。可以通过城市名称进行查询。`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
city	|string	|是	|城市名（url编码）|	南京|
province	|string	|否	|当前城市的所属省份 如：北京-通州、江苏-通州（url编码）	|江苏|

__返回字段__：

|name	|type|	N	|D	|
|------|------|------|------|
retCode	|string	|是|	返回码	
msg	|string	|是|	返回说明	
result|	string|	是	|返回结果集	
airCondition	|string|	是	|空气质量	
city|	string	|是	|城市	
coldIndex	|string	|是|	感冒指数	
updateTime|	string	|是	|更新时间	
date|	string	|是	|日期	
distrct|	string	|是	|区县	
dressingIndex	|string	|是|	穿衣指数	
humidity	|string	|是	|湿度	
pollutionIndex|	string	|是|	空气质量指数	
province|	string|	是	|省份	
sunset|	string|	是	|日落时间	
sunrise|	string|	是	|日出时间	
temperature|	string|	是|	温度	
time	|string|	是	|时间	
washIndex|	string	|是	|洗车指数	
weather	|string	|是	|天气	
week	|string|	是	|星期	
wind	|string|	是	|风向	
exerciseIndex|	string|	是	|运动指数	
dayTime	|string	|是|	白天天气	
night|	string	|是	|晚上天气	

JSON返回示例：

	{
	    "msg": "success",
	    "result": [
	        {
	            "airCondition": "优",
	            "airQuality": {
	                "aqi": 25,
	                "city": "通州",
	                "district": "通州",
	                "fetureData": [
	                    {
	                        "aqi": 35,
	                        "date": "2018-09-08",
	                        "quality": "优"
	                    },
	                    {
	                        "aqi": 83,
	                        "date": "2018-09-09",
	                        "quality": "良"
	                    },
	                    {
	                        "aqi": 111,
	                        "date": "2018-09-10",
	                        "quality": "轻度污染"
	                    }
	                ],
	                "hourData": [
	                    {
	                        "aqi": 26,
	                        "dateTime": "2018-09-07 17:00:00"
	                    },
	                    {
	                        "aqi": 25,
	                        "dateTime": "2018-09-07 16:00:00"
	                    }
	                ],
	                "no2": 11,
	                "pm10": 24,
	                "pm25": 4,
	                "province": "北京",
	                "quality": "优",
	                "so2": 1,
	                "updateTime": "2018-09-07 17:00:00"
	            },
	            "city": "通州",
	            "coldIndex": "低发期",
	            "date": "2018-09-07",
	            "distrct": "通州",
	            "dressingIndex": "单衣类",
	            "exerciseIndex": "适宜",
	            "future": [
	                {
	                    "date": "2018-09-07",
	                    "dayTime": "晴",
	                    "night": "晴",
	                    "temperature": "27°C / 15°C",
	                    "week": "今天",
	                    "wind": "西北风 3～4级"
	                },
	                {
	                    "date": "2018-09-08",
	                    "dayTime": "多云",
	                    "night": "多云",
	                    "temperature": "27°C / 14°C",
	                    "week": "星期六",
	                    "wind": "北风 小于3级"
	                }
	            ],
	            "humidity": "湿度：27%",
	            "pollutionIndex": "25",
	            "province": "北京",
	            "sunrise": "04:49",
	            "sunset": "19:46",
	            "temperature": "25℃",
	            "time": "17:40",
	            "updateTime": "20180907180101",
	            "washIndex": "非常适宜",
	            "weather": "晴",
	            "week": "周五",
	            "wind": "西风3级"
	        }
	    ],
	    "retCode": "200"
	}


<h3 id="1.3">根据IP查询天气</h3>

__接口地址__：`http://apicloud.mob.com/v1/weather/ip`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/weather/ip?key=1af5f5c45b9f8&ip=115.239.210.27&province=浙江](http://apicloud.mob.com/v1/weather/ip?key=1af5f5c45b9f8&ip=115.239.210.27&province=浙江)

__备注说明__：`根据IP地址查询IP地址所在地的天气预报。`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
ip	|string	|是	|ip地址	|	115.239.210.27|
province	|string	|否	|当前城市的所属省份 如：北京-通州、江苏-通州（url编码）	|江苏|

__返回字段__：

|name	|type|	N	|D	|
|------|------|------|------|
retCode	|string	|是|	返回码	
msg	|string	|是|	返回说明	
msg	|string	|是|	返回说明	
result	|string|	是|	返回结果集	
airCondition	|string|	是|	空气质量	
city	|string|	是|	城市	
coldIndex	|string|	是|	感冒指数	
updateTime	|string	|是	|更新时间	
date	|string	|是	|日期	
distrct	|string|	是	|区县	
dressingIndex|	string|	是	|穿衣指数	
humidity|	string	|是|	湿度	
pollutionIndex	|string|	是	|空气污染指数
province	|string	|是	|省份	
sunset	|string	|是	|日落时间	
sunrise	|string|	是|	日出时间	
temperature	|string	|是	|温度	
time	|string	|是	|时间	
washIndex|	string	|是	|洗车指数	
weather	|string|	是	|天气	
week	|string	|是	|星期	
wind	|string	|是|	风向	
exerciseIndex	|string	|是	|运动指数
	
__JSON返回示例__：

	{
	    "msg": "success",
	    "result": [
	        {
	            "airCondition": "优",
	            "airQuality": {
	                "aqi": 46,
	                "city": "杭州",
	                "district": "杭州",
	                "fetureData": [
	                    {
	                        "aqi": 86,
	                        "date": "2018-09-08",
	                        "quality": "良"
	                    },
	                    {
	                        "aqi": 80,
	                        "date": "2018-09-09",
	                        "quality": "良"
	                    }
	                ],
	                "hourData": [
	                    {
	                        "aqi": 46,
	                        "dateTime": "2018-09-07 17:00:00"
	                    },
	                    {
	                        "aqi": 45,
	                        "dateTime": "2018-09-07 16:00:00"
	                    },
	                    {
	                        "aqi": 42,
	                        "dateTime": "2018-09-07 15:00:00"
	                    }
	                ],
	                "no2": 32,
	                "pm10": 45,
	                "pm25": 32,
	                "province": "浙江",
	                "quality": "优",
	                "so2": 6,
	                "updateTime": "2018-09-07 17:00:00"
	            },
	            "city": "杭州",
	            "coldIndex": "低发期",
	            "date": "2018-09-07",
	            "distrct": "杭州",
	            "dressingIndex": "薄短袖类",
	            "exerciseIndex": "适宜",
	            "future": [
	                {
	                    "date": "2018-09-07",
	                    "dayTime": "阵雨",
	                    "night": "阵雨",
	                    "temperature": "26°C / 21°C",
	                    "week": "今天",
	                    "wind": "北风 4～5级"
	                },
	                {
	                    "date": "2018-09-08",
	                    "dayTime": "阴",
	                    "night": "阴",
	                    "temperature": "27°C / 20°C",
	                    "week": "星期六",
	                    "wind": "北风 3～4级"
	                }
	            ],
	            "humidity": "湿度：81%",
	            "pollutionIndex": "46",
	            "province": "浙江",
	            "sunrise": "05:11",
	            "sunset": "19:01",
	            "temperature": "23℃",
	            "time": "17:42",
	            "updateTime": "20180907175945",
	            "washIndex": "不适宜",
	            "weather": "阴",
	            "week": "周五",
	            "wind": "东风1级"
	        }
	    ],
	    "retCode": "200"
	}


<h3 id="1.4">空气质量查询</h3>


__接口地址__：`http://apicloud.mob.com/environment/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/environment/query?key=1af5f5c45b9f8&city=海淀&province=北京](http://apicloud.mob.com/environment/query?key=1af5f5c45b9f8&city=海淀&province=北京)

__备注说明__：`提供城市实时和未来几天的空气质量情况`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	
city	|string	|是	|城市或地区名字	||
province|	string	|否	|当前城市的所属省份 |北京-通州、江苏-通州（url编码）

__返回字段__：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                        <tr>
<td>retCode</td>
<td>string</td>
<td>是</td>
<td>返回码</td>
<td></td>
</tr>
                        <tr>
<td>msg</td>
<td>string</td>
<td>是</td>
<td>返回说明</td>
<td></td>
</tr>
                        <tr>
<td>retCode</td>
<td>string</td>
<td>是</td>
<td>返回结果集</td>
<td></td>
</tr>
                        <tr>
<td>aqi</td>
<td>int</td>
<td>是</td>
<td>空气质量指数</td>
<td></td>
</tr>
                        <tr>
<td>city</td>
<td>string</td>
<td>是</td>
<td>城市</td>
<td></td>
</tr>
                        <tr>
<td>district</td>
<td>string</td>
<td>是</td>
<td>区县</td>
<td></td>
</tr>
                        <tr>
<td>no2</td>
<td>int</td>
<td>是</td>
<td>污染物no2</td>
<td></td>
</tr>
                        <tr>
<td>pm25</td>
<td>int</td>
<td>是</td>
<td>污染物pm2.5</td>
<td></td>
</tr>
                        <tr>
<td>so2</td>
<td>int</td>
<td>是</td>
<td>污染物so2</td>
<td></td>
</tr>
                        <tr>
<td>province</td>
<td>string</td>
<td>是</td>
<td>省份</td>
<td></td>
</tr>
                        <tr>
<td>updateTime</td>
<td>string</td>
<td>是</td>
<td>更新时间</td>
<td></td>
</tr>
                        <tr>
<td>quality</td>
<td>string</td>
<td>是</td>
<td>空气质量</td>
<td></td>
</tr>
                        <tr>
<td>fetureData</td>
<td>array</td>
<td>是</td>
<td>未来几天数据</td>
<td></td>
</tr>
                        <tr>
<td>date</td>
<td>string</td>
<td>是</td>
<td>日期</td>
<td></td>
</tr>
                        <tr>
<td>quality</td>
<td>string</td>
<td>是</td>
<td>空气质量</td>
<td></td>
</tr>
                        <tr>
<td>hourData</td>
<td>array</td>
<td>是</td>
<td>空气质量指数小时数据</td>
<td></td>
</tr>
                        <tr>
<td>dateTime</td>
<td>string</td>
<td>是</td>
<td>时间</td>
<td></td>
</tr>
</tbody></table>

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": [
	        {
	            "aqi": 53,
	            "city": "海淀",
	            "district": "海淀",
	            "fetureData": [
	                {
	                    "aqi": 66,
	                    "date": "2018-09-10",
	                    "quality": "良"
	                },
	                {
	                    "aqi": 82,
	                    "date": "2018-09-11",
	                    "quality": "良"
	                },
	                {
	                    "aqi": 110,
	                    "date": "2018-09-12",
	                    "quality": "轻度污染"
	                },
	                {
	                    "aqi": 83,
	                    "date": "2018-09-13",
	                    "quality": "良"
	                },
	                {
	                    "aqi": 58,
	                    "date": "2018-09-14",
	                    "quality": "良"
	                },
	                {
	                    "aqi": 51,
	                    "date": "2018-09-15",
	                    "quality": "良"
	                }
	            ],
	            "hourData": [
	                {
	                    "aqi": 53,
	                    "dateTime": "2018-09-09 09:00:00"
	                },
	                {
	                    "aqi": 56,
	                    "dateTime": "2018-09-09 08:00:00"
	                },
	                {
	                    "aqi": 52,
	                    "dateTime": "2018-09-09 07:00:00"
	                }
	            ],
	            "no2": 39,
	            "pm10": 57,
	            "pm25": 22,
	            "province": "北京",
	            "quality": "良",
	            "so2": 3,
	            "updateTime": "2018-09-09 09:00:00"
	        }
	    ],
	    "retCode": "200"
	}


<h3 id="1.5">空气质量查询城市列表接口</h3>


__接口地址__：`http://apicloud.mob.com/environment/citys`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/environment/citys?key=1af5f5c45b9f8](http://apicloud.mob.com/environment/citys?key=1af5f5c45b9f8)

__备注说明__：`空气质量支持的城市列表`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||

__返回字段__：

<table>
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr><tr>
<td>retCode</td>
<td>string</td>
<td>是</td>
<td>返回码</td>
<td></td>
</tr><tr>
<td>msg</td>
<td>string</td>
<td>是</td>
<td>返回说明</td>
<td></td>
</tr><tr>
<td>result</td>
<td>string</td>
<td>是</td>
<td>返回结果集</td>
<td></td>
</tr> <tr>
<td>province</td>
<td>string</td>
<td>是</td>
<td>省份</td>
<td></td>
</tr><tr>
<td>city</td>
<td>string</td>
<td>是</td>
<td>城市</td>
<td></td>
</tr> <tr>
<td>district</td>
<td>string</td>
<td>是</td>
<td>区县</td>
<td></td>
</tr>
</tbody></table>
                                                    
__JSON返回示例__：

```
{
    "msg": "success",
    "result": [
        {
            "city": [
                {
                    "city": "合肥",
                    "district": [
                        {
                            "district": "合肥"
                        },
                        {
                            "district": "长丰"
                        },
                        {
                            "district": "肥东"
                        },
                        {
                            "district": "肥西"
                        },
                        {
                            "district": "巢湖"
                        },
                        {
                            "district": "庐江"
                        }
                    ]
                },
                {
                    "city": "安庆",
                    "district": [
                        {
                            "district": "安庆"
                        },
                        {
                            "district": "枞阳"
                        },
                        {
                            "district": "太湖"
                        },
                        {
                            "district": "潜山"
                        },
                        {
                            "district": "怀宁"
                        },
                        {
                            "district": "宿松"
                        },
                        {
                            "district": "望江"
                        },
                        {
                            "district": "岳西"
                        },
                        {
                            "district": "桐城"
                        }
                    ]
                },
                {
                    "city": "铜陵",
                    "district": [
                        {
                            "district": "铜陵"
                        }
                    ]
                }
            ],
            "province": "安徽"
        }
    ],
    "retCode": "200"
}
```

<h2 id="2">手机号码归属地</h2>

<h3 id="2.1">手机号码查询接口</h3>


__接口地址__：`http://apicloud.mob.com/v1/mobile/address/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/mobile/address/query?key=1af5f5c45b9f8&phone=13300001982](http://apicloud.mob.com/v1/mobile/address/query?key=1af5f5c45b9f8&phone=13300001982)

__备注说明__：`仅支持国内的手机号码查询，具体城市可根据支持的城市列表API来查询。可以通过城市名称进行查询。`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
phone	|int|	是	|要查询的手机号码	|13300001982

__返回字段__：

|name	|type|	N	|D	|
|------|------|------|------|
retCode	|string|	是	|返回码	
msg	|string	|是	|返回说明	
result	|string|	是	|返回结果集	
province|	string	|是	|省份	
city	|string	|是|城市	
cityCode|	string	|是	|城市区号	
mobileNumber	|string	|是	|手机号前7位	
zipCode	|string	|是|	邮编	
operator	|string	|是	|运营商信息

__JSON返回示例__：


	{
	    "msg": "success",
	    "result": {
	        "city": "南宁市",
	        "cityCode": "0771",
	        "mobileNumber": "1330000",
	        "operator": "电信CDMA卡",
	        "province": "广西",
	        "zipCode": "530000"
	    },
	    "retCode": "200"
	}

<h3 id="2.2">身份证信息查询接口</h3>


__接口地址__：`http://apicloud.mob.com/idcard/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/idcard/query?key=1af5f5c45b9f8&cardno=45102519800411512X](http://apicloud.mob.com/idcard/query?key=1af5f5c45b9f8&cardno=45102519800411512X)

__备注说明__：`查询身份证的基本信息`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
cardno	|string	|是	|身份证号码|

__返回参数__:

|name	|type|	N	|D	|
|------|------|------|------|
retCode|	string|	是	|返回码	
msg	|string|	是|	返回说明	
result	|string	|是|	返回结果集	
area	|string	|是|	身份证所属地区	
birthday	|string	|是	|生日	
sex	|string	|是	|性别

__JSON返回示例__:

	{
	    "msg": "success",
	    "result": {
	        "area": "广西壮族自治区百色市靖西县",
	        "birthday": "1980年04月11日",
	        "sex": "女"
	    },
	    "retCode": "200"
	}


<h3 id="2.3">IP地址查询接口</h3>


__接口地址__：`http://apicloud.mob.com/ip/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/station/query?key=1af5f5c45b9f8&ip=222.73.199.34](http://apicloud.mob.com/station/query?key=1af5f5c45b9f8&ip=222.73.199.34)

__备注说明__：`根据IP地址查询对应的省市区信息`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
ip	|string	|是	|要查询的IP地址||

__返回参数__:

|name	|type|	N	|D	|value|
|------|------|------|------|------|
retCode|	string|	是	|返回码	
msg	|string|	是|	返回说明	
result	|string	|是|	返回结果集	
ip	|string|	是	|查询的ip地址	|
country|	string	|是	|国家|	
province|	string|	是|	省	|
city	|string|	是	|市	|
district	|string	|是	|区|

__JSON返回示例__:

	{
	    "msg": "success",
	    "result": {
	        "city": "上海",
	        "country": "中国",
	        "ip": "222.73.199.34",
	        "province": "上海"
	    },
	    "retCode": "200"
	}


<h3 id="2.4">基站定位查询接口</h3>


__接口地址__：`http://apicloud.mob.com/station/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/station/query?key=1af5f5c45b9f8&mcc=460&mnc=0&lac=34860&cell=62041](http://apicloud.mob.com/station/query?key=1af5f5c45b9f8&mcc=460&mnc=0&lac=34860&cell=62041)

__备注说明__：`通过MNC、LAC、CELL 进行基站定位查询，覆盖全国移动、联通、电信基站数据`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
mcc|	int	|否	|移动设备国家代码（默认中国 = 460）|
mnc	|int|	是	|移动设备网络代码(中国移动 = 0/2/7, 中国联通 = 1/6, 中国电信 = 3/5)|
lac|	long	|是|	位置区码|	
cell|	long	|是	|基站小区号|

__返回字段__：

|name	|type|	N	|D	|
|------|------|------|------|
retCode	|string	|是	|返回码	
msg|	string|	是	|返回说明	
result|	string|	是	|返回结果集	
lat	|double	|是|	纬度	
googleLat|	double	|是|	google地图纬度	
googleLng|	double|	是|	google地图经度	
precision|	double|	是	|覆盖范围（单位/米）
addr	|string	|是|	基站位置	
lng	|double|	是	|经度

__JSON返回示例__:

	{
	    "msg": "success",
	    "result": {
	        "addr": "云南省西双版纳傣族自治州景洪市嘎洒镇傣家印象西,026乡道西南约348米",
	        "cell": 62041,
	        "googleLat": 22.01428,
	        "googleLng": 100.752143,
	        "id": "0_34860_62041",
	        "lac": 34860,
	        "lat": 22.0171,
	        "lng": 100.751,
	        "mcc": 460,
	        "mnc": 0,
	        "precision": 1500
	    },
	    "retCode": "200"
	}

<h3 id="2.5">万年历查询接口</h3>


__接口地址__：`http://apicloud.mob.com/appstore/calendar/day`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/appstore/calendar/day?key=1af5f5c45b9f8&date=2015-05-01](http://apicloud.mob.com/appstore/calendar/day?key=1af5f5c45b9f8&date=2015-05-01)

__备注说明__：`支持通过指定日期获得万年历的数据`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
date |	string|	是|	日期|	2015-05-01


__返回字段__：

|name	|type|	N	|D	|
|------|------|------|------|
retCode	|string	|是	|返回码	
msg|	string|	是	|返回说明	
result|	string|	是	|返回结果集	
avoid|	string|	是	|不宜/忌	|
date|	string|	是	|日期	|
holiday	|string	|否	|节假日(不是节假日的日期数据为空)|
lunar|	string|	是	|农历日期	|
lunarYear|	string|	是|	农历年	|
suit|	string	|是	|宜|	
weekday	|string	|是|	星期几	|
zodiac	|string|	是|	生肖|

__JSON返回示例__:

	{
	    "msg": "success",
	    "result": {
	        "avoid": "诉讼 诉讼 ",
	        "date": "2018-09-09",
	        "holiday": "毛泽东逝世纪念",
	        "lunar": "七月卅十",
	        "lunarHoliday": "地藏菩萨诞",
	        "lunarYear": "戊戌",
	        "suit": "入学 开市 入学 嫁娶 上官 赴任 婚礼 造作 动土 旅行 ",
	        "weekday": "星期日",
	        "zodiac": "狗"
	    },
	    "retCode": "200"
	}

<h2 id="3">邮编查询</h2>

<h3 id="3.1">邮编查询接口</h3>


__接口地址__：`http://apicloud.mob.com/v1/postcode/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/postcode/query?key=1af5f5c45b9f8&code=102629](http://apicloud.mob.com/v1/postcode/query?key=1af5f5c45b9f8&code=102629)

__备注说明__：`通过邮编查询对应的地名`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
code	|int|	是	|邮政编码	| 102629

__返回字段__：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
    <th>name</th>
    <th>type</th>
    <th>N</th>
    <th>D</th>
    <th>value</th>
</tr><tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr><tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td>
</tr><tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr><tr>
    <td>address</td>
    <td>string</td>
    <td>是</td>
    <td>地址数组</td>
    <td></td>
</tr><tr>
    <td>province</td>
    <td>string</td>
    <td>是</td>
    <td>省份</td>
    <td></td>
</tr> <tr>
    <td>city</td>
    <td>string</td>
    <td>是</td>
    <td>城市</td>
    <td></td>
</tr> <tr>
    <td>district</td>
    <td>string</td>
    <td>是</td>
    <td>区县</td>
    <td></td>
</tr> <tr>
    <td>PostNumber</td>
    <td>string</td>
    <td>是</td>
    <td>邮编</td>
    <td></td>
</tr> <tr>
    <td>size</td>
    <td>string</td>
    <td>是</td>
    <td>address数组长度</td>
    <td></td>
</tr>
</tbody></table>


__JSON返回示例__：


	{
	    "msg": "success",
	    "result": {
	        "address": [
	            "黄良路",
	            "天河西路",
	            "黄村镇宋庄",
	            "黄村镇太福庄",
	            "黄村镇大庄村",
	            "北臧村镇砖楼",
	            "北臧村镇西大营",
	            "黄村镇韩园子村",
	            "北臧村镇新立村",
	            "北臧村镇六合庄"
	        ],
	        "city": "北京市",
	        "district": "大兴区",
	        "postNumber": "102629",
	        "province": "北京市",
	        "size": "10"
	    },
	    "retCode": "200"
	}


<h3 id="3.2">邮编城市列表查询接口</h3>


__接口地址__：`http://apicloud.mob.com/v1/postcode/pcd`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/postcode/pcd?key=appkey](http://apicloud.mob.com/v1/postcode/pcd?key=1af5f5c45b9f8)

__备注说明__：`返回省份、城市、地区（县）关联的列表`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||

__返回字段__：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
<tr>
<td>retCode</td>
<td>string</td>
<td>是</td>
<td>返回码</td>
<td></td>
</tr>
<tr>
<td>msg</td>
<td>string</td>
<td>是</td>
<td>返回说明</td>
<td></td>
</tr>
<tr>
<td>result</td>
<td>string</td>
<td>是</td>
<td>返回结果集</td>
<td></td>
</tr>
<tr>
<td>address</td>
<td>array</td>
<td>是</td>
<td>地址数组</td>
<td></td>
</tr>
<tr>
<td>province</td>
<td>string</td>
<td>是</td>
<td>省份</td>
<td></td>
</tr>
<tr>
<td>id(province)</td>
<td>string</td>
<td>是</td>
<td>省份ID</td>
<td></td>
</tr>
<tr>
<td>city</td>
<td>string</td>
<td>是</td>
<td>城市</td>
<td></td>
</tr>
<tr>
<td>id(city)</td>
<td>string</td>
<td>是</td>
<td>城市ID</td>
<td></td>
</tr>
<tr>
<td>district</td>
<td>string</td>
<td>是</td>
<td>区县</td>
<td></td>
</tr>
<tr>
<td>id(district)</td>
<td>string</td>
<td>是</td>
<td>区县ID</td>
<td></td>
</tr>
</tbody></table>

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": [
	        {
	            "city": [
	                {
	                    "city": "北京市",
	                    "district": [
	                        {
	                            "district": "石景山区",
	                            "id": "10010"
	                        },
	                        {
	                            "district": "门头沟区",
	                            "id": "10011"
	                        },
	                        {
	                            "district": "朝阳区",
	                            "id": "10012"
	                        }
	                    ],
	                    "id": "1001"
	                }
	            ],
	            "id": "10",
	            "province": "北京市"
	        }
	    ],
	    "retCode": "200"
	}


<h3 id="3.3">邮编城市列表查询接口</h3>


__接口地址__：`http://apicloud.mob.com/v1/postcode/search`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/postcode/search?key=appkey&pid=40&cid=4001&word=安康](http://apicloud.mob.com/v1/postcode/search?key=1af5f5c45b9f8&pid=40&cid=4001&word=安康)

__备注说明__：`返回省份、城市、地区（县）关联的列表`

__请求参数__：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                            <tr>
    <td>key</td>
    <td>string</td>
    <td>是</td>
    <td>用户申请的appkey</td>
    <td></td>
</tr>
                            <tr>
    <td>pid</td>
    <td>int</td>
    <td>是</td>
    <td>省份ID</td>
    <td>40</td>
</tr>
                            <tr>
    <td>cid</td>
    <td>int</td>
    <td>是</td>
    <td>城市ID</td>
    <td>4001</td>
</tr>
                            <tr>
    <td>did</td>
    <td>int</td>
    <td>否</td>
    <td>区域ID</td>
    <td></td>
</tr>
                            <tr>
    <td>word</td>
    <td>string</td>
    <td>否</td>
    <td>关键字(url编码)</td>
    <td>安康</td>
</tr>
</tbody></table>

__返回字段__：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                            <tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr>
                            <tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td>
</tr>
                            <tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr>
                            <tr>
    <td>address</td>
    <td>string</td>
    <td>是</td>
    <td>地址数组</td>
    <td></td>
</tr>
                            <tr>
    <td>province</td>
    <td>string</td>
    <td>是</td>
    <td>省份</td>
    <td></td>
</tr>
                            <tr>
    <td>city</td>
    <td>string</td>
    <td>是</td>
    <td>城市</td>
    <td></td>
</tr>
                            <tr>
    <td>district</td>
    <td>string</td>
    <td>是</td>
    <td>区县</td>
    <td></td>
</tr>
                            <tr>
    <td>postNumber</td>
    <td>string</td>
    <td>是</td>
    <td>邮编</td>
    <td></td>
</tr>
                            <tr>
    <td>size</td>
    <td>string</td>
    <td>是</td>
    <td>address数组长度</td>
    <td></td>
</tr>
</tbody></table>


__JSON返回示例__：

	{
	    "msg": "success",
	    "result": [
	        {
	            "address": [
	                "葡萄街",
	                "沟西路",
	                "北塔街",
	                "警民路",
	                "南屏街",
	                "中枢路",
	                "站前街",
	                "沙雅路",
	                "西园街",
	                "东林街",
	                "安康路",
	                "中枢北路",
	                "铁三小路",
	                "西站七街",
	                "西站五街",
	                "西站八街",
	                "西站六街",
	                "机务段路",
	                "车辆段路",
	                "北站公路",
	                "小地窝村",
	                "西站十二街",
	                "西站十四街",
	                "西站十一街",
	                "西站十五街",
	                "三十五户路",
	                "8街8街住宅小区",
	                "5街5街住宅小区",
	                "6街6街住宅小区",
	                "11街11街住宅小区",
	                "头屯河农场王家沟6队",
	                "12街12街住宅小区",
	                "15街15街住宅小区",
	                "14街14街住宅小区",
	                "乌昌路(10号，18号#)"
	            ],
	            "cId": "4001",
	            "city": "乌鲁木齐市",
	            "dId": "40011",
	            "district": "头屯河区",
	            "pId": "40",
	            "postNumber": "830023",
	            "province": "新疆维吾尔自治区",
	            "size": "35"
	        }
	    ],
	    "retCode": "200"
	}


<h2 id="4">菜谱查询</h2>

<h3 id="4.1">菜谱分类标签查询</h3>


__接口地址__：`http://apicloud.mob.com/v1/cook/category/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/cook/category/query?key=1af5f5c45b9f8](http://apicloud.mob.com/v1/cook/category/query?key=1af5f5c45b9f8)

__备注说明__：`查询菜谱的所有分类`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	

__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
ctgId	|string|	是	|分类ID	||
name	| string	|是|	分类描述		||
parentId |	string	|是	|上层分类ID	||

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": {
	        "categoryInfo": {
	            "ctgId": "0010001001",
	            "name": "全部菜谱"
	        },
	        "childs": [
	            {
	                "categoryInfo": {
	                    "ctgId": "0010001002",
	                    "name": "按菜品选择菜谱",
	                    "parentId": "0010001001"
	                },
	                "childs": [
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001007",
	                            "name": "荤菜",
	                            "parentId": "0010001002"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001008",
	                            "name": "素菜",
	                            "parentId": "0010001002"
	                        }
	                    }
	                ]
	            },
	            {
	                "categoryInfo": {
	                    "ctgId": "0010001003",
	                    "name": "按工艺选择菜谱",
	                    "parentId": "0010001001"
	                },
	                "childs": [
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001015",
	                            "name": "红烧",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001016",
	                            "name": "炒",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001017",
	                            "name": "煎",
	                            "parentId": "0010001003"
	                        }
	                    }
	                ]
	            },
	            {
	                "categoryInfo": {
	                    "ctgId": "0010001004",
	                    "name": "按菜系选择菜谱",
	                    "parentId": "0010001001"
	                },
	                "childs": [
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001030",
	                            "name": "鲁菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001031",
	                            "name": "川菜",
	                            "parentId": "0010001004"
	                        }
	                    }
	                ]
	            },
	            {
	                "categoryInfo": {
	                    "ctgId": "0010001005",
	                    "name": "按人群选择菜谱",
	                    "parentId": "0010001001"
	                },
	                "childs": [
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001047",
	                            "name": "孕妇食谱",
	                            "parentId": "0010001005"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001048",
	                            "name": "婴幼食谱",
	                            "parentId": "0010001005"
	                        }
	                    }
	                ]
	            },
	            {
	                "categoryInfo": {
	                    "ctgId": "0010001006",
	                    "name": "按功能选择菜谱",
	                    "parentId": "0010001001"
	                },
	                "childs": [
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001056",
	                            "name": "减肥",
	                            "parentId": "0010001006"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001057",
	                            "name": "便秘",
	                            "parentId": "0010001006"
	                        }
	                    }
	                ]
	            }
	        ]
	    },
	    "retCode": "200"
	}


<h3 id="4.2">按标签查询菜谱接口</h3>


__接口地址__：`http://apicloud.mob.com/v1/cook/menu/search`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/cook/menu/search?key=1af5f5c45b9f8&cid=0010001007&page=1&size=20](http://apicloud.mob.com/v1/cook/menu/search?key=1af5f5c45b9f8&cid=0010001007&page=1&size=20)

__备注说明__：`查询菜谱的所有分类`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	
cid|	string	|否	|标签ID(末级分类标签)	|0010001007
name|	string	|否	|菜谱名称	|红烧肉
page|	int	|否	|起始页(默认1)	|1
size|	int|	否|	返回数据条数(默认20)|	20

__返回字段__：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                            <tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr>
                            <tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td>
</tr>
                            <tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr>
                            <tr>
    <td>total</td>
    <td>int</td>
    <td>是</td>
    <td>菜谱总条数</td>
    <td></td>
</tr>
                            <tr>
    <td>curPage</td>
    <td>int</td>
    <td>是</td>
    <td>当前页</td>
    <td></td>
</tr>
                            <tr>
    <td>ctgIds</td>
    <td>array</td>
    <td>是</td>
    <td>分类ID</td>
    <td></td>
</tr>
                            <tr>
    <td>ctgTitles</td>
    <td>string</td>
    <td>是</td>
    <td>分类标签</td>
    <td></td>
</tr>
                            <tr>
    <td>menuId</td>
    <td>string</td>
    <td>是</td>
    <td>菜谱id</td>
    <td></td>
</tr>
                            <tr>
    <td>recipe</td>
    <td>string</td>
    <td>是</td>
    <td>制作步骤</td>
    <td></td>
</tr>
                            <tr>
    <td>thumbnail</td>
    <td>string</td>
    <td>是</td>
    <td>预览图地址</td>
    <td></td>
</tr>
</tbody></table>

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": {
	        "curPage": 1,
	        "list": [
	            {
	                "ctgIds": [
	                    "0010001007",
	                    "0010001020",
	                    "0010001038",
	                    "0010001063"
	                ],
	                "ctgTitles": "荤菜,炖,京菜,养生",
	                "menuId": "00100010070000017758",
	                "name": "腔骨萝卜汤",
	                "recipe": {
	                    "ingredients": "[\"猪腔骨500g，最好是在超市现买的新鲜腔骨，\",\"白萝卜一整个，大概1000g\",\"超市买的炖肉料两小包,整包是五六块钱；也可以用香叶3片、桂皮5克、丁香3克、肉桂2克、大料10瓣、花椒10克制作成料包\",\"葱30克、姜20克、蒜2头\"]",
	                    "method": "[{\"step\":\"1.大葱一根，切成七八厘米的葱段姜蒜若干，切成蒜瓣，姜片\"},{\"step\":\"2.腔骨在买时，就让老板给切成一节一节的小块，用冷水放在炖锅里，放入葱段，姜片，炖肉料\"},{\"step\":\"3.用小火开始烧,这样可以保证肉嫩\"},{\"step\":\"4.炖二十分钟后，将白萝卜块放入锅中一起炖，火可以开到中火，但是小心汤溢出来\"},{\"step\":\"5.再四十分钟后，放入适量盐，尝尝肉如果熟了 ，萝卜如果烂了，就可以出锅啦\"}]",
	                    "sumary": "猪腔骨骨头多肉少，很适合拿来炖汤，如果在配上能够润肺的白萝卜，就更爽啦！！",
	                    "title": "怎样做出浓郁的腔骨萝卜汤"
	                }
	            },
	            {
	                "ctgIds": [
	                    "0010001007",
	                    "0010001025",
	                    "0010001031",
	                    "0010001063"
	                ],
	                "ctgTitles": "荤菜,煮,川菜,养生",
	                "menuId": "00100010070000017757",
	                "name": "川式水煮鱼",
	                "recipe": {
	                    "method": "[{\"step\":\"1.开始动手了: 1.将鱼头剁下,并从中分两半; 2.将鱼身平放用锋利的刀平着将两大片鱼肉和鱼排分开; 3.继续将两大片鱼肉片成适量的鱼片; 4.将鱼排分为三四段与鱼头放一起备用; 5.将鱼片内放一个蛋清,少许盐,干淀粉和料酒,拌匀(最好用手抓匀);\"},{\"step\":\"2.可以动火了: 1.将一小碗色拉油,所有花椒和辣椒倒入锅内,用小火慢炸; 2.在辣椒变色后,用铲子捞出一半的油和花椒辣椒,备用; 3.将火开大,放入拍好的蒜瓣儿和姜片儿,出香味后,将鱼头鱼排入锅; 4.翻炒两下,倒入料酒约一小晚,盐半调羹,加沸水三四碗; 5.等鱼头汤沸腾出味,将鱼片一片一片平放到出水滚的汤中; 6.鱼片会熟的很快,出锅前放入适量鸡精,白胡椒粉和椒盐粉;\"},{\"step\":\"3.终于可以盛盆了: 1.一定要用够大的盆(也可考虑用电火锅),盆中放着已抄好的黄豆芽和榨菜; 2.将鱼片一系列汤汤水水倒入此盆; 3.最后将那半碗捞出的辣椒和油倒在上面;\"}]",
	                    "sumary": "制作前备料:",
	                    "title": "怎样做川式水煮鱼?"
	                }
	            }
	        ],
	        "total": 17758
	    },
	    "retCode": "200"
	}

<h3 id="4.3">菜谱查询接口</h3>


__接口地址__：`http://apicloud.mob.com/v1/cook/menu/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/v1/cook/menu/query?key=1af5f5c45b9f8&id=00100010070000000001](http://apicloud.mob.com/v1/cook/menu/query?key=1af5f5c45b9f8&id=00100010070000000001)

__备注说明__：`查询菜谱的所有分类`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	
id|	string	|是	|菜谱ID	| 00100010070000000001

__返回字段__：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                            <tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr>
                            <tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td>
</tr>
                            <tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr>
                            <tr>
    <td>ctgIds</td>
    <td>array</td>
    <td>是</td>
    <td>分类ID</td>
    <td></td>
</tr>
                            <tr>
    <td>ctgTitles</td>
    <td>string</td>
    <td>是</td>
    <td>分类标签</td>
    <td></td>
</tr>
                            <tr>
    <td>menuId</td>
    <td>string</td>
    <td>是</td>
    <td>菜谱id</td>
    <td></td>
</tr>
                            <tr>
    <td>recipe</td>
    <td>string</td>
    <td>是</td>
    <td>制作步骤</td>
    <td></td>
</tr>
                            <tr>
    <td>thumbnail</td>
    <td>string</td>
    <td>是</td>
    <td>预览图地址</td>
    <td></td>
</tr>
                            <tr>
    <td>name</td>
    <td>string</td>
    <td>是</td>
    <td>菜谱名称</td>
    <td></td>
</tr></tbody></table>

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": {
	        "ctgIds": [
	            "0010001007",
	            "0010001016",
	            "0010001034",
	            "0010001049",
	            "0010001063"
	        ],
	        "ctgTitles": "荤菜,炒,浙菜,儿童食谱,养生",
	        "menuId": "00100010070000000001",
	        "name": "三色炒虾仁",
	        "recipe": {
	            "img": "http://f2.mob.com/null/2015/08/18/1439876711867.jpg",
	            "ingredients": "[\"虾仁350g、油1大勺、盐1小勺、白酒1小勺、淀粉2小勺、黄瓜30g、胡萝卜30g、玉米粒30g\"]",
	            "method": "[{\"img\":\"http://f2.mob.com/null/2015/08/18/1439876712533.jpg\",\"step\":\"1.虾仁清洗干净，去掉虾线\"},{\"img\":\"http://f2.mob.com/null/2015/08/18/1439876713007.jpg\",\"step\":\"2.加入1小勺盐\"},{\"img\":\"http://f2.mob.com/null/2015/08/18/1439876713790.jpg\",\"step\":\"3.加入1小勺白酒拌匀，腌制15分钟。\"},{\"img\":\"http://f2.mob.com/null/2015/08/18/1439876715218.jpg\",\"step\":\"4.腌制好的虾仁加入2小勺淀粉抓拌均匀\"},{\"img\":\"http://f2.mob.com/null/2015/08/18/1439876715861.jpg\",\"step\":\"5.胡萝卜和黄瓜洗净切小丁。\"},{\"img\":\"http://f2.mob.com/null/2015/08/18/1439876716477.jpg\",\"step\":\"6.锅中加入1大勺油，油热后下锅滑炒虾仁，虾仁变色后即可捞出\"},{\"img\":\"http://f2.mob.com/null/2015/08/18/1439876717026.jpg\",\"step\":\"7.另起锅加入少许油，将胡萝卜和黄瓜丁下锅炒至断生\"},{\"img\":\"http://f2.mob.com/null/2015/08/18/1439876717929.jpg\",\"step\":\"8.加入少许盐，加入玉米粒翻炒\"},{\"img\":\"http://f2.mob.com/null/2015/08/18/1439876718385.jpg\",\"step\":\"9.然后加入事先炒好的虾仁，翻炒均匀，即可关火，一道美味的虾仁就出来啦\"}]",
	            "sumary": "鲜虾中含有丰富的钾、碘、镁、磷等矿物质及多种维生素，尤其是它特有的虾青素，是目前发现的最强的一种抗氧化剂，所以虾是对人体十分有益的食材。这是一道以虾仁为主要材料炒制的菜肴。炒虾仁因其清淡爽口，易于消化，老幼皆宜，而深受食客欢迎，它的配料可以随个人喜好而变化，做法多样，我今天就加入了玉米、胡萝卜和黄瓜，不但颜色好看，而且口感丰富，一看就让人食欲大开，还能摄取多种营养。",
	            "title": "怎样做一道好吃的三色炒虾仁"
	        },
	        "thumbnail": "http://f2.mob.com/null/2015/08/18/1439876700896.jpg"
	    },
	    "retCode": "200"
	}


<h2 id="5">微信精选</h2>

<h3 id="5.1">微信精选分类查询</h3>


__接口地址__：`http://apicloud.mob.com/wx/article/category/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/wx/article/category/query?key=1af5f5c45b9f8](http://apicloud.mob.com/wx/article/category/query?key=1af5f5c45b9f8)

__备注说明__：`查询菜谱的所有分类`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	

__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
cid	|string|	是	|分类ID	||
name	| string	|是|	分类名称		||

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": [
	        {
	            "cid": "1",
	            "name": "时尚"
	        },
	        {
	            "cid": "2",
	            "name": "热点"
	        },
	        {
	            "cid": "3",
	            "name": "健康"
	        }
	    ],
	    "retCode": "200"
	}

<h3 id="5.2">微信精选列表查询</h3>


__接口地址__：`http://apicloud.mob.com/wx/article/search`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/wx/article/search?key=1af5f5c45b9f8&cid=1](http://apicloud.mob.com/wx/article/search?key=1af5f5c45b9f8&cid=1)

__备注说明__：`查询菜谱的所有分类`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	
cid	|string	|是|	分类id	|1
page|	int	|是	|分页参数，起始页|	1
size|	int	|是	|分页参数，每页记录数据	|20

__返回字段__：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                            <tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr>
                            <tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td>
</tr>
                            <tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr>
                            <tr>
    <td>curPage</td>
    <td>int</td>
    <td>是</td>
    <td>当前页</td>
    <td></td>
</tr>
                            <tr>
    <td>total</td>
    <td>int</td>
    <td>是</td>
    <td>总条数</td>
    <td></td>
</tr>
                            <tr>
    <td>id</td>
    <td>string</td>
    <td>是</td>
    <td>文章id</td>
    <td></td>
</tr>
                            <tr>
    <td>cid</td>
    <td>string</td>
    <td>是</td>
    <td>分类Id</td>
    <td></td>
</tr>
                            <tr>
    <td>title</td>
    <td>string</td>
    <td>是</td>
    <td>文章标题</td>
    <td></td>
</tr>
                            <tr>
    <td>subTitle</td>
    <td>string</td>
    <td>是</td>
    <td>文章副标题</td>
    <td></td>
</tr>
                            <tr>
    <td>sourceUrl</td>
    <td>string</td>
    <td>是</td>
    <td>文章来源</td>
    <td></td>
</tr>
                            <tr>
    <td>pubTime</td>
    <td>string</td>
    <td>是</td>
    <td>文章的发布时间</td>
    <td></td>
</tr>
                            <tr>
    <td>thumbnails</td>
    <td>string</td>
    <td>是</td>
    <td>导航缩略图，多个图片用$分割</td>
    <td></td>
</tr></tbody></table>

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": {
	        "curPage": 1,
	        "list": [
	            {
	                "cid": "1",
	                "hitCount": "4107",
	                "id": "3be3ce7d9b82f2831045e255b75baf32",
	                "pubTime": "2018-09-09",
	                "sourceUrl": "https://mini.eastday.com/a/180909094630235.html",
	                "subTitle": "一心一娱",
	                "thumbnails": "http://01imgmini.eastday.com/mobile/20180909/20180909_809f6bd1e80825245f0d39b3bcda50c9_cover_mwpl_05500201.jpg",
	                "title": "街拍：漂亮内向精致的小姐姐，凹凸有致,在人群中显眼！"
	            },
	            {
	                "cid": "1",
	                "hitCount": "4548",
	                "id": "8f6c73b8f9fd9500ce8efebff9ed5b6e",
	                "pubTime": "2018-09-09",
	                "sourceUrl": "https://mini.eastday.com/a/180909094539393.html",
	                "subTitle": "玉都天光墟",
	                "thumbnails": "http://07imgmini.eastday.com/mobile/20180909/20180909094539_2fa75fd19e884e7f60c4db88b98489c7_2_mwpl_05500201.jpg",
	                "title": "谁再问你翡翠有什么种，就把这篇文章甩给他！"
	            }
	        ],
	        "total": 195438
	    },
	    "retCode": "200"
	}

<h2 id="6">驾考题库</h2>

<h3 id="6.1">科目一题库列表查询接口</h3>


__接口地址__：`http://apicloud.mob.com/tiku/kemu1/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/tiku/kemu1/query?key=1af5f5c45b9f8&page=1&size=20](http://apicloud.mob.com/tiku/kemu1/query?key=1af5f5c45b9f8&page=1&size=20)

__备注说明__：`提供科目一、科目四、以及专项练习题库`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
page|	int|	否|	查询起始页：默认为1	|
size	|int	|否|	查询页大小：默认为10	|

__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
id	|string|	是	|题库id	|
title	|string|	是|	标题	|
a	|string	|是|	选项A	|
b	|string	|是|	选项B	|
c	|string	|是|	选项C	|
d	|string	|是	|选项D	|
val|string|是|答案选项（如果是选择题，则1-a,2-b,3-c,4-d；如果是判断题，则1=正确，0=错误）	|
file|	string|	是|	图片文件链接url	|
explainText	|string	|是	|答案解释	|
tikuType	|string|	是	|题库类型:判断题-judge ; 选择题-select|

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": {
	        "curPage": 1,
	        "list": [
	            {
	                "a": "注意新手标志",
	                "b": "注意避让标志",
	                "c": "统一式样的实习标志",
	                "d": "注意车距标志",
	                "explainText": "试题解释：《公安部令第123号》第六十四条规定：在实习期内驾驶机动车的，应当在车身后部粘贴或者悬挂统一式样的实习标志。",
	                "file": "",
	                "id": "1536",
	                "tikuType": "select",
	                "title": "在实习期内驾驶机动车的，应当在车身后部粘贴或者悬挂哪种标志？",
	                "val": "3"
	            },
	            {
	                "a": "3年内",
	                "b": "终身",
	                "c": "1年内",
	                "d": "5年内",
	                "explainText": "试题解释：记住最核心的“吊二撤三醉五逃终身”！ 《公安部令第123号》第七十八条规定：申请人以欺骗、贿赂等不正当手段取得机动车驾驶证的，公安机关交通管理部门收缴机动车驾驶证，撤销机动车驾驶许可；申请人在三年内不得再次申领机动车驾驶证。吊销机动车证的为二年，撤销机动车证的为三年，以醉酒吊销五年，因逃跑而吊销是终身，叫“吊二撤三醉五逃终身”。",
	                "file": "",
	                "id": "1537",
	                "tikuType": "select",
	                "title": "以欺骗、贿赂等不正当手段取得驾驶证被依法撤销驾驶许可的，多长时间不得重新申请驾驶许可？",
	                "val": "1"
	            }
	        ],
	        "total": 1311
	    },
	    "retCode": "200"
	}


<h3 id="6.2">科目四题库列表查询接口</h3>


__接口地址__：`http://apicloud.mob.com/tiku/kemu4/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/tiku/kemu4/query?key=1af5f5c45b9f8&page=1&size=20](http://apicloud.mob.com/tiku/kemu4/query?key=1af5f5c45b9f8&page=1&size=20)

__备注说明__：`提供科目一、科目四、以及专项练习题库`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	
page|	int|	否|	查询起始页：默认为1	|
size	|int	|否|	查询页大小：默认为10	|

__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
id	|string|	是	|题库id	|
title	|string|	是|	标题	|
a	|string	|是|	选项A	|
b	|string	|是|	选项B	|
c	|string	|是|	选项C	|
d	|string	|是	|选项D	|
val|string|是|答案选项（如果是选择题，则1-a,2-b,3-c,4-d；如果是判断题，则1=正确，0=错误）	|
file|	string|	是|	图片文件链接url	|
explainText	|string	|是	|答案解释	|
tikuType	|string|	是	|题库类型:判断题-judge ; 选择题-select|

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": {
	        "curPage": 1,
	        "list": [
	            {
	                "a": "观察机动车周围情况",
	                "b": "不用观察周围情况",
	                "c": "开启车门直接上车",
	                "d": "注意观察天气情况",
	                "explainText": "试题解释：注意“进入驾驶室前”，也就是上车前，因此本题选A。",
	                "file": "",
	                "id": "3143",
	                "tikuType": "select",
	                "title": "驾驶人进入驾驶室前，首先要做什么？",
	                "val": "1"
	            },
	            {
	                "a": "什么也不用检查",
	                "b": "轮胎有没有清洗",
	                "c": "备胎在什么位置",
	                "d": "轮胎的紧固和气压",
	                "explainText": "试题解释：对轮胎的检查是为了确保在行车过程中能安全行驶，由此本题应选D。",
	                "file": "",
	                "id": "3144",
	                "tikuType": "select",
	                "title": "出车前对轮胎进行哪些方面的检查？",
	                "val": "4"
	            }
	        ],
	        "total": 836
	    },
	    "retCode": "200"
	}

<h3 id="6.3">专项题库分类查询接口</h3>


__接口地址__：`http://apicloud.mob.com/tiku/shitiku/category/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/tiku/shitiku/category/query?key=1af5f5c45b9f8](http://apicloud.mob.com/tiku/shitiku/category/query?key=1af5f5c45b9f8)

__备注说明__：`提供科目一、科目四、以及专项练习题库`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	

__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
cid|	string	|是	|专项练习分类	|
title|	string	|是	|标题|

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": {
	        "客车科目四考试题库2016": [
	            {
	                "cid": "193",
	                "title": "违法行为综合判断与案例分析"
	            },
	            {
	                "cid": "196",
	                "title": "安全行车常识"
	            }
	        ],
	        "小车科目四考试题库2016": [
	            {
	                "cid": "193",
	                "title": "违法行为综合判断与案例分析"
	            },
	            {
	                "cid": "195",
	                "title": "安全行车常识"
	            }
	        ],
	        "货车科目一考试题库2016": [
	            {
	                "cid": "183",
	                "title": "道路交通安全法律、法规和规章"
	            },
	            {
	                "cid": "184",
	                "title": "道路交通信号"
	            }
	        ],
	        "小车科目一考试题库2016": [
	            {
	                "cid": "183",
	                "title": "道路交通安全法律、法规和规章"
	            },
	            {
	                "cid": "184",
	                "title": "道路交通信号"
	            },
	            {
	                "cid": "185",
	                "title": "安全行车、文明驾驶基础知识"
	            }
	        ],
	        "货车科目四考试题库2016": [
	            {
	                "cid": "193",
	                "title": "违法行为综合判断与案例分析"
	            },
	            {
	                "cid": "196",
	                "title": "安全行车常识"
	            },
	            {
	                "cid": "198",
	                "title": "常见交通标志、标线和交警手势信号辨识"
	            }
	        ],
	        "客车科目一考试题库2016": [
	            {
	                "cid": "183",
	                "title": "道路交通安全法律、法规和规章"
	            },
	            {
	                "cid": "184",
	                "title": "道路交通信号"
	            }
	        ]
	    },
	    "retCode": "200"
	}


<h3 id="6.4">专项练习题库查询接口</h3>


__接口地址__：`http://apicloud.mob.com/wx/article/category/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/tiku/shitiku/query?key=1af5f5c45b9f8&page=1&size=20&cid=207](http://apicloud.mob.com/tiku/shitiku/query?key=1af5f5c45b9f8&page=1&size=20&cid=207)

__备注说明__：`提供科目一、科目四、以及专项练习题库`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	
page|	int|	否|	查询起始页：默认为1	|
size	|int	|否|	查询页大小：默认为10	|
cid	|string	|是	|分类id	|


__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
id	|string|	是	|题库id	|
title|	string|	是	|标题	|
a	|string	|是|	选项A	|
b|	string	|是|	选项B	|
c	|string	|是	|选项C	|
d	|string	|是|	选项D	|
val	|string|	是	|答案选项（如果是选择题，则1-a,2-b,3-c,4-d；如果是判断题，则1=正确，0=错误）	
file|	string	|是	|图片文件链接url	|
explainText|	string	|是	|答案解释	|
tikuType	|string|	是	|题库类型:判断题-judge ; 选择题-select|

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": {
	        "curPage": 1,
	        "list": [
	            {
	                "explainText": "试题解释：正确的，所以要及时去处理扣分。",
	                "id": "5128",
	                "tikuType": "judge",
	                "title": "机动车驾驶人在一个记分周期内累积记分达到12分，拒不参加学习和考试的，将被公安机关...",
	                "val": "1"
	            },
	            {
	                "explainText": "试题解释：《公安部令第123号》第十一条：1、申请小型汽车等准驾车型在18周岁以上、70周岁以下；2、申请低速载货汽车、三轮汽车等准驾车型的，在18周岁以上，60周岁以下。此题正确。本题车管所已经修正。",
	                "id": "5129",
	                "tikuType": "judge",
	                "title": "申请小型汽车汽车驾驶证的，年龄应在18周岁以上70周岁以下。",
	                "val": "1"
	            }
	        ],
	        "total": 165
	    },
	    "retCode": "200"
	}


<h2 id="7">汽车信息查询</h2>

<h3 id="7.1">查询所有汽车品牌</h3>


__接口地址__：`http://apicloud.mob.com/car/brand/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/car/brand/query?key=1af5f5c45b9f8](http://apicloud.mob.com/car/brand/query?key=1af5f5c45b9f8)

__备注说明__：`查询汽车品牌，汽车基本信息`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||

__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
name|	string	|是	|汽车品牌	|
car|	string	|是	|汽车子品牌或合资品牌	|
type|	string	|是	|车系名称|

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": [
	        {
	            "name": "AC Schnitzer",
	            "son": [
	                {
	                    "car": "AC Schnitzer",
	                    "type": "AC Schnitzer X5"
	                }
	            ]
	        },
	        {
	            "name": "阿斯顿·马丁",
	            "son": [
	                {
	                    "car": "阿斯顿·马丁",
	                    "type": "Rapide"
	                },
	                {
	                    "car": "阿斯顿·马丁",
	                    "type": "拉共达Taraf"
	                },
	                {
	                    "car": "阿斯顿·马丁",
	                    "type": "V8 Vantage"
	                },
	                {
	                    "car": "阿斯顿·马丁",
	                    "type": "V12 Vantage"
	                },
	                {
	                    "car": "阿斯顿·马丁",
	                    "type": "阿斯顿·马丁DB9"
	                },
	                {
	                    "car": "阿斯顿·马丁",
	                    "type": "Vanquish"
	                },
	                {
	                    "car": "阿斯顿·马丁",
	                    "type": "阿斯顿·马丁DB11"
	                }
	            ]
	        },
	        {
	            "name": "安凯客车",
	            "son": [
	                {
	                    "car": "安凯客车",
	                    "type": "宝斯通"
	                }
	            ]
	        }
	    ],
	    "retCode": "200"
	}


<h3 id="7.2">车型查询</h3>


__接口地址__：`http://apicloud.mob.com/car/seriesname/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/car/seriesname/query?key=1af5f5c45b9f8&name=Rapide](http://apicloud.mob.com/car/seriesname/query?key=1af5f5c45b9f8&name=Rapide)

__备注说明__：`根据车系名称查询车型`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
name	|string	|是	|车系名称(从所有汽车品牌接口中取)|

__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
brandName	|string|	是	|品牌名称	|
carId	|string	|是	|数据id(查询车型详细信息用到)|
guidePrice|	string|	是	|指导价	|
seriesName|	string|	是	|车型名称|

__JSON返回示例__：

	{
	    "msg": "success",
	    "result": [
	        {
	            "brandName": "Rapide",
	            "carId": "104012",
	            "guidePrice": "298.80万",
	            "seriesName": "Rapide 2016款 Rapide CE"
	        },
	        {
	            "brandName": "Rapide",
	            "carId": "104013",
	            "guidePrice": "318.80万",
	            "seriesName": "Rapide 2016款 Rapide Great Britain Edition"
	        },
	        {
	            "brandName": "Rapide",
	            "carId": "104014",
	            "guidePrice": "364.50万",
	            "seriesName": "Rapide 2016款 6.0L S"
	        }
	    ],
	    "retCode": "200"
	}

<h3 id="7.3">查询车型详细信息</h3>


__接口地址__：`http://apicloud.mob.com/car/series/query`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/car/series/query?key=1af5f5c45b9f8&cid=104013](http://apicloud.mob.com/car/series/query?key=1af5f5c45b9f8&cid=104013)

__备注说明__：`查询车型详细信息`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||
cid	|string	|是	|车型接口id|

__返回字段__：

|name	|type|	N|	D|	value|
|------|------|------|------|------|
retCode|	string	|是|	返回码	||
msg	|string|	是|	返回说明	||
result|	string|	是|	返回结果集	||
brand	|string	|是|	品牌名称|	
brandName|	string	|是	|车系名称	|
carImage	|string	|是|	图片地址	|
seriesName|	string|	是	|车型名称	|
sonBrand	|string	|是	|子品牌或合资品牌|	
baseInfo|	string	|是|	车型基本配置信息	|
airConfig	|string	|是	|空调/冰箱配置信息	|
carbody	|string	|是	|车身配置信息	|
chassis	|string	|是	|底盘配置信息	|
controlConfig|	string|	是|	操控配置信息|
engine	|string	|是	|发动机配置信息	|
exterConfig|	string	|是|	外部配置信息	|
glassConfig|	string	|是|	玻璃/后视镜配置信息|
interConfig|	string	|是|	内部配置信息	|
lightConfig|	string	|是	|灯光配置信息	|
mediaConfig|	string	|是	|多媒体配置信息	|
safetyDevice|	string|	是|	安全装置信息|	
seatConfig	|string|	是|	座椅配置信息|	
techConfig	|string|	是	|高科技配置信息	|
transmission	|string	|是|	变速箱信息	|
wheelInfo	|string|	是	|车轮制动信息	|
motorList	|string|	是	|电动机配置信息|

__JSON返回示例__:

	{
	    "msg": "success",
	    "result": [
	        {
	            "airConfig": [
	                {
	                    "name": "空调控制方式",
	                    "value": "自动 1"
	                },
	                {
	                    "name": "后排独立空调",
	                    "value": "-"
	                },
	                {
	                    "name": "后座出风口",
	                    "value": "1"
	                },
	                {
	                    "name": "温度分区控制",
	                    "value": "1"
	                },
	                {
	                    "name": "车内空气调节/花粉过滤",
	                    "value": "1"
	                },
	                {
	                    "name": "车载冰箱",
	                    "value": "-"
	                }
	            ],
	            "baseInfo": [
	                {
	                    "name": "车型名称",
	                    "value": "Rapide 2016款 Rapide Great Britain Edition"
	                },
	                {
	                    "name": "厂商指导价(元)",
	                    "value": "318.80万"
	                },
	                {
	                    "name": "厂商",
	                    "value": "阿斯顿·马丁"
	                },
	                {
	                    "name": "级别",
	                    "value": "大型车"
	                },
	                {
	                    "name": "发动机",
	                    "value": "6.0L 558马力 V12"
	                },
	                {
	                    "name": "变速箱",
	                    "value": "8挡手自一体"
	                },
	                {
	                    "name": "长*宽*高(mm)",
	                    "value": "5019*2140*1360"
	                },
	                {
	                    "name": "车身结构",
	                    "value": "5门4座掀背车"
	                },
	                {
	                    "name": "最高车速(km/h)",
	                    "value": "306"
	                },
	                {
	                    "name": "官方0-100km/h加速(s)",
	                    "value": "4.6"
	                },
	                {
	                    "name": "实测0-100km/h加速(s)",
	                    "value": "-"
	                },
	                {
	                    "name": "实测100-0km/h制动(m)",
	                    "value": "-"
	                },
	                {
	                    "name": "实测油耗(L/100km)",
	                    "value": "-"
	                },
	                {
	                    "name": "工信部综合油耗(L/100km)",
	                    "value": "-"
	                },
	                {
	                    "name": "实测离地间隙(mm)",
	                    "value": "-"
	                },
	                {
	                    "name": "整车质保",
	                    "value": "三年不限公里"
	                }
	            ],
	            "brand": "阿斯顿·马丁",
	            "brandName": "Rapide",
	            "carImage": "http://f2.mob.com/imgs/2016/06/30/3AA/K52JN3AM6KXU6IRI5KUA_240x180.jpg",
	            "carbody": [
	                {
	                    "name": "长度(mm)",
	                    "value": "5019"
	                },
	                {
	                    "name": "宽度(mm)",
	                    "value": "2140"
	                },
	                {
	                    "name": "高度(mm)",
	                    "value": "1360"
	                },
	                {
	                    "name": "轴距(mm)",
	                    "value": "2989"
	                },
	                {
	                    "name": "前轮距(mm)",
	                    "value": "-"
	                },
	                {
	                    "name": "后轮距(mm)",
	                    "value": "-"
	                },
	                {
	                    "name": "最小离地间隙(mm)",
	                    "value": "-"
	                },
	                {
	                    "name": "整备质量(kg)",
	                    "value": "-"
	                },
	                {
	                    "name": "车身结构",
	                    "value": "掀背车"
	                },
	                {
	                    "name": "车门数(个)",
	                    "value": "5"
	                },
	                {
	                    "name": "座位数(个)",
	                    "value": "4"
	                },
	                {
	                    "name": "油箱容积(L)",
	                    "value": "91"
	                },
	                {
	                    "name": "行李厢容积(L)",
	                    "value": "-"
	                }
	            ],
	            "chassis": [
	                {
	                    "name": "驱动方式",
	                    "value": "前置后驱"
	                },
	                {
	                    "name": "前悬架类型",
	                    "value": "螺旋弹簧双叉臂独立悬架"
	                },
	                {
	                    "name": "后悬架类型",
	                    "value": "螺旋弹簧双叉臂独立悬架"
	                },
	                {
	                    "name": "助力类型",
	                    "value": "电动助力"
	                },
	                {
	                    "name": "车体结构",
	                    "value": "承载式"
	                }
	            ],
	            "controlConfig": [
	                {
	                    "name": "ABS防抱死",
	                    "value": "1"
	                },
	                {
	                    "name": "制动力分配(EBD/CBC等)",
	                    "value": "1"
	                },
	                {
	                    "name": "刹车辅助(EBA/BAS/BA等)",
	                    "value": "1"
	                },
	                {
	                    "name": "牵引力控制(ASR/TCS/TRC等)",
	                    "value": "1"
	                },
	                {
	                    "name": "车身稳定控制(ESC/ESP/DSC等)",
	                    "value": "1"
	                },
	                {
	                    "name": "上坡辅助",
	                    "value": "-"
	                },
	                {
	                    "name": "自动驻车",
	                    "value": "-"
	                },
	                {
	                    "name": "陡坡缓降",
	                    "value": "-"
	                },
	                {
	                    "name": "可变悬架",
	                    "value": "-"
	                },
	                {
	                    "name": "空气悬架",
	                    "value": "-"
	                },
	                {
	                    "name": "可变转向比",
	                    "value": "-"
	                },
	                {
	                    "name": "前桥限滑差速器/差速锁",
	                    "value": "-"
	                },
	                {
	                    "name": "中央差速器锁止功能",
	                    "value": "-"
	                },
	                {
	                    "name": "后桥限滑差速器/差速锁",
	                    "value": "-"
	                }
	            ],
	            "engine": [
	                {
	                    "name": "发动机型号",
	                    "value": "-"
	                },
	                {
	                    "name": "排量(mL)",
	                    "value": "5935"
	                },
	                {
	                    "name": "排量(L)",
	                    "value": "6.0"
	                },
	                {
	                    "name": "进气形式",
	                    "value": "自然吸气"
	                },
	                {
	                    "name": "气缸排列形式",
	                    "value": "V"
	                },
	                {
	                    "name": "气缸数(个)",
	                    "value": "12"
	                },
	                {
	                    "name": "每缸气门数(个)",
	                    "value": "4"
	                },
	                {
	                    "name": "压缩比",
	                    "value": "-"
	                },
	                {
	                    "name": "配气机构",
	                    "value": "DOHC"
	                },
	                {
	                    "name": "缸径(mm)",
	                    "value": "-"
	                },
	                {
	                    "name": "行程(mm)",
	                    "value": "-"
	                },
	                {
	                    "name": "最大马力(Ps)",
	                    "value": "558"
	                },
	                {
	                    "name": "最大功率(kW)",
	                    "value": "410"
	                },
	                {
	                    "name": "最大功率转速(rpm)",
	                    "value": "6750"
	                },
	                {
	                    "name": "最大扭矩(N·m)",
	                    "value": "620"
	                },
	                {
	                    "name": "最大扭矩转速(rpm)",
	                    "value": "5500"
	                },
	                {
	                    "name": "发动机特有技术",
	                    "value": "-"
	                },
	                {
	                    "name": "燃料形式",
	                    "value": "汽油"
	                },
	                {
	                    "name": "燃油标号",
	                    "value": "97号(京95号)"
	                },
	                {
	                    "name": "供油方式",
	                    "value": "多点电喷"
	                },
	                {
	                    "name": "缸盖材料",
	                    "value": "铝"
	                },
	                {
	                    "name": "缸体材料",
	                    "value": "铝"
	                },
	                {
	                    "name": "环保标准",
	                    "value": "欧IV"
	                }
	            ],
	            "exterConfig": [
	                {
	                    "name": "电动天窗",
	                    "value": "-"
	                },
	                {
	                    "name": "全景天窗",
	                    "value": "-"
	                },
	                {
	                    "name": "运动外观套件",
	                    "value": "-"
	                },
	                {
	                    "name": "铝合金轮圈",
	                    "value": "1"
	                },
	                {
	                    "name": "电动吸合门",
	                    "value": "-"
	                },
	                {
	                    "name": "侧滑门",
	                    "value": "-"
	                },
	                {
	                    "name": "电动后备厢",
	                    "value": "-"
	                },
	                {
	                    "name": "感应后备厢",
	                    "value": "-"
	                },
	                {
	                    "name": "车顶行李架",
	                    "value": "-"
	                }
	            ],
	            "glassConfig": [
	                {
	                    "name": "前/后电动车窗",
	                    "value": "前 1/后 1"
	                },
	                {
	                    "name": "车窗防夹手功能",
	                    "value": "1"
	                },
	                {
	                    "name": "防紫外线/隔热玻璃",
	                    "value": "1"
	                },
	                {
	                    "name": "后视镜电动调节",
	                    "value": "1"
	                },
	                {
	                    "name": "后视镜加热",
	                    "value": "-"
	                },
	                {
	                    "name": "内/外后视镜自动防眩目",
	                    "value": "内 1/外-"
	                },
	                {
	                    "name": "后视镜电动折叠",
	                    "value": "1"
	                },
	                {
	                    "name": "后视镜记忆",
	                    "value": "1"
	                },
	                {
	                    "name": "后风挡遮阳帘",
	                    "value": "-"
	                },
	                {
	                    "name": "后排侧遮阳帘",
	                    "value": "-"
	                },
	                {
	                    "name": "后排侧隐私玻璃",
	                    "value": "-"
	                },
	                {
	                    "name": "遮阳板化妆镜",
	                    "value": "1"
	                },
	                {
	                    "name": "后雨刷",
	                    "value": "-"
	                },
	                {
	                    "name": "感应雨刷",
	                    "value": "1"
	                }
	            ],
	            "interConfig": [
	                {
	                    "name": "真皮方向盘",
	                    "value": "1"
	                },
	                {
	                    "name": "方向盘调节",
	                    "value": "上下+前后调节"
	                },
	                {
	                    "name": "方向盘电动调节",
	                    "value": "-"
	                },
	                {
	                    "name": "多功能方向盘",
	                    "value": "1"
	                },
	                {
	                    "name": "方向盘换挡",
	                    "value": "1"
	                },
	                {
	                    "name": "方向盘加热",
	                    "value": "-"
	                },
	                {
	                    "name": "方向盘记忆",
	                    "value": "-"
	                },
	                {
	                    "name": "定速巡航",
	                    "value": "1"
	                },
	                {
	                    "name": "前/后驻车雷达",
	                    "value": "前 1/后 1"
	                },
	                {
	                    "name": "倒车视频影像",
	                    "value": "-"
	                },
	                {
	                    "name": "行车电脑显示屏",
	                    "value": "1"
	                },
	                {
	                    "name": "全液晶仪表盘",
	                    "value": "-"
	                },
	                {
	                    "name": "HUD抬头数字显示",
	                    "value": "-"
	                }
	            ],
	            "lightConfig": [
	                {
	                    "name": "近光灯",
	                    "value": "氙气"
	                },
	                {
	                    "name": "远光灯",
	                    "value": "氙气"
	                },
	                {
	                    "name": "日间行车灯",
	                    "value": "1"
	                },
	                {
	                    "name": "自适应远近光",
	                    "value": "-"
	                },
	                {
	                    "name": "自动头灯",
	                    "value": "1"
	                },
	                {
	                    "name": "转向辅助灯",
	                    "value": "-"
	                },
	                {
	                    "name": "转向头灯",
	                    "value": "1"
	                },
	                {
	                    "name": "前雾灯",
	                    "value": "-"
	                },
	                {
	                    "name": "大灯高度可调",
	                    "value": "1"
	                },
	                {
	                    "name": "大灯清洗装置",
	                    "value": "1"
	                },
	                {
	                    "name": "车内氛围灯",
	                    "value": "-"
	                }
	            ],
	            "mediaConfig": [
	                {
	                    "name": "GPS导航系统",
	                    "value": "1"
	                },
	                {
	                    "name": "定位互动服务",
	                    "value": "-"
	                },
	                {
	                    "name": "中控台彩色大屏",
	                    "value": "1"
	                },
	                {
	                    "name": "蓝牙/车载电话",
	                    "value": "1"
	                },
	                {
	                    "name": "车载电视",
	                    "value": "-"
	                },
	                {
	                    "name": "后排液晶屏",
	                    "value": "-"
	                },
	                {
	                    "name": "220V/230V电源",
	                    "value": "-"
	                },
	                {
	                    "name": "外接音源接口",
	                    "value": "USB+AUX"
	                },
	                {
	                    "name": "CD支持MP3/WMA",
	                    "value": "1"
	                },
	                {
	                    "name": "多媒体系统",
	                    "value": "多碟CD"
	                },
	                {
	                    "name": "扬声器品牌",
	                    "value": "Bang & Olufsen"
	                },
	                {
	                    "name": "扬声器数量",
	                    "value": "-"
	                }
	            ],
	            "safetyDevice": [
	                {
	                    "name": "主/副驾驶座安全气囊",
	                    "value": "主 1/副 1"
	                },
	                {
	                    "name": "前/后排侧气囊",
	                    "value": "前 1/后-"
	                },
	                {
	                    "name": "前/后排头部气囊(气帘)",
	                    "value": "前 1/后 1"
	                },
	                {
	                    "name": "膝部气囊",
	                    "value": "-"
	                },
	                {
	                    "name": "胎压监测装置",
	                    "value": "1"
	                },
	                {
	                    "name": "零胎压继续行驶",
	                    "value": "1"
	                },
	                {
	                    "name": "安全带未系提示",
	                    "value": "1"
	                },
	                {
	                    "name": "ISOFIX儿童座椅接口",
	                    "value": "1"
	                },
	                {
	                    "name": "发动机电子防盗",
	                    "value": "1"
	                },
	                {
	                    "name": "车内中控锁",
	                    "value": "1"
	                },
	                {
	                    "name": "遥控钥匙",
	                    "value": "1"
	                },
	                {
	                    "name": "无钥匙启动系统",
	                    "value": "1"
	                },
	                {
	                    "name": "无钥匙进入系统",
	                    "value": "1"
	                }
	            ],
	            "seatConfig": [
	                {
	                    "name": "座椅材质",
	                    "value": "真皮"
	                },
	                {
	                    "name": "运动风格座椅",
	                    "value": "1"
	                },
	                {
	                    "name": "座椅高低调节",
	                    "value": "1"
	                },
	                {
	                    "name": "腰部支撑调节",
	                    "value": "1"
	                },
	                {
	                    "name": "肩部支撑调节",
	                    "value": "-"
	                },
	                {
	                    "name": "主/副驾驶座电动调节",
	                    "value": "主 1/副 1"
	                },
	                {
	                    "name": "第二排靠背角度调节",
	                    "value": "-"
	                },
	                {
	                    "name": "第二排座椅移动",
	                    "value": "-"
	                },
	                {
	                    "name": "后排座椅电动调节",
	                    "value": "-"
	                },
	                {
	                    "name": "电动座椅记忆",
	                    "value": "1"
	                },
	                {
	                    "name": "前/后排座椅加热",
	                    "value": "前 1/后 1"
	                },
	                {
	                    "name": "前/后排座椅通风",
	                    "value": "-"
	                },
	                {
	                    "name": "前/后排座椅按摩",
	                    "value": "-"
	                },
	                {
	                    "name": "第三排座椅",
	                    "value": "-"
	                },
	                {
	                    "name": "后排座椅放倒方式",
	                    "value": "比例放倒"
	                },
	                {
	                    "name": "前/后中央扶手",
	                    "value": "前 1/后 1"
	                },
	                {
	                    "name": "后排杯架",
	                    "value": "1"
	                }
	            ],
	            "seriesName": "Rapide 2016款 Rapide Great Britain Edition",
	            "sonBrand": "阿斯顿·马丁",
	            "techConfig": [
	                {
	                    "name": "自动泊车入位",
	                    "value": "-"
	                },
	                {
	                    "name": "发动机启停技术",
	                    "value": "-"
	                },
	                {
	                    "name": "并线辅助",
	                    "value": "-"
	                },
	                {
	                    "name": "车道偏离预警系统",
	                    "value": "-"
	                },
	                {
	                    "name": "主动刹车/主动安全系统",
	                    "value": "-"
	                },
	                {
	                    "name": "整体主动转向系统",
	                    "value": "-"
	                },
	                {
	                    "name": "夜视系统",
	                    "value": "-"
	                },
	                {
	                    "name": "中控液晶屏分屏显示",
	                    "value": "-"
	                },
	                {
	                    "name": "自适应巡航",
	                    "value": "-"
	                },
	                {
	                    "name": "全景摄像头",
	                    "value": "-"
	                }
	            ],
	            "transmission": [
	                {
	                    "name": "简称",
	                    "value": "8挡手自一体"
	                },
	                {
	                    "name": "挡位个数",
	                    "value": "8"
	                },
	                {
	                    "name": "变速箱类型",
	                    "value": "手自一体变速箱(AT)"
	                }
	            ],
	            "wheelInfo": [
	                {
	                    "name": "前制动器类型",
	                    "value": "通风盘式"
	                },
	                {
	                    "name": "后制动器类型",
	                    "value": "通风盘式"
	                },
	                {
	                    "name": "驻车制动类型",
	                    "value": "电子驻车"
	                },
	                {
	                    "name": "前轮胎规格",
	                    "value": "245/40 R20"
	                },
	                {
	                    "name": "后轮胎规格",
	                    "value": "295/35 R20"
	                },
	                {
	                    "name": "备胎规格",
	                    "value": "无"
	                }
	            ]
	        }
	    ],
	    "retCode": "200"
	}

<h2 id="8">休闲</h2>

<h3 id="8.1">周公解梦</h3>


__接口地址__：`http://apicloud.mob.com/appstore/dream/search`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/appstore/dream/search?key=1af5f5c45b9f8&name=蛇](http://apicloud.mob.com/appstore/dream/search?key=1af5f5c45b9f8&name=蛇)

__备注说明__：`根据关键字查询梦境的含义`

__请求参数__：

|name	|type|	N	|D	|value|
|------|------|------|------|------|
key|	string|	是	|用户申请的appkey||	
name|	string|	是	|梦源关键字	||	
page|	int|	否	|页码（默认1）	||	
size|	int|	否	|每页显示条数（默认20条）	||	

__返回字段__：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                            <tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr>
                            <tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td>
</tr>
                            <tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr>
                            <tr>
    <td>page</td>
    <td>int</td>
    <td>是</td>
    <td>日期</td>
    <td></td>
</tr>
                            <tr>
    <td>total</td>
    <td>int</td>
    <td>是</td>
    <td>月份</td>
    <td></td>
</tr>
                            <tr>
    <td>name</td>
    <td>string</td>
    <td>是</td>
    <td>梦源</td>
    <td></td>
</tr>
                            <tr>
    <td>detail</td>
    <td>string</td>
    <td>是</td>
    <td>解说</td>
    <td></td>
</tr>
                    </tbody></table>

__JSON返回示例__:


```
{
	    "msg": "success",
	    "result": {
	        "list": [
	            {
	                "detail": "梦见蛇，是凶兆。女人梦见蛇，自己和孩子都会病倒。梦见一对蛇，很快会分家。商人梦见一对蛇，能发大财。梦见蛇咬你自己，要交好运，生活会丰裕。但是梦见蛇咬自己妻子，是不祥之兆，会遇到忧愁不幸。梦见敌人被蛇咬伤，敌人会互相残杀,最后两败俱伤。梦见打死蛇，能征服敌人。梦见蛇钻进洞里，家里会被偷窃或被劫。梦见蛇捕捉老鼠或青蛙，会有不幸的消息。梦见蛇与猫争斗，所有的灾难都会过去。",
	                "name": "蛇"
	            }
	        ],
	        "page": 1,
	        "total": 1
	    },
	    "retCode": "200"
	}

```


<h3 id="8.2">婚姻匹配查询</h3>


__接口地址__：`http://apicloud.mob.com/appstore/marriage/day`

__支持格式__：`JSON`

__请求方式__：`GET`

__请求示例__：[http://apicloud.mob.com/appstore/marriage/day?key=1af5f5c45b9f8&menDate=1987-4-26&menHour=10&womanDate=1992-03-18&womanHour=11](http://apicloud.mob.com/appstore/marriage/day?key=1af5f5c45b9f8&menDate=1987-4-26&menHour=10&womanDate=1992-03-18&womanHour=11)

__备注说明__:`分别根据男女出生日期和时间查询婚姻结果`

__请求参数__:

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                            <tr>
    <td>key</td>
    <td>string</td>
    <td>是</td>
    <td>用户申请的appkey</td>
    <td></td>
</tr>
                            <tr>
    <td>menDate</td>
    <td>string</td>
    <td>是</td>
    <td>男：出生日期</td>
    <td>1987-04-26</td>
</tr>
                            <tr>
    <td>menHour</td>
    <td>string</td>
    <td>是</td>
    <td>男：出生小时</td>
    <td>10</td>
</tr>
                            <tr>
    <td>womanDate</td>
    <td>string</td>
    <td>是</td>
    <td>女：出生日期</td>
    <td>1992-03-18</td>
</tr>
                            <tr>
    <td>womanHour</td>
    <td>string</td>
    <td>是</td>
    <td>女：出生小时</td>
    <td>11</td>
</tr>
                    </tbody></table>	

__返回字段__:

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                            <tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr>
                            <tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td>
</tr>
                            <tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr>
                            <tr>
    <td>marriageType</td>
    <td>string</td>
    <td>是</td>
    <td>婚姻匹配结果(可能匹配不了结果)</td>
    <td></td>
</tr>
                            <tr>
    <td>menLunar</td>
    <td>string</td>
    <td>是</td>
    <td>男：阴历出生日期</td>
    <td></td>
</tr>
                            <tr>
    <td>menLunarTime</td>
    <td>string</td>
    <td>是</td>
    <td>男：农历出生日期</td>
    <td></td>
</tr>
                            <tr>
    <td>menMarriage</td>
    <td>string</td>
    <td>是</td>
    <td>男：犯什么婚姻类型 (可能会计算不到结果)</td>
    <td></td>
</tr>
                            <tr>
    <td>menZodiac</td>
    <td>string</td>
    <td>是</td>
    <td>男：属相</td>
    <td></td>
</tr>
                            <tr>
    <td>womanLunar</td>
    <td>string</td>
    <td>是</td>
    <td>女：阴历出生日期</td>
    <td></td>
</tr>
                            <tr>
    <td>wonmanLuarTime</td>
    <td>string</td>
    <td>是</td>
    <td>女：农历出生日期</td>
    <td></td>
</tr>
                            <tr>
    <td>wonmanMarriage</td>
    <td>string</td>
    <td>是</td>
    <td>女：犯什么婚姻类型(可能会计算不到结果)</td>
    <td></td>
</tr>
                            <tr>
    <td>wonmanZodiac</td>
    <td>string</td>
    <td>是</td>
    <td>女：属相</td>
    <td></td>
</tr>
                    </tbody></table>

__JSON返回示例__:

	{
	    "msg": "success",
	    "result": {
	        "marriageType": "六煞婚",
	        "menLunar": "一九八七年三月廿八",
	        "menLunarTime": "丁卯年甲辰月甲辰日己巳时",
	        "menMarriage": "女破男家",
	        "menZodiac": "兔",
	        "womanLunar": "一九九二年二月十五",
	        "wonmanLuarTime": "壬申年癸卯月癸巳日丁巳时",
	        "wonmanMarriage": "大狼籍,绝房,男扫女家",
	        "wonmanZodiac": "猴"
	    },
	    "retCode": "200"
	}


<h3 id="8.3">手机号码查吉凶</h3>


__接口地址__:`http://apicloud.mob.com/appstore/lucky/mobile/query`

__支持格式__:`JSON`

__请求方式__:`GET`

__请求示例__:[http://apicloud.mob.com/appstore/lucky/mobile/query?key=1af5f5c45b9f8&mobile=13816863588](http://apicloud.mob.com/appstore/lucky/mobile/query?key=1af5f5c45b9f8&mobile=13816863588)

__备注说明__:`分别根据男女出生日期和时间查询婚姻结果`

__请求参数__:

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
    <th>name</th>
    <th>type</th>
    <th>N</th>
    <th>D</th>
    <th>value</th>
</tr><tr>
    <td>key</td>
    <td>string</td>
    <td>是</td>
    <td>用户申请的appkey</td>
    <td></td>
</tr><tr>
    <td>mobile</td>
    <td>string</td>
    <td>是</td>
    <td>手机号</td>
    <td></td>
</tr></tbody></table>


__返回字段__:


<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
	<th>name</th>
	<th>type</th>
	<th>N</th>
	<th>D</th>
	<th>value</th>
</tr><tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr><tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td> <tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr> <tr>
    <td>conclusion</td>
    <td>string</td>
    <td>是</td>
    <td>吉凶描述</td>
    <td></td>
</tr></tbody></table>


__JSON返回示例__:


	{
	    "msg": "success",
	    "result": {
	        "conclusion": "时来运转，事事如意，功成名就，富贵自来 吉"
	    },
	    "retCode": "200"
	}


<h3 id="8.4">八字算命</h3>


__接口地址__ ：`http://apicloud.mob.com/appstore/horoscope/day`

__支持格式__ ：`JSON`

__请求方式__ ：`GET`

__请求示例__ ：[http://apicloud.mob.com/appstore/horoscope/day?key=1af5f5c45b9f8&date=2016-01-19&hour=20](http://apicloud.mob.com/appstore/horoscope/day?key=1af5f5c45b9f8&date=2016-01-19&hour=20)

__备注说明__ :`根据日期和小时数据进行简单八字算命`

__请求参数__:

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
    <th>name</th>
    <th>type</th>
    <th>N</th>
    <th>D</th>
    <th>value</th>
</tr><tr>
    <td>key</td>
    <td>string</td>
    <td>是</td>
    <td>用户申请的appkey</td>
    <td></td>
</tr><tr>
    <td>mobile</td>
    <td>string</td>
    <td>是</td>
    <td>手机号</td>
    <td></td>
</tr></tbody></table>

__返回字段__:

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
	<th>name</th>
	<th>type</th>
	<th>N</th>
	<th>D</th>
	<th>value</th>
</tr><tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr><tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td> <tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr> <tr>
    <td>conclusion</td>
    <td>string</td>
    <td>是</td>
    <td>吉凶描述</td>
    <td></td>
</tr></tbody></table>

__JSON返回示例__:

```
{
    "msg": "success",
    "result": {
        "horoscope": "金玉出海日，临死，坐支，伤官。能歌善舞笔和墨，犹如白虎戏江水。冲在禄马登科甲，斑竹细雨伤情泪。子月，衰，伤官，无土运，鬼旺，风烛夭贱。丑月，虚名，轻财。寅月，偏财，不禄。卯月，合财，金玉满目。辰月，利路经商。巳月，武职显跃。午月，文官近卫。四季月，印旺富而有名，亥月，漂蓬，僧侣。",
        "lunar": "二零一五年腊月初十",
        "lunarDate": "乙未年己丑月庚子日丙戌时",
        "zodiac": "羊"
    },
    "retCode": "200"
}
```


<h3 id="8.5">老黄历</h3>


__接口地址__ ：`http://apicloud.mob.com/appstore/laohuangli/day`

__支持格式__ ：`JSON`

__请求方式__ ：`GET`

__请求示例__ ：[http://apicloud.mob.com/appstore/laohuangli/day?key=1af5f5c45b9f8&date=2016-01-19](http://apicloud.mob.com/appstore/laohuangli/day?key=1af5f5c45b9f8&date=2016-01-19)

__备注说明__ ：`根据日期查询查询当前日期的老黄历信息`

__请求参数__ ：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
    <th>name</th>
    <th>type</th>
    <th>N</th>
    <th>D</th>
    <th>value</th>
</tr>
                                <tr>
        <td>key</td>
        <td>string</td>
        <td>是</td>
        <td>用户申请的appkey</td>
        <td></td>
    </tr>
                                <tr>
        <td>date</td>
        <td>string</td>
        <td>是</td>
        <td>查询日期</td>
        <td>2016-01-19</td>
    </tr>
                        </tbody></table>

__返回字段__ ：

<table cellspacing="0" cellpadding="0" border="0">
<tbody><tr>
<th>name</th>
<th>type</th>
<th>N</th>
<th>D</th>
<th>value</th>
</tr>
                            <tr>
    <td>retCode</td>
    <td>string</td>
    <td>是</td>
    <td>返回码</td>
    <td></td>
</tr>
                            <tr>
    <td>msg</td>
    <td>string</td>
    <td>是</td>
    <td>返回说明</td>
    <td></td>
</tr>
                            <tr>
    <td>result</td>
    <td>string</td>
    <td>是</td>
    <td>返回结果集</td>
    <td></td>
</tr>
                            <tr>
    <td>avoid</td>
    <td>string</td>
    <td>是</td>
    <td>不宜/忌</td>
    <td></td>
</tr>
                            <tr>
    <td>date</td>
    <td>string</td>
    <td>是</td>
    <td>查询日期</td>
    <td></td>
</tr>
                            <tr>
    <td>jishen</td>
    <td>string</td>
    <td>是</td>
    <td>吉煞</td>
    <td></td>
</tr>
                            <tr>
    <td>lunar</td>
    <td>string</td>
    <td>是</td>
    <td>农历日期</td>
    <td></td>
</tr>
                            <tr>
    <td>suit</td>
    <td>string</td>
    <td>是</td>
    <td>宜</td>
    <td></td>
</tr>
                            <tr>
    <td>xiongshen</td>
    <td>string</td>
    <td>是</td>
    <td>凶煞</td>
    <td></td>
</tr>
                    </tbody></table>

__JSON返回示例__ ：

```
{
    "msg": "success",
    "result": {
        "avoid": "治目 修造 筑堤 ",
        "date": "2016-01-19",
        "jishen": "天德 月德 月德合 天成 天官 天马 天财 月空 天贵 天赦 母仓 福厚 大红砂 相日 煞贡 直星 人专 ",
        "lunar": "乙未年十二月初十日",
        "suit": "安床 ",
        "xiongshen": "天吏 天狱 天地转煞 正四废 傍四废 白虎 玄武 勾陈 披麻 重丧 荒鞠 鲁班杀 斧头杀 万砍杀 五虚 重复 土禁 四时大墓 "
    },
    "retCode": "200"
}
```
























