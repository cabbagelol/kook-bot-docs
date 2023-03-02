---
title: 指令
layout: home
nav_order: 2
---

()表示可选，[]表示必选

---

### 通用字段

- `v`表示版本，指令存在版本迭代
- `debug`是否中测试，返回测试用例

## 帮助

Stable
{: .label .label-green }

| 状态  | 指令    | 描述   | 例子          | 版本  |
|-----|-------|------|-------------|-----|
| [x] | .help | 寻求帮助 | .help | 1   |

- 此命令会展示所有已注入命令集描述

## 邀请机器人

Stable
{: .label .label-green }

| 状态  | 指令    | 描述    | 例子          | 版本  |
|-----|-------|-------|-------------|-----|
| [x] | .invitation | 邀请机器人 | .invitation | 1   |


## 查询玩家

| 状态  | 指令                                                                         | 描述           | 例子                           | 版本  |
|-----|----------------------------------------------------------------------------|--------------|------------------------------|-----|
| []  | .checkban                                                                  | -            | -                            | 1   |
| [x] | .checkban id [id:number] (v:number)                                        | 使用EAid查询玩家状态 | .checkban id 2000000         | 1   |
|   [x]  | .checkban name [name:string] (v:number) (limit:5) (sort:default) (limit:5) | 使用名字查询玩家状态   | .checkban name cabb limit:10 | 1   |

## widget

|     | 指令                                 | 描述                                                                                 | 例子                       |
|-----|------------------------------------|------------------------------------------------------------------------------------|--------------------------|
| []  | .widget                            | -                                                                                  | -                        |
| []  | .widget img [id:number] (v:number) | 生成图片小组件，参考网站生成分享图片[链接](https://bfban.gametools.network/player/1005868194472/share) | .widget img 1000000 |

## 网站统计

|     | 指令                                   | 描述                  | 例子                    | 版本  |
|-----|--------------------------------------|---------------------|-----------------------|-----|
| [x] | .sitestats                           | -                   | -                     | 1   |
| [x] | .sitestats site (v:number)           | 网站统计，返回统计信息         | .sitestats site  | 1   |
| [x] | .sitestats admin (v:number)          | 网站统计，返回站点管理员统计      | .sitestats admin | 1   |
| [x] | .sitestats hot (v:number) (time:string) | 网站统计，热点案件,time不选择一周 | .sitestats hot   | 1   |

time: daily/week/monthly/yearly
