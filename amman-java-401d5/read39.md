## Amplify and Kinesis

Amazon Brand Analytics is a selection of reports available to approved members of the Amazon Brand Registry. Previously known as Amazon Retail Analytics, the feature allows brand owners to view valuable insights into customer behaviour, popular search terms, competitor success and advertising campaigns.

Amazon Kinesis makes it easy to collect, process, and analyze real-time, streaming data so you can get timely insights and react quickly to new information. Amazon Kinesis offers key capabilities to cost-effectively process streaming data at any scale, along with the flexibility to choose the tools that best suit the requirements of your application. With Amazon Kinesis, you can ingest real-time data such as video, audio, application logs, website clickstreams, and IoT telemetry data for machine learning, analytics, and other applications. Amazon Kinesis enables you to process and analyze data as it arrives and respond instantly instead of having to wait until all your data is collected before the processing can begin.

## Set up Analytics backend
1. To prompt the analytics catagory use the following command: 

``` 
amplify add analytics
```
2. Then after answering the questions, push the changes: `amplify push`

3. Add the dependencies in build.gradle (Module:app) 
``` 
dependencies {
    // Add these lines in `dependencies`
    implementation 'com.amplifyframework:aws-analytics-pinpoint:1.30.0'
    implementation 'com.amplifyframework:aws-auth-cognito:1.30.0'
}
```
and sync.
4. Initialize the analytics category by: 

``` Amplify.addPlugin(new AWSPinpointAnalyticsPlugin(this));
```

5. To recors event, create the AnalyticsEvent: 

``` 
AnalyticsEvent event = AnalyticsEvent.builder()
    .name("PasswordReset")
    .addProperty("Channel", "SMS")
    .addProperty("Successful", true)
    .addProperty("ProcessDuration", 792)
    .addProperty("UserAge", 120.3)
    .build();

Amplify.Analytics.recordEvent(event);
```
6. View the analytics console using the command: 
```
amplify console analytics
``` 