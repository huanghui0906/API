# 快递网 #

[戳我查看快递码](https://github.com/jokermonn/-Api/blob/master/ExpressDeliveryCode.json)

url：`http://www.kuaidi.com/index-ajaxselectcourierinfo- + 运单号 + - + 快递码 + .html`

url 示例：[`http://www.kuaidi.com/index-ajaxselectcourierinfo-1202247993797-yunda.html`](http://www.kuaidi.com/index-ajaxselectcourierinfo-1202247993797-yunda.html)（`韵达`单号为`1202247993797`的快递）

json 示例：

	{
	  "success": true,
	  "ico": "/data/upload/201407/yd_logo.gif",
	  "phone": "95546",
	  "url": "http://www.yundaex.com",
	  "status": 6,
	  "companytype": "yunda",
	  "nu": "1202247993797",
	  "company": "韵达快递",
	  "reason": "",
	  "data": [
	    {
	      "time": "2016-08-21 19:47:14",
	      "context": "到达：贵州都匀市公司 由 已签收 签收"
	    },
	    {
	      "time": "2016-08-21 09:45:36",
	      "context": "到达：贵州都匀市公司 指定：小围寨分部(1111-1111111) 派送"
	    },
	    {
	      "time": "2016-08-20 06:32:38",
	      "context": "到达：贵州贵阳分拨中心 发往：贵州都匀市公司"
	    },
	    {
	      "time": "2016-08-20 06:17:24",
	      "context": "到达：贵州贵阳分拨中心 上级站点：福建晋江分拨中心"
	    },
	    {
	      "time": "2016-08-18 21:48:53",
	      "context": "到达：福建晋江分拨中心 发往：贵州贵阳分拨中心"
	    },
	    {
	      "time": "2016-08-18 21:46:25",
	      "context": "到达：福建晋江分拨中心"
	    },
	    {
	      "time": "2016-08-18 08:30:44",
	      "context": "到达：福建市场部台江服务部 已收件"
	    },
	    {
	      "time": "2016-08-18 06:48:19",
	      "context": "到达：福建市场部台江服务部 发往：贵州贵阳分拨中心"
	    },
	    {
	      "time": "2016-08-18 06:37:54",
	      "context": "到达：福建市场部台江服务部 已收件"
	    },
	    {
	      "time": "2016-08-18 05:51:57",
	      "context": "到达：福建市场部台江服务部 已收件"
	    }
	  ],
	  "time": "",
	  "rank": "2.3",
	  "exceed": "",
	  "timeused": "--"
	}

解析：

- `success`：是否成功，取值 `true` 或 `false`
- `status`：`6`表示成功，`0`表示失败
- `companytype`：快递公司拼音
- `nu`：快递单号
- `company`：快递公司
- `data`：具体数据
- `time`：收货时间
- `context`：收货信息
- `rank`：快递公司评分
- `timeused`：花费时间（以天数为单位）
- `exceed`：超重???
