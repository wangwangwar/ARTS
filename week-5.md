# 第五周打卡

## Algorithm

## Tips

如果希望每一个需要登录的方法，都从 Session 中获得当前用户标识，并进行一些后续处理的话，我们没有必要在每一个方法内都复制粘贴相同的获取用户身份的逻辑，可以定义一个自定义注解 @LoginRequired 到 userId 参数上，然后通过 HandlerMethodArgumentResolver 自动实现参数的组装：
```java
@GetMapping("right")
public String right(@LoginRequired Long userId) {
    return "当前用户Id：" + userId;
}
```

实现见 https://time.geekbang.org/column/article/235700

## Review

### [Write a time-series database engine from scratch](https://nakabonne.dev/posts/write-tsdb-from-scratch/)

总结：
1. Motivation 内存占用高
2. 时间序列数据的特征
  - 海量数据 1,000,000/s   写性能
  - 追加写 Append-only 
  - 按时间排序 Ordered by time
  - 批量访问 Accessed in bulk
  - 最近优先 Most recent first
  - 高势 High cardinality 
3. 解决方案
  Level DB -> Prometheus,InfluxDB
  
4. tstorage

Data model

1. memory partition
 
 - Data point list
 - Out-of-order data points
 - WAL

2. disk partition 
  - Memory-mapped data
  - Metadata
 
3. Encoding
  - Delta encoding
  - Delta-of-delta encoding
  - XOR encoding

## Share

[Why and how we wrote a compiler in Rust](https://bnjjj.medium.com/why-and-how-we-wrote-a-compiler-in-rust-blog-post-series-1-x-the-context-e2f83b10edb9)

为什么：
1. 团队已有 Rust 经验且信任 Rust
2. 项目是安全相关，Rust 擅长领域
3. Compile Rust to WASM
4. 
