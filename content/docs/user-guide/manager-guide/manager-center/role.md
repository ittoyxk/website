+++
title = "角色管理"
weight = 3
description = "角色是一组特定权限的集合，管理员通过给成员分配角色来赋予成员权限"
+++

# 角色管理

## 1. 概述


角色是一组特定权限的集合，管理员可通过给对应层级的成员分配角色来赋予成员权限，且一个角色仅能对应为一个层级（组织层或项目层）。Choerodon在组织层与项目层均有预置角色，能满足一般的组织与项目结构；同时，为了满足更多的使用场景，Choerodon还支持组织管理员在此为该组织或组织中的所有项目创建自定义角色。

## 2. 角色列表 

路径：管理中心->角色管理。

![组织层角色管理](/docs/user-guide/manager-guide/image/org-role-permission.png)

列表字段：

- 角色名称：角色名称是根据角色的用途与权限来定义的。
- 角色编码：角色编码具有唯一性，是角色的标识。    
- 角色层级：即角色所属的层级。
- 角色来源：分为自定义和预定义两种。预定义即系统预置的角色，不可更改；自定义角色为用户在角色管理界面所创建的角色。  
- 状态：存在`启用`与`停用`状态。

## 3. 创建角色  

![组织层角色管理](/docs/user-guide/manager-guide/image/create-org-role.png)  

- 点击“管理中心>角色管理”，进入角色管理页面。
- 点击操作栏的`创建组织角色`按钮，打开创建角色页面。
- 您可以在此创建新角色：
    
    - 角色编码：角色编码具有唯一性，是角色的标识。用户可自定义。角色创建成功后生成的角色编码为role/层级/custom/用户自定义角色编码，其中role和custom为常量，role表示角色这个大类，custom表示角色来源为用户自定义，即用户在界面创建的角色；层级和用户自定义编码为变量，层级为当前所在层级，用户自定义角色编码为用户在角色编码输入框中所填写的值。
    - 角色名称：角色的名称应该根据角色权限与功能来定义。
    - 角色权限：创建组织角色时，用户可以在此为角色分配组织层各菜单的权限以及其中各个操作按钮的权限。

- 点击创建，完成角色的创建。

 > 若想创建一个项目层角色，点击操作栏的`创建项目角色`按钮，重复上述步骤即可。



## 4. 修改角色
- 点击目标角色的角色名称，进入修改角色页面。
- 您可在此可对所选角色进行修改:

    不可修改字段：
    - 角色编码：因为角色编码具有唯一性，是角色的标识，所以角色一旦创建成功，角色编码不可更改。
    可修改字段：
    - 角色名称：应该根据角色的权限特性进行命名，这样分配角色的时候可以直观的选择角色。
    - 角色权限：可以增加或删除角色的权限。

- 点击`确定`按钮，保存对角色的修改。

<blockquote class="note">
         预定义角色不能修改。
      </blockquote>


## 6. 启停用角色

点击要停用角色所在列的![三点](/docs/user-guide/manager-guide/image/more-vert.png)按钮，点击`停用`即可停用该角色，再次点击则可启用。


* 停用角色：只能停用用户自定义角色。停用角色后，角色状态将变为`停用`；赋予该角色的权限将失效，且已被分配该角色的成员对应的权限也将失效，后续进行角色分配的操作时，不再显示该角色。

* 启用角色：自定义角色被停用后，可以再次启用。启用角色后，角色状态变为'启用'。赋予该角色的权限生效。并在角色分配中，显示该角色。

<blockquote class="note">
         预定义角色不可停用，只能启/停用自定义角色。
      </blockquote>


## 9. 阅读更多

- [如何使用Choerodon管理组织的用户](../org-user)
- [菜单管理](../../system-configuration/hzero/hzero-menu)
- [设置root用户](../../system-configuration/rootuser)