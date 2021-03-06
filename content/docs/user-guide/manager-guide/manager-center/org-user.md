+++
title = "用户管理"
description = "是对组织下用户进行系统的管理"
weight = 3
+++


# 用户管理

## 1. 概述

用户管理页面包含用户的个人信息和角色分配信息。您可以看到用户名、登录名、状态、角色和安全状态。
通过本文档您可以了解在用户管理如何查询全局用户、添加或导入平台用户、启停用户，以及修改用户信息、重置密码。

<div id="createuser"></div>

## 2. 创建用户

您可以在此创建新用户，点击操作栏的`创建用户`，会跳转出创建页面，创建一个新用户。

输入用户名、邮箱和密码，选择分配的角色。

必填字段：

* 用户名：用户的昵称。
* 邮箱：一个邮箱只能被一个用户使用。用户需填写真实有效的邮箱。邮箱可用于登录平台、找回密码。
* 密码：系统默认密码为abcd1234。
* 角色：至少向新建用户分配一个角色。

点击创建，完成一个用户的创建。

![image](/docs/user-guide/manager-guide/image/org-user-01.png)

## 3. 导入用户

您也可以选择从外部文件中批量导入用户。

点击工具栏`导入用户`，会跳出导入用户页面。

1. 先下载模板文件，在下载的Excel模板中填入下图所示的用户信息：

    用户的用户名、邮箱、角色为必填项；

    密码、手机号为选填项；
    
    当密码为空时，该用户的密码为系统默认密码abcd1234。

2. 点击上传和保存即可。

![image](https://minio.choerodon.com.cn/knowledgebase-service/file_f6066a508e994af8877c9fe20a88b110_blob.png)

## 4. 添加组织用户

添加组织用户即给用户分配组织层角色。角色分配时，可以给一到多个成员分配一到多个角色。角色是权限的集合，给成员分配角色即给成员赋予权限。权限与角色都具有层级性，且角色权限的层级必须与角色层级相同。角色分配具有层级性，角色分配中被分配的角色层级必须与角色分配的层级相同。即，在某一层级的角色分配中，只能给用户分配对应的层级的角色，只能给角色分配对应层级的权限。

添加用户为组织用户，步骤如下：

1. 进入管理中心，点击菜单“管理>用户管理”，进入用户管理页面。
2. 点击操作栏的`添加组织用户`→![添加组织用户](/docs/user-guide/manager-guide/image/add-org-user.png)，打开添加组织用户侧开页。
3. 在用户选择框中选中用户，您可以通过搜索用户的登录名或用户名选择要添加角色的用户。
4. 在角色选择框中选择角色。点击保存即可。
5. （可选）点击添加其他用户按钮，添加更多平台用户，即为更多用户分配组织层角色。

<blockquote class="note">
         添加新的成员角色之间的关联：如果成员已经被分配过角色，则将本次操作新增的与该成员有关的成员角色关联合并到已有关联列表，即已有的不变，新增的增加。
      </blockquote>


## 5. 导入组织用户

> 您也可以通过Excel表格批量导入组织用户。

1. 进入管理中心的用户管理页面，点击`导入组织用户`→![导入组织用户](/docs/user-guide/manager-guide/image/import-site-user.png)，进入导入组织用户界面。
2. 首先您需要点击下载模板按钮下载Excel模板。你所上传的角色分配Excel表必须完全按照模板样式。您填写的内容必须按照模板说明：
    - 填写导入成员的用户名和对应角色编码。
    - 点击此处查看[预定义角色的角色编码](../../role-permission)
3. 点击`上传文件`按钮，选择您要上传的角色分配Excel表。
4. 接着，您可以在此查看导入结果。


## 6. LDAP同步设置

LDAP是轻量目录访问协议。LDAP管理是对组织应用的LDAP信息设置的管理。LDAP只针对LDAP用户，LDAP用户的登录名和密码取自LDAP指向的外部系统中的数据。

组织下的LDAP属于该组织。LDAP设置包括服务器设置和用户属性设置两种LDAP信息设置，且有LDAP连接测试和LDAP用户同步这两种功能。用户可以使用测试连接功能来检测LDAP服务器是否可以连通以及是否可以正常获取用户属性值。用户可以使用同步用户功能来将LDAP服务器中的用户信息同步到平台中。  

LDAP同步设置中包含了自动同步、手动同步以及同步记录三个模块，支持在此直接对LDAP用户进行同步操作。

### 6.1 手动同步

点击`用户管理`界面上方的`LDAP同步设置`按钮，会从右侧弹出LDAP同步界面。选择`手动同步`页签，点击`手动同步`按钮，即可执行对LDAP用户的同步操作。  

![image](/docs/user-guide/manager-guide/image/manual-ldap.jpg)

<blockquote class="note">

注意：在同步之前，请确保您已在“通用-LDAP设置”中配置好相关的参数。若未配置，可在该页面点击“跳转至LDAP设置”前往设置。
</blockquote>


### 6.2 自动同步

在LDAP同步设置页面，选择`自动同步`页签，即可看到自动同步相关的设置。 

![image](/docs/user-guide/manager-guide/image/auto-ldap.jpg)  

- 是否自动同步：若想启用LDAP用户自动同步的功能，需在此处选择 `是`。  
- 同步频率：目前支持选择一天一次、一周一次、一月一次。  
- 开始同步时间：即同步的起始时间，从这之后，就按照所选的同步频率在此时间开始自动同步。  

<blockquote class="note">

注意：在同步之前，请确保您已在“通用-LDAP设置”中配置好相关的参数。若未配置，可在该页面点击“跳转至LDAP设置”前往设置。
</blockquote>


### 6.3 同步记录

在LDAP同步设置页面，选择`同步记录`页签，您可以查看此组织下的同步ldap用户的历史记录。  

#### 6.3.1 同步记录列表

列表字段：

- 同步时间：同步开始的时间。  
- 同步类型：分为手动同步与自动同步。
- 成功人数：此次同步成功的人数与同步总人数之比。
- 失败人数：此次同步失败的人数。
- 耗时：此次同步花费的时间。

#### 3.4.2 ldap同步失败详情

点击同步记录列表的第一列（即时间列），即可查看同步用户失败的原因。

## 7. 修改用户信息

你可以在用户管理修改用户的基本信息和角色信息。操作步骤如下：

1. 进入管理中心，点击菜单“管理>用户管理”，进入用户管理页面。
2. 点击组织用户的用户名，进入修改组织用户界面。
3. 您可以在此查看组织用户的详细个人信息，包括用户名、邮箱、手机号码、语言、时区、在组织层分配角色信息。
4. 您可以在此修改用户的详细信息和分配的角色，也可以继续为平台用户分配角色，或者移除角色。
    - 可修改字段：
    - 用户名：用户的昵称。
    - 邮箱：一个邮箱只能被一个用户使用。用户需填写真实有效的邮箱。邮箱可用于登录平台、找回密码。
    - 手机号：用户的手机号码，一个手机号码只能被一个启用用户使用。
    - 语言：默认为简体中文。
    - 时区：默认为北京时间。
    - 角色：用户在组织层分配的角色，您可以继续添加角色，也可以移除角色。

5. 点击保存按钮，保存您对组织用户的修改。

## 8. 启停用用户

在用户管理列表中，点击你要停用用户所在列的![三点](/docs/user-guide/manager-guide/image/more-vert.png)按钮，点击`停用`，可停用该用户。再次单击可恢复启用。

<blockquote class="warning">
         用户被停用之后，无法登录系统。
      </blockquote>


## 9. 重置密码

在用户列表中，点击您要重置密码用户所在列的![三点](/docs/user-guide/manager-guide/image/more-vert.png)按钮，单击`重置密码`，可重置该用户密码。

> 选择重置密码后，用户的当前密码将失效。如果您启用组织密码策略，将重置为组织默认密码，否则将重置为平台密码。

## 10. 解锁用户

当密码策略中的登录安全策略被启用时，如果用户输错密码的次数大于登录安全策略中设置的最大密码输错次数，则用户被锁住，在一定时间内无法登录平台。

在用户管理列表中，点击你要解锁用户所在列的![三点](/docs/user-guide/manager-guide/image/more-vert.png)按钮，单击`解锁`，可解锁该用户。


<blockquote class="note">
         当用户的安全状态为锁住时，可以解锁该用户。解锁成功后，用户的安全状态变为正常，可以正常登录系统。
      </blockquote>

## 11. 阅读更多

- [如何在Choerodon进行角色管理](../role)
- [快速添加组织管理员](../org_admin)
- [LDAP设置](../setting)

