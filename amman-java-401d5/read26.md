# Android fundamentals

## The difference between Andriod package and Android bundle. 

Android Package: .apk, required contents at runtime, android-powered devices use to install the app. 
Android App Bundle: .aab, it's not installable on the Android devices, it has some additional metadata that id not required at runtime. 

## Security of Andriod app
1. Each app in the google store is a **diiferent** user, since Andriod operating system is a nulti-user linux system. 
2. Each app is assigned to to **unique** linux user ID, this ID is not known to the app. 
3. Each app runs in isolation from other apps.
4. Since the app runs in it's own linux process, starting point is when app components exected and shut sown in 2 cases: when there is no need for the linux process or when the system must recover memory for other apps. 

Andriod apps provide secure environment by letting the app access parts of the system that has persmission. It uses the **principle of least privilege.** Sometimes, two apps share the same ID so they are able to access each other's files.

## App components

1. Activities: each entry point that interacts with user is called activity. 
Even when many activities works togother in the app, they are **dependent** and defined dependently. It tracks the screen to **ensure** that the system running the process live on screen. This tracking is useful when prioritize the the activities depending on the activity of the user. 

2. Service: I'll quote the definition as it is, ` service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. It is a component that runs in the background to perform long-running operations or to perform work for remote processes. ` It's not like the activity, in other words it does not run user interface. It'm more likely running music in the background, though the user is using other app or not using the device at all. Let's indroduce the types of the services: 
1. Started services: the system keeps running the app **until** their process is done, regardless if the user is using the app or not. Some of the services the user needed to be aware of, like playing music in the background, so if the service is needed to keep running by the system. Other services are not required to run all the time so it's possible for them to be killed and restart the service when needed. 
2. Bounded services: this kind of services is active when an app wanted to use the service of other app. In this case, dependency between the apps is a **must**. 

3. Broadcast receivers: They are defined to be another entry-point to the app. If the app is not running, the broadcast can be delivered to the user regradless their flow and it doesn't require to run the app while sending these broadcasts. Note that they don't use UI but van appear as a notification in the status bar. They are not holding that much of functionality, this can be realted to the main idea that the don't require the running of the app. 

4. Content providers: it relates to the set of data stored in the file system. This data can be manipulated by other apps if they have permissions. To make it easier for you, think of the content provider as an abstraction of the database. No need to the app to keep running when assigning the URI, but there's a need when retreiving the app's data. You can lock up the content provider to ensure that other apps are not able to access it. 

**NOTE**: Android apps don;thave only one entry point, because they are capable to run other components with thier classes in other apps. 

## Activating contents

To activate activities, services, and broadcast receivers, intents are used. Intentsbind or link components together at running time. Intents request **components** without considering if they are in the app or in other app. 
Intents function differnetly depending on the components type, for ezample, they would define an action to perform fot activities and servers. On other hand, they would define the announcement for the broadcast receivers not the the action it self. For content providers, things works differently, they are activated by ContentResolver. 

## The manifest file

Andriod system can't **start** any app componentwithout checking whether the component exists or not. This is dine using manifest file which hold the component of the app. Manifest file also defines the user permissions, the minimum API leveland API libraries the app needs, hardware and software features used or required by the app. 

## Declaring components 

In the following code, we can see: 
```
<?xml version="1.0" encoding="utf-8"?>
<manifest ... >
    <application android:icon="@drawable/app_icon.png" ... >
        <activity android:name="com.example.project.ExampleActivity"
                  android:label="@string/example_label" ... >
        </activity>
        ...
    </application>
</manifest>
``` 

`<application>` element has `andriod:icon` attribute points to resources of the icon that define the app. 
![](https://cms-assets.tutsplus.com/uploads/users/1865/posts/30624/preview_image/android-preview@2x.jpg)

In `<activity>` element, `android:name` refers the class name of the activity. Broadcast receivers are not neccesary declared in the manifest file, they can be created dynamically as a BroadcastReceiver. Other cpmpnenets will not run unless they are declared in the manifest file. 


## Declaring component capabilities

To start an activity, we use the intent, explict intent or implicit intent. Implicit intent allows the user to choose the component to perform the action in the intent. That is done using `<intent-filter>` 

## Declaring app requirements

Since there are a lot of and different devices use Android, that means they don't allshre the same capabilities. To avoid installing an app that its properties,  it's important to define a profile for the types of devices the app supports by declaring device and software requirements in manifest file. They are niot excuted, they are onlu informative declarations. 