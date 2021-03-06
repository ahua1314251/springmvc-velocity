# springmvc-velocity  解决高版本springboot不兼容
配合新版本springboot使用 解决高版本springmvc不支持velocity模板语言问题
最高支持 springboot 2.5.5 及以上版本

use with springboot 2.5.5 and above，solve high version springmvc cant support velocity template render.


使用示例
sample
pom.xml 添加

``` xml
    <repositories>
        <repository>
            <id>github</id>
            <url>https://raw.githubusercontent.com/ahua1314251/maven/master/repo/</url>
        </repository>
    </repositories>
    
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.5.5</version>
    </parent>
    <dependencies>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>ch.qos.logback</groupId>
            <artifactId>logback-core</artifactId>
        </dependency>

        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-test</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
        </dependency>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
            <exclusions>
                <exclusion>
                    <groupId>org.springframework.boot</groupId>
                    <artifactId>spring-boot-starter-tomcat</artifactId>
                </exclusion>
            </exclusions>
        </dependency>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-tomcat</artifactId>
<!--            <scope>provided</scope>-->
        </dependency>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-velocity</artifactId>
            <version>1.4.7.RELEASE</version>
        </dependency>
        
        <dependency>
            <groupId>org.winker</groupId>
            <artifactId>springmvc-velocity</artifactId>
            <version>2.5.5</version>
        </dependency>


        <!-- aop -->
        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-aop</artifactId>
        </dependency>

        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-aspects</artifactId>
            <!-- 	<version>4.2.2.RELEASE</version> -->
        </dependency>

   
        <!-- jackson -->
        <dependency>
            <groupId>com.fasterxml.jackson.core</groupId>
            <artifactId>jackson-annotations</artifactId>
        </dependency>
        <dependency>
            <groupId>com.fasterxml.jackson.core</groupId>
            <artifactId>jackson-core</artifactId>
        </dependency>
        <dependency>
            <groupId>com.fasterxml.jackson.core</groupId>
            <artifactId>jackson-databind</artifactId>
        </dependency>
        
    </dependencies>
```



重点引入  其他根据自己需要调整

important dependency , other jar help yourself

``` xml
        <repositories>
            <repository>
                <id>github</id>
                <url>https://raw.githubusercontent.com/ahua1314251/maven/master/repo/</url>
            </repository>
        </repositories>

        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-velocity</artifactId>
            <version>1.4.7.RELEASE</version>
        </dependency>
        
        <dependency>
            <groupId>org.winker</groupId>
            <artifactId>springmvc-velocity</artifactId>
            <version>2.5.5</version>
        </dependency>
```

  不使用maven 也可直接下载 jar包
  
  if you do not use maven,you can download jar directly. jar link

  https://github.com/ahua1314251/maven/blob/master/repo/org/winker/springmvc-velocity2.5.5.jar
