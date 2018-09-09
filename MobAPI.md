# Mob API接口

- [1 天气预报](#1)
	- [1.1 城市列表查询接口](#1.1)
	- [1.2 根据城市名查询天气](#1.2)
	- [1.3 根据IP查询天气](#1.3)
	- [1.4 空气质量查询](#1.4)
- [2](#2)
	- [2.1](#2.1)
- [3](#3)
	- [3.1](#3.1)
	- [3.2](#3.2)
	- [3.3](#3.3)
- [4 菜谱查询](#4)
	- [4.1 菜谱分类标签查询](#4.1)
	- [4.2 按标签查询菜谱接口](#4.2)
	- [4.3 菜谱查询接口](#4.3)
- [5 微信精选](#5)
	- [5.1 微信精选分类查询](#5.1)
	- [5.2 微信精选列表查询](#5.2)

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
	                    },
	                    {
	                        "aqi": 106,
	                        "date": "2018-09-11",
	                        "quality": "轻度污染"
	                    },
	                    {
	                        "aqi": 129,
	                        "date": "2018-09-12",
	                        "quality": "轻度污染"
	                    },
	                    {
	                        "aqi": 101,
	                        "date": "2018-09-13",
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
	                    },
	                    {
	                        "aqi": 25,
	                        "dateTime": "2018-09-07 15:00:00"
	                    },
	                    {
	                        "aqi": 24,
	                        "dateTime": "2018-09-07 14:00:00"
	                    },
	                    {
	                        "aqi": 24,
	                        "dateTime": "2018-09-07 13:00:00"
	                    },
	                    {
	                        "aqi": 22,
	                        "dateTime": "2018-09-07 12:00:00"
	                    },
	                    {
	                        "aqi": 20,
	                        "dateTime": "2018-09-07 11:00:00"
	                    },
	                    {
	                        "aqi": 20,
	                        "dateTime": "2018-09-07 10:00:00"
	                    },
	                    {
	                        "aqi": 17,
	                        "dateTime": "2018-09-07 09:00:00"
	                    },
	                    {
	                        "aqi": 25,
	                        "dateTime": "2018-09-07 08:00:00"
	                    },
	                    {
	                        "aqi": 44,
	                        "dateTime": "2018-09-07 07:00:00"
	                    },
	                    {
	                        "aqi": 53,
	                        "dateTime": "2018-09-07 06:00:00"
	                    },
	                    {
	                        "aqi": 23,
	                        "dateTime": "2018-09-07 05:00:00"
	                    },
	                    {
	                        "aqi": 24,
	                        "dateTime": "2018-09-07 04:00:00"
	                    },
	                    {
	                        "aqi": 22,
	                        "dateTime": "2018-09-07 03:00:00"
	                    },
	                    {
	                        "aqi": 24,
	                        "dateTime": "2018-09-07 02:00:00"
	                    },
	                    {
	                        "aqi": 20,
	                        "dateTime": "2018-09-07 01:00:00"
	                    },
	                    {
	                        "aqi": 29,
	                        "dateTime": "2018-09-07 00:00:00"
	                    },
	                    {
	                        "aqi": 25,
	                        "dateTime": "2018-09-06 23:00:00"
	                    },
	                    {
	                        "aqi": 26,
	                        "dateTime": "2018-09-06 22:00:00"
	                    },
	                    {
	                        "aqi": 30,
	                        "dateTime": "2018-09-06 21:00:00"
	                    },
	                    {
	                        "aqi": 39,
	                        "dateTime": "2018-09-06 20:00:00"
	                    },
	                    {
	                        "aqi": 31,
	                        "dateTime": "2018-09-06 19:00:00"
	                    },
	                    {
	                        "aqi": 38,
	                        "dateTime": "2018-09-06 18:00:00"
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
	                },
	                {
	                    "date": "2018-09-09",
	                    "dayTime": "多云",
	                    "night": "多云",
	                    "temperature": "27°C / 15°C",
	                    "week": "星期日",
	                    "wind": "西南风 小于3级"
	                },
	                {
	                    "date": "2018-09-10",
	                    "dayTime": "晴",
	                    "night": "多云",
	                    "temperature": "28°C / 17°C",
	                    "week": "星期一",
	                    "wind": "南风 小于3级"
	                },
	                {
	                    "date": "2018-09-11",
	                    "dayTime": "多云",
	                    "night": "多云",
	                    "temperature": "27°C / 17°C",
	                    "week": "星期二",
	                    "wind": "南风 3～4级"
	                },
	                {
	                    "date": "2018-09-12",
	                    "dayTime": "多云",
	                    "night": "晴",
	                    "temperature": "27°C / 16°C",
	                    "week": "星期三",
	                    "wind": "南风 小于3级"
	                },
	                {
	                    "date": "2018-09-13",
	                    "dayTime": "多云",
	                    "night": "多云",
	                    "temperature": "28°C / 17°C",
	                    "week": "星期四",
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
	                    },
	                    {
	                        "aqi": 65,
	                        "date": "2018-09-10",
	                        "quality": "良"
	                    },
	                    {
	                        "aqi": 80,
	                        "date": "2018-09-11",
	                        "quality": "良"
	                    },
	                    {
	                        "aqi": 77,
	                        "date": "2018-09-12",
	                        "quality": "良"
	                    },
	                    {
	                        "aqi": 82,
	                        "date": "2018-09-13",
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
	                    },
	                    {
	                        "aqi": 43,
	                        "dateTime": "2018-09-07 14:00:00"
	                    },
	                    {
	                        "aqi": 43,
	                        "dateTime": "2018-09-07 13:00:00"
	                    },
	                    {
	                        "aqi": 49,
	                        "dateTime": "2018-09-07 12:00:00"
	                    },
	                    {
	                        "aqi": 54,
	                        "dateTime": "2018-09-07 11:00:00"
	                    },
	                    {
	                        "aqi": 54,
	                        "dateTime": "2018-09-07 10:00:00"
	                    },
	                    {
	                        "aqi": 53,
	                        "dateTime": "2018-09-07 09:00:00"
	                    },
	                    {
	                        "aqi": 53,
	                        "dateTime": "2018-09-07 08:00:00"
	                    },
	                    {
	                        "aqi": 50,
	                        "dateTime": "2018-09-07 07:00:00"
	                    },
	                    {
	                        "aqi": 49,
	                        "dateTime": "2018-09-07 06:00:00"
	                    },
	                    {
	                        "aqi": 52,
	                        "dateTime": "2018-09-07 05:00:00"
	                    },
	                    {
	                        "aqi": 64,
	                        "dateTime": "2018-09-07 04:00:00"
	                    },
	                    {
	                        "aqi": 77,
	                        "dateTime": "2018-09-07 03:00:00"
	                    },
	                    {
	                        "aqi": 82,
	                        "dateTime": "2018-09-07 02:00:00"
	                    },
	                    {
	                        "aqi": 80,
	                        "dateTime": "2018-09-07 01:00:00"
	                    },
	                    {
	                        "aqi": 90,
	                        "dateTime": "2018-09-07 00:00:00"
	                    },
	                    {
	                        "aqi": 94,
	                        "dateTime": "2018-09-06 23:00:00"
	                    },
	                    {
	                        "aqi": 95,
	                        "dateTime": "2018-09-06 22:00:00"
	                    },
	                    {
	                        "aqi": 105,
	                        "dateTime": "2018-09-06 21:00:00"
	                    },
	                    {
	                        "aqi": 102,
	                        "dateTime": "2018-09-06 20:00:00"
	                    },
	                    {
	                        "aqi": 94,
	                        "dateTime": "2018-09-06 19:00:00"
	                    },
	                    {
	                        "aqi": 90,
	                        "dateTime": "2018-09-06 18:00:00"
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
	                },
	                {
	                    "date": "2018-09-09",
	                    "dayTime": "多云",
	                    "night": "多云",
	                    "temperature": "27°C / 19°C",
	                    "week": "星期日",
	                    "wind": "东北风 小于3级"
	                },
	                {
	                    "date": "2018-09-10",
	                    "dayTime": "多云",
	                    "night": "多云",
	                    "temperature": "28°C / 20°C",
	                    "week": "星期一",
	                    "wind": "东北风 小于3级"
	                },
	                {
	                    "date": "2018-09-11",
	                    "dayTime": "阴",
	                    "night": "多云",
	                    "temperature": "28°C / 23°C",
	                    "week": "星期二",
	                    "wind": "东北风 小于3级"
	                },
	                {
	                    "date": "2018-09-12",
	                    "dayTime": "阵雨",
	                    "night": "多云",
	                    "temperature": "28°C / 24°C",
	                    "week": "星期三",
	                    "wind": "东北风 小于3级"
	                },
	                {
	                    "date": "2018-09-13",
	                    "dayTime": "阵雨",
	                    "night": "多云",
	                    "temperature": "29°C / 24°C",
	                    "week": "星期四",
	                    "wind": "东北风 小于3级"
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
	                },
	                {
	                    "aqi": 53,
	                    "dateTime": "2018-09-09 06:00:00"
	                },
	                {
	                    "aqi": 54,
	                    "dateTime": "2018-09-09 05:00:00"
	                },
	                {
	                    "aqi": 49,
	                    "dateTime": "2018-09-09 04:00:00"
	                },
	                {
	                    "aqi": 50,
	                    "dateTime": "2018-09-09 03:00:00"
	                },
	                {
	                    "aqi": 50,
	                    "dateTime": "2018-09-09 02:00:00"
	                },
	                {
	                    "aqi": 50,
	                    "dateTime": "2018-09-09 01:00:00"
	                },
	                {
	                    "aqi": 49,
	                    "dateTime": "2018-09-09 00:00:00"
	                },
	                {
	                    "aqi": 46,
	                    "dateTime": "2018-09-08 23:00:00"
	                },
	                {
	                    "aqi": 47,
	                    "dateTime": "2018-09-08 22:00:00"
	                },
	                {
	                    "aqi": 44,
	                    "dateTime": "2018-09-08 21:00:00"
	                },
	                {
	                    "aqi": 39,
	                    "dateTime": "2018-09-08 20:00:00"
	                },
	                {
	                    "aqi": 37,
	                    "dateTime": "2018-09-08 19:00:00"
	                },
	                {
	                    "aqi": 32,
	                    "dateTime": "2018-09-08 18:00:00"
	                },
	                {
	                    "aqi": 31,
	                    "dateTime": "2018-09-08 17:00:00"
	                },
	                {
	                    "aqi": 30,
	                    "dateTime": "2018-09-08 16:00:00"
	                },
	                {
	                    "aqi": 29,
	                    "dateTime": "2018-09-08 15:00:00"
	                },
	                {
	                    "aqi": 27,
	                    "dateTime": "2018-09-08 14:00:00"
	                },
	                {
	                    "aqi": 24,
	                    "dateTime": "2018-09-08 13:00:00"
	                },
	                {
	                    "aqi": 20,
	                    "dateTime": "2018-09-08 12:00:00"
	                },
	                {
	                    "aqi": 17,
	                    "dateTime": "2018-09-08 11:00:00"
	                },
	                {
	                    "aqi": 18,
	                    "dateTime": "2018-09-08 10:00:00"
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

<table>
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
        <td>airCondition</td>
        <td>string</td>
        <td>是</td>
        <td>空气质量</td>
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
        <td>coldIndex</td>
        <td>string</td>
        <td>是</td>
        <td>感冒指数</td>
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
        <td>date</td>
        <td>string</td>
        <td>是</td>
        <td>日期</td>
        <td></td>
    </tr>
                                <tr>
        <td>distrct</td>
        <td>string</td>
        <td>是</td>
        <td>区县</td>
        <td></td>
    </tr>
                                <tr>
        <td>dressingIndex</td>
        <td>string</td>
        <td>是</td>
        <td>穿衣指数</td>
        <td></td>
    </tr>
                                <tr>
        <td>humidity</td>
        <td>string</td>
        <td>是</td>
        <td>湿度</td>
        <td></td>
    </tr>
                                <tr>
        <td>pollutionIndex</td>
        <td>string</td>
        <td>是</td>
        <td>空气污染指数</td>
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
        <td>sunset</td>
        <td>string</td>
        <td>是</td>
        <td>日落时间</td>
        <td></td>
    </tr>
                                <tr>
        <td>sunrise</td>
        <td>string</td>
        <td>是</td>
        <td>日出时间</td>
        <td></td>
    </tr>
                                <tr>
        <td>temperature</td>
        <td>string</td>
        <td>是</td>
        <td>温度</td>
        <td></td>
    </tr>
                                <tr>
        <td>time</td>
        <td>string</td>
        <td>是</td>
        <td>时间</td>
        <td></td>
    </tr>
                                <tr>
        <td>washIndex</td>
        <td>string</td>
        <td>是</td>
        <td>洗车指数</td>
        <td></td>
    </tr>
                                <tr>
        <td>weather</td>
        <td>string</td>
        <td>是</td>
        <td>天气</td>
        <td></td>
    </tr>
                                <tr>
        <td>week</td>
        <td>string</td>
        <td>是</td>
        <td>星期</td>
        <td></td>
    </tr>
                                <tr>
        <td>wind</td>
        <td>string</td>
        <td>是</td>
        <td>风向</td>
        <td></td>
    </tr>
                                <tr>
        <td>exerciseIndex</td>
        <td>string</td>
        <td>是</td>
        <td>运动指数</td>
        <td></td>
    </tr>
</tbody></table>	

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
	                        },
	                        {
	                            "district": "宣武区",
	                            "id": "10013"
	                        },
	                        {
	                            "district": "西城区",
	                            "id": "10014"
	                        },
	                        {
	                            "district": "通州区",
	                            "id": "10015"
	                        },
	                        {
	                            "district": "顺义区",
	                            "id": "10016"
	                        },
	                        {
	                            "district": "平谷区",
	                            "id": "10017"
	                        },
	                        {
	                            "district": "怀柔区",
	                            "id": "10018"
	                        },
	                        {
	                            "district": "海淀区",
	                            "id": "10019"
	                        },
	                        {
	                            "district": "丰台区",
	                            "id": "100110"
	                        },
	                        {
	                            "district": "房山区",
	                            "id": "100111"
	                        },
	                        {
	                            "district": "东城区",
	                            "id": "100112"
	                        },
	                        {
	                            "district": "大兴区",
	                            "id": "100113"
	                        },
	                        {
	                            "district": "崇文区",
	                            "id": "100114"
	                        },
	                        {
	                            "district": "昌平区",
	                            "id": "100115"
	                        },
	                        {
	                            "district": "延庆县",
	                            "id": "10010"
	                        },
	                        {
	                            "district": "密云县",
	                            "id": "10011"
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
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001009",
	                            "name": "汤粥",
	                            "parentId": "0010001002"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001010",
	                            "name": "西点",
	                            "parentId": "0010001002"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001011",
	                            "name": "主食",
	                            "parentId": "0010001002"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001012",
	                            "name": "饮品",
	                            "parentId": "0010001002"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001013",
	                            "name": "便当",
	                            "parentId": "0010001002"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001014",
	                            "name": "小吃",
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
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001018",
	                            "name": "炸",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001019",
	                            "name": "焖",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001020",
	                            "name": "炖",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001021",
	                            "name": "蒸",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001022",
	                            "name": "烩",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001023",
	                            "name": "熏",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001024",
	                            "name": "腌",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001025",
	                            "name": "煮",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001026",
	                            "name": "炝",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001027",
	                            "name": "卤",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001028",
	                            "name": "拌",
	                            "parentId": "0010001003"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001029",
	                            "name": "烤",
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
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001032",
	                            "name": "粤菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001033",
	                            "name": "闽菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001034",
	                            "name": "浙菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001035",
	                            "name": "湘菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001036",
	                            "name": "上海菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001037",
	                            "name": "徽菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001038",
	                            "name": "京菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001039",
	                            "name": "东北菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001040",
	                            "name": "西北菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001041",
	                            "name": "客家菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001042",
	                            "name": "台湾美食",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001043",
	                            "name": "泰国菜",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001044",
	                            "name": "日本料理",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001045",
	                            "name": "韩国料理",
	                            "parentId": "0010001004"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001046",
	                            "name": "西餐",
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
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001049",
	                            "name": "儿童食谱",
	                            "parentId": "0010001005"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001050",
	                            "name": "懒人食谱",
	                            "parentId": "0010001005"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001051",
	                            "name": "宵夜",
	                            "parentId": "0010001005"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001052",
	                            "name": "素食",
	                            "parentId": "0010001005"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001053",
	                            "name": "产妇食谱",
	                            "parentId": "0010001005"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001054",
	                            "name": "二人世界",
	                            "parentId": "0010001005"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001055",
	                            "name": "下午茶",
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
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001058",
	                            "name": "养胃",
	                            "parentId": "0010001006"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001059",
	                            "name": "滋阴",
	                            "parentId": "0010001006"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001060",
	                            "name": "补阳",
	                            "parentId": "0010001006"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001061",
	                            "name": "月经不调",
	                            "parentId": "0010001006"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001062",
	                            "name": "美容",
	                            "parentId": "0010001006"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001063",
	                            "name": "养生",
	                            "parentId": "0010001006"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001064",
	                            "name": "贫血",
	                            "parentId": "0010001006"
	                        }
	                    },
	                    {
	                        "categoryInfo": {
	                            "ctgId": "0010001065",
	                            "name": "润肺",
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
	        },
	        {
	            "cid": "5",
	            "name": "百科"
	        },
	        {
	            "cid": "7",
	            "name": "娱乐"
	        },
	        {
	            "cid": "8",
	            "name": "美文"
	        },
	        {
	            "cid": "9",
	            "name": "旅行"
	        },
	        {
	            "cid": "10",
	            "name": "媒体达人"
	        },
	        {
	            "cid": "11",
	            "name": "搞笑"
	        },
	        {
	            "cid": "12",
	            "name": "影视音乐"
	        },
	        {
	            "cid": "13",
	            "name": "互联网"
	        },
	        {
	            "cid": "14",
	            "name": "文史"
	        },
	        {
	            "cid": "15",
	            "name": "金融"
	        },
	        {
	            "cid": "16",
	            "name": "体育"
	        },
	        {
	            "cid": "17",
	            "name": "游戏"
	        },
	        {
	            "cid": "18",
	            "name": "两性"
	        },
	        {
	            "cid": "19",
	            "name": "社交交友"
	        },
	        {
	            "cid": "20",
	            "name": "女人"
	        },
	        {
	            "cid": "23",
	            "name": "购物"
	        },
	        {
	            "cid": "24",
	            "name": "美女"
	        },
	        {
	            "cid": "25",
	            "name": "微信技巧"
	        },
	        {
	            "cid": "26",
	            "name": "星座"
	        },
	        {
	            "cid": "27",
	            "name": "美食"
	        },
	        {
	            "cid": "28",
	            "name": "教育"
	        },
	        {
	            "cid": "29",
	            "name": "职场"
	        },
	        {
	            "cid": "30",
	            "name": "酷品"
	        },
	        {
	            "cid": "31",
	            "name": "母婴"
	        },
	        {
	            "cid": "32",
	            "name": "摄影"
	        },
	        {
	            "cid": "33",
	            "name": "创投"
	        },
	        {
	            "cid": "34",
	            "name": "典藏"
	        },
	        {
	            "cid": "35",
	            "name": "家装"
	        },
	        {
	            "cid": "36",
	            "name": "汽车"
	        },
	        {
	            "cid": "37",
	            "name": "段子"
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
















