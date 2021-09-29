### cdn配置部骤流程图:

![image](https://user-images.githubusercontent.com/90588289/134606462-0cc3014d-b8c1-416d-8f88-291e4753e271.png)

### 第一步： 配置DNS接入

![image](https://user-images.githubusercontent.com/90588289/134446404-8fcee193-0fc9-4387-9c74-0629edf3ce97.png)

接入文档：[DNS接入](/SharkCdnDoc/系统管理/系统设置/DNS接入.md)

### 第二步：增加区域和增加节点

(1).新增一个区域

![image](https://user-images.githubusercontent.com/90588289/134446437-9523368c-6332-42b9-b774-be7e87d087ed.png)

立即配置：[添加区域](zh-cn/SharkCdnDoc/CDN管理/区域列表/添加区域.md)

(2). 点击CDN管理---节点列表---新增节点 会弹出节点的安装程序

![image](https://user-images.githubusercontent.com/90588289/134446455-cbb2c796-e881-4a96-bd0d-95742fdd42d6.png)

立即配置：[添加节点](zh-cn/SharkCdnDoc/CDN管理/节点列表/添加节点.md)

(3).linux服务器，直接复制下图脚本命令运行。windows服务器，下载对应版本到服务器上运行安装。

![image](https://user-images.githubusercontent.com/90588289/134446470-76f1498e-e447-4383-80d0-9f0c8ab0c100.png)

(4).安装成功后,节点会出现在待初始化列表,点击初始化

![image](https://user-images.githubusercontent.com/90588289/134446496-0f8f2548-0d50-483e-8228-6f9d9656230d.png)

注:4.6.0版初始化是默认不显示，有新节点需要初始化时会自动显示

区域：选择要初始化节点到哪个区域

名称：设置节点的名字，只能用英文和数字。

节点类型：选择默认的边缘节点就行了。 中间节点是多层CDN功能(需vip4以上套餐支持)。

备注：可留空

![image](https://user-images.githubusercontent.com/90588289/134446514-2636db7a-dccb-4dd0-885f-92ff479cb79f.png)

(5). 初始化成功后，节点会显示在对应的区域中，显示版本号则表示节点连接主控后台正常

![image](https://user-images.githubusercontent.com/90588289/134446533-35b1f317-4c28-4e53-8659-3c3a320ae742.png)

### 第三步：分组解析

在分组解析中启用相应的节点ip(分组可自行新增，同一区域下的节点可在不同分组中共用)，

立即配置：[新建分组](zh-cn/SharkCdnDoc/CDN管理/分组解析/新建分组.md)

(1). 点击分组解析，进入分组，点击分组名称，进入启用节点界面

![image](https://user-images.githubusercontent.com/90588289/134446548-b9d913f5-8532-43a8-8098-7820d8e8b72e.png)

(2). 如下图操作选择启用节点，添加到右边的为启用的ip

![image](https://user-images.githubusercontent.com/90588289/134446561-a644de98-b3cf-460f-94da-cecd86c67d6b.png)

### 第四步：新增产品

如下图点击新增产品，根据自已需求设置产品

端口类型中混合端口是vip4套餐功能，可同时支持四层端口和七层端口

注：七层主分组和副分组如果有多个是可以多选的，在新增站点时会随机指定一个主分组和副分组

![image](https://user-images.githubusercontent.com/90588289/134446579-23de9056-1b30-4245-9354-3f58dfd611c5.png)

立即配置：[添加产品](zh-cn/SharkCdnDoc/CDN管理/产品列表/添加产品.md)

### 第五步：新增站点

如下图点击站点列表--添加站点--输入站点名称、密码（选填），增加站点

![image](https://user-images.githubusercontent.com/90588289/134446595-d4ac24fc-ce07-4792-a1dc-16311b8b57a2.png)

### 第六步：登陆站点

点击站点列表，点击站点名登录

![image](https://user-images.githubusercontent.com/90588289/134446615-dea979b0-4210-4f60-b7a3-63b4e964eb10.png)

### 第七步：添加域名

记录管理--添加域名，域名是要做cdn的域名，IP是源服务器IP, CNAME系统会自动生成

![image](https://user-images.githubusercontent.com/90588289/134446635-b28a9769-f67d-4d91-b21f-52d5421be052.png)

到这里就配置完成了
