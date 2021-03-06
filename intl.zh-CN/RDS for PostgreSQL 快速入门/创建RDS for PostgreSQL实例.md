# 创建RDS for PostgreSQL实例 {#concept_kzn_qcg_wdb .concept}

您可以通过阿里云RDS管理控制台或API创建RDS实例。关于实例计费说明，请参见[云数据库RDS详细价格信息](https://www.alibabacloud.com/product/apsaradb-for-rds?spm=a3c0i.7938564.220486.8.10521d15zCpnIt#pricing)。本文将介绍在RDS管理控制台上创建实例的步骤，关于如何通过API创建实例的信息，请参见[创建RDS实例](../intl.zh-CN/API参考/实例管理/CreateDBInstance.md#)。

## 前提条件 {#section_vqd_tcg_wdb .section}

-   已注册阿里云账号。

## 注意事项 {#section_kmf_kkp_mgb .section}

-   包年包月实例无法转为按量付费实例。
-   按量付费实例可以转为包年包月实例，请参见[按量付费转包年包月](../intl.zh-CN/用户指南/计费管理/按量付费转包年包月.md#)。
-   同一个主账号，最多可以创建30个按量付费的RDS实例。如需提高此限额，请[提交工单](https://workorder-intl.console.aliyun.com/console.htm#/ticket/createIndex)申请。

## 操作步骤 {#section_nk5_5cg_wdb .section}

1.  登录[RDS管理控制台](https://rds.console.aliyun.com/?spm=5176.doc43185.2.7.mR2Syx)。
2.  在实例列表页面，单击**新建实例**，进入创建页面。
3.  选择**包年包月**或**按量付费**。关于计费方式的选择，请参见。
4.  选择实例配置，参数说明如下。

    |参数|说明|
    |--|--|
    |地域|实例所在的地理位置。购买后无法更换地域。    -   请根据目标用户所在的地理位置就近选择地域，提升用户访问速度。
    -   请确保RDS实例与需要连接的ECS实例创建于同一个地域，否则它们无法通过内网互通，只能通过外网互通，无法发挥最佳性能。
|
    |资源组|实例所属的资源组。|
    |数据库类型|     -   即数据库引擎的类型：MySQL、SQL Server、PostgreSQL和PPAS。
    -   不同地域支持的数据库类型不同，请以实际界面为准。
 |
    |版本|指数据库版本。RDS for PostgreSQL支持的数据库版本包括PostgreSQL 9.4、PostgreSQL 10。不同地域所支持的数据库版本不同，请以实际界面为准。|
    |系列|    -   基础版：单节点，计算与存储分离，性价比高。
    -   高可用版：一个主节点和一个备节点，经典高可用架构。
关于各个系列的详细介绍，请参见[产品系列概述](../intl.zh-CN/云数据库RDS简介/产品系列/产品系列概述.md)。不同数据库版本支持的系列不同，请以实际界面为准。

|
    |可用区|可用区是地域中的一个独立物理区域，不同可用区之间没有实质性区别。您可以选择将RDS实例的主备节点创建在同一可用区或不同可用区。

|
    |网络类型|     -   经典网络：传统的网络类型。
    -   专有网络（推荐）：也称为VPC（Virtual Private Cloud）。VPC是一种隔离的网络环境，安全性和性能均高于传统的经典网络。

**说明：** 请确保RDS实例与需要连接的ECS实例网络类型一致，否则它们无法通过内网互通。

 |
    |规格|每种规格都有对应的CPU核数、内存、最大连接数和最大IOPS。具体请参见[实例规格表](../intl.zh-CN/云数据库RDS简介/实例规格/实例规格表.md#)。RDS实例有以下规格族：

    -   通用型：独享被分配的内存和I/O资源，与同一服务器上的其他通用型实例共享CPU和存储资源。
    -   独享型：独享被分配的CPU、内存、存储和I/O资源。
    -   独占物理机型：是独享型的顶配，独占整台服务器的CPU、内存、存储和I/O资源。
例如，**8核32GB**是通用型实例规格，**8核32GB（独享套餐）**是独享型实例规格，**30核220GB（独占主机）**是独占物理机型实例规格。

|
    |存储空间|该存储空间包括数据空间、系统文件空间、Binlog文件空间和事务文件空间。|

5.  设置购买时长（仅针对包年包月实例）和实例数量，然后单击右侧的**立即购买**。

    **说明：** 对于包年包月实例，您也可以单击**加入购物车**将实例加入到购物车中，最后单击**购物车**进行结算。

6.  在订单确认页面，勾选**《产品服务条款》和《服务级别协议》和《使用条款》**，根据提示完成支付。

## 下一步 {#section_msy_dgt_2fb .section}

在控制台左上角，选择实例所在的地域即可查看到刚刚创建的实例。

![选择地域](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/7814/154780239536543_zh-CN.png)

创建实例后，您需要[设置白名单](intl.zh-CN/RDS for PostgreSQL 快速入门/初始化配置/设置白名单.md)和[创建账号](intl.zh-CN/RDS for PostgreSQL 快速入门/初始化配置/创建数据库和账号.md)，如果是通过外网连接，还需要[申请外网地址](https://www.alibabacloud.com/help/zh/doc-detail/97738.htm)。然后就可以[连接实例](intl.zh-CN/RDS for PostgreSQL 快速入门/连接实例.md)。

## 相关API {#section_etp_dbb_kgb .section}

|API|描述|
|---|--|
|[CreateDBInstance](../intl.zh-CN/API参考/实例管理/CreateDBInstance.md#)|创建RDS实例|

