# KillGTA (一个用来打GTAOL犯罪之神挑战的小工具)
GTAOL, 犯罪之神挑战

抢劫首脑: 玩家所在的队伍成员依次完成五个难度为困难的抢劫, 顺序为: `全福` -> `越狱` -> `人道` -> `首轮` -> `太平洋`, 即可达成条件

末日首脑: 末日首脑分2个人的(犯罪之神2), 3个人的(犯罪之神3), 4个人的(犯罪之神4), 同一小队按顺序依次完成前置任务(可死亡),  准备任务(不可死亡)以及分红任务(不可死亡), 难度全为困难, 即可达成条件.

### 目的
由于硬性的条件是**不可死亡**, 但GTAOL当在出现死亡的一瞬间, 结束掉游戏进程, 不让它上传死亡数据, 即可重新上线继续从当前进度开始打, 不过要队伍里面的人都结束掉进程, 如果有人没结束掉, 那么他的进度将会重置(一个人重置之后所有人都要重新打), 为了防止这种尴尬的情况, 就有了此软件.

### 功能
`Server.go`
```
服务端, 用于分发任意一个客户端提交上来的kill请求, 并且支持心跳检测, 以及客户端数量检测.
```

`Client.go`

```
客户端, 使用TCP连接至服务端, 并每隔30秒都进行心跳检测, 当按下F4键, 向服务端发送一个kill请求, 服务器收到kill请求, 就会分发至各个客户端, 保证每个人都可以结束掉GTA.exe
```

### 特别感谢
[JetBrains](http://jetbrains.com/)提供IDE, 以用来编写此软件代码.

