# 必应词典 #

- [词典](#dic)
- [翻译](#translation)

ps：必应词典在本地存有数据库，所以它的联想功能是直接在数据库中查找 —— [戳我下载 Android 数据库文件](https://github.com/jokermonn/-Api/blob/master/mircrosoft_bing_dic.db) 或 [戳我下载 wps 表格](https://github.com/jokermonn/-Api/blob/master/mircrosoft_bing_dic..xlsx)。**本地数据库中包含单词的基础默认翻译**

<h2 id="dic">词典</h2>

url：https://dict.bing.com.cn/api/http/v2/4154AA7A1FC54ad7A84A0236AA4DCAF3/en-us/zh-cn/

拼接参数：

- `q`：关键词
- `format`：返回格式。`application/json` 或 `application/xml`

url 示例：[`https://dict.bing.com.cn/api/http/v2/4154AA7A1FC54ad7A84A0236AA4DCAF3/en-us/zh-cn/?q=address&format=application/json`](https://dict.bing.com.cn/api/http/v2/4154AA7A1FC54ad7A84A0236AA4DCAF3/en-us/zh-cn/?q=address&format=application/json)

json 示例：

	  {
      "LEX": {
        "C_DEF": [
          {
            "DEF": "地址$$(信上的)称呼$$演说$$致辞$$姓名$$谈话$$话$$策略$$谈吐$$献殷勤$$行踪$$吆喝$$妙法$$口才$$求爱$$求亲$$寒喧$$正式请愿$$灵巧$$风度$$娴熟",
            "POS": "n",
            "SEN": [
              {
                "D": "(信上的)称呼,姓名;地址",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "地址;行踪",
                "R": 0,
                "STS": [
                  {
                    "DATE": "/Date(1336460400000-0700)/",
                    "ID": 0,
                    "ORAL": false,
                    "R": 0,
                    "READ": 0,
                    "S": {
                      "AD": null,
                      "COL": null,
                      "D": "He gave me the address.",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "T": {
                      "AD": null,
                      "COL": null,
                      "D": "他给了我地址。",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "TECH": false,
                    "TITLE": false,
                    "WA": 0,
                    "WAD": null
                  }
                ],
                "URL": null
              },
              {
                "D": "致辞;寒喧;演说;正式请愿",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "话;演说;谈话;吆喝",
                "R": 0,
                "STS": [
                  {
                    "DATE": "/Date(1336460400000-0700)/",
                    "ID": 0,
                    "ORAL": false,
                    "R": 0,
                    "READ": 0,
                    "S": {
                      "AD": null,
                      "COL": null,
                      "D": "The latter part of this address was scarcely heard by Darcy.",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "T": {
                      "AD": null,
                      "COL": null,
                      "D": "后半段话达西几乎没有听见。",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "TECH": false,
                    "TITLE": false,
                    "WA": 0,
                    "WAD": null
                  }
                ],
                "URL": null
              },
              {
                "D": "谈吐,风度",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "谈吐;口才",
                "R": 0,
                "STS": [
                  {
                    "DATE": "/Date(1336460400000-0700)/",
                    "ID": 0,
                    "ORAL": false,
                    "R": 0,
                    "READ": 0,
                    "S": {
                      "AD": null,
                      "COL": null,
                      "D": "Edward Ferrars was not recommended to their good opinion by any peculiar graces of person or address.",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "T": {
                      "AD": null,
                      "COL": null,
                      "D": "爱德华·费拉尔斯得到她们的好评并不是由于他的人品或谈吐特别出众。",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "TECH": false,
                    "TITLE": false,
                    "WA": 0,
                    "WAD": null
                  }
                ],
                "URL": null
              },
              {
                "D": "妙法;策略;灵巧",
                "R": 0,
                "STS": [
                  {
                    "DATE": "/Date(1336460400000-0700)/",
                    "ID": 0,
                    "ORAL": false,
                    "R": 0,
                    "READ": 0,
                    "S": {
                      "AD": null,
                      "COL": null,
                      "D": "It was now that I applauded my perseverance and address.",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "T": {
                      "AD": null,
                      "COL": null,
                      "D": "我自己赞美我的耐性同我的妙法。",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "TECH": false,
                    "TITLE": false,
                    "WA": 0,
                    "WAD": null
                  }
                ],
                "URL": null
              },
              {
                "D": "求爱,献殷勤",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "灵巧,娴熟",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "求亲",
                "R": 0,
                "STS": [
                  {
                    "DATE": "/Date(1336460400000-0700)/",
                    "ID": 0,
                    "ORAL": false,
                    "R": 0,
                    "READ": 0,
                    "S": {
                      "AD": null,
                      "COL": null,
                      "D": "I'll fairly own that it was I that instructed my girls to encourage our landlord's addresses.",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "T": {
                      "AD": null,
                      "COL": null,
                      "D": "我说句公道话,原是我叫女儿们鼓励我们的房东求亲的。",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "TECH": false,
                    "TITLE": false,
                    "WA": 0,
                    "WAD": null
                  }
                ],
                "URL": null
              }
            ]
          },
          {
            "DEF": "解决$$讲话$$处理$$处理(问题等)$$称呼$$满足(需求等)$$发言$$应付$$说$$【商业】交$$引导$$委托$$着手处理$$钻研$$倾述$$在…上写姓名住址$$向…致意$$给…讲话$$向…演说$$向…求爱$$向…献殷勤$$对…说$$引见$$【法律】(立法部门)请求撤销(不适任法官的)职务$$【高尔夫球】瞄准",
            "POS": "v",
            "SEN": [
              {
                "D": "钻研;解决,处理,着手处理",
                "R": 0,
                "STS": [
                  {
                    "DATE": "/Date(1336460400000-0700)/",
                    "ID": 0,
                    "ORAL": false,
                    "R": 0,
                    "READ": 0,
                    "S": {
                      "AD": null,
                      "COL": null,
                      "D": "We addressed ourselves vigorously to this problem.",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "T": {
                      "AD": null,
                      "COL": null,
                      "D": "我们奋力钻研这一问题。",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "TECH": false,
                    "TITLE": false,
                    "WA": 0,
                    "WAD": null
                  }
                ],
                "URL": null
              },
              {
                "D": "在…上写姓名住址;称呼;向…致意",
                "R": 0,
                "STS": [
                  {
                    "DATE": "/Date(1336460400000-0700)/",
                    "ID": 0,
                    "ORAL": false,
                    "R": 0,
                    "READ": 0,
                    "S": {
                      "AD": null,
                      "COL": null,
                      "D": "How should one address a senator?",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "T": {
                      "AD": null,
                      "COL": null,
                      "D": "如何称呼一位议院的参议员?",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "TECH": false,
                    "TITLE": false,
                    "WA": 0,
                    "WAD": null
                  }
                ],
                "URL": null
              },
              {
                "D": "给…讲话;向…演说,向…求爱,向…献殷勤",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "说,对…说;讲话,发言;倾述",
                "R": 0,
                "STS": [
                  {
                    "DATE": "/Date(1336460400000-0700)/",
                    "ID": 0,
                    "ORAL": false,
                    "R": 0,
                    "READ": 0,
                    "S": {
                      "AD": null,
                      "COL": null,
                      "D": "He addressed the strong, silent shareholder.",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "T": {
                      "AD": null,
                      "COL": null,
                      "D": "他向那个坚强沉默的股东说。",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "TECH": false,
                    "TITLE": false,
                    "WA": 0,
                    "WAD": null
                  }
                ],
                "URL": null
              },
              {
                "D": "应付,处理(问题等)",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "满足(需求等)",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "引导,引见",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "【商业】交,委托",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "【法律】(立法部门)请求撤销(不适任法官的)职务",
                "R": 0,
                "STS": [
                  {
                    "DATE": "/Date(1336460400000-0700)/",
                    "ID": 0,
                    "ORAL": false,
                    "R": 0,
                    "READ": 0,
                    "S": {
                      "AD": null,
                      "COL": null,
                      "D": "We do not address the unforgettable Gods.",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "T": {
                      "AD": null,
                      "COL": null,
                      "D": "我们没有请求值得铭心刻骨的众神的帮助。",
                      "IME": null,
                      "M": 0,
                      "SIG": null,
                      "TG": null,
                      "URL": null,
                      "W": null
                    },
                    "TECH": false,
                    "TITLE": false,
                    "WA": 0,
                    "WAD": null
                  }
                ],
                "URL": null
              },
              {
                "D": "【高尔夫球】瞄准",
                "R": 0,
                "STS": null,
                "URL": null
              }
            ]
          },
          {
            "DEF": null,
            "POS": "web",
            "SEN": [
              {
                "D": "住址",
                "R": 130854,
                "STS": null,
                "URL": "http://www.360doc.com/content/05/1025/15/1275_23749.shtml"
              },
              {
                "D": "通讯地址",
                "R": 40287,
                "STS": null,
                "URL": "http://zhidao.baidu.com/question/133764336.html"
              },
              {
                "D": "联系地址",
                "R": 4631,
                "STS": null,
                "URL": "http://www.tzsunrui.com.cn/"
              },
              {
                "D": "公司地址",
                "R": 1769,
                "STS": null,
                "URL": "http://edu.ebay.cn/tips/201110246866.html"
              },
              {
                "D": "联络地址",
                "R": 1280,
                "STS": null,
                "URL": "http://www.oh100.com/a/201107/2887.html"
              },
              {
                "D": "详细地址",
                "R": 837,
                "STS": null,
                "URL": "http://www.xici.net/d108454468.htm"
              },
              {
                "D": "演说",
                "R": 652,
                "STS": null,
                "URL": "http://wenku.baidu.com/view/5c993ed5360cba1aa811daec.html"
              }
            ]
          }
        ],
        "HW": {
          "DEF": "地址$$解决$$讲话$$处理$$处理(问题等)$$(信上的)称呼$$称呼$$演说$$满足(需求等)$$致辞$$发言$$姓名$$应付$$谈话$$话$$说$$【商业】交$$策略$$引导$$委托$$谈吐$$着手处理$$献殷勤$$行踪$$钻研$$倾述$$吆喝$$妙法$$口才$$求爱$$求亲$$在…上写姓名住址$$向…致意$$给…讲话$$向…演说$$向…求爱$$向…献殷勤$$对…说$$寒喧$$正式请愿$$灵巧$$引见$$风度$$娴熟$$【法律】(立法部门)请求撤销(不适任法官的)职务$$【高尔夫球】瞄准",
          "SIG": "3C7B74A40CD8FE4F165330F051C7C4BF",
          "V": "address"
        },
        "H_DEF": [
          {
            "DEF": null,
            "POS": "n",
            "SEN": [
              {
                "D": "the number, street name, and other information that describes where a building is or where somebody lives",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "the address of a person or organization when written on a letter or an item of mail",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "a formal speech or report",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "a number that specifies a location in a computer's memory",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "a statement of opinions or desires sent to the sovereign by either or both of the Houses of Parliament",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "a formal speech given by someone to a group of people, especially as part of an important occasion",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "the name of the place where you live or work, including the house or office number and the name of the street, area, and town. It may also include a set of numbers and letters, called a postcode in British English and a zip code in American English",
                "R": 0,
                "STS": null,
                "URL": null
              }
            ]
          },
          {
            "DEF": null,
            "POS": "np",
            "SEN": [
              {
                "D": "attention paid to somebody that is intended as courtship",
                "R": 0,
                "STS": null,
                "URL": null
              }
            ]
          },
          {
            "DEF": null,
            "POS": "v",
            "SEN": [
              {
                "D": "to write or print on an item of mail details of where it is to be delivered",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "to say something to somebody, or make a speech to an audience",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "to use the proper name or title in speaking or writing to somebody",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "to set about doing some task",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "to face up to and deal with a problem or issue",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "to stand facing a dance partner or an archery target",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "to take up the correct stance beside a golf ball before hitting it",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "to write the name and address of a particular person or organization on an envelope, package, etc.",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "to officially tell a particular person or organization your complaints, questions, or comments",
                "R": 0,
                "STS": null,
                "URL": null
              },
              {
                "D": "to speak publicly to a group of people",
                "R": 0,
                "STS": null,
                "URL": null
              }
            ]
          }
        ],
        "INF": [
          {
            "IE": "addresses",
            "T": "pl"
          },
          {
            "IE": "addressed",
            "T": "pp"
          },
          {
            "IE": "addressing",
            "T": "prp"
          },
          {
            "IE": "addresses",
            "T": "3pps"
          },
          {
            "IE": "address",
            "T": "s"
          },
          {
            "IE": "addresses",
            "T": "prt"
          },
          {
            "IE": "addressed",
            "T": "pt"
          }
        ],
        "LCS": [
          {
            "LC": [
              {
                "T1": "address",
                "T2": "issue"
              },
              {
                "T1": "address",
                "T2": "problem"
              },
              {
                "T1": "give",
                "T2": "address"
              },
              {
                "T1": "address",
                "T2": "meeting"
              },
              {
                "T1": "address",
                "T2": "audience"
              },
              {
                "T1": "deliver",
                "T2": "address"
              },
              {
                "T1": "note",
                "T2": "address"
              },
              {
                "T1": "address",
                "T2": "Congress"
              },
              {
                "T1": "address",
                "T2": "crowd"
              },
              {
                "T1": "address",
                "T2": "appeal"
              },
              {
                "T1": "address",
                "T2": "rally"
              },
              {
                "T1": "address",
                "T2": "nation"
              },
              {
                "T1": "address",
                "T2": "assembly"
              },
              {
                "T1": "address",
                "T2": "envelope"
              },
              {
                "T1": "address",
                "T2": "Parliament"
              }
            ],
            "RELA": "v.+n."
          },
          {
            "LC": [
              {
                "T1": "same",
                "T2": "address"
              },
              {
                "T1": "inaugural",
                "T2": "address"
              },
              {
                "T1": "final",
                "T2": "address"
              }
            ],
            "RELA": "adj.+n."
          }
        ],
        "PHRASE": [
          {
            "DEF": "实际地址",
            "SIG": null,
            "V": "actual address"
          },
          {
            "DEF": "通讯花名册",
            "SIG": null,
            "V": "address book"
          },
          {
            "DEF": "地址代码",
            "SIG": null,
            "V": "address code"
          },
          {
            "DEF": "地址字段地址部分",
            "SIG": null,
            "V": "address field"
          },
          {
            "DEF": "地址标记",
            "SIG": null,
            "V": "address mark"
          },
          {
            "DEF": "地址存储器",
            "SIG": null,
            "V": "address memory"
          },
          {
            "DEF": "基址",
            "SIG": null,
            "V": "base address"
          },
          {
            "DEF": "计算地址",
            "SIG": null,
            "V": "calculated address"
          },
          {
            "DEF": "浮动地址",
            "SIG": null,
            "V": "floating address"
          },
          {
            "DEF": "转发地址",
            "SIG": null,
            "V": "forwarding address"
          },
          {
            "DEF": "标识地址",
            "SIG": null,
            "V": "home address"
          },
          {
            "DEF": "立即地址",
            "SIG": null,
            "V": "immediate address"
          },
          {
            "DEF": "地址",
            "SIG": null,
            "V": "mailing address"
          },
          {
            "DEF": "推定地址",
            "SIG": null,
            "V": "presumptive address"
          },
          {
            "DEF": "基准地址",
            "SIG": null,
            "V": "reference address"
          },
          {
            "DEF": "区域地址",
            "SIG": null,
            "V": "regional address"
          },
          {
            "DEF": "绝对地址",
            "SIG": null,
            "V": "specific address"
          },
          {
            "DEF": "电报挂号",
            "SIG": null,
            "V": "telegraphic address"
          },
          {
            "DEF": "二地址",
            "SIG": null,
            "V": "two address"
          },
          {
            "DEF": "虚拟地址",
            "SIG": null,
            "V": "virtual address"
          }
        ],
        "PRON": [
          {
            "L": "US",
            "V": "'ædres"
          },
          {
            "L": "UK",
            "V": "ə'dres"
          }
        ],
        "THES": [
          {
            "A": [
              "ignore"
            ],
            "POS": "v",
            "S": [
              "direct",
              "deliver",
              "forward",
              "speak",
              "lecture",
              "talk",
              "tackle",
              "deal with"
            ]
          },
          {
            "A": null,
            "POS": "n",
            "S": [
              "speech",
              "discourse",
              "report",
              "statement"
            ]
          }
        ]
      },
      "MT": null,
      "Q": "address",
      "SENT": {
        "COUNT": 10,
        "OFFSET": 0,
        "ST": [
          {
            "DATE": "/Date(1384975564000-0800)/",
            "ID": 606158,
            "ORAL": false,
            "R": 63050,
            "READ": 69,
            "S": {
              "AD": "{1#dàn$1} {2#tā$2} {3#hái$3} {4#shì$4} {5#tóng yì$5} {6#le$6} {7#,$7} {8#tā$8} {9#jiù$9} {10#jì xià$10} {11#le$11} {12#tā$12} {13#de$13} {14#míng zì$14} {15#hé$15} {##*{16#dì zhǐ$16}*$$} {17#。$17}",
              "COL": null,
              "D": "{1#但$1}{2#她$2}{3#还$3}{4#是$4}{5#同意$5}{6#了$6}{7#，$7}{8#他$8}{9#就$9}{10#记下$10}{11#了$11}{12#她$12}{13#的$13}{14#名字$14}{15#和$15}{##*{16#地址$16}*$$}{17#。$17}",
              "IME": null,
              "M": 0,
              "SIG": "7F05BBC94BDEE5DB2585BB40571BD116",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{12#She$12} {5#acquiesced$5}{7#,$7} {1#however$1}, {15#and$15} {8#he$8} took {2#her$2} {14#name$14} {15#and$15} {#*{16#address$16}*$}{17#.$17}",
              "IME": null,
              "M": 17,
              "SIG": "BA56B3B550CFA51E6CDA3DEC4FE592F5",
              "TG": null,
              "URL": null,
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 30,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975527000-0800)/",
            "ID": 947925,
            "ORAL": false,
            "R": 60703,
            "READ": 55,
            "S": {
              "AD": "{1#wǒ$1} {2#shì$2} {3#zài$3} {4#xīn qíng$4} {5#jī dòng$5} {6#de$6} {7#qíng kuàng$7} {8#xià qù$8} {9#lǚ xíng$9} {10#duì$10} {11#měi guó$11} {12#guó huì$12} {##*{13#yǎn shuō$13}*$$} {14#de$14} {15#yāo yuē$15} {16#de$16} {17#。$17}",
              "COL": null,
              "D": "{1#我$1}{2#是$2}{3#在$3}{4#心情$4}{5#激动$5}{6#的$6}{7#情况$7}{8#下去$8}{9#履行$9}{10#对$10}{11#美国$11}{12#国会$12}{##*{13#演说$13}*$$}{14#的$14}{15#邀约$15}{16#的$16}{17#。$17}",
              "IME": null,
              "M": 0,
              "SIG": "6C47D4B54FDABC1EFD47FB2E1443AB5A",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{8#It$8} {2#was$2} with {4#heart$4}-{5#stirring$5} that {1#I$1} {9#fulfilled$9} {3#the$3} {15#invitation$15} {10#to$10} {#*{13#address$13}*$} the {12#Congress$12} {6#of$6} the {11#United States$11}{17#.$17}",
              "IME": null,
              "M": 17,
              "SIG": "04BBFCC3A4C199C17DF5908E958BB378",
              "TG": null,
              "URL": null,
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 37,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975535000-0800)/",
            "ID": 947745,
            "ORAL": false,
            "R": 60704,
            "READ": 90,
            "S": {
              "AD": "{1#guò lái$1} {2#yī$2} {3#liàng$3} {4#chū zū qì chē$4} {5#,$5} {6#wǒ$6} {7#shàng$7} {8#le$8} {9#chē$9} {10#,$10} {11#gào su$11} {12#sī jī$12} {13#wǒ$13} {14#de$14} {##*{15#zhù zhǐ$15}*$$} {16#。$16}",
              "COL": null,
              "D": "{1#过来$1}{2#一$2}{3#辆$3}{4#出租汽车$4}{5#，$5}{6#我$6}{7#上$7}{8#了$8}{9#车$9}{10#，$10}{11#告诉$11}{12#司机$12}{13#我$13}{14#的$14}{##*{15#住址$15}*$$}{16#。$16}",
              "IME": null,
              "M": 0,
              "SIG": "9DC5E0C210ABB47583C9E23CA223CB57",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{2#A$2} {4#taxi$4} {1#came$1} along {5#and$5} {6#I$6} got in and {11#gave$11} the {12#driver$12} the {#*{15#address$15}*$} {14#of$14} {13#my$13} flat{16#.$16}",
              "IME": null,
              "M": 17,
              "SIG": "A5E7E762923FF069843CEE6EDAAD7F05",
              "TG": null,
              "URL": null,
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 34,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975524000-0800)/",
            "ID": 335200,
            "ORAL": false,
            "R": 65535,
            "READ": 59,
            "S": {
              "AD": "{1#duì$1} {2#yī gè$2} {3#yìn dì ān rén$3} {4#zhí$4} {5#hū$5} {6#qí$6} {7#míng$7} {8#,$8} {9#huò$9} {10#zhí jiē$10} {11#xún wèn$11} {12#duì fāng$12} {13#de$13} {14#míng zì$14} {15#,$15} {16#zhè$16} {17#dōu$17} {18#bèi$18} {19#shì wéi$19} {20#táng tū$20} {21#wú lǐ$21} {22#de$22} {23#xíng wéi$23} {24#。$24}",
              "COL": null,
              "D": "{1#对$1}{2#一个$2}{3#印第安人$3}{4#直$4}{5#呼$5}{6#其$6}{7#名$7}{8#，$8}{9#或$9}{10#直接$10}{11#询问$11}{12#对方$12}{13#的$13}{14#名字$14}{15#，$15}{16#这$16}{17#都$17}{18#被$18}{19#视为$19}{20#唐突$20}{21#无礼$21}{22#的$22}{23#行为$23}{24#。$24}",
              "IME": null,
              "M": 0,
              "SIG": "BE3BE5A73695C35E6389F655052CBC2D",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "It {17#would$17} {18#be$18} {19#esteemed$19} {2#an$2} {23#act$23} {13#of$13} {21#rudeness$21} {1#to$1} {#*address*$} an {3#Indian$3} by {6#his$6} personal {14#name$14}{8#,$8} {9#or$9} to {11#inquire$11} his {7#name$7} {4#directly$4} from himself{24#.$24}",
              "IME": null,
              "M": 17,
              "SIG": "40D6E58EB3A27EE46FA1E6F1E541F8E9",
              "TG": null,
              "URL": null,
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 50,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975526000-0800)/",
            "ID": 329212,
            "ORAL": false,
            "R": 65535,
            "READ": 65,
            "S": {
              "AD": "{1#hàn$1} {2#mí$2} {3#ěr$3} {4#dēng$4} {5#hú tòng$5} {6#hái$6} {7#méi yǒu$7} {8#dào$8} {9#,$9} {10#tā$10} {11#yǐ jīng$11} {12#gǎi biàn$12} {13#zhǔ yì$13} {14#,$14} {15#jiào$15} {16#le$16} {17#yī$17} {18#bù$18} {19#mǎ chē$19} {20#,$20} {21#gào su$21} {22#mǎ fū$22} {23#shàng$23} {24#wēi$24} {25#sī$25} {26#dá lǐ yà$26} {23#dà jiē$23} {28#yī gè$28} {##*{29#dì fāng$29}*$$} {30#qù$30} {31#。$31}",
              "COL": null,
              "D": "{1#汉$1}{2#弥$2}{3#尔$3}{4#登$4}{5#胡同$5}{6#还$6}{7#没有$7}{8#到$8}{9#，$9}{10#他$10}{11#已经$11}{12#改变$12}{13#主意$13}{14#，$14}{15#叫$15}{16#了$16}{17#一$17}{18#部$18}{19#马车$19}{20#，$20}{21#告诉$21}{22#马夫$22}{23#上$23}{24#威$24}{25#斯$25}{26#达里亚$26}{23#大街$23}{28#一个$28}{##*{29#地方$29}*$$}{30#去$30}{31#。$31}",
              "IME": null,
              "M": 0,
              "SIG": "1DF1CF6976A6C52B1C415332CA3ED092",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{10#He$10} {11#had$11} {7#not$7} {8#reached$8} {1#Hamilton$1} Terrace before he {12#changed$12} his {13#mind$13}{9#,$9} and hailing {28#a$28} {19#cab$19}{14#,$14} {21#gave$21} the {22#driver$22} an {#*{29#address$29}*$} {3#in$3} Wistaria {23#Avenue$23}{31#.$31}",
              "IME": null,
              "M": 17,
              "SIG": "9C7EBD8162F6C5DA8A3F15230A7D1B2A",
              "TG": null,
              "URL": null,
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 57,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975507000-0800)/",
            "ID": 318169,
            "ORAL": false,
            "R": 65535,
            "READ": 89,
            "S": {
              "AD": "{1#wǒ$1} {2#zhī dào$2} {3#tā$3} {4#de$4} {##*{5#dì zhǐ$5}*$$} {6#,$6} {7#dàn shì$7} {8#wǒ$8} {9#xiàn zài$9} {10#xiǎng$10} {11#bù$11} {12#qǐ lái$12} {13#。$13}",
              "COL": null,
              "D": "{1#我$1}{2#知道$2}{3#他$3}{4#的$4}{##*{5#地址$5}*$$}{6#，$6}{7#但是$7}{8#我$8}{9#现在$9}{10#想$10}{11#不$11}{12#起来$12}{13#。$13}",
              "IME": null,
              "M": 0,
              "SIG": "A1021CD3E8DBF00C0C1548AC0DF82DBE",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{1#I$1} {2#knew$2} {3#his$3} {#*{5#address$5}*$}{6#,$6} {7#but$7} {8#I$8} {11#cannot$11} {10#think$10} {4#of$4} {9#it$9} at the moment{13#.$13}",
              "IME": null,
              "M": 17,
              "SIG": "47A307BCBF3FAB9531FFC48A168BF2DF",
              "TG": null,
              "URL": "http://learning.sohu.com/20040906/n221901517.shtml",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 28,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975564000-0800)/",
            "ID": 260637,
            "ORAL": true,
            "R": 65535,
            "READ": 100,
            "S": {
              "AD": "{1#fēng pí$1} {2#shàng$2} {3#méi yǒu$3} {4#míng zì$4} {5#hé$5} {##*{6#dì zhǐ$6}*$$} {7#。$7}",
              "COL": null,
              "D": "{1#封皮$1}{2#上$2}{3#没有$3}{4#名字$4}{5#和$5}{##*{6#地址$6}*$$}{7#。$7}",
              "IME": null,
              "M": 0,
              "SIG": "11B44689B17EC6EDF54CF69EF5464DE6",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "There was {3#no$3} {4#name$4} {5#or$5} {#*{6#address$6}*$} {2#on$2} the {1#front$1}{7#.$7}",
              "IME": null,
              "M": 1,
              "SIG": "6ED5E69B5BD37FB8E71AD2AD77D4F0C1",
              "TG": null,
              "URL": "http://article.yeeyan.org/compare/163378/125808",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 17,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975547000-0800)/",
            "ID": 299165,
            "ORAL": false,
            "R": 65535,
            "READ": 95,
            "S": {
              "AD": "{1#zhè shí$1} {2#ài dé huá zī$2} {3#zhàn$3} {4#qǐ shēn$4} {5#,$5} {6#duì$6} {7#shí èr$7} {8#rén$8} {##*{9#jiǎng huà$9}*$$} {10#。$10}",
              "COL": null,
              "D": "{1#这时$1}{2#爱德华兹$2}{3#站$3}{4#起身$4}{5#，$5}{6#对$6}{7#十二$7}{8#人$8}{##*{9#讲话$9}*$$}{10#。$10}",
              "IME": null,
              "M": 0,
              "SIG": "10A1AC6515147A27EB55CD5E45D77F37",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{1#Then$1} {2#Edwards$2} {3#got$3} {6#to$6} his {4#feet$4} to {#*{9#address$9}*$} the {7#twelve$7}{10#.$10}",
              "IME": null,
              "M": 1,
              "SIG": "EAFEA7CB980AD370F9AA7C1B059C8BB8",
              "TG": null,
              "URL": "http://bbs.rtucn.com/ipb/index.php?act=Print&client=html&f=14&t=17319",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 21,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975530000-0800)/",
            "ID": 60713,
            "ORAL": false,
            "R": 65535,
            "READ": 68,
            "S": {
              "AD": "{1#wǒ$1} {2#de$2} {3#IP$3} {##*{4#dì zhǐ$4}*$$} {5#xiǎn shì$5} {6#de$6} {7#bú shi$7} {8#yuán lái$8} {9#de$9} {10#chéng shì$10} {11#,$11} {12#ér shì$12} {13#hé$13} {14#tā$14} {15#tóng$15} {16#yī gè$16} {17#chéng shì$17} {18#。$18}",
              "COL": null,
              "D": "{1#我$1}{2#的$2}{3#IP$3}{##*{4#地址$4}*$$}{5#显示$5}{6#的$6}{7#不是$7}{8#原来$8}{9#的$9}{10#城市$10}{11#，$11}{12#而是$12}{13#和$13}{14#他$14}{15#同$15}{16#一个$16}{17#城市$17}{18#。$18}",
              "IME": null,
              "M": 0,
              "SIG": "2EF93DAB347F412284BC4CEA1FDAB007",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{1#My$1} {3#IP$3} {#*{4#address$4}*$} is {5#displayed$5} is {7#not$7} {2#the$2} {8#original$8} {17#city$17}{11#,$11} {12#but$12} {15#with$15} {14#him$14} in {16#a$16} {10#city$10}{18#.$18}",
              "IME": null,
              "M": 1,
              "SIG": "23E4C7B7984B25690B2E63FD96956552",
              "TG": null,
              "URL": "http://www.dota123.com/shuihuzhuan/shuihuchuan-news/huaqiang-shier.html",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 36,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975527000-0800)/",
            "ID": 284354,
            "ORAL": false,
            "R": 65535,
            "READ": 89,
            "S": {
              "AD": "{1#wǒ$1} {2#zhī dào$2} {3#tā$3} {4#de$4} {##*{5#dì zhǐ$5}*$$} {6#,$6} {7#dàn$7} {8#wǒ$8} {9#cǐ kè$9} {10#bù$10} {11#jì dé$11} {12#le$12} {13#。$13}",
              "COL": null,
              "D": "{1#我$1}{2#知道$2}{3#他$3}{4#的$4}{##*{5#地址$5}*$$}{6#，$6}{7#但$7}{8#我$8}{9#此刻$9}{10#不$10}{11#记得$11}{12#了$12}{13#。$13}",
              "IME": null,
              "M": 0,
              "SIG": "7B749D031E050FC2F8571B7D4A893E76",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{1#I$1} {2#know$2} {3#his$3} {#*{5#address$5}*$}{6#,$6} {7#but$7} {8#I$8} {10#cannot$10} think {4#of$4} it at the {9#moment$9}{13#.$13}",
              "IME": null,
              "M": 17,
              "SIG": "73B44D0AA49F7AEF30E3B3EAE9A59110",
              "TG": null,
              "URL": "http://www.uuzone.com/blog/any_time/85619.htm",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 28,
            "WAD": null
          }
        ],
        "TOTAL": 30100
      },
      "SUGG": {
        "AC": null,
        "PH": [
          {
            "DEF": "地址$$称呼$$演说$$处理$$致辞$$满足$$姓名$$应付$$谈吐$$交$$委托$$引导$$寒喧$$正式请愿$$风度$$求爱$$献殷勤$$灵巧$$娴熟$$在…上写姓名住址$$向…致意$$引见$$给…讲话$$向…演说$$向…求爱$$向…献殷勤$$请求撤销职务$$瞄准",
            "SIG": "5E4DA50643DCD624689B005E9579BDF2",
            "V": "addressed"
          },
          {
            "DEF": "地址$$称呼$$演说$$处理$$致辞$$满足$$姓名$$应付$$谈吐$$交$$委托$$引导$$寒喧$$正式请愿$$风度$$求爱$$献殷勤$$灵巧$$娴熟$$在…上写姓名住址$$向…致意$$引见$$给…讲话$$向…演说$$向…求爱$$向…献殷勤$$请求撤销职务$$瞄准",
            "SIG": "0681CFAC2C48B0A4BC6E432D9C203202",
            "V": "addresses"
          },
          {
            "DEF": "议院答辞$$总统咨文$$撤职请求",
            "SIG": "748D7B0FE14F2D5C5A40D5E9465ADBCF",
            "V": "the Address"
          },
          {
            "DEF": "相并,并肩;并列;并排;看齐",
            "SIG": "C0228D666028D4907D5C05D2F7BA5ADA",
            "V": "abreast"
          },
          {
            "DEF": "逮捕$$阻止$$抑制$$拘捕$$停止$$扣留$$吸引$$拘留$$止住$$收押$$制动",
            "SIG": "145CF552B5ED6EAC8D1EF0558970F7B3",
            "V": "arrest"
          }
        ],
        "PY": null,
        "SP": null
      }
    }

解析：

- `LEX`
	- `C_DEF`：英-汉
		- `POS`：词性。PS：若该值为 `web`，则是必应词典中的`互联网释义`的内容
		- `SEN`：
			- `D`：释义
			- `R`：???
			- `STS`
				- `S`
					- `D`：例句
				- `T`
					- `D`：例句翻译
			- `URL`：参考链接
	- `H_DEF`：英-英
		- `POS`：词性。PS：若该值为 `web`，则是必应词典中的`互联网释义`的内容
		- `SEN`：
			- `D`：例句
			- `URL`：参考链接
	- `THES`：同义词和反义词
		- `A`：反义词列表
		- `POS`：词性
		- `S`：同义词列表
	- `PRON`：音标
		- `L`：地区，取 `US` 或 `UK`
		- `V`：音标
	- `PHRASE`：词组列表
		- `DEF`：词组翻译
		- `SIG`：???
		- `V`：词组
	- `INF`：其他形式
		- `IE`：形式
		- `T`：什么式，取 `pl`(复数)、`pp`(过去分词)、`prp`(现在分词)、`3pps`(第三人称单数)、`s`(原型)、`prt`(现在式)、`pt`(过去式)
- `SENT`：例句
	- `COUNT`：数量
	- `OFFSET`：分页
	- `ST`
		- `S`：例句翻译信息
			- `AD`：拼音
			- `D`：例句翻译
		- `T`：例句信息
			- `D`：例句

<h2 id="translation">翻译</h2>

url：https://dict.bing.com.cn/api/http/v2/4154AA7A1FC54ad7A84A0236AA4DCAF3/en-us/zh-cn/

拼接参数：

- `q`：查询内容，使用 `+` 将多个单词连接起来
- `format`：返回内容格式。`application/xml` 或 `application/json`

url 示例：[`https://dict.bing.com.cn/api/http/v2/4154AA7A1FC54ad7A84A0236AA4DCAF3/en-us/zh-cn/?q=merry+me&format=application/json`](https://dict.bing.com.cn/api/http/v2/4154AA7A1FC54ad7A84A0236AA4DCAF3/en-us/zh-cn/?q=merry+me&format=application/json)

json 示例：

	{
      "LEX": {
        "C_DEF": [
          {
            "DEF": null,
            "POS": "web",
            "SEN": [
              {
                "D": "等你愿意",
                "R": 21,
                "STS": null,
                "URL": "http://tw.knowledge.yahoo.com/question/question?qid=1306070310435"
              },
              {
                "D": "我嫁给你",
                "R": 4,
                "STS": null,
                "URL": "http://blog.yam.com/jamie690526/article/41776830"
              },
              {
                "D": "珍宝箱",
                "R": 3,
                "STS": null,
                "URL": "http://www.topbester.com/ebook/view/8163.html"
              },
              {
                "D": "爱戴",
                "R": 2,
                "STS": null,
                "URL": "http://www.aiyae.cn/fashion/ny/bra/"
              },
              {
                "D": "败香心得",
                "R": 2,
                "STS": null,
                "URL": "http://www.xici.net/d139286593.htm"
              },
              {
                "D": "麦瑞蜜",
                "R": 2,
                "STS": null,
                "URL": "http://www.people.com.cn/h/2011/0721/c25408-3243172348.html"
              },
              {
                "D": "愤怒的胖子",
                "R": 1,
                "STS": null,
                "URL": "http://www.3sir.com/3s/i9e-1c-7a-ac-4d-0d-aa-0d-4e-cb-3d-db-2e-dc-eb-1b-7c-cb-ac-1b-r.html"
              }
            ]
          }
        ],
        "HW": {
          "DEF": null,
          "SIG": "C1C9F0999D7018DFE163908D0098A266",
          "V": "merry me"
        },
        "H_DEF": null,
        "INF": null,
        "LCS": null,
        "PHRASE": null,
        "PRON": null,
        "THES": null
      },
      "MT": null,
      "Q": "merry me",
      "SENT": {
        "COUNT": 10,
        "OFFSET": 0,
        "ST": [
          {
            "DATE": "/Date(1384975541000-0800)/",
            "ID": 8203258,
            "ORAL": true,
            "R": 47998,
            "READ": 80,
            "S": {
              "AD": "{1#jià gěi$1} {##*{2#wǒ$2}*$$} {3#,$3} {4#zhū lì yè$4} {5#。$5} {6#nǐ$6} {7#bù$7} {8#zài$8} {9#gū dú$9} {10#le$10} {11#。$11}",
              "COL": null,
              "D": "{1#嫁给$1}{##*{2#我$2}*$$}{3#，$3}{4#朱丽叶$4}{5#。$5}{6#你$6}{7#不$7}{8#在$8}{9#孤独$9}{10#了$10}{11#。$11}",
              "IME": null,
              "M": 0,
              "SIG": "9DE84C6BED3585184DFD7610ED225F54",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{#*merry*$} {#*{2#me$2}*$}{3#,$3} {4#juliet$4}{5#.$5} {6#you$6}'ll {7#never$7} have {8#to$8} been {9#alone$9}{11#.$11}",
              "IME": null,
              "M": 1,
              "SIG": "3A0B6F93E75460F671619266251EEE5F",
              "TG": null,
              "URL": "http://blog.sina.com.cn/s/blog_5e3f02650100cajw.html",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 24,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975544000-0800)/",
            "ID": 698601,
            "ORAL": false,
            "R": 62303,
            "READ": 84,
            "S": {
              "AD": "{1#tā$1} {2#fù mǔ$2} {3#bù$3} {4#yǔn xǔ$4} {##*{5#wǒ$5}*$$} {6#gēn$6} {7#tā$7} {8#jié hūn$8} {9#。$9}",
              "COL": null,
              "D": "{1#她$1}{2#父母$2}{3#不$3}{4#允许$4}{##*{5#我$5}*$$}{6#跟$6}{7#她$7}{8#结婚$8}{9#。$9}",
              "IME": null,
              "M": 0,
              "SIG": "6F5BAC7FF01FDA572750EA5869382BA7",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{1#Her$1} {2#parents$2} would {3#not$3} {4#permit$4} her {6#to$6} {#*merry*$} {#*{5#me$5}*$}{9#.$9}",
              "IME": null,
              "M": 17,
              "SIG": "584233065B2457389F18A1981D0FF558",
              "TG": null,
              "URL": "http://www.kuxue.com/201106/532.htm",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 19,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975535000-0800)/",
            "ID": 17486916,
            "ORAL": true,
            "R": 10693,
            "READ": 100,
            "S": {
              "AD": "{1#jià gěi$1} {2#wǒ$2} {##*{3#ba$3}*$$} {4#。$4} {##*{5#wǒ$5}*$$} {6#huì$6} {7#gěi$7} {8#nǐ$8} {9#xìng fú$9} {10#de$10} {11#。$11} {12#($12} {13#dì$13} {14#jiè zhi$14} {15#hé$15} {16#)$16}",
              "COL": null,
              "D": "{1#嫁给$1}{2#我$2}{##*{3#吧$3}*$$}{4#。$4}{##*{5#我$5}*$$}{6#会$6}{7#给$7}{8#你$8}{9#幸福$9}{10#的$10}{11#。$11}{12#（$12}{13#递$13}{14#戒指$14}{15#盒$15}{16#）$16}",
              "IME": null,
              "M": 0,
              "SIG": "EA84E70265D2222B2E8992D5EA522CBF",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "Would {8#you$8} {#*{3#merry$3}*$} {#*{5#me$5}*$}? {2#I$2} swear we {6#will$6} be {9#happy$9}{4#.$4} {12#($12}{13#pass$13} {10#the$10} {14#ring$14} {15#box$15}{4#.$4} {16#)$16}",
              "IME": null,
              "M": 1,
              "SIG": "BFEF271A83D0D0C94A5B803B322815D8",
              "TG": null,
              "URL": "http://zhidao.baidu.com/question/184842837.html",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 35,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975514000-0800)/",
            "ID": 739601,
            "ORAL": true,
            "R": 62005,
            "READ": 87,
            "S": {
              "AD": "{1#shì$1} {2#shí hou$2} {3#qìng zhù$3} {4#zhè ge$4} {5#wéi yī$5} {6#yǒu$6} {7#kě néng$7} {8#bǐ$8} {##*{9#wǒ$9}*$$} {10#hái$10} {11#ài$11} {12#nǐ$12} {13#de$13} {14#rén$14} {15#de$15} {16#shēng rì$16} {17#le$17} {18#。$18} {19#shèng dàn$19} {##*{20#kuài lè$20}*$$} {21#,$21} {22#wǒ$22} {23#qīn ài de$23} {24#。$24}",
              "COL": null,
              "D": "{1#是$1}{2#时候$2}{3#庆祝$3}{4#这个$4}{5#唯一$5}{6#有$6}{7#可能$7}{8#比$8}{##*{9#我$9}*$$}{10#还$10}{11#爱$11}{12#你$12}{13#的$13}{14#人$14}{15#的$15}{16#生日$16}{17#了$17}{18#。$18}{19#圣诞$19}{##*{20#快乐$20}*$$}{21#，$21}{22#我$22}{23#亲爱的$23}{24#。$24}",
              "IME": null,
              "M": 0,
              "SIG": "9310FEFE369060BFF8A41CE85D7EABFA",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{2#Time$2} to {3#celebrate$3} {4#the$4} {16#birth$16} {13#of$13} the {5#only$5} {14#one$14} who {7#could$7} {11#love$11} {12#you$12} more {8#than$8} {#*{9#me$9}*$}{18#.$18} {#*{20#Merry$20}*$} {19#Christmas$19} to {12#you$12} my {23#darling$23}!",
              "IME": null,
              "M": 1,
              "SIG": "A19F737A856327BD712BD552C27DDC30",
              "TG": null,
              "URL": "http://article.yeeyan.org/view/339854/339704",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 48,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975584000-0800)/",
            "ID": 2448591,
            "ORAL": true,
            "R": 55717,
            "READ": 68,
            "S": {
              "AD": "{1#xǔ duō$1} {2#ài liàn$2} {3#de$3} {4#zhù yuàn$4} {5#,$5} {6#xiàn gěi$6} {##*{7#wǒ$7}*$$} {8#de$8} {9#ài rén$9} {10#,$10} {11#nǐ$11} {12#yǒng yuǎn$12} {13#shì$13} {14#wǒ$14} {15#zuì měi hǎo$15} {17#de$17} {18#shèng dàn$18} {19#lǐ wù$19} {20#hé$20} {21#wǒ$21} {22#de$22} {23#yí qiè$23} {24#shèng dàn$24} {25#kuài lè$25} {26#!$26}",
              "COL": null,
              "D": "{1#许多$1}{2#爱恋$2}{3#的$3}{4#祝愿$4}{5#，$5}{6#献给$6}{##*{7#我$7}*$$}{8#的$8}{9#爱人$9}{10#，$10}{11#你$11}{12#永远$12}{13#是$13}{14#我$14}{15#最美好$15}{17#的$17}{18#圣诞$18}{19#礼物$19}{20#和$20}{21#我$21}{22#的$22}{23#一切$23}{24#圣诞$24}{25#快乐$25}{26#！$26}",
              "IME": null,
              "M": 0,
              "SIG": "4EE93E884ECF9BA830CB375E7DD845B2",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{1#Lots$1} {3#of$3} {2#loving$2} {4#wishes$4} {6#for$6} my {9#sweetheart$9} who'll {12#always$12} {13#be$13} my {15#nicest$15} {18#Christmas$18} {19#gift$19} {20#and$20} {23#everything$23} to {#*{7#me$7}*$}{5#,$5} {#*Merry*$} {24#Christmas$24}{26#!$26}",
              "IME": null,
              "M": 17,
              "SIG": "D8E416A614597D1CFF66B1902E389462",
              "TG": null,
              "URL": "http://bbs.bjhr.gov.cn/dispbbs.asp?boardID=70&amp;ID=52976&amp;page=2",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 49,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975535000-0800)/",
            "ID": 12503221,
            "ORAL": true,
            "R": 37899,
            "READ": 82,
            "S": {
              "AD": "{1#néng$1} {2#gěi$2} {##*{3#wǒ$3}*$$} {4#yī$4} {5#zhāng$5} {6#nǐ$6} {7#de$7} {8#zhào piàn$8} {9#ma$9} {10#?$10} {11#zhè yàng$11} {12#,$12} {13#shèng dàn lǎo rén$13} {14#jiù$14} {15#zhī dào$15} {16#sòng$16} {17#wǒ$17} {18#shén me$18} {19#lǐ wù$19} {20#la$20} {21#,$21} {22#shèng dàn$22} {##*{23#kuài lè$23}*$$} {24#!$24}",
              "COL": null,
              "D": "{1#能$1}{2#给$2}{##*{3#我$3}*$$}{4#一$4}{5#张$5}{6#你$6}{7#的$7}{8#照片$8}{9#吗$9}{10#？$10}{11#这样$11}{12#，$12}{13#圣诞老人$13}{14#就$14}{15#知道$15}{16#送$16}{17#我$17}{18#什么$18}{19#礼物$19}{20#啦$20}{21#，$21}{22#圣诞$22}{##*{23#快乐$23}*$$}{24#！$24}",
              "IME": null,
              "M": 0,
              "SIG": "0B5202033058EF71881BB32C7A2B6B5C",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "{1#Can$1} {3#I$3} have {6#your$6} {8#picture$8}{12#,$12} {11#so$11}{21#,$21} {13#Santa Claus$13} {15#knows$15} exactly {18#what$18} {2#to$2} {16#give$16} {#*{3#me$3}*$}{24#.$24} {#*{23#merry$23}*$} {22#Christmas$22}.",
              "IME": null,
              "M": 1,
              "SIG": "6AE98593BC8E51D26A321F3F14C64C76",
              "TG": null,
              "URL": "http://www.en8848.com.cn/kouyu/use/greeting/148857.html",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 44,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975527000-0800)/",
            "ID": 2167473,
            "ORAL": false,
            "R": 56355,
            "READ": 100,
            "S": {
              "AD": "{1#bú shì$1} {2#yī$2} {3#pí náng$3} {4#de$4} {5#jiǔ$5} {6#,$6} {7#yīn wèi$7} {8#yī$8} {9#pí náng$9} {10#de$10} {11#jiǔ huì$11} {12#ràng$12} {13#wǒ$13} {14#zuì$14} {15#dǎo$15} {16#,$16} {17#huì$17} {18#shǐ$18} {##*{19#wǒ$19}*$$} {20#chéng wéi$20} {21#yī gè$21} {22#shǎ guā$22} {23#。$23} {24#jiù$24} {25#zhǐ shì$25} {26#yī$26} {27#xiǎo$27} {28#bēi$28} {29#jiǔ$29} {30#,$30} {31#ràng$31} {32#wǒ$32} {33#nuǎn huo$33} {34#yí xià$34} {35#。$35}",
              "COL": null,
              "D": "{1#不是$1}{2#一$2}{3#皮囊$3}{4#的$4}{5#酒$5}{6#，$6}{7#因为$7}{8#一$8}{9#皮囊$9}{10#的$10}{11#酒会$11}{12#让$12}{13#我$13}{14#醉$14}{15#倒$15}{16#，$16}{17#会$17}{18#使$18}{##*{19#我$19}*$$}{20#成为$20}{21#一个$21}{22#傻瓜$22}{23#。$23}{24#就$24}{25#只是$25}{26#一$26}{27#小$27}{28#杯$28}{29#酒$29}{30#，$30}{31#让$31}{32#我$32}{33#暖和$33}{34#一下$34}{35#。$35}",
              "IME": null,
              "M": 0,
              "SIG": "23C8021EDBEA54DF9BF23BEC5C473192",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "Not {21#a$21} {3#skin$3} of {29#wine$29}{23#.$23} {7#For$7} {21#a$21} {9#skin$9} of {5#wine$5} {17#would$17} {18#make$18} {13#me$13} {#*merry*$}{6#,$6} and {22#foolish$22}{35#.$35} {25#Merely$25} {21#a$21} {28#cup$28} of {5#wine$5}{16#,$16} to {33#warm$33} {#*{19#me$19}*$}.",
              "IME": null,
              "M": 1,
              "SIG": "6B16ED0B1C918B3EE947DDC66798C08E",
              "TG": null,
              "URL": "http://www.odyguild.net/bbs/thread-16295-1-1.html",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 64,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975566000-0800)/",
            "ID": 10308900,
            "ORAL": false,
            "R": 45037,
            "READ": 78,
            "S": {
              "AD": "{1#xià rì$1} {2#wēn nuǎn$2} {3#de$3} {4#zǎo chén$4} {5#shǐ$5} {##*{6#wǒ$6}*$$} {7#xīn qíng$7} {8#shū chàng$8} {9#。$9}",
              "COL": null,
              "D": "{1#夏日$1}{2#温暖$2}{3#的$3}{4#早晨$4}{5#使$5}{##*{6#我$6}*$$}{7#心情$7}{8#舒畅$8}{9#。$9}",
              "IME": null,
              "M": 0,
              "SIG": "385688C1FF832209990C4C837194C9C1",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "A {2#warm$2} {1#summer$1} {4#morning$4} {5#makes$5} {#*{6#me$6}*$} {#*merry*$}{9#.$9}",
              "IME": null,
              "M": 1,
              "SIG": "61F0EB7B91ADDE4A5C741DD6357055AA",
              "TG": null,
              "URL": "http://wwyk08.blog.163.com/blog/static/95550477200911284433244",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 17,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975565000-0800)/",
            "ID": 15755609,
            "ORAL": true,
            "R": 16260,
            "READ": 54,
            "S": {
              "AD": "{1#duì bu qǐ$1} {2#,$2} {3#ràng$3} {4#yí xià$4} {2#,$2} {6#ràng$6} {7#yí xià$7} {8#-$8} {9#shèng dàn$9} {##*{10#kuài lè$10}*$$}",
              "COL": null,
              "D": "{1#对不起$1}{2#，$2}{3#让$3}{4#一下$4}{2#，$2}{6#让$6}{7#一下$7}{8#-$8}{9#圣诞$9}{##*{10#快乐$10}*$$}",
              "IME": null,
              "M": 0,
              "SIG": "6C33FE0DE57EB4053905D37DB3D26986",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "sorry . {1#excuse$1} me {2#,$2} {1#excuse$1} {#*me*$} . {8#-$8} {#*{10#merry$10}*$} {9#christmas$9}",
              "IME": null,
              "M": 1,
              "SIG": "53D0548F1680690CA7E56BEF189B79D4",
              "TG": null,
              "URL": "http://www.ichacha.net/merry.html",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 21,
            "WAD": null
          },
          {
            "DATE": "/Date(1384975526000-0800)/",
            "ID": 1902661,
            "ORAL": false,
            "R": 57041,
            "READ": 74,
            "S": {
              "AD": "{1#tā$1} {2#dòng zuò$2} {3#mǐn jié$3} {4#de$4} {5#bǎ$5} {6#huā shù$6} {5#gěi$5} {8#le$8} {9#wǒ$9} {10#,$10} {11#zhù$11} {##*{12#wǒ$12}*$$} {13#shèng dàn$13} {##*{14#kuài lè$14}*$$} {15#,$15} {16#rán hòu$16} {17#lí kāi$17} {18#le$18} {19#。$19}",
              "COL": null,
              "D": "{1#他$1}{2#动作$2}{3#敏捷$3}{4#地$4}{5#把$5}{6#花束$6}{5#给$5}{8#了$8}{9#我$9}{10#，$10}{11#祝$11}{##*{12#我$12}*$$}{13#圣诞$13}{##*{14#快乐$14}*$$}{15#，$15}{16#然后$16}{17#离开$17}{18#了$18}{19#。$19}",
              "IME": null,
              "M": 0,
              "SIG": "2B80A73F385EEB4C3A4ADDF2BCDB2B0B",
              "TG": null,
              "URL": null,
              "W": null
            },
            "T": {
              "AD": null,
              "COL": null,
              "D": "In one {3#quick$3} {2#motion$2} {1#he$1} {5#gave$5} {9#me$9} the corsage{10#,$10} {11#wished$11} {#*{12#me$12}*$} a {#*{14#Merry$14}*$} {13#Christmas$13} {16#and$16} {17#departed$17}{19#.$19}",
              "IME": null,
              "M": 1,
              "SIG": "E72E95317C05A7A77779FB47D0A05F49",
              "TG": null,
              "URL": "http://dict.ebigear.com/w/merry/",
              "W": null
            },
            "TECH": false,
            "TITLE": false,
            "WA": 37,
            "WAD": null
          }
        ],
        "TOTAL": 44
      },
      "SUGG": {
        "AC": null,
        "PH": [
          {
            "DEF": "玛利一世(1516—1558,英国女王,在位期间1553—1558)",
            "SIG": "0A79AF279AAF1065D003CA4069BBF3B7",
            "V": "mary i"
          },
          {
            "DEF": "随从$$侍从",
            "SIG": "0C4D26C5B8B8BCA47C14CE01AA6F43C9",
            "V": "merry men"
          },
          {
            "DEF": "大麻",
            "SIG": "BEA1E16DF5DDD8268143C4770A420CF0",
            "V": "Mary Jane"
          },
          {
            "DEF": "",
            "SIG": "C56442FF8BEB540F2AB2890099614EEF",
            "V": "mark you"
          },
          {
            "DEF": "愉悦的气氛",
            "SIG": "BA5CBC6C5D2D2792F89BA8E7197705EA",
            "V": "merry mood"
          }
        ],
        "PY": null,
        "SP": null
      }
    }

解析：
同[词典](#dic)解析