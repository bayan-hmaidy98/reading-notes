# Using WebSocket to build an interactive web application

What is WebSocket and how it works?
A WebSocket is a persistent connection between a client and server. WebSockets provide a bidirectional, full-duplex communications channel that operates over HTTP through a single TCP/IP socket connection. At its core, the WebSocket protocol facilitates message passing between a client and server.

Spring Initializr
Gradle:
```
dependencies {
implementation 'org.webjars:webjars-locator-core'
implementation 'org.webjars:sockjs-client:1.0.2'
implementation 'org.webjars:stomp-websocket:2.3.3'
implementation 'org.webjars:bootstrap:3.3.7'
implementation 'org.webjars:jquery:3.1.1-1'
}
```
### Create a Resource Representation Class
Now that you have set up the project and build system, you can create your STOMP message service.

Begin the process by thinking about service interactions.

1. The service will accept messages that contain a name in a STOMP message whose body is a JSON object.
2. To model the message create a plain old Java object with a name of property and a corresponding getName().

3. Upon receiving the message and extracting the name, the service will process it by creating a greeting and publishing that greeting on a separate queue to which the client is subscribed. The greeting will also be a JSON object.

4. o model the greeting representation, add another plain old Java object with a content property and a corresponding getContent() method.

### Create a Message-handling Controller

STOMP messages can be routed to @Controller classes.

```
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
### Configure Spring for STOMP messaging

```
@Configuration
@EnableWebSocketMessageBroker
public class WebSocketConfig implements WebSocketMessageBrokerConfigurer {
  @Override
  public void configureMessageBroker(MessageBrokerRegistry config) {
    config.enableSimpleBroker("/topic");
    config.setApplicationDestinationPrefixes("/app");
  }
  @Override
  public void registerStompEndpoints(StompEndpointRegistry registry) {
    registry.addEndpoint("/gs-guide-websocket").withSockJS();
  }
}
```
### Create a Browser Client

With the server-side pieces in place, you can turn your attention to the JavaScript client that will send messages to and receive messages from the server side.

Create an index.html file ,This HTML file imports the SockJS and STOMP javascript libraries that will be used to communicate with our server through STOMP over websocket. We also import app.js, which contains the logic of our client application. 