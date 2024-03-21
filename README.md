# simple-ecs-log

### EcsLayout Spring-Boot

    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-log4j2</artifactId>
    </dependency>

    <dependency>
      <groupId>org.apache.logging.log4j</groupId>
      <artifactId>log4j-layout-template-json</artifactId>
      <version>2.23.1</version>
    </dependency>


### EcsLayout Log4J

    Configuration:
       Appenders:
          Console:
             name: Console_Appender
             target: SYSTEM_OUT
             JsonTemplateLayout:
                eventTemplateUri: classpath:EcsLayout.json

       Loggers:
          Root:
             level: info
             AppenderRef:
             -  ref: Console_Appender    