drop user 'vhr'@'127.0.0.1';
create database vhr default character set utf8mb4 collate utf8mb4_unicode_ci;
use vhr;
create user 'vhr'@'127.0.0.1' identified by '123465';
grant all privileges on vhr.* to 'vhr'@'127.0.0.1';
flush privileges;


create user 'vhr'@'localhost' identified by '123465';
grant all privileges on vhr.* to 'vhr'@'localhost';
flush privileges;


org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'flywayInitializer' defined in class path resource [org/springframework/boot/autoconfigure/flyway/FlywayAutoConfiguration$FlywayConfiguration.class]: Invocation of init method failed; nested exception is org.flywaydb.core.internal.exception.FlywaySqlException:
Unable to determine value for 'foreign_key_checks' variable
-----------------------------------------------------------
SQL State  : null
Error Code : 0
Message    : connection holder is null

        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1788) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:609) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:531) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.AbstractBeanFactory.lambda$doGetBean$0(AbstractBeanFactory.java:335) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:234) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:333) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:208) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:322) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:208) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.DefaultListableBeanFactory.preInstantiateSingletons(DefaultListableBeanFactory.java:944) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.context.support.AbstractApplicationContext.finishBeanFactoryInitialization(AbstractApplicationContext.java:925) ~[spring-context-5.3.1.jar!/:5.3.1]
        at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:588) ~[spring-context-5.3.1.jar!/:5.3.1]
        at org.springframework.boot.web.servlet.context.ServletWebServerApplicationContext.refresh(ServletWebServerApplicationContext.java:144) ~[spring-boot-2.4.0.jar!/:2.4.0]
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:767) [spring-boot-2.4.0.jar!/:2.4.0]
        at org.springframework.boot.SpringApplication.refresh(SpringApplication.java:759) [spring-boot-2.4.0.jar!/:2.4.0]
        at org.springframework.boot.SpringApplication.refreshContext(SpringApplication.java:426) [spring-boot-2.4.0.jar!/:2.4.0]
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:326) [spring-boot-2.4.0.jar!/:2.4.0]
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:1309) [spring-boot-2.4.0.jar!/:2.4.0]
        at org.springframework.boot.SpringApplication.run(SpringApplication.java:1298) [spring-boot-2.4.0.jar!/:2.4.0]
        at org.javaboy.vhr.VhrApplication.main(VhrApplication.java:16) [classes!/:0.0.1-SNAPSHOT]
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[na:1.8.0_262]
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[na:1.8.0_262]
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[na:1.8.0_262]
        at java.lang.reflect.Method.invoke(Method.java:498) ~[na:1.8.0_262]
        at org.springframework.boot.loader.MainMethodRunner.run(MainMethodRunner.java:49) [vhr-web-0.0.1-SNAPSHOT.jar:0.0.1-SNAPSHOT]
        at org.springframework.boot.loader.Launcher.launch(Launcher.java:107) [vhr-web-0.0.1-SNAPSHOT.jar:0.0.1-SNAPSHOT]
        at org.springframework.boot.loader.Launcher.launch(Launcher.java:58) [vhr-web-0.0.1-SNAPSHOT.jar:0.0.1-SNAPSHOT]
        at org.springframework.boot.loader.JarLauncher.main(JarLauncher.java:88) [vhr-web-0.0.1-SNAPSHOT.jar:0.0.1-SNAPSHOT]
Caused by: org.flywaydb.core.internal.exception.FlywaySqlException:
Unable to determine value for 'foreign_key_checks' variable
-----------------------------------------------------------
SQL State  : null
Error Code : 0
Message    : connection holder is null

        at org.flywaydb.core.internal.database.mysql.MySQLConnection.getIntVariableValue(MySQLConnection.java:64) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.internal.database.mysql.MySQLConnection.<init>(MySQLConnection.java:56) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.internal.database.mysql.MySQLDatabase.doGetConnection(MySQLDatabase.java:195) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.internal.database.mysql.MySQLDatabase.doGetConnection(MySQLDatabase.java:41) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.internal.database.base.Database.getConnection(Database.java:118) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.internal.database.base.Database.getMainConnection(Database.java:326) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.Flyway.prepareSchemas(Flyway.java:627) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.Flyway.execute(Flyway.java:516) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.Flyway.migrate(Flyway.java:164) ~[flyway-core-7.1.1.jar!/:na]
        at org.springframework.boot.autoconfigure.flyway.FlywayMigrationInitializer.afterPropertiesSet(FlywayMigrationInitializer.java:66) ~[spring-boot-autoconfigure-2.4.0.jar!/:2.4.0]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1847) ~[spring-beans-5.3.1.jar!/:5.3.1]
        at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1784) ~[spring-beans-5.3.1.jar!/:5.3.1]
        ... 27 common frames omitted
Caused by: java.sql.SQLException: connection holder is null
        at com.alibaba.druid.pool.DruidPooledConnection.checkStateInternal(DruidPooledConnection.java:1155) ~[druid-1.1.10.jar!/:1.1.10]
        at com.alibaba.druid.pool.DruidPooledConnection.checkState(DruidPooledConnection.java:1148) ~[druid-1.1.10.jar!/:1.1.10]
        at com.alibaba.druid.pool.DruidPooledConnection.prepareStatement(DruidPooledConnection.java:336) ~[druid-1.1.10.jar!/:1.1.10]
        at org.flywaydb.core.internal.jdbc.JdbcTemplate.prepareStatement(JdbcTemplate.java:344) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.internal.jdbc.JdbcTemplate.queryForInt(JdbcTemplate.java:144) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.internal.database.mysql.MySQLConnection.getIntVariableValue(MySQLConnection.java:62) ~[flyway-core-7.1.1.jar!/:na]
        ... 38 common frames omitted
Caused by: java.sql.SQLSyntaxErrorException: SELECT command denied to user 'vhr'@'localhost' for table 'user_variables_by_thread'
        at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:120) ~[mysql-connector-java-8.0.22.jar!/:8.0.22]
        at com.mysql.cj.jdbc.exceptions.SQLError.createSQLException(SQLError.java:97) ~[mysql-connector-java-8.0.22.jar!/:8.0.22]
        at com.mysql.cj.jdbc.exceptions.SQLExceptionsMapping.translateException(SQLExceptionsMapping.java:122) ~[mysql-connector-java-8.0.22.jar!/:8.0.22]
        at com.mysql.cj.jdbc.ClientPreparedStatement.executeInternal(ClientPreparedStatement.java:953) ~[mysql-connector-java-8.0.22.jar!/:8.0.22]
        at com.mysql.cj.jdbc.ClientPreparedStatement.executeQuery(ClientPreparedStatement.java:1003) ~[mysql-connector-java-8.0.22.jar!/:8.0.22]
        at com.alibaba.druid.filter.FilterChainImpl.preparedStatement_executeQuery(FilterChainImpl.java:3188) ~[druid-1.1.10.jar!/:1.1.10]
        at com.alibaba.druid.filter.FilterEventAdapter.preparedStatement_executeQuery(FilterEventAdapter.java:465) ~[druid-1.1.10.jar!/:1.1.10]
        at com.alibaba.druid.filter.FilterChainImpl.preparedStatement_executeQuery(FilterChainImpl.java:3185) ~[druid-1.1.10.jar!/:1.1.10]
        at com.alibaba.druid.proxy.jdbc.PreparedStatementProxyImpl.executeQuery(PreparedStatementProxyImpl.java:181) ~[druid-1.1.10.jar!/:1.1.10]
        at com.alibaba.druid.pool.DruidPooledPreparedStatement.executeQuery(DruidPooledPreparedStatement.java:228) ~[druid-1.1.10.jar!/:1.1.10]
        at org.flywaydb.core.internal.jdbc.JdbcTemplate.queryForStringList(JdbcTemplate.java:116) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.internal.database.mysql.MySQLConnection.hasUserVariableResetCapability(MySQLConnection.java:84) ~[flyway-core-7.1.1.jar!/:na]
        at org.flywaydb.core.internal.database.mysql.MySQLConnection.<init>(MySQLConnection.java:54) ~[flyway-core-7.1.1.jar!/:na]
        ... 37 common frames omitted
