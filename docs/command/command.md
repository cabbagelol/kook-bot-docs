---
layout: default
title: 指令集
nav_order: 2
has_children: true
---

# 命令组成

**.[commend Name] (child Name) (value:any) (parameters Key:parameters Value)**

**例子:** `.checkban name call limit:6`

| 名称               | 对应例子内容    | 是否必须 | 描述                                       |    类型    |    版本    |
|:-----------------|-----------|---|:-----------------------------------------|:--------:|:--------:|
| commend Name     | .checkban | 是 | 命令名称                                     |  string  |    -     |
| child Name       | name      | 否 | 孩子命令，在某些独立功能中可能只有它自己                     |  string  |    -     |
| value            | call      | 否 | 在一些指令中，它必须提供一个值，且有严格类型限制                 |   any    |    -     |
| parameters Key   | limit     | 否 | 额外参数名                                    |  string  |    -     |
| parameters Value | 6         | 否 | 额外参数值                                    |   any    |    -     |

ps: ()表示可选，[]表示必选

---

## 通用字段

它们都在`parameters`中添加

- `v`表示版本，指令存在版本迭代, 例子(.help v:1)
- `debug`是否中测试，返回测试用例, 例子(.help debug:true)
