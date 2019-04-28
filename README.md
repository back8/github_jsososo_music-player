# Vue 音乐播放器

## 介绍

项目用 vue-cli 3.0 搭建，功能有根据qq号获取歌单、qq音乐的搜索功能、歌词显示、下载等。所有的设置信息均存在 localStorage。

同时支持获取网易云音乐歌单中对应的qq音乐歌曲


## 问题

腾讯在 19.3.29 对原有的获取歌单接口增加了一步登陆校验，需要用户现在 y.qq.com 进行登陆

## 接口

接口都是自己从 企鹅音乐网站上拔的，自己整理了一下可以参考 http://jsososo.com/#/article?id=5a6254c0c4  
部分接口通过php转发伪造refer，下载接口通过php将音乐转成流文件接收，方便前端下载。

目前已经添加喜欢和取消喜欢的功能，但是由于接口限制，目前的措施比较low，需要先用户现在qq音乐web端登陆，然后将cookie信息复制粘贴到站内的一个输入弹窗内，之后通过iframe的形式来请求。但是因为无法获取iframe内容，通过简单粗暴的直接拉取歌单全部歌曲并通过判断有无歌曲的方式来确定是否增删成功。


## 开发计划

+ ~~接入歌词~~
+ ~~接入加入歌单等功能 （因为需要获取qq音乐页面的部分cookie，暂缓）~~
+ ~~接入推荐音乐~~
+ ~~背景给美化一下~~
+ ~~无损音质~~
+ 移动端兼容
+ ~~下载管理~~
+ ~~歌单列表批量操作~~

## 更新记录

+ 19-04-28: 评论
+ 19-04-26: 电台
+ 19-04-22: 下载中出错捕获
+ 19-04-12: 二维码手机下载
+ 19-04-08: 歌词翻译
+ 19-03-19: 下载中心 & fix 歌词第一次点击滚动后会卡住的问题
+ 19-02-13: 批量添加、删除到歌单
+ 19-02-12: 歌词拖动 & 列表页批量下载
+ 19-01-26: 网易云歌单转qq音乐
+ 19-01-11: 播放器增加喜欢按钮 & 列表增加下载按钮
+ 19-01-10: 新增添加、取消喜欢的歌曲 & fix 某些情况下非128k的音乐403
+ 18-12-13: bug fix: 切歌单下一首报错 && 下架歌曲播放
+ 18-12-12: 无损音质 & 下载
+ 18-12-10: 各种细节优化
+ 18-12-06: 背景图片用专辑图片
+ 18-12-04: 接入企鹅音乐歌词
+ 18-11-06: 接口更换为企鹅音乐
