请求参数中需要使用到城市 id，分为两种：一种是市级城市，[戳我查看 json](https://github.com/jokermonn/-Api/blob/master/Meizu_cities.json)；一种是县级城市，[戳我查看 json](https://github.com/jokermonn/-Api/blob/master/Meizu_city.json)

<h2 id="weather">魅族天气</h2>

url：http://aider.meizu.com/app/weather/listWeather?cityIds= + 城市 id

ps：注意，该 url 可携带多个 `cityIds` 参数以此一次性返回多个城市的天气信息

url 示例：[`http://aider.meizu.com/app/weather/listWeather?cityIds=101240101`](http://aider.meizu.com/app/weather/listWeather?cityIds=101240101)

json 示例：

	{
      "code": "200",
      "message": "",
      "redirect": "",
      "value": [
        {
          "alarms": [],
          "city": "南昌",
          "cityid": 101240101,
          "indexes": [
            {
              "abbreviation": "zs",
              "alias": "",
              "content": "温度不高，其他各项气象条件适宜，中暑机率极低。",
              "level": "无",
              "name": "中暑指数"
            },
            {
              "abbreviation": "ys",
              "alias": "",
              "content": "天气较好，不会降水，因此您可放心出门，无须带雨伞。",
              "level": "不带伞",
              "name": "雨伞指数"
            },
            {
              "abbreviation": "yh",
              "alias": "",
              "content": "天气较好，和恋人一起徜徉于熙攘人群中或漫步于柔软草地上，都是不错的主意哦。",
              "level": "适宜",
              "name": "约会指数"
            },
            {
              "abbreviation": "yd",
              "alias": "",
              "content": "天气较好，但考虑气温较低，推荐您进行室内运动，若户外适当增减衣物并注意防晒。",
              "level": "较适宜",
              "name": "运动指数"
            },
            {
              "abbreviation": "xq",
              "alias": "",
              "content": "天气较好，温度适宜，心情会不错，学习、工作效率较高。",
              "level": "较好",
              "name": "心情指数"
            },
            {
              "abbreviation": "xc",
              "alias": "",
              "content": "不宜洗车，未来24小时内有雨，如果在此期间洗车，雨水和路上的泥水可能会再次弄脏您的爱车。",
              "level": "不宜",
              "name": "洗车指数"
            },
            {
              "abbreviation": "wc",
              "alias": "",
              "content": "温度未达到风寒所需的低温，稍作防寒准备即可。",
              "level": "无",
              "name": "风寒指数"
            },
            {
              "abbreviation": "uv",
              "alias": "",
              "content": "属弱紫外线辐射天气，无需特别防护。若长期在户外，建议涂擦SPF在8-12之间的防晒护肤品。",
              "level": "最弱",
              "name": "紫外线强度指数"
            },
            {
              "abbreviation": "tr",
              "alias": "",
              "content": "天气较好，但丝毫不会影响您出行的心情。温度适宜又有微风相伴，适宜旅游。",
              "level": "适宜",
              "name": "旅游指数"
            },
            {
              "abbreviation": "pp",
              "alias": "",
              "content": "风力不大，建议用中性保湿型霜类化妆品，无需选用防晒化妆品。",
              "level": "保湿",
              "name": "化妆指数"
            },
            {
              "abbreviation": "pl",
              "alias": "",
              "content": "气象条件对空气污染物稀释、扩散和清除无明显影响，易感人群应适当减少室外活动时间。",
              "level": "中",
              "name": "空气污染扩散条件指数"
            },
            {
              "abbreviation": "pk",
              "alias": "",
              "content": "天气不错，风略小，选择合适的地点，还是较适宜放风筝的。",
              "level": "较适宜",
              "name": "放风筝指数"
            },
            {
              "abbreviation": "pj",
              "alias": "",
              "content": "适量的饮用啤酒可能会更增加您舒适的感觉，但要注意千万不要过量呦。",
              "level": "较适宜",
              "name": "啤酒指数"
            },
            {
              "abbreviation": "nl",
              "alias": "",
              "content": "有风，且有降水，会给您的出行带来很大的不便，建议就近或最好在室内进行夜生活。",
              "level": "较不适宜",
              "name": "夜生活指数"
            },
            {
              "abbreviation": "mf",
              "alias": "",
              "content": "出门前要在头发上涂上含防晒和滋润成分的护发品，或备好遮阳帽、遮阳伞，以减轻太阳对头发的直接照射。",
              "level": "一般",
              "name": "美发指数"
            },
            {
              "abbreviation": "ls",
              "alias": "",
              "content": "天气不错，适宜晾晒。赶紧把久未见阳光的衣物搬出来吸收一下太阳的味道吧！",
              "level": "适宜",
              "name": "晾晒指数"
            },
            {
              "abbreviation": "lk",
              "alias": "",
              "content": "天气较好，路面比较干燥，路况较好。",
              "level": "干燥",
              "name": "路况指数"
            },
            {
              "abbreviation": "jt",
              "alias": "",
              "content": "天气较好，路面干燥，交通气象条件良好，车辆可以正常行驶。",
              "level": "良好",
              "name": "交通指数"
            },
            {
              "abbreviation": "hc",
              "alias": "",
              "content": "白天天气较好，适宜划船或嬉玩各种水上运动。",
              "level": "适宜",
              "name": "划船指数"
            },
            {
              "abbreviation": "gm",
              "alias": "",
              "content": "昼夜温差很大，易发生感冒，请注意适当增减衣服，加强自我防护避免感冒。",
              "level": "易发",
              "name": "感冒指数"
            },
            {
              "abbreviation": "gj",
              "alias": "",
              "content": "天气较好，在这种天气里去逛街，既可畅快地放松身心，又会有很多意外收获，真是无比惬意。",
              "level": "适宜",
              "name": "逛街指数"
            },
            {
              "abbreviation": "fs",
              "alias": "",
              "content": "属弱紫外辐射天气，长期在户外，建议涂擦SPF在8-12之间的防晒护肤品。",
              "level": "弱",
              "name": "防晒指数"
            },
            {
              "abbreviation": "dy",
              "alias": "",
              "content": "白天风和日丽，适宜垂钓，渺渺蓝天，悠悠白云将陪伴你度过愉快的垂钓时光。",
              "level": "适宜",
              "name": "钓鱼指数"
            },
            {
              "abbreviation": "ct",
              "alias": "",
              "content": "建议着薄外套、开衫牛仔衫裤等服装。年老体弱者应适当添加衣物，宜着夹克衫、薄毛衣等。",
              "level": "较舒适",
              "name": "穿衣指数"
            },
            {
              "abbreviation": "co",
              "alias": "",
              "content": "白天不太热也不太冷，风力不大，相信您在这样的天气条件下，应会感到比较清爽和舒适。",
              "level": "舒适",
              "name": "舒适度指数"
            },
            {
              "abbreviation": "cl",
              "alias": "",
              "content": "天气不错，空气清新，是您晨练的大好时机，建议不同年龄段的人们积极参加户外健身活动。",
              "level": "适宜",
              "name": "晨练指数"
            },
            {
              "abbreviation": "ag",
              "alias": "",
              "content": "天气条件极不易诱发过敏，可放心外出，享受生活。",
              "level": "极不易发",
              "name": "过敏指数"
            },
            {
              "abbreviation": "ac",
              "alias": "",
              "content": "您将感到很舒适，一般不需要开启空调。",
              "level": "较少开启",
              "name": "空调开启指数"
            }
          ],
          "pm25": {
            "advice": "",
            "aqi": "83",
            "citycount": 1767,
            "cityrank": 54,
            "co": "0.0",
            "color": "",
            "level": "0",
            "no2": "0",
            "o3": "0",
            "pm10": "21",
            "pm25": "61",
            "quality": "良",
            "so2": "0",
            "timestamp": "0",
            "upDateTime": "2017-02-18 15:00:00"
          },
          "provinceName": "江西省",
          "realtime": {
            "img": "1",
            "sD": "67",
            "sendibleTemp": "14",
            "temp": "14",
            "time": "2017-02-18 16:00:00",
            "wD": "东风",
            "wS": "2级",
            "weather": "多云",
            "ziwaixian": "N/A"
          },
          "weatherDetailsInfo": {
            "publishTime": "2017-02-18 16:00:00",
            "weather3HoursDetailsInfos": [
              {
                "endTime": "2017-02-18 17:00:00",
                "highestTemperature": "15",
                "img": "1",
                "isRainFall": "无降水",
                "lowerestTemperature": "15",
                "precipitation": "0",
                "startTime": "2017-02-18 14:00:00",
                "wd": "无持续风向",
                "weather": "多云",
                "ws": "0级"
              },
              {
                "endTime": "2017-02-18 20:00:00",
                "highestTemperature": "15",
                "img": "1",
                "isRainFall": "无降水",
                "lowerestTemperature": "12",
                "precipitation": "0",
                "startTime": "2017-02-18 17:00:00",
                "wd": "无持续风向",
                "weather": "多云",
                "ws": "0级"
              },
              {
                "endTime": "2017-02-18 23:00:00",
                "highestTemperature": "12",
                "img": "1",
                "isRainFall": "无降水",
                "lowerestTemperature": "10",
                "precipitation": "0",
                "startTime": "2017-02-18 20:00:00",
                "wd": "无持续风向",
                "weather": "多云",
                "ws": "0级"
              },
              {
                "endTime": "2017-02-19 02:00:00",
                "highestTemperature": "10",
                "img": "1",
                "isRainFall": "无降水",
                "lowerestTemperature": "8",
                "precipitation": "0",
                "startTime": "2017-02-18 23:00:00",
                "wd": "无持续风向",
                "weather": "多云",
                "ws": "0级"
              },
              {
                "endTime": "2017-02-19 05:00:00",
                "highestTemperature": "8",
                "img": "1",
                "isRainFall": "无降水",
                "lowerestTemperature": "8",
                "precipitation": "0",
                "startTime": "2017-02-19 02:00:00",
                "wd": "无持续风向",
                "weather": "多云",
                "ws": "0级"
              },
              {
                "endTime": "2017-02-19 08:00:00",
                "highestTemperature": "9",
                "img": "1",
                "isRainFall": "无降水",
                "lowerestTemperature": "8",
                "precipitation": "0",
                "startTime": "2017-02-19 05:00:00",
                "wd": "无持续风向",
                "weather": "多云",
                "ws": "0级"
              },
              {
                "endTime": "2017-02-19 11:00:00",
                "highestTemperature": "13",
                "img": "1",
                "isRainFall": "无降水",
                "lowerestTemperature": "9",
                "precipitation": "0",
                "startTime": "2017-02-19 08:00:00",
                "wd": "无持续风向",
                "weather": "多云",
                "ws": "0级"
              },
              {
                "endTime": "2017-02-19 14:00:00",
                "highestTemperature": "20",
                "img": "1",
                "isRainFall": "无降水",
                "lowerestTemperature": "13",
                "precipitation": "0",
                "startTime": "2017-02-19 11:00:00",
                "wd": "无持续风向",
                "weather": "多云",
                "ws": "0级"
              },
              {
                "endTime": "2017-02-19 17:00:00",
                "highestTemperature": "20",
                "img": "1",
                "isRainFall": "无降水",
                "lowerestTemperature": "15",
                "precipitation": "0",
                "startTime": "2017-02-19 14:00:00",
                "wd": "无持续风向",
                "weather": "多云",
                "ws": "0级"
              }
            ]
          },
          "weathers": [
            {
              "date": "2017-02-18",
              "img": "1",
              "sun_down_time": "18:08",
              "sun_rise_time": "06:51",
              "temp_day_c": "16",
              "temp_day_f": "60.8",
              "temp_night_c": "8",
              "temp_night_f": "46.4",
              "wd": "无持续风向",
              "weather": "多云",
              "week": "星期六",
              "ws": "0级"
            },
            {
              "date": "2017-02-19",
              "img": "1",
              "sun_down_time": "18:09",
              "sun_rise_time": "06:51",
              "temp_day_c": "21",
              "temp_day_f": "69.8",
              "temp_night_c": "9",
              "temp_night_f": "48.2",
              "wd": "无持续风向",
              "weather": "多云",
              "week": "星期日",
              "ws": "0级"
            },
            {
              "date": "2017-02-20",
              "img": "1",
              "sun_down_time": "18:10",
              "sun_rise_time": "06:50",
              "temp_day_c": "24",
              "temp_day_f": "75.2",
              "temp_night_c": "10",
              "temp_night_f": "50.0",
              "wd": "无持续风向",
              "weather": "多云",
              "week": "星期一",
              "ws": "0级"
            },
            {
              "date": "2017-02-21",
              "img": "3",
              "sun_down_time": "18:10",
              "sun_rise_time": "06:49",
              "temp_day_c": "17",
              "temp_day_f": "62.6",
              "temp_night_c": "9",
              "temp_night_f": "48.2",
              "wd": "无持续风向",
              "weather": "阵雨",
              "week": "星期二",
              "ws": "0级"
            },
            {
              "date": "2017-02-22",
              "img": "7",
              "sun_down_time": "18:11",
              "sun_rise_time": "06:48",
              "temp_day_c": "11",
              "temp_day_f": "51.8",
              "temp_night_c": "6",
              "temp_night_f": "42.8",
              "wd": "北风",
              "weather": "小雨",
              "week": "星期三",
              "ws": "1级"
            },
            {
              "date": "2017-02-23",
              "img": "2",
              "sun_down_time": "18:12",
              "sun_rise_time": "06:47",
              "temp_day_c": "8",
              "temp_day_f": "46.4",
              "temp_night_c": "4",
              "temp_night_f": "39.2",
              "wd": "北风",
              "weather": "阴",
              "week": "星期四",
              "ws": "1级"
            },
            {
              "date": "2017-02-17",
              "img": "1",
              "sun_down_time": "18:08",
              "sun_rise_time": "06:52",
              "temp_day_c": "21",
              "temp_day_f": "69.8",
              "temp_night_c": "10",
              "temp_night_f": "50.0",
              "wd": "无持续风向",
              "weather": "多云",
              "week": "星期五",
              "ws": "1级"
            }
          ]
        }
      ]
    }

解析：

- `code`：访问成功时返回`200`
- `message`：错误时将携带错误信息
- `redirect`：???
- `value`：所有城市天气信息列表
	- `alarms`：天气预警???
	- `city`：该城市名称
	- `cityid`：该城市 id
	- `indexes`：一些预警信息
	- `pm25`：pm2.5 信息
		- `advice`：建议
		- `aqi`：空气质量指数
		- `citycount`：城市总量
		- `cityrank`：空气质量指数超越城市百分比
		- `pm10`：pm10 指数
		- `pm25`：pm2.5 指数
		- `quality`：空气质量
		- `upDateTime`：更新时间
	- `provinceName`：所属省份
	- `realtime`：其他指数
		- `sD`：空气湿度百分比
		- `sendibleTemp` 或 `temp`：体感温度
		- `time`：更新时间
		- `wD`：风向
		- `wS`：风力大小
		- `weather`：天气情况
	- `weatherDetailsInfo`：天气情况细节
		- `publishTime`：更新时间
		- `weather3HoursDetailsInfos`：未来天气情况细节（以三个小时为单位）
			- `endTime`：时间间隔结束点
			- `highestTemperature`：最高温度
			- `isRainFall`：是否下雨
			- `lowerestTemperature`：最低温度
			- `precipitation`：降雨量
			- `startTime`：时间间隔起始点
			- `wd`：风向
			- `weather`：天气情况
			- `ws`：风力大小
	- `weathers`：最近几日天气情况
		- `data`：日期
		- `sun_down_time`：日落时间
		- `sun_rise_time`：日出时间
		- `temp_day_c`：白天气温，摄氏度为单位
		- `temp_night_c`：夜间气温，摄氏度为单位
		- `temp_night_f`：夜间气温，华氏度为单位
		- `temp_day_f`：白天气温，华氏度为单位
		- `wd`：风向
		- `weather`：天气情况
		- `week`：星期几
		- `ws`：风力大小