# spring-cloud-eureka-server-kotlin


### gradle 추가
```
    // https://mvnrepository.com/artifact/org.springframework.cloud/spring-cloud-starter-netflix-eureka-server
    implementation("org.springframework.cloud:spring-cloud-starter-netflix-eureka-server:3.1.0")
    // https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-actuator
    implementation("org.springframework.boot:spring-boot-actuator:2.6.1")
```

### yml
```
spring:
    application:
        name: Eureka Server
server:
    port: 9999
eureka:
  client: 
    serviceUrl:
      defaultZone: http://localhost:9999/eureka/
    register-with-eureka: false
    fetch-registry: false
  server:
    ## Self-Preservation 모드를 켜고 끌 수 있는 설정이다. 가급적이면 운영 상황에서는 끄지 않는 것을 권장한다.
    enable-self-preservation: true

```

### 메인메서드
```
@EnableEurekaServer 
```
