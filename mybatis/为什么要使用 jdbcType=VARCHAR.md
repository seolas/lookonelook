MyBatis 通过`@Param("xxx")` 和 `#{xxxx}` 传递参数给数据库，会将 Java 类型转为数据库的数据类型，如果传入的是 null 值，类型转换错误时会报错。jdbcType 针对为空的字段，手动转换为指定的类型，如 `#{xxx, jdbcType = VARCHAR}`。

> 参考链接：https://blog.csdn.net/qq_42739012/article/details/81220214
