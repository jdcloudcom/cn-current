**实现基于4层（TCP协议）的监听转发**

### **准备与规划**

* 
网络准备

根据业务部署需求，需提前规划负载均衡所在地域、可用区、所属私有网络、子网，配置网络ACL规则等。

* 
服务器准备

需提前创建承载业务流量的云主机，并确保打开监听所需的端口，合理配置安全组策略。

注意：负载均衡与后端服务器需要在同一地域、同一私有网络下，否则无法实现监听和流量转发。

### **创建负载均衡实例**

通过控制台菜单-负载均衡打开负载均衡资源列表页，点击“创建”新建一个负载均衡实例。

![1.png](https://img1.jcloudcs.com/cms/81f5cb86-0956-4da0-8294-5f4e1ba9389820171207202514.png)

选择相应的地域、可用区、私有网络、子网、公网IP，设置负载均衡实例名称，点击右侧“立即购买”。

![2.png](https://img1.jcloudcs.com/cms/6b2b9286-177c-47d9-a428-783abf30dc2420171207202527.png)![2-1.png](https://img1.jcloudcs.com/cms/46ea21b4-d010-42db-bbd2-da0e3593995f20171207202533.png)

确认订单信息并完成支付，创建负载均衡实例。

![3.png](https://img1.jcloudcs.com/cms/bafd8902-a6b6-43e3-9e6f-08291bcc07d820171207202543.png)

刷新负载均衡列表，查看新创建的负载均衡实例。

![4.png](https://img1.jcloudcs.com/cms/472ceb48-58df-4b18-a591-8ef6af7dde3520171207202552.png)

点击列表右侧“添加监听”打开监听规则页。

![5.png](https://img1.jcloudcs.com/cms/7e6174df-d344-4226-975b-e59d2fcb633d20171207202604.png)

**创建一个TCP监听器**

点击“添加”创建一个监听器：选择TCP协议，配置监听端口、转发规则选择轮询、绑定虚拟服务器组、配置健康检查。

![6.png](https://img1.jcloudcs.com/cms/73b33b07-a914-449a-8655-7a90084fc93420171207202612.png)

点击“新建虚拟服务器组”可添加一组后端服务器，根据业务负载情况设置监听端口和权重。

![7.png](https://img1.jcloudcs.com/cms/e8160bde-9c7d-43d4-b52c-387a93720d4020171207202621.png)

返回监听规则创建页，选择该虚拟服务器组，点击“确定”创建一个监听器。

![8.png](https://img1.jcloudcs.com/cms/0eb573dd-6c92-4fcc-ab1b-1f48a414b59a20171207202633.png)

通过“监控”查看负载均衡实例的监控信息。

![9.png](https://img1.jcloudcs.com/cms/7584a376-f433-41e3-96a0-0ecc4c72ab5620171207202702.png)