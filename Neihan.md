# 内涵段子 #
- [获取 content_type](#get)
- [推荐](#recommend)
- [视频](#video)
- [段友秀](#video_show)
- [直播](#live)
- [图片](#picture)
- [段子](#joke)

<h1 id="get">获取 content_type</h1>
url：http://lf.snssdk.com/neihan/service/tabs/

拼接参数：
同[推荐](#recommend)

url 示例：[`http://lf.snssdk.com/neihan/service/tabs/?essence=1&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120`](http://lf.snssdk.com/neihan/service/tabs/?essence=1&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120)

json 示例：

	{
          "message": "success",
          "data": [
            {
              "double_col_mode": false,
              "umeng_event": "moment",
              "is_default_tab": false,
              "url": "http://lf.snssdk.com/neihan/dongtai/dongtai_list/v1/",
              "list_id": -10001,
              "refresh_interval": 86400,
              "type": 3,
              "name": "关注"
            },
            {
              "double_col_mode": false,
              "umeng_event": "recommend",
              "is_default_tab": true,
              "url": "http://lf.snssdk.com/neihan/stream/mix/v1/?content_type=-101",
              "list_id": -101,
              "refresh_interval": 21600,
              "type": 1,
              "name": "推荐"
            },
            {
              "double_col_mode": false,
              "umeng_event": "video",
              "is_default_tab": false,
              "url": "http://lf.snssdk.com/neihan/stream/mix/v1/?content_type=-104",
              "list_id": -104,
              "refresh_interval": 21600,
              "type": 1,
              "name": "视频"
            },
            {
              "double_col_mode": true,
              "umeng_event": "personal_show",
              "is_default_tab": false,
              "url": "http://lf.snssdk.com/neihan/stream/mix/v1/?content_type=-301",
              "list_id": -301,
              "refresh_interval": 21600,
              "type": 1,
              "name": "段友秀"
            },
            {
              "double_col_mode": false,
              "umeng_event": "live",
              "is_default_tab": false,
              "url": "https://hotsoon.snssdk.com/hotsoon/feed/",
              "list_id": -10002,
              "refresh_interval": 300,
              "type": 6,
              "name": "直播"
            },
            {
              "double_col_mode": false,
              "umeng_event": "pic",
              "is_default_tab": false,
              "url": "http://lf.snssdk.com/neihan/stream/mix/v1/?content_type=-103",
              "list_id": -103,
              "refresh_interval": 21600,
              "type": 1,
              "name": "图片"
            },
            {
              "double_col_mode": false,
              "umeng_event": "essay",
              "is_default_tab": false,
              "url": "http://lf.snssdk.com/neihan/stream/mix/v1/?content_type=-102",
              "list_id": -102,
              "refresh_interval": 21600,
              "type": 1,
              "name": "段子"
            },
            {
              "double_col_mode": false,
              "umeng_event": "essence",
              "is_default_tab": false,
              "url": "http://ic.snssdk.com/neihan/in_app/essence_list/",
              "list_id": -20002,
              "refresh_interval": 86400,
              "type": 4,
              "name": "精华"
            },
            {
              "double_col_mode": false,
              "umeng_event": "local",
              "is_default_tab": false,
              "url": "http://lf.snssdk.com/neihan/stream/mix/v1/?content_type=-201",
              "list_id": -201,
              "refresh_interval": 86400,
              "type": 5,
              "name": "同城"
            },
            {
              "double_col_mode": false,
              "umeng_event": "game",
              "is_default_tab": false,
              "url": "http://ic.snssdk.com/game/game_hall?app_source=essay_android",
              "list_id": -20003,
              "refresh_interval": 86400,
              "type": 4,
              "name": "游戏"
            }
          ]
        }

json 解析：

其中 `list_id` 是每个标签页分类的标识，详情见[推荐](#recommend)中的 `content_type` 字段

<h1 id="recommend">推荐</h1>

url：`http://iu.snssdk.com/neihan/stream/mix/v1/`

拼接参数：

- `webp`：固定值 `1`
- `essence`：固定值 `1`
- `content_type`：从[获取 content_type](#get) 中获取得到的 `list_id` 字段值。目前[推荐](#recommend)的是`-101`，[视频](#video)的是`-104`，[段友秀](#video_show)的是`-301`，[图片](#picture)的是`-103`，[段子](#joke)的是`-102`
- `message_cursor`：固定值`-1`
- `am_longitude`：经度。可为空
- `am_latitude`：纬度。可为空
- `am_city`：城市名，例如：`北京市`。可为空
- `am_loc_time`：当前时间 Unix 时间戳，毫秒为单位
- `count`：返回数量
- `min_time`：上次更新时间的 Unix 时间戳，秒为单位
- `screen_width`：屏幕宽度，px为单位
- `double_col_mode`：固定值`0`
- `iid`：???，一个长度为10的纯数字字符串，用于标识用户唯一性
- `device_id`：设备 id，一个长度为11的纯数字字符串
- `ac`：网络环境，可取值 `wifi`
- `channel`：下载渠道，可`360`、`tencent`等
- `aid`：固定值`7`
- `app_name`：固定值`joke_essay`
- `version_code`：版本号去除小数点，例如`612`
- `version_name`：版本号，例如`6.1.2`
- `device_platform`：设备平台，`android` 或 `ios`
- `ssmix`：固定值 `a`
- `device_type`：设备型号，例如 `hongmi`
- `device_brand`：设备品牌，例如 `xiaomi`
- `os_api`：操作系统版本，例如`20`
- `os_version`：操作系统版本号，例如`7.1.0`
- `uuid`：用户 id，一个长度为15的纯数字字符串
- `openudid`：一个长度为16的数字和小写字母混合字符串
- `manifest_version_code`：版本号去除小数点，例如`612`
- `resolution`：屏幕宽高，例如 `1920*1080`
- `dpi`：手机 dpi
- `update_version_code`：版本号去除小数点后乘10，例如`6120`

url 示例：

[`http://iu.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-101&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1463225362314&count=30&min_time=1465232121&screen_width=1450&do00le_col_mode=0&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120`](http://iu.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-101&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1463225362314&count=30&min_time=1465232121&screen_width=1450&do00le_col_mode=0&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120)

json 示例：

	{
          "message": "success",
          "data": {
            "has_more": true,
            "tip": "1条新内容",
            "has_new_message": false,
            "max_time": 1489235731,
            "min_time": 1489235731,
            "data": [
              {
                "group": {
                  "360p_video": {
                    "width": 640,
                    "url_list": [
                      {
                        "url": "http://ic.snssdk.com/neihan/video/playback/1489235732.1/?video_id=d2a0fc9bb4784a6c983cd4a341df6d76&quality=360p&line=0&is_gif=0&device_platform=android"
                      },
                      {
                        "url": "http://ic.snssdk.com/neihan/video/playback/1489235732.1/?video_id=d2a0fc9bb4784a6c983cd4a341df6d76&quality=360p&line=1&is_gif=0&device_platform=android"
                      }
                    ],
                    "uri": "360p/d2a0fc9bb4784a6c983cd4a341df6d76",
                    "height": 360
                  },
                  "mp4_url": "http://ic.snssdk.com/neihan/video/playback/1489235732.1/?video_id=d2a0fc9bb4784a6c983cd4a341df6d76&quality=480p&line=0&is_gif=0&device_platform=android.mp4",
                  "text": "大胃王密子君（异国风情餐）芝士就是力量，所以我要多吃一点！",
                  "720p_video": {
                    "width": 640,
                    "url_list": [
                      {
                        "url": "http://ic.snssdk.com/neihan/video/playback/1489235732.1/?video_id=d2a0fc9bb4784a6c983cd4a341df6d76&quality=720p&line=0&is_gif=0&device_platform=android"
                      },
                      {
                        "url": "http://ic.snssdk.com/neihan/video/playback/1489235732.1/?video_id=d2a0fc9bb4784a6c983cd4a341df6d76&quality=720p&line=1&is_gif=0&device_platform=android"
                      }
                    ],
                    "uri": "720p/d2a0fc9bb4784a6c983cd4a341df6d76",
                    "height": 360
                  },
                  "digg_count": 288,
                  "duration": 297.672,
                  "480p_video": {
                    "width": 640,
                    "url_list": [
                      {
                        "url": "http://ic.snssdk.com/neihan/video/playback/1489235732.1/?video_id=d2a0fc9bb4784a6c983cd4a341df6d76&quality=480p&line=0&is_gif=0&device_platform=android"
                      },
                      {
                        "url": "http://ic.snssdk.com/neihan/video/playback/1489235732.1/?video_id=d2a0fc9bb4784a6c983cd4a341df6d76&quality=480p&line=1&is_gif=0&device_platform=android"
                      }
                    ],
                    "uri": "480p/d2a0fc9bb4784a6c983cd4a341df6d76",
                    "height": 360
                  },
                  "create_time": 1489234877,
                  "keywords": "",
                  "id": 57656588474,
                  "favorite_count": 0,
                  "go_detail_count": 738,
                  "m3u8_url": "",
                  "large_cover": {
                    "url_list": [
                      {
                        "url": "http://p1.pstatp.com/large/18b50004f8e236297f69.webp"
                      },
                      {
                        "url": "http://pb3.pstatp.com/large/18b50004f8e236297f69.webp"
                      },
                      {
                        "url": "http://pb3.pstatp.com/large/18b50004f8e236297f69.webp"
                      }
                    ],
                    "uri": "large/18b50004f8e236297f69"
                  },
                  "user_favorite": 0,
                  "share_type": 1,
                  "title": "大胃王密子君（异国风情餐）芝士就是力量，所以我要多吃一点！",
                  "user": {
                    "user_id": 6623500329,
                    "name": "大胃王密子君",
                    "followings": 0,
                    "user_verified": true,
                    "ugc_count": 41,
                    "avatar_url": "http://p3.pstatp.com/medium/e5900153ca3fe711770",
                    "followers": 270098,
                    "is_following": false,
                    "is_pro_user": false
                  },
                  "is_can_share": 1,
                  "category_type": 1,
                  "share_url": "http://m.neihanshequ.com/share/group/57656588474/?iid=3216590132&app=joke_essay",
                  "label": 4,
                  "content": "大胃王密子君（异国风情餐）芝士就是力量，所以我要多吃一点！",
                  "video_height": 360,
                  "comment_count": 28,
                  "cover_image_uri": "18b50004f8e236297f69",
                  "id_str": "57656588474",
                  "media_type": 3,
                  "share_count": 65,
                  "type": 2,
                  "category_id": 65,
                  "status": 102,
                  "has_comments": 0,
                  "publish_time": "",
                  "user_bury": 0,
                  "activity": {},
                  "status_desc": "已发表，粉丝第一时间可见",
                  "dislike_reason": [
                    {
                      "type": 1,
                      "id": 321,
                      "title": "美女"
                    },
                    {
                      "type": 1,
                      "id": 326,
                      "title": "美食"
                    },
                    {
                      "type": 1,
                      "id": 340,
                      "title": "猎奇"
                    },
                    {
                      "type": 1,
                      "id": 581,
                      "title": "PGC原创"
                    },
                    {
                      "type": 2,
                      "id": 65,
                      "title": "吧:搞笑视频"
                    },
                    {
                      "type": 4,
                      "id": 0,
                      "title": "内容重复"
                    },
                    {
                      "type": 3,
                      "id": 6623500329,
                      "title": "作者:大胃王密子君"
                    }
                  ],
                  "neihan_hot_start_time": "00-00-00",
                  "play_count": 9024,
                  "user_repin": 0,
                  "quick_comment": false,
                  "medium_cover": {
                    "url_list": [
                      {
                        "url": "http://p1.pstatp.com/w202/18b50004f8e236297f69.webp"
                      },
                      {
                        "url": "http://pb3.pstatp.com/w202/18b50004f8e236297f69.webp"
                      },
                      {
                        "url": "http://pb3.pstatp.com/w202/18b50004f8e236297f69.webp"
                      }
                    ],
                    "uri": "medium/18b50004f8e236297f69"
                  },
                  "neihan_hot_end_time": "00-00-00",
                  "user_digg": 0,
                  "video_width": 640,
                  "online_time": 1489234877,
                  "category_name": "搞笑视频",
                  "flash_url": "",
                  "category_visible": true,
                  "bury_count": 38,
                  "is_anonymous": false,
                  "repin_count": 0,
                  "is_neihan_hot": false,
                  "uri": "d2a0fc9bb4784a6c983cd4a341df6d76",
                  "is_public_url": 1,
                  "has_hot_comments": 0,
                  "allow_dislike": true,
                  "origin_video": {
                    "width": 640,
                    "url_list": [
                      {
                        "url": "http://ic.snssdk.com/neihan/video/playback/1489235732.1/?video_id=d2a0fc9bb4784a6c983cd4a341df6d76&quality=origin&line=0&is_gif=0&device_platform=android"
                      },
                      {
                        "url": "http://ic.snssdk.com/neihan/video/playback/1489235732.1/?video_id=d2a0fc9bb4784a6c983cd4a341df6d76&quality=origin&line=1&is_gif=0&device_platform=android"
                      }
                    ],
                    "uri": "origin/d2a0fc9bb4784a6c983cd4a341df6d76",
                    "height": 360
                  },
                  "cover_image_url": "",
                  "neihan_hot_link": {},
                  "group_id": 57656588474,
                  "is_video": 1,
                  "display_type": 0
                },
                "comments": [],
                "type": 1,
                "display_time": 1489235731,
                "online_time": 1489235731
              }
            ]
          }
        }

json 解析：

- `message`：成功时为 `success`
- `data`：具体数据信息
	- `has_more`：是否有更多，一般情况都为 `true`
	- `tip`：更新提示
	- `has_new_message`：是否有新的数据
	- `data`：具体数据
		- `group`：
			- `360p_video`：清晰度为360p的视频信息
			- `720p_video`：清晰度为720p的视频信息
			- `480p_video`：清晰度为480p的视频信息
			- `large_cover`：视频截图
			- `user`：作者信息
			- `play_count`：播放次数
			- `bury_count`：不顶次数
			- `digg_count`：点赞数量
			- `share_count`：转发数量
			- `content`：视频描述
		- `comments`：评论
			- `text`：热门评论
			- `user_name`：热门评论用户名
			- `comment_count`：评论数量
			- `digg_count`：热门评论点赞量

<h1 id="video">视频</h1>

url：同[推荐](#recommend)

拼接参数：同[推荐](#recommend)

url 示例：[`http://iu.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-104&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1463225362814&count=30&min_time=1489143837&screen_width=1450&do00le_col_mode=0&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120`](http://iu.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-104&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1463225362814&count=30&min_time=1489143837&screen_width=1450&do00le_col_mode=0&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120)

json 示例：同[推荐](#recommend)

json 解析：同[推荐](#recommend)

<h1 id="video_show">段友秀</h1>
url：http://iu.snssdk.com/neihan/stream/mix/v1/

拼接参数：同[推荐](#recommend)

url 示例：[`http://iu.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-301&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1463225362814&count=30&min_time=1489205906&screen_width=1450&do00le_col_mode=1&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120`](http://iu.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-301&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1463225362814&count=30&min_time=1489205906&screen_width=1450&do00le_col_mode=1&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120)

json 示例：同[推荐](#recommend)

json 解析：同[推荐](#recommend)

<h1 id="live">直播</h1>
url：http://hotsoon.snssdk.com/hotsoon/feed/

拼接参数：

- `type`：固定值 `recommend`
- `min_time`：固定值`0`
- `live_sdk_version`：直播 sdk，目前取值`170`
- 其他参数同[推荐](#recommend)，没有 `essence`，`content_type`，`message_cursor`，`am_longitude`，`am_latitude`，`am_city`，`am_loc_time`，`screen_width`，`do00le_col_mode`等参数，详情请见 url 示例

url 示例：[`http://hotsoon.snssdk.com/hotsoon/feed/?count=20&min_time=1489205906&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120`](http://hotsoon.snssdk.com/hotsoon/feed/?count=20&min_time=1489205906&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120)

json 示例：

	{
          "status_code": 0,
          "data": [
            {
              "type": 1,
              "rid": "201703112108510100030480291753B5",
              "data": {
                "status": 2,
                "user_count": 460,
                "stats": {
                  "money": 540,
                  "fan_ticket": 108,
                  "id": 6396222601244445442,
                  "total_user": 1428,
                  "id_str": "6396222601244445442"
                },
                "title": "35071926529",
                "finish_time": 1489237726,
                "enable_room_perspective": true,
                "share_url": "https://www.huoshan.com/share/room/6396222601244445442/",
                "id": 6396222601244445442,
                "stream_id": 6396222601387051777,
                "create_time": 1489236625,
                "cell_style": 3,
                "id_str": "6396222601244445442",
                "stream_url": {
                  "rtmp_pull_url": "http://pull-flv-l1-hs.pstatp.com/hudong/stream-6396222601387051777.flv",
                  "provider": 2,
                  "id": 6396222601387051777,
                  "id_str": "6396222601387051777"
                },
                "dynamic_cover_low": null,
                "owner": {
                  "avatar_large": {
                    "url_list": [
                      "http://p3.pstatp.com/live/1080x1080/123f0003b79889feafa6.webp",
                      "http://pb2.pstatp.com/live/1080x1080/123f0003b79889feafa6.webp",
                      "http://pb3.pstatp.com/live/1080x1080/123f0003b79889feafa6.webp"
                    ],
                    "uri": "1080x1080/123f0003b79889feafa6"
                  },
                  "signature": "",
                  "birthday_description": "未知年龄",
                  "birthday": 0,
                  "allow_others_download_video": true,
                  "stats": {
                    "record_count": 46,
                    "following_count": 2,
                    "total_duration": 112387,
                    "daily_income": 0,
                    "item_count": 0,
                    "daily_fan_ticket_count": 0,
                    "id_str": "55538074947",
                    "follower_count": 967,
                    "diamond_count": 0,
                    "id": 55538074947,
                    "diamond_consumed_count": 0
                  },
                  "avatar_thumb": {
                    "url_list": [
                      "http://p3.pstatp.com/live/100x100/123f0003b79889feafa6.webp",
                      "http://pb2.pstatp.com/live/100x100/123f0003b79889feafa6.webp",
                      "http://pb3.pstatp.com/live/100x100/123f0003b79889feafa6.webp"
                    ],
                    "uri": "100x100/123f0003b79889feafa6"
                  },
                  "constellation": "谜之星座",
                  "id": 55538074947,
                  "city": "上海",
                  "fan_ticket_count": 39547,
                  "verified": false,
                  "follow_status": 0,
                  "short_id": 82856196,
                  "level": 1,
                  "push_comment_status": true,
                  "nickname": "tansy甜",
                  "birthday_valid": false,
                  "verified_reason": "",
                  "pay_grade": {
                    "diamond_icon": {
                      "url_list": [
                        "http://p3.pstatp.com/obj/12400003aba3dd42e213",
                        "http://pb2.pstatp.com/obj/12400003aba3dd42e213",
                        "http://pb3.pstatp.com/obj/12400003aba3dd42e213"
                      ],
                      "uri": "12400003aba3dd42e213"
                    },
                    "next_name": "树叶",
                    "total_diamond_count": 9,
                    "name": "暂无",
                    "now_diamond": 9,
                    "level": 0,
                    "screen_chat_type": 1,
                    "next_icon": {
                      "url_list": [
                        "http://p3.pstatp.com/obj/12400003aae89daccd69",
                        "http://pb2.pstatp.com/obj/12400003aae89daccd69",
                        "http://pb3.pstatp.com/obj/12400003aae89daccd69"
                      ],
                      "uri": "12400003aae89daccd69"
                    },
                    "next_diamond": 10000,
                    "icon": {
                      "url_list": [
                        "http://p3.pstatp.com/obj/f2100085e55a62833b1",
                        "http://pb2.pstatp.com/obj/f2100085e55a62833b1",
                        "http://pb3.pstatp.com/obj/f2100085e55a62833b1"
                      ],
                      "uri": "f2100085e55a62833b1"
                    }
                  },
                  "id_str": "55538074947",
                  "avatar_medium": {
                    "url_list": [
                      "http://p3.pstatp.com/live/720x720/123f0003b79889feafa6.webp",
                      "http://pb2.pstatp.com/live/720x720/123f0003b79889feafa6.webp",
                      "http://pb3.pstatp.com/live/720x720/123f0003b79889feafa6.webp"
                    ],
                    "uri": "720x720/123f0003b79889feafa6"
                  },
                  "gender": 0,
                  "push_status": true
                },
                "stream_id_str": "6396222601387051777",
                "dynamic_cover": null
              },
              "tags": []
            }
          ],
          "extra": {
            "min_time": 0,
            "has_more": true,
            "now": 1489237731702,
            "total": 1,
            "max_time": 1489237731702
          }
        }

json 解析：基本同[推荐](#recommend)

<h1 id="picture">图片</h1>
url：同[推荐](#recommend)

拼接参数：同[推荐](#recommend)

url 示例：[`http://is.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-103&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1489226058493&count=30&min_time=1489226061&screen_width=1450&do00le_col_mode=0&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120`](http://is.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-103&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1489226058493&count=30&min_time=1489226061&screen_width=1450&do00le_col_mode=0&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120)

json 示例：基本同[推荐](#recommend)

json 解析：基本同[推荐](#recommend)

<h1 id="joke">段子</h1>
url：同[推荐](#recommend)

拼接参数：同[推荐](#recommend)

url 示例：[`http://is.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-102&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1489226058493&count=30&min_time=1489205901&screen_width=1450&do00le_col_mode=0&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120`](http://is.snssdk.com/neihan/stream/mix/v1/?mpic=1&webp=1&essence=1&content_type=-102&message_cursor=-1&am_longitude=110&am_latitude=120&am_city=%E5%8C%97%E4%BA%AC%E5%B8%82&am_loc_time=1489226058493&count=30&min_time=1489205901&screen_width=1450&do00le_col_mode=0&iid=3216590132&device_id=32613520945&ac=wifi&channel=360&aid=7&app_name=joke_essay&version_code=612&version_name=6.1.2&device_platform=android&ssmix=a&device_type=sansung&device_brand=xiaomi&os_api=28&os_version=6.10.1&uuid=326135942187625&openudid=3dg6s95rhg2a3dg5&manifest_version_code=612&resolution=1450*2800&dpi=620&update_version_code=6120)

json 示例：基本同[推荐](#recommend)

json 解析：基本同[推荐](#recommend)