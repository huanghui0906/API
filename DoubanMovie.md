- [上映](#playing)
- [电影介绍](#introduce)
- [图片](#photo)
- [短评](#short_comments)
- [影评](#movie_comments)

<h2 id="playing">上映</h2>
url：https://api.douban.com/v2/movie/in_theaters

拼接参数：

- `apikey`：固定值`0b2bdeda43b5688921839c8ecb20399b`
- `city`：所在城市，例如`北京`、`上海`等
- `start`：分页使用，表示第几页
- `count`：分页使用，表示数量
- `client`：客户端信息。可为空
- `udid`：用户 id。可为空

url 示例：[`https://api.douban.com/v2/movie/in_theaters?apikey=0b2bdeda43b5688921839c8ecb20399b&city=%E5%8C%97%E4%BA%AC&start=0&count=100&client=somemessage&udid=dddddddddddddddddddddd`](https://api.douban.com/v2/movie/in_theaters?apikey=0b2bdeda43b5688921839c8ecb20399b&city=%E5%8C%97%E4%BA%AC&start=0&count=100&client=somemessage&udid=dddddddddddddddddddddd) 或 [`https://api.douban.com/v2/movie/in_theaters?apikey=0b2bdeda43b5688921839c8ecb20399b&city=%E5%8C%97%E4%BA%AC&start=0&count=100&client=&udid=`](https://api.douban.com/v2/movie/in_theaters?apikey=0b2bdeda43b5688921839c8ecb20399b&city=%E5%8C%97%E4%BA%AC&start=0&count=100&client=&udid=)

json 示例：

	{
      "count": 2,
      "start": 0,
      "total": 22,
      "subjects": [
        {
          "rating": {
            "max": 10,
            "average": 5.8,
            "details": {
              "1": 735,
              "3": 3826,
              "2": 1997,
              "5": 560,
              "4": 1612
            },
            "stars": "30",
            "min": 0
          },
          "genres": [
            "动作",
            "惊悚",
            "冒险"
          ],
          "title": "极限特工3：终极回归",
          "casts": [
            {
              "avatars": {
                "small": "https://img5.doubanio.com/img/celebrity/small/53186.jpg",
                "large": "https://img5.doubanio.com/img/celebrity/large/53186.jpg",
                "medium": "https://img5.doubanio.com/img/celebrity/medium/53186.jpg"
              },
              "name_en": "Vin Diesel",
              "name": "范·迪塞尔",
              "alt": "https://movie.douban.com/celebrity/1041020/",
              "id": "1041020"
            },
            {
              "avatars": {
                "small": "https://img3.doubanio.com/img/celebrity/small/10695.jpg",
                "large": "https://img3.doubanio.com/img/celebrity/large/10695.jpg",
                "medium": "https://img3.doubanio.com/img/celebrity/medium/10695.jpg"
              },
              "name_en": "Donnie Yen",
              "name": "甄子丹",
              "alt": "https://movie.douban.com/celebrity/1025194/",
              "id": "1025194"
            },
            {
              "avatars": {
                "small": "https://img5.doubanio.com/img/celebrity/small/4946.jpg",
                "large": "https://img5.doubanio.com/img/celebrity/large/4946.jpg",
                "medium": "https://img5.doubanio.com/img/celebrity/medium/4946.jpg"
              },
              "name_en": "Deepika Padukone",
              "name": "迪皮卡·帕度柯妮",
              "alt": "https://movie.douban.com/celebrity/1014002/",
              "id": "1014002"
            }
          ],
          "durations": [
            "107分钟"
          ],
          "collect_count": 36845,
          "mainland_pubdate": "2017-02-10",
          "has_video": false,
          "original_title": "xXx: The Return of Xander Cage",
          "subtype": "movie",
          "directors": [
            {
              "avatars": {
                "small": "https://img1.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
                "large": "https://img3.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
                "medium": "https://img1.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
              },
              "name_en": "D.J. Caruso",
              "name": "D·J·卡卢索",
              "alt": "https://movie.douban.com/celebrity/1014019/",
              "id": "1014019"
            }
          ],
          "pubdates": [
            "2017-01-05(墨西哥)",
            "2017-01-20(美国)",
            "2017-02-10(中国大陆)"
          ],
          "year": "2017",
          "images": {
            "small": "https://img5.doubanio.com/view/movie_poster_cover/ipst/public/p2410569976.jpg",
            "large": "https://img5.doubanio.com/view/movie_poster_cover/lpst/public/p2410569976.jpg",
            "medium": "https://img5.doubanio.com/view/movie_poster_cover/spst/public/p2410569976.jpg"
          },
          "alt": "https://movie.douban.com/subject/3230115/",
          "id": "3230115"
        },
        {
          "rating": {
            "max": 10,
            "average": 8.1,
            "details": {
              "1": 7,
              "3": 608,
              "2": 40,
              "5": 851,
              "4": 1280
            },
            "stars": "40",
            "min": 0
          },
          "genres": [
            "喜剧",
            "动画",
            "歌舞"
          ],
          "title": "欢乐好声音",
          "casts": [
            {
              "avatars": {
                "small": "https://img3.doubanio.com/img/celebrity/small/1392653727.04.jpg",
                "large": "https://img3.doubanio.com/img/celebrity/large/1392653727.04.jpg",
                "medium": "https://img3.doubanio.com/img/celebrity/medium/1392653727.04.jpg"
              },
              "name_en": "Matthew McConaughey",
              "name": "马修·麦康纳",
              "alt": "https://movie.douban.com/celebrity/1040511/",
              "id": "1040511"
            },
            {
              "avatars": {
                "small": "https://img1.doubanio.com/img/celebrity/small/49827.jpg",
                "large": "https://img1.doubanio.com/img/celebrity/large/49827.jpg",
                "medium": "https://img1.doubanio.com/img/celebrity/medium/49827.jpg"
              },
              "name_en": "Reese Witherspoon",
              "name": "瑞茜·威瑟斯彭",
              "alt": "https://movie.douban.com/celebrity/1031217/",
              "id": "1031217"
            },
            {
              "avatars": {
                "small": "https://img3.doubanio.com/img/celebrity/small/1354381657.24.jpg",
                "large": "https://img3.doubanio.com/img/celebrity/large/1354381657.24.jpg",
                "medium": "https://img3.doubanio.com/img/celebrity/medium/1354381657.24.jpg"
              },
              "name_en": "Seth MacFarlane",
              "name": "塞思·麦克法兰",
              "alt": "https://movie.douban.com/celebrity/1041123/",
              "id": "1041123"
            }
          ],
          "durations": [
            "108分钟"
          ],
          "collect_count": 6549,
          "mainland_pubdate": "2017-02-17",
          "has_video": false,
          "original_title": "Sing",
          "subtype": "movie",
          "directors": [
            {
              "avatars": {
                "small": "https://img1.doubanio.com/img/celebrity/small/21808.jpg",
                "large": "https://img1.doubanio.com/img/celebrity/large/21808.jpg",
                "medium": "https://img1.doubanio.com/img/celebrity/medium/21808.jpg"
              },
              "name_en": "Garth Jennings",
              "name": "加斯·詹宁斯",
              "alt": "https://movie.douban.com/celebrity/1303814/",
              "id": "1303814"
            },
            {
              "avatars": {
                "small": "https://img1.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
                "large": "https://img3.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
                "medium": "https://img1.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
              },
              "name_en": "Christophe Lourdelet",
              "name": "克里斯托夫·卢尔德莱",
              "alt": "https://movie.douban.com/celebrity/1366253/",
              "id": "1366253"
            }
          ],
          "pubdates": [
            "2016-09-11(多伦多电影节)",
            "2016-12-21(美国)",
            "2017-02-17(中国大陆)"
          ],
          "year": "2016",
          "images": {
            "small": "https://img5.doubanio.com/view/movie_poster_cover/ipst/public/p2411622136.jpg",
            "large": "https://img5.doubanio.com/view/movie_poster_cover/lpst/public/p2411622136.jpg",
            "medium": "https://img5.doubanio.com/view/movie_poster_cover/spst/public/p2411622136.jpg"
          },
          "alt": "https://movie.douban.com/subject/26354572/",
          "id": "26354572"
        }
      ],
      "title": "正在上映的电影-北京"
    }

解析：

- `count`：返回数量
- `start`：分页量
- `total`：数据库总数量
- `title`：返回数据相关信息
- `subjects`：具体电影信息
	- `rating`：排名信息
		- `max`：最高分
		- `average`：该电影得分
		- `details`：?
		- `stars`：星数
		- `min`：最低分
	- `genres`：电影分类
	- `title`：电影名
	- `casts`：原型
		- `avatars`：该演员剧照
		- `name_en`：该演员英文名
		- `name`：该演员中文名
		- `alt`：网页链接
		- `id`：演员 id
	- `duration`：电影时长
	- `collect_count`：多少人看过
	- `mainland_pubdate`：大陆上映时间
	- `has_video`：是否有资源
	- `original_title`：电影原名
	- `subtype`：固定值 `movie`
	- `directors`：导演信息
		- `avatars`：该导演剧照
		- `name_en`：该导演英文名
		- `name`：该导演中文名
		- `alt`：网页链接
		- `id`：导演 id
	- `pubdates`：各地上映日期
	- `year`：上映年
	- `images`：剧照
	- `alt`：网页链接
	- `id`：电影 id，用于[电影介绍](#introduce)

<h2 id="introduce">电影介绍</h2>

url：http://api.douban.com/v2/movie/subject/ + 电影 id（来源[上映](#playing)中的 `subjects` 中的 `id` 字段）

拼接参数：

- `apikey`：略，同[上映](#playing)
- `city`：略，同[上映](#playing)
- `client`：略，同[上映](#playing)
- `udid`：略，同[上映](#playing)

url 示例：[`http://api.douban.com/v2/movie/subject/26865690?apikey=0b2bdeda43b5688921839c8ecb20399b&city=%E5%8C%97%E4%BA%AC&client=something&udid=dddddddddddddddddddddd`](http://api.douban.com/v2/movie/subject/26865690?apikey=0b2bdeda43b5688921839c8ecb20399b&city=%E5%8C%97%E4%BA%AC&client=something&udid=dddddddddddddddddddddd) 或 [`http://api.douban.com/v2/movie/subject/26865690?apikey=0b2bdeda43b5688921839c8ecb20399b&city=%E5%8C%97%E4%BA%AC&client=&udid=`](http://api.douban.com/v2/movie/subject/26865690?apikey=0b2bdeda43b5688921839c8ecb20399b&city=%E5%8C%97%E4%BA%AC&client=&udid=)

json 示例：

	{
      "rating": {
        "max": 10,
        "average": 2.7,
        "details": {
          "1": 27,
          "3": 0,
          "2": 3,
          "5": 2,
          "4": 0
        },
        "stars": "15",
        "min": 0
      },
      "reviews_count": 8,
      "videos": [],
      "wish_count": 199,
      "original_title": "恐怖理发店",
      "blooper_urls": [],
      "collect_count": 347,
      "images": {
        "small": "http://img7.doubanio.com/view/movie_poster_cover/ipst/public/p2406903891.jpg",
        "large": "http://img7.doubanio.com/view/movie_poster_cover/lpst/public/p2406903891.jpg",
        "medium": "http://img7.doubanio.com/view/movie_poster_cover/spst/public/p2406903891.jpg"
      },
      "douban_site": "",
      "year": "2017",
      "popular_comments": [
        {
          "rating": {
            "max": 5,
            "value": 1,
            "min": 0
          },
          "useful_count": 0,
          "author": {
            "uid": "maggie841212",
            "avatar": "http://img7.doubanio.com/icon/u33450230-272.jpg",
            "signature": "一名拉玛西亚青年近卫军",
            "alt": "http://www.douban.com/people/maggie841212/",
            "id": "33450230",
            "name": "笑子大魔王"
          },
          "subject_id": "26865690",
          "content": "很不错的片子，评分还可以更低一些，并且有很大的空间",
          "created_at": "2017-02-03 23:06:17",
          "id": "1146632816"
        },
        {
          "rating": {
            "max": 5,
            "value": 1,
            "min": 0
          },
          "useful_count": 49,
          "author": {
            "uid": "150848902",
            "avatar": "http://img7.doubanio.com/icon/u150848902-2.jpg",
            "signature": "",
            "alt": "http://www.douban.com/people/150848902/",
            "id": "150848902",
            "name": "皮卡皮卡皮卡啾"
          },
          "subject_id": "26865690",
          "content": "第一部恐怖理发店，第二部恐怖美容院，第三部美甲店，第四部恐怖学校，第五部。。。可以一直拍下去，地老天荒",
          "created_at": "2017-01-06 13:12:37",
          "id": "1132879082"
        },
        {
          "rating": {
            "max": 5,
            "value": 0,
            "min": 0
          },
          "useful_count": 8,
          "author": {
            "uid": "99742301",
            "avatar": "http://img3.doubanio.com/icon/user_normal.jpg",
            "signature": "",
            "alt": "http://www.douban.com/people/99742301/",
            "id": "99742301",
            "name": "文艺不起来"
          },
          "subject_id": "26865690",
          "content": "自从看过三五部国产鬼片后 我再也不浪费钱了 现在的国产鬼片一定是用来洗钱的 妈蛋 侮辱观众智商  不看给差评",
          "created_at": "2017-01-09 23:28:18",
          "id": "1134858583"
        },
        {
          "rating": {
            "max": 5,
            "value": 1,
            "min": 0
          },
          "useful_count": 12,
          "author": {
            "uid": "88046629",
            "avatar": "http://img7.doubanio.com/icon/u88046629-4.jpg",
            "signature": "",
            "alt": "http://www.douban.com/people/88046629/",
            "id": "88046629",
            "name": "沉睡的真真真真"
          },
          "subject_id": "26865690",
          "content": "我没看过这篇也知道一分，我就是想来问问大家明知道不好看为什么还来看？？（标题写暂无评分是因为分实在太低了吗？）",
          "created_at": "2017-01-09 23:16:31",
          "id": "1134851423"
        }
      ],
      "alt": "https://movie.douban.com/subject/26865690/",
      "id": "26865690",
      "mobile_url": "https://movie.douban.com/subject/26865690/mobile",
      "photos_count": 27,
      "pubdate": "2017-01-06",
      "title": "恐怖理发店",
      "do_count": null,
      "has_video": false,
      "share_url": "http://m.douban.com/movie/subject/26865690",
      "seasons_count": null,
      "languages": [
        "汉语普通话"
      ],
      "schedule_url": "https://movie.douban.com/subject/26865690/cinema/",
      "writers": [
        {
          "avatars": {
            "small": "http://img3.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
            "large": "http://img7.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
            "medium": "http://img3.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
          },
          "name_en": "",
          "name": "纪然",
          "alt": "https://movie.douban.com/celebrity/1366595/",
          "id": "1366595"
        },
        {
          "avatars": {
            "small": "http://img3.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
            "large": "http://img7.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
            "medium": "http://img3.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
          },
          "name_en": "Shilei Lu",
          "name": "陆诗雷",
          "alt": "https://movie.douban.com/celebrity/1360707/",
          "id": "1360707"
        }
      ],
      "pubdates": [
        "2017-01-06(中国大陆)"
      ],
      "website": "",
      "tags": [
        "惊悚",
        "一个星都不想给！",
        "烂片",
        "烂片之中的烂片啊~",
        "垃圾",
        "呵呵",
        "MDZZ",
        "中国",
        "真的好恐怖啊！",
        "狗屎"
      ],
      "has_schedule": true,
      "durations": [
        "89分钟"
      ],
      "genres": [
        "爱情",
        "悬疑",
        "惊悚"
      ],
      "collection": null,
      "trailers": [
        {
          "medium": "http://img3.doubanio.com/img/trailer/medium/2395934439.jpg?",
          "title": "预告片：正式版 (中文字幕)",
          "subject_id": "26865690",
          "alt": "https://movie.douban.com/trailer/206905/",
          "small": "http://img3.doubanio.com/img/trailer/small/2395934439.jpg?",
          "resource_url": "http://vt1.doubanio.com/201702180820/994ce6a83c4d28a0eb8b93f8f71fe45a/view/movie/M/302060905.mp4",
          "id": "206905"
        },
        {
          "medium": "http://img3.doubanio.com/img/trailer/medium/2408079427.jpg?1482683047",
          "title": "预告片：终极版 (中文字幕)",
          "subject_id": "26865690",
          "alt": "https://movie.douban.com/trailer/209536/",
          "small": "http://img3.doubanio.com/img/trailer/small/2408079427.jpg?1482683047",
          "resource_url": "http://vt1.doubanio.com/201702180820/b556b239a4051f4fde74c18379d2beee/view/movie/M/302090536.mp4",
          "id": "209536"
        },
        {
          "medium": "http://img7.doubanio.com/img/trailer/medium/2406384532.jpg?",
          "title": "预告片：激情版 (中文字幕)",
          "subject_id": "26865690",
          "alt": "https://movie.douban.com/trailer/209076/",
          "small": "http://img7.doubanio.com/img/trailer/small/2406384532.jpg?",
          "resource_url": "http://vt1.doubanio.com/201702180820/ddaaf1f51061b7b16d84429b29e373b9/view/movie/M/302090076.mp4",
          "id": "209076"
        }
      ],
      "episodes_count": null,
      "trailer_urls": [
        "http://vt1.doubanio.com/201702180820/994ce6a83c4d28a0eb8b93f8f71fe45a/view/movie/M/302060905.mp4",
        "http://vt1.doubanio.com/201702180820/b556b239a4051f4fde74c18379d2beee/view/movie/M/302090536.mp4",
        "http://vt1.doubanio.com/201702180820/ddaaf1f51061b7b16d84429b29e373b9/view/movie/M/302090076.mp4"
      ],
      "has_ticket": true,
      "bloopers": [],
      "clip_urls": [],
      "current_season": null,
      "casts": [
        {
          "avatars": {
            "small": "http://img3.doubanio.com/img/celebrity/small/1403756298.69.jpg",
            "large": "http://img3.doubanio.com/img/celebrity/large/1403756298.69.jpg",
            "medium": "http://img3.doubanio.com/img/celebrity/medium/1403756298.69.jpg"
          },
          "name_en": "Guoer Yin",
          "name": "殷果儿",
          "alt": "https://movie.douban.com/celebrity/1340984/",
          "id": "1340984"
        },
        {
          "avatars": {
            "small": "http://img3.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
            "large": "http://img7.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
            "medium": "http://img3.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
          },
          "name_en": "Qingan Ren",
          "name": "任青安",
          "alt": "https://movie.douban.com/celebrity/1359164/",
          "id": "1359164"
        },
        {
          "avatars": {
            "small": "http://img7.doubanio.com/img/celebrity/small/1451209491.55.jpg",
            "large": "http://img7.doubanio.com/img/celebrity/large/1451209491.55.jpg",
            "medium": "http://img7.doubanio.com/img/celebrity/medium/1451209491.55.jpg"
          },
          "name_en": "SungGoo Kang",
          "name": "姜星丘",
          "alt": "https://movie.douban.com/celebrity/1353667/",
          "id": "1353667"
        },
        {
          "avatars": {
            "small": "http://img3.doubanio.com/img/celebrity/small/1478601324.49.jpg",
            "large": "http://img3.doubanio.com/img/celebrity/large/1478601324.49.jpg",
            "medium": "http://img3.doubanio.com/img/celebrity/medium/1478601324.49.jpg"
          },
          "name_en": "Jiamin Chen",
          "name": "陈嘉敏",
          "alt": "https://movie.douban.com/celebrity/1340988/",
          "id": "1340988"
        }
      ],
      "countries": [
        "中国大陆"
      ],
      "mainland_pubdate": "2017-01-06",
      "photos": [
        {
          "thumb": "http://img7.doubanio.com/view/photo/thumb/public/p2406383762.jpg",
          "image": "http://img7.doubanio.com/view/photo/photo/public/p2406383762.jpg",
          "cover": "http://img7.doubanio.com/view/photo/albumcover/public/p2406383762.jpg",
          "alt": "https://movie.douban.com/photos/photo/2406383762/",
          "id": "2406383762",
          "icon": "http://img7.doubanio.com/view/photo/icon/public/p2406383762.jpg"
        },
        {
          "thumb": "http://img3.doubanio.com/view/photo/thumb/public/p2411789707.jpg",
          "image": "http://img3.doubanio.com/view/photo/photo/public/p2411789707.jpg",
          "cover": "http://img3.doubanio.com/view/photo/albumcover/public/p2411789707.jpg",
          "alt": "https://movie.douban.com/photos/photo/2411789707/",
          "id": "2411789707",
          "icon": "http://img3.doubanio.com/view/photo/icon/public/p2411789707.jpg"
        },
        {
          "thumb": "http://img7.doubanio.com/view/photo/thumb/public/p2411789702.jpg",
          "image": "http://img7.doubanio.com/view/photo/photo/public/p2411789702.jpg",
          "cover": "http://img7.doubanio.com/view/photo/albumcover/public/p2411789702.jpg",
          "alt": "https://movie.douban.com/photos/photo/2411789702/",
          "id": "2411789702",
          "icon": "http://img7.doubanio.com/view/photo/icon/public/p2411789702.jpg"
        },
        {
          "thumb": "http://img7.doubanio.com/view/photo/thumb/public/p2411789693.jpg",
          "image": "http://img7.doubanio.com/view/photo/photo/public/p2411789693.jpg",
          "cover": "http://img7.doubanio.com/view/photo/albumcover/public/p2411789693.jpg",
          "alt": "https://movie.douban.com/photos/photo/2411789693/",
          "id": "2411789693",
          "icon": "http://img7.doubanio.com/view/photo/icon/public/p2411789693.jpg"
        },
        {
          "thumb": "http://img7.doubanio.com/view/photo/thumb/public/p2408074732.jpg",
          "image": "http://img7.doubanio.com/view/photo/photo/public/p2408074732.jpg",
          "cover": "http://img7.doubanio.com/view/photo/albumcover/public/p2408074732.jpg",
          "alt": "https://movie.douban.com/photos/photo/2408074732/",
          "id": "2408074732",
          "icon": "http://img7.doubanio.com/view/photo/icon/public/p2408074732.jpg"
        },
        {
          "thumb": "http://img7.doubanio.com/view/photo/thumb/public/p2408074723.jpg",
          "image": "http://img7.doubanio.com/view/photo/photo/public/p2408074723.jpg",
          "cover": "http://img7.doubanio.com/view/photo/albumcover/public/p2408074723.jpg",
          "alt": "https://movie.douban.com/photos/photo/2408074723/",
          "id": "2408074723",
          "icon": "http://img7.doubanio.com/view/photo/icon/public/p2408074723.jpg"
        },
        {
          "thumb": "http://img7.doubanio.com/view/photo/thumb/public/p2408074715.jpg",
          "image": "http://img7.doubanio.com/view/photo/photo/public/p2408074715.jpg",
          "cover": "http://img7.doubanio.com/view/photo/albumcover/public/p2408074715.jpg",
          "alt": "https://movie.douban.com/photos/photo/2408074715/",
          "id": "2408074715",
          "icon": "http://img7.doubanio.com/view/photo/icon/public/p2408074715.jpg"
        },
        {
          "thumb": "http://img7.doubanio.com/view/photo/thumb/public/p2406383761.jpg",
          "image": "http://img7.doubanio.com/view/photo/photo/public/p2406383761.jpg",
          "cover": "http://img7.doubanio.com/view/photo/albumcover/public/p2406383761.jpg",
          "alt": "https://movie.douban.com/photos/photo/2406383761/",
          "id": "2406383761",
          "icon": "http://img7.doubanio.com/view/photo/icon/public/p2406383761.jpg"
        },
        {
          "thumb": "http://img3.doubanio.com/view/photo/thumb/public/p2406383759.jpg",
          "image": "http://img3.doubanio.com/view/photo/photo/public/p2406383759.jpg",
          "cover": "http://img3.doubanio.com/view/photo/albumcover/public/p2406383759.jpg",
          "alt": "https://movie.douban.com/photos/photo/2406383759/",
          "id": "2406383759",
          "icon": "http://img3.doubanio.com/view/photo/icon/public/p2406383759.jpg"
        },
        {
          "thumb": "http://img7.doubanio.com/view/photo/thumb/public/p2395927790.jpg",
          "image": "http://img7.doubanio.com/view/photo/photo/public/p2395927790.jpg",
          "cover": "http://img7.doubanio.com/view/photo/albumcover/public/p2395927790.jpg",
          "alt": "https://movie.douban.com/photos/photo/2395927790/",
          "id": "2395927790",
          "icon": "http://img7.doubanio.com/view/photo/icon/public/p2395927790.jpg"
        }
      ],
      "summary": "位于深山小镇的理发店发生的一系列灵异奇闻，殷果儿、任青安、姜星丘等人陷入危难绝境中无法脱身，和理发店有关联的人物接连被惨绝杀害，血腥残暴引来人心惶惶，而抽丝剥茧之后的真相更加令人心惊胆战。",
      "clips": [],
      "subtype": "movie",
      "directors": [
        {
          "avatars": {
            "small": "http://img3.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
            "large": "http://img7.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
            "medium": "http://img3.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
          },
          "name_en": "Shilei Lu",
          "name": "陆诗雷",
          "alt": "https://movie.douban.com/celebrity/1360707/",
          "id": "1360707"
        }
      ],
      "comments_count": 191,
      "popular_reviews": [
        {
          "rating": {
            "max": 5,
            "value": 1,
            "min": 0
          },
          "title": "国产恐怖片，注定成烂片？",
          "subject_id": "26865690",
          "author": {
            "uid": "123404248",
            "avatar": "http://img7.doubanio.com/icon/u123404248-3.jpg",
            "signature": "",
            "alt": "http://www.douban.com/people/123404248/",
            "id": "123404248",
            "name": "世界奇妙物语"
          },
          "summary": "这一系列国产恐怖片太多，现在总结下国产电影拍摄门槛为什么这么低…… 1.找个导演，内地导演优先考虑(省钱)。 2.去网上热搜榜（也是经纪公司）上挑几个网红明星（省钱）。网红明星就像木偶一样被装扮上了。 3.去...",
          "alt": "https://movie.douban.com/review/8301338/",
          "id": "8301338"
        }
      ],
      "ratings_count": 318,
      "aka": [
        "Ghost in Barber's"
      ]
    }

解析：

- `videos`：片源
- `wish_count`：多少人想看
- `id`：电影 id
- `mobile_url`：移动端 url
- `languages`：电影语言
- `writers`：编剧
- `trailers`：原型
	- `title`：预告片名
	- `resource_url`：预告片源
	- `id`：预告片 id
- `has_ticket`：是否有票
- `photos`：剧照列表
- `popular_comments`：热门短评
	- `rating`：评分
		- `max`：最高分
		- `min`：最低分
		- `value`：该评论给分
	- `useful_count`：有用点赞量
	- `author`：评论者信息
		- `uid`：用户 id
		- `avatar`：用户头像
		- `signature`：用户个签
		- `alt`：用户主页链接
		- `id`：用户 id
		- `name`：用户名
	- `subject_id`：电影 id
	- `content`：评论内容
	- `create_at`：评论发表时间
	- `id`：评论 id
- `comments_count`：短评总量
- `summary`：电影介绍
- `popular_reviews`：热门影评
- `reviews_count`：影评总量

<h2 id="photo">图片</h2>

url：https://api.douban.com/v2/movie/subject/ + 电影 id + /photos

拼接参数：

- `apikey`：略，同[上映](#playing)
- `count`：返回图片数量
- `client`：略，同[上映](#playing)
- `udid`：略，同[上映](#playing)
- `start`：从第多少个开始

url 示例：[`https://api.douban.com/v2/movie/subject/26865690/photos?apikey=0b2bdeda43b5688921839c8ecb20399b&start=0&count=100&client=something&udid=dddddddddddddddddddddd`](https://api.douban.com/v2/movie/subject/26865690/photos?apikey=0b2bdeda43b5688921839c8ecb20399b&start=0&count=100&client=something&udid=dddddddddddddddddddddd) 或 [`https://api.douban.com/v2/movie/subject/26865690/photos?apikey=0b2bdeda43b5688921839c8ecb20399b&start=0&count=100&client=&udid=`](https://api.douban.com/v2/movie/subject/26865690/photos?apikey=0b2bdeda43b5688921839c8ecb20399b&start=0&count=100&client=&udid=)

json 示例：

	{
      "count": 1,
      "photos": [
        {
          "photos_count": 12,
          "thumb": "https://img3.doubanio.com/view/photo/thumb/public/p2406383762.jpg",
          "icon": "https://img3.doubanio.com/view/photo/icon/public/p2406383762.jpg",
          "author": {
            "uid": "122971558",
            "avatar": "https://img3.doubanio.com/icon/u122971558-2.jpg",
            "signature": "",
            "alt": "https://www.douban.com/people/122971558/",
            "id": "122971558",
            "name": "轮子"
          },
          "created_at": "2016-12-18 20:14:19",
          "album_id": "1638319514",
          "cover": "https://img3.doubanio.com/view/photo/albumcover/public/p2406383762.jpg",
          "id": "2406383762",
          "prev_photo": "2408074715",
          "album_url": "https://movie.douban.com/subject/26865690/photos",
          "comments_count": 2,
          "image": "https://img3.doubanio.com/view/photo/photo/public/p2406383762.jpg",
          "recs_count": 1,
          "position": 6,
          "alt": "https://movie.douban.com/photos/photo/2406383762/",
          "album_title": "恐怖理发店(26865690)",
          "next_photo": "2406383761",
          "subject_id": "26865690",
          "desc": ""
        }
      ],
      "total": 17,
      "start": 0,
      "subject": {
        "rating": {
          "max": 10,
          "average": 2.7,
          "details": {
            "1": 27,
            "3": 0,
            "2": 3,
            "5": 2,
            "4": 0
          },
          "stars": "15",
          "min": 0
        },
        "genres": [
          "爱情",
          "悬疑",
          "惊悚"
        ],
        "title": "恐怖理发店",
        "casts": [
          {
            "avatars": {
              "small": "https://img1.doubanio.com/img/celebrity/small/1403756298.69.jpg",
              "large": "https://img1.doubanio.com/img/celebrity/large/1403756298.69.jpg",
              "medium": "https://img1.doubanio.com/img/celebrity/medium/1403756298.69.jpg"
            },
            "name_en": "Guoer Yin",
            "name": "殷果儿",
            "alt": "https://movie.douban.com/celebrity/1340984/",
            "id": "1340984"
          },
          {
            "avatars": {
              "small": "https://img1.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
              "large": "https://img3.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
              "medium": "https://img1.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
            },
            "name_en": "Qingan Ren",
            "name": "任青安",
            "alt": "https://movie.douban.com/celebrity/1359164/",
            "id": "1359164"
          },
          {
            "avatars": {
              "small": "https://img3.doubanio.com/img/celebrity/small/1451209491.55.jpg",
              "large": "https://img3.doubanio.com/img/celebrity/large/1451209491.55.jpg",
              "medium": "https://img3.doubanio.com/img/celebrity/medium/1451209491.55.jpg"
            },
            "name_en": "SungGoo Kang",
            "name": "姜星丘",
            "alt": "https://movie.douban.com/celebrity/1353667/",
            "id": "1353667"
          }
        ],
        "durations": [
          "89分钟"
        ],
        "collect_count": 348,
        "mainland_pubdate": "2017-01-06",
        "has_video": false,
        "original_title": "恐怖理发店",
        "subtype": "movie",
        "directors": [
          {
            "avatars": {
              "small": "https://img1.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
              "large": "https://img3.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
              "medium": "https://img1.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
            },
            "name_en": "Shilei Lu",
            "name": "陆诗雷",
            "alt": "https://movie.douban.com/celebrity/1360707/",
            "id": "1360707"
          }
        ],
        "pubdates": [
          "2017-01-06(中国大陆)"
        ],
        "year": "2017",
        "images": {
          "small": "https://img3.doubanio.com/view/movie_poster_cover/ipst/public/p2406903891.jpg",
          "large": "https://img3.doubanio.com/view/movie_poster_cover/lpst/public/p2406903891.jpg",
          "medium": "https://img3.doubanio.com/view/movie_poster_cover/spst/public/p2406903891.jpg"
        },
        "alt": "https://movie.douban.com/subject/26865690/",
        "id": "26865690"
      }
    }

解析：

- `count`：返回数量
- `total`：数据库中图片总数
- `start`：从第多少个开始
- `subject`：该电影信息，与[电影介绍](#introduce)中差不多
- `photos`：图片信息
	- `thumb`：缩略图
	- `icon`：小图
	- `cover`：封面
	- `album_url`：网页链接
	- `image`：大图
	- `alt`：网页链接
	- `created_at`：创建日期
	- `album_title`：电影名

<h2 id="short_comments">短评</h2>

url：https://api.douban.com/v2/movie/subject/ + 电影 id + /reviews

拼接参数：

- `apikey`：略，同[上映](#playing)
- `count`：返回短评数量
- `client`：略，同[上映](#playing)
- `udid`：略，同[上映](#playing)
- `start`：从第多少个开始

url 示例：[`https://api.douban.com/v2/movie/subject/26865690/reviews?apikey=0b2bdeda43b5688921839c8ecb20399b&start=0&count=20&client=something&udid=dddddddddddddddddddddd`](https://api.douban.com/v2/movie/subject/26865690/reviews?apikey=0b2bdeda43b5688921839c8ecb20399b&start=0&count=20&client=something&udid=dddddddddddddddddddddd) 或 [`https://api.douban.com/v2/movie/subject/26865690/reviews?apikey=0b2bdeda43b5688921839c8ecb20399b&start=0&count=20&client=&udid=`](https://api.douban.com/v2/movie/subject/26865690/reviews?apikey=0b2bdeda43b5688921839c8ecb20399b&start=0&count=20&client=&udid=)

json 示例：

	{
      "count": 1,
      "reviews": [
        {
          "rating": {
            "max": 5,
            "value": 1,
            "min": 0
          },
          "useful_count": 21,
          "author": {
            "uid": "123404248",
            "avatar": "https://img3.doubanio.com/icon/u123404248-3.jpg",
            "signature": "",
            "alt": "https://www.douban.com/people/123404248/",
            "id": "123404248",
            "name": "世界奇妙物语"
          },
          "created_at": "2017-01-19 21:46:33",
          "title": "国产恐怖片，注定成烂片？",
          "updated_at": "2017-01-23 20:38:42",
          "share_url": "https://m.douban.com/movie/review/8301338",
          "summary": "这一系列国产恐怖片太多，现在总结下国产电影拍摄门槛为什么这么低…… 1.找个导演，内地导演优先考虑(省钱)。 2.去网上热搜榜（也是经纪公司）上挑几个网红明星（省钱）。网红明星就像木偶一样被装扮上了。 3.去...",
          "content": "这一系列国产恐怖片太多，现在总结下国产电影拍摄门槛为什么这么低……\r\n1.找个导演，内地导演优先考虑(省钱)。\r\n2.去网上热搜榜（也是经纪公司）上挑几个网红明星（省钱）。网红明星就像木偶一样被装扮上了。\r\n3.去影视学院和北漂南漂找上其他演员龙套（省钱）。\r\n4.租个摄制组，拍摄场地，演出服。（如上）\r\n5.找二三线编剧（如上）或自己操刀花上一星期把剧本凑到一部电影时长（参考网上剧本的对话） \r\n6.拍完，就剪辑成89分钟左右的电影长度。\r\n7.打包给营销公司，目标是各样马凳占领各搜索微博等阵地(电影蹭热度)。内容主题只要不反动不犯罪随便换，一小时出现在页面前3条。\r\n8.全国各地影院排档期上映了（电影院排片多于鸿毛，分成不少）。\r\n一路过来的只要遵循国家法律制度，避开行业不成文的禁区基本绿灯通过。哪怕是伦理道德，逻辑规律。不触犯法律要求也是可以放低的，导演就是上帝。\r\n\r\n最后总结：如果算是创作的话，除了原著用了脑力，搭上劳力，主要靠资源配置，就可以公放收钱了。 \r\n\r\nps:国产恐怖片的组成：15%的创作+65%的钱+20%的劳力=作品",
          "useless_count": 0,
          "comments_count": 1,
          "alt": "https://movie.douban.com/review/8301338/",
          "id": "8301338",
          "subject_id": "26865690"
        }
      ],
      "start": 0,
      "total": 8,
      "next_start": 1,
      "subject": {
        "rating": {
          "max": 10,
          "average": 2.7,
          "details": {
            "1": 27,
            "3": 0,
            "2": 3,
            "5": 2,
            "4": 0
          },
          "stars": "15",
          "min": 0
        },
        "genres": [
          "爱情",
          "悬疑",
          "惊悚"
        ],
        "title": "恐怖理发店",
        "casts": [
          {
            "avatars": {
              "small": "https://img1.doubanio.com/img/celebrity/small/1403756298.69.jpg",
              "large": "https://img1.doubanio.com/img/celebrity/large/1403756298.69.jpg",
              "medium": "https://img1.doubanio.com/img/celebrity/medium/1403756298.69.jpg"
            },
            "name_en": "Guoer Yin",
            "name": "殷果儿",
            "alt": "https://movie.douban.com/celebrity/1340984/",
            "id": "1340984"
          },
          {
            "avatars": {
              "small": "https://img1.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
              "large": "https://img3.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
              "medium": "https://img1.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
            },
            "name_en": "Qingan Ren",
            "name": "任青安",
            "alt": "https://movie.douban.com/celebrity/1359164/",
            "id": "1359164"
          },
          {
            "avatars": {
              "small": "https://img3.doubanio.com/img/celebrity/small/1451209491.55.jpg",
              "large": "https://img3.doubanio.com/img/celebrity/large/1451209491.55.jpg",
              "medium": "https://img3.doubanio.com/img/celebrity/medium/1451209491.55.jpg"
            },
            "name_en": "SungGoo Kang",
            "name": "姜星丘",
            "alt": "https://movie.douban.com/celebrity/1353667/",
            "id": "1353667"
          }
        ],
        "durations": [
          "89分钟"
        ],
        "collect_count": 348,
        "mainland_pubdate": "2017-01-06",
        "has_video": false,
        "original_title": "恐怖理发店",
        "subtype": "movie",
        "directors": [
          {
            "avatars": {
              "small": "https://img1.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
              "large": "https://img3.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
              "medium": "https://img1.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
            },
            "name_en": "Shilei Lu",
            "name": "陆诗雷",
            "alt": "https://movie.douban.com/celebrity/1360707/",
            "id": "1360707"
          }
        ],
        "pubdates": [
          "2017-01-06(中国大陆)"
        ],
        "year": "2017",
        "images": {
          "small": "https://img3.doubanio.com/view/movie_poster_cover/ipst/public/p2406903891.jpg",
          "large": "https://img3.doubanio.com/view/movie_poster_cover/lpst/public/p2406903891.jpg",
          "medium": "https://img3.doubanio.com/view/movie_poster_cover/spst/public/p2406903891.jpg"
        },
        "alt": "https://movie.douban.com/subject/26865690/",
        "id": "26865690"
      }
    }

解析：

- `count`：返回数量
- `start`：从第多少个开始
- `total`：总短评量
- `next_start`：下一评论位置
- `subject`：该电影信息，与[电影介绍](#introduce)中差不多
- `reviews`：短评内容
	- `rating`：评分
		- `max`：最高分
		- `min`：最低分
		- `value`：该评论给分
	- `useful_count`：有用点赞量
	- `author`：评论者信息
		- `uid`：用户 id
		- `avatar`：用户头像
		- `signature`：用户个签
		- `alt`：用户主页链接
		- `id`：用户 id
		- `name`：用户名
	- `subject_id`：电影 id
	- `content`：评论内容
	- `create_at`：评论发表时间
	- `id`：评论 id
	- `summary`：评论内容开头
	- `share_url`：网页链接

<h2 id="movie_comments">影评</h2>

url：https://api.douban.com/v2/movie/subject/26865690/comments

拼接参数：

- `apikey`：略，同[上映](#playing)
- `count`：返回影评数量
- `client`：略，同[上映](#playing)
- `udid`：略，同[上映](#playing)

url 示例：[`https://api.douban.com/v2/movie/subject/26865690/comments?apikey=0b2bdeda43b5688921839c8ecb20399b&count=20&client=something&udid=dddddddddddddddddddddd`](https://api.douban.com/v2/movie/subject/26865690/comments?apikey=0b2bdeda43b5688921839c8ecb20399b&count=20&client=something&udid=dddddddddddddddddddddd) 或 [`https://api.douban.com/v2/movie/subject/26865690/comments?apikey=0b2bdeda43b5688921839c8ecb20399b&count=20&client=&udid=`](https://api.douban.com/v2/movie/subject/26865690/comments?apikey=0b2bdeda43b5688921839c8ecb20399b&count=20&client=&udid=)

json 示例：

	{
      "count": 1,
      "comments": [
        {
          "rating": {
            "max": 5,
            "value": 1,
            "min": 0
          },
          "useful_count": 168,
          "author": {
            "uid": "62598926",
            "avatar": "https://img3.doubanio.com/icon/u62598926-1.jpg",
            "signature": "",
            "alt": "https://www.douban.com/people/62598926/",
            "id": "62598926",
            "name": "小曦讨厌下雨天"
          },
          "subject_id": "26865690",
          "content": "太恐怖了！吓得我从第十分钟开始就没敢睁眼睛，最后直接睡着了。",
          "created_at": "2017-01-06 15:16:12",
          "id": "1132938490"
        }
      ],
      "start": 0,
      "total": 191,
      "next_start": 1,
      "subject": {
        "rating": {
          "max": 10,
          "average": 2.7,
          "details": {
            "1": 27,
            "3": 0,
            "2": 3,
            "5": 2,
            "4": 0
          },
          "stars": "15",
          "min": 0
        },
        "genres": [
          "爱情",
          "悬疑",
          "惊悚"
        ],
        "title": "恐怖理发店",
        "casts": [
          {
            "avatars": {
              "small": "https://img1.doubanio.com/img/celebrity/small/1403756298.69.jpg",
              "large": "https://img1.doubanio.com/img/celebrity/large/1403756298.69.jpg",
              "medium": "https://img1.doubanio.com/img/celebrity/medium/1403756298.69.jpg"
            },
            "name_en": "Guoer Yin",
            "name": "殷果儿",
            "alt": "https://movie.douban.com/celebrity/1340984/",
            "id": "1340984"
          },
          {
            "avatars": {
              "small": "https://img1.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
              "large": "https://img3.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
              "medium": "https://img1.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
            },
            "name_en": "Qingan Ren",
            "name": "任青安",
            "alt": "https://movie.douban.com/celebrity/1359164/",
            "id": "1359164"
          },
          {
            "avatars": {
              "small": "https://img3.doubanio.com/img/celebrity/small/1451209491.55.jpg",
              "large": "https://img3.doubanio.com/img/celebrity/large/1451209491.55.jpg",
              "medium": "https://img3.doubanio.com/img/celebrity/medium/1451209491.55.jpg"
            },
            "name_en": "SungGoo Kang",
            "name": "姜星丘",
            "alt": "https://movie.douban.com/celebrity/1353667/",
            "id": "1353667"
          }
        ],
        "durations": [
          "89分钟"
        ],
        "collect_count": 348,
        "mainland_pubdate": "2017-01-06",
        "has_video": false,
        "original_title": "恐怖理发店",
        "subtype": "movie",
        "directors": [
          {
            "avatars": {
              "small": "https://img1.doubanio.com/f/movie/ca527386eb8c4e325611e22dfcb04cc116d6b423/pics/movie/celebrity-default-small.png",
              "large": "https://img3.doubanio.com/f/movie/63acc16ca6309ef191f0378faf793d1096a3e606/pics/movie/celebrity-default-large.png",
              "medium": "https://img1.doubanio.com/f/movie/8dd0c794499fe925ae2ae89ee30cd225750457b4/pics/movie/celebrity-default-medium.png"
            },
            "name_en": "Shilei Lu",
            "name": "陆诗雷",
            "alt": "https://movie.douban.com/celebrity/1360707/",
            "id": "1360707"
          }
        ],
        "pubdates": [
          "2017-01-06(中国大陆)"
        ],
        "year": "2017",
        "images": {
          "small": "https://img3.doubanio.com/view/movie_poster_cover/ipst/public/p2406903891.jpg",
          "large": "https://img3.doubanio.com/view/movie_poster_cover/lpst/public/p2406903891.jpg",
          "medium": "https://img3.doubanio.com/view/movie_poster_cover/spst/public/p2406903891.jpg"
        },
        "alt": "https://movie.douban.com/subject/26865690/",
        "id": "26865690"
      }
    }

解析：同[短评](#playing)