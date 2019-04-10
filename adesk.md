- [不分类别获取手机壁纸接口](#vertical)
- [获取手机壁纸类别](#vertical-category)
- [获取某类手机壁纸下壁纸](#category-img)
- [获取手机壁纸评论](#vertical-comment)
- [下载手机壁纸](#get-vertical-img)
- [获取电脑壁纸类别](#pc-category)
- [获取类别下的电脑壁纸](#category-wallpaper)
- [获取电脑壁纸专辑](#wallpaper-album)
- [获取专辑下的壁纸](#album-wallpaper)
- [下载电脑壁纸](#get-wallpaper-img)

# 手机壁纸相关

<h2 id="vertical">不分类别获取壁纸接口</h2>

url：http://service.picasso.adesk.com/v1/vertical/vertical

拼接参数：

- `limit`：返回数量
- `adult`：布尔值，暂时未知
- `first`：数字，如1
- `skip`：略过数量
- `order`：值 `hot`为favs， `new`

url 示例：[`http://service.picasso.adesk.com/v1/vertical/vertical?limit=30&skip=180&adult=false&first=0&order=hot`](http://service.picasso.adesk.com/v1/vertical/vertical?limit=30&skip=180&adult=false&first=0&order=hot)


json 示例：

	{
    "msg": "success",
    "res": {
        "vertical": [
            {
                "preview": "http://img5.adesk.com/595de628e7bce77b95a5968f",
                "thumb": "http://img5.adesk.com/595de628e7bce77b95a5968f?imageMogr2/thumbnail/!350x540r/gravity/Center/crop/350x540",
                "img": "http://img5.adesk.com/595de628e7bce77b95a5968f?imageMogr2/thumbnail/!720x1280r/gravity/Center/crop/720x1280",
                "views": 0,
                "cid": [
                    "4e4d610cdf714d2966000002"
                ],
                "ncos": 10,
                "rank": 221797,
                "url": [
                ],
                "tag": [
                    "海",
                    "海浪",
                    "蓝色",
                    "风景",
                    "沙滩"
                ],
                "rule": "?imageMogr2/thumbnail/!$<Width>x$<Height>r/gravity/Center/crop/$<Width>x$<Height>",
                "wp": "http://img5.adesk.com/595de628e7bce77b95a5968f",
                "xr": false,
                "cr": false,
                "favs": 1725,
                "atime": 1500618604,
                "id": "595de628e7bce77b95a5968f",
                "store": "qiniu",
                "desc": ""
            }
        ]
    },
    "code": 0
}


解析：

- `msg`：响应信息
- `res`：返回的数据
	- `vertical`：返回的壁纸数据
		- `preview`：壁纸地址
		- `thumb`：小缩略图地址
		- `img`：大缩略图地址
		- `views`：查看数
		- `cid`：所属的类别ID
    - `rank`：点赞数
    - `tag`：壁纸标签
    - `rule`：返回不同大小壁纸规则
    - `wp`：手机版下载地址
    - `favs`：收藏数
    - `atime`：创建时间（单位：秒）
    - `id`：ID
    - `store`：云服务器地址
    - `desc`：描述
- `code`：返回码

<h2 id="vertical-category">获取手机壁纸类别</h2>

url：http://service.picasso.adesk.com/v1/vertical/category

拼接参数：

- `adult`：布尔值，暂时未知
- `first`：数字，如1

url 示例：[`http://service.picasso.adesk.com/v1/vertical/category?adult=false&first=1`](http://service.picasso.adesk.com/v1/vertical/category?adult=false&first=1)

json 示例：

	{
    "msg": "success",
    "res": {
        "category": [
            {
                "ename": "girl",
                "atime": 1291266021,
                "name": "美女",
                "cover": "http://img0.adesk.com/download/57e7155894e5cc60a375f653",
                "sn": 1,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4e4d610cdf714d2966000000",
                "desc": ""
            },
            {
                "ename": "animation",
                "atime": 1291266057,
                "name": "动漫",
                "cover": "http://img0.adesk.com/download/57e1111069401b6ca3675092",
                "sn": 2,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4e4d610cdf714d2966000003",
                "desc": ""
            },
            {
                "ename": "landscape",
                "atime": 1291266049,
                "name": "风景",
                "cover": "http://img0.adesk.com/download/57e9b82f94e5cc0a9e3e4148",
                "sn": 3,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4e4d610cdf714d2966000002",
                "desc": ""
            },
            {
                "ename": "game",
                "atime": 1300683934,
                "name": "游戏",
                "cover": "http://img0.adesk.com/download/57e4719c94e5cc3320a842d6",
                "sn": 4,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4e4d610cdf714d2966000007",
                "desc": ""
            },
            {
                "ename": "text",
                "atime": 1359601742,
                "name": "文字",
                "cover": "http://img0.adesk.com/download/57e3a91869401b37277ebd8f",
                "sn": 5,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "5109e04e48d5b9364ae9ac45",
                "desc": ""
            },
            {
                "ename": "vision",
                "atime": null,
                "name": "视觉",
                "cover": "http://img0.adesk.com/download/57e374d094e5cc14c62ac7ff",
                "sn": 6,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4fb479f75ba1c65561000027",
                "desc": ""
            },
            {
                "ename": "emotion",
                "atime": null,
                "name": "情感",
                "cover": "http://img0.adesk.com/download/57e9b7f994e5cc0a9e3e3fdb",
                "sn": 7,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4ef0a35c0569795756000000",
                "desc": ""
            },
            {
                "ename": "creative",
                "atime": null,
                "name": "设计",
                "cover": "http://img0.adesk.com/download/57e4aacc94e5cc3204926349",
                "sn": 8,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4fb47a195ba1c60ca5000222",
                "desc": ""
            },
            {
                "ename": "celebrity",
                "atime": 1359601746,
                "name": "明星",
                "cover": "http://img0.adesk.com/download/57d6291794e5cc1662ab12b4",
                "sn": 9,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "5109e05248d5b9368bb559dc",
                "desc": ""
            },
            {
                "ename": "stuff",
                "atime": null,
                "name": "物语",
                "cover": "http://img0.adesk.com/download/57e3cab494e5cc4d4267546b",
                "sn": 10,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4fb47a465ba1c65561000028",
                "desc": ""
            },
            {
                "ename": "art",
                "atime": null,
                "name": "艺术",
                "cover": "http://img0.adesk.com/download/57e3ad7794e5cc0dfd73401e",
                "sn": 11,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4ef0a3330569795757000000",
                "desc": ""
            },
            {
                "ename": "man",
                "atime": 1298251540,
                "name": "男人",
                "cover": "http://img0.adesk.com/download/57e3cb3594e5cc4d426756e2",
                "sn": 12,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4e4d610cdf714d2966000006",
                "desc": ""
            },
            {
                "ename": "cartoon",
                "atime": 1291266067,
                "name": "卡通",
                "cover": "http://img0.adesk.com/download/57e8655394e5cc322c85cffc",
                "sn": 13,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4e4d610cdf714d2966000004",
                "desc": ""
            },
            {
                "ename": "machine",
                "atime": 1297756191,
                "name": "机械",
                "cover": "http://img0.adesk.com/download/57e7696794e5cc15c9e09423",
                "sn": 13,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4e4d610cdf714d2966000005",
                "desc": ""
            },
            {
                "ename": "cityscape",
                "atime": null,
                "name": "城市",
                "cover": "http://img0.adesk.com/download/57e4e2e094e5cc2b50ce3664",
                "sn": 14,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4fb47a305ba1c60ca5000223",
                "desc": ""
            },
            {
                "ename": "animal",
                "atime": 1291266042,
                "name": "动物",
                "cover": "http://img0.adesk.com/download/57e6971394e5cc5209e89a1f",
                "sn": 16,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4e4d610cdf714d2966000001",
                "desc": ""
            },
            {
                "ename": "sport",
                "atime": null,
                "name": "运动",
                "cover": "http://img0.adesk.com/download/57e07cf794e5cc4c8af92a51",
                "sn": 17,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4ef0a34e0569795757000001",
                "desc": ""
            },
            {
                "ename": "movie",
                "atime": null,
                "name": "影视",
                "cover": "http://img0.adesk.com/download/57e3abb994e5cc0a2560e021",
                "sn": 18,
                "nimgs": 0,
                "uid": null,
                "type": 1,
                "id": "4e58c2570569791a19000000",
                "desc": ""
            }
        ]
    },
    "code": 0
}


解析：

- `msg`：响应信息
- `res`：返回的数据
  - `category`：返回的分类数据
    - `ename`：英文名
    - `atime`：创建时间
    - `name`：中文名
    - `cover`：封面
    - `id`：ID
    - `desc`：描述
- `code`：返回码

<h2 id="category-img">获取某类手机壁纸下壁纸</h2>

url：http://service.picasso.adesk.com/v1/vertical/category/ + 类别ID

拼接参数与解析均与`手机壁纸接口`一致

url 示例：[`http://service.picasso.adesk.com/v1/vertical/category/4e4d610cdf714d2966000003/vertical?limit=30&adult=false&first=1&order=new`](http://service.picasso.adesk.com/v1/vertical/category/4e4d610cdf714d2966000003/vertical?limit=30&adult=false&first=1&order=new)

<h2 id="vertical-comment">获取手机壁纸评论</h2>

url：http://service.picasso.adesk.com/v2/vertical/vertical/ + 壁纸ID +/comment

url 示例：[`http://service.picasso.adesk.com/v2/vertical/vertical/5ab8a9c4e7bce7356a197a07/comment`](http://service.picasso.adesk.com/v2/vertical/vertical/5ab8a9c4e7bce7356a197a07/comment)

json 示例：

	{
    "msg": "success",
    "res": {
        "comment": [
            {
                "reply_user": {
                },
                "reply_meta": {
                },
                "content": "赋册了那个男头整好一对",
                "isup": false,
                "user": {
                    "gcid": "",
                    "name": "呐",
                    "title": [
                    ],
                    "gender": 1,
                    "follower": 0,
                    "avatar": "http://wx.qlogo.cn/mmopen/vi_32/87rAP06gwZRdu0bsJxArlyMSbCmkWZdL4XbHJutOYrU7AtibEoQcSRXiaNceetPGXy4KYryWtEZzFYwiauuCZ52Lw/0",
                    "viptime": 1514605739,
                    "following": 0,
                    "isvip": false,
                    "id": "5a470cab2549593c6feff4c5"
                },
                "atime": 1523412606,
                "id": "5acd6e7e042208758c4fdbe9",
                "size": 1
            },
            {
                "reply_user": {
                    "gcid": "",
                    "name": "卍野念玉秋声雨卍",
                    "gender": 0,
                    "follower": 0,
                    "avatar": "http://q.qlogo.cn/qqapp/100428621/440684AEB14435F6BB257E8843139849/100",
                    "viptime": 1508053370,
                    "following": 1,
                    "isvip": false,
                    "id": "59e3117a9a1aa3405bfddbd8"
                },
                "reply_meta": {
                    "parent_id": "5acb29e19a1aa320b09b52fd",
                    "comment_id": "5acb29e19a1aa320b09b52fd",
                    "uid": "59e3117a9a1aa3405bfddbd8"
                },
                "content": "看我收藏",
                "isup": false,
                "user": {
                    "gcid": "",
                    "name": "▪ D ▪",
                    "title": [
                    ],
                    "gender": 0,
                    "follower": 0,
                    "avatar": "http://q.qlogo.cn/qqapp/100428621/8080E8F27C400BF30CC2ACEC2E2459E9/100",
                    "viptime": 978278400,
                    "following": 1,
                    "isvip": false,
                    "id": "54d3847c174cf15a4c95eb48"
                },
                "atime": 1523326825,
                "id": "5acc1f6904220875bde01eb2",
                "size": 2
            },
            {
                "reply_user": {
                },
                "reply_meta": {
                },
                "content": "另一半呢？",
                "isup": false,
                "user": {
                    "gcid": "",
                    "name": "卍野念玉秋声雨卍",
                    "title": [
                    ],
                    "gender": 0,
                    "follower": 0,
                    "avatar": "http://q.qlogo.cn/qqapp/100428621/440684AEB14435F6BB257E8843139849/100",
                    "viptime": 1508053370,
                    "following": 1,
                    "isvip": false,
                    "id": "59e3117a9a1aa3405bfddbd8"
                },
                "atime": 1523263969,
                "id": "5acb29e19a1aa320b09b52fd",
                "size": 3
            },
            {
                "reply_user": {
                },
                "reply_meta": {
                },
                "content": "情头",
                "isup": false,
                "user": {
                    "gcid": "",
                    "name": "无幻",
                    "title": [
                    ],
                    "gender": 0,
                    "follower": 0,
                    "avatar": "http://q.qlogo.cn/qqapp/100428621/E6517D0DC78EA100B9C7AB3AC1AF05BE/100",
                    "viptime": 1490668360,
                    "following": 0,
                    "isvip": false,
                    "id": "58d9cb482549595a962cd5b5"
                },
                "atime": 1523186209,
                "id": "5ac9fa2104220875bde0146b",
                "size": 3
            }
        ],
        "hot": [
        ],
        "meta": {
            "more": false
        },
        "vertical": {
            "isfavor": false
        }
    },
    "code": 0
}


解析：

- `msg`：响应信息
- `res`：返回的数据
  - `comment`：返回的评论数据
    - `reply_user`：所回复的评论的发表用户信息
    - `reply_meta`：所回复的评论的元数据
    - `content`：评论内容
    - `isup`：封面
    - `user`：
      - `gcid`：
      - `name`：
      - `title`：
      - `gender`：
      - `avatar`：
      - `follower`：
      - `viptime`：
      - `following`：
      - `isvip`：
      - `id`：
    - `atime`：
    - `id`：ID
    - `size`：点赞数
- `code`：返回码


<h2 id="get-vertical-img">下载手机壁纸</h2>

url：http://img5.adesk.com/ + 壁纸ID


# 电脑壁相关

<h2 id="pc-category">获取电脑壁纸类别</h2>

url：http://service.picasso.adesk.com/v1/wallpaper/category

json 示例：

	{
    "msg": "success",
    "res": {
        "category": [
            {
                "count": 50741,
                "ename": "girl",
                "rname": "美女",
                "cover_temp": "56a964df69401b2866828acb",
                "name": "美女",
                "cover": "http://img5.adesk.com/5ac9b7f3e7bce7251e7c51d6?imageMogr2/thumbnail/!640x480r/gravity/Center/crop/640x480",
                "rank": 1,
                "filter": [
                ],
                "sn": 1,
                "icover": "564d831f69401b5aed4a86ca",
                "atime": 1291266021,
                "type": 1,
                "id": "4e4d610cdf714d2966000000",
                "picasso_cover": "5ac9b7f3e7bce7251e7c51d6"
            },
            {
                "count": 93572,
                "ename": "animation",
                "rname": "动漫",
                "cover_temp": "56a221c969401b3f4aa6700a",
                "name": "动漫",
                "cover": "http://img5.adesk.com/5abed1a6e7bce735c2ee06ef?imageMogr2/thumbnail/!640x480r/gravity/Center/crop/640x480",
                "rank": 4,
                "id": "4e4d610cdf714d2966000003",
                "icover": "5880889ae7bce7755f3607d9",
                "sn": 2,
                "atime": 1291266057,
                "type": 1,
                "filter": [
                ],
                "picasso_cover": "5abed1a6e7bce735c2ee06ef"
            },
            {
                "count": 72666,
                "ename": "landscape",
                "rname": "风景",
                "cover_temp": "56a770e269401b756c748b28",
                "name": "风景",
                "cover": "http://img5.adesk.com/5ac32b7de7bce7256756a404?imageMogr2/thumbnail/!640x480r/gravity/Center/crop/640x480",
                "rank": 3,
                "id": "4e4d610cdf714d2966000002",
                "icover": "58734362e7bce76b93ca2739",
                "sn": 3,
                "atime": 1291266049,
                "type": 1,
                "filter": [
                ],
                "picasso_cover": "5ac32b7de7bce7256756a404"
            }
        ]
    },
    "code": 0
}

解析：

- `msg`：响应信息
- `res`：返回的数据
  - `category`：返回的类别数据
    - `count`：总数量
    - `ename`：英文名
    - `name`：类别中文名
    - `cover`：封面
    - `atime`：创建时间
    - `id`：ID
    - `picasso_cover`：封面图ID
- `code`：返回码


<h2 id="category-wallpaper">获取类别下的电脑壁纸</h2>

url：http://service.picasso.adesk.com/v1/wallpaper/category/+ 类别ID +/wallpaper

拼接参数与解析与`手机壁纸接口`类似

url 示例：[`http://service.picasso.adesk.com/v1/wallpaper/category/4e4d610cdf714d2966000003/wallpaper?limit=30&adult=false&first=1&order=new`](http://service.picasso.adesk.com/v1/wallpaper/category/4e4d610cdf714d2966000003/wallpaper?limit=30&adult=false&first=1&order=new)

json 示例：

    {
    "msg": "success",
    "res": {
        "wallpaper": [
            {
                "views": 0,
                "ncos": 63,
                "rank": 28586,
                "tag": [
                    "动漫",
                    "二次元",
                    "萝莉",
                    "粉色",
                    "可爱"
                ],
                "wp": "http://img0.adesk.com/wallpaper?imgid=58808890e7bce774e155766e",
                "xr": true,
                "cr": false,
                "favs": 899,
                "atime": 1486044199,
                "id": "58808890e7bce774e155766e",
                "desc": "",
                "thumb": "http://img0.adesk.com/download/58933c27e7bce76a0ab897cf",
                "img": "http://img0.adesk.com/download/58933c27e7bce76a0ab897d9",
                "cid": [
                    "4e4d610cdf714d2966000003"
                ],
                "url": [
                ],
                "preview": "http://img0.adesk.com/download/58933c27e7bce76a0ab897ae",
                "store": "adesk"
            },
            {
                "views": 0,
                "ncos": 16,
                "rank": 6673,
                "tag": [
                    "动漫",
                    "二次元",
                    "风夏",
                    "少女",
                    "蓝发",
                    "耳机"
                ],
                "wp": "http://img0.adesk.com/wallpaper?imgid=58808988e7bce774f46e9d0a",
                "xr": false,
                "cr": false,
                "favs": 271,
                "atime": 1486022615,
                "id": "58808988e7bce774f46e9d0a",
                "desc": "",
                "thumb": "http://img0.adesk.com/download/5892e7d7e7bce708ac9434f2",
                "img": "http://img0.adesk.com/download/5892e7d7e7bce708ac9434fb",
                "cid": [
                    "4e4d610cdf714d2966000003"
                ],
                "url": [
                ],
                "preview": "http://img0.adesk.com/download/5892e7d7e7bce708ac9434d0",
                "store": "adesk"
            }
        ]
    },
    "code": 0
}


<h2 id="wallpaper-album">获取电脑壁纸专辑</h2>
url：http://service.picasso.adesk.com/v1/wallpaper/album

拼接参数与`手机壁纸接口`类似


url 示例：[`http://service.picasso.adesk.com/v1/wallpaper/album?limit=10&adult=false&first=1&order=hot`](http://service.picasso.adesk.com/v1/wallpaper/album?limit=10&adult=false&first=1&order=hot)

json 示例：

    {
    "msg": "success",
    "res": {
        "album": [
            {
                "status": "online",
                "ename": "多啦A梦",
                "atime": 1313732913,
                "user": {
                    "gcid": "",
                    "name": "Ipaper",
                    "gender": 0,
                    "follower": 18,
                    "avatar": "http://img0.adesk.com/download/50f37f0d94e5cc5765e941fd",
                    "viptime": 978278400,
                    "following": 7,
                    "isvip": false,
                    "id": "4d5a337c716ec209a5000000"
                },
                "name": "多啦A梦",
                "url": [
                ],
                "desc": "“我可以实现你一个愿望”“那我……想要一个机器猫”",
                "cover": "http://img0.adesk.com/download/53a1020b69401b6f29d91459",
                "id": "4e4df93105697918e6000000",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a1020b69401b6f29d9145b",
                "favs": 12252,
                "type": 1,
                "isfeed": false
            },
            {
                "status": "online",
                "ename": "小动物",
                "atime": 1291266042,
                "user": {
                    "gcid": "",
                    "name": "安卓壁纸蛋蛋君",
                    "gender": 1,
                    "follower": 4521,
                    "avatar": "http://img0.adesk.com/download/53bcf873174cf12dc1add149",
                    "viptime": 978278400,
                    "following": 0,
                    "isvip": false,
                    "id": "4d5a2259716ec209a4000000"
                },
                "name": "小动物",
                "url": [
                ],
                "desc": "感谢生命中有他们的温暖陪伴",
                "cover": "http://img0.adesk.com/download/53a16dc569401b6f29dae5c9",
                "id": "4cf727fa716ec22db1000000",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a16dc569401b6f29dae5cb",
                "favs": 2792,
                "type": 1,
                "isfeed": false
            },
            {
                "status": "online",
                "ename": "卡通",
                "atime": 1291266057,
                "user": {
                    "gcid": "",
                    "name": "安卓壁纸蛋蛋君",
                    "gender": 1,
                    "follower": 4521,
                    "avatar": "http://img0.adesk.com/download/53bcf873174cf12dc1add149",
                    "viptime": 978278400,
                    "following": 0,
                    "isvip": false,
                    "id": "4d5a2259716ec209a4000000"
                },
                "name": "卡通",
                "url": [
                ],
                "desc": "cartoon, cute little thing",
                "cover": "http://img0.adesk.com/download/53a297d569401b458afca610",
                "id": "4cf72809716ec22daf000001",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a297d569401b458afca62c",
                "favs": 26111,
                "type": 1,
                "isfeed": false
            },
            {
                "status": "online",
                "ename": "机械",
                "atime": 1297756191,
                "user": {
                    "gcid": "",
                    "name": "安卓壁纸蛋蛋君",
                    "gender": 1,
                    "follower": 4521,
                    "avatar": "http://img0.adesk.com/download/53bcf873174cf12dc1add149",
                    "viptime": 978278400,
                    "following": 0,
                    "isvip": false,
                    "id": "4d5a2259716ec209a4000000"
                },
                "name": "机械",
                "url": [
                ],
                "desc": "guns,machine,etc",
                "cover": "http://img0.adesk.com/download/53a07f2f69401b6f29d6cef9",
                "id": "4d5a301f716ec20999000004",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a07f3069401b6f29d6cefb",
                "favs": 2012,
                "type": 1,
                "isfeed": false
            },
            {
                "status": "online",
                "ename": "安卓机器人",
                "atime": 1313696307,
                "user": {
                    "gcid": "",
                    "name": "安卓壁纸蛋蛋君",
                    "gender": 1,
                    "follower": 4521,
                    "avatar": "http://img0.adesk.com/download/53bcf873174cf12dc1add149",
                    "viptime": 978278400,
                    "following": 0,
                    "isvip": false,
                    "id": "4d5a2259716ec209a4000000"
                },
                "name": "安卓机器人",
                "url": [
                ],
                "desc": "安卓无敌！",
                "cover": "http://img0.adesk.com/download/53a16ff869401b6f29daef2d",
                "id": "4e4d6a3305697911c9000005",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a16ff869401b6f29daef2f",
                "favs": 2197,
                "type": 1,
                "isfeed": false
            },
            {
                "status": "online",
                "ename": "盒子先生",
                "atime": 1313696371,
                "user": {
                    "gcid": "",
                    "name": "安卓壁纸蛋蛋君",
                    "gender": 1,
                    "follower": 4521,
                    "avatar": "http://img0.adesk.com/download/53bcf873174cf12dc1add149",
                    "viptime": 978278400,
                    "following": 0,
                    "isvip": false,
                    "id": "4d5a2259716ec209a4000000"
                },
                "name": "盒子先生",
                "url": [
                ],
                "desc": "发现盒子先生的世界 ( ¯ □ ¯ )",
                "cover": "http://img0.adesk.com/download/53a1798a69401b6f29db131a",
                "id": "4e4d6a7305697911c9000006",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a1798a69401b6f29db131c",
                "favs": 14898,
                "type": 1,
                "isfeed": false
            },
            {
                "status": "online",
                "ename": "中国风",
                "atime": 1313697638,
                "user": {
                    "gcid": "",
                    "name": "安卓壁纸蛋蛋君",
                    "gender": 1,
                    "follower": 4521,
                    "avatar": "http://img0.adesk.com/download/53bcf873174cf12dc1add149",
                    "viptime": 978278400,
                    "following": 0,
                    "isvip": false,
                    "id": "4d5a2259716ec209a4000000"
                },
                "name": "中国风",
                "url": [
                ],
                "desc": "中国文化，博大精深",
                "cover": "http://img0.adesk.com/download/53a13db669401b6f29da1913",
                "id": "4e4d6f660569791281000000",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a13db769401b6f29da1915",
                "favs": 22159,
                "type": 1,
                "isfeed": false
            },
            {
                "status": "online",
                "ename": "我爱汽车",
                "atime": 1313697740,
                "user": {
                    "gcid": "",
                    "name": "安卓壁纸蛋蛋君",
                    "gender": 1,
                    "follower": 4521,
                    "avatar": "http://img0.adesk.com/download/53bcf873174cf12dc1add149",
                    "viptime": 978278400,
                    "following": 0,
                    "isvip": false,
                    "id": "4d5a2259716ec209a4000000"
                },
                "name": "贴地飞行",
                "url": [
                ],
                "desc": "激活细胞的跃动，引爆血液的燃烧",
                "cover": "http://img0.adesk.com/download/53a2c15b69401b45756b47e9",
                "id": "4e4d6fcc0569791281000001",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a2c15b69401b45756b4806",
                "favs": 7249,
                "type": 1,
                "isfeed": false
            },
            {
                "status": "online",
                "ename": "看灰机",
                "atime": 1313697841,
                "user": {
                    "gcid": "",
                    "name": "安卓壁纸蛋蛋君",
                    "gender": 1,
                    "follower": 4521,
                    "avatar": "http://img0.adesk.com/download/53bcf873174cf12dc1add149",
                    "viptime": 978278400,
                    "following": 0,
                    "isvip": false,
                    "id": "4d5a2259716ec209a4000000"
                },
                "name": "看灰机",
                "url": [
                ],
                "desc": "看，灰过来了，又灰过去了！",
                "cover": "http://img0.adesk.com/download/53a1753169401b6f29db02ae",
                "id": "4e4d70310569791281000003",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a1753169401b6f29db02b0",
                "favs": 3950,
                "type": 1,
                "isfeed": false
            },
            {
                "status": "online",
                "ename": "山水",
                "atime": 1313697989,
                "user": {
                    "gcid": "",
                    "name": "安卓壁纸蛋蛋君",
                    "gender": 1,
                    "follower": 4521,
                    "avatar": "http://img0.adesk.com/download/53bcf873174cf12dc1add149",
                    "viptime": 978278400,
                    "following": 0,
                    "isvip": false,
                    "id": "4d5a2259716ec209a4000000"
                },
                "name": "山水",
                "url": [
                ],
                "desc": "临深而志清 登高而意远",
                "cover": "http://img0.adesk.com/download/53a2994e69401b461bc08dda",
                "id": "4e4d70c50569791387000001",
                "tag": [
                ],
                "sn": 999,
                "lcover": "http://img0.adesk.com/download/53a2994e69401b461bc08dfb",
                "favs": 8542,
                "type": 1,
                "isfeed": false
            }
        ],
        "banner": [
            {
                "value": {
                    "ename": "",
                    "isfeed": false,
                    "tag": [
                    ],
                    "id": "5acc62e8e7bce7251e7c5377",
                    "top": 0,
                    "type": 1,
                    "status": "online",
                    "user": {
                        "gcid": "",
                        "name": "蛋蛋君",
                        "gender": 0,
                        "follower": 2982,
                        "avatar": "http://s.adesk.com/picasso/avatar_default.png",
                        "viptime": 978278400,
                        "following": 0,
                        "isvip": false,
                        "id": "561f6b2194e5cc423617f328"
                    },
                    "favs": 10,
                    "atime": 1523344104,
                    "desc": "毕业季伤感未至，离奇“作品”却是汹汹来袭，毕设内容新奇独特，创作过程却是一波三折，4.13 无刺激，不毕业，《毕业作品》不见不散",
                    "name": "【独家】毕业作品",
                    "url": [
                        {
                            "name": "点我送票哦！",
                            "target": "https://weibo.com/1977161541/GbsudF1gx?from=page_1006061977161541_profile&wvr=6&mod=weibotime&type=comment"
                        }
                    ],
                    "cover": "http://img5.adesk.com/5acc664ee7bce72552e69f12?imageView2/3/h/240",
                    "lcover": "http://img5.adesk.com/5acc664ee7bce72552e69f12?imageView2/3/h/720",
                    "subname": "",
                    "sn": 999
                },
                "offtm": 1523345483,
                "target": "5acc62e8e7bce7251e7c5377",
                "img": "5acc684be7bce7251e7c537a",
                "new_img": null,
                "new_thumb": "http://img0.adesk.com/download/http://img0.adesk.com/download/5acc684be7bce7251e7c537a",
                "oid": null,
                "thumb": "http://img0.adesk.com/download/5acc684be7bce7251e7c537a",
                "module": 5,
                "_id": "5acc684be7bce7251e7c537d",
                "reco": "",
                "ontm": 1523345483,
                "desc": "",
                "atime": 1523345483,
                "type": 7,
                "id": "5acc684be7bce7251e7c537d",
                "market": [
                ],
                "uid": "5965cd0be7bce7312ef79fbf"
            },
            {
                "value": {
                    "status": "online",
                    "ename": "",
                    "atime": 1481871292,
                    "url": [
                    ],
                    "user": {
                        "gcid": "",
                        "name": "兔几",
                        "gender": 1,
                        "follower": 6228,
                        "avatar": "http://img0.adesk.com/download/5847b5adda76f7450a045ef4",
                        "viptime": 1479363990,
                        "following": 0,
                        "isvip": false,
                        "id": "582d4d9694e5cc1942a88c3e"
                    },
                    "cover": "http://img5.adesk.com/5acb1a18e7bce72552e69ed5?imageView2/3/h/240",
                    "name": "魔卡少女樱",
                    "tag": [
                    ],
                    "sn": 999,
                    "id": "58538fbc69401b34865ef784",
                    "lcover": "http://img5.adesk.com/5acb1a18e7bce72552e69ed5?imageView2/3/h/720",
                    "favs": 6733,
                    "type": 1,
                    "isfeed": false,
                    "desc": "木之本樱，是就读于友枝小学的小学4年级学生。与父亲和哥哥3人一起生活。一天，小樱在父亲的书房发现一本奇怪的书。那本书中是会给这个世界带来灾难的“库洛牌”！为了回收散布各处的库洛牌，小樱成为了“魔卡捕获者”并不断奋斗……"
                },
                "offtm": 1518438510,
                "target": "58538fbc69401b34865ef784",
                "img": "5a81886ee7bce7259115e72f",
                "new_img": "5a81886ee7bce7259115e732",
                "new_thumb": "http://img0.adesk.com/download/5a81886ee7bce7259115e732",
                "oid": null,
                "thumb": "http://img0.adesk.com/download/5a81886ee7bce7259115e72f",
                "module": 5,
                "_id": "5a81886ee7bce7259115e735",
                "reco": "",
                "ontm": 1518438510,
                "desc": "",
                "atime": 1518438510,
                "type": 7,
                "id": "5a81886ee7bce7259115e735",
                "market": [
                ],
                "uid": "507b922bcd29911da5b9bea8"
            }
        ]
    },
    "code": 0
}


解析：

- `msg`：响应信息
- `res`：返回的数据
  - `album`：返回的专辑数据
    - `name`：专辑名
    - `desc`：描述
    - `cover`：封面
    - `lcover`：大封面
    - `atime`：创建时间
    - `favs`：收藏数
    - `id`：ID
  - `banner`：返回的banner信息（与专辑无关，是时间的banner）
    - `value`：banner宣传的专辑信息
    - `offtm`：时间
    - `img`：封面图片ID
    - `atime`：创建时间
    - `target`：所宣传的专辑的ID
    - `thumb`：封面图片地址
    - `id`：ID
- `code`：返回码


<h2 id="album-wallpaper">获取专辑下的壁纸</h2>

url：http://service.picasso.adesk.com/v1/wallpaper/album/+ 专辑ID +/wallpaper

拼接参数、解析与`手机壁纸接口`类似


url 示例：[`http://service.picasso.adesk.com/v1/wallpaper/album/5acc579be7bce7253c78cf9c/wallpaper?limit=30&adult=false&first=1&order=new`](http://service.picasso.adesk.com/v1/wallpaper/album/5acc579be7bce7253c78cf9c/wallpaper?limit=30&adult=false&first=1&order=new)

json示例：

    {
    "msg": "success",
    "res": {
        "album": {
            "ename": "",
            "isfeed": false,
            "tag": [
            ],
            "id": "5acc579be7bce7253c78cf9c",
            "top": 0,
            "type": 1,
            "status": "online",
            "user": {
                "gcid": "",
                "name": "一念夕雾",
                "gender": 1,
                "follower": 13656,
                "avatar": "http://img0.adesk.com/download/5ab664ca254959399461b5f7",
                "viptime": 1499843851,
                "following": 0,
                "isvip": false,
                "id": "5965cd0be7bce7312ef79fbf"
            },
            "favs": 74,
            "atime": 1523341211,
            "desc": "九头龙八一仅16岁就获得了将棋界最强头衔“龙王”，某天他的家中竟突然出现了一名9岁的小学女生雏鹤爱，并且对方还要成为八一的弟子？！在这样的背景下，一场奇妙的同居生活就此开始。",
            "name": "龙王的工作",
            "url": [
            ],
            "cover": "http://img5.adesk.com/5acc73c0e7bce7250515cdcb?imageView2/3/h/240",
            "lcover": "http://img5.adesk.com/5acc73c0e7bce7250515cdcb?imageView2/3/h/720",
            "subname": "",
            "sn": 999
        },
        "wallpaper": [
        ],
        "subject": [
        ]
    },
    "code": 0
}



<h2 id="get-wallpaper-img">下载电脑壁纸</h2>

url：http://img5.adesk.com/ + 壁纸ID