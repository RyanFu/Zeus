# Zeus

<p align="center">
<img src="/images/logo.png" alt="Zeus" width="100">
</p>

![](https://img.shields.io/badge/zeus-1.0-orange)       ![](https://img.shields.io/badge/license-apache-brightgreen)

### 介绍

Zeus可以用于服务发现，服务治理，负载均衡，服务容错，服务调用，API网关，配置中心。

理念是用最简单的方式使用。

#### 服务注册

引入zeus-client，在启动类添加`@ZeusRegistry`标签即可。

* registryName ：命名空间(集群管理)
* zkAddr ：zookeeper地址
* serverName ：服务名称
* serverAddr ：服务注册地址

```java
@SpringBootApplication
@ZeusRegistry(registryName = "user-center", zkAddr = "192.168.124.16:2181",
        serverName = "server-1", serverAddr = "48.89.13.53:8080")
public class ZeusDemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(ZeusDemoApplication.class, args);
    }
}
```
