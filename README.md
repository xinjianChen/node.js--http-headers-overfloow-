# node.js--http-headers-overfloow-
解决由于http/https请求头太大而导致headers overflow 问题
# 哭了 被这个问题卡了十来天，主要还是因为我是个半路出家的node程序员
# 起初以为是我的头部写错了，后面才发觉是请求token时，包含token的头部太大导致的头部溢出错误，当时处理接收头部的时Node低层，我没法设置
# 最后经过千辛万苦，终于在node 手册中发现可以通过启动时在命令行设置http的头部大小
```
node --max-http-header-size=81000 app.js
```
