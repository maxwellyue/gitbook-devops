## **CMDB模型层次**

---

* 核心模型<br>核心模型是记录了业务、应用和主机Host的关系，其他的关系都可以不记录。有了这个模型基本上可以运转后续的自动化和监控系统了；其次还可以有效的管理公有云上的主机信息。

* 扩展模型<br>扩展模型就是依赖核心模型扩展出来的，比如说基于应用需要找到关联的一些资源信息；基于主机找到它关联的一些依赖设备信息，比如说机柜、存储和交换机等等，不断的扩展对象模型。

## **CMDB的对象关系**
---
* 主从关系<br>这种关系是一种强父子关系，主不存在了，则从就不存在了。用明细表来表达，属于对象级别的关系。可以通过明细表来表达，在easyops平台中用内联表来表达。
* 依赖关系<br>是一种对象属性级之间的关联关系，比如说服务器放在机柜上，机柜摆在某个机房内，这是对象级别的关系。通过对象的属性关联来表达。
* 连接关系<br>主机和存储、主机和网络设备的关系，是连接关系。这种关系是动态生成的，是一种实例级的关系。



---
[如何理解CMDB的套路](http://www.yunweipai.com/archives/9652.html)