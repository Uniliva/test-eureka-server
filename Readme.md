01 - Spring Cloud Netflix Eureka

### o que é 


https://coderef.com.br/arquitetura-de-microservices-com-spring-cloud-e-spring-boot-parte-3-b84b3dce13a0




#### Para criar um Eureka server

1. **Baixe um projeto do https://start.spring.io/**

![7c2e67220c38e7341a37f298d7d578c2.png](_resources/95e9505aa06a494b82853a0fd72e2040.png)

ou adicione no pom 

```xml
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>
</dependency>
 
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-parent</artifactId>
            <version>Greenwich.RELEASE</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

2.  importe com o eclipse
3. Adicione a anotação na classe de aplicação

```java
@EnableEurekaServer
@SpringBootApplication
public class EurekaServerApplication {
    public static void main(String[] args) {
        SpringApplication.run(EurekaServerApplication.class, args);
    }
}
```

![04beabc9b2be4f02cc935899905c2a53.png](_resources/35ba928e474d4d99b81132cd76a3d067.png)


4. add as propriedades no arquivo `application.properties`

```
server.port=8761
eureka.client.registerWithEureka=false
eureka.client.fetchRegistry=false
```

![1ba447799546725a632f11f61976f498.png](_resources/22c1842579464dfd912763589bc34809.png)

