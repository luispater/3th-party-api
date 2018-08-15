#Bing 每日壁纸#


- XML: 

	`http://www.bing.com/HPImageArchive.aspx?format=xml&idx=0&n=1&mkt=zh-CN`

		<images>
			<image>
				<startdate>20180814</startdate>
				<fullstartdate>201808140900</fullstartdate>
				<enddate>20180815</enddate>
				<url>
					https://www.bing.com/az/hprichbg/rb/OtterChillin_ZH-CN11488013572_1366x768.jpg
				</url>
				<urlBase>/az/hprichbg/rb/OtterChillin_ZH-CN11488013572</urlBase>
				<copyright>
				在设得兰群岛休憩的欧亚水獭，苏格兰 (© Scotland: The Big Picture/Minden Picture)
				</copyright>
				<copyrightlink>
					http://www.bing.com/search?q=%E6%AC%A7%E4%BA%9A%E6%B0%B4%E7%8D%AD&form=hpcapt&mkt=zh-cn
				</copyrightlink>
				<drk>1</drk>
				<top>1</top>
				<bot>1</bot>
				<hotspots/>
			</image>
			<tooltips>
				<loadMessage>
					<message>正在加载...</message>
				</loadMessage>
				<previousImage>
					<text>上一个图像</text>
				</previousImage>
				<nextImage>
					<text>下一个图像</text>
				</nextImage>
				<play>
					<text>播放视频</text>
				</play>
				<pause>
					<text>暂停视频</text>
				</pause>
			</tooltips>
		</images>


- JSON: 

	`http://www.bing.com/HPImageArchive.aspx?format=js&idx=0&n=1&mkt=en-US`

		{
		    "images": [
		        {
		            "startdate": "20180814",
		            "fullstartdate": "201808141600",
		            "enddate": "20180815",
		            "url": "/az/hprichbg/rb/OtterChillin_ZH-CN11488013572_1920x1080.jpg",
		            "urlbase": "/az/hprichbg/rb/OtterChillin_ZH-CN11488013572",
		            "copyright": "在设得兰群岛休憩的欧亚水獭，苏格兰 (© Scotland: The Big Picture/Minden Picture)",
		            "copyrightlink": "http://www.bing.com/search?q=%E6%AC%A7%E4%BA%9A%E6%B0%B4%E7%8D%AD&form=hpcapt&mkt=zh-cn",
		            "quiz": "/search?q=Bing+homepage+quiz&filters=WQOskey:%22HPQuiz_20180814_OtterChillin%22&FORM=HPQUIZ",
		            "wp": true,
		            "hsh": "edb03af9f51196ac48412f45be00f4b4",
		            "drk": 1,
		            "top": 1,
		            "bot": 1,
		            "hs": []
		        }
		    ],
		    "tooltips": {
		        "loading": "正在加载...",
		        "previous": "上一个图像",
		        "next": "下一个图像",
		        "walle": "此图片不能下载用作壁纸。",
		        "walls": "下载今日美图。仅限用作桌面壁纸。"
		    }
		}

- RSS: 
 	
 	`http://www.bing.com/HPImageArchive.aspx?format=rss&idx=0&n=1&mkt=en-US`
 	
	 	<rss version="2.0">
			<channel>
				<title>必应图片</title>
				<description>必应的主页图片存档</description>
				<link>http://bing.com/HPImageArchive.aspx?format=rss</link>
				<ttl>1440</ttl>
				<item>
					<title>
					在设得兰群岛休憩的欧亚水獭，苏格兰 (© Scotland: The Big Picture/Minden Picture)
					</title>
					<link>
					http://www.bing.com/az/hprichbg/rb/OtterChillin_ZH-CN11488013572_1366x768.jpg
					</link>
					<pubDate>周二, 14 8月 2018 09:00:00 G8T</pubDate>
					<description>
					<![CDATA[
						<img height="280" src="/az/hprichbg/rb/OtterChillin_ZH-CN11488013572_1366x768.jpg" usemap="#map1" border="0"/><map name="map1"></map>
					]]>
					</description>
				</item>
			</channel>
		</rss>
 	
 	
 	
 	`注：图片前面拼接url:https://www.bing.com`
 	