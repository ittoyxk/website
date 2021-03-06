+++
title = "测试计划"
description = ""
weight = 2
+++

# 测试计划

## 1. 概述

了解如何在Choerodon中如何创建计划，并且分类测试用例，添加执行，记录测试步骤结果，查看测试进度。

## 2. 创建计划

单击操作栏的`创建计划`按钮，填写计划名称、描述、负责人、持续时间、选择导入的用例范围、是否自动同步等信息创建对应计划。

- 名称：测试计划的名称。
- 描述：对测试计划的作用、测试范围、涉及功能等的补充说明。
- 负责人：测试计划的负责人。
- 持续时间：测试计划的起止时间。
- 选择导入范围：你可以选择导入全部用例，或者自选部分用例导入到测试计划中。
- 自动同步：选择源用例更改后是否自动同步到测试计划的相关用例；

![image](/docs/user-guide/test/image/TestPlan/TestPlan-02.png)

## 3.编辑测试计划

## 3.1 修改计划

- 点击操作栏上的修改计划按钮，打开修改计划页面。

- 您可以修改计划的名称、描述、负责人、持续时间、是否自动同步。

- 点击保存，即可保存修改。

## 3.2 创建文件夹

点击文件夹上添加文件夹按钮，填写文件夹名称，点击空白处或者回车即可向该文件夹添加子文件夹；


### 3.3 编辑文件夹

点击文件夹右侧![三点](/docs/user-guide/manager-guide/image/more-vert.png)按钮标识，选择重命名或者删除，可对该文件夹进行重命名或者删除操作。

<blockquote class="note">
    删除文件夹后，文件夹下的测试执行将一并被删除。
</blockquote>

## 3.4 导入用例

- 点击文件夹右侧![三点](/docs/user-guide/manager-guide/image/more-vert.png)按钮标识，选择导入用例，即可打开导入用例侧开页。

- 勾选您要添加到此文件夹的测试用例。（已添加的测试用例不能再次添加）

- 点击确定按钮，即可导入用例到该计划下的此文件夹。

## 3.5 更新用例

源用例更新后，会提醒未选择自动同步的计划中相应的测试用例进行更新。您可以选择更新，也可以选择忽略当次更新。

![image](/content/docs/user-guide/test/image/TestPlan/TestPlan-03.png)

## 3.6. 查看执行测试详情

点击某个测试用例，会进入到执行详情页面，您从执行详情中能够看到执行详情、测试步骤详情、执行历史变更。

![image](https://minio.choerodon.com.cn/knowledgebase-service/file_37e5a530cbcf4da5832565edc71724d9_blob.png)

- 测试详细信息： 包含测试步骤的名称、期待数据、预期结果、状态等信息。
- 执行历史记录： 主要记录用户对执行信息的修改，如执行状态、指定人、描述等信息的修改。

点击左上角的`查看详情`，会跳出测试执行详细信息页面。


- 测试执行： 包含执行的状态、执行人、执行时间、描述、附件、关联缺陷等详细信息。

## 3.7 修改测试执行

1. 点击某个测试用例，会进入到执行详情页面。
2. 点击修改测试用例，进入测试执行修改页面。
    - 您可以选择修改测试执行的概要、描述、附件信息、测试步骤。
3. 您可以选择直接保存，将当次修改仅保存到当前执行中。
4. 您也可以选择保存并同步到用例库。

## 4. 开始手工测试

点击操作栏的开始手工测试按钮，测试计划将进入进行中状态，测试人员可以执行测试计划。

## 5. 测试计划的3种状态

测试计划有三种测试状态：未开始、进行中、已完成。

- 未开始：测试计划尚在规划中，测试人员可以在规划测试的内容，但是不能执行测试。您可以点击开始手工测试，将计划转换为进行中状态。
- 进行中：测试计划正在执行中，测试人员可以进行测试执行。您可以点击完成计划按钮，将计划转换为已完成状态。
- 已完成：测试计划已完成，不能修改测试计划的任何内容。

<blockquote class="note">
    测试计划的状态转换不可逆。
</blockquote>

## 6. 执行测试计划

仅可以执行状态为进行中的测试计划。

- 您可以点击测试计划中测试用例列表的快速通过或者失败按钮，快速修改测试用例的状态；
- 您可以点击测试用例的名称，进入执行详情，点击快速变更测试用例的状态，点击修改测试步骤列表中步骤的状态，在步骤列表上添加关联的缺陷，或者添加备注信息。



## 6. 复制计划

项目成员可以对本页中的测试计划进行复制，减少不同迭代中的重复测试再次创建。

- 点击计划右侧![三点](/docs/user-guide/manager-guide/image/more-vert.png)按钮标识，选择复制，即可复制此计划。

- 新复制的计划默认名称为“源计划的名称-副本”，且新计划的状态为未开始。

- 新复制的计划的用例及用例步骤的状态全部重置为未执行。

## 7. 删除计划

点击计划右侧![三点](/docs/user-guide/manager-guide/image/more-vert.png)按钮标识，选择删除，即可删除此计划。

<blockquote class="warning">
删除计划后，计划下的测试用例及测试状态也将被删除。
</blockquote>


## 7. 阅读更多

- [测试用例](../../store/whatisstore)
- [自动化测试](../../automation)