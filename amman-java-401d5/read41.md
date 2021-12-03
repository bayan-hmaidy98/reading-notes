## Intent Filters

Any app that want to use an action in other app should **support** the `ACTION_SEND` intent. As aresult, app will appear when ever the user presses on share action as an option of many. Note that you need to add an `<intent-filter>` element in your manifest file for the corresponding `<activity>` element. In other words, intent filter tells android which activities can handle which actions. 

When the user installs the app, the intent filters are added to an internal catalog of intents supported by installed apps. This way, when you start the app using implicit intent, the system will find the activity that is able to respond to the intent.

### Adding intent filter

 When you add an intent filter to the activity, you should definr it accurately. Intent object has the following: 

Action: tells android the activity can handle `ACTION_SEND`
Data: The tyoes of data the activity can handle. 
Category: supplies extra information about  the activity, such as how would we start the activity. See the example bellow: 

```
<activity android:name="ShareActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
    </intent-filter>
</activity>
``` 

Note that `Each incoming intent specifies only one action and one data type, but it's OK to declare multiple instances of the <action>, <category>, and <data> elements in each <intent-filter>.` I quote it as it is because it's clear and simple. 

When your activity has two pairs of actions and data, they must be separated in 2 intent filters. 

### Handle the Intent in Your Activity

Intent helps ypu to define which action to choose. Call `getIntent()` to retrieve the intent in the activity, when the axctivity starts. This is done in `onCreate()` or `onStart()` callbacks.

### Return a result

This step is pretty simple to do, just call `setResult()` to specify the result code then to return the result call `finish()` to close the activity. The sesult must be specified like the following example: 

```
Intent result = new Intent("com.example.RESULT_ACTION", Uri.parse("content://result_uri"));
setResult(Activity.RESULT_OK, result);
finish();
```




