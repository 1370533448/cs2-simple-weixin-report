但是目前外网的举报插件都是走ds、tg等软件，对国人服主很不友好！

![image](https://github.com/user-attachments/assets/d9f17dc5-b639-434a-932b-8cf8de4cdd6c)
![image](https://github.com/user-attachments/assets/8e678b48-ff5a-4d8f-b03e-ba3da854397f)

如果你没有对企业微信认证貌似只能通过企业微信的APP接收，不能通过微信接收。

上传插件后，启动服务器后会自动在本目录生成一个Config.json
![image](https://github.com/user-attachments/assets/fe610933-c6ac-462d-81a3-712ba39f3e54)
详细的微信机器人配置文档：https://developer.work.weixin.qq.com/document/path/91770 

将后面的Key换成你的机器人令牌即可！

第一个版本https://bbs.csgocn.net/thread-807.htm
想要一个菜单交互所以创建这个分支

Simple Discord Report Plugin

Simply it will send message to discord web hook whatever the player types

- Example Usage
```!report something happened, send admin please```

- Example Discord Output
``` Server1 | Player1 | 7777777777(steamid) =  something happened, send admin please```


Add as many as commands as you like into ```Commands``` section of the json as given example. 



```json
{
  "Prefix": "Prefix", //prefix to player response
  "PlayerResponseNotEnoughInput": "Daha fazla bilgi vermelisiniz", //when player input is not enough like when player only types !report
  "Commands": { //add as many you like like this
    "report": "https://discord.com/api/webhooks/****************/*************************",
    "report2": "https://discord.com/api/webhooks/****************/*************************",
    "reports": "https://discord.com/api/webhooks/****************/*************************"
  },
  "PlayerResponseSuccessfull": "Report başarıyla iletildi", //This will be shown to player
  "ServerName": "Server1" //This will be shown in discord, if you dont want to see just remove it like "ServerName": "" or completly remove the property
}
```

How to get Discord Webhook

* 1 - Open the Discord channel you want to receive notifications.
* 2 - From the channel menu, select Edit channel.
* 3 - Select Integrations.
* 4 - If there are no existing webhooks, select Create Webhook. Otherwise, select View Webhooks then New Webhook.
* 5 - Enter the name of the bot to post the message.
* 6 - Optional. Edit the avatar.
* 7 - Copy the URL from the WEBHOOK URL field.
* 8 - Select Save.
