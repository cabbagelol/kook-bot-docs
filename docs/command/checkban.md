---
layout: default
title: 检查案件
parent: 指令集
nav_order: 3
---

# 查询玩家

|     | 指令                                                                         | 描述           | 例子                           | 版本  |
|-----|----------------------------------------------------------------------------|--------------|------------------------------|-----|
| [x] | .checkban                                                                  | -            | -                            | 1   |
| [x] | .checkban id [id:number] (v:number)                                        | 使用EAid查询玩家状态 | .checkban id 2000000         | 1   |
| [x] | .checkban name [name:string] (v:number) (limit:5) (sort:default) (limit:5) | 使用名字查询玩家状态   | .checkban name cabb limit:10 | 1   |
