# Using WebSocket to build an interactive web application
## How to complete this guide
1. To start from scratch, move on to Starting with Spring Initializr.
2. If you use Gradle, visit the Spring Initializr (https://start.spring.io/)to generate a new project with the required dependency (Websocket).
3. build.gradle file:
```plugins {
	id 'org.springframework.boot' version '2.5.2'
	id 'io.spring.dependency-management' version '1.0.11.RELEASE'
	id 'java'
}

group = 'com.example'
version = '0.0.1-SNAPSHOT'
sourceCompatibility = '1.8'

repositories {
	mavenCentral()
}

dependencies {
	implementation 'org.springframework.boot:spring-boot-starter-websocket'
	testImplementation 'org.springframework.boot:spring-boot-starter-test'
}

test {
	useJUnitPlatform()
}
```
## Adding Dependencies
* If you use Gradle, you need to add the following dependencies:
implementation 'org.webjars:webjars-locator-core'
implementation 'org.webjars:sockjs-client:1.0.2'
implementation 'org.webjars:stomp-websocket:2.3.3'
implementation 'org.webjars:bootstrap:3.3.7'
implementation 'org.webjars:jquery:3.1.1-1'

## Create a Resource Representation Class
* Spring will use the Jackson JSON library to automatically marshal instances of type Greeting into JSON.
* you will create a controller to receive the hello message and send a greeting message.
## Create a Message-handling Controller
* STOMP messages can be routed to @Controller classes.
*  For example, the GreetingController (from src/main/java/com/example/messagingstompwebsocket/GreetingController.java)
```package com.example.messagingstompwebsocket;

import org.springframework.messaging.handler.annotation.MessageMapping;
import org.springframework.messaging.handler.annotation.SendTo;
import org.springframework.stereotype.Controller;
import org.springframework.web.util.HtmlUtils;

@Controller
public class GreetingController {


  @MessageMapping("/hello")
  @SendTo("/topic/greetings")
  public Greeting greeting(HelloMessage message) throws Exception {
    Thread.sleep(1000); // simulated delay
    return new Greeting("Hello, " + HtmlUtils.htmlEscape(message.getName()) + "!");
  }

}
```
* The @MessageMapping annotation ensures that, if a message is sent to the /hello destination, the greeting() method is called.
* as specified in the @SendTo annotation. Note that the name from the input message is sanitized, since, in this case, it will be echoed back and re-rendered in the browser DOM on the client side.
## Configure Spring for STOMP messaging
* Create a Java class named WebSocketConfig that resembles the following listing 
* WebSocketConfig is annotated with @Configuration to indicate that it is a Spring configuration class
* it is also annotated with @EnableWebSocketMessageBroker enables WebSocket message handling, backed by a message broker.
## Create a Browser Client
* Create an index.html file similar to the following listing (from src/main/resources/static/index.html)
## Make the Application Executable
* @SpringBootApplication is a convenience annotation that adds all of the following:
. @Configuration
. @EnableAutoConfiguration
. @ComponentScan

## Test the service
* Now that the service is running, point your browser at http://localhost:8080 and click the Connect button.




























