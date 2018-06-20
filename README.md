由于 StackExchange.Redis 不可靠，导致 Microsoft.Extensions.Caching.Redis 不能放心使用。故使用 CSRedisCore 作为分布式缓存。

# 使用方法

> Install-Package Caching.CSRedis -Version 2.1.2

```csharp
public void ConfigureServices(IServiceCollection services) {
	services.AddSingleton<IDistributedCache>(new Microsoft.Extensions.Caching.CSRedisCache());
}
```