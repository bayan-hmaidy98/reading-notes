# GraphQL @connection
### what is Serverless?
Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers. A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider.
### AWS Amplify
It is a set of tools and services that can be used together or on their own, to help front-end web and mobile developers build scalable full stack applications

With Amplify, user can configure app backends and connect app in minutes, deploy static web apps in a few clicks, and easily manage app content outside the AWS console.

### Add relationships between types:
### @connection
* The @connection directive enables you to specify relationships between @model types. Currently, this supports one-to-one, one-to-many, and many-to-one relationships.

* You may implement many-to-many relationships using two one-to-many connections and a joining @model type.

### Usage
Relationships between types are specified by annotating fields on an @model object type with the @connection directive.

The fields argument can be provided and indicates which fields can be queried by to get connected objects. The keyName argument can optionally be used to specify the name of secondary index (an index that was set up using @key) that should be queried from the other type in the relationship.

When specifying a keyName, the fields argument should be provided to indicate which field(s) will be used to get connected objects. If keyName is not provided, then @connection queries the target table’s primary index.

### Relations:
* Has one

* Has many

Note how a one-to-many connection needs an @key that allows comments to be queried by the postID and the connection uses this key to get all comments whose postID is the id of the post was called on.

* Belongs to

* Many-to-many connections

You can implement many to many using two 1-M @connections, an @key, and a joining @model. For example:

### Limit
>The default number of nested objects is 100. You can override this behavior by setting the limit argument.
### Generates
>In order to keep connection queries fast and efficient, the GraphQL transform manages global secondary indexes (GSIs) on the generated tables on your behalf when using @connection