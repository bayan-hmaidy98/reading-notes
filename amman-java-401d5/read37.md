# S3
### What is Amazon S3?
* Amazon S3:It is storage for the Internet. It is designed to make web-scale computing easier.
* Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web.
### Advantages of using Amazon S3
* Creating buckets

* Storing data

* Downloading data

* Permissions

* Standard interfaces

### Amazon S3 concepts
* Buckets: is a container for objects stored in Amazon S3. Every object is contained in a bucket.

* Objects:Objects are the fundamental entities stored in Amazon S3. Objects consist of object data and metadata.

* Keys:A key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key.

* Regions:You can choose the geographical AWS Region where Amazon S3 will store the buckets that you create.

### Amazon S3 application programming interfaces (API)
The Amazon S3 architecture is designed to be programming language-neutral, using AWS Supported interfaces to store and retrieve objects.

### The REST interface
The REST API is an HTTP interface to Amazon S3. Using REST, you use standard HTTP requests to create, fetch, and delete buckets and objects.

### Paying for Amazon S3
Pricing for Amazon S3 is designed so that you don't have to plan for the storage requirements of your application

### Provision backend storage
* To start provisioning storage resources in the backend, go to your project directory and execute the command:
**amplify add storage**

* Enter the following when prompted:
```
? Please select from one of the below mentioned services:
    `Content (Images, audio, video, etc.)`
? You need to add auth (Amazon Cognito) to your project in order to add storage for user files. Do you want to add auth now?
    `Yes`
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`
? Please provide a friendly name for your resource that will be used to label this category in the project:
    `S3friendlyName`
? Please provide bucket name:
    `storagebucketname`
? Who should have access:
    `Auth and guest users`
? What kind of access do you want for Authenticated users?
    `create/update, read, delete`
? What kind of access do you want for Guest users?
    `create/update, read, delete`
? Do you want to add a Lambda Trigger for your S3 Bucket?
    `No`
    ```
* To push your changes to the cloud, execute the command:
amplify push

### Install Amplify Libraries
* Expand Gradle Scripts, open build.gradle (Module: app).

* Add these libraries into the dependencies block:

```
dependencies {
    implementation 'com.amplifyframework:aws-storage-s3:1.17.4'
    implementation 'com.amplifyframework:aws-auth-cognito:1.17.4'
}
```

### Initialize Amplify Storage
* To initialize the Amplify Auth and Storage categories you call Amplify.addPlugin() method for each category. To complete initialization call Amplify.configure().

* Add the following code to your onCreate() method in your application class:

```
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.addPlugin(new AWSS3StoragePlugin());
```

### Uploading data to your bucket
* To upload to S3 from a data object, specify the key and the data object to be uploaded.

```
private void uploadFile() {
    File exampleFile = new File(getApplicationContext().getFilesDir(), "ExampleKey");
    try {
        BufferedWriter writer = new BufferedWriter(new FileWriter(exampleFile));
        writer.append("Example file contents");
        writer.close();
    } catch (Exception exception) {
        Log.e("MyAmplifyApp", "Upload failed", exception);
    }
    Amplify.Storage.uploadFile(
            "ExampleKey",
            exampleFile,
            result -> Log.i("MyAmplifyApp", "Successfully uploaded: " + result.getKey()),
            storageFailure -> Log.e("MyAmplifyApp", "Upload failed", storageFailure)
    );
}