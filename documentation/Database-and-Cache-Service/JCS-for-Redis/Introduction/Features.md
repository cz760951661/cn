# 功能特点

## 产品功能
### 数据持久化存储
- Redis将数据完全保存在内存中，保证了高效性，并且同时会在物理磁盘进行持久化，保证数据安全性。

### 丰富的数据类型
- 兼容开源Redis协议中定义的所有数据类型，如字符串（String）、链表（List）、集合（Set）、有序集合（SortedSet）、哈希表（Hash），充分满足业务需求。

### 主从备份
- 确保数据的可靠完整，以及故障时的用户无感知切换。

### 操作具有原子性
- 确保如果有多个客户端并发访问时，Redis服务器能够接收到更新的值。
