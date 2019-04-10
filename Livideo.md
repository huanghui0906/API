# 梨视频 #
- [首页](#home)
	- [列表获取](#list_get)
	- [头条](#head)
	- [其它标签](#other_tag)
		- [详细内容](#details)

ps:后续请求中，有的需要请求头，有的不需要请求头，建议大家都加上，请求头数据如下——

请求头：

| 请求头        | 值           |
| ------------- |:-------------:|
|  X-Channel-Code    | 固定值 `official`，可为空 |
|  X-Client-Agent    | 手机品牌，例如 Xiaomi，可为空 |
|   X-Client-Hash   | 长度为32的小写字母和数字混合字符串，例`2f3d6ffkda95dlz2fhju8d3s6dfges3t`，可为空 |
|   X-Client-ID   | 长度为的15数字字符串，例`123456789123456`，可为空 |
|   X-Client-Version   | 为空即可 |
|   X-Long-Token   | 为空即可 |
|   X-Platform-Type   | 为空即可 |
|   X-Platform-Version   | 为空即可 |
|  X-Serial-Num    | 当前时间 Unix 时间戳 |
|   X-User-ID   | 为空即可 |

请求头示例：

	X-Channel-Code:official
	X-Client-Agent:Xiaomi
	X-Client-Hash:2f3d6ffkda95dlz2fhju8d3s6dfges3t
	X-Client-ID:123456789123456
	X-Client-Version:2.3.2
	X-Long-Token:
	X-Platform-Type:0
	X-Platform-Version:5.0
	X-Serial-Num:1492140134
	X-User-ID:

<h2 id="home">首页</h2>

<h3 id="list_get">列表获取</h3>

url：[`http://app.pearvideo.com/clt/jsp/v2/getCategorys.jsp`](http://app.pearvideo.com/clt/jsp/v2/getCategorys.jsp)

请求方式：GET

json 示例：

	{
      "resultCode": "1",
      "resultMsg": "success",
      "reqId": "20228065-eef4-4a54-8426-31b663482cb0",
      "systemTime": "1492218570221",
      "categoryList": [
        {
          "categoryId": "4",
          "name": "娱乐",
          "color": "#E966AE"
        },
        {
          "categoryId": "1",
          "name": "社会",
          "color": "#F04A50"
        },
        {
          "categoryId": "6",
          "name": "美食",
          "color": "#F58D4E"
        },
        {
          "categoryId": "7",
          "name": "搞笑",
          "color": "#B869AD"
        },
        {
          "categoryId": "2",
          "name": "世界",
          "color": "#33B7A7"
        },
        {
          "categoryId": "8",
          "name": "科技",
          "color": "#33A7D8"
        },
        {
          "categoryId": "9",
          "name": "体育",
          "color": "#FECE3E"
        },
        {
          "categoryId": "3",
          "name": "财富",
          "color": "#3276B5"
        },
        {
          "categoryId": "10",
          "name": "新知",
          "color": "#A2B0A0"
        },
        {
          "categoryId": "5",
          "name": "生活",
          "color": "#8CD931"
        }
      ]
    }

json 解析：

- `resultCode`：为`1`时表请求成功
- `name`：标签名
- `categoryId`：标签 id，用作[其它标签](#other_tag)中

<h3 id="head">头条</h3>

url：[`http://app.pearvideo.com/clt/jsp/v2/home.jsp?lastLikeIds=1063871%2C1063985%2C1064069%2C1064123%2C1064078%2C1064186%2C1062372%2C1064164%2C1064081%2C1064176%2C1064070%2C1064019`](http://app.pearvideo.com/clt/jsp/v2/home.jsp?lastLikeIds=1063871%2C1063985%2C1064069%2C1064123%2C1064078%2C1064186%2C1062372%2C1064164%2C1064081%2C1064176%2C1064070%2C1064019)

请求方式：GET

json 示例：

	{
      "resultCode": "1",
      "resultMsg": "success",
      "reqId": "b79c9436-4d59-4452-a7ad-20836d15b8ab",
      "systemTime": "1492218827264",
      "areaList": [
        {
          "area_id": "100001",
          "expInfo": {
            "algorighm_exp_id": "",
            "front_exp_id": "0",
            "s_value": "b79c9436-4d59-4452-a7ad-20836d15b8ab_2153673381279278"
          }
        },
        {
          "area_id": "100006",
          "expInfo": {
            "algorighm_exp_id": "1000",
            "front_exp_id": "0",
            "s_value": "b79c9436-4d59-4452-a7ad-20836d15b8ab_2153673398586355"
          }
        },
        {
          "area_id": "100007",
          "expInfo": {
            "algorighm_exp_id": "1000",
            "front_exp_id": "0",
            "s_value": "b79c9436-4d59-4452-a7ad-20836d15b8ab_2153673398586355"
          }
        },
        {
          "area_id": "100008",
          "expInfo": {
            "algorighm_exp_id": "1000",
            "front_exp_id": "0",
            "s_value": "b79c9436-4d59-4452-a7ad-20836d15b8ab_2153673398586355"
          }
        },
        {
          "area_id": "100011",
          "expInfo": {
            "algorighm_exp_id": "",
            "front_exp_id": "0",
            "s_value": "70ab571b-47ed-498b-92df-730064445b97_2152771001328326"
          }
        },
        {
          "area_id": "100012",
          "expInfo": {
            "algorighm_exp_id": "",
            "front_exp_id": "0",
            "s_value": "70ab571b-47ed-498b-92df-730064445b97_2152771001328326"
          }
        },
        {
          "area_id": "100013",
          "expInfo": {
            "algorighm_exp_id": "",
            "front_exp_id": "0",
            "s_value": "12907b85-0605-4290-bb91-9d7a721d0895_2153655394105802"
          }
        },
        {
          "area_id": "100014",
          "expInfo": {
            "algorighm_exp_id": "",
            "front_exp_id": "0",
            "s_value": "12907b85-0605-4290-bb91-9d7a721d0895_2153655394105802"
          }
        },
        {
          "area_id": "100023",
          "expInfo": {
            "algorighm_exp_id": "",
            "front_exp_id": "0",
            "s_value": "bb9ae641-4ba5-4324-8dc4-a28691d2948f_2124643064523555"
          }
        }
      ],
      "dataList": [
        {
          "nodeType": "1",
          "nodeName": "头条",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "",
          "contList": [
            {
              "contId": "1064396",
              "name": "周末推片：速8与西游的王牌之战！",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064396-10256904.jpg",
              "nodeInfo": {
                "nodeId": "18",
                "name": "文娱小队长",
                "logoImg": "http://image1.pearvideo.com/node/18-10027897-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'03\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "228",
              "adExpMonitorUrl": "",
              "coverVideo": "http://video.pearvideo.com/head/20170414/cont-1064396-10371532.mp4"
            },
            {
              "contId": "1064563",
              "name": "当轮滑遇上中国风，小姐姐完美演绎",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064563-10257243.jpg",
              "nodeInfo": {
                "nodeId": "25",
                "name": "一手Video",
                "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'13\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "351",
              "adExpMonitorUrl": "",
              "coverVideo": "http://video.pearvideo.com/head/20170414/cont-1064563-10372062.mp4"
            },
            {
              "contId": "1064519",
              "name": "《人民的名义》中他们都是健身达人",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064519-10257416.jpg",
              "nodeInfo": {
                "nodeId": "174",
                "name": "看球",
                "logoImg": "http://image.pearvideo.com/node/174-10065489-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'20\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "191",
              "adExpMonitorUrl": "",
              "coverVideo": "http://video.pearvideo.com/head/20170414/cont-1064519-10372273.mp4"
            },
            {
              "contId": "1064434",
              "name": "来看！朝鲜国宝杂技团表演空中飞人",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064434-10257006.jpg",
              "nodeInfo": {
                "nodeId": "22",
                "name": "DIGGER",
                "logoImg": "http://image.pearvideo.com/node/22-10027893-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'22\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "237",
              "adExpMonitorUrl": "",
              "coverVideo": "http://video.pearvideo.com/head/20170414/cont-1064434-10371684.mp4"
            },
            {
              "contId": "1063755",
              "name": "宋小宝春晚灵感，来自撸串吃饺子",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1063755-10256684.jpg",
              "nodeInfo": {
                "nodeId": "25",
                "name": "一手Video",
                "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'10\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "2309",
              "adExpMonitorUrl": "",
              "coverVideo": "http://video.pearvideo.com/head/20170414/cont-1063755-10371239.mp4"
            }
          ]
        },
        {
          "nodeType": "7",
          "nodeName": "为你推荐",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "",
          "contList": [
            {
              "contId": "1063985",
              "name": "大佬说：匠心是个什么玩意儿？",
              "pic": "http://image.pearvideo.com/cont/20170413/cont-1063985-10254756.jpg",
              "nodeInfo": {
                "nodeId": "140",
                "name": "品牌",
                "logoImg": "http://image.pearvideo.com/node/140-10050957-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'50\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "11089",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064124",
              "name": "给“公车私用”的民警点赞",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064124-10255297.jpg",
              "nodeInfo": {
                "nodeId": "169",
                "name": "长安剑",
                "logoImg": "http://image1.pearvideo.com/node/169-10059817-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'17\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "43",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1060644",
              "name": "宅男，你的女朋友是这样造出来的！",
              "pic": "http://image1.pearvideo.com/cont/20170407/cont-1060644-10240906.png",
              "nodeInfo": {
                "nodeId": "13",
                "name": "风声视频",
                "logoImg": "http://image1.pearvideo.com/node/13-10027906-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "03'16\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "24947",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1063022",
              "name": "这名2.6米高的长腿美女从不出门？",
              "pic": "http://image2.pearvideo.com/cont/20170412/cont-1063022-10250792.png",
              "nodeInfo": {
                "nodeId": "10",
                "name": "时差视频",
                "logoImg": "http://image1.pearvideo.com/node/10-10027909-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'10\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "228",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064362",
              "name": "他能让你任打一分钟，绝对不还手",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064362-10256374.png",
              "nodeInfo": {
                "nodeId": "605",
                "name": "街力",
                "logoImg": "http://image1.pearvideo.com/node/605-10160149-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "04'53\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "13",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064578",
              "name": "在朝鲜乘坐世界最深地铁是什么体验",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064578-10257069.png",
              "nodeInfo": {
                "nodeId": "22",
                "name": "DIGGER",
                "logoImg": "http://image.pearvideo.com/node/22-10027893-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'22\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "104",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1063793",
              "name": "美女胸模月入五万：我不是坏女孩",
              "pic": "http://image1.pearvideo.com/cont/20170413/cont-1063793-10253989.jpg",
              "nodeInfo": {
                "nodeId": "27",
                "name": "灰度视频",
                "logoImg": "http://image.pearvideo.com/node/27-10027887-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'28\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "2831",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064146",
              "name": "她收养40流浪猫:让它们有尊严活着",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064146-10255376.png",
              "nodeInfo": {
                "nodeId": "25",
                "name": "一手Video",
                "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'57\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "416",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064373",
              "name": "白人男子辱骂\"中国人渣\",乘客怒了",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064373-10256306.jpg",
              "nodeInfo": {
                "nodeId": "10",
                "name": "时差视频",
                "logoImg": "http://image1.pearvideo.com/node/10-10027909-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'04\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "36",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064350",
              "name": "厨余垃圾还可以用来保护环境？",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064350-10256210.jpg",
              "nodeInfo": {
                "nodeId": "838",
                "name": "新武夷",
                "logoImg": "http://image2.pearvideo.com/node/838-10210901-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'06\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "10",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1040476",
              "name": "美联航受害者：门牙打落，精神受创",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1040476-10255020.JPG",
              "nodeInfo": {
                "nodeId": "24",
                "name": "ING现场",
                "logoImg": "http://image1.pearvideo.com/node/24-10027891-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'15\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "322",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064676",
              "name": "洪金宝大谈赵文卓",
              "pic": "http://image2.pearvideo.com/cont/20170415/cont-1064676-10257620.png",
              "nodeInfo": {
                "nodeId": "710",
                "name": "饭爱豆娱乐",
                "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'47\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "3",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "11",
          "nodeName": "硬广告",
          "moreId": "14"
        },
        {
          "nodeType": "12",
          "nodeName": "全民拍客活动",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "",
          "activityList": [
            {
              "activityId": "12",
              "name": "晒出身边神奇的孩子",
              "runStatus": "0",
              "backgroundImg": "http://imageugc2.pearvideo.com/activity/20170413/12-bg-161653.png",
              "beginTime": "2017.4.14",
              "endTime": "2017.4.24"
            },
            {
              "activityId": "10",
              "name": "以读攻读！朗读集赞换大奖",
              "runStatus": "1",
              "backgroundImg": "http://imageugc1.pearvideo.com/activity/20170331/10-bg-165708.png",
              "beginTime": "2017.4.5",
              "endTime": "2017.4.14"
            }
          ]
        },
        {
          "nodeType": "10",
          "nodeName": "最新视频",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "",
          "contList": [
            {
              "contId": "1064685",
              "name": "村民枕古墓睡一辈子，拆迁时才发现",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064685-10257582.png",
              "nodeInfo": {
                "nodeId": "25",
                "name": "一手Video",
                "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'40\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "0",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064350",
              "name": "厨余垃圾还可以用来保护环境？",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064350-10256210.jpg",
              "nodeInfo": {
                "nodeId": "838",
                "name": "新武夷",
                "logoImg": "http://image2.pearvideo.com/node/838-10210901-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'06\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "10",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064681",
              "name": "杨幂对拿奖保持平常心称努力过就好",
              "pic": "http://image2.pearvideo.com/cont/20170415/cont-1064681-10257632.jpg",
              "nodeInfo": {
                "nodeId": "710",
                "name": "饭爱豆娱乐",
                "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'25\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "7",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064679",
              "name": "青春励志剧谭松韵首演菜鸟记者",
              "pic": "http://image1.pearvideo.com/cont/20170415/cont-1064679-10257664.png",
              "nodeInfo": {
                "nodeId": "710",
                "name": "饭爱豆娱乐",
                "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'04\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "8",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064678",
              "name": "暖男魏大勋表示会认真做自己",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064678-10257587.png",
              "nodeInfo": {
                "nodeId": "710",
                "name": "饭爱豆娱乐",
                "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'17\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "1",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "娱乐精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "4",
          "contList": [
            {
              "contId": "1064667",
              "name": "言承旭求过婚吗？林志玲答了三个字",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064667-10257503.png",
              "nodeInfo": {
                "nodeId": "66",
                "name": "水煮娱",
                "logoImg": "http://image2.pearvideo.com/node/66-10035464-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'21\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "57",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064638",
              "name": "林志玲又与富豪曝恋情？",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064638-10257353.jpg",
              "nodeInfo": {
                "nodeId": "689",
                "name": "关爱八卦成长协会",
                "logoImg": "http://image1.pearvideo.com/node/689-10173475-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'50\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "35",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064640",
              "name": "决赛前夜，张碧晨帮唱嘉宾还没来",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064640-10257371.jpg",
              "nodeInfo": {
                "nodeId": "66",
                "name": "水煮娱",
                "logoImg": "http://image2.pearvideo.com/node/66-10035464-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'08\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "21",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064673",
              "name": "baby携子亮相跑男：要向超哥学带娃",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064673-10257547.jpg",
              "nodeInfo": {
                "nodeId": "66",
                "name": "水煮娱",
                "logoImg": "http://image2.pearvideo.com/node/66-10035464-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'10\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "19",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "社会精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "1",
          "contList": [
            {
              "contId": "1064417",
              "name": "湘深山现神秘古寨,明建文帝避难处?",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064417-10256473.png",
              "nodeInfo": {
                "nodeId": "25",
                "name": "一手Video",
                "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'54\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "130",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064577",
              "name": "贵阳一修车厂着火，烧了隔壁居民楼",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064577-10257064.png",
              "nodeInfo": {
                "nodeId": "25",
                "name": "一手Video",
                "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'36\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "137",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064629",
              "name": "婆婆阳台喊救命，儿媳房内看电视",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064629-10257332.png",
              "nodeInfo": {
                "nodeId": "25",
                "name": "一手Video",
                "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'06\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "136",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064620",
              "name": "直播:纽约车展开幕,多款新车将入华",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064620-10257256.jpg",
              "nodeInfo": {
                "nodeId": "24",
                "name": "ING现场",
                "logoImg": "http://image1.pearvideo.com/node/24-10027891-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "2",
              "cornerLabelDesc": "图文直播",
              "forwordType": "2",
              "videoType": "2",
              "duration": "94'27\"",
              "liveStatus": "2",
              "liveStartTime": "",
              "praiseTimes": "8079",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "美食精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "6",
          "contList": [
            {
              "contId": "1064595",
              "name": "10分钟搞定的正宗香辣毛血旺！",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064595-10257142.jpg",
              "nodeInfo": {
                "nodeId": "846",
                "name": "好好吃",
                "logoImg": "http://image2.pearvideo.com/node/846-10217315-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'21\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "39",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064421",
              "name": "水果做圆子，甜品店门口排起了长队",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064421-10256591.jpg",
              "nodeInfo": {
                "nodeId": "58",
                "name": "太阳猫美食TV",
                "logoImg": "http://image.pearvideo.com/node/58-10167780-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'01\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "88",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064562",
              "name": "宝宝最爱吃的香炸凤尾虾来啦！",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064562-10257056.jpg",
              "nodeInfo": {
                "nodeId": "747",
                "name": "黄先生厨房",
                "logoImg": "http://image.pearvideo.com/node/747-10186023-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'58\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "30",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064590",
              "name": "坚决不向网红茶低头，动手族放大招",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064590-10257119.png",
              "nodeInfo": {
                "nodeId": "407",
                "name": "太吃",
                "logoImg": "http://image.pearvideo.com/node/407-10110597-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'10\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "48",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "搞笑精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "7",
          "contList": [
            {
              "contId": "1064565",
              "name": "朋友圈晒父母的，你们交家用了吗？",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064565-10257117.jpg",
              "nodeInfo": {
                "nodeId": "625",
                "name": "粤知一二",
                "logoImg": "http://image2.pearvideo.com/node/625-10163189-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'46\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "58",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064272",
              "name": "看完这个你还想找女朋友算我输！",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064272-10255920.png",
              "nodeInfo": {
                "nodeId": "165",
                "name": "污毒炼金术",
                "logoImg": "http://image2.pearvideo.com/node/165-10095989-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'50\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "77",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064156",
              "name": "神经男友吃霸王餐，贴心女友舍命陪",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064156-10256024.png",
              "nodeInfo": {
                "nodeId": "780",
                "name": "好好先森",
                "logoImg": "http://image.pearvideo.com/node/780-10196724-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'55\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "25",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064487",
              "name": "下课别走，小树林见！",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064487-10256795.png",
              "nodeInfo": {
                "nodeId": "767",
                "name": "我差点就信了",
                "logoImg": "http://image2.pearvideo.com/node/767-10193237-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'56\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "62",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "世界精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "2",
          "contList": [
            {
              "contId": "1064648",
              "name": "俄炸弹之父威力，四倍美国炸弹之母",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064648-10257417.png",
              "nodeInfo": {
                "nodeId": "10",
                "name": "时差视频",
                "logoImg": "http://image1.pearvideo.com/node/10-10027909-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'42\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "24",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064509",
              "name": "美国老师抛妻别子，与15岁女生私奔",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064509-10256829.jpg",
              "nodeInfo": {
                "nodeId": "10",
                "name": "时差视频",
                "logoImg": "http://image1.pearvideo.com/node/10-10027909-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'15\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "28",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064619",
              "name": "她收养900多条流浪狗，从未想放弃",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064619-10257253.png",
              "nodeInfo": {
                "nodeId": "35",
                "name": "OMG!",
                "logoImg": "http://image2.pearvideo.com/node/35-10030502-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'18\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "40",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064533",
              "name": "去女仆健身房，身体会不会越练越差",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064533-10256898.jpg",
              "nodeInfo": {
                "nodeId": "345",
                "name": " 必看视频",
                "logoImg": "http://image2.pearvideo.com/node/345-10098044-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'45\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "20",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "科技精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "8",
          "contList": [
            {
              "contId": "1064550",
              "name": "这卫星上天，高铁上网不再断断续续",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064550-10257105.png",
              "nodeInfo": {
                "nodeId": "9",
                "name": "微辣Video",
                "logoImg": "http://image2.pearvideo.com/node/9-10027910-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'37\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "108",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064644",
              "name": "小国宇宙梦：星战前夜玩家齐聚冰岛",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064644-10257487.jpg",
              "nodeInfo": {
                "nodeId": "27",
                "name": "灰度视频",
                "logoImg": "http://image.pearvideo.com/node/27-10027887-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'37\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "91",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1063631",
              "name": "老年痴呆是啥体验？这套设备满足你",
              "pic": "http://image.pearvideo.com/cont/20170413/cont-1063631-10253895.png",
              "nodeInfo": {
                "nodeId": "26",
                "name": "seekr",
                "logoImg": "http://image2.pearvideo.com/node/26-10027889-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'50\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "242",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064564",
              "name": "日本发明排球机器人！中国女排别怕",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064564-10257024.jpg",
              "nodeInfo": {
                "nodeId": "27",
                "name": "灰度视频",
                "logoImg": "http://image.pearvideo.com/node/27-10027887-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'49\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "24",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "体育精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "9",
          "contList": [
            {
              "contId": "1064362",
              "name": "他能让你任打一分钟，绝对不还手",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064362-10256374.png",
              "nodeInfo": {
                "nodeId": "605",
                "name": "街力",
                "logoImg": "http://image1.pearvideo.com/node/605-10160149-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "04'53\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "13",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064344",
              "name": "极限酷跑——啊，多么痛的领悟！",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064344-10256186.jpg",
              "nodeInfo": {
                "nodeId": "559",
                "name": "野玩儿",
                "logoImg": "http://image1.pearvideo.com/node/559-10150378-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "05'01\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "46",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064327",
              "name": "背着山地车暴走几十公里，风景值得",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064327-10256102.jpg",
              "nodeInfo": {
                "nodeId": "559",
                "name": "野玩儿",
                "logoImg": "http://image1.pearvideo.com/node/559-10150378-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'18\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "27",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064374",
              "name": "水上飞人大合集，看完好想飞上天",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064374-10256285.jpg",
              "nodeInfo": {
                "nodeId": "559",
                "name": "野玩儿",
                "logoImg": "http://image1.pearvideo.com/node/559-10150378-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'59\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "48",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "财富精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "3",
          "contList": [
            {
              "contId": "1064659",
              "name": "王健林马云马化腾出行仪仗大比拼",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064659-10257470.png",
              "nodeInfo": {
                "nodeId": "14",
                "name": "老板联播",
                "logoImg": "http://image.pearvideo.com/node/14-10027905-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'06\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "55",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064616",
              "name": "竹子造车？不管你信不信，反正我信",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064616-10257285.png",
              "nodeInfo": {
                "nodeId": "17",
                "name": "麻辣车评",
                "logoImg": "http://image2.pearvideo.com/node/17-10027898-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'00\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "181",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064628",
              "name": "高能预警，这些概念车帅到没朋友",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064628-10257310.png",
              "nodeInfo": {
                "nodeId": "17",
                "name": "麻辣车评",
                "logoImg": "http://image2.pearvideo.com/node/17-10027898-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'58\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "351",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064632",
              "name": "一分半，别眨眼，这些全是车展干货",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064632-10257304.jpg",
              "nodeInfo": {
                "nodeId": "17",
                "name": "麻辣车评",
                "logoImg": "http://image2.pearvideo.com/node/17-10027898-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'58\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "36",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "新知精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "10",
          "contList": [
            {
              "contId": "1064050",
              "name": "苏联秘密研制的超级核潜艇",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064050-10255056.jpg",
              "nodeInfo": {
                "nodeId": "855",
                "name": "武器大讲堂",
                "logoImg": "http://image.pearvideo.com/node/855-10220985-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "04'32\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "30",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064596",
              "name": "为什么大家一听到特区就exciting",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064596-10257183.png",
              "nodeInfo": {
                "nodeId": "53",
                "name": "视知",
                "logoImg": "http://image1.pearvideo.com/node/53-10045375-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'28\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "22",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064047",
              "name": "同室操枪CQB 贴脸硬怼的反恐绝技",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064047-10255041.jpg",
              "nodeInfo": {
                "nodeId": "342",
                "name": "军武",
                "logoImg": "http://image2.pearvideo.com/node/342-10097261-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "19'13\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "6",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064520",
              "name": "为什么宿醉这么难受？",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064520-10256860.png",
              "nodeInfo": {
                "nodeId": "702",
                "name": "探吧",
                "logoImg": "http://image2.pearvideo.com/node/702-10176599-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'57\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "33",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "8",
          "nodeName": "生活精选",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "5",
          "contList": [
            {
              "contId": "1063489",
              "name": "鹦鹉的聪明程度你无法想象！",
              "pic": "http://image1.pearvideo.com/cont/20170413/cont-1063489-10252864.jpg",
              "nodeInfo": {
                "nodeId": "744",
                "name": "funplay",
                "logoImg": "http://image1.pearvideo.com/node/744-10195576-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'10\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "42",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064448",
              "name": "主人回家了，狗狗激动躺地起不来",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064448-10256633.png",
              "nodeInfo": {
                "nodeId": "797",
                "name": "西门小P爱趣闻",
                "logoImg": "http://image1.pearvideo.com/node/797-10201147-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'16\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "44",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064579",
              "name": "凡士林的5种妙用，赶紧get起来！",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064579-10257091.jpg",
              "nodeInfo": {
                "nodeId": "417",
                "name": "喵招",
                "logoImg": "http://image1.pearvideo.com/node/417-10111834-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'05\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "9",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1062923",
              "name": "你敢在这样的地方独自生活吗？",
              "pic": "http://image1.pearvideo.com/cont/20170412/cont-1062923-10250392.jpg",
              "nodeInfo": {
                "nodeId": "61",
                "name": "旅食家",
                "logoImg": "http://image.pearvideo.com/node/61-10034025-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "05'10\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "9",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "6",
          "nodeName": "排行榜",
          "isOrder": "",
          "nodeLogo": "",
          "nodeDesc": "",
          "moreId": "",
          "contList": [
            {
              "contId": "1064477",
              "name": "南京宝马案主角，事发当天越开越快",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064477-10256695.jpg",
              "nodeInfo": {
                "nodeId": "9",
                "name": "微辣Video",
                "logoImg": "http://image2.pearvideo.com/node/9-10027910-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "03'12\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "44",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064545",
              "name": "突发：杭州萧山一高架引桥断裂！",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064545-10256969.jpg",
              "nodeInfo": {
                "nodeId": "257",
                "name": "辣焦视频",
                "logoImg": "http://image.pearvideo.com/node/257-10082685-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'38\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "77",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064298",
              "name": "颤抖吧!老戏骨们7句狠话猛喷小鲜肉",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064298-10256023.png",
              "nodeInfo": {
                "nodeId": "66",
                "name": "水煮娱",
                "logoImg": "http://image2.pearvideo.com/node/66-10035464-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'47\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "305",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1063952",
              "name": "江湖菜馆不卖菜，暗藏按摩女\"卖肉\"",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1063952-10254994.png",
              "nodeInfo": {
                "nodeId": "25",
                "name": "一手Video",
                "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "00'51\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "218",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064218",
              "name": "攻壳机动队幕后： 寡姐吐槽紧身衣",
              "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064218-10255661.png",
              "nodeInfo": {
                "nodeId": "75",
                "name": "DailyBlah",
                "logoImg": "http://image2.pearvideo.com/node/75-10037639-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "04'16\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "715",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1063793",
              "name": "美女胸模月入五万：我不是坏女孩",
              "pic": "http://image1.pearvideo.com/cont/20170413/cont-1063793-10253989.jpg",
              "nodeInfo": {
                "nodeId": "27",
                "name": "灰度视频",
                "logoImg": "http://image.pearvideo.com/node/27-10027887-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "3",
              "cornerLabelDesc": "独播",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'28\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "2831",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "9",
          "nodeName": "1MILLIONofficial",
          "isOrder": "0",
          "nodeLogo": "http://image2.pearvideo.com/node/468-10136612-logo.png",
          "nodeDesc": "Inspire Million",
          "moreId": "468",
          "contList": [
            {
              "contId": "1060716",
              "name": "这么甜的情人舞，看的都想恋爱了",
              "pic": "http://image2.pearvideo.com/cont/20170407/cont-1060716-10241189.jpg",
              "nodeInfo": {
                "nodeId": "468",
                "name": "1MILLIONofficial",
                "logoImg": "http://image2.pearvideo.com/node/468-10136612-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "04'27\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "291",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1057894",
              "name": "小鲜肉变大男神只是一套舞的时间",
              "pic": "http://image1.pearvideo.com/cont/20170401/cont-1057894-10229716.jpg",
              "nodeInfo": {
                "nodeId": "468",
                "name": "1MILLIONofficial",
                "logoImg": "http://image2.pearvideo.com/node/468-10136612-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "04'01\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "101",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1057335",
              "name": "看了会睡不着的舞蹈",
              "pic": "http://image1.pearvideo.com/cont/20170331/cont-1057335-10227376.jpg",
              "nodeInfo": {
                "nodeId": "468",
                "name": "1MILLIONofficial",
                "logoImg": "http://image2.pearvideo.com/node/468-10136612-logo.png"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'36\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "42",
              "adExpMonitorUrl": ""
            }
          ]
        },
        {
          "nodeType": "9",
          "nodeName": "罐头视频",
          "isOrder": "0",
          "nodeLogo": "http://image2.pearvideo.com/node/57-10033238-logo.jpg",
          "nodeDesc": "盛产最脑洞的生活方式类短视频！",
          "moreId": "57",
          "contList": [
            {
              "contId": "1064331",
              "name": "自制纯天然安心味精",
              "pic": "http://image.pearvideo.com/cont/20170414/cont-1064331-10256154.jpg",
              "nodeInfo": {
                "nodeId": "57",
                "name": "罐头视频",
                "logoImg": "http://image2.pearvideo.com/node/57-10033238-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "5",
              "cornerLabelDesc": "推荐",
              "forwordType": "1",
              "videoType": "1",
              "duration": "01'00\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "49",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1064245",
              "name": "《迟到疑云》脑洞太大的迟到理由",
              "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064245-10256167.jpg",
              "nodeInfo": {
                "nodeId": "57",
                "name": "罐头视频",
                "logoImg": "http://image2.pearvideo.com/node/57-10033238-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "04'04\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "31",
              "adExpMonitorUrl": ""
            },
            {
              "contId": "1063652",
              "name": "DIY移动式木盘书桌",
              "pic": "http://image.pearvideo.com/cont/20170413/cont-1063652-10253871.jpg",
              "nodeInfo": {
                "nodeId": "57",
                "name": "罐头视频",
                "logoImg": "http://image2.pearvideo.com/node/57-10033238-logo.jpg"
              },
              "link": "http://",
              "linkType": "0",
              "cornerLabel": "",
              "cornerLabelDesc": "",
              "forwordType": "1",
              "videoType": "1",
              "duration": "02'33\"",
              "liveStatus": "",
              "liveStartTime": "",
              "praiseTimes": "10",
              "adExpMonitorUrl": ""
            }
          ]
        }
      ]
    }

json 解析：

- `resultCode`：为`1`时表请求成功
- `dataList`：具体数据
	- `nodeName`：所属板块，取值有`头条`、`为你推荐`、`全民拍客活动`、`最新视频`、`娱乐精选`等
	- `contList`：详细内容
		- `contId`：详细内容 id，用作查看[头条详细内容](#head_details)
		- `name`：标题
		- `pic`：图片 url
		- `nodeInfo`：
			- `name`：作者名
		- `duration`：时长
		- `cornerLabel`：视频类型代码
		- `cornerLabelDesc`：视频类型描述
		- `coverVideo`：视频播放地址
		- `praiseTimes`：点赞量
<h3 id="other_tag">其它标签</h3>

url：http://app.pearvideo.com/clt/jsp/v2/getCategoryConts.jsp

请求方式：POST

请求体：

- `hotPageidx`：请求页，取`1`、`2`、`3`等
- `categoryId`：从[列表获取](list_get)中获取到 json 中 `categoryId` 字段值

json 示例：

	{
      "resultCode": "1",
      "resultMsg": "success",
      "reqId": "56df84c3-1e98-4d6e-9a19-b04435697b43",
      "systemTime": "1492219550371",
      "areaList": [
        {
          "area_id": "101001",
          "expInfo": {
            "algorighm_exp_id": "",
            "front_exp_id": "0",
            "s_value": "7a2bd32d-b34a-44f5-aba3-31514d25bcaf_2153763857689046"
          }
        },
        {
          "area_id": "101002",
          "expInfo": {
            "algorighm_exp_id": "0",
            "front_exp_id": "0",
            "s_value": "0"
          }
        }
      ],
      "categoryInfo": {
        "categoryId": "4",
        "name": "娱乐",
        "color": "#E966AE"
      },
      "nextUrl": "http://app.pearvideo.com/clt/jsp/v2/getCategoryConts.jsp?categoryId=4&start=10",
      "hotList": [
        {
          "contId": "1064298",
          "name": "颤抖吧!老戏骨们7句狠话猛喷小鲜肉",
          "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064298-10256023.png",
          "nodeInfo": {
            "nodeId": "66",
            "name": "水煮娱",
            "logoImg": "http://image2.pearvideo.com/node/66-10035464-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "5",
          "cornerLabelDesc": "推荐",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'47\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "314"
        },
        {
          "contId": "1064218",
          "name": "攻壳机动队幕后： 寡姐吐槽紧身衣",
          "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064218-10255661.png",
          "nodeInfo": {
            "nodeId": "75",
            "name": "DailyBlah",
            "logoImg": "http://image2.pearvideo.com/node/75-10037639-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "04'16\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "735"
        },
        {
          "contId": "1064226",
          "name": "谁都敢怼！金星这张嘴到底有多毒？",
          "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064226-10255700.jpg",
          "nodeInfo": {
            "nodeId": "66",
            "name": "水煮娱",
            "logoImg": "http://image2.pearvideo.com/node/66-10035464-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'10\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "20"
        }
      ],
      "contList": [
        {
          "contId": "1064681",
          "name": "杨幂对拿奖保持平常心称努力过就好",
          "pic": "http://image2.pearvideo.com/cont/20170415/cont-1064681-10257632.jpg",
          "nodeInfo": {
            "nodeId": "710",
            "name": "饭爱豆娱乐",
            "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'25\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "7"
        },
        {
          "contId": "1064679",
          "name": "青春励志剧谭松韵首演菜鸟记者",
          "pic": "http://image1.pearvideo.com/cont/20170415/cont-1064679-10257664.png",
          "nodeInfo": {
            "nodeId": "710",
            "name": "饭爱豆娱乐",
            "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "02'04\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "8"
        },
        {
          "contId": "1064678",
          "name": "暖男魏大勋表示会认真做自己",
          "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064678-10257587.png",
          "nodeInfo": {
            "nodeId": "710",
            "name": "饭爱豆娱乐",
            "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'17\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "1"
        },
        {
          "contId": "1064676",
          "name": "洪金宝大谈赵文卓",
          "pic": "http://image2.pearvideo.com/cont/20170415/cont-1064676-10257620.png",
          "nodeInfo": {
            "nodeId": "710",
            "name": "饭爱豆娱乐",
            "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'47\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "3"
        },
        {
          "contId": "1064675",
          "name": "高晓松助阵威尼斯国际电影节",
          "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064675-10257616.png",
          "nodeInfo": {
            "nodeId": "710",
            "name": "饭爱豆娱乐",
            "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'28\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "20"
        },
        {
          "contId": "1064674",
          "name": "陈雅婷看秀理解战乱风波",
          "pic": "http://image.pearvideo.com/cont/20170414/cont-1064674-10257603.png",
          "nodeInfo": {
            "nodeId": "710",
            "name": "饭爱豆娱乐",
            "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'53\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "2"
        },
        {
          "contId": "1064672",
          "name": "林依晨凤小岳cp亮相惊艳全场",
          "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064672-10257590.png",
          "nodeInfo": {
            "nodeId": "710",
            "name": "饭爱豆娱乐",
            "logoImg": "http://image1.pearvideo.com/node/710-10178290-logo.png"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "02'08\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "14"
        },
        {
          "contId": "1064673",
          "name": "baby携子亮相跑男：要向超哥学带娃",
          "pic": "http://image1.pearvideo.com/cont/20170414/cont-1064673-10257547.jpg",
          "nodeInfo": {
            "nodeId": "66",
            "name": "水煮娱",
            "logoImg": "http://image2.pearvideo.com/node/66-10035464-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'10\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "36"
        },
        {
          "contId": "1064667",
          "name": "言承旭求过婚吗？林志玲答了三个字",
          "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064667-10257503.png",
          "nodeInfo": {
            "nodeId": "66",
            "name": "水煮娱",
            "logoImg": "http://image2.pearvideo.com/node/66-10035464-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'21\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "57"
        },
        {
          "contId": "1064640",
          "name": "决赛前夜，张碧晨帮唱嘉宾还没来",
          "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064640-10257371.jpg",
          "nodeInfo": {
            "nodeId": "66",
            "name": "水煮娱",
            "logoImg": "http://image2.pearvideo.com/node/66-10035464-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'08\"",
          "liveStatus": "",
          "liveStartTime": "",
          "praiseTimes": "21"
        }
      ]
    }

json 解析：

<h4 id="details">详细内容</h4>

url：http://app.pearvideo.com/clt/jsp/v2/content.jsp

拼接参数：

- `contId`：从[头条](#head) json 中 `contId` 字段获取到的值

url 示例：[`http://app.pearvideo.com/clt/jsp/v2/content.jsp?contId=1064146`](http://app.pearvideo.com/clt/jsp/v2/content.jsp?contId=1064146)

json 示例：

	{
      "resultCode": "1",
      "resultMsg": "success",
      "reqId": "215d100a-d167-47ee-8d27-fab609b36934",
      "systemTime": "1492153703690",
      "areaList": [
        {
          "area_id": "200008",
          "expInfo": {
            "algorighm_exp_id": "",
            "front_exp_id": "0",
            "s_value": "8f8a74f4-d7bc-41f9-b442-1e5f74622f9b_2088549785888668"
          }
        }
      ],
      "content": {
        "contId": "1064146",
        "name": "她收养40流浪猫:让它们有尊严活着",
        "summary": "辽宁沈阳，73岁老太孔德荣，是远近闻名的“猫奶奶”，10年收养流浪猫40余只，月花销上千元，她说服儿子让出车库给猫咪住，想让它们活得有尊严。",
        "source": "",
        "pubTime": "2017-04-14 12:53",
        "isVr": "0",
        "aspectRatio": "0",
        "contentHtml": "",
        "liveHtml": "",
        "postHtml": "http://app.pearvideo.com/clt/page/v2/topic_comm.jsp?postId=1047857&type=living",
        "praiseTimes": "266",
        "commentTimes": "3",
        "isFavorited": "0",
        "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064146-10255376.png",
        "postId": "1047857",
        "liveRoomId": "",
        "sharePic": "http://image.pearvideo.com/cont/20170414/cont-1064146-10255377.png",
        "shareUrl": "http://www.pearvideo.com/detail_1064146",
        "liveInfo": {},
        "cornerLabel": "3",
        "cornerLabelDesc": "独播",
        "authors": [
          {
            "userId": "10265801",
            "nickname": "泛    舟",
            "isPaike": "1",
            "paikeType": "1"
          }
        ],
        "tags": [
          {
            "tagId": "1365",
            "name": "老人"
          },
          {
            "tagId": "5390",
            "name": "好心人"
          },
          {
            "tagId": "15721",
            "name": "流浪猫"
          }
        ],
        "videos": [
          {
            "videoId": "10369556",
            "url": "http://video.pearvideo.com/mp4/short/20170414/cont-1064146-10369519-ld.mp4",
            "tag": "ld",
            "format": "mp4",
            "fileSize": "5913937",
            "duration": "117"
          },
          {
            "videoId": "10369557",
            "url": "http://video.pearvideo.com/mp4/short/20170414/cont-1064146-10369519-fhd.mp4",
            "tag": "fhd",
            "format": "mp4",
            "fileSize": "36734910",
            "duration": "117"
          },
          {
            "videoId": "10369558",
            "url": "http://video.pearvideo.com/mp4/short/20170414/cont-1064146-10369519-sd.mp4",
            "tag": "sd",
            "format": "mp4",
            "fileSize": "10265849",
            "duration": "117"
          },
          {
            "videoId": "10369559",
            "url": "http://video.pearvideo.com/mp4/short/20170414/cont-1064146-10369519-hd.mp4",
            "tag": "hd",
            "format": "mp4",
            "fileSize": "19314179",
            "duration": "117"
          }
        ],
        "nodeInfo": {
          "nodeId": "25",
          "name": "一手Video",
          "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg",
          "isOrder": "0",
          "desc": "千万拍客为你现场播报"
        },
        "copyright": "版权声明：本内容系梨视频独家，未经授权，不得转载",
        "isDownload": "1",
        "duration": "01'57\"",
        "adMonitorUrl": ""
      },
      "nextInfo": {
        "contId": "1060885",
        "name": "车祸现场交警脱衣，上演温馨一幕",
        "forwordType": "1"
      },
      "postInfo": {
        "postId": "1047857",
        "name": "“猫奶奶”十年收养40多只流浪猫",
        "commentTimes": "3",
        "communityInfo": {
          "communityId": "12",
          "name": "露一手",
          "logoImg": "http://imageugc2.pearvideo.com/community/12-10001210-logo.jpg"
        },
        "isfavorited": "0",
        "postHtml": "http://app.pearvideo.com/clt/page/v2/topic_comm.jsp?postId=1047857&contId=1064146",
        "childList": [
          {
            "commentId": "10324796",
            "content": "好人有好报！",
            "pubTime": "04-14 13:03",
            "topTimes": "1",
            "stepTimes": "2",
            "replyTimes": "0",
            "userInfo": {
              "userId": "10246234",
              "nickname": "鱼小胖",
              "isPaike": "0",
              "pic": "http://imageugc.pearvideo.com/user/20170214/10246234-210230.jpg"
            }
          },
          {
            "commentId": "10324982",
            "content": "对待流浪猫最好的方式是抓捕——绝育——放归，对流浪猫来说这样都关在笼子里就有尊严了么",
            "pubTime": "04-14 14:04",
            "topTimes": "0",
            "stepTimes": "0",
            "replyTimes": "0",
            "userInfo": {
              "userId": "10091535",
              "nickname": "刘面瘫",
              "isPaike": "0",
              "pic": "http://imageugc.pearvideo.com/user/20161224/10091535-123600.jpg"
            }
          },
          {
            "commentId": "10324977",
            "content": "人为出名无所不能",
            "pubTime": "04-14 13:56",
            "topTimes": "0",
            "stepTimes": "0",
            "replyTimes": "0",
            "userInfo": {
              "userId": "10558703",
              "nickname": "良",
              "isPaike": "0",
              "pic": "http://imageugc.pearvideo.com/user/20170413/10558703-213237.jpg"
            }
          }
        ]
      },
      "relateConts": [
        {
          "contId": "1060885",
          "name": "车祸现场交警脱衣，上演温馨一幕",
          "pic": "http://image2.pearvideo.com/cont/20170408/cont-1060885-10241849.png",
          "nodeInfo": {
            "nodeId": "25",
            "name": "一手Video",
            "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "3",
          "cornerLabelDesc": "独播",
          "forwordType": "1",
          "videoType": "1",
          "duration": "00'51\"",
          "liveStatus": "",
          "praiseTimes": "63"
        },
        {
          "contId": "1054359",
          "name": "感动！他竟然是这样给猫过生日的！",
          "pic": "http://image1.pearvideo.com/cont/20170327/cont-1054359-10215505.png",
          "nodeInfo": {
            "nodeId": "189",
            "name": "上海街头",
            "logoImg": "http://image1.pearvideo.com/node/189-10070077-logo.png"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "04'12\"",
          "liveStatus": "",
          "praiseTimes": "20"
        },
        {
          "contId": "1017920",
          "name": "理发只收1元，老人坚持了23年",
          "pic": "http://image2.pearvideo.com/cont/20161222/cont-1017920-10075253.jpg",
          "nodeInfo": {
            "nodeId": "9",
            "name": "微辣Video",
            "logoImg": "http://image2.pearvideo.com/node/9-10027910-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'05\"",
          "liveStatus": "",
          "praiseTimes": "5"
        },
        {
          "contId": "1019106",
          "name": "老人除雪17年，因儿子雪天车祸离世",
          "pic": "http://image1.pearvideo.com/cont/20161227/cont-1019106-10080103.png",
          "nodeInfo": {
            "nodeId": "25",
            "name": "一手Video",
            "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "3",
          "cornerLabelDesc": "独播",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'42\"",
          "liveStatus": "",
          "praiseTimes": "42"
        },
        {
          "contId": "1046947",
          "name": "他流浪一生，88岁终于住进敬老院",
          "pic": "http://image2.pearvideo.com/cont/20170313/cont-1046947-10186541.png",
          "nodeInfo": {
            "nodeId": "25",
            "name": "一手Video",
            "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "5",
          "cornerLabelDesc": "推荐",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'04\"",
          "liveStatus": "",
          "praiseTimes": "93"
        },
        {
          "contId": "1062475",
          "name": "拾荒老父再流浪:捡瓶换馍,不找女儿",
          "pic": "http://image1.pearvideo.com/cont/20170411/cont-1062475-10248622.png",
          "nodeInfo": {
            "nodeId": "25",
            "name": "一手Video",
            "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "3",
          "cornerLabelDesc": "独播",
          "forwordType": "1",
          "videoType": "1",
          "duration": "02'54\"",
          "liveStatus": "",
          "praiseTimes": "5428"
        }
      ]
    }

json 解析：

- `resultCode`：为`1`时表请求成功
- `content`：视频具体内容
	- `name`：视频标题
	- `summary`：视频描述
	- `pubTime`：视频上传时间
	- `tags`：标签
	- `relateConts`：相关视频
	- `postInfo`：其他信息
		- `childList`：评论信息
			- `commentId`：评论 id
			- `content`：评论内容
			- `pubTime`：评论时间
			- `topTimes`：顶的数量
			- `stepTimes`：踩的数量
			- `userInfo`：评论者信息
			- `replyTimes`：回复评论的数量
		- `videos`：各个版本视频连接
			- `url`：视频地址
			- `tag`：视频清晰度
			- `duration`：视频时长
			- `fileSize`：视频大小