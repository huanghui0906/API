# 图虫 #
- [推荐](#recommend)
	- [图片细节](#photo)
- [发现](#discover)
	- [标签](#tag)
	- [内容](#content)

<h2 id="recommend">推荐</h2>

url：`https://api.tuchong.com/feed-app`

拼接参数：

- `os_api`：操作系统 api。可为空
- `device_type`：设备类型。可为空
- `device_platform`：设备平台。可为空
- `ssmix`：固定值 `a`。可为空
- `manifest_version_code`：版本号去除小数点，例如 `232`。可为空
- `dpi`：设备 dpi。可为空
- `abflag`：固定值`0`。可为空
- `uuid`：一个长度为15的纯数字字符串。可为空
- `version_code`：版本号去除小数点，例如 `232`。可为空
- `app_name`：固定值 `tuchong`。可为空
- `version_name`：版本号。可为空
- `openudid`：一个长度为16的小写字母和数字混合字符串。可为空
- `resolution`：设备宽高像素。可为空
- `os_version`：操作系统版本号。可为空
- `ac`：设备环境，例如 `wifi`。可为空
- `aid`：固定值`0`。可为空
- `page`：翻页值。从 1 开始。需要搭配 json 中的 `pose_id` 字段使用。可为空
- `post_id`：如果是第一页则不需要添加该字段。否则，需要加上该字段，该字段的值为上一页最后一个 json 中的 `post_id` 值
- `type`：如果是第一页则是 `refresh`，如果是加载更多，则是 `loadmore`。可为空

url 示例：

第一页加载 ：
[`
https://api.tuchong.com/feed-app?os_api=22&device_type=MI&device_platform=android&ssmix=a&manifest_version_code=232&dpi=400&abflag=0&uuid=651384659521356&version_code=232&app_name=tuchong&version_name=2.3.2&openudid=65143269dafd1f3a5&resolution=1280*1000&os_version=5.8.1&ac=wifi&aid=0&page=1&type=refresh`](https://api.tuchong.com/feed-app?os_api=22&device_type=MI&device_platform=android&ssmix=a&manifest_version_code=232&dpi=400&abflag=0&uuid=651384659521356&version_code=232&app_name=tuchong&version_name=2.3.2&openudid=65143269dafd1f3a5&resolution=1280*1000&os_version=5.8.1&ac=wifi&aid=0&page=1&type=refresh)

第二页加载：
[`https://api.tuchong.com/feed-app?os_api=22&device_type=MI&device_platform=android&ssmix=a&manifest_version_code=232&dpi=400&abflag=0&uuid=651384659521356&version_code=232&app_name=tuchong&version_name=2.3.2&openudid=65143269dafd1f3a5&post_id=13828311&resolution=1280*1000&os_version=5.0.1&ac=wifi&aid=0&page=2&type=loadmore`](https://api.tuchong.com/feed-app?os_api=22&device_type=MI&device_platform=android&ssmix=a&manifest_version_code=232&dpi=400&abflag=0&uuid=651384659521356&version_code=232&app_name=tuchong&version_name=2.3.2&openudid=65143269dafd1f3a5&post_id=13828311&resolution=1280*1000&os_version=5.0.1&ac=wifi&aid=0&page=2&type=loadmore)

url 示例：

	{
      "is_history": true,
      "counts": 1,
      "feedList": [
        {
          "post_id": 13828311,
          "type": "multi-photo",
          "url": "https://tuchong.com/1107603/13828311/",
          "site_id": "1107603",
          "author_id": "1107603",
          "published_at": "2016-12-11 08:14:40",
          "excerpt": "海纳百川有容乃大,壁立千仞无欲则刚",
          "favorites": 537,
          "comments": 27,
          "delete": false,
          "update": false,
          "content": "海纳百川有容乃大,壁立千仞无欲则刚",
          "title": "海纳百川有容乃大",
          "image_count": 1,
          "images": [
            {
              "img_id": 21522551,
              "user_id": 1107603,
              "title": "001",
              "excerpt": "",
              "width": 2500,
              "height": 1646,
              "description": ""
            }
          ],
          "tags": [
            "Kase卡色现金大奖赛",
            "风光",
            "色彩",
            "佳能",
            "自然",
            "江苏"
          ],
          "event_tags": [
            "Kase卡色现金大奖赛"
          ],
          "data_type": "post",
          "created_at": "2016-12-11 08:14:40",
          "sites": [],
          "site": {
            "site_id": "1107603",
            "type": "user",
            "name": "燕子Photography",
            "domain": "",
            "description": "自然风光摄影师；图虫网资深摄影师；江苏摄影家协会会员；A色艺术摄影教学机构辅导老师；热爱风光摄影和城市建筑摄影（微信：jiangyan-741006）（新浪微博：燕子Photography）",
            "followers": 3662,
            "url": "https://tuchong.com/1107603/",
            "icon": "https://s1.tuchong.com/sites/110/1107603/logo_small.jpg?4",
            "verified": false,
            "verified_type": 0,
            "verified_reason": "",
            "verifications": 0,
            "verification_list": []
          },
          "recom_type": "",
          "rqt_id": "",
          "is_favorite": false
        }
      ],
      "message": "添加成功",
      "more": true,
      "result": "SUCCESS"
    }

json 解析：

- `message`、`result`：等字段表示请求成功
- `counts`：返回数据长度
- `feedList`：详细数据
	- `post_id`：用于翻页
	- `type`：`multi-photo`表组图
	- `url`：网页链接
	- `published_at`：发表日期
	- `favorites`：多少人喜爱
	- `comments`：多少人评论
	- `images`：图片宽高等信息
		- `img_id`：用于查看[图片细节](#photo_details)
		- `user_id`：https://photo.tuchong.com/ + user_id +/f/ + img_id 即图片地址，例：[`https://photo.tuchong.com/1673709/f/25389444.jpg`](https://photo.tuchong.com/1673709/f/25389444.jpg)
	- `title`：图片名称
	- `tags`：图片标签
	- `site`：作者信息
		- `name`：作者名
		- `description`：作者个签
		- `url`：作者主页
		- `icon`：作者头像
		- `followers`：
		- `followers`：粉丝数量

<h3 id="photo">图片细节</h3>

url：https://api.tuchong.com/images/ + `img_id`([推荐](#recommend) json 中的字段) + /exif

拼接参数：

同[推荐](#recommend)

url 示例：[`https://api.tuchong.com/images/8223054/exif?os_api=28&device_type=MI&device_platform=android&ssmix=a&manifest_version_code=232&dpi=440&abflag=0&uuid=012345678912345&version_code=232&app_name=tuchong&version_name=2.3.2&openudid=adf123dfa45d3fa2&resolution=1280*1000&os_version=5.8.1&ac=wifi&aid=0`](https://api.tuchong.com/images/8223054/exif?os_api=28&device_type=MI&device_platform=android&ssmix=a&manifest_version_code=232&dpi=440&abflag=0&uuid=012345678912345&version_code=232&app_name=tuchong&version_name=2.3.2&openudid=adf123dfa45d3fa2&resolution=1280*1000&os_version=5.8.1&ac=wifi&aid=0)

json 示例：

	{
      "exif": {
        "摘要": [
          {
            "desc": "器材",
            "content": "HUAWEI P9 LEICA DUAL CAMERA"
          },
          {
            "desc": "模式",
            "content": "曝光模式:Program AE, 测光模式:Multi-segment, 曝光补偿:0"
          },
          {
            "desc": "曝光",
            "content": "光圈:2.2, 快门:1/38秒, ISO1250"
          },
          {
            "desc": "焦距",
            "content": "4.5 mm (35 mm equivalent: 27.0 mm), 视角:67.4 deg"
          },
          {
            "desc": "色彩",
            "content": "白平衡:Auto, 色彩空间:sRGB"
          },
          {
            "desc": "时间",
            "content": "2017-03-11 16:49:07.450586"
          },
          {
            "desc": "地点",
            "content": "29 deg 56' 15.00\" N, 121 deg 48' 20.00\" E"
          }
        ],
        "File": [
          {
            "tagid": null,
            "tagname": "FileType",
            "desc": "FileType",
            "content": "JPEG"
          },
          {
            "tagid": null,
            "tagname": "FileTypeExtension",
            "desc": "FileTypeExtension",
            "content": "jpg"
          },
          {
            "tagid": null,
            "tagname": "MIMEType",
            "desc": "MIMEType",
            "content": "image/jpeg"
          },
          {
            "tagid": null,
            "tagname": "ExifByteOrder",
            "desc": "ExifByteOrder",
            "content": "Big-endian (Motorola, MM)"
          },
          {
            "tagid": null,
            "tagname": "ImageWidth",
            "desc": "ImageWidth",
            "content": "3584"
          },
          {
            "tagid": null,
            "tagname": "ImageHeight",
            "desc": "ImageHeight",
            "content": "2341"
          },
          {
            "tagid": null,
            "tagname": "EncodingProcess",
            "desc": "EncodingProcess",
            "content": "Baseline DCT, Huffman coding"
          },
          {
            "tagid": null,
            "tagname": "BitsPerSample",
            "desc": "BitsPerSample",
            "content": "8"
          },
          {
            "tagid": null,
            "tagname": "ColorComponents",
            "desc": "ColorComponents",
            "content": "3"
          },
          {
            "tagid": null,
            "tagname": "YCbCrSubSampling",
            "desc": "YCbCrSubSampling",
            "content": "YCbCr4:2:0 (2 2)"
          }
        ],
        "IFD0": [
          {
            "tagid": null,
            "tagname": "BitsPerSample",
            "desc": "采样位数",
            "content": "8 8 8"
          },
          {
            "tagid": null,
            "tagname": "ImageDescription",
            "desc": "图像描述",
            "content": "mde"
          },
          {
            "tagid": null,
            "tagname": "Make",
            "desc": "制造商",
            "content": "HUAWEI GPS"
          },
          {
            "tagid": null,
            "tagname": "Model",
            "desc": "型号",
            "content": "EVA-TL00"
          },
          {
            "tagid": null,
            "tagname": "Orientation",
            "desc": "方向",
            "content": "Horizontal (normal)"
          },
          {
            "tagid": null,
            "tagname": "XResolution",
            "desc": "X分辨率",
            "content": "72"
          },
          {
            "tagid": null,
            "tagname": "YResolution",
            "desc": "Y分辨率",
            "content": "72"
          },
          {
            "tagid": null,
            "tagname": "ResolutionUnit",
            "desc": "分辨率单位",
            "content": "inches"
          },
          {
            "tagid": null,
            "tagname": "Software",
            "desc": "软件",
            "content": "Snapseed 2.0"
          },
          {
            "tagid": null,
            "tagname": "ModifyDate",
            "desc": "修改日期",
            "content": "2017:03:12 19:16:53"
          },
          {
            "tagid": null,
            "tagname": "YCbCrPositioning",
            "desc": "YCbCr定位",
            "content": "Centered"
          }
        ],
        "ExifIFD": [
          {
            "tagid": null,
            "tagname": "ExposureTime",
            "desc": "曝光时间",
            "content": "1/38"
          },
          {
            "tagid": null,
            "tagname": "FNumber",
            "desc": "光圈值",
            "content": "2.2"
          },
          {
            "tagid": null,
            "tagname": "ExposureProgram",
            "desc": "曝光程序",
            "content": "Program AE"
          },
          {
            "tagid": null,
            "tagname": "ISO",
            "desc": "ISO",
            "content": "1250"
          },
          {
            "tagid": null,
            "tagname": "ExifVersion",
            "desc": "Exif版本",
            "content": "0210"
          },
          {
            "tagid": null,
            "tagname": "DateTimeOriginal",
            "desc": "原始日期时间",
            "content": "2017:03:11 16:49:07"
          },
          {
            "tagid": null,
            "tagname": "CreateDate",
            "desc": "创建日期",
            "content": "2016:08:07 19:59:37"
          },
          {
            "tagid": null,
            "tagname": "ComponentsConfiguration",
            "desc": "ComponentsConfiguration",
            "content": "Y, Cb, Cr, -"
          },
          {
            "tagid": null,
            "tagname": "ShutterSpeedValue",
            "desc": "快门速度值",
            "content": "1/999963365"
          },
          {
            "tagid": null,
            "tagname": "ApertureValue",
            "desc": "光圈值",
            "content": "2.2"
          },
          {
            "tagid": null,
            "tagname": "BrightnessValue",
            "desc": "亮度值",
            "content": "0"
          },
          {
            "tagid": null,
            "tagname": "ExposureCompensation",
            "desc": "曝光补偿",
            "content": "0"
          },
          {
            "tagid": null,
            "tagname": "MeteringMode",
            "desc": "测光模式",
            "content": "Multi-segment"
          },
          {
            "tagid": null,
            "tagname": "LightSource",
            "desc": "光源",
            "content": "Other"
          },
          {
            "tagid": null,
            "tagname": "Flash",
            "desc": "闪光灯",
            "content": "No Flash"
          },
          {
            "tagid": null,
            "tagname": "FocalLength",
            "desc": "焦距",
            "content": "4.5 mm"
          },
          {
            "tagid": null,
            "tagname": "SubSecTime",
            "desc": "SubSecTime",
            "content": "450586"
          },
          {
            "tagid": null,
            "tagname": "SubSecTimeOriginal",
            "desc": "SubSecTime原始",
            "content": "450586"
          },
          {
            "tagid": null,
            "tagname": "SubSecTimeDigitized",
            "desc": "SubSecTime数码化",
            "content": "450586"
          },
          {
            "tagid": null,
            "tagname": "FlashpixVersion",
            "desc": "Flashpix版本",
            "content": "0100"
          },
          {
            "tagid": null,
            "tagname": "ColorSpace",
            "desc": "色彩空间",
            "content": "sRGB"
          },
          {
            "tagid": null,
            "tagname": "ExifImageWidth",
            "desc": "Exif图像宽度",
            "content": "3584"
          },
          {
            "tagid": null,
            "tagname": "ExifImageHeight",
            "desc": "Exif图像高度",
            "content": "2341"
          },
          {
            "tagid": null,
            "tagname": "SensingMethod",
            "desc": "感光模式",
            "content": "One-chip color area"
          },
          {
            "tagid": null,
            "tagname": "FileSource",
            "desc": "文件来源",
            "content": "Digital Camera"
          },
          {
            "tagid": null,
            "tagname": "SceneType",
            "desc": "场景类型",
            "content": "Directly photographed"
          },
          {
            "tagid": null,
            "tagname": "CustomRendered",
            "desc": "CustomRendered",
            "content": "Custom"
          },
          {
            "tagid": null,
            "tagname": "ExposureMode",
            "desc": "曝光模式",
            "content": "Auto"
          },
          {
            "tagid": null,
            "tagname": "WhiteBalance",
            "desc": "白平衡",
            "content": "Auto"
          },
          {
            "tagid": null,
            "tagname": "DigitalZoomRatio",
            "desc": "数码变焦比",
            "content": "1"
          },
          {
            "tagid": null,
            "tagname": "FocalLengthIn35mmFormat",
            "desc": "35mm等效焦距",
            "content": "27 mm"
          },
          {
            "tagid": null,
            "tagname": "SceneCaptureType",
            "desc": "场景Capture类型",
            "content": "Standard"
          },
          {
            "tagid": null,
            "tagname": "GainControl",
            "desc": "Gain控制",
            "content": "None"
          },
          {
            "tagid": null,
            "tagname": "Contrast",
            "desc": "对比度",
            "content": "Normal"
          },
          {
            "tagid": null,
            "tagname": "Saturation",
            "desc": "饱和度",
            "content": "Normal"
          },
          {
            "tagid": null,
            "tagname": "Sharpness",
            "desc": "锐度",
            "content": "Normal"
          },
          {
            "tagid": null,
            "tagname": "SubjectDistanceRange",
            "desc": "主体距离范围",
            "content": "Unknown"
          }
        ],
        "InteropIFD": [
          {
            "tagid": null,
            "tagname": "InteropIndex",
            "desc": "Interop索引",
            "content": "R98 - DCF basic file (sRGB)"
          }
        ],
        "GPS": [
          {
            "tagid": null,
            "tagname": "GPSLatitudeRef",
            "desc": "GPSLatitudeRef",
            "content": "North"
          },
          {
            "tagid": null,
            "tagname": "GPSLatitude",
            "desc": "GPSLatitude",
            "content": "29 deg 56' 15.00\""
          },
          {
            "tagid": null,
            "tagname": "GPSLongitudeRef",
            "desc": "GPSLongitudeRef",
            "content": "East"
          },
          {
            "tagid": null,
            "tagname": "GPSLongitude",
            "desc": "GPSLongitude",
            "content": "121 deg 48' 20.00\""
          }
        ],
        "JFIF": [
          {
            "tagid": null,
            "tagname": "JFIFVersion",
            "desc": "JFIF版本",
            "content": "1.01"
          },
          {
            "tagid": null,
            "tagname": "ResolutionUnit",
            "desc": "分辨率单位",
            "content": "None"
          },
          {
            "tagid": null,
            "tagname": "XResolution",
            "desc": "X轴分辨率",
            "content": "1"
          },
          {
            "tagid": null,
            "tagname": "YResolution",
            "desc": "Y轴分辨率",
            "content": "1"
          }
        ],
        "Composite": [
          {
            "tagid": null,
            "tagname": "Aperture",
            "desc": "光圈",
            "content": "2.2"
          },
          {
            "tagid": null,
            "tagname": "GPSLatitude",
            "desc": "GPS纬度",
            "content": "29 deg 56' 15.00\" N"
          },
          {
            "tagid": null,
            "tagname": "GPSLongitude",
            "desc": "GPS经度",
            "content": "121 deg 48' 20.00\" E"
          },
          {
            "tagid": null,
            "tagname": "GPSPosition",
            "desc": "GPS位置",
            "content": "29 deg 56' 15.00\" N, 121 deg 48' 20.00\" E"
          },
          {
            "tagid": null,
            "tagname": "ImageSize",
            "desc": "图像尺寸",
            "content": "3584x2341"
          },
          {
            "tagid": null,
            "tagname": "Megapixels",
            "desc": "Megapixels",
            "content": "8.4"
          },
          {
            "tagid": null,
            "tagname": "ScaleFactor35efl",
            "desc": "35mm等效因子",
            "content": "6.0"
          },
          {
            "tagid": null,
            "tagname": "ShutterSpeed",
            "desc": "快门速度",
            "content": "1/38"
          },
          {
            "tagid": null,
            "tagname": "SubSecCreateDate",
            "desc": "SubSecCreateDate",
            "content": "2016:08:07 19:59:37.450586"
          },
          {
            "tagid": null,
            "tagname": "SubSecDateTimeOriginal",
            "desc": "SubSec原始日期时间",
            "content": "2017:03:11 16:49:07.450586"
          },
          {
            "tagid": null,
            "tagname": "SubSecModifyDate",
            "desc": "SubSecModifyDate",
            "content": "2017:03:12 19:16:53.450586"
          },
          {
            "tagid": null,
            "tagname": "CircleOfConfusion",
            "desc": "(最小)模糊圈",
            "content": "0.005 mm"
          },
          {
            "tagid": null,
            "tagname": "FOV",
            "desc": "视角",
            "content": "67.4 deg"
          },
          {
            "tagid": null,
            "tagname": "FocalLength35efl",
            "desc": "35mm等效焦距",
            "content": "4.5 mm (35 mm equivalent: 27.0 mm)"
          },
          {
            "tagid": null,
            "tagname": "HyperfocalDistance",
            "desc": "超焦距",
            "content": "1.84 m"
          },
          {
            "tagid": null,
            "tagname": "LightValue",
            "desc": "亮度值",
            "content": "3.9"
          }
        ]
      },
      "result": "SUCCESS"
    }

json 解析：这个就免了吧，应该很容易看得懂了

<h2 id="discover">发现</h2>
<h3 id="tag">标签</h3>

url：`https://api.tuchong.com/discover-app`

url 拼接参数：

同[推荐](#recommend)

url 示例：[`https://api.tuchong.com/discover-app?os_api=23&device_type=MI&device_platform=android&ssmix=a&manifest_version_code=232&dpi=440&abflag=0&uuid=326132612301652&version_code=232&app_name=tuchong&version_name=2.3.2&openudid=4352d5fadf543531&resolution=1280*1000&os_version=5.8.1&ac=wifi&aid=0`](https://api.tuchong.com/discover-app?os_api=23&device_type=MI&device_platform=android&ssmix=a&manifest_version_code=232&dpi=440&abflag=0&uuid=326132612301652&version_code=232&app_name=tuchong&version_name=2.3.2&openudid=4352d5fadf543531&resolution=1280*1000&os_version=5.8.1&ac=wifi&aid=0)

json 示例：

	{
      "banners": [
        {
          "url": "tuchong://?type=tag&id=449941&tag_name=图虫一周精选",
          "src": "https://s1.tuchong.com/content-image/c64b2b54057eea977ba9250a93e235a3.jpg"
        }
      ],
      "hotEvents": [
        {
          "tag_id": "463912",
          "tag_name": "青春，我爱过的那个女孩！",
          "status": "open",
          "posts": "358",
          "new_posts": "243",
          "participants": "292",
          "end_at": null,
          "title": "青春，我爱过的那个女孩！",
          "url": "https://tuchong.com/events/463912/",
          "event_type": "topic",
          "remainingDays": 999,
          "image_posts": [
            "14236914"
          ],
          "app_banner": false,
          "images": [
            "https://photo.tuchong.com/1136739/g/18644368.webp"
          ],
          "app_url": "https://tuchong.com/app-events/463912/"
        },
        {
          "tag_id": "459789",
          "tag_name": "2017全球华人摄影",
          "status": "open",
          "posts": "1843",
          "new_posts": "351",
          "participants": "990",
          "end_at": "2017-04-06 00:00:00",
          "title": "2017全球华人新春摄影大赛",
          "url": "https://tuchong.com/events/459789/",
          "event_type": "competition",
          "remainingDays": 23,
          "image_posts": [
            "14224452"
          ],
          "app_banner": false,
          "images": [
            "https://photo.tuchong.com/986007/g/9012621.webp"
          ],
          "app_url": "https://tuchong.com/app-events/459789/"
        },
        {
          "tag_id": "437309",
          "tag_name": "朋友，这是艺术",
          "status": "open",
          "posts": "1119",
          "new_posts": "267",
          "participants": "669",
          "end_at": null,
          "title": "朋友，这是艺术",
          "url": "https://tuchong.com/events/437309/",
          "event_type": "topic",
          "remainingDays": 999,
          "image_posts": [
            "14222622"
          ],
          "app_banner": false,
          "images": [
            "https://photo.tuchong.com/1205980/g/16546585.webp"
          ],
          "app_url": "https://tuchong.com/app-events/437309/"
        },
        {
          "tag_id": "450772",
          "tag_name": "镜头前不一样的天空",
          "status": "open",
          "posts": "865",
          "new_posts": "170",
          "participants": "589",
          "end_at": null,
          "title": "致风光",
          "url": "https://tuchong.com/events/450772/",
          "event_type": "topic",
          "remainingDays": 999,
          "image_posts": [
            "14216633"
          ],
          "app_banner": false,
          "images": [
            "https://photo.tuchong.com/243108/g/16276332.webp"
          ],
          "app_url": "https://tuchong.com/app-events/450772/"
        },
        {
          "tag_id": "463200",
          "tag_name": "B.Way蓝色星球摄影赛",
          "status": "open",
          "posts": "1104",
          "new_posts": "497",
          "participants": "536",
          "end_at": "2017-04-01 00:00:00",
          "title": "B.Way蓝色星球摄影赛",
          "url": "https://tuchong.com/events/463200/",
          "event_type": "competition",
          "remainingDays": 18,
          "image_posts": [
            "14223186"
          ],
          "app_banner": false,
          "images": [
            "https://photo.tuchong.com/1145421/g/18107452.webp"
          ],
          "app_url": "https://tuchong.com/app-events/463200/"
        }
      ],
      "categories": [
        {
          "tag_name": "热门",
          "tag_id": -1
        },
        {
          "tag_name": "最新",
          "tag_id": -2
        },
        {
          "tag_name": "精选",
          "tag_id": -3
        },
        {
          "tag_name": "人像",
          "tag_id": 131
        },
        {
          "tag_name": "风光",
          "tag_id": 693
        },
        {
          "tag_name": "人文",
          "tag_id": 133
        },
        {
          "tag_name": "旅行",
          "tag_id": 743
        },
        {
          "tag_name": "建筑",
          "tag_id": 767
        },
        {
          "tag_name": "静物",
          "tag_id": 684
        },
        {
          "tag_name": "黑白",
          "tag_id": 729
        }
      ],
      "result": "SUCCESS"
    }

json 解析：

- `result`：如果为 `SUCCESS` 则请求成功
- `banners`：标题栏图片
	- `url`：
	- `src`：图片 url
- `hotEvents`：热门活动
	- `tag_name`：文字描述
	- `url`：专栏链接
	- `images`：图片信息
	- ``：
	- ``：
- `categories`：分类信息
	- `tag_name`：分类名
	- `tag_id`：分类 id，用于查看[内容](#content)

<h3 id="content">内容</h3>

url：https://api.tuchong.com/discover/ + tag_id（[标签](#tag) json中的字段） + /category

拼接参数：

同[推荐](#recommend)

url 示例：`https://api.tuchong.com/discover/-1/category?os_api=25&device_type=MI&device_platform=android&ssmix=a&manifest_version_code=232&dpi=450&abflag=0&uuid=329642135962135&version_code=232&count=20&app_name=tuchong&version_name=2.3.2&openudid=53fa4df32154dfa3&resolution=1280*1000&os_version=5.0.1&ac=wifi&aid=0&page=1`

json 示例：

	{
      "post_list": [
        {
          "post_id": 14238903,
          "author_id": "1027179",
          "type": "multi-photo",
          "url": "https://tuchong.com/1027179/14238903/",
          "published_at": "2017-03-13 20:46:29",
          "excerpt": "",
          "favorites": 474,
          "comments": 28,
          "title": "《白世界的森林》",
          "image_count": 1,
          "delete": false,
          "content": "",
          "update": false,
          "images": [
            {
              "img_id": 20867843,
              "user_id": 1027179,
              "title": "",
              "excerpt": "《白世界的森林》一阵大雪过后，给大地的披上了洁白无垠的地毯，看上去就像席梦思，真想让人躺上去，这等待了一个小时的阳光，它像一缕缕金色的细沙，穿过重重叠叠的树枝照进来，斑斑驳驳地洒落在雪地上。拍摄于坝上塞罕坝。创作思路来自于闭眼缄默老师的《密林深处》。拍摄这张时，当时是这么想的。前面的树枝，是我想表达一种纵深感。像是一个对着新世界充满好奇的小孩，藏在树的后面，窥视着前方树林的情况。。阿卡.Carson",
              "width": 1920,
              "height": 1080,
              "description": "《白世界的森林》一阵大雪过后，给大地的披上了洁白无垠的地毯，看上去就像席梦思，真想让人躺上去，这等待了一个小时的阳光，它像一缕缕金色的细沙，穿过重重叠叠的树枝照进来，斑斑驳驳地洒落在雪地上。拍摄于坝上塞罕坝。创作思路来自于闭眼缄默老师的《密林深处》。拍摄这张时，当时是这么想的。前面的树枝，是我想表达一种纵深感。像是一个对着新世界充满好奇的小孩，藏在树的后面，窥视着前方树林的情况。。阿卡.Carson"
            }
          ],
          "tags": [
            {
              "tag_id": 463903,
              "type": "event",
              "tag_name": "PS挑战赛：完美逆光效果",
              "event_type": "competition"
            },
            {
              "tag_id": 693,
              "type": "subject",
              "tag_name": "风光",
              "event_type": ""
            },
            {
              "tag_id": 2105,
              "type": "style",
              "tag_name": "色彩",
              "event_type": ""
            },
            {
              "tag_id": 1314,
              "type": "equipment",
              "tag_name": "尼康",
              "event_type": ""
            },
            {
              "tag_id": 209,
              "type": "style",
              "tag_name": "后期",
              "event_type": ""
            },
            {
              "tag_id": 1001,
              "type": "location",
              "tag_name": "中国",
              "event_type": ""
            },
            {
              "tag_id": 458229,
              "type": "uncategorized",
              "tag_name": "飞图映像",
              "event_type": ""
            }
          ],
          "users": [
            {
              "site_id": 329597,
              "icon": "https://s1.tuchong.com/sites/329/329597/logo_small.jpg?1"
            },
            {
              "site_id": 267240,
              "icon": "https://s1.tuchong.com/sites/267/267240/logo_small.jpg?1"
            },
            {
              "site_id": 1492037,
              "icon": "https://s1.tuchong.com/sites/149/1492037/logo_small.jpg?2"
            },
            {
              "site_id": 14198,
              "icon": "https://static.tuchong.net/styles/images/noavatar_small.gif"
            },
            {
              "site_id": 346986,
              "icon": "https://static.tuchong.net/styles/images/noavatar_small.gif"
            },
            {
              "site_id": 332768,
              "icon": "https://static.tuchong.net/styles/images/noavatar_small.gif"
            },
            {
              "site_id": 1166910,
              "icon": "https://s1.tuchong.com/sites/116/1166910/logo_small.jpg?1"
            }
          ],
          "is_favorite": false,
          "site": {
            "site_id": 1027179,
            "type": "user",
            "name": "阿卡-Carson",
            "domain": "",
            "description": "自由摄影师，微博@阿卡-Carson  ，微信：15919563666",
            "followers": 8343,
            "url": "https://tuchong.com/1027179/",
            "icon": "https://s1.tuchong.com/sites/102/1027179/logo_small.jpg?6",
            "verified": false,
            "verified_type": 0,
            "verified_reason": "",
            "verifications": 0,
            "verification_list": []
          }
        }
      ],
      "result": "SUCCESS"
    }

json 解析：

基本等同[推荐](#recommend)