# Serverless and Amplify
## Intro to Serverless
## What is Serverless?
>Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers.
>A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider.
>Pricing is based on the number of executions rather than pre-purchased compute capacity, isn’t it the ideal framework for that project you have been planning since a long time? Well, go ahead do it.
### Traditional vs. Serverless Architecture:
* Traditional: applications have run on servers which you had to patch, update, and continuously look after late nights and early mornings due to all the unimaginable errors that broke your production.

* Serveless: users are no longer need to worry about the underlying servers.beacuse they are not managed by users anymore and with management out of the picture the responsibility falls on the Cloud vendors.

![img](https://cdn.hackernoon.com/hn-images/1*x_v5NRC3TTMt1MaYl1gMUg.jpeg)

### AWS Amplify
AWS Amplify is a set of tools and services that can be used together or on their own, to help front-end web and mobile developers build scalable full stack applications, powered by AWS. With Amplify, you can configure app backends and connect your app in minutes, deploy static web apps in a few clicks, and easily manage app content outside the AWS console.

*Benefits:*
1. Configure backends fast.

2. Seamlessly connect frontends.

3. Deploy in a few clicks.

4. Easily manage content.

### The GraphQL
The GraphQL Transform provides a simple to use abstraction that helps you quickly create backends for your web and mobile applications on AWS. With the GraphQL Transform, you define your application's data model using the GraphQL Schema Definition Language (SDL) and the library handles converting your SDL definition into a set of fully descriptive AWS CloudFormation templates that implement your data mode.
*Create a GraphQL API*
>Navigate into the root of a JavaScript, iOS, or Android project and run amplify init.

* *Test the API*
Once the API is finished deploying, go to the AWS AppSync console or run amplify mock api to try some of these queries in your new API's query page.

* *Update schema*

If you want to update your API, open your project's backend/api/apiname/schema.graphql file (NOT the one in the backend/api/apiname/build folder) and edit it in your favorite code editor. You can compile the backend/api/apiname/schema.graphql by running **amplify api gql-compile** .

* *API Category Project Structure*

At a high level, the transform libraries take a schema defined in the GraphQL Schema Definition Language (SDL) and converts it into a set of AWS CloudFormation templates and other assets that are deployed as part of amplify push. The full set of assets uploaded can be found at amplify/backend/api/YOUR-API-NAME/build.