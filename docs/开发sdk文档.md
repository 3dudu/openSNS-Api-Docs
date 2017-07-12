## 华为SDK项目
[caasSDK](http://git.easier.cn/easierVideo/caasSDK)


## 客户端SDK
开发过程中 一些SDK等文档

[HUAWEI_CaaS_SDK_Android平台开发者指南.pdf](/uploads/0b5acc1486e79c591c62822e4a76d17a/HUAWEI_CaaS_SDK_Android平台开发者指南.pdf)



##  消息定义

客户端只使用 caas的文本消息，消息的内容采用下面json格式，客户端自行解析json进行界面效果展示。

图片，视频通过SNS的接口上传获取：(http://git.easier.cn/easierVideo/ui-design/wikis/home#其他)

> - 观看电影时，分享时需要传递 movieid和moviename，用于在聊天对话界面打开影片详情页。attach_ids为截屏图片，录屏视频，上传后得到的id

> - 直接分享 电影时，需要传递movieid和moviename，且需要上传一张电影的海报做为attach_ids

> - 聊天界面直接发送图片，视频时，只需要上传后得到 attach_ids，不需要moviename和moviename

> - 聊天界面目前不做发送movie

```json
{
  "messageType":"image",
  "messageData":{
    "content":"搞笑的电影",
    "attach_data": {
      "attach_ids": "9",
      "movieid": "2000034545",
      "moviename": "极品飞车"
    }
  }
}
````
|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
| messageType |是  |String |消息类型，支持：text|image|video|movie`   |

