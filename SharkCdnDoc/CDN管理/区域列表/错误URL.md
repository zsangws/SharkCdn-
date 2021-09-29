### 错误URL

点击CDN管理--区域列表--配置--错误URL

![image](https://user-images.githubusercontent.com/90588289/134640725-5eaee839-cfb0-46ea-8a09-5b977a62ef0b.png)

![image](https://user-images.githubusercontent.com/90588289/133735570-55c9bdd1-d5fd-4a17-994e-35a656922818.png)

备注：错误url主要是配置独立主控的自定义错误状态码时会用到

独立主控自定义错误状态码

输入域名，https格式为：```https://域名:4430/system/error``` http格式为：```http://域名:82/system/error``` 域名是你自己的域名，要解析到cdn主控ip

配置完url这个地址在浏览器的访问效果如下就是正常的：

function $(id){if(document.getElementById){return document.getElementById(id);}else if(document.all){return document.all(id);}return document.layers[id];} function check_main(){var m=$('main')
