###  **一键申请ssl证书相关错误解释**

证书申请失败首先需要排查的原因：

1.cdn节点的状态是否正常

2.域名是否有正确解析到cdn自动生成的别名，或直接解析到cdn的节点ip

3.独立cdn主控的用户还需查看主控服务器上的ssl进程是否有运行，如果没有运行命令如下：

sh /vhs2/boot.sh

申请 SSL/TLS 证书的常见错误列表及解决方式

错误类型：```urn:acme:error:connection```

1、错误信息：```DNS problem: NXDOMAIN looking up A for test.com```

错误原因：域名不存在

解决方式1：检查域名是否填写正确

解决方式2：到域名注册商处检查是否设置了 DNS 服务器

解决方式3：咨询 DNS 服务商是否支持解析该域名

2、错误信息：```DNS problem: SERVFAIL looking up A for test.com```

错误原因：DNS 解析 A 记录出错

解决方式1：到域名注册商处检查是否设置了 DNS 服务器

解决方式2：咨询 DNS 服务商是否屏蔽了 Let’s Encrypt 的解析请求

3、错误信息：```DNS problem: SERVFAIL looking up CAA for test.com```

错误原因：DNS 解析 CAA 记录出错

解决方式1：到域名注册商处检查是否设置了 DNS 服务器

解决方式2：咨询 DNS 服务商是否支持解析 CAA 记录

4、错误信息：```DNS problem: query timed out looking up A for test.com```

错误原因：DNS 解析超时

解决方式1：到域名注册商处检查是否设置了 DNS 服务器

解决方式2：咨询 DNS 服务商是否屏蔽了 Let’s Encrypt 的解析请求

解决方式3：重新申请

解决方式4：cdn节点的ip状态是否正常

5、错误信息：```Fetching http://test.com/.well-known/acme-challenge/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx: xxxxxxxx```

错误原因：获取域名验证信息失败

解决方式1：重新申请

解决方式2：请确认是否启动了 DNS 的分区解析。如果有则要把国外的解析记录也设置成 CNAME 至 pages.coding.me。SSL 证书是通过 Let’s Encrypt API 申请。申请证书前需要验证域名，而 Let’s Encrypt 位于国外，所以需要保证 Let’s Encrypt 能通过您的域名正常访问到 cdn节点服务器以读取验证信息。

错误类型：```urn:acme:error:malformed```

错误信息：Error creating new authz :: Name does not end in a public suffix

错误原因：域名不以公共后缀结尾

解决方式：咨询域名注册商

错误类型：```urn:acme:error:unauthorized```

1、错误信息：```Invalid response from http://test.com/.well-known/acme-challenge/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx: xxxxxxxxx```

错误原因：无法获取正确的域名验证信息

解决方式1：检查 DNS 的 CNAME 记录是否设置正确

解决方式2：cdn节点的ip状态是否正常

2、错误信息：```The key authorization file from the server did not match this challenge```

错误原因：无法获取正确的域名验证信息

解决方式1：检查 DNS 的 CNAME 记录是否设置正确

解决方式2：cdn节点的ip状态是否正常

3、错误信息：```Error creating new authz :: “test.com” was considered an unsafe domain by a third-party API```

错误原因：无法获取正确的域名验证信息

解决方式：使用 ```https://transparencyreport.google.com/safe-browsing/search``` 查看域名存在的安全隐患，按照说明进行清理，清理完后到 ```https://www.stopbadware.org/``` 提交审查请求。审查通过后，回到 Coding Pages 重新申请证书

错误类型：```urn:acme:error:unknownHost```

错误信息：No valid IP addresses found for test.com

错误原因：找不到可用 IP 地址

解决方式1：检查 DNS 的 CNAME 记录是否设置正确

解决方式2：cdn节点的ip状态是否正常

解决方式3：咨询 DNS 服务商是否屏蔽了 Let’s Encrypt 的解析请求

错误类型：```urn:acme:error:rateLimited```

错误信息：```Error creating new cert :: too many certificates already issued for exact set of domains: test.com```

错误原因：证书申请数目超出限制

解决方式：下周再重新申请，详情见 ```https://letsencrypt.org/docs/rate-limits/```

错误类型：```urn:acme:error:rejectedIdentifier```

错误信息：```Error creating new authz :: Policy forbids issuing for name```

错误原因：相关政策禁止为此域名签发证书
