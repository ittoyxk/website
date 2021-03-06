+++
title = "证书管理"
description = ""
weight = 2
+++

# 证书管理

## 1. 概述

证书是遵守某种网络安全协议，具有服务器身份验证和数据传输加密功能的数字证书。此处的证书可共享至该组织下任意的项目。

<blockquote class="note"> 
    只有项目所有者才能对集群中的证书进行查看、创建和编辑的操作。
    </blockquote>

通过该页面，您将了解到如何上传、修改以及删除证书。

## 2. 上传证书

1. 点击菜单栏`上传证书`，按钮，右侧会弹出创建页面。

    ![image](/docs/user-guide/deploy/cluster/image/cert-management-01.png)

2. 填写证书名称，为该证书填写一个名称。
    - 证书名称：由小写字母、数字或‘-’组成，并且必须以字母或数字开始和结束！环境下唯一。

3. 点击上传证书，包括一个key文件和一个cert文件，可以点击 `切换文件上传模式`进行切换。
4. 点击`上传`完成证书的上传。

## 3. 查看证书详情

在证书界面，通过列表，可以查看到证书名称和域名地址。

![image](/docs/user-guide/deploy/cluster/image/cert-management-02.png)

## 4. 证书权限分配

点击证书列表的![image](https://minio.choerodon.com.cn/knowledgebase-service/file_b53c0c1755864d7f9e3f7bb1f88b37fc_blob.png)标识，选择 ` 权限管理`，此时会弹出证书权限分配的界面，便可在此设置证书的公开范围，其中包括组织下所有项目与组织下特定项目。

- 若选择 `组织下所有项目`，那么表示在该组织所有项目中的环境下创建证书时都能选择此证书；
- 若选择 `项目下特定项目`，就表示只有在已被分配权限的项目下的环境中创建证书时才能选择此证书。

## 5. 修改证书

在证书列表中，点击对应证书的名称，右侧会弹出证书的修改界面，支持修改证书的名称、域名地址以及证书文件。

![image](/docs/user-guide/deploy/cluster/image/cert-management-03.png)

## 6. 删除证书

点击证书列表的![image](https://minio.choerodon.com.cn/knowledgebase-service/file_b53c0c1755864d7f9e3f7bb1f88b37fc_blob.png)标识，可以选择删除该证书。

 <blockquote class="note"> 
    在项目下存在关联证书时，集群下的证书便不能删除！
    </blockquote>
 
## 7. 阅读更多
 
- [资源管理](../../app-deploy/resource)
- [环境配置](../../env-config)