+++
title = "统计图"
description = "根据指定字段以统计图呈现项目或筛选器下的问题，这可以使您一目了然地了解问题详情。"
weight = 7
+++

# 统计图

根据指定字段以统计图呈现项目或筛选器下的问题，这可以使您一目了然地了解问题详情。  


## 操作步骤

* 选择报告
    1. 选择`报告`
    2. 选择`统计图`
* 切换报告
    1. 点击`切换报表`按钮
    2. 选择`统计图`或其他报表

## 报告说明
* `统计类型`：包括`经办人`、`模块`、`问题类型`、`修复版本`、`优先级`、`状态`、`冲刺`、`史诗`、`解决结果`

{{< note >}}这里的统计包括当前项目中的所有问题：包括`史诗`、`任务`、`子任务`、`故事`、`故障`{{< /note >}}

### 图表  
![image](/docs/user-guide/agile/report/img/statistical.png)

### 报告详情

- **数据统计**
    - `指定字段`:当前项目中所有问题的统计类型
    - `图例`:不同的颜色代表不同的维度的筛选出的具体名称，随机生成不同的颜色，分别和指定字段筛选出的子项相匹配
    - `问题数量`:按照指定字段筛选出的问题数量
    - `百分比`:按照指定字段筛选出的问题数量/当前项目中所有问题数量

- **图表过程**
    - 选择统计类型的字段，下拉框中存在当前所有的统计类型字段，选择其中一种类型，按饼图的形式显示各子项的名称，包含问题数、所占百分比
    - 按图表的图例来区别筛选出的各类问题数量占所有问题数量的百分比
    - 停放在不同的区域时，显示其具体名称、包含的问题数、所占百分比
    
 {{< note >}}
若存在没有归类的问题或者当前系统尚未创建指定字段时，则默认为一类：未分配
 {{< /note >}}


## 其他报表

- [累积流量图](../cumulative-flow)
- [冲刺报告](../sprint)
- [燃尽图](../burn-down)
- [版本报告](../version-report)
- [迭代速度图](../iterative-chart)
- [史诗报告](../epic-report)