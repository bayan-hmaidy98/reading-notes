# Notifications
### What is Amazon SNS?
Amazon Simple Notification Service 

Pub/sub messaging for microservices and serverless applications. Amazon SNS is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and event-driven serverless applications. Amazon SNS provides topics for high-throughput, push-based, many-to-many messaging.

### Features and capabilities
Amazon SNS provides the following features and capabilities:

* Reliably deliver messages with durability Amazon SNS uses cross availability zone message storage to provide high message durability. Amazon SNS reliably delivers messages to valid AWS endpoints, such as Amazon SQS queues and AWS Lambda functions.

* Simplify your architecture with Message Filtering Amazon SNS helps you simplify your pub/sub messaging architecture by offloading the message filtering logic from your subscriber systems, and message routing logic from your publisher systems.

* Automatically scale your workload Amazon SNS leverages the proven AWS cloud to dynamically scale with your application. Amazon SNS is a fully managed service, taking care of the heavy lifting related to capacity planning, provisioning, monitoring, and patching.

* Keep messages private and secure Amazon SNS topic owners can set topic policies that restrict who can publish and subscribe to a topic. Amazon SNS also ensures that data is encrypted in transit and at rest, and provides VPC endpoints for message privacy.

### Related services
You can use the following services with Amazon SNS:

* Amazon SQS offers a secure, durable, and available hosted queue that lets you integrate and decouple distributed software systems and components.

* AWS Lambda enables you to build applications that respond quickly to new information. Run your application code in Lambda functions on highly available compute infrastructure.

* AWS Identity and Access Management (IAM) helps you securely control access to AWS resources for your users. Use IAM to control who can use your Amazon SNS topics (authentication), what topics they can use, and how they can use them (authorization).

* AWS CloudFormation enables you to model and set up your AWS resources. Create a template that describes the AWS resources that you want, including Amazon SNS topics and subscriptions. AWS CloudFormation takes care of provisioning and configuring those resources for you.

### Accessing Amazon SNS
You can configure and manage SNS topics and subscriptions using the Amazon SNS console, command line tools, or AWS SDKs.