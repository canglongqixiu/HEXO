---
title: Windows操作系统安全配置
date: 2021-09-10 14:54:38
categories: 网络安全
tags:
      - 中科磐云	
      - P100
---

### Windows操作系统安全配置

#### 设置密码策略必须同时满足大小写字母、数字、特殊字符，最小密码长度不少于8个字符，密码最长使用期限为15天。将服务器上密码策略配置信息截图;

> 本地安全策略-账户策略-密码策略

{% asset_img 1.png %}

#### 在用户登录系统时，应该有“For authorized users only”提示信息，将登录系统时系统弹出警告信息窗口截图;

> 本地安全策略-本地策略-安全选项-交互式登录：试图登录的用户消息标题和文本

{% asset_img 2.png %}

#### 一分钟内仅允许5次登录失败的尝试，超过5次，登录帐号锁定1分钟,将账号锁定策略配置信息截图；

> 本地安全策略-账户策略-账户锁定策略
>
> 注意，超过五次锁定，所以这里锁定阈值应为6次，截图中若为5次则不计分。

{% asset_img 3.png %}

#### 设置远程桌面用户非活动会话连接超时应小于等于5分钟，将RDP-Tcp属性对应的配置界面截图；

> 远程桌面服务-远程桌面会话主机配置-RDP-Tcp属性-会话
>
> 注意，设置非活动会话，除活动会话都勾选

{% asset_img 4.png %}

#### 通过SSL（TLS 1.0）加密服务器的远程桌面服务，将RDP-Tcp属性对应的配置界面截图；

> 远程桌面服务-远程桌面会话主机配置-RDP-Tcp属性-常规

{% asset_img 5.png %}

#### 仅允许超级管理员账号关闭系统，将关闭系统属性的配置界面截图；

> 本地安全策略-本地策略-用户权限分配-关闭系统

{% asset_img 6.png %}

#### 开启IIS的日志审计记录，日志文件保存格式为W3C,只记录日期、时间、客户端IP地址、用户名、服务器端口、方法，将W3C日志记录字段的配置界面截图；

> Internet信息服务(IIS)管理器-主机-Default Web Site主页-日志-选择字段

{% asset_img 7.png %}

#### 设置网站的最大并发连接数为1000，网站连接超时为60s，将编辑网站限制的配置界面截图；

> Internet信息服务(IIS)管理器-主机-Default Web Site主页-右列表操作-限制

{% asset_img 8.png %}

#### 禁用IIS内核缓存，避免对方利用ms15_034漏洞进行DOS攻击，出现蓝屏的现象，将编辑输出缓存设置的配置界面截图；

> Internet信息服务(IIS)管理器-主机-Default Web Site主页-输出缓存-编辑功能设置

{% asset_img 9.png %}

#### 设置user1用户只能在上班时间（周一至周五的9:00~18:00）可以登录。将user1的登录时间配置界面截图。

> Active Directory用户和计算机-***.com-Users-user1属性-账户-登录时间

{% asset_img 10.png %}

