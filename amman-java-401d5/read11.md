## Spring

Spring initializer is used to start the project **quickly.** It is provided by Pivotal Web Service. 

### Spring Boot Devtools
Spring Boot makes it easy to create stand-alone, production-grade Spring based Applications that you can "just run". This wouls save a lot of time. 

**Example**

`package com.example.servingwebcontent;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class ServingWebContentApplication {

    public static void main(String[] args) {
        SpringApplication.run(ServingWebContentApplication.class, args);
    }

}`

One more advantage is you can't find any xml line, it's **pure java.**

## Spring MVC and Thymeleaf

Thymeleaf is a template engine that executes makes all the variables available within the template.


### Spring MVC application contains:
@Controller classes - responsible for preparing a model map with data and selecting a view to be rendered
model map allows for the complete abstraction of the view technology, and in the case of Thymeleaf, it is transformed into a Thymeleaf context object that makes all the defined variables available to expressions executed in templates.

Spring model attributes:

model attributes - Spring MVC calls the pieces of data that can be accessed during the execution of views

context variables - Thymeleaf language version of model attributes

Request parameters

Request parameters - easily accessed in Thymeleaf views, and passed from the client to server

Session attributes

Session attributes - can be accessed by using the session. prefix or using #session

ServletContext attributes

ServletContext attributes - shared between requests and sessions, and to access ServletContext attributes in Thymeleaf you can use the 
#servletContext. prefix

Spring beans

Thymeleaf allows accessing beans registered at the Spring Application Context with the @beanName syntax

