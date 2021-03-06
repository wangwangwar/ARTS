# 第五周打卡

## Algorithm

## Tips

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
