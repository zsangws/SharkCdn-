Cdn三种添加ssl证书的方法

一、第一种在站点设置中添加：

![image](https://user-images.githubusercontent.com/90588289/133751334-d8196aea-c1c0-451d-a335-3e4b327cfdae.png)

点打开，加入证书后点提交

![image](https://user-images.githubusercontent.com/90588289/133751344-d555b34b-50b6-4fa5-a63c-f44b7ba3e68a.png)

可以点检测功能检查证书是否有效，打勾说明证书是有效的，打叉说明证书无效

二. 第二种是在域名记录里添加：

如下图点击，添加证书后点确定即可

![image](https://user-images.githubusercontent.com/90588289/133751358-61891461-df4a-467a-80e0-526160f901dc.png)

三. 第三种是用sharkcdn自动获取证书功能：

开启申请ssl证书前域名要做好cname解析记录，或者域名直接解析到了节点的ip也行

如下图点击开启自动申请ssl证书的功能

![image](https://user-images.githubusercontent.com/90588289/133751382-f5222a12-ab59-420f-9eaa-14b4f81a60d6.png)

如下图显示就申请成功了，到期后会自动续期，（注：独立主控用户开通这个功能需联系客服开通）

自动申请证书也有可能失败，失败可先检查下解析是否做好，然后重新申请

![image](https://user-images.githubusercontent.com/90588289/133751396-6df1d446-a0c0-4576-b5d1-99e866a5c390.png)

以上就是三种添加证书的方式

备注：无
