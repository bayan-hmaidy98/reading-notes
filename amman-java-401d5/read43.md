# Kinesis & Analytics

* The Analytics category enables you to collect analytics data for your App. The Analytics category comes with built-in support for Amazon Pinpoint and Amazon Kinesis (Kinesis support is currently only available in the Amplify JavaScript library).

## Goal
* To setup and configure your application with Amplify Analytics and record an analytics event.

## Prerequisites
* Install and configure Amplify CLI
* An Android application targeting Android API level 16 (Android 4.1) or above

## Set up Analytics backend
* The CLI will prompt configuration options for the Analytics category such as Amazon Pinpoint resource name and analytics event settings.

* The Analytics category utilizes the Authentication category behind the scenes to authorize your app to send analytics events.

```
amplify add analytics
```
```
? Select an Analytics provider (Use arrow keys)
    `Amazon Pinpoint`
? Provide your pinpoint resource name:
    `yourPinpointResourceName`
? Apps need authorization to send analytics events. Do you want to allow guests and unauthenticated users to send analytics events? (we recommend you allow this when getting started)
    `Yes`
```
* To deploy your backend, run:
>amplify push
## Install Amplify Libraries

Add Analytics by adding these libraries into the dependencies block:
```
dependencies {
    // Add these lines in `dependencies`
    implementation 'com.amplifyframework:aws-analytics-pinpoint:1.24.0'
    implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
}
```
## Initialize Amplify Analytics
* To initialize the Amplify Auth and Analytics categories you call 1. Amplify.addPlugin() method for each category. To complete initialization call 2. Amplify.configure().
## Record events
* To record an event, create an AnalyticsEvent and call Amplify.Analytics.recordEvent()
## amplify console analytics
>amplify console analytics