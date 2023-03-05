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

依照`/src/commends/`下例子来实现

---

## 部署
整个项目基于ts和sdk写的，因此它需要运行在node.js环境下。 在生成环境中，为防止机器人掉线或是奔溃、线程溢出等原因终止任务，使用pm2来管理脚本，遇到上诉问题后自动重启。

### 基本配置

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

立即在服务器上运行查看效果(正式跳过看下方pm2的配置):
```
npm i
npm start
```

- 如果你是在liunx下，请依照[Install Google Chrome for Linux]获取内核，其他系统请看[chrome-headless-disables-gpu-compositing]
- 当出现.os异常，可能是因为`puppeteer`引起，具体查看[troubleshooting]故障排查
- 意外终止，请先前往logs查看error日志检查问题，无法解决可以在社区@cabbagelol

### pm2配置

这里例子创建一个pm2线程

```
npm i -g pm2
pm2 install typescript ts-node@latest
pm2 init simple
```

ecosystem.config.js
```ts
module.exports = {
  apps : [{
    name   : "you name",
    script : "./index.ts",
    kill_timeout: 10000,
    wait_ready: true,
    watch: false,
    ignore_watch: ['node_modules'],
  }]
}
```

```
pm2 start ecosystem.config.js --only server
```

[kook机器人]:https://developer.kookapp.cn/doc/intro
[Install Google Chrome for Linux]:https://learn.microsoft.com/en-us/windows/wsl/tutorials/gui-apps#install-google-chrome-for-linux
[troubleshooting]:https://github.com/puppeteer/puppeteer/blob/main/docs/troubleshooting.md
[chrome-headless-disables-gpu-compositing]:https://pptr.dev/troubleshooting#chrome-headless-disables-gpu-compositing
