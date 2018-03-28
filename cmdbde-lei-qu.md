## CMDB为什么不成功
---
##### 组织设计问题

就是以什么为核心去划分资源、组织资源。

最好是以服务为核心，如小米的服务树。

##### 产品设计问题

* 产品易用性问题：易用性不够，你怎么让能用户有使用的欲望呢？
* 信息复杂：很多产品都管理了一些无光的信息，信息的管理归类也是有考究的，没归类好，用户又被淹没了。
* 流程不合理：很多配置的变更都是因为场景变更引起的，比如说机器搬迁导致机器的物理位置信息发生变化，那就搞一个机器搬迁流程吧；机器上的业务下线了，但进程信息没有清理，那是业务下线流程的问题

##### 和应用没有关联

要以应用（服务）为核心，并对CMDB进行中心化。

## CMDB重构逻辑

##### 重构CMDB思想
* 一切皆资源
* 划为两层：底层基础资源层和应用的信息管理层

##### 重构CMDB方法
* 放弃excel
* 构建CMDB的微内核和弹性CMDB模型库
  * 微内核：只需要应用、集群和主机三个概念就可以构建起一个CMDB，基于这三个概念，可以不断去向周边扩散。应用可以往用户侧的概念不断靠拢，形成业务的概念。主机可以在其关联或者拥有的资源上不断去扩展，比如说主机所在的机柜、机柜所在的机房、机器关联的交换机等等。
  * 弹性模型：这个微内核，可以适用一切场景，但还不够，如何保证这个模型对所有企业做到落地可适配的？这个时候就是弹性模型的作用了。弹性模型由对象的弹性和对象CI及其关联的弹性定义实现的。TODO
* 自动发现+标准流程+人工维护
* 持续迭代的过程：贪大求全求细、一步到位都是它的反义词，建议以微内核和核心需求为中心，快速实现，然后在此基础上快速迭代。Docker和其他类似服务化平台出现之后，又如何实现这类资源的管理
* 边界：CMDB实现拓扑是为了故障定位，但不能实现故障定位；CMDB实现资源管理，可以去评估故障影响，但不能实现故障和变更影响评估；CMDB实现业务拓扑是为了快速的故障定位，但不能实现故障根因分析；一切都是因为在CMDB提供的数据基础之上，周边系统（变更、监控、发布）借助的CMDB提供的数据能力，实现自身的场景化系统能力。

##### 重构CMDB产品形态

建立面向应用的资源管理CMDB，即以服务为核心。



CMDB应该成为运维人的入口，不仅仅是静态信息的入口，而且是一个动态变更和状态管理的入口，把面向场景的运维编排集成到CMDB之中才是未来。



---
内容来源：
[重构CMDB，避免运维之耻](http://www.yunweipai.com/archives/6856.html)

