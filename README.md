<h1 align="center">
  <br>Telegram 关键词自动回复机器人<br>
</h1>

### 基本命令

- 添加关键词回复规则 `/add 关键词===回复内容` 或者 `/add 关键词1||关键词2===回复内容` 
- 关键词可以使用正则表达式,例如`/add re:p([a-z]+)ch===测试正则`,就会匹配规则`p([a-z]+)ch`  
- 删除关键词规则 `/del 关键词` 暂不支持一次性删除多个关键词
- 自动删除含有关键词的文字消息, 只需要将回复内容设置成 `delete`, 并给机器人添加删除消息权限
- 使用`/list`命令可以查看本群内所有自动回复规则
- 给机器人添加删除消息和踢人的管理权限,可以自动防清真(阿拉伯语)

### 回复特殊内容

- 回复内容支持文字\图片\GIF\视频,默认文字
- 如需图片,回复内容设置成`photo:https://t.me/c/1472018167/53095`,`https://t.me/c/1472018167/53095`是已经发送过的图片获取到的链接
- 同理,gif将`photo`替换成`gif`,视频替换成`video`,文件替换成`file`
- 注意: 这里的链接必须是公开群组的,否则无法发出来

### 如何搭建
自己编译
clone本仓库并按照需求进行修改
使用 go build -ldflags "-w -s" -trimpath -o tgbot . 进行编译
使用 ./tgbot -t TOKEN 运行机器人
使用Github Action编译的版本
访问 https://github.com/zu1k/tg-keyword-reply-bot/actions
下载Github Action编译的可执行文件，解压bin.zip
使用 ./tg-keyword-reply-bot -t TOKEN 运行机器人
## License

MIT zu1k i@zu1k.com

不提供任何机器人相关的咨询或其他服务，不要私聊我
