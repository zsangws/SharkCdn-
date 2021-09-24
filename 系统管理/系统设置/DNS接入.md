### DNS接入

1.在dns平台解析域名，并获得如下信息：

DNS主域名：输入需要解析的域名

2.在帐户设置中生成API_KEY

UID: 这个uid是dns平台自动生成的
API_KEY： API_KEY需要点击生成key,然后点保存。看下图

3.进入cdn的系统设置，点击DNS接入。如下图

![image](https://user-images.githubusercontent.com/90588289/133720402-1d73883d-6043-462f-80d4-02969af07119.png)

把相关信息接入系统设置，然后点测试连接，可测试是否对接成功

默认TTL：600
UID与API_KEY可在letcdn帐户设置中找到

备注：点击dns修复可以重新同步因网络原因没有及时更新同步的配置信息到dns解析
