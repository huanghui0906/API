请求参数中需要使用到城市 id，分为两种：一种是市级城市，[戳我查看 json](https://github.com/jokermonn/-Api/blob/master/Meizu_cities.json)；一种是县级城市，[戳我查看 json](https://github.com/jokermonn/-Api/blob/master/Meizu_city.json)

# OPPO 天气 #

url：http://i1.weather.oppomobile.com/chinaWeather/smChinaWeathersGz/ + 年月日时 + / + 城市 id + - + 年月日时 +.json.gz

该网址返回的并不是一个 json，而是一个压缩包，将压缩包中的文件解压后就是一个 json 文件，例如`大连市2017年08月08日09时的天气情况`的访问示例如下：

url 示例：[`i1.weather.oppomobile.com/chinaWeather/smChinaWeathersGz/2017080808/101070201-2017080809.json.gz`](i1.weather.oppomobile.com/chinaWeather/smChinaWeathersGz/2017080808/101070201-2017080809.json.gz)

json 示例：

	{
        "ts": "201708080806",
        "ver": "2.0",
        "info": {
            "city_id": "101070201",
            "city": "大连",
            "current": {
                "temp": "31",
                "weather": "多云",
                "wind_direction": "西南风",
                "wind_power": "2级",
                "humidity": "70",       // 湿度(％)
                "time": "08:06",
                "uv": "中等",
                "avg_pm25": "59",
                "pm_time": "2017-08-08 06:00:00",
                "aqi": "良",
                "body_temp": "31",      // 体感温度
                "pressure": "999",      // 气压(百帕)
                "visibility": "14000"   // 能见度(米)
            },
            "days": [{
                "date": "20170808",
                "day_weather": "多云",
                "day_temp": "37",
                "night_weather": "多云",
                "night_temp": "31",
                "sunrise": "05:41:00",
                "sunset": "19:03:00"
            }, {
                "date": "20170809",
                "day_weather": "中雨",
                "day_temp": "33",
                "night_weather": "小到中雨",
                "night_temp": "27",
                "sunrise": "05:42:00",
                "sunset": "19:02:00"
            }, {
                "date": "20170810",
                "day_weather": "阴",
                "day_temp": "32",
                "night_weather": "多云",
                "night_temp": "26",
                "sunrise": "05:42:00",
                "sunset": "19:01:00"
            }, {
                "date": "20170811",
                "day_weather": "多云",
                "day_temp": "35",
                "night_weather": "多云",
                "night_temp": "26",
                "sunrise": "05:43:00",
                "sunset": "19:00:00"
            }, {
                "date": "20170812",
                "day_weather": "小到中雨",
                "day_temp": "31",
                "night_weather": "雷阵雨",
                "night_temp": "26",
                "sunrise": "05:43:00",
                "sunset": "19:00:00"
            }, {
                "date": "20170813",
                "day_weather": "中雨",
                "day_temp": "31",
                "night_weather": "雷阵雨",
                "night_temp": "26",
                "sunrise": "05:44:00",
                "sunset": "18:59:00"
            }],
            "hours": [{
                "time": "2017-08-08 08:00:00",
                "weather": "多云",
                "temp": "33",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 09:00:00",
                "weather": "多云",
                "temp": "34",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 10:00:00",
                "weather": "多云",
                "temp": "35",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 11:00:00",
                "weather": "多云",
                "temp": "35",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 12:00:00",
                "weather": "多云",
                "temp": "36",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 13:00:00",
                "weather": "多云",
                "temp": "36",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 14:00:00",
                "weather": "多云",
                "temp": "37",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 15:00:00",
                "weather": "多云",
                "temp": "36",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 16:00:00",
                "weather": "多云",
                "temp": "35",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 17:00:00",
                "weather": "多云",
                "temp": "35",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 18:00:00",
                "weather": "多云",
                "temp": "34",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 19:00:00",
                "weather": "多云",
                "temp": "33",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 20:00:00",
                "weather": "多云",
                "temp": "32",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 21:00:00",
                "weather": "多云",
                "temp": "31",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 22:00:00",
                "weather": "多云",
                "temp": "31",
                "pcpratio": ""
            }, {
                "time": "2017-08-08 23:00:00",
                "weather": "多云",
                "temp": "31",
                "pcpratio": ""
            }, {
                "time": "2017-08-09 00:00:00",
                "weather": "多云",
                "temp": "30",
                "pcpratio": ""
            }, {
                "time": "2017-08-09 01:00:00",
                "weather": "多云",
                "temp": "30",
                "pcpratio": ""
            }, {
                "time": "2017-08-09 02:00:00",
                "weather": "多云",
                "temp": "30",
                "pcpratio": ""
            }, {
                "time": "2017-08-09 03:00:00",
                "weather": "多云",
                "temp": "29",
                "pcpratio": ""
            }, {
                "time": "2017-08-09 04:00:00",
                "weather": "雷阵雨",
                "temp": "28",
                "pcpratio": ""
            }, {
                "time": "2017-08-09 05:00:00",
                "weather": "多云",
                "temp": "29",
                "pcpratio": ""
            }, {
                "time": "2017-08-09 06:00:00",
                "weather": "多云",
                "temp": "30",
                "pcpratio": ""
            }, {
                "time": "2017-08-09 07:00:00",
                "weather": "多云",
                "temp": "30",
                "pcpratio": ""
            }],
            "warn": {
                "warn_name": "高温橙色",
                "warn_text": "大连市气象局08月07日09时45分继续发布高温橙色预警信号：24小时内我市大部分地区最高气温将升至37℃以上，请注意做好防暑降温工作。"
            }
        }
    }