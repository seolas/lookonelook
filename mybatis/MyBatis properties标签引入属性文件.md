文件结构：
第一步，db.properties
```properties
#key=value
#mysql8版本
db.driver=com.mysql.cj.jdbc.Driver
db.url=jdbc:mysql://localhost:3306/dbdemo
db.username=root
db.password=root
```
第二步，mybatis-config.xml
```xml
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE configuration
        PUBLIC "-//mybatis.org//DTD Config 3.0//EN"
        "http://mybatis.org/dtd/mybatis-3-config.dtd">
<configuration>
    <properties resource="db.properties"></properties>
    <environments default="development">
        <environment id="development">
            <transactionManager type="JDBC"></transactionManager>
            <dataSource type="POOLED">
                <property name="driver" value="${db.driver}"/>
                <property name="url" value="${db.url}"/>
                <property name="username" value="${db.username}"/>
                <property name="password" value="${db.password}"/>
            </dataSource>
        </environment>
    </environments>
    <!-- 设置映射文件路径-->
    <mappers>
        <mapper resource="mapper/UserMapper.xml"/>
    </mappers>

</configuration>
```
文件结构：
<img src="https://user-images.githubusercontent.com/59484008/196708428-d563dd20-f580-488c-9f55-679a23f2d95c.png" width="60%">
