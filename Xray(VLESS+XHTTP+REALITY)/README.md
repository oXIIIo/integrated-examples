介绍：

本示例实现类似 Xray 的 [VLESS+XHTTP+TLS](https://github.com/lxhao61/integrated-examples/tree/main/Xray(VLESS%2BXHTTP)%2BNginx%5CCaddy) 应用，TLS 由 REALITY 取代。可指向别人的网站，无需自己买域名、配置 TLS 服务端，更方便，实现向中间人呈现指定 SNI 的全程真实 TLS，可解决 SNI 名单阻断问题。

原理：

使用目标网站证书（受信证书）的 TLS 伪装代理。

注意：

1、Xray 版本不小于 v24.10.31，其 XHTTP 传输方式才正式支持 REALITY。

2、若目标网站使用外部的，其网站最低要求：国外网站、域名非跳转、支持 TLSv1.3 与 HTTP/2，是否符合要求可用 [SSL Server Test](https://www.ssllabs.com/ssltest/) 检查。

3、若目标网站使用自己的，其配置修改及网站配置可参考 [Xray(M+H+G+B+A)+Nginx](https://github.com/lxhao61/integrated-examples/tree/main/Xray(M%2BH%2BG%2BB%2BA)%2BNginx) 或 [Xray(M+H+D+G+B+A)+Caddy(N+T)](https://github.com/lxhao61/integrated-examples/tree/main/Xray(M%2BH%2BD%2BG%2BB%2BA)%2BCaddy(N%2BT)) 示例。
