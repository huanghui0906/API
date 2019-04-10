# 快递100 #

url：`http://www.kuaidi100.com/query`

拼接参数：

| 参数名称        | 参数取值           | 参数类型  |
| ------------- |:-------------:| -----:|
| type      | 快递码，请参考[快递100码](https://github.com/jokermonn/-Api/blob/master/ExpressDelivery100Code.json) | String |
| postid      | 快递单号      |   String |
| id | 未知，可为空      |    String |
| valicode | 未知，可为空      |    String |
| temp | 未知，可为空      |    String |

url 示例：[`https://www.kuaidi100.com/query?type=yuantong&postid=2234014274&id=1&valicode=&temp=`](https://www.kuaidi100.com/query?type=yuantong&postid=2234014274&id=1&valicode=&temp=)（`圆通`单号为`2234014274`的快递，不过快递已经过期了，所以显示不了信息，可以自行套用快递单号）

请求方式：`GET`

json 示例：

	{
	    "message": "ok",
	    "nu": "2234014274",
	    "ischeck": "1",
	    "condition": "F00",
	    "com": "yuantong",
	    "status": "200",
	    "state": "3",
	    "data": [
	      {
	        "time": "2016-11-26 19:10:30",
	        "ftime": "2016-11-26 19:10:30",
	        "context": "客户 签收人 : 本人签收 已签收  感谢使用圆通速递，期待再次为您服务",
	        "location": null
	      },
	      {
	        "time": "2016-11-22 18:19:03",
	        "ftime": "2016-11-22 18:19:03",
	        "context": "派送不成功，政府机关、学校等特殊单位，正在安排处理中。",
	        "location": null
	      },
	      {
	        "time": "2016-11-22 14:20:50",
	        "ftime": "2016-11-22 14:20:50",
	        "context": "北京大学 已签收",
	        "location": null
	      },
	      {
	        "time": "2016-11-22 10:33:25",
	        "ftime": "2016-11-22 10:33:25",
	        "context": "北京七道堰 已发出,下一站 北京大学",
	        "location": null
	      },
	      {
	        "time": "2016-11-22 10:27:47",
	        "ftime": "2016-11-22 10:27:47",
	        "context": "北京六和塔 已收入",
	        "location": null
	      },
	      {
	        "time": "2016-11-22 16:53:18",
	        "ftime": "2016-11-22 16:53:18",
	        "context": "浙江省五道口 已发出,下一站 北京转运中心",
	        "location": null
	      },
	      {
	        "time": "2016-11-22 00:33:51",
	        "ftime": "2016-11-22 00:33:51",
	        "context": "浙江省四码头 已收入",
	        "location": null
	      },
	      {
	        "time": "2016-11-11 23:53:09",
	        "ftime": "2016-11-11 23:53:09",
	        "context": "浙江省三里屯 已发出,下一站 浙江省金华市义乌市",
	        "location": null
	      },
	      {
	        "time": "2016-11-11 20:04:10",
	        "ftime": "2016-11-11 20:04:10",
	        "context": "浙江省二亩地 已打包",
	        "location": null
	      },
	      {
	        "time": "2016-11-1 18:11:16",
	        "ftime": "2016-11-11 18:11:16",
	        "context": "浙江省一条街 已揽收",
	        "location": null
	      }
	    ]
	  }

解析：

- `message`：`ok` 则表示没有问题，否则携带错误信息
- `nu`：运单号
- `ischeck`：`1`表示成功，`0`表示错误
- `com`：快递拼音
- `data`：具体到达的派送点，逆序
- `time`：到达时间
- `ftime`：到达时间
- `context`：到达地点具体信息
- `location`：到达地点，但取值一直为 `null`