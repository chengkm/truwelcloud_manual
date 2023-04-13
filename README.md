# 快速了解

## 它是什么?

华益瑞数据云平台(Truwel Cloud)是完全由华益瑞自主研发的一套**完整的**、**通用的**B/S架构数据管理平台，能够让广大科研用户快速便捷地管理台站的**数据**、**照片**、**监控**等各种类型业务数据。

平台目前用户有中国林业科学研究院、中国科学院新疆生态与地理研究所、中国科学院青藏高原研究所、中国生态系统研究网络(CERN)等。

## 主要特性

- 可部署在用户`Windows`/`Linux`服务器
- 后端支持`单体版`或`微服务版`
- 前端页面响应式布局
- 接口符合`RESTful API`规范
- 支持按钮级别数据权限
- 保证用户之间绝对的权限隔离
- 支持`微信`、`QQ`、`钉钉`、`短信`、`邮件`等多种方式的告警信息推送
- 支持数据报表一键导出
- 支持`MQTT`消息接入
- 支持国内外数采数据接入
- 支持物候照片及数据文件管理
- 支持符合国标GB28181监控视频接入
- 支持LAS点云数据接入

## 技术选型
1、系统环境
- Java EE 8
- Apache Maven 3
- Node 16
- NPM 8

2、主框架

`单体版`

- Spring Boot
- Spring Security

> 视频监控架构图:point_down:
<div align=center><img src="_media/video-architecture.png" width="70%"/></div>

视频监控`信令服务`与`流媒体服务`均采用成熟`开源`框架搭建,更加注重用户监控数据安全

`微服务版`

- Spring Cloud Hoxton
- Spring Framework

> 微服务版架构图:point_down:
<div align=center><img src="_media/truwel_spring_cloud.png" width="70%"/></div>

3、持久层
- Apache MyBatis
- Alibaba Druid

4、消息中间件
- ActiveMQ
- Kafka

5、视图层
- Vue全家桶
- Element UI

6、数据库
- Mysql
- Redis

## 系统需求

- JDK >= 1.8
- MySQL >= 5.7
- Redis >= 7.0.0
- Windows Server or Linux
- 2核(vCPU) 8GiB内存 30GiB硬盘 5Mbps带宽

## 浏览器支持

支持现代浏览器, 不支持 IE
<div style="width: auto;
  display: table;
  margin-left: auto;
  margin-right: auto">

| [<img src="_media/edge_48x48.png" alt=" Edge" width="24px" height="24px" />]()</br>IE | [<img src="_media/edge_48x48.png" alt=" Edge" width="24px" height="24px" />]()</br>Edge | [<img src="_media/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />]()</br>Firefox | [<img src="_media/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />]()</br>Chrome | [<img src="_media/safari_48x48.png" alt="Safari" width="24px" height="24px" />]()</br>Safari |
| :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|                                                                                             not support                                                                                              |                                                                                            last 2 versions                                                                                             |                                                                                                  last 2 versions                                                                                                  |                                                                                                last 2 versions                                                                                                |                                                                                                last 2 versions                                                                                                |

</div>

# 使用手册

## 注册

<div align=center><img src="_media/register.png" width="100%"/></div>

> :raising_hand: 如果想体验平台功能可在首页进行注册，申请通过后会通过邮件通知

## 首页

<div align=center><img src="_media/dashboard_sidebar.jpg" width="50%"/><img src="_media/dashboard_topnav.jpg" width="50%"/></div>
<div align=center><img src="_media/dashboard_egi.png" width="50%"/><img src="_media/dashboard_exhibition.png" width="50%"/></div>
<div align=center><img src="_media/dashboard3.png" width="50%"/><img src="_media/dashboard4.png" width="50%"/></div>
<div align=center><img src="_media/Kapture 2022-06-25 at 20.30.01.gif" width="100%"/></div>
<div align=center><img src="_media/dashboard_mapbox.gif" width="100%"/></div>

:bar_chart: 系统页面分为三大部分，菜单栏用于切换不同功能，导航栏用于展示用户信息、报警信息以及路由信息，主区域展示各种数据信息；首页大屏可根据用户需求定制不同样式

> :100: 支持皮肤切换、展示数据自定义、分组全屏功能、左侧或顶部菜单栏切换
## 站点数据

### 气象数据

<div align=center><img src="_media/analysis_data_split.gif" width="70%"/></div>

> **提示：** 可以拖拽中间区域:point_left:调整左右显示比例

#### 数据图表

<div align=center><img src="_media/analysis_classification.png" width="70%"/></div>

默认显示第1个表格前两个字段的最近24小时数据，可通过设置按钮进行参数和间隔时间的选择，通过点击左边树形列表进行站点切换显示

> **提示：** 树形列表可按照系统类型进行划分展示;支持参数中:cn:英:us:显示、单位显示

#### 最新数据

<div align=center><img src="_media/analysis_data_realtime.png" width="70%"/></div>

展示表格最新一条数据，同样可以通过点击左边树形列表进行站点切换显示

#### 数据分析

<div align=center><img src="_media/analysis_data_diagram.png" width="70%"/></div>

在这里可以对数据进行更细化的分析，包括`折线图`、`散点图`、`风玫瑰`、`梯度图`、`列表`，可以对数据进行列表下载或打包下载

> **提示：** 参数可以随意组合，支持跨站点数据分析

### 物候数据

<div align=center><img src="_media/analysis_img_normal.png" width="50%"/><img src="_media/analysis_img_ndvi.png" width="50%"/></div>

平台按照物候图片的类型进行分类展示，后期将增加GCC实时计算功能

> :camera: 目前支持`CCFC`、`NetCam`、`PhotoNet`等市面主流物候相机

### 点云数据

<div align=center><img src="_media/analysis_point_cloud.png" width="50%"/></div>

> :cloud: 目前仅支持`LAS`格式点云

### 视频监控

<div align=center><img src="_media/analysis_video.png" width="50%"/></div>

> **提示：** 可一、四、九分屏展示

### 原始文件

<div align=center><img src="_media/analysis_file_unique.png" width="50%"/></div>

平台除了将对接数据直接入库外，不管原始文件是追加模式还是唯一模式都可以很方便地进行管理

### 数据管理

<div align=center><img src="_media/analysis_data.png" width="50%"/><img src="_media/analysis_data_upload.png" width="50%"/></div>

数据的:arrow_up:上传、:arrow_down:下载就在这里

> **提示：** 平台能够记住用户上次下载记录，方便之后进行一键下载:thumbsup:

### 数据报表

<div align=center><img src="_media/analysis_report.png" width="50%"/><img src="_media/analysis_report_excel.png" width="44%"/></div>

> **提示：** 可按周、月和季度定时生成:page_facing_up:


### 系统详情

<div align=center><img src="_media/analysis_station_map.png" width="50%"/><img src="_media/analysis_station_document.png" width="50%"/></div>

全景图/视频、地图、档案资料等多种方式进行展示

## 系统监控

### 传输监控

<div align=center><img src="_media/monitor_transmit.png" width="70%"/></div>

对数据传输状态进行实时监控

> 1. 蓝色=>正常 
> 2. 红色=>离线

### 系统监控

<div align=center><img src="_media/monitor_server.png" width="70%"/></div>

对服务器CPU、Java虚拟机、磁盘状态进行实时监控

### 缓存监控

<div align=center><img src="_media/monitor_redis.png" width="70%"/></div>

对Redis缓存进行实时监控

### 在线用户

<div align=center><img src="_media/monitor_online.png" width="70%"/></div>

对已登陆平台的用户进行管理，可以对其进行强退操作

## 系统管理

### 用户管理

<div align=center><img src="_media/sys_user.png" width="50%"/><img src="_media/sys_user_categories.png" width="44%"/></div>


> 一个用户可以分配多个角色

### 角色管理

<div align=center><img src="_media/sys_role.png" width="50%"/><img src="_media/sys_role_permission.png" width="50%"/></div>


### 菜单管理

<div align=center><img src="_media/sys_menu.png" width="70%"/></div>

可以对平台菜单栏内容进行更改，包括名称、顺序、图标等

### 视频管理

<div align=center><img src="_media/sys_video_device.png" width="70%"/><img src="_media/sys_video_channel.png" width="70%"/></div>

管理监控设备、视频通道、控制云台等

### 站点管理

<div align=center><img src="_media/sys_station.png" width="50%"/><img src="_media/sys_station_field.png" width="50%"/></div>

平台按照`站点`->`系统`->`数据表`三级进行分类，在`数据表`层可继续细分`数据`、`图片`和`文件`三大类

> 平台目前支持`campbell数据`、`mqtt消息`、`本地文件`等多种市面主流数据类型，其他类型可根据需求进行定制开发

## 日志管理

### 数据告警

<div align=center><img src="_media/log_warning.png" width="70%"/></div>

### 登陆日志

<div align=center><img src="_media/log_login.png" width="70%"/></div>

### 操作日志

<div align=center><img src="_media/log_operate.png" width="70%"/></div>

> 操作日志颗粒度可根据用户需求增减