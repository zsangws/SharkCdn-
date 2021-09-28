### 防SQL注入

点击CDN管理--区域列表--配置--防SQL注入

![image](https://user-images.githubusercontent.com/90588289/134640725-5eaee839-cfb0-46ea-8a09-5b977a62ef0b.png)

![image](https://user-images.githubusercontent.com/90588289/133735783-76c31b06-be24-42db-a41f-52c23df07958.png)

备注：代码如下：

'.*[; ]?((or)|(insert)|(select)|(union)|(update)|(delete)|(replace)|(create)|(drop)|(alter)|(grant)|(load)|(show)|(exec))[\s(]
