# Tasks and the back stack 

A task is a collection of activities that users interact with when trying to do something in your app. These activities are arranged in a stack—the back stack—in the order in which each activity is opened. For example, an email app might have one activity to show a list of new messages. When the user selects a message, a new activity opens to view that message. This new activity is added to the back stack. Then, if the user presses or gestures Back, that new activity is finished and popped off the stack.

## Background and foreground tasks

Figure 2. Two tasks: Task B receives user interaction in the foreground, while Task A is in the background, waiting to be resumed.
A task is a cohesive unit that can move to the background when a user begins a new task or goes to the Home screen. While in the background, all the activities in the task are stopped, but the back stack for the task remains intact—the task has simply lost focus while another task takes place, as shown in figure 2. A task can then return to the foreground so users can pick up where they left off.

![img](https://developer.android.com/images/fundamentals/diagram_multitasking.png)


## Defining launch modes
Launch modes allow you to define how a new instance of an activity is associated with the current task. You can define different launch modes in two ways:

* Using the manifest file

When you declare an activity in your manifest file, you can specify how the activity should associate with tasks when it starts.

* Using Intent flags

When you call startActivity(), you can include a flag in the Intent that declares how (or whether) the new activity should associate with the current task.

**Using the manifest file, we can specify how the activity should associate with a task using the element’s launchMode attribute in manifest file. launch modes have four different mode can assign to the launchMode attribute:**

1. standard
2. singleTop
3. singleTask
4. singleInstance

## Save key-value data
* SharedPreferences APIs: is a object points to a file containing key-value pairs and provides simple methods to read and write them.
SharedPreferences APIs managed by the framework and can be private or shared.
we can create a new shared preference file or access an existing one by calling one of these methods:
* getSharedPreferences()
* getPreferences()
*how to Write to shared preferences*
* create a SharedPreferences.Editor by calling edit() on your SharedPreferences.
* Pass the keys and values you want to write with methods such as putInt() and putString().
* call apply() or commit() to save the changes.
*how to Read from shared preferences*
* call methods such as getInt() and getString()
* providing the key for the value you want
* optionally a default value to return if the key isn’t present .