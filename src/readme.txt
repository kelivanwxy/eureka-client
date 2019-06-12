一、勾选spring cloud discovery、选择Eureka Discovery Client
二、启动类添加注解@EnableDiscoveryClient 而不是 @EnableEurekaClient（服务端注解@EnableEurekaServer）
三、web模块加入，否则启动失败
四、自定义链接地址
    spring:
      application:
        name: eureka-client
    server:
      port: 8081
    eureka:
      client:
        service-url:
          defaultZone: http://localhost:8761/eureka
      instance:
        hostname: clientTest
