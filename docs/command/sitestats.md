---
layout: default
title: 统计
parent: 指令集
nav_order: 5
---

# 网站统计

查询网站信息，它们都在[bfban.gametools.network/sitestats](https://bfban.gametools.network/sitestats)能看见

| 指令                                   | 描述                    | 例子                    | 版本  |
|--------------------------------------|-----------------------|-----------------------|-----|
| .sitestats                           | -                     | -                     | 1   |
| .sitestats site        | 返回统计信息                | .sitestats site  | 1   |
| .sitestats admin          | 返回站点管理员统计             | .sitestats admin | 1   |
| .sitestats hot (time:string) | 热点案件,可以按照`time`[^1]查询范围 | .sitestats hot   | 1   |

[^1]: 可用参: daily/week/monthly/yearly，它默认week
