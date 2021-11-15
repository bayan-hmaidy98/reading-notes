# **Intents, Activities, and SharedPreferences**

## **Tasks and Back Stack**

A task is a collection of activities that users interact with when performing a certain job. The activities are arranged in a stack—the back stack)—in the order in which each activity is opened. For example, an email app might have one activity to show a list of new messages. When the user selects a message, a new activity opens to view that message. This new activity is added to the back stack. If the user presses the Back button, that new activity is finished and popped off the stack. 

The device Home screen is the starting place for most tasks. When the user touches an icon in the app launcher (or a shortcut on the Home screen), that app's task comes to the foreground. If no task exists for the app (the app has not been used recently), then a new task is created and the "main" activity for that app opens as the root activity in the stack.

When the current activity starts another, the new activity is pushed on the top of the stack and takes focus. The previous activity remains in the stack, but is stopped. When an activity stops, the system retains the current state of its user interface. When the user presses the **Back** button, the current activity is popped from the top of the stack (the activity is destroyed) and the previous activity resumes (the previous state of its UI is restored). Activities in the stack are never rearranged, only pushed and popped from the stack—pushed onto the stack when started by the current activity and popped off when the user leaves it using the **Back** button. As such, the back stack operates as a "last in, first out" object structure.

<img src="https://developer.android.com/images/fundamentals/diagram_backstack.png" width="600" hight="300"/>

If the user continues to press **Back**, then each activity in the stack is popped off to reveal the previous one, until the user returns to the Home screen (or to whichever activity was running when the task began). When all activities are removed from the stack, the task no longer exists.

A task is a cohesive unit that can move to the "background" when users begin a new task or go to the Home screen, via the Home button. While in the background, all the activities in the task are stopped, but the back stack for the task remains intact—the task has simply lost focus while another task takes place

>Note: Multiple tasks can be held in the background at once. However, if the user is running many background tasks at the same time, the system might begin destroying background activities in order to recover memory, causing the activity states to be lost.
### **Managing Tasks**

 you might decide that you want to interrupt the normal behavior. Perhaps you want an activity in your app to begin a new task when it is started (instead of being placed within the current task); or, when you start an activity, you want to bring forward an existing instance of it (instead of creating a new instance on top of the back stack); or, you want your back stack to be cleared of all activities except for the root activity when the user leaves the task.

 You can do these things and more, with attributes in the `<activity>` manifest element and with flags in the intent that you pass to `startActivity()`.

 In this regard, the principal `<activity>` ***attributes*** you can use are:

`taskAffinity`
`launchMode`
`allowTaskReparenting`
`clearTaskOnLaunch`
`alwaysRetainTaskState`
`finishOnTaskLaunch`

And the principal intent ***flags*** you can use are:

`FLAG_ACTIVITY_NEW_TASK`
`FLAG_ACTIVITY_CLEAR_TOP`
`FLAG_ACTIVITY_SINGLE_TOP`

### **Defining launch modes**

Launch modes allow you to define how a new instance of an activity is associated with the current task. You can define different launch modes in two ways:

1. Using the manifest file
When you declare an activity in your manifest file, you can specify how the activity should associate with tasks when it starts.

2. Using Intent flags
When you call `startActivity()`, you can include a flag in the Intent that declares how (or whether) the new activity should associate with the current task.

As such, if Activity A starts Activity B, Activity B can define in its manifest how it should associate with the current task (if at all) and Activity A can also request how Activity B should associate with current task. If *both* activities define how Activity B should associate with a task, t***hen Activity A's request (as defined in the intent) is honored over Activity B's request (as defined in its manifest).***

>Note: Some launch modes available for the manifest file are not available as flags for an intent and, likewise, some launch modes available as flags for an intent cannot be defined in the manifest.
* *Using the manifest file*

When declaring an activity in your manifest file, you can specify how the activity should associate with a task using the `<activity> `element's launchMode attribute.

The launchMode attribute specifies an instruction on how the activity should be launched into a task. There are `four` different launch modes you can assign to the launchMode attribute:

1. "standard" (the default mode)
2. "singleTop"
3. "singleTask"
4. "singleInstance"

<img src="https://developer.android.com/images/fundamentals/diagram_backstack_singletask_multiactivity.png" width="600" hight="300"/>

this figure is representation of how an activity with launch mode "singleTask" is added to the back stack. If the activity is already a part of a background task with its own back stack, then the entire back stack also comes forward, on top of the current task.

>Note: The behaviors that you specify for your activity with the launchMode attribute can be overridden by flags included with the intent that start your activity, as discussed in the next section.
* ***Using Intent flags***

When starting an activity, you can modify the default association of an activity to its task by including flags in the intent that you deliver to `startActivity()`. The flags you can use to modify the default behavior are:

* `FLAG_ACTIVITY_NEW_TASK`

Start the activity in a new task. If a task is already running for the activity you are now starting, that task is brought to the foreground with its last state restored and the activity receives the new intent in onNewIntent().
This produces the same behavior as the "singleTask" launchMode value, discussed in the previous section.

* `FLAG_ACTIVITY_SINGLE_TOP`

If the activity being started is the current activity (at the top of the back stack), then the existing instance receives a call to onNewIntent(), instead of creating a new instance of the activity.
This produces the same behavior as the "singleTop" launchMode value, discussed in the previous section.

* `FLAG_ACTIVITY_CLEAR_TOP`

If the activity being started is already running in the current task, then instead of launching a new instance of that activity, all of the other activities on top of it are destroyed and this intent is delivered to the resumed instance of the activity (now on top), through onNewIntent()).
There is no value for the launchMode attribute that produces this behavior.

`FLAG_ACTIVITY_CLEAR_TOP` is most often used in conjunction with `FLAG_ACTIVITY_NEW_TASK`. When used together, these flags are a way of locating an existing activity in another task and putting it in a position where it can respond to the intent.

### **Starting a task**

You can set up an activity as the entry point for a task by giving it an intent filter with "android.intent.action.MAIN" as the specified action and "android.intent.category.LAUNCHER" as the specified category. For example:

```
<activity ... >
    <intent-filter ... >
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.LAUNCHER" />
    </intent-filter>
    ...
</activity>
```

<hr>

## **Save key-value data**


If you have a relatively small collection of key-values that you'd like to save, you should use the `SharedPreferences` APIs. A `SharedPreferences` object points to a file containing key-value pairs and provides simple methods to read and write them. Each `SharedPreferences` file is managed by the framework and can be private or shared.

### **Get a handle to shared preferences**

You can create a new shared preference file or access an existing one by calling one of these methods:

`getSharedPreferences()` — Use this if you need multiple shared preference files identified by name, which you specify with the first parameter. You can call this from any Context in your app.

`getPreferences()` — Use this from an Activity if you need to use only one shared preference file for the activity. Because this retrieves a default shared preference file that belongs to the activity, you don't need to supply a name.

For example, the following code accesses the shared preferences file that's identified by the resource string R.string.preference_file_key and opens it using the private mode so the file is accessible by only your app:

```
Context context = getActivity();
SharedPreferences sharedPref = context.getSharedPreferences(
        getString(R.string.preference_file_key), Context.MODE_PRIVATE);
```

When naming your shared preference files, you should use a name that's uniquely identifiable to your app. An easy way to do this is prefix the file name with your application ID. For example: "com.example.myapp.PREFERENCE_FILE_KEY"

* Alternatively, if you need just one shared preference file for your activity, you can use the `getPreferences()` method:

```
SharedPreferences sharedPref = getActivity().getPreferences(Context.MODE_PRIVATE);
```

If you're using the `SharedPreferences` API to save app settings, you should instead use `getDefaultSharedPreferences()` to get the default shared preference file for your entire app. 


### **Write to shared preferences**

To write to a shared preferences file, create a `SharedPreferences.Editor` by calling `edit()` on your `SharedPreferences`.

Pass the keys and values you want to write with methods such as `putInt()` and `putString()`. Then call `apply()` or `commit()` to save the changes. For example:

```
SharedPreferences sharedPref = getActivity().getPreferences(Context.MODE_PRIVATE);
SharedPreferences.Editor editor = sharedPref.edit();
editor.putInt(getString(R.string.saved_high_score_key), newHighScore);
editor.apply();
```

`apply()` changes the in-memory `SharedPreferences` object immediately but writes the updates to disk asynchronously. Alternatively, you can use `commit()` to write the data to disk synchronously. But because `commit()` is synchronous, you should avoid calling it from your main thread because it could pause your UI rendering.


### **Read from shared preferences**

To retrieve values from a shared preferences file, call methods such as `getInt()` and `getString()`, providing the key for the value you want, and optionally a default value to return if the key isn't present. For example:

```
SharedPreferences sharedPref = getActivity().getPreferences(Context.MODE_PRIVATE);
int defaultValue = getResources().getInteger(R.integer.saved_high_score_default_key);
int highScore = sharedPref.getInt(getString(R.string.saved_high_score_key), defaultValue);
```