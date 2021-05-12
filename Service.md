# Service/业务逻辑层

#### Service层中每一个方法都是一个事务



使用多个Dao中的方法

```
conn.setAutoCommit(false);// 数据库链接设置为手动提交

conn.commit();// 数据库提交

conn.rollback();// 异常回退
```

