#### 关键的注解
    Configuration注解 作用于类文件 相当于一个spring配置的xml文件。
    Bean 注解 相当于xml配置的bean注解。
    ComponentScan 注解，配置扫描得java包目录
    PropertySource(value="classpath:xxxx.properties") 在类中对属性使用@value("${jdbc.driverName}")
#### SpingBoot 基础
* @SpringBootApplication 作用于SpingBoot入口类
* pom 依赖 的parrent
  ```
     <parent>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-parent</artifactId>
            <version>2.0.5.RELEASE</version>
            <relativePath/> <!-- lookup parent from repository -->
     </parent>
   ```
#### starter pom
* web pom starter
    ```
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    ```
#### 全局配置
    server.port 
    server.server-path
    [document][http://https://docs.spring.io/spring-boot/docs/current/reference/html/common-application-properties.html]
