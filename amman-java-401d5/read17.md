## Spring Boot and OAuth2

The OAuth 2.0 authorization framework is a protocol that allows a user to grant a third-party web site or application access to the user's protected resources, without necessarily revealing their long-term credentials or even their identity.

### Single Sign On With GitHub

To do do, you need to follow the steps: 

1. Create a new project. Using the commands below:

` $ mkdir ui && cd ui
$ curl https://start.spring.io/starter.tgz -d style=web -d name=simple | tar -xzvf - `

2. Add home page. Adding some stylesheets to it is not nessecary it relates only to neat UI. 
3. secure the account by adding the following dependencies: 

` <dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-oauth2-client</artifactId>
</dependency> `

Next steps, you need to add new GitHup app, cinfigure application .yml, and boot up the application. 

### Adding an error page for unauthenticated users

1. Switching to GitHup because ` two- preoviders sample uses GitHup as an Auth 2.0 provider.`

2. Detecting an authentication failure in the client by adding this div to index.html: 

` <div class="container text-danger error"></div> `

3. Adding an error message:
4. Generating a 401 in the server. 