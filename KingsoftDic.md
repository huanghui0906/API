# 金山词霸 #

- [联想](#associate)
- [释义](#explain)
- [翻译](#translation)

<h2 id="associate">联想</h2>

url：http://dict-mobile.iciba.com/interface/index.php

拼接参数：

- `c`：固定值 `word`
- `m`：固定值 `getsuggest`
- `nums`：返回数量
- `client`：固定值 `6`
- `is_need_mean`：固定值 `1`
- `word`：搜索词

示例 url：[`http://dict-mobile.iciba.com/interface/index.php?c=word&m=getsuggest&nums=10&client=6&is_need_mean=1&word=h`](http://dict-mobile.iciba.com/interface/index.php?c=word&m=getsuggest&nums=10&client=6&is_need_mean=1&word=h)

json 示例：

	{
      "status": 1,
      "message": [
        {
          "key": "hold",
          "value": 2170,
          "means": [
            {
              "part": "vt.",
              "means": [
                "拿住，握住",
                "保留，保存",
                "扣留，拘押",
                "容纳"
              ]
            },
            {
              "part": "vi.",
              "means": [
                "拿住，握住",
                "同意，赞成",
                "保持不变",
                "有效"
              ]
            },
            {
              "part": "n.",
              "means": [
                "握住",
                "保留",
                "控制"
              ]
            }
          ]
        },
        {
          "key": "hang",
          "value": 1943,
          "means": [
            {
              "part": "vt.",
              "means": [
                "悬挂",
                "（被）绞死",
                "贴，装饰",
                "使悬而未决"
              ]
            },
            {
              "part": "vi.",
              "means": [
                "悬垂",
                "被吊死",
                "附属，依靠",
                "悬而未决"
              ]
            },
            {
              "part": "n.",
              "means": [
                "悬挂的样子",
                "（动作的）暂停",
                "〈口〉大意，要点",
                "〈口〉做法，诀窍"
              ]
            }
          ]
        },
        {
          "key": "have",
          "value": 1883,
          "means": [
            {
              "part": "aux.",
              "means": [
                "用以构成完成式及完成式的不定式，表示已经…"
              ]
            },
            {
              "part": "vt.",
              "means": [
                "有，具有",
                "拿，取得",
                "从事",
                "必须，不得不"
              ]
            },
            {
              "part": "n.",
              "means": [
                "〈口〉有产者，有钱人",
                "富国",
                "〈英俚〉欺骗，诈骗"
              ]
            }
          ]
        },
        {
          "key": "hit",
          "value": 1809,
          "means": [
            {
              "part": "vt.& vi.",
              "means": [
                "打，打击",
                "碰撞"
              ]
            },
            {
              "part": "vt.",
              "means": [
                "击（球）",
                "（在精神上）打击（某人）",
                "猜中",
                "迎合"
              ]
            },
            {
              "part": "n.",
              "means": [
                "打，打击",
                "碰撞",
                "（演出等）成功",
                "批评，讽刺"
              ]
            },
            {
              "part": "vi.",
              "means": [
                "（风暴、疾病等）袭击",
                "抨击",
                "（偶然）碰上",
                "（突然）想到（与 on, upon 连用）"
              ]
            }
          ]
        },
        {
          "key": "heart",
          "value": 1771,
          "means": [
            {
              "part": "n.",
              "means": [
                "心，心脏",
                "感情",
                "要点",
                "胸部"
              ]
            },
            {
              "part": "vt.",
              "means": [
                "鼓励",
                "激励"
              ]
            },
            {
              "part": "vi.",
              "means": [
                "结心"
              ]
            }
          ]
        }
      ]
    }

解析：

- `status`：请求成功时为 `1`
- `message`：具体联想单词信息列表
	- `key`：联想单词
	- `value`：???
	- `means`：释义列表
		- `part`：词性
		- `means`：释义列表

<h2 id="explain">释义</h2>

url：http://www.iciba.com/index.php

拼接参数：

- `a`：固定值 `getWordMean`
- `c`：固定值 `search`
- `list`：以 `1,3,4,5,8,9,10,12,13,14,18,21,3003,3005` 为字符串进行组合
	- `1`：对应 json 中 `baesInfo` 字段，基础释义
	- `3`：对应 json 中 `collins` 字段，柯林斯高阶英汉双解学习词典
	- `4`：对应 json 中 `ee_mean` 字段，英英词典
	- `5`：对应 json 中 `trade_means` 字段，行业词典
	- `8`：对应 json 中 `sentence` 字段，双语例句
	- `9`：对应 json 中 `netmean` 字段，网络释义
	- `10`：对应 json 中 `auth_sentence` 字段，权威例句
	- `12`：对应 json 中 `synonym` 字段，同义词
	- `13`：对应 json 中 `antonym` 字段，反义词
	- `14`：对应 json 中 `phrase` 字段，词组搭配
	- `18`：对应 json 中 `encyclopedia` 字段，百科全书
	- `21`：对应 json 中 `cetFour` 字段，四级真题
	- `3003`：对应 json 中 `bidec` 字段，英汉双向大词典
	- `3005`：对应 json 中 `jushi` 字段，例句
- `word`：释义单词

url 示例：[`http://www.iciba.com/index.php?a=getWordMean&c=search&list=1%2C2%2C3%2C4%2C5%2C8%2C9%2C10%2C12%2C13%2C14%2C18%2C21%2C22%2C3003%2C3005&word=hello`](http://www.iciba.com/index.php?a=getWordMean&c=search&list=1%2C2%2C3%2C4%2C5%2C8%2C9%2C10%2C12%2C13%2C14%2C18%2C21%2C22%2C3003%2C3005&word=hello)

json 示例：

	{
      "errno": 0,
      "errmsg": "success",
      "baesInfo": {
        "word_name": "hello",
        "is_CRI": 1,
        "exchange": {
          "word_pl": [
            "hellos"
          ],
          "word_past": [],
          "word_done": [],
          "word_ing": [],
          "word_third": [],
          "word_er": [],
          "word_est": [],
          "word_prep": [],
          "word_adv": [],
          "word_verb": [],
          "word_noun": [],
          "word_adj": [],
          "word_conn": []
        },
        "symbols": [
          {
            "ph_en": "hə'ləʊ",
            "ph_am": "həˈloʊ",
            "ph_other": "",
            "ph_en_mp3": "",
            "ph_am_mp3": "http://res.iciba.com/resource/amp3/1/0/5d/41/5d41402abc4b2a76b9719d911017c592.mp3",
            "ph_tts_mp3": "http://res-tts.iciba.com/5/d/4/5d41402abc4b2a76b9719d911017c592.mp3",
            "parts": [
              {
                "part": "int.",
                "means": [
                  "哈喽，喂",
                  "你好，您好",
                  "表示问候",
                  "打招呼"
                ]
              },
              {
                "part": "n.",
                "means": [
                  "“喂”的招呼声或问候声"
                ]
              },
              {
                "part": "vi.",
                "means": [
                  "喊“喂”"
                ]
              }
            ]
          }
        ],
        "translate_type": 1
      },
      "trade_means": [
        {
          "word_trade": "计算机",
          "word_mean": [
            "【信】呼叫"
          ]
        }
      ],
      "sentence": [
        {
          "Network_id": "2305937",
          "Network_en": "I answered the phone and this voice went, \"Hello? Is that Alison?\"",
          "Network_cn": "我拿起电话，就听到这个声音：“喂？是艾利森吗？”",
          "tts_mp3": "http://res-tts.iciba.com/tts_new_dj//9/c/5/9c5d0ff9b35eebb6513dedcbebd1dab2.mp3",
          "tts_size": "23K",
          "source_type": 0,
          "source_id": 0,
          "source_title": "普通双语例句"
        },
        {
          "Network_id": "2316006",
          "Network_en": "A moment later, Cohen picked up the phone. \"Hello?\"",
          "Network_cn": "过了一会儿，科恩接起电话。“喂？”",
          "tts_mp3": "http://res-tts.iciba.com/tts_new_dj//3/2/a/32afb35883a6db321dc9fbfb1bce03b0.mp3",
          "tts_size": "19K",
          "source_type": 0,
          "source_id": 0,
          "source_title": "普通双语例句"
        },
        {
          "Network_id": "2370456",
          "Network_en": "\"Hello, I don't think we've met,\" Robert introduced himself.",
          "Network_cn": "“你好，我想我们还没有见过吧，”罗伯特自我介绍道。",
          "tts_mp3": "http://res-tts.iciba.com/tts_new_dj//d/d/4/dd4e191c23a5f6e41416d1cbbe9da999.mp3",
          "tts_size": "20K",
          "source_type": 0,
          "source_id": 0,
          "source_title": "普通双语例句"
        }
      ],
      "netmean": {
        "PerfectNetExp": [
          {
            "id": "13356",
            "key": "hello",
            "exp": "你好",
            "url": "http://wenku.baidu.com/view/17275e1252d380eb62946d48.html",
            "bas": 17040,
            "abs": "小学英语单词表_百度文库 ... Module 4 let′s 让我们 Hello 你好 Goodbye 再见."
          },
          {
            "id": "30576",
            "key": "hello",
            "exp": "哈罗",
            "url": "http://xh.5156edu.com/html3/5555.html",
            "bas": 6806,
            "abs": "哈字的解释---在线新华字典 ... 哈雷彗星〖 Halley’scomet;theHalleyComet〗 哈罗〖 hello〗 哈密〖 Kumul;Hami〗."
          },
          {
            "id": "65650",
            "key": "hello",
            "exp": "喂",
            "url": "http://www.docin.com/p-206550454.html",
            "bas": 2880,
            "abs": "初中英语单词表大全2182个带音标 - 豆丁网 ... fifteen 十五 44 hello 喂(问候或唤起注意) 45 please 请 46."
          },
          {
            "id": "121482",
            "key": "hello",
            "exp": "您好",
            "url": "http://wenku.baidu.com/view/39b6ca41336c1eb91a375dcd.html",
            "bas": 1344,
            "abs": "做一个有道德的人_百度文库 ... 晚安！ 6、老师再见！ see you everyone! 、 “您好”“ ”“ Hello” “请”“ ”“ please”."
          }
        ],
        "RelatedPhrase": [
          {
            "word": "hello kitty",
            "list": [
              {
                "id": "98200",
                "key": "hello kitty",
                "exp": "凯蒂猫",
                "url": "http://dj.iciba.com",
                "bas": 1756,
                "abs": "why hello kitty has no mouth ., 凯蒂猫为什么没有嘴巴."
              }
            ]
          },
          {
            "word": "hello summer",
            "list": [
              {
                "id": "9325",
                "key": "hello summer",
                "exp": "夏日甜心",
                "url": "http://www.youtube.com/playlist?list=PLMxdtc9UYU_rdstX2KeqsoF2-UmkwYtDc",
                "bas": 25873,
                "abs": "武艺Philip ✰... ... 2011 Dare - As One 敢不敢之在一起 2011 Hello Summer 夏日甜心 2010 Begin To Understand 开始懂了."
              }
            ]
          },
          {
            "word": "say hello",
            "list": [
              {
                "id": "323744",
                "key": "say hello",
                "exp": "打招呼",
                "url": "http://www.chinajiaoan.cn/you3/onews9.asp?id=3746",
                "bas": 368,
                "abs": "大班英语（学习单词）—幼儿园大班英语教案 ... 5. say good bye（ 说再见）。 1. say hello( 打招呼)： 2. warm up( 热身运动)：."
              }
            ]
          },
          {
            "word": "hello baby",
            "list": [
              {
                "id": "19439",
                "key": "hello baby",
                "exp": "哈罗宝贝",
                "url": "http://tw.mag.cnyes.com/Content/20110113/F13FC3E6257749BBAF082DA7DB6474EF.shtml",
                "bas": 11299,
                "abs": "目前旗下自有品牌有贝喜力克（Basilic）与哈罗宝贝（Hello Baby），产品则专注于奶嘴、奶瓶、奶粉盒、喂药器与固齿器等小型婴幼 …"
              },
              {
                "id": "40617",
                "key": "hello baby",
                "exp": "你好宝贝",
                "url": "http://zhidao.baidu.com/question/168012638.html",
                "bas": 4983,
                "abs": "求英语翻译_百度知道 ... courage to hug 拥抱的勇气 hello baby 你好宝贝 to cuddle 相拥而卧."
              }
            ]
          }
        ]
      },
      "synonym": [
        {
          "part_name": "n.",
          "means": [
            {
              "word_mean": "表示问候",
              "cis": [
                "greetings",
                "good",
                "salutations",
                "day"
              ]
            }
          ]
        },
        {
          "part_name": "",
          "means": [
            {
              "word_mean": "其他释义",
              "cis": [
                "day",
                "salute",
                "greeting",
                "salutation",
                "good"
              ]
            }
          ]
        }
      ],
      "encyclopedia": {
        "image": "",
        "url": "http://baike.baidu.com/view/4741.htm",
        "content": " 演唱：莱昂纳尔·里奇（Lionel Richie） 这是一首85年的冠军金曲 HELLO I've been alone with you inside my mind And in my dreams I've kissed your lips a thousand times I sometimes see you pass outside my door Hello, is it me you're looking for? I can see it in your eyes I can see it in your smile You're all I've ever wanted, (and) my arms are open wide 'Cause you know just what to say And you know jus"
      },
      "collins": [
        {
          "entry": [
            {
              "posp": "CONVENTION",
              "tran": "哈罗;你好",
              "def": "You say 'Hello' to someone when you meet them.",
              "example": [
                {
                  "ex": "Hello, Trish...",
                  "tran": "你好，特里茜。",
                  "tts_mp3": "http://res-tts.iciba.com/tts_dj/8/6/4/864e12ad6ce80d24e1ba37e053926db9.mp3",
                  "tts_size": "7K"
                },
                {
                  "ex": "Do you want to pop your head in and say hallo to my girlfriend?",
                  "tran": "你要不要进来和我女友打个招呼？",
                  "tts_mp3": "http://res-tts.iciba.com/tts_dj/8/9/a/89a65a15f9484c27baa044eaaae6aa5e.mp3",
                  "tts_size": "18K"
                }
              ]
            },
            {
              "posp": "CONVENTION",
              "tran": "（打电话时的招呼语）喂",
              "def": "You say 'Hello' to someone at the beginning of a telephone conversation, either when you answer the phone or before you give your name or say why you are phoning.",
              "example": [
                {
                  "ex": "A moment later, Cohen picked up the phone. 'Hello?'",
                  "tran": "过了一会儿，科恩接起电话。“喂？”",
                  "tts_mp3": "http://res-tts.iciba.com/tts_dj/5/d/0/5d0adc572a923f70295005dad2c016ef.mp3",
                  "tts_size": "19K"
                },
                {
                  "ex": "Hallo, may I speak to Frank, please.",
                  "tran": "喂，我找弗兰克。",
                  "tts_mp3": "http://res-tts.iciba.com/tts_dj/7/f/7/7f7ecf52c91adc778a7f830e82abf9c5.mp3",
                  "tts_size": "15K"
                }
              ]
            },
            {
              "posp": "CONVENTION",
              "tran": "（用于引起别人注意）喂",
              "def": "You can call 'hello' to attract someone's attention.",
              "example": [
                {
                  "ex": "She could see the open door of a departmental office. 'Hello! Excuse me. This is the department of French, isn't it?'...",
                  "tran": "她看到一个系办公室的门开着。“喂！请问，这是法语系，对吗？”",
                  "tts_mp3": "http://res-tts.iciba.com/tts_dj/b/6/f/b6fec747bebb7612e7c87284c50443a4.mp3",
                  "tts_size": "46K"
                },
                {
                  "ex": "Very softly, she called out: 'Hallo? Who's there?'",
                  "tran": "她轻声细气喊道：“喂？有人吗？”",
                  "tts_mp3": "http://res-tts.iciba.com/tts_dj/1/8/1/1813d136cd08698cd45940c3e8b72bce.mp3",
                  "tts_size": "20K"
                }
              ]
            }
          ]
        }
      ],
      "ee_mean": [
        {
          "part_name": "Noun",
          "means": [
            {
              "word_mean": "1. an expression of greeting;",
              "sentences": [
                {
                  "sentence": "\"every morning they exchanged polite hellos\""
                }
              ]
            }
          ]
        }
      ],
      "auth_sentence": [
        {
          "id": "22993",
          "content": "Hello - some responses to some of your points.",
          "link": "http://www.bbc.co.uk/blogs/theeditors/2007/05/suggestions_box.html",
          "short_link": "http://www.bbc.co.uk/8kw5s",
          "source": "BBC",
          "score": "1",
          "cache_status": "1",
          "tts_mp3": "http://res-tts.iciba.com/tts_authority/7/4/5/74562d88262e506cebe79879155c345d.mp3",
          "tts_size": "15.0",
          "diff": "2",
          "oral": "1",
          "res_content": "<b>Hello</b> - some responses to some of your points.",
          "res_content_con": "Hello - some responses to some of your points.",
          "res_key": "74562d88262e506cebe79879155c345d",
          "source_type": 0,
          "source_id": 0,
          "source_title": "普通权威例句"
        },
        {
          "id": "58450",
          "content": "Hello, focus on what's important in life.",
          "link": "http://online.wsj.com/community/86b3f6ab-6a73-4d5a-b5b4-09c6da4b7a5e/activity",
          "short_link": "http://asia.wsj.com/yyjsn",
          "source": "WSJ",
          "score": "1",
          "cache_status": "1",
          "tts_mp3": "http://res-tts.iciba.com/tts_authority/4/5/9/45925c53c74f0554e794ef1301dc7da6.mp3",
          "tts_size": "15.0",
          "diff": "1",
          "oral": "1",
          "res_content": "<b>Hello</b>, focus on what's important in life.",
          "res_content_con": "Hello, focus on what's important in life.",
          "res_key": "45925c53c74f0554e794ef1301dc7da6",
          "source_type": 0,
          "source_id": 0,
          "source_title": "普通权威例句"
        },
        {
          "id": "93924",
          "content": "I say hello and offer a hand in greeting.",
          "link": "http://www.thetimes.co.uk/tto/life/article3592197.ece",
          "short_link": "http://www.thetimes.co.uk/82buh",
          "source": "THETIMES",
          "score": "1",
          "cache_status": "1",
          "tts_mp3": "http://res-tts.iciba.com/tts_authority/e/4/7/e474cdfb8c160c66794037b75eb2be5b.mp3",
          "tts_size": "13.0",
          "diff": "1",
          "oral": "0",
          "res_content": "I say <b>hello</b> and offer a hand in greeting.",
          "res_content_con": "I say hello and offer a hand in greeting.",
          "res_key": "e474cdfb8c160c66794037b75eb2be5b",
          "source_type": 0,
          "source_id": 0,
          "source_title": "普通权威例句"
        }
      ],
      "bidec": {
        "word_name": "hello",
        "parts": [
          {
            "part_name": "interj.",
            "word_id": "20092",
            "part_id": "26780",
            "means": [
              {
                "word_mean": "喂",
                "part_id": "26780",
                "mean_id": "50506",
                "sentences": [
                  {
                    "en": "Hello, Brooks!How are you?",
                    "cn": "喂, 布鲁克斯!你好吗?"
                  }
                ]
              }
            ]
          }
        ]
      },
      "jushi": [
        {
          "english": "Hello,Brooks!How are you?",
          "chinese": "喂,布鲁克斯!你好吗?",
          "mp3": "http://res-tts.iciba.com/tts_synusage/c/2/2/c22734dcdc231e646434c320d81740b4.mp3"
        },
        {
          "english": "Hello, who is speaking, please?",
          "chinese": "喂,请问是谁呀?",
          "mp3": "http://res-tts.iciba.com/tts_synusage/b/7/3/b738ffa4f7de074f7916df487d0e10e6.mp3"
        },
        {
          "english": "Hello!Is there anybody there?",
          "chinese": "喂!有人吗?",
          "mp3": "http://res-tts.iciba.com/tts_synusage/6/e/4/6e460d1cdd682c180949c39bed30faee.mp3"
        }
      ],
      "_word_flag": 1,
      "exchanges": [
        "hellos",
        "hello"
      ]
    }

解析：

- `errno`：请求成功时返回 `0`
- `errmsg`：请求失败时返回错误信息，否则返回 `success`
- `baseInfo`：基础信息
	- `word_name`：
	- `exchange`：其他形式
		- `word_pl`：复数形式
		- `word_third`：第三人称单数
		- `word_past`：过去分词
		- `word_done`：现在分词
		- `word_ing`：正在进行时
		- `word_er`：比较式
		- `word_est`：最高级
		- `word_prep`：介词形式
		- `word_adv`：副词形式
		- `word_verb`：动词形式
		- `word_noun`：名词形式
		- `word_adj`：形容词形式
		- `word_conn`：连词形式
	- `symbols`：发音信息
		- `ph_en`：美式英标
		- `ph_am`：英式音标
		- `ph_en_mp3`：英式发音
		- `ph_am_mp3`：
		- `parts`：词性信息，同[联想](#associate)
- `sameAnalysis`：简单分析
	- `part_name`：解释
	- `means`：释义列表
		- `word_list`：相近含义单词
		- `means`：相近含义单词释义
- ... // 后续太长，笔者此处不做扩展，详情可对照网页和 json 自行解析

<h2 id="translation">翻译</h2>

url：http://fy.iciba.com/ajax.php

拼接参数：

- `a`：固定值 `fy`
- `f`：原文内容类型，日语取 `ja`，中文取 `zh`，英语取 `en`，韩语取 `ko`，德语取 `de`，西班牙语取 `es`，法语取 `fr`，自动则取 `auto`
- `t`：译文内容类型，日语取 `ja`，中文取 `zh`，英语取 `en`，韩语取 `ko`，德语取 `de`，西班牙语取 `es`，法语取 `fr`，自动则取 `auto`
- `w`：查询内容

url 示例：[`http://fy.iciba.com/ajax.php?a=fy&f=auto&t=auto&w=hello%20world`](http://fy.iciba.com/ajax.php?a=fy&f=auto&t=auto&w=hello%20world)

json 示例：

	{
      "status": 1,
      "content": {
        "from": "en-EU",
        "to": "zh-CN",
        "vendor": "baidu",
        "out": "你好世界<br/>",
        "err_no": 0
      }
    }

解析：

- `status`：请求成功时则取 `1`
- `content`：内容信息
	- `from`：原文内容类型
	- `to`：译文内容类型
	- `vendor`：来源平台
	- `out`：译文内容
	- `err_no`：请求成功时取 `0`