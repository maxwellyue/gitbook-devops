# 小米运维平台和监控

主要分为服务树、监控系统、部署系统三部分。

## 服务树

### 组织方式

公司-部门-产品线-服务-模块-分组-机房-状态

### 筛选、反筛选、权限管理

* 某个服务部署在哪些机器上（API接口或命令行工具）
* 某个机器上有哪些模块（API接口或命令行工具）
* 哪些人对哪些机器有哪些权限

### 服务树设计

标签的定义  
一个有特定意义的属性，所有的标签都可以显示在树上，比如：机房、位置、在线状态、产品线、模块。

标签的运用  
①机器的“状态”发生变化的时候，伴随着标签的变更  
②“状态”什么时候会发生变更：人工操作；周边系统

举例：  
筛选上地机房offline机器：idc.sd, status.offline  
筛选米聊产品线第一个分组：pdl.miliao, grp.1

## 基于服务树的服务监控

TODO

