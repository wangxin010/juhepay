# 聚合支付
以Spring Cloud Alibaba技术栈开发的平台，它将目前主流的第三方支付进行整合，形成第三方支付的聚合通道

### 项目介绍

- 聚合支付目前主要的做法就是线上聚合收银台(开放API)，线下C2B一码多付、线下B2C商家扫码。平台应以SaaS服务形式提供给各商户订单管理、门店管理、财务数据统计等基础服务，平台主要包括三个模块，官网&开放平台、商户平台、运营平台。
- 聚合支付是以Spring Cloud Alibaba技术栈开发的平台，它将目前主流的第三方支付进行整合，形成第三方支付的聚合通道。为线上商户提供聚合收银，为线下商户提供C2B一码多付、B2C商家扫码功能，并以SaaS服务形式提供给各商户订单管理等基础服务。



### ![image-1](jpg\image-1.png)软件架构

微服务技术栈
所有微服务基于 Spring Boot 、Spring Cloud Alibaba 构建。

控制层
Spring MVC 、Swagger

业务层
事务控制：Spring
数据缓存：Spring Data Redis
消息队列：Spring RocketTemplate
持久层
MySQL 数据库
MyBatisPlus 持久层框架
连接池 com.alibaba.druid （采用 druid-spring-boot-starter ）



![image-20230406002556455](jpg\image-2.png)

### 数据库

- shanjupay_merchant_service 用户中心数据
- shanjupay_transaction 交易服务数据库

### 项目工程

- 商户平台应用(shanjupay-merchant-application) 为前端提供商户管理功能
- 商户服务API(shanjupay-merchant-api) 定义商户服务提供的接口
- 商户服务(shanjupay-merchant-service) 实现商户服务的所有接口