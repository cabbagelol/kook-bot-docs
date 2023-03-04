---
title: 开发
layout: home
nav_order: 3
---

# 参与机器人开发

此文档专门为开发者设立，在开始前你需要申请新Kook机器人key，作为本地测试机器人，申请方式请参考[kook机器人]。

## 开发

在目录下创建`config.ts`, 并将字段`__DEBUG__`设置为`true`, 同时配置机器人key

前往目录执行
```
npm i

npm start
```

此时机器人运行！，创建一个自己的频道，给测试机器人发言权，通过该频道测试。 试试发送`.help`查询机器人是否活动

## 新增命令

依照/src/commends/下例子来实现

---

## 部署

执行前你需要配置生产环境`config.ts`, 不要在任何网络中公开机器人目录，检查它。

请将`__DEBUG__`设置为`false`, 在运行后会执行生产环境功能，如日志、心跳
```json
"__DEBUG__": false
```

使用正式环境机器人key

```json
"kookAuth": {
    "khlkey": "",
    "khltoken": "",
    "khlverify": ""
}
```

整个项目基于ts和sdk写的，因此它需要运行在node.js环境下。 在生成环境中，为防止机器人掉线或是奔溃、线程溢出等原因终止任务，使用pm2来管理脚本，遇到上诉问题后自动重启。



[kook机器人]:https://developer.kookapp.cn/doc/intro