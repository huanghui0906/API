<h2 id="weather">小米天气</h2>

url：https://weatherapi.market.xiaomi.com/wtr-v3/weather/all

拼接参数：

- `latitude`：纬度信息。可填固定值`0`
- `longitude`：经度信息。可填固定值`0`
- `locationKey`：`weathercn:` + 地区 `city_num`，见[数据库](https://github.com/jokermonn/-Api/blob/master/xiaomi_weather.db)中的 `city_num` 字段，例：`weathercn:101010100` 表北京
- `sign`：签名值，固定值`zUFJoAR2ZVrDy1vF3D07`
- `isGlobal`：固定值 `false`
- `locale`：固定值 `zh_cn`
- `days`：获取包括今日在内的几天内的数据。可不填，默认为`5`
- `romVersion`：可不填或者去除该参数
- `appVersion`：可不填或者去除该参数
- `alpha`：可不填或者去除该参数
- `device`：可不填或者去除该参数
- `modDevice`：可不填或者去除该参数

url 示例：[`https://weatherapi.market.xiaomi.com/wtr-v3/weather/all?latitude=110&longitude=112&isLocated=true&locationKey=weathercn%3A101010100&days=15&appKey=weather20151024&sign=zUFJoAR2ZVrDy1vF3D07&romVersion=7.2.16&appVersion=87&alpha=false&isGlobal=false&device=cancro&modDevice=&locale=zh_cn`](https://weatherapi.market.xiaomi.com/wtr-v3/weather/all?latitude=110&longitude=112&isLocated=true&locationKey=weathercn%3A101010100&days=15&appKey=weather20151024&sign=zUFJoAR2ZVrDy1vF3D07&romVersion=7.2.16&appVersion=87&alpha=false&isGlobal=false&device=cancro&modDevice=&locale=zh_cn) 或 [`https://weatherapi.market.xiaomi.com/wtr-v3/weather/all?latitude=110&longitude=112&locationKey=weathercn%3A101010100&days=15&appKey=weather20151024&sign=zUFJoAR2ZVrDy1vF3D07&isGlobal=false&locale=zh_cn`](https://weatherapi.market.xiaomi.com/wtr-v3/weather/all?latitude=110&longitude=112&locationKey=weathercn%3A101010100&days=15&appKey=weather20151024&sign=zUFJoAR2ZVrDy1vF3D07&isGlobal=false&locale=zh_cn)

json 示例：

	{
      "current": {
        "feelsLike": {
          "unit": "℃",
          "value": "22"
        },
        "humidity": {
          "unit": "%",
          "value": "56"
        },
        "pressure": {
          "unit": "mb",
          "value": "1010.4"
        },
        "pubTime": "2017-02-20T15:25:00+08:00",
        "temperature": {
          "unit": "℃",
          "value": "21"
        },
        "uvIndex": "2",
        "visibility": {
          "unit": "km",
          "value": ""
        },
        "weather": "0",
        "wind": {
          "direction": {
            "unit": "°",
            "value": "360"
          },
          "speed": {
            "unit": "km/h",
            "value": "3.0"
          }
        }
      },
      "forecastDaily": {
        "aqi": {
          "brandInfo": {
            "brands": [
              {
                "brandId": "caiyun",
                "logo": "http://f5.market.mi-img.com/download/MiSafe/0d2cde44e7d5b4a742b9846b8e5aaae62ebed7784/a.webp",
                "names": {
                  "en_US": "彩云天气",
                  "zh_TW": "彩雲天氣",
                  "zh_CN": "彩云天气"
                },
                "url": ""
              }
            ]
          },
          "pubTime": "2017-02-20T00:00:00+08:00",
          "status": 0,
          "value": [
            130,
            66,
            27,
            24,
            45
          ]
        },
        "precipitationProbability": {
          "status": 0,
          "value": [
            "8",
            "25",
            "73",
            "58",
            "6"
          ]
        },
        "pubTime": "2017-02-20T15:10:00+08:00",
        "status": 0,
        "sunRiseSet": {
          "status": 0,
          "value": [
            {
              "from": "2017-02-20T06:50:00+08:00",
              "to": "2017-02-20T18:10:00+08:00"
            },
            {
              "from": "2017-02-21T06:50:00+08:00",
              "to": "2017-02-21T18:11:00+08:00"
            },
            {
              "from": "2017-02-22T06:49:00+08:00",
              "to": "2017-02-22T18:11:00+08:00"
            },
            {
              "from": "2017-02-23T06:48:00+08:00",
              "to": "2017-02-23T18:12:00+08:00"
            },
            {
              "from": "2017-02-24T06:47:00+08:00",
              "to": "2017-02-24T18:13:00+08:00"
            }
          ]
        },
        "temperature": {
          "status": 0,
          "unit": "℃",
          "value": [
            {
              "from": "23",
              "to": "9"
            },
            {
              "from": "13",
              "to": "7"
            },
            {
              "from": "7",
              "to": "4"
            },
            {
              "from": "8",
              "to": "6"
            },
            {
              "from": "12",
              "to": "5"
            }
          ]
        },
        "weather": {
          "status": 0,
          "value": [
            {
              "from": "1",
              "to": "1"
            },
            {
              "from": "7",
              "to": "22"
            },
            {
              "from": "8",
              "to": "7"
            },
            {
              "from": "2",
              "to": "2"
            },
            {
              "from": "1",
              "to": "1"
            }
          ]
        },
        "wind": {
          "direction": {
            "status": 0,
            "unit": "°",
            "value": [
              {
                "from": "360",
                "to": "360"
              },
              {
                "from": "360",
                "to": "360"
              },
              {
                "from": "0",
                "to": "0"
              },
              {
                "from": "360",
                "to": "360"
              },
              {
                "from": "360",
                "to": "360"
              }
            ]
          },
          "speed": {
            "status": 0,
            "unit": "km/h",
            "value": [
              {
                "from": "3.0",
                "to": "3.0"
              },
              {
                "from": "0.0",
                "to": "0.0"
              },
              {
                "from": "24.0",
                "to": "24.0"
              },
              {
                "from": "0.0",
                "to": "0.0"
              },
              {
                "from": "0.0",
                "to": "0.0"
              }
            ]
          }
        }
      },
      "forecastHourly": {
        "aqi": {
          "brandInfo": {
            "brands": [
              {
                "brandId": "caiyun",
                "logo": "http://f5.market.mi-img.com/download/MiSafe/0d2cde44e7d5b4a742b9846b8e5aaae62ebed7784/a.webp",
                "names": {
                  "en_US": "彩云天气",
                  "zh_TW": "彩雲天氣",
                  "zh_CN": "彩云天气"
                },
                "url": ""
              }
            ]
          },
          "pubTime": "2017-02-20T16:00:00+08:00",
          "status": 0,
          "value": [
            50,
            47,
            47,
            47,
            50,
            55,
            59,
            63,
            64,
            61,
            52,
            43,
            35,
            31,
            29,
            27,
            27,
            26,
            24,
            23,
            22,
            20,
            20
          ]
        },
        "status": 0,
        "temperature": {
          "pubTime": "2017-02-20T16:00:00+08:00",
          "status": 0,
          "unit": "",
          "value": [
            18,
            15,
            13,
            11,
            10,
            10,
            10,
            10,
            10,
            10,
            10,
            9,
            9,
            8,
            8,
            8,
            8,
            10,
            10,
            11,
            12,
            13,
            13
          ]
        },
        "weather": {
          "pubTime": "2017-02-20T16:00:00+08:00",
          "status": 0,
          "value": [
            0,
            0,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            0,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            1,
            2,
            2,
            2,
            3
          ]
        }
      },
      "indices": {
        "indices": [
          {
            "type": "uvIndex",
            "value": "2"
          },
          {
            "type": "humidity",
            "value": "56"
          },
          {
            "type": "feelsLike",
            "value": "22"
          },
          {
            "type": "pressure",
            "value": "1010.4"
          },
          {
            "type": "carWash",
            "value": "1"
          },
          {
            "type": "sports",
            "value": "0"
          }
        ],
        "pubTime": "",
        "status": 0
      },
      "aqi": {
        "aqi": "130",
        "brandInfo": {
          "brands": [
            {
              "brandId": "CNEMC",
              "logo": "",
              "names": {
                "en_US": "CNEMC",
                "zh_TW": "中國環境監測總站",
                "zh_CN": "中国环境监测总站"
              },
              "url": ""
            }
          ]
        },
        "co": "1",
        "no2": "33",
        "o3": "89",
        "pm10": "159",
        "pm25": "99",
        "primary": "pm10",
        "pubTime": "2017-02-20T14:00:00+08:00",
        "so2": "31",
        "src": "中国环境监测总站",
        "status": 0
      },
      "alerts": [],
      "yesterday": {
        "aqi": "223",
        "date": "2017-02-19T12:10:00+08:00",
        "status": 0,
        "sunRise": "2017-02-19T06:51:00+08:00",
        "sunSet": "2017-02-19T18:09:00+08:00",
        "tempMax": "21",
        "tempMin": "10",
        "weatherEnd": "1",
        "weatherStart": "2",
        "windDircEnd": "360",
        "windDircStart": "360",
        "windSpeedEnd": "0.0",
        "windSpeedStart": "0.0"
      },
      "url": {
        "weathercn": "",
        "caiyun": ""
      },
      "brandInfo": {
        "brands": [
          {
            "brandId": "caiyun",
            "logo": "http://f5.market.mi-img.com/download/MiSafe/0d2cde44e7d5b4a742b9846b8e5aaae62ebed7784/a.webp",
            "names": {
              "en_US": "彩云天气",
              "zh_TW": "彩雲天氣",
              "zh_CN": "彩云天气"
            },
            "url": ""
          }
        ]
      }
    }

解析：

- `current`：当前天气状况
	- `feelsLike`：体感温度
	- `humidity`：相对空气湿度
	- `pressure`：气压
	- `temperature`：温度
	- `visibility`：能见度
	- `wind`：风信息
		- `unit`：该值单位
		- `value`：该值
	- `weather`：天气状况，[查看天气状况 json](https://github.com/jokermonn/-Api/blob/master/xiaomi_weather_status.json)
	- `pubTime`：更新时间
	- `uvIndex`：???
- `forecastDaily`：今日预测
	- `aqi`：空气质量相关
		- `pubTime`：更新时间
		- `value`：包括今日的五日内空气质量指数
	- `precipitationProbability`：降雨概率
		- `value`：包括今日的五日内降雨概率
	- `sunRiseSet`：日落日出相关
		- `from`：日出时间
		- `to`：日落时间
	- `temperature`：温度信息
		- `unit`：温度单位
		- `value`：包括今日的五日内温度信息
			- `from`：最高气温
			- `to`：最低气温
	- `weather`：天气状况，[查看天气状况 json](https://github.com/jokermonn/-Api/blob/master/xiaomi_weather_status.json)
	- `wind`：风信息
		- `direction`：风向
		- `speed`：风速
			- `unit`：该值单位
			- `from` 或 `to`：该值
- `forecastHourly`：今日小时预警
	- `aqi`：空气质量指数
	- `temperature`：温度信息
	- `weather`：天气状况，[查看天气状况 json](https://github.com/jokermonn/-Api/blob/master/xiaomi_weather_status.json)
		- `value`：今日二十四小时内的值
- `indices`：原型
- `aqi`：空气相关
	- `aqi`：空气质量指数
	- `co`：一氧化碳指数
	- `no2`：二氧化氮指数
	- `o3`：臭氧指数
	- `pm10`：pm10指数
	- `pm25`：pm2.5指数
	- `so2`：二氧化硫指数
	- `src`：来源地
- `yesterday`：昨日信息
	- `aqi`：空气质量指数
	- `date`：日期
	- `sunRise`：日出时间
	- `sunSet`：日落时间
	- `tempMax`：最高气温
	- `tempMin`：最低气温
	- `weatherEnd`：结束天气
	- `weatherStart`：起始天气
	- `windDircEnd`：结束风向
	- `windDircStart`：起始风向
	- `windSpeedEnd`：结束风速
	- `windSpeedStart`：起始风速