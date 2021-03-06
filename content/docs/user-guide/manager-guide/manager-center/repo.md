+++
title = "仓库"
description = "支持用户在组织下配置使用自定义的Helm仓库"
weight = 8
+++

# 仓库

## 1. 概述

仓库设置支持用户在组织下配置使用自定义的Helm仓库，配置成功后，该组织下使用默认Helm仓库的项目，之后生成的charts包将存放在新的Helm仓库之中。

## 2. 修改仓库

点击`管理中心-仓库`进入详情页，便可在主页修改组织层仓库的相关配置。

![image](/docs/user-guide/manager-guide/image/repo.jpg)

- 修改默认Helm仓库为自定义Helm仓库。
    * 将默认Helm仓库切换为自定义Helm仓库。
    * 输入仓库地址。    
    * 输入用户名和密码；非必填，若
    * 点击测试连接，若连接成功，则代表自定义仓库有效；若连接失败，则无法使用。   

    <blockquote class="note">
    
    组织层配置使用自定义的Helm仓库后，该组织下使用“默认Helm仓库”的项目，之后生成的Charts包会被存放在组织层配置的自定义仓库之中；而使用“项目层-自定义Helm仓库”的项目，生成的Charts会被存放于项目层配置的自定义仓库之中。</blockquote>