### **操作步骤**

1. 
登录京东云控制台。
1. 
在左侧导航栏，点击私有网络-公网IP，然后在弹性公网IP列表页面选择需要绑定资源的弹性公网IP，点击操作栏中的“绑定资源”。如下图所示：
![弹性公网IP绑定云主机1.png](https://img1.jcloudcs.com/cms/94d3013e-1f56-443e-9e2f-597a59a57a4220180416102413.png "弹性公网IP绑定云主机1.png")
1. 
弹性公网IP列表页面弹出选择资源弹框，依据需求，选择云主机标签页，在列表中选择需要绑定的资源。如下图所示：
![弹性公网IP绑定云主机2.png](https://img1.jcloudcs.com/cms/5a11a32e-97e4-4c4d-aa6a-c9d34a21a5b220180416102434.png)
1. 
选定弹性公网IP需要绑定的资源，点击“确定”。
1. 
绑定成功，页面返回弹性公网IP列表页，并更新弹性公网IP的绑定状态；绑定失败，页面将出现提示信息，请重新尝试绑定，如果多次绑定失败，请联系客服人员。
1. 
注意：需保证绑定的资源所在子网所关联的路由表中有访问公网的路由规则(路由的下一跳类型和下一跳均为Internet网关)，否则资源仍不能通过弹性公网IP进行公网通信。