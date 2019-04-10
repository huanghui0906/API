# 「一个」 API 接口 #
## 截止到 v3.5.0 ##
## 图片 ##
// 此 url 获取所有近期图片列表，返回 json 中的的数字作为参数传入后面的 url 中

**图片列表** url:``http://v3.wufazhuce.com:8000/api/hp/idlist/0?version=3.5.0&platform=android``

// 将下面的 ``id`` 兑换成上面获取到的值

**图片详情** url:``http://v3.wufazhuce.com:8000/api/hp/detail/ + id + ?version=3.5.0&platform=android``

例：``http://v3.wufazhuce.com:8000/api/hp/detail/1557?version=3.5.0&platform=android``

## 阅读 ##
// 此 url 获取当日所有阅读文章的列表，返回 json 中的 ``content_id`` 作为后面两个 url 的传入值

**阅读列表** url:``http://v3.wufazhuce.com:8000/api/reading/index/?version=3.5.0&platform=android``

// 将下面的 ``content_id`` 兑换成上面获取到的值

**阅读详情** url:``http://v3.wufazhuce.com:8000/api/essay/ + content_id + ?version=3.5.0&platform=android``

例：``http://v3.wufazhuce.com:8000/api/essay/1634?version=3.5.0&platform=android``

// 将下面的 ``content_id`` 兑换成上面获取到的值

**阅读评论** url:``http://v3.wufazhuce.com:8000/api/comment/praiseandtime/essay/ + content_id + /0?version=3.5.0&platform=android``

例：``http://v3.wufazhuce.com:8000/api/comment/praiseandtime/essay/1634/0?version=3.5.0&platform=android``

## 音乐 ##
// 此 url 获取所有的歌曲 ``id``，返回 json 中的 ``id`` 作为后面两个 url 的传入值

**音乐列表** id url:``http://v3.wufazhuce.com:8000/api/music/idlist/0?version=3.5.0&platform=android``

// 将下面的 ``id`` 兑换成上面获取到的值

**歌曲详情** url:``http://v3.wufazhuce.com:8000/api/music/detail/ + id + ?version=3.5.0&platform=android``

例：``http://v3.wufazhuce.com:8000/api/music/detail/1147?version=3.5.0&platform=android``

## 电影 ##
// 此 url 获取当日近期电影的列表，返回 json 中的数字作为后面两个 url 的传入值

**电影列表** url:``http://v3.wufazhuce.com:8000/api/movie/list/0?version=3.5.0&platform=android``

// 将下面的 ``id`` 兑换成上面获取到的值

**电影详情** url:``http://v3.wufazhuce.com:8000/api/movie/183/story/1/0?version=3.5.0&platform=android``

// 将下面的 ``id`` 兑换成上面获取到的值

**配合电影详情所使用图片和其他信息** url:``http://v3.wufazhuce.com:8000/api/movie/detail/183?version=3.5.0&platform=android``

