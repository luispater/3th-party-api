# 酷狗音乐web端数据接口

- [音乐新歌榜](#new-songs)
- [音乐排行榜](#rank)
- [排行榜分类歌曲列表](#rank-songs)
- [获取歌单列表](#plist)
- [获取歌单下的音乐列表](#plist-songs)
- [歌手分类列表](#singer-class)
- [歌手列表](#class-singers)
- [歌手信息](#singer-info)
- [歌曲详情](#song-info)
- [音乐详情-带歌词版本](#song-info-lyrics)
- [热搜列表](#hot-keywords)
- [搜索歌曲v2](#songs-search-v2)
- [搜索歌曲v3](#songs-search-v3)
- [搜索MV](#mv-search)
- [mv详情](#mv-info)


>酷狗音乐Web端音乐API接口数据整理,本音乐API数据整理仅用于学习研究,请勿将以下接口用来商业推广以及其他获利用途，如有版权问题请告知删除!


<h2 id="new-songs">音乐新歌榜</h2>

__说明:__ 获取新歌曲榜单

__接口地址:__ `http://m.kugou.com`

__参数:__

- `json`: true

__示例:__ [http://m.kugou.com/?json=true](http://m.kugou.com/?json=true)

__返回数据__

	{
	    "JS_CSS_DATE": 20130320,
	    "kg_domain": "http://m.kugou.com",
	    "src": "http://downmobile.kugou.com/promote/package/download/channel=6",
	    "fr": null,
	    "ver": "v3",
	    "data": [
	        {
	            "pay_type_320": 0,
	            "m4afilesize": 0,
	            "price_sq": 0,
	            "first": 1,
	            "filesize": 4702989,
	            "bitrate": 128,
	            "trans_param": {
	                "roaming_astrict": 0,
	                "display": 0,
	                "pay_block_tpl": 1,
	                "musicpack_advance": 0
	            },
	            "price": 0,
	            "inlist": 1,
	            "old_cpy": 1,
	            "pkg_price_sq": 0,
	            "pay_type": 0,
	            "topic_url": "",
	            "rp_type": "audio",
	            "pkg_price": 0,
	            "recommend_reason": "",
	            "filename": "白举纲 - 说走就走【说走就走之不说再见电影主题曲】",
	            "price_320": 0,
	            "extname": "mp3",
	            "hash": "3E4610179007CD0173A8B68663401927",
	            "audio_id": 42217281,
	            "privilege": 0,
	            "topic_url_320": "",
	            "addtime": "2018-08-28 00:13:38",
	            "pkg_price_320": 0,
	            "sqfilesize": 34874026,
	            "fail_process_320": 0,
	            "duration": 293,
	            "feetype": 0,
	            "320filesize": 11757305,
	            "rp_publish": 1,
	            "has_accompany": 0,
	            "topic_url_sq": "",
	            "remark": "《说走就走之不说再见》电影主题曲",
	            "isfirst": 0,
	            "sqhash": "40EE9BDE621BDA8BF9C2D2FFB0DD5A03",
	            "320privilege": 0,
	            "320hash": "B1F1A332F390A4E2B60129DA2DE52E67",
	            "fail_process": 0,
	            "album_id": "9616459",
	            "pay_type_sq": 0,
	            "mvhash": "",
	            "sqprivilege": 0,
	            "album_audio_id": 113327956,
	            "fail_process_sq": 0
	        },
	        {
	            "pay_type_320": 0,
	            "m4afilesize": 0,
	            "price_sq": 0,
	            "first": 1,
	            "filesize": 3497174,
	            "bitrate": 128,
	            "trans_param": {
	                "roaming_astrict": 0,
	                "display": 0,
	                "pay_block_tpl": 1,
	                "musicpack_advance": 0
	            },
	            "price": 0,
	            "inlist": 1,
	            "old_cpy": 1,
	            "pkg_price_sq": 0,
	            "pay_type": 0,
	            "topic_url": "",
	            "rp_type": "audio",
	            "pkg_price": 0,
	            "recommend_reason": "",
	            "filename": "老猫 - 土味情歌",
	            "price_320": 0,
	            "extname": "mp3",
	            "hash": "9AB82484710387A759EE740B6DCE8421",
	            "audio_id": 42214243,
	            "privilege": 0,
	            "topic_url_320": "",
	            "addtime": "2018-08-28 09:25:04",
	            "pkg_price_320": 0,
	            "sqfilesize": 28527767,
	            "fail_process_320": 0,
	            "duration": 218,
	            "feetype": 0,
	            "320filesize": 8742771,
	            "rp_publish": 1,
	            "has_accompany": 0,
	            "topic_url_sq": "",
	            "remark": "土味情歌",
	            "isfirst": 0,
	            "sqhash": "3DE2226F2ABAA73ED873412BB343FC12",
	            "320privilege": 0,
	            "320hash": "29444CC63CBD32F254066D545A561E6F",
	            "fail_process": 0,
	            "album_id": "9614160",
	            "pay_type_sq": 0,
	            "mvhash": "",
	            "sqprivilege": 0,
	            "album_audio_id": 113327958,
	            "fail_process_sq": 0
	        }
	    ],
	    "banner": [
	        {
	            "imgurl": "http://imge.kugou.com/mobilebanner/20180823/20180823185717600490.jpg",
	            "title": "【举铁必备】肌肉撕裂者在健身房听什么？",
	            "id": 9375,
	            "type": 1,
	            "online": 1535385458,
	            "extra": {
	                "trans_param": {
	                    "special_tag": 0
	                },
	                "play_count": 422763,
	                "specialname": "【举铁必备】肌肉撕裂者在健身房听什么？",
	                "publishtime": "2018-08-08",
	                "singername": "",
	                "intro": "热爱健身，那就意味着：\n沉溺在健身房\n听着燥热的歌\n闻着弥漫在空气中汗液的味道\n举着生锈的铁\n孤独 自我 拒绝不利健康的东西\n只为热爱\n我不后悔\n为了改变\n\n真正的强大是来源于健身这项运动对你人格上、精神上的塑造。苦其心志，劳其筋骨，经历过大重量的酣畅淋漓，也经历过减脂期对身体的严苛洗礼，你所得到的不应该仅仅是肌肉，你所展示给别人的也不应该仅仅是外在。而是你那颗通过百般磨难，遭受各种重量碾压后千锤百炼的强大内心。",
	                "songcount": 41,
	                "imgurl": "http://imge.kugou.com/soft/collection/{size}/20180808/20180808150904752284.jpg",
	                "suid": 1321573048,
	                "specialid": 504314,
	                "collectcount": 2711,
	                "slid": 0,
	                "tourl": "http://m.kugou.com/plist/list/504314"
	            }
	        },
	        {
	            "imgurl": "http://imge.kugou.com/mobilebanner/20180827/20180827162914455541.jpg",
	            "title": "精彩直播预告",
	            "id": 9399,
	            "type": 4,
	            "online": 1535358590,
	            "extra": {
	                "tourl": "http://sdn.kugou.com/link.aspx?id=65906&dl=1"
	            }
	        }
	    ],
	    "__Tpl": "index/index.html"
	}


<h2 id="rank">音乐排行榜</h2>

__说明:__ 获取音乐排行榜

__参数:__

- `json`：true

__接口地址:__ `http://m.kugou.com/rank/list`

__示例:__ [http://m.kugou.com/rank/list?json=true](http://m.kugou.com/rank/list?json=true)

__返回数据__

	{
	    "JS_CSS_DATE": 20130320,
	    "kg_domain": "http://m.kugou.com",
	    "src": "http://downmobile.kugou.com/promote/package/download/channel=6",
	    "fr": null,
	    "ver": "v3",
	    "rank": {
	        "total": 24,
	        "list": [
	            {
	                "rankid": 6666,
	                "id": 1,
	                "update_frequency": "每天",
	                "intro": "数据来源：酷狗\r\n排序方式：按歌曲搜索播放量的涨幅排序\r\n更新周期：每天",
	                "jump_url": "",
	                "jump_title": "",
	                "imgurl": "http://imge.kugou.com/mcommon/{size}/20180824/20180824183716926902.jpg",
	                "banner7url": "http://imge.kugou.com/mcommon/{size}/20180824/20180824183723328334.png",
	                "isvol": 1,
	                "bannerurl": "http://imge.kugou.com/mcommonbanner/{size}/20180824/20180824183726102467.jpg",
	                "custom_type": 0,
	                "rankname": "酷狗飙升榜",
	                "ranktype": 2
	            }
	        ]
	    },
	    "__Tpl": "rank/list.html"
	}

<h2 id="rank-songs">排行榜分类歌曲列表</h2>

__说明:__ 排行榜分类歌曲列表

__接口地址:__ `http://m.kugou.com/rank/info`

__必选参数:__

- `rankid` ：排行榜分类下id
- `json` ：返回类型
- `page`：页码

__示例:__ [http://m.kugou.com/rank/info/?rankid=22163&page=1&json=true](http://m.kugou.com/rank/info/?rankid=22163&page=1&json=true)

__返回数据__

	{
	    "JS_CSS_DATE": 20130320,
	    "kg_domain": "http://m.kugou.com",
	    "src": "http://downmobile.kugou.com/promote/package/download/channel=6",
	    "fr": null,
	    "ver": "v3",
	    "info": {
	        "rankid": 22163,
	        "id": 40,
	        "update_frequency": "周一",
	        "intro": "数据来源：音乐之声\r\n排序方式：由音乐之声主持人及编辑进行专业打分，综合短信、销量、微博投票的结果进行排序\r\n更新周期：周一",
	        "jump_url": "",
	        "jump_title": "",
	        "imgurl": "http://imge.kugou.com/mcommon/{size}/20180824/20180824190434287350.jpg",
	        "banner7url": "http://imge.kugou.com/mcommon/{size}/20180824/20180824190438837704.png",
	        "isvol": 1,
	        "bannerurl": "http://imge.kugou.com/mcommonbanner/{size}/20180824/20180824190440797224.jpg",
	        "custom_type": 0,
	        "rankname": "中国TOP排行榜",
	        "ranktype": 1
	    },
	    "songs": {
	        "total": 3,
	        "page": 1,
	        "pagesize": 30,
	        "timestamp": 1535506636,
	        "list": [
	            {
	                "pay_type_320": 0,
	                "m4afilesize": 0,
	                "price_sq": 0,
	                "first": 0,
	                "filesize": 4009238,
	                "bitrate": 128,
	                "trans_param": {
	                    "roaming_astrict": 0,
	                    "display": 0,
	                    "pay_block_tpl": 1,
	                    "musicpack_advance": 0
	                },
	                "price": 0,
	                "inlist": 1,
	                "old_cpy": 1,
	                "pkg_price_sq": 0,
	                "pay_type": 0,
	                "topic_url": "",
	                "rp_type": "audio",
	                "pkg_price": 0,
	                "recommend_reason": "",
	                "filename": "薛之谦 - 怪咖【内地】",
	                "price_320": 0,
	                "extname": "mp3",
	                "hash": "62FD6C7D70ADBB5264E41569885563D4",
	                "audio_id": 39003366,
	                "privilege": 0,
	                "topic_url_320": "",
	                "addtime": "2018-08-27 14:42:56",
	                "pkg_price_320": 0,
	                "sqfilesize": 25563631,
	                "fail_process_320": 0,
	                "duration": 250,
	                "feetype": 0,
	                "320filesize": 10022660,
	                "rp_publish": 1,
	                "has_accompany": 1,
	                "topic_url_sq": "",
	                "remark": "怪咖",
	                "isfirst": 0,
	                "sqhash": "DED1718432137A7B7F5B2881577521FB",
	                "320privilege": 0,
	                "320hash": "597C18086AD47B75780F227524E7E479",
	                "fail_process": 0,
	                "album_id": "8655175",
	                "pay_type_sq": 0,
	                "mvhash": "77F7148D007619FCE1E11AC762A353DF",
	                "sqprivilege": 0,
	                "album_audio_id": 108965808,
	                "fail_process_sq": 0
	            },
	            {
	                "pay_type_320": 0,
	                "m4afilesize": 0,
	                "price_sq": 0,
	                "first": 0,
	                "filesize": 4087266,
	                "bitrate": 128,
	                "trans_param": {
	                    "roaming_astrict": 0,
	                    "display": 0,
	                    "pay_block_tpl": 1,
	                    "musicpack_advance": 0
	                },
	                "price": 0,
	                "inlist": 1,
	                "old_cpy": 1,
	                "pkg_price_sq": 0,
	                "pay_type": 0,
	                "topic_url": "",
	                "rp_type": "audio",
	                "pkg_price": 0,
	                "recommend_reason": "",
	                "filename": "许嵩 - 大千世界【内地】",
	                "price_320": 0,
	                "extname": "mp3",
	                "hash": "608642E601C009E2E0970B78C6C1475B",
	                "audio_id": 38451531,
	                "privilege": 0,
	                "topic_url_320": "",
	                "addtime": "2018-08-27 14:42:57",
	                "pkg_price_320": 0,
	                "sqfilesize": 28673086,
	                "fail_process_320": 0,
	                "duration": 255,
	                "feetype": 0,
	                "320filesize": 10446407,
	                "rp_publish": 1,
	                "has_accompany": 1,
	                "topic_url_sq": "",
	                "remark": "寻宝游戏",
	                "isfirst": 0,
	                "sqhash": "E8F44B950952AEDCA78F6DC4B82C057F",
	                "320privilege": 0,
	                "320hash": "1C8AAD784999CF0C3501A68105BB97DB",
	                "fail_process": 0,
	                "album_id": "8778792",
	                "pay_type_sq": 0,
	                "mvhash": "2B1EAE4D1CA48BB863C167CC1FB3B157",
	                "sqprivilege": 0,
	                "album_audio_id": 110010418,
	                "fail_process_sq": 0
	            }
	        ]
	    },
	    "pagesize": 30,
	    "__Tpl": "rank/info.html"
	}


<h2 id="plist">音乐歌单</h2>

__说明:__ 音乐歌单

__接口地址:__ `http://m.kugou.com/plist/index`

__参数:__

- `json`：true
- `page`：页码

__接口地址:__ [http://m.kugou.com/plist/index?json=true&page=2](http://m.kugou.com/plist/index?json=true&page=2)

__返回数据__

	{
	    "JS_CSS_DATE": 20130320,
	    "kg_domain": "http://m.kugou.com",
	    "src": "http://downmobile.kugou.com/promote/package/download/channel=6",
	    "fr": null,
	    "ver": "v3",
	    "plist": {
	        "list": {
	            "timestamp": 1535512851,
	            "info": [
	                {
	                    "recommendfirst": 0,
	                    "specialname": "摇滚硬汉唱分手：撕心裂肺下释放悲伤",
	                    "intro": "当重金属的老将把狂躁、\n愤怒的激情沉淀下来，\n用最朴素最真实的声音唱出的柔情歌曲，\n那绝对是摇滚乐中的传世经典。\n\n是啊，毕竟再强悍的人在深爱的人面前也会感到自己的无力，会不知所措。当一切坚强的外衣卸下来了，那必定呈现出汉子内心里最为柔情的那一面",
	                    "songs": [
	                        {
	                            "pay_type_320": 0,
	                            "m4afilesize": 0,
	                            "price_sq": 0,
	                            "filesize": 3410094,
	                            "bitrate": 128,
	                            "trans_param": {
	                                "roaming_astrict": 0,
	                                "display": 0,
	                                "pay_block_tpl": 1,
	                                "musicpack_advance": 0
	                            },
	                            "price": 0,
	                            "inlist": 1,
	                            "old_cpy": 1,
	                            "fail_process_sq": 0,
	                            "pay_type": 0,
	                            "topic_url": "",
	                            "rp_type": "audio",
	                            "pkg_price": 0,
	                            "feetype": 0,
	                            "filename": "Rod Stewart - It's a Heartache",
	                            "price_320": 0,
	                            "extname": "mp3",
	                            "hash": "0CE52D802BB514BEC099DABCDC79AF02",
	                            "audio_id": 603058,
	                            "privilege": 0,
	                            "pkg_price_320": 0,
	                            "album_id": "565201",
	                            "fail_process_320": 0,
	                            "sqprivilege": 0,
	                            "mvhash": "",
	                            "320filesize": 8539034,
	                            "rp_publish": 1,
	                            "has_accompany": 1,
	                            "topic_url_sq": "",
	                            "320hash": "4A28D40E54BA8319FE8586010C3993D7",
	                            "remark": "心痛的感觉",
	                            "fail_process": 0,
	                            "320privilege": 0,
	                            "sqhash": "",
	                            "duration": 213,
	                            "sqfilesize": 0,
	                            "pay_type_sq": 0,
	                            "album_audio_id": 28235475,
	                            "brief": "",
	                            "topic_url_320": "",
	                            "pkg_price_sq": 0
	                        }
	                    ],
	                    "collectcount": 427,
	                    "is_selected": 0,
	                    "selected_reason": "",
	                    "slid": 0,
	                    "trans_param": {
	                        "special_tag": 0
	                    },
	                    "publishtime": "2018-07-28 00:00:00",
	                    "singername": "",
	                    "verified": 0,
	                    "ugc_talent_review": 1,
	                    "songcount": 12,
	                    "user_avatar": "http://imge.kugou.com/kugouicon/165/20180801/20180801122659226993.jpg",
	                    "playcount": 116394,
	                    "suid": 1287576754,
	                    "specialid": 493768,
	                    "username": "上晏",
	                    "imgurl": "http://imge.kugou.com/soft/collection/{size}/20180730/20180730125503291356.jpg",
	                    "user_type": 1
	                },
	                {
	                    "recommendfirst": 0,
	                    "specialname": "美貌与性感并存：韩国女团solo成员大盘点",
	                    "intro": "韩国女团经历了几代发展，曾经由二代女团掌握的天下，如今已然成为了四代女团的天下，代表的女团主要有BLACKPINK,Twice,Girlfriend等\n在韩国本土来说，女团的音源成绩总是比男团的靠前，不仅仅是因为长得好看，还有的是才华，比如MAMAMOO全团的成员，都是实打实的好主唱，不论是做词作曲，还是唱歌，都是超强。\n也有一些女团，虽然整体发展并不是很明朗，却也是凭借个别成员的突出，而让整个团队有了一定的发展机会。\n此单主要盘点的是韩国女团里solo过的，或者是出过专辑的成员，领略人美歌还好听的成员们的魅力。",
	                    "songs": [
	                        {
	                            "pay_type_320": 0,
	                            "m4afilesize": 0,
	                            "price_sq": 0,
	                            "filesize": 3178623,
	                            "bitrate": 128,
	                            "trans_param": {
	                                "roaming_astrict": 0,
	                                "display": 0,
	                                "pay_block_tpl": 1,
	                                "musicpack_advance": 0
	                            },
	                            "price": 0,
	                            "inlist": 1,
	                            "old_cpy": 1,
	                            "fail_process_sq": 0,
	                            "pay_type": 0,
	                            "topic_url": "",
	                            "rp_type": "audio",
	                            "pkg_price": 0,
	                            "feetype": 0,
	                            "filename": "徐贤 - Stress",
	                            "price_320": 0,
	                            "extname": "mp3",
	                            "hash": "D9FD35A0DF9D56D28DFC48D54F140787",
	                            "audio_id": 23429625,
	                            "privilege": 0,
	                            "pkg_price_320": 0,
	                            "album_id": "0",
	                            "fail_process_320": 0,
	                            "sqprivilege": 0,
	                            "mvhash": "",
	                            "320filesize": 0,
	                            "rp_publish": 1,
	                            "has_accompany": 0,
	                            "topic_url_sq": "",
	                            "320hash": "",
	                            "remark": "",
	                            "fail_process": 0,
	                            "320privilege": 0,
	                            "sqhash": "",
	                            "duration": 199,
	                            "sqfilesize": 0,
	                            "pay_type_sq": 0,
	                            "album_audio_id": 51416714,
	                            "brief": "",
	                            "topic_url_320": "",
	                            "pkg_price_sq": 0
	                        },
	                        {
	                            "pay_type_320": 0,
	                            "m4afilesize": 0,
	                            "price_sq": 0,
	                            "filesize": 3708353,
	                            "bitrate": 128,
	                            "trans_param": {
	                                "roaming_astrict": 0,
	                                "display": 0,
	                                "pay_block_tpl": 1,
	                                "musicpack_advance": 0
	                            },
	                            "price": 0,
	                            "inlist": 1,
	                            "old_cpy": 1,
	                            "fail_process_sq": 0,
	                            "pay_type": 0,
	                            "topic_url": "",
	                            "rp_type": "audio",
	                            "pkg_price": 0,
	                            "feetype": 0,
	                            "filename": "LOCO、华莎 - 주지마 (别给我)",
	                            "price_320": 0,
	                            "extname": "mp3",
	                            "hash": "D8794BF148DC18C2C2B0A6D1E3947273",
	                            "audio_id": 37715670,
	                            "privilege": 0,
	                            "pkg_price_320": 0,
	                            "album_id": "8498794",
	                            "fail_process_320": 0,
	                            "sqprivilege": 0,
	                            "mvhash": "4DF756D5B1872A346307107F096E4DF0",
	                            "320filesize": 9270577,
	                            "rp_publish": 1,
	                            "has_accompany": 1,
	                            "topic_url_sq": "",
	                            "320hash": "2E15B91E22113AE7EFB32A8CBD56FBB5",
	                            "remark": "不要给",
	                            "fail_process": 0,
	                            "320privilege": 0,
	                            "sqhash": "",
	                            "duration": 231,
	                            "sqfilesize": 0,
	                            "pay_type_sq": 0,
	                            "album_audio_id": 107181368,
	                            "brief": "",
	                            "topic_url_320": "",
	                            "pkg_price_sq": 0
	                        }
	                    ],
	                    "collectcount": 303,
	                    "is_selected": 0,
	                    "selected_reason": "",
	                    "slid": 0,
	                    "trans_param": {
	                        "special_tag": 0
	                    },
	                    "publishtime": "2018-07-28 00:00:00",
	                    "singername": "",
	                    "verified": 0,
	                    "ugc_talent_review": 1,
	                    "songcount": 4,
	                    "user_avatar": "http://imge.kugou.com/kugouicon/165/20180725/20180725163304817260.jpg",
	                    "playcount": 97409,
	                    "suid": 1314415167,
	                    "specialid": 493283,
	                    "username": "时光如水",
	                    "imgurl": "http://imge.kugou.com/soft/collection/{size}/20180730/20180730165009237230.jpg",
	                    "user_type": 1
	                }
	            ],
	            "total": 1762
	        },
	        "pagesize": 30
	    },
	    "pagesize": 30,
	    "__Tpl": "plist/index.html"
	}


<h2 id="plist-songs">获取歌单下的音乐列表</h2>

__说明:__ 获取歌单下的音乐列表


__接口地址:__ `http://m.kugou.com/plist/list/{specialid}`

__必选参数:__

- `specialid` 125032
- `json` true

__示例:__ [http://m.kugou.com/plist/list/125032?json=true](http://m.kugou.com/plist/list/125032?json=true)

__返回数据__

	{
	    "JS_CSS_DATE": 20130320,
	    "kg_domain": "http://m.kugou.com",
	    "src": "http://downmobile.kugou.com/promote/package/download/channel=6",
	    "fr": null,
	    "ver": "v3",
	    "list": {
	        "list": {
	            "timestamp": 1535515613,
	            "info": [
	                {
	                    "pay_type_320": 0,
	                    "m4afilesize": 0,
	                    "price_sq": 0,
	                    "filesize": 4210171,
	                    "bitrate": 128,
	                    "trans_param": {
	                        "roaming_astrict": 0,
	                        "display": 0,
	                        "pay_block_tpl": 1,
	                        "musicpack_advance": 0
	                    },
	                    "price": 0,
	                    "inlist": 1,
	                    "old_cpy": 1,
	                    "pkg_price_sq": 0,
	                    "pay_type": 0,
	                    "topic_url": "",
	                    "fail_process_320": 0,
	                    "pkg_price": 0,
	                    "feetype": 0,
	                    "filename": "孟庭苇 - 没有情人的情人节",
	                    "price_320": 0,
	                    "extname": "mp3",
	                    "hash": "087F6543D580F86AB1B179E1800B4FE7",
	                    "mvhash": "BA82B56916E3A8224D03D957D7376F23",
	                    "privilege": 0,
	                    "album_id": "561101",
	                    "sqprivilege": 0,
	                    "320privilege": 0,
	                    "album_audio_id": 28185196,
	                    "rp_type": "audio",
	                    "320filesize": 10192140,
	                    "rp_publish": 1,
	                    "has_accompany": 1,
	                    "topic_url_sq": "",
	                    "audio_id": 324814,
	                    "remark": "节日的狂欢情人的浪漫",
	                    "pkg_price_320": 0,
	                    "fail_process": 0,
	                    "sqhash": "A1C9E9FCA0442BA8859540BBA8005ADD",
	                    "duration": 263,
	                    "sqfilesize": 24960568,
	                    "pay_type_sq": 0,
	                    "fail_process_sq": 0,
	                    "brief": "",
	                    "topic_url_320": "",
	                    "320hash": "6CA881C9A8258689227AF0B6AF4CFCD5"
	                },
	                {
	                    "pay_type_320": 0,
	                    "m4afilesize": 0,
	                    "price_sq": 0,
	                    "filesize": 4165334,
	                    "bitrate": 128,
	                    "trans_param": {
	                        "roaming_astrict": 0,
	                        "display": 0,
	                        "pay_block_tpl": 1,
	                        "musicpack_advance": 0
	                    },
	                    "price": 0,
	                    "inlist": 1,
	                    "old_cpy": 1,
	                    "pkg_price_sq": 0,
	                    "pay_type": 0,
	                    "topic_url": "",
	                    "fail_process_320": 0,
	                    "pkg_price": 0,
	                    "feetype": 0,
	                    "filename": "张真 - 携手游人间",
	                    "price_320": 0,
	                    "extname": "mp3",
	                    "hash": "EDE90DCED53031261473FAF2727614F2",
	                    "mvhash": "1315C8480F0B83971D97351C2BBC891C",
	                    "privilege": 0,
	                    "album_id": "610239",
	                    "sqprivilege": 0,
	                    "320privilege": 0,
	                    "album_audio_id": 28743171,
	                    "rp_type": "audio",
	                    "320filesize": 10396919,
	                    "rp_publish": 1,
	                    "has_accompany": 1,
	                    "topic_url_sq": "",
	                    "audio_id": 68780,
	                    "remark": "《包青天》电视剧片尾曲",
	                    "pkg_price_320": 0,
	                    "fail_process": 0,
	                    "sqhash": "FE76CBBE05D4F04BB9E71C8EF3862F48",
	                    "duration": 259,
	                    "sqfilesize": 29157410,
	                    "pay_type_sq": 0,
	                    "fail_process_sq": 0,
	                    "brief": "",
	                    "topic_url_320": "",
	                    "320hash": "B442B1F3999B145FBB5E1BE558025A74"
	                },
	                {
	                    "pay_type_320": 0,
	                    "m4afilesize": 0,
	                    "price_sq": 0,
	                    "filesize": 3515386,
	                    "bitrate": 128,
	                    "trans_param": {
	                        "roaming_astrict": 0,
	                        "display": 0,
	                        "pay_block_tpl": 1,
	                        "musicpack_advance": 0
	                    },
	                    "price": 0,
	                    "inlist": 1,
	                    "old_cpy": 1,
	                    "pkg_price_sq": 0,
	                    "pay_type": 0,
	                    "topic_url": "",
	                    "fail_process_320": 0,
	                    "pkg_price": 0,
	                    "feetype": 0,
	                    "filename": "张清芳 - 大雨的夜里",
	                    "price_320": 0,
	                    "extname": "mp3",
	                    "hash": "2F3DE00A4D8B808450780FA9FF5A89B6",
	                    "mvhash": "0405F2379C0BB8B6BDDD58D8A7B929E6",
	                    "privilege": 0,
	                    "album_id": "575484",
	                    "sqprivilege": 0,
	                    "320privilege": 0,
	                    "album_audio_id": 28366279,
	                    "rp_type": "audio",
	                    "320filesize": 8611131,
	                    "rp_publish": 1,
	                    "has_accompany": 1,
	                    "topic_url_sq": "",
	                    "audio_id": 63023,
	                    "remark": "大雨的夜里",
	                    "pkg_price_320": 0,
	                    "fail_process": 0,
	                    "sqhash": "CA1C02011D022B2BC66C6D5E8FDD7DBA",
	                    "duration": 219,
	                    "sqfilesize": 26690522,
	                    "pay_type_sq": 0,
	                    "fail_process_sq": 0,
	                    "brief": "",
	                    "topic_url_320": "",
	                    "320hash": "FBBFDD7EB279668A319ECAEB6E4101AF"
	                }
	            ],
	            "total": 3
	        },
	        "pagesize": 30,
	        "page": 1
	    },
	    "info": {
	        "list": {
	            "trans_param": {
	                "special_tag": 0
	            },
	            "specialname": "连怀旧情歌都不爱，怎么能爱你",
	            "nickname": "水色小妖",
	            "publishtime": "2017-05-27 00:00:00",
	            "singername": "",
	            "intro": "我是这么的怀旧的人，专一又长情。如果我连这些经典情歌都不爱了，还有什么资格去爱你呢，哈哈哈哈哈！",
	            "commentcount": 46,
	            "songcount": 17,
	            "imgurl": "http://imge.kugou.com/soft/collection/{size}/20170527/20170527114227818831.jpg",
	            "collectcount": 17337,
	            "suid": 509005005,
	            "tags": [
	                {
	                    "tagname": "经典",
	                    "tagid": 12
	                },
	                {
	                    "tagname": "80后",
	                    "tagid": 14
	                }
	            ],
	            "playcount": 18856008,
	            "specialid": 125032,
	            "slid": 31
	        }
	    },
	    "pagesize": 30,
	    "__Tpl": "plist/list.html"
	}

<h2 id="singer-class">歌手分类</h2>

__说明:__ 获取 歌手分类

__接口地址:__ `http://m.kugou.com/singer/class`

__参数:__

- `json`:true

__示例:__ [http://m.kugou.com/singer/class?json=true](http://m.kugou.com/singer/class?json=true)

__返回数据__

	{
	    "JS_CSS_DATE": 20130320,
	    "kg_domain": "http://m.kugou.com",
	    "src": "http://downmobile.kugou.com/promote/package/download/channel=6",
	    "fr": null,
	    "ver": "v3",
	    "list": [
	        {
	            "classid": 88,
	            "classname": "热门歌手",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-11.jpg"
	        },
	        {
	            "classid": 1,
	            "classname": "华语男歌手",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-1.jpg"
	        },
	        {
	            "classid": 2,
	            "classname": "华语女歌手",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-2.jpg"
	        },
	        {
	            "classid": 3,
	            "classname": "华语组合",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-3.jpg"
	        },
	        {
	            "classid": 4,
	            "classname": "日韩男歌手",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-4.jpg"
	        },
	        {
	            "classid": 5,
	            "classname": "日韩女歌手",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-5.jpg"
	        },
	        {
	            "classid": 6,
	            "classname": "日韩组合",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-6.jpg"
	        },
	        {
	            "classid": 7,
	            "classname": "欧美男歌手",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-7.jpg"
	        },
	        {
	            "classid": 8,
	            "classname": "欧美女歌手",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-8.jpg"
	        },
	        {
	            "classid": 9,
	            "classname": "欧美组合",
	            "imgurl": "http://mobileimg.kugou.com/billImage/150/26-9.jpg"
	        }
	    ],
	    "__Tpl": "singer/class.html"
	}


<h2 id="class-singers">歌手分类下面的歌手列表</h2>

__说明:__ 获取 歌手分类下面的歌手列表

__接口地址:__ `http://m.kugou.com/singer/list/{classid}`

__必选参数:__

- `classid` : 分类ID

__接口地址:__ [http://m.kugou.com/singer/list/88?json=true](http://m.kugou.com/singer/list/88?json=true)

__返回数据__

	{
	    "JS_CSS_DATE": 20130320,
	    "kg_domain": "http://m.kugou.com",
	    "src": "http://downmobile.kugou.com/promote/package/download/channel=6",
	    "fr": null,
	    "ver": "v3",
	    "classid": 88,
	    "classname": "热门歌手",
	    "singers": {
	        "total": 50,
	        "list": {
	            "total": 50,
	            "info": [
	                {
	                    "singerid": 4490,
	                    "singername": "G.E.M.邓紫棋",
	                    "imgurl": "http://singerimg.kugou.com/uploadpic/pass/softhead/{size}/20180530/20180530085619631.jpg"
	                },
	                {
	                    "singerid": 3521,
	                    "singername": "张学友",
	                    "imgurl": "http://singerimg.kugou.com/uploadpic/pass/softhead/{size}/20140527/20140527095042283066.jpg"
	                },
	                {
	                    "singerid": 1573,
	                    "singername": "刘德华",
	                    "imgurl": "http://singerimg.kugou.com/uploadpic/pass/softhead/{size}/20180507/20180507120242140.jpg"
	                },
	                {
	                    "singerid": 86281,
	                    "singername": "庄心妍",
	                    "imgurl": "http://singerimg.kugou.com/uploadpic/pass/softhead/{size}/20180302/20180302142740562.jpg"
	                },
	                {
	                    "singerid": 185839,
	                    "singername": "白小白",
	                    "imgurl": "http://singerimg.kugou.com/uploadpic/pass/softhead/{size}/20180808/20180808180400236.jpg"
	                },
	                {
	                    "singerid": 730,
	                    "singername": "刀郎",
	                    "imgurl": "http://singerimg.kugou.com/uploadpic/pass/softhead/{size}/20140520/20140520101227819989.jpg"
	                }
	            ]
	        },
	        "pagesize": 50,
	        "page": 1
	    },
	    "pagesize": 30,
	    "__Tpl": "singer/list.html"
	}


<h2 id="singer-info">歌手信息</H2>

__说明:__ 获取 歌手分类

__接口地址:__ `http://m.kugou.com/singer/info/{singerid}`

注：`该接口目前有些问题 需要追加request headers 设置成手机浏览器`

__必选参数:__

- `singerid` : 歌手id  295762 
- `json` : true

__示例:__ [http://m.kugou.com/singer/info/295762?json=true](http://m.kugou.com/singer/info/295762?json=true)

__返回数据__

	{
	    "JS_CSS_DATE": 20130320,
	    "kg_domain": "http://m.kugou.com",
	    "src": "http://sdn.kugou.com/link.aspx?id=16632&dl=1",
	    "fr": null,
	    "ver": "v3",
	    "info": {
	        "mvcount": 0,
	        "has_long_intro": 0,
	        "intro": "DJ电音分享QQ群号133587037 \n\nDJ杨二爷官方QQ625406903",
	        "songcount": 73,
	        "imgurl": "http://singerimg.kugou.com/uploadpic/softhead/{size}/20180828/20180828174515601.jpg",
	        "profile": "",
	        "singerid": 295762,
	        "singername": "杨二爷",
	        "albumcount": 5
	    },
	    "songs": {
	        "total": 48,
	        "pagesize": 30,
	        "list": [
	            {
	                "pay_type_320": 0,
	                "m4afilesize": 0,
	                "price_sq": 0,
	                "filesize": 2994045,
	                "bitrate": 128,
	                "trans_param": {
	                    "roaming_astrict": 0,
	                    "display": 0,
	                    "pay_block_tpl": 1,
	                    "musicpack_advance": 0
	                },
	                "price": 0,
	                "inlist": 1,
	                "old_cpy": 1,
	                "pkg_price_sq": 0,
	                "pay_type": 0,
	                "topic_url": "",
	                "rp_type": "audio",
	                "pkg_price": 0,
	                "feetype": 0,
	                "filename": "杨二爷 - 厉害了我的哥 (DJ版)",
	                "price_320": 0,
	                "topic_url_320": "",
	                "hash": "657AE90F5A875FE6D8139E0848564053",
	                "mvhash": "",
	                "privilege": 0,
	                "album_id": "2282728",
	                "sqhash": "",
	                "album_audio_id": 59741910,
	                "pkg_price_320": 0,
	                "320filesize": 7578689,
	                "rp_publish": 1,
	                "duration": 187,
	                "topic_url_sq": "",
	                "fail_process_320": 0,
	                "remark": "全民社会摇",
	                "extname": "mp3",
	                "320privilege": 0,
	                "fail_process": 0,
	                "fail_process_sq": 0,
	                "has_accompany": 0,
	                "pay_type_sq": 0,
	                "audio_id": 3393896,
	                "sqprivilege": 0,
	                "sqfilesize": 0,
	                "320hash": "FF2F29FCABBC6E52BA71860E988B4D59"
	            },
	            {
	                "pay_type_320": 0,
	                "m4afilesize": 0,
	                "price_sq": 0,
	                "filesize": 2768258,
	                "bitrate": 130,
	                "trans_param": {
	                    "roaming_astrict": 0,
	                    "display": 0,
	                    "pay_block_tpl": 1,
	                    "musicpack_advance": 0
	                },
	                "price": 0,
	                "inlist": 1,
	                "old_cpy": 1,
	                "pkg_price_sq": 0,
	                "pay_type": 0,
	                "topic_url": "",
	                "rp_type": "audio",
	                "pkg_price": 0,
	                "feetype": 0,
	                "filename": "杨二爷 - 听觉盛宴 (DJ版)",
	                "price_320": 0,
	                "topic_url_320": "",
	                "hash": "7EAB5ACB6651A3B72203665455E0B3D1",
	                "mvhash": "",
	                "privilege": 0,
	                "album_id": "531819",
	                "sqhash": "",
	                "album_audio_id": 61695706,
	                "pkg_price_320": 0,
	                "320filesize": 6763713,
	                "rp_publish": 1,
	                "duration": 169,
	                "topic_url_sq": "",
	                "fail_process_320": 0,
	                "remark": "银川一把火",
	                "extname": "mp3",
	                "320privilege": 0,
	                "fail_process": 0,
	                "fail_process_sq": 0,
	                "has_accompany": 0,
	                "pay_type_sq": 0,
	                "audio_id": 4371908,
	                "sqprivilege": 0,
	                "sqfilesize": 0,
	                "320hash": "3F1D91CEF2E9BD9AFDDE76D698FA50D2"
	            }
	        ]
	    },
	    "__Tpl": "singer/info.html"
	}


<h2 id="song-info">音乐详情</h2>

__说明:__ 获取 歌曲音乐详情信息

__接口地址:__ `http://m.kugou.com/app/i/getSongInfo.php`

__参数:__

`hash`：音乐列表下的 音乐id
- `cmd`：playInfo

__接口地址:__ [http://m.kugou.com/app/i/getSongInfo.php?cmd=playInfo&hash=CB7EE97F4CC11C4EA7A1FA4B516A5D97](http://m.kugou.com/app/i/getSongInfo.php?cmd=playInfo&hash=CB7EE97F4CC11C4EA7A1FA4B516A5D97)

__返回数据__

	{
	    "fileHead": 100,
	    "q": 0,
	    "extra": {
	        "320filesize": 7998693,
	        "sqfilesize": 23222557,
	        "sqhash": "CAC59E48D58853BF40BB6158F2F5B0C5",
	        "128hash": "CB7EE97F4CC11C4EA7A1FA4B516A5D97",
	        "320hash": "47F63F15A7C048829FA796BC7F74E62B",
	        "128filesize": 3198974
	    },
	    "fileSize": 3198974,
	    "choricSinger": "李玉刚",
	    "album_img": "http://imge.kugou.com/stdmusic/{size}/20161109/20161109171040932108.jpg",
	    "topic_remark": "",
	    "url": "http://fs.open.kugou.com/53b6fcb1bddd6a80340874b8598d919a/5b8618b7/G078/M08/18/17/jg0DAFgi6G-AKqsqADDP_nSW5F4051.mp3",
	    "time": 1535515452,
	    "trans_param": {
	        "roaming_astrict": 0,
	        "display": 16,
	        "pay_block_tpl": 1,
	        "musicpack_advance": 0
	    },
	    "albumid": 1820033,
	    "singerName": "李玉刚",
	    "topic_url": "",
	    "extName": "mp3",
	    "songName": "刚好遇见你",
	    "singerHead": "",
	    "hash": "CB7EE97F4CC11C4EA7A1FA4B516A5D97",
	    "mvhash": "",
	    "error": "",
	    "imgUrl": "http://singerimg.kugou.com/uploadpic/softhead/{size}/20140304/20140304154338526832.jpg",
	    "bitRate": 128,
	    "req_hash": "CB7EE97F4CC11C4EA7A1FA4B516A5D97",
	    "status": 1,
	    "stype": 11323,
	    "intro": "",
	    "320privilege": 10,
	    "errcode": 0,
	    "singerId": 2018,
	    "fileName": "李玉刚 - 刚好遇见你",
	    "privilege": 8,
	    "128privilege": 8,
	    "sqprivilege": 10,
	    "ctype": 1009,
	    "timeLength": 200
	}

<h2 id="song-info-lyrics">音乐详情-带歌词版本</h2>

__说明:__ 获取 音乐详情-带歌词版本

__接口地址:__ `http://www.kugou.com/yy/index.php`

__参数:__

- `hash` : 音乐列表下的 音乐id
- `album_id` ：专辑ID
- `_`：时间戳
- `r`：接口方法：play/getdata

__示例:__ [http://www.kugou.com/yy/index.php?r=play/getdata&hash=3C3D93A5615FB42486CAB22024945264&album_id=1645030&_=1497972864535](http://www.kugou.com/yy/index.php?r=play/getdata&hash=3C3D93A5615FB42486CAB22024945264&album_id=1645030&_=1497972864535)

__返回数据__

	{
	    "status": 1,
	    "err_code": 0,
	    "data": {
	        "hash": "3C3D93A5615FB42486CAB22024945264",
	        "timelength": 216000,
	        "filesize": 3449934,
	        "audio_name": "周杰伦 - 告白气球",
	        "have_album": 1,
	        "album_name": "周杰伦的床边故事",
	        "album_id": "1645030",
	        "img": "http://imge.kugou.com/stdmusic/20160623/20160623233610830051.jpg",
	        "have_mv": 1,
	        "video_id": "589001",
	        "author_name": "周杰伦",
	        "song_name": "告白气球",
	        "lyrics": "[00:00.17]周杰伦 - 告白气球\r\n[00:01.69]作词：方文山\r\n[00:02.86]作曲：周杰伦\r\n[00:23.60]塞纳河畔 左岸的咖啡\r\n[00:26.35]我手一杯 品尝你的美\r\n[00:29.52]留下唇印的嘴\r\n[00:34.30]花店玫瑰 名字写错谁\r\n[00:36.94]告白气球 风吹到对街\r\n[00:40.11]微笑在天上飞\r\n[00:44.11]你说你有点难追 想让我知难而退\r\n[00:49.28]礼物不需挑最贵 只要香榭的落叶\r\n[00:54.81]喔 营造浪漫的约会\r\n[00:57.28]不害怕搞砸一切\r\n[00:59.86]拥有你就拥有 全世界\r\n[01:05.13]亲爱的 爱上你 从那天起\r\n[01:11.17]甜蜜的很轻易\r\n[01:15.84]亲爱的 别任性 你的眼睛\r\n[01:22.02]在说我愿意\r\n[01:49.00]塞纳河畔 左岸的咖啡\r\n[01:51.59]我手一杯 品尝你的美\r\n[01:54.76]留下唇印的嘴\r\n[01:59.65]花店玫瑰 名字写错谁\r\n[02:02.38]告白气球 风吹到对街\r\n[02:05.43]微笑在天上飞\r\n[02:09.54]你说你有点难追\r\n[02:11.87]想让我知难而退\r\n[02:14.55]礼物不需挑最贵\r\n[02:17.52]只要香榭的落叶\r\n[02:19.82]喔 营造浪漫的约会\r\n[02:22.61]不害怕搞砸一切\r\n[02:25.25]拥有你就拥有 全世界\r\n[02:30.13]亲爱的 爱上你 从那天起\r\n[02:36.53]甜蜜的很轻易\r\n[02:40.83]亲爱的 别任性 你的眼睛\r\n[02:47.32]在说我愿意\r\n[02:51.57]亲爱的 爱上你 恋爱日记\r\n[02:57.95]飘香水的回忆\r\n[03:02.26]一整瓶 的梦境 全都有你\r\n[03:08.70]搅拌在一起\r\n[03:12.99]亲爱的别任性 你的眼睛\r\n[03:21.25]在说我愿意\r\n",
	        "author_id": "3520",
	        "privilege": 8,
	        "privilege2": "1000",
	        "play_url": "http://fs.w.kugou.com/201808291001/bb7de636fdf7b47e7a35a5ccf01f2518/G059/M02/17/1D/ew0DAFdr9KmAf5GnADSkTnjFCm0437.mp3",
	        "authors": [
	            {
	                "is_publish": "1",
	                "author_id": "3520",
	                "avatar": "20180515002522714.jpg",
	                "author_name": "周杰伦"
	            }
	        ],
	        "bitrate": 128
	    }
	}


<h2 id="hot-keywords">热门搜索列表</h2>

__说明:__ 获取 热门搜索列表

__接口地址:__ `http://mobilecdn.kugou.com/api/v3/search/hot`

__必选参数:__

- `plat` : 偏移量
- `count` : 热门搜索关键字返回条数
- `format` : 返回数据格式，json

__接口地址:__ [http://mobilecdn.kugou.com/api/v3/search/hot?format=json&plat=0&count=30](http://mobilecdn.kugou.com/api/v3/search/hot?format=json&plat=0&count=30)

__返回数据__

	{
	    "status": 1,
	    "error": "",
	    "data": {
	        "timestamp": 1535503094,
	        "info": [
	            {
	                "sort": 1,
	                "keyword": "独家首发",
	                "jumpurl": "http://m.www2.kugou.com/yueku/category/html/index.html?areaid=30"
	            },
	            {
	                "sort": 2,
	                "keyword": "影视原声",
	                "jumpurl": "http://m.www2.kugou.com/yueku/category/html/index.html?areaid=11"
	            },
	            {
	                "sort": 3,
	                "keyword": "中国好声音",
	                "jumpurl": ""
	            },
	            {
	                "sort": 4,
	                "keyword": "幻乐之城",
	                "jumpurl": ""
	            },
	            {
	                "sort": 5,
	                "keyword": "ACG",
	                "jumpurl": "http://m.www2.kugou.com/yueku/category/html/index.html?areaid=3"
	            },
	            {
	                "sort": 6,
	                "keyword": "儿歌大全",
	                "jumpurl": "http://m.www2.kugou.com/yueku/category/html/index.html?areaid=2&searchPosition=1&searchKey=%e5%84%bf%e6%ad%8c%e5%a4%a7%e5%85%a8"
	            },
	            {
	                "sort": 7,
	                "keyword": "古风好歌",
	                "jumpurl": "http://m.www2.kugou.com/yueku/category/html/index.html?areaid=5"
	            },
	            {
	                "sort": 8,
	                "keyword": "洗脑电音",
	                "jumpurl": "http://m.www2.kugou.com/yueku/category/html/index.html?areaid=25"
	            }
	        ]
	    },
	    "errcode": 0
	}

<h2 id="songs-search-v2">搜索歌曲v2</h2>

__接口地址:__ `http://songsearch.kugou.com/song_search_v2`

__参数：__

- `callback`：回调，可以为空
- `keyword`：搜索关键词，可以为歌手名或歌曲名
- `page`：页码
- `pagesize`：每页返回数据条数
- `clientver`：
- `platform`：来源，WebFilter
- `filter`：
- `tag`：
- `userid`：
- `privilege_filter`：
- `iscorrection`：


__示例：__

[http://songsearch.kugou.com/song_search_v2?callback=jQuery19107655316341116605_1497970603262&keyword=周杰伦&page=1&pagesize=1&userid=-1&clientver=&platform=WebFilter&tag=em&filter=2&iscorrection=1&privilege_filter=0](http://songsearch.kugou.com/song_search_v2?callback=jQuery19107655316341116605_1497970603262&keyword=周杰伦&page=1&pagesize=1&userid=-1&clientver=&platform=WebFilter&tag=em&filter=2&iscorrection=1&privilege_filter=0)


__返回示例：__

	{
	    "status": 1,
	    "error_code": 0,
	    "data": {
	        "page": 1,
	        "tab": "全部",
	        "lists": [
	            {
	                "SongName": "告白气球",
	                "OwnerCount": 137384,
	                "MvType": 2,
	                "TopicRemark": "",
	                "SQFailProcess": 4,
	                "Source": "",
	                "Bitrate": 128,
	                "HQExtName": "mp3",
	                "SQFileSize": 25058814,
	                "ResFileSize": 43915053,
	                "Duration": 215,
	                "MvTrac": 3,
	                "SQDuration": 215,
	                "ExtName": "mp3",
	                "Auxiliary": "",
	                "SongLabel": "",
	                "Scid": 22084042,
	                "OriSongName": "告白气球",
	                "FailProcess": 4,
	                "SQBitrate": 931,
	                "HQBitrate": 320,
	                "Audioid": 22084042,
	                "HiFiQuality": 3,
	                "Grp": {},
	                "OriOtherName": "",
	                "AlbumPrivilege": 8,
	                "TopicUrl": "",
	                "SuperFileHash": "",
	                "ASQPrivilege": 10,
	                "M4aSize": 880014,
	                "AlbumName": "周杰伦的床边故事",
	                "IsOriginal": 0,
	                "Privilege": 8,
	                "ResBitrate": 1632,
	                "FileHash": "5FCE4CBCB96D6025033BCE2025FC3943",
	                "SQPayType": 3,
	                "HQPrice": 200,
	                "Type": "audio",
	                "trans_param": {
	                    "roaming_astrict": 0,
	                    "display": 0,
	                    "pay_block_tpl": 1,
	                    "musicpack_advance": 0
	                },
	                "SourceID": 0,
	                "FoldType": 0,
	                "SingerId": [
	                    3520
	                ],
	                "A320Privilege": 10,
	                "ID": "39612569",
	                "SuperFileSize": 0,
	                "SQPrivilege": 10,
	                "SQFileHash": "B2C0A23919EEE8B47831FFAA2604107F",
	                "AlbumID": "1645030",
	                "HQPrivilege": 10,
	                "SuperBitrate": 0,
	                "SuperDuration": 0,
	                "MixSongID": "39612569",
	                "ResFileHash": "05CCCE134338BD3B2AAB176218FCB0F9",
	                "FileSize": 3443771,
	                "SuperExtName": "",
	                "HQFileHash": "2398DDFC7C7420AB22A77DFEAE4CA551",
	                "HQPkgPrice": 1,
	                "AudioCdn": 100,
	                "FileName": "<em>周杰伦</em> - 告白气球",
	                "OtherName": "",
	                "mvTotal": 3,
	                "PkgPrice": 1,
	                "HQFileSize": 8608960,
	                "HQFailProcess": 4,
	                "Publish": 1,
	                "QualityLevel": 3,
	                "SQPrice": 200,
	                "ResDuration": 215,
	                "PublishAge": 255,
	                "Price": 200,
	                "HQPayType": 3,
	                "SingerName": "<em>周杰伦</em>",
	                "SQExtName": "flac",
	                "MvHash": "AFF3B6219C15D030F957B82FF50AA91E",
	                "SQPkgPrice": 1,
	                "HQDuration": 215,
	                "PayType": 3,
	                "HasAlbum": 1,
	                "Accompany": 1,
	                "OldCpy": 0
	            }
	        ],
	        "chinesecount": 3,
	        "searchfull": 1,
	        "correctiontype": 0,
	        "subjecttype": 0,
	        "aggregation": [
	            {
	                "key": "DJ",
	                "count": 0
	            },
	            {
	                "key": "现场",
	                "count": 0
	            },
	            {
	                "key": "广场舞",
	                "count": 0
	            },
	            {
	                "key": "伴奏",
	                "count": 0
	            },
	            {
	                "key": "铃声",
	                "count": 0
	            }
	        ],
	        "allowerr": 0,
	        "correctionsubject": "",
	        "correctionforce": 0,
	        "total": 420,
	        "istagresult": 0,
	        "istag": 0,
	        "correctiontip": "",
	        "pagesize": 1
	    }
	}


<h2 id="songs-search-v3">搜索歌曲v3</h2>

__说明:__ 获取 音乐搜索结果

__接口地址:__ `http://mobilecdn.kugou.com/api/v3/search/song`

__参数:__

- `keyword`：关键字
- `format`：返回数据格式，json
- `showtype`：
- `page`：页码
- `pagesize`：每页条数

__示例:__ [http://mobilecdn.kugou.com/api/v3/search/song?format=json&keyword=周杰伦&page=1&pagesize=2&showtype=1](http://mobilecdn.kugou.com/api/v3/search/song?format=json&keyword=周杰伦&page=1&pagesize=2&showtype=1)

__返回数据__

	{
	    "status": 1,
	    "error": "",
	    "data": {
	        "aggregation": [
	            {
	                "key": "DJ",
	                "count": 0
	            },
	            {
	                "key": "现场",
	                "count": 0
	            },
	            {
	                "key": "广场舞",
	                "count": 0
	            },
	            {
	                "key": "伴奏",
	                "count": 0
	            },
	            {
	                "key": "铃声",
	                "count": 0
	            }
	        ],
	        "tab": "全部",
	        "info": [
	            {
	                "othername_original": "KTV版伴奏",
	                "pay_type_320": 0,
	                "m4afilesize": 977808,
	                "price_sq": 0,
	                "isoriginal": 0,
	                "filesize": 3807652,
	                "source": "",
	                "bitrate": 128,
	                "topic": "",
	                "trans_param": {
	                    "roaming_astrict": 0,
	                    "display": 0,
	                    "pay_block_tpl": 1,
	                    "musicpack_advance": 0
	                },
	                "price": 0,
	                "Accompany": 1,
	                "old_cpy": 1,
	                "songname_original": "青花瓷",
	                "singername": "周杰伦",
	                "pay_type": 0,
	                "sourceid": 0,
	                "topic_url": "",
	                "fail_process_320": 0,
	                "pkg_price": 0,
	                "feetype": 0,
	                "filename": "周杰伦 - 青花瓷 (KTV版伴奏)",
	                "price_320": 0,
	                "songname": "青花瓷 (KTV版伴奏)",
	                "group": [
	                    {
	                        "othername_original": "原版伴奏",
	                        "pay_type_320": 0,
	                        "m4afilesize": 1010779,
	                        "price_sq": 0,
	                        "isoriginal": 0,
	                        "filesize": 3848575,
	                        "source": "",
	                        "bitrate": 128,
	                        "topic": "",
	                        "trans_param": {
	                            "roaming_astrict": 0,
	                            "display": 0,
	                            "pay_block_tpl": 1,
	                            "musicpack_advance": 0
	                        },
	                        "price": 0,
	                        "Accompany": 1,
	                        "old_cpy": 1,
	                        "songname_original": "青花瓷",
	                        "singername": "周杰伦",
	                        "pay_type": 0,
	                        "sourceid": 0,
	                        "topic_url": "",
	                        "fail_process_320": 0,
	                        "pkg_price": 0,
	                        "feetype": 0,
	                        "filename": "周杰伦 - 青花瓷 (原版伴奏)",
	                        "price_320": 0,
	                        "songname": "青花瓷 (原版伴奏)",
	                        "hash": "abab5600ac1481fc88d6925a18f496bf",
	                        "mvhash": "",
	                        "rp_type": "audio",
	                        "privilege": 0,
	                        "album_audio_id": 41301045,
	                        "rp_publish": 1,
	                        "album_id": "",
	                        "ownercount": 30,
	                        "fold_type": 0,
	                        "audio_id": 2559735,
	                        "pkg_price_sq": 0,
	                        "320filesize": 9567216,
	                        "isnew": 0,
	                        "duration": 240,
	                        "pkg_price_320": 0,
	                        "srctype": 1,
	                        "fail_process_sq": 0,
	                        "sqfilesize": 0,
	                        "fail_process": 0,
	                        "320hash": "e0d456732dace9dabb7bf3f7c5d95b70",
	                        "extname": "mp3",
	                        "sqhash": "",
	                        "pay_type_sq": 0,
	                        "320privilege": 0,
	                        "sqprivilege": 0,
	                        "album_name": "",
	                        "othername": ""
	                    }
	                ],
	                "hash": "56948d774766503d04010db54594f150",
	                "mvhash": "",
	                "rp_type": "audio",
	                "privilege": 0,
	                "album_audio_id": 40478713,
	                "rp_publish": 1,
	                "album_id": "",
	                "ownercount": 1590,
	                "fold_type": 1,
	                "audio_id": 339830,
	                "pkg_price_sq": 0,
	                "320filesize": 9519126,
	                "isnew": 0,
	                "duration": 238,
	                "pkg_price_320": 0,
	                "srctype": 1,
	                "fail_process_sq": 0,
	                "sqfilesize": 0,
	                "fail_process": 0,
	                "320hash": "50b628a8a469134bc714bfa0a73b9b8c",
	                "extname": "mp3",
	                "sqhash": "",
	                "pay_type_sq": 0,
	                "320privilege": 0,
	                "sqprivilege": 0,
	                "album_name": "",
	                "othername": ""
	            },
	            {
	                "othername_original": "CCTV音乐频道",
	                "pay_type_320": 0,
	                "m4afilesize": 962911,
	                "price_sq": 0,
	                "isoriginal": 0,
	                "filesize": 3753641,
	                "source": "",
	                "bitrate": 128,
	                "topic": "",
	                "trans_param": {
	                    "roaming_astrict": 0,
	                    "pay_block_tpl": 1,
	                    "display": 0,
	                    "musicpack_advance": 0
	                },
	                "price": 0,
	                "Accompany": 1,
	                "old_cpy": 1,
	                "songname_original": "爱我别走",
	                "singername": "周杰伦",
	                "pay_type": 0,
	                "sourceid": 0,
	                "topic_url": "",
	                "fail_process_320": 0,
	                "pkg_price": 0,
	                "feetype": 0,
	                "filename": "周杰伦 - 爱我别走 (CCTV音乐频道)",
	                "price_320": 0,
	                "songname": "爱我别走 (CCTV音乐频道)",
	                "group": [],
	                "hash": "b566b53077a02f24fc9980912fb3eeca",
	                "mvhash": "af246fd620a697580b7cd164235fad5f",
	                "rp_type": "audio",
	                "privilege": 0,
	                "album_audio_id": 38167864,
	                "rp_publish": 1,
	                "album_id": "939265",
	                "ownercount": 1446,
	                "fold_type": 0,
	                "audio_id": 333062,
	                "pkg_price_sq": 0,
	                "320filesize": 9382298,
	                "isnew": 0,
	                "duration": 234,
	                "pkg_price_320": 0,
	                "srctype": 1,
	                "fail_process_sq": 0,
	                "sqfilesize": 28226534,
	                "fail_process": 0,
	                "320hash": "d88dd2280c0010ccab95fe00ddc7ef5b",
	                "extname": "mp3",
	                "sqhash": "67ed35cca054679f3f3138b14538ddfe",
	                "pay_type_sq": 0,
	                "320privilege": 0,
	                "sqprivilege": 0,
	                "album_name": "精彩音乐汇",
	                "othername": ""
	            }
	        ],
	        "correctiontype": 0,
	        "timestamp": 1535514140,
	        "allowerr": 0,
	        "total": 365,
	        "istag": 0,
	        "istagresult": 0,
	        "forcecorrection": 0,
	        "correctiontip": ""
	    },
	    "errcode": 0
	}

<h2 id="mv-search">mv搜索</h2>

__说明:__ 获取mv搜索列表

__接口地址:__ `http://mvsearch.kugou.com/mv_search`

__必选参数:__

- `keyword`：搜索关键字
- `_`:时间戳
- `page`：页码
- `pagesize`：返回每页条数
- `userid`：
- `clientver`：
- `platform`：来源，WebFilter
- `tag`：
- `filter`：
- `iscorrection`：
- `privilege_filter`：

__接口地址:__ [http://mvsearch.kugou.com/mv_search?keyword=海阔天空&page=1&pagesize=30&userid=-1&clientver=&platform=WebFilter&tag=em&filter=2&iscorrection=1&privilege_filter=0&_=1515052279917](http://mvsearch.kugou.com/mv_search?keyword=海阔天空&page=1&pagesize=30&userid=-1&clientver=&platform=WebFilter&tag=em&filter=2&iscorrection=1&privilege_filter=0&_=1515052279917)

__返回数据__

	{
	    "status": 1,
	    "error_code": 0,
	    "data": {
	        "page": 1,
	        "correctionforce": 0,
	        "total": 154,
	        "lists": [
	            {
	                "MixSongID": "",
	                "MvType": 2,
	                "Privilege": 8,
	                "IsOfficial": 1,
	                "Bitrate": 128,
	                "FileHash": "090CF9A7E9A49C8FCF24AE81AABC2201",
	                "AudioCdn": 100,
	                "MvTrac": 3,
	                "Pic": "20160630122006780783.jpg",
	                "ExtName": "mp3",
	                "Auxiliary": "",
	                "Username": "",
	                "OstAuxiliary": "",
	                "MvName": "<em>海阔天空</em>",
	                "MvID": 114443,
	                "IsNew": 0,
	                "FileSize": 5152404,
	                "Scid": 3261014,
	                "Description": "",
	                "HistoryHeat": 14661451,
	                "Isshort": 0,
	                "PublishDate": "",
	                "Remark": "",
	                "MvHashMark": "高清",
	                "SingerName": "BEYOND",
	                "AudioID": "3261014",
	                "MvHash": "4135FC477494AA522A85B515410C101A",
	                "FileName": "BEYOND - <em>海阔天空</em>",
	                "Duration": 317,
	                "PublishAge": 255,
	                "AlbumID": "",
	                "Userid": 0,
	                "MvHot": 17976
	            },
	            {
	                "MixSongID": "",
	                "MvType": 2,
	                "Privilege": 5,
	                "IsOfficial": 0,
	                "Bitrate": 128,
	                "FileHash": "470290D8CD00C737F37E5EDC40F3E7E7",
	                "AudioCdn": 100,
	                "MvTrac": 3,
	                "Pic": "20160512100521329045.jpg",
	                "ExtName": "mp3",
	                "Auxiliary": "",
	                "Username": "",
	                "OstAuxiliary": "",
	                "MvName": "<em>海阔天空</em>",
	                "MvID": 189864,
	                "IsNew": 0,
	                "FileSize": 3474203,
	                "Scid": 16532271,
	                "Description": "高音震撼低音婉转",
	                "HistoryHeat": 2053491,
	                "Isshort": 0,
	                "PublishDate": "",
	                "Remark": "2015中国新声代第三季第五期现场",
	                "MvHashMark": "超清",
	                "SingerName": "汤晶锦",
	                "AudioID": "16532271",
	                "MvHash": "D15C17D5ED5C0C284F3AB1F30B8B9438",
	                "FileName": "汤晶锦 - <em>海阔天空</em> - 2015中国新声代第三季第五期现场",
	                "Duration": 209,
	                "PublishAge": 255,
	                "AlbumID": "",
	                "Userid": 0,
	                "MvHot": 1575
	            },
	            {
	                "MixSongID": "",
	                "MvType": 1,
	                "Privilege": 8,
	                "IsOfficial": 0,
	                "Bitrate": 128,
	                "FileHash": "15386BF487FDAF728EA88535CC5329E5",
	                "AudioCdn": 100,
	                "MvTrac": 0,
	                "Pic": "20160426232659789774.jpg",
	                "ExtName": "mp3",
	                "Auxiliary": "",
	                "Username": "",
	                "OstAuxiliary": "",
	                "MvName": "<em>海阔天空</em>",
	                "MvID": 343,
	                "IsNew": 0,
	                "FileSize": 4433700,
	                "Scid": 325829,
	                "Description": "",
	                "HistoryHeat": 1439608,
	                "Isshort": 0,
	                "PublishDate": "",
	                "Remark": "",
	                "MvHashMark": "标清",
	                "SingerName": "信乐团",
	                "AudioID": "325829",
	                "MvHash": "AB1ED5873697C720F2668E7A56DC1229",
	                "FileName": "信乐团 - <em>海阔天空</em>",
	                "Duration": 336,
	                "PublishAge": 255,
	                "AlbumID": "",
	                "Userid": 0,
	                "MvHot": 1683
	            }
	        ],
	        "correctiontype": 0,
	        "correctiontip": "",
	        "pagesize": 3
	    }
	}


<h2 id="mv-info">mv详情</h2>

__说明:__ 获取mv详情、包括MP4文件

__接口地址:__`http://m.kugou.com/app/i/mv.php`

__必选参数:__

- `hash`：mvhsah
- `ismp3`:
- `ext`:
- `cmd`:

__示例：__[http://m.kugou.com/app/i/mv.php?cmd=100&hash=5F8393A55D5762A63F1A5E92B46E575E&ismp3=1&ext=mp4](http://m.kugou.com/app/i/mv.php?cmd=100&hash=5F8393A55D5762A63F1A5E92B46E575E&ismp3=1&ext=mp4)

__返回数据__

	{
	    "timelength": 260440,
	    "play_count": 4751649,
	    "songname": "等你等到我心痛",
	    "id": 125,
	    "status": 1,
	    "remark": "",
	    "singer": "张学友",
	    "track": 0,
	    "error": "",
	    "mp3data": {
	        "hash": "30eec2ec657ba8504a151401d8da7da4",
	        "filesize": 4058374,
	        "timelength": 253,
	        "bitrate": 128
	    },
	    "hash": "2460E490609D31DC58B8DF8E70C7B537",
	    "mvicon": "http://imge.kugou.com/mvhdpic/{size}/20160426/20160426190516322192.jpg",
	    "type": 1,
	    "is_publish": 1,
	    "mvdata": {
	        "sq": {},
	        "le": {
	            "downurl": "http://fs.mv.web.kugou.com/201808291040/798b0e9540784fb86fd726aa7decbe1d/G088/M00/0D/11/OJQEAFi9BjeAXTX4ARZ69LH5V1g680.mp4",
	            "bitrate": 560674,
	            "backupdownurl": [
	                "http://fs.mv.web2.kugou.com/201808291040/54c79bc3af4e30b169c36704534b6683/G088/M00/0D/11/OJQEAFi9BjeAXTX4ARZ69LH5V1g680.mp4"
	            ],
	            "hash": "2460e490609d31dc58b8df8e70c7b537",
	            "timelength": 260440,
	            "filesize": 18250484
	        },
	        "rq": {}
	    },
	    "errcode": 0
	}


