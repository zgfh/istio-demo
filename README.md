# istio-demo
整理了 istio 1.1 版本的配置,方便复制粘贴  
istio 分以下几个大类配置：
1. 流量管理： 本目录的配置
1. 策略与遥测: policies-and-telemetry 目录 
1. 安全: security 目录
1. envoy配置: envoy 目录



### 流量管理配置
主要有一下几个配置
- VirtualService 在 Istio 服务网格中定义路由规则，控制路由如何路由到服务上。(路由规则)

- DestinationRule 是 VirtualService 路由生效后，配置应用与请求的策略集。(内部后端集群定义)

- ServiceEntry 是通常用于在 Istio 服务网格之外启用对服务的请求。(pod访问外部,外部后端集群定义)

- Gateway 为 HTTP/TCP 流量配置负载均衡器，最常见的是在网格的边缘的操作，以启用应用程序的入口流量。(外部访问pod)
