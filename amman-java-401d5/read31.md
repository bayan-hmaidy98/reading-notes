# Espresso 

## What is Espresso? 

Espresso is a testing framework that helps developers write automation test cases for user interface (UI) testing. It runs fast comparing to other tests. This kind of tests are useful to developers. 

## Espresso calling

Espresso calls onView() method to test the wanted UI until one of the following came up: 
1. Queue message is **empty.**
2. There are no instances of AsyncTask currently executing a task.
3. All developer-defined idling resources are idle.

## Packages in Espresso

1. espresso-core
2. espresso-web
3. espresso-idling-resource
4. espresso-intents
5. espresso-contrib
6. espresso-remote

# Create UI tests with Espresso Test Recorder 

Espresso Test Recorder let you test the app and no test is written. They are used because of their consistance and reliablity. This is done by `stating expectations, interactions, and assertions without directly accessing the underlying app’s activities and views.` 

**NOTE:** it's very important to turn off the animations on the app before testing the device. 

## Record Espresso test 

iIf you want to test your app, you need to check 2 things: tap and type action in the app and exitance of the elements. They are called interactions and assertions respectively.

To add assertions, you need to cutomize the assertion type: text is to check text content of the **selsecte** element, exists to check if the **element exits**, and does not exist to check if the element **does not exist** in the on the screen. 



