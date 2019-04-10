## 途牛火车票查询 ##

url： `http://huoche.tuniu.com/station_1708_2500`

请求方式：`GET`

请求参数：

- `r`：固定取值 `train/trainTicket/getTickets`

- `primary[departureDate]`：发车日期，`yyyy-MM-dd` 格式，例如：`2017-02-06`

- `primary[departureCityCode]`：出发站码，请参考[途牛站码 json](https://github.com/jokermonn/-Api/blob/master/TuniuStationCode.json)

- `primary[departureCityName]`：出发站名，请参考[途牛站码 json](https://github.com/jokermonn/-Api/blob/master/TuniuStationCode.json)

- `primary[arrivalCityCode]`：到达站码，请参考[途牛站码 json](https://github.com/jokermonn/-Api/blob/master/TuniuStationCode.json)

- `primary[arrivalCityName]`：到达站名，请参考[途牛站码 json](https://github.com/jokermonn/-Api/blob/master/TuniuStationCode.json)

- `start`：起始值，默认 `0`

- `limit`：数量，默认 `0`

ps：`start` 和 `limit` 是分页相关的值，如果都是默认取`0`的话则返回所有的信息

url 示例：[`http://huoche.tuniu.com/yii.php?r=train/trainTicket/getTickets&primary%5BdepartureDate%5D=2017-02-23&primary%5BdepartureCityCode%5D=200&primary%5BdepartureCityName%5D=%E5%8C%97%E4%BA%AC&primary%5BarrivalCityCode%5D=2500&primary%5BarrivalCityName%5D=%E4%B8%8A%E6%B5%B7&start=0&limit=0`](http://huoche.tuniu.com/yii.php?r=train/trainTicket/getTickets&primary%5BdepartureDate%5D=2017-02-23&primary%5BdepartureCityCode%5D=200&primary%5BdepartureCityName%5D=%E5%8C%97%E4%BA%AC&primary%5BarrivalCityCode%5D=2500&primary%5BarrivalCityName%5D=%E4%B8%8A%E6%B5%B7&start=0&limit=5)（`北京`到`上海`的`2017年02月13日`前十辆火车信息，`start` 取 `0`，`limit` 取 `5`）

json 示例：

	{
	  "code": 200,
	  "data": {
	    "count": 5,
	    "stores": null,
	    "trainTypeDetails": [
	      {
	        "trainType": 0,
	        "number": 36,
	        "trainTypeName": "G-高铁"
	      },
	      {
	        "trainType": 6,
	        "number": 1,
	        "trainTypeName": "其它"
	      },
	      {
	        "trainType": 4,
	        "number": 1,
	        "trainTypeName": "T-特快"
	      },
	      {
	        "trainType": 2,
	        "number": 3,
	        "trainTypeName": "D-动车"
	      }
	    ],
	    "streamId": null,
	    "remark": null,
	    "isFinish": null,
	    "lastTime": 0,
	    "expire": false,
	    "freshUrl": null,
	    "reserveUrls": null,
	    "crossURL": null,
	    "list": [
	      {
	        "trainId": 16101,
	        "trainNum": "G101",
	        "trainType": 0,
	        "trainTypeName": "高铁",
	        "departStationName": "北京南站",
	        "destStationName": "上海虹桥站",
	        "departDepartTime": "06:44",
	        "destArriveTime": "12:38",
	        "duration": 354,
	        "prices": [
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 0,
	            "price": 1748,
	            "stuPrice": null,
	            "promotionPrice": 1748,
	            "resId": 354865547,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "商务座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 2,
	            "price": 933,
	            "stuPrice": null,
	            "promotionPrice": 933,
	            "resId": 354865549,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "一等座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 3,
	            "price": 553,
	            "stuPrice": null,
	            "promotionPrice": 553,
	            "resId": 354865551,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "二等座"
	          }
	        ],
	        "durationDay": 1,
	        "departStationType": 0,
	        "destStationType": 1,
	        "saleStatus": 0,
	        "departStationId": 1175341,
	        "destStationId": 1175076,
	        "startSaleTime": "",
	        "canChooseSeat": 0,
	        "memo": "",
	        "departureCityCode": 200,
	        "arrivalCityCode": 2500,
	        "departureCityName": "北京",
	        "arrivalCityName": "上海",
	        "upOrDown": 0,
	        "trainStartDate": null,
	        "durationStr": "5小时54分钟",
	        "departStationTypeName": "ticketbtn",
	        "destStationTypeName": "ticketbtn",
	        "sellOut": 0
	      },
	      {
	        "trainId": 165,
	        "trainNum": "G5",
	        "trainType": 0,
	        "trainTypeName": "高铁",
	        "departStationName": "北京南站",
	        "destStationName": "上海虹桥站",
	        "departDepartTime": "07:00",
	        "destArriveTime": "11:55",
	        "duration": 295,
	        "prices": [
	          {
	            "leftNumber": 10,
	            "seatStatus": "",
	            "seat": 0,
	            "price": 1748,
	            "stuPrice": null,
	            "promotionPrice": 1748,
	            "resId": 1507056962,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "商务座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 2,
	            "price": 933,
	            "stuPrice": null,
	            "promotionPrice": 933,
	            "resId": 1507056963,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "一等座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 3,
	            "price": 553,
	            "stuPrice": null,
	            "promotionPrice": 553,
	            "resId": 1507056964,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "二等座"
	          }
	        ],
	        "durationDay": 1,
	        "departStationType": 0,
	        "destStationType": 1,
	        "saleStatus": 0,
	        "departStationId": 1175341,
	        "destStationId": 1175076,
	        "startSaleTime": "",
	        "canChooseSeat": 0,
	        "memo": "",
	        "departureCityCode": 200,
	        "arrivalCityCode": 2500,
	        "departureCityName": "北京",
	        "arrivalCityName": "上海",
	        "upOrDown": 0,
	        "trainStartDate": null,
	        "durationStr": "4小时55分钟",
	        "departStationTypeName": "ticketbtn",
	        "destStationTypeName": "ticketbtn",
	        "sellOut": 0
	      },
	      {
	        "trainId": 16105,
	        "trainNum": "G105",
	        "trainType": 0,
	        "trainTypeName": "高铁",
	        "departStationName": "北京南站",
	        "destStationName": "上海虹桥站",
	        "departDepartTime": "07:35",
	        "destArriveTime": "13:15",
	        "duration": 340,
	        "prices": [
	          {
	            "leftNumber": 14,
	            "seatStatus": "",
	            "seat": 0,
	            "price": 1748,
	            "stuPrice": null,
	            "promotionPrice": 1748,
	            "resId": 354865684,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "商务座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 2,
	            "price": 933,
	            "stuPrice": null,
	            "promotionPrice": 933,
	            "resId": 354865687,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "一等座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 3,
	            "price": 553,
	            "stuPrice": null,
	            "promotionPrice": 553,
	            "resId": 354865690,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "二等座"
	          }
	        ],
	        "durationDay": 1,
	        "departStationType": 0,
	        "destStationType": 1,
	        "saleStatus": 0,
	        "departStationId": 1175341,
	        "destStationId": 1175076,
	        "startSaleTime": "",
	        "canChooseSeat": 0,
	        "memo": "",
	        "departureCityCode": 200,
	        "arrivalCityCode": 2500,
	        "departureCityName": "北京",
	        "arrivalCityName": "上海",
	        "upOrDown": 0,
	        "trainStartDate": null,
	        "durationStr": "5小时40分钟",
	        "departStationTypeName": "ticketbtn",
	        "destStationTypeName": "ticketbtn",
	        "sellOut": 0
	      },
	      {
	        "trainId": 1611,
	        "trainNum": "G11",
	        "trainType": 0,
	        "trainTypeName": "高铁",
	        "departStationName": "北京南站",
	        "destStationName": "上海虹桥站",
	        "departDepartTime": "08:00",
	        "destArriveTime": "13:10",
	        "duration": 310,
	        "prices": [
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 0,
	            "price": 1748,
	            "stuPrice": null,
	            "promotionPrice": 1748,
	            "resId": 354865337,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "商务座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 2,
	            "price": 933,
	            "stuPrice": null,
	            "promotionPrice": 933,
	            "resId": 354865338,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "一等座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 3,
	            "price": 553,
	            "stuPrice": null,
	            "promotionPrice": 553,
	            "resId": 354865339,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "二等座"
	          }
	        ],
	        "durationDay": 1,
	        "departStationType": 0,
	        "destStationType": 1,
	        "saleStatus": 0,
	        "departStationId": 1175341,
	        "destStationId": 1175076,
	        "startSaleTime": "",
	        "canChooseSeat": 0,
	        "memo": "",
	        "departureCityCode": 200,
	        "arrivalCityCode": 2500,
	        "departureCityName": "北京",
	        "arrivalCityName": "上海",
	        "upOrDown": 0,
	        "trainStartDate": null,
	        "durationStr": "5小时10分钟",
	        "departStationTypeName": "ticketbtn",
	        "destStationTypeName": "ticketbtn",
	        "sellOut": 0
	      },
	      {
	        "trainId": 16107,
	        "trainNum": "G107",
	        "trainType": 0,
	        "trainTypeName": "高铁",
	        "departStationName": "北京南站",
	        "destStationName": "上海虹桥站",
	        "departDepartTime": "08:05",
	        "destArriveTime": "13:38",
	        "duration": 333,
	        "prices": [
	          {
	            "leftNumber": 13,
	            "seatStatus": "",
	            "seat": 0,
	            "price": 1748,
	            "stuPrice": null,
	            "promotionPrice": 1748,
	            "resId": 354865873,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "商务座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 2,
	            "price": 933,
	            "stuPrice": null,
	            "promotionPrice": 933,
	            "resId": 354865874,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "一等座"
	          },
	          {
	            "leftNumber": 99,
	            "seatStatus": "有",
	            "seat": 3,
	            "price": 553,
	            "stuPrice": null,
	            "promotionPrice": 553,
	            "resId": 354865875,
	            "detail": [],
	            "priceMemo": null,
	            "seatName": "二等座"
	          }
	        ],
	        "durationDay": 1,
	        "departStationType": 0,
	        "destStationType": 1,
	        "saleStatus": 0,
	        "departStationId": 1175341,
	        "destStationId": 1175076,
	        "startSaleTime": "",
	        "canChooseSeat": 0,
	        "memo": "",
	        "departureCityCode": 200,
	        "arrivalCityCode": 2500,
	        "departureCityName": "北京",
	        "arrivalCityName": "上海",
	        "upOrDown": 0,
	        "trainStartDate": null,
	        "durationStr": "5小时33分钟",
	        "departStationTypeName": "ticketbtn",
	        "destStationTypeName": "ticketbtn",
	        "sellOut": 0
	      }
	    ],
	    "allTrainType": {
	      "list": [
	        {
	          "trainType": 0,
	          "trainTypeName": "G-高铁",
	          "trainTypeCode": "G",
	          "link": "http://huoche.tuniu.com/station_200_2500/G"
	        }
	      ],
	      "departureCityName": "北京",
	      "arrivalCityName": "上海"
	    },
	    "filter": {
	      "filter": [
	        {
	          "id": "trainTypes",
	          "name": "车型",
	          "pros": [
	            {
	              "id": 0,
	              "name": "G-高铁"
	            },
	            {
	              "id": 2,
	              "name": "D-动车"
	            },
	            {
	              "id": 4,
	              "name": "T-特快"
	            },
	            {
	              "id": 6,
	              "name": "其它"
	            }
	          ]
	        },
	        {
	          "id": "seats",
	          "name": "座席",
	          "pros": [
	            {
	              "id": 0,
	              "name": "商务座"
	            },
	            {
	              "id": 2,
	              "name": "一等座"
	            },
	            {
	              "id": 3,
	              "name": "二等座"
	            },
	            {
	              "id": 4,
	              "name": "高级软卧"
	            },
	            {
	              "id": 5,
	              "name": "软卧"
	            },
	            {
	              "id": 6,
	              "name": "硬卧"
	            },
	            {
	              "id": 8,
	              "name": "硬座"
	            }
	          ]
	        },
	        {
	          "id": "departureStations",
	          "name": "出发车站",
	          "pros": [
	            {
	              "name": "北京南站",
	              "id": 1175341
	            },
	            {
	              "name": "北京站",
	              "id": 1175342
	            }
	          ]
	        },
	        {
	          "id": "arrivalStations",
	          "name": "到达车站",
	          "pros": [
	            {
	              "name": "上海站",
	              "id": 1175075
	            },
	            {
	              "name": "上海虹桥站",
	              "id": 1175076
	            }
	          ]
	        },
	        {
	          "id": "departureTimes",
	          "name": "出发时段",
	          "pros": [
	            {
	              "id": "6-12",
	              "name": "6-12点"
	            },
	            {
	              "id": "12-18",
	              "name": "12-18点"
	            },
	            {
	              "id": "18-24",
	              "name": "18-24点"
	            }
	          ]
	        },
	        {
	          "id": "arrivalTimes",
	          "name": "到达时段",
	          "pros": [
	            {
	              "id": "6-12",
	              "name": "6-12点"
	            },
	            {
	              "id": "12-18",
	              "name": "12-18点"
	            },
	            {
	              "id": "18-24",
	              "name": "18-24点"
	            }
	          ]
	        },
	        {
	          "id": "departStationTypes",
	          "name": "是否始发",
	          "pros": [
	            {
	              "id": 0,
	              "name": "始发"
	            }
	          ]
	        }
	      ],
	      "sort": [
	        {
	          "type": 2,
	          "id": 1,
	          "name": "出发时间"
	        },
	        {
	          "type": 2,
	          "id": 3,
	          "name": "运行时间"
	        },
	        {
	          "type": 2,
	          "id": 2,
	          "name": "到达时间"
	        },
	        {
	          "type": 2,
	          "id": 4,
	          "name": "价格"
	        }
	      ]
	    }
	  }
	}

解析：

- `trainTypeDetails`：车辆类型信息
- `trainType`：车辆类型码
- `number`：该类车辆数量
- `trainTypeName`：车辆类型码对应信息
- `trainId`：车辆 id
- `trainNum`：车辆车次号
- `departStationName`：出发站
- `destStationName`：到达站
- `departDepartTime`：发车时间
- `destArriveTime`：到达时间
- `duration`：历时（以分钟为单位）
- `price`：座位价格信息
- `leftNumber`：剩余票量（`99`是表示票量充足）
- `seatStatus`：`有`或为空，票量充足情况下为`有`，反之为空
- `stuPrice`：学生价，但是途牛网好像一直获取为 `null`
- `resId`：座位对应 id
- `detail`：座位具体细节
- `seat`：座位类型码
- `price`：价格
- `promotionPrice`：折扣价
- `seatName`：座位类型
- `durationDay`：历时天数
- `departStationType`：???
- `destStationType`：???
- `saleStatus`：???
- `departStationId`：出发车站 id
- `destStationId`：到达车站 id
- `startSaleTime`：售票时间
- `canChooseSeat`：是否可以选择座位，`0`表示不可以
- `departureCityCode`：出发站城市码
- `arrivalCityCode`：到达站城市码
- `departureCityName`：出发站城市
- `arrivalCityName`：到达站城市
- `trainStartDate`：???
- `durationStr`：耗时
- `sellOut`：是否售罄，`0`表没有售罄
- `filter`：过滤信息
- `id`：过滤参数名
- `name`：名称
- `pros`：参数及参数取值