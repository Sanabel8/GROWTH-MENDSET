## Android Tasks and the Back Stack
### Understand Tasks and Back Stack 
* A task : is a collection of activities that users interact with when performing a certain job.
* The activities are arranged in a stack—the back stack)—in the order in which each activity is opened. 
* an email app might have one activity to show a list of new messages. 
* When apps are running simultaneously in a multi-windowed environment, supported in Android 7.0 (API level 24) and higher, the system manages tasks separately for each window;
* each window may have multiple tasks.
* The device Home screen is the starting place for most tasks
* When the current activity starts another, the new activity is pushed on the top of the stack and takes focus.
*  The previous activity remains in the stack, but is stopped. 
* A task is a cohesive unit that can move to the "background" when users begin a new task or go to the Home screen, via the Home button.
* To summarize the default behavior for activities and tasks:
1. When Activity A starts Activity B, Activity A is stopped, but the system retains its state (such as scroll position and text entered into forms). If the user presses the Back button while in Activity B, Activity A resumes with its state restored.
2. When the user leaves a task by pressing the Home button, the current activity is stopped and its task goes into the background. The system retains the state of every activity in the task. If the user later resumes the task by selecting the launcher icon that began the task, the task comes to the foreground and resumes the activity at the top of the stack.
3. If the user presses the Back button, the current activity is popped from the stack and destroyed. The previous activity in the stack is resumed. When an activity is destroyed, the system does not retain the activity's state.
4. Activities can be instantiated multiple times, even from other tasks.

* In this regard, the principal <activity> attributes you can use are:

taskAffinity
launchMode
allowTaskReparenting
clearTaskOnLaunch
alwaysRetainTaskState
finishOnTaskLaunch

* And the principal intent flags you can use are:

FLAG_ACTIVITY_NEW_TASK
FLAG_ACTIVITY_CLEAR_TOP
FLAG_ACTIVITY_SINGLE_TOP

## Defining launch modes
* Launch modes allow you to define how a new instance of an activity is associated with the current task. You can define different launch modes in two ways:
1. Using the manifest file
When you declare an activity in your manifest file, you can specify how the activity should associate with tasks when it starts.

2.Using Intent flags
When you call startActivity(), you can include a flag in the Intent that declares how (or whether) the new activity should associate with the current task.

## Using the manifest file
* When declaring an activity in your manifest file, you can specify how the activity should associate with a task using the <activity> element's launchMode attribute.
* The launchMode attribute specifies an instruction on how the activity should be launched into a task.
* There are four different launch modes you can assign to the launchMode attribute:
1. "standard" (the default mode)
2. "singleTop"
3. "singleTask"
4. "singleInstance"

## Using Intent flags
* The flags you can use to modify the default behavior are:
1. FLAG_ACTIVITY_NEW_TASK
2. FLAG_ACTIVITY_SINGLE_TOP
3. FLAG_ACTIVITY_CLEAR_TOP

## Clearing the back stack
* There are some activity attributes that you can use to modify this behavior:
1. alwaysRetainTaskState
2. clearTaskOnLaunch
3. finishOnTaskLaunch

## Starting a task
```<activity ... >
    <intent-filter ... >
        <action android:name="android.intent.action.MAIN" />
        <category android:name="android.intent.category.LAUNCHER" />
    </intent-filter>
    ...
</activity>
```

## Android SharedPreferences
### Save key-value data 
*  A SharedPreferences object points to a file containing key-value pairs and provides simple methods to read and write them. Each SharedPreferences file is managed by the framework and can be private or shared.
* If you have a relatively small collection of key-values that you'd like to save, you should use the SharedPreferences APIs

## Get a handle to shared preferences
* You can create a new shared preference file or access an existing one by calling one of these methods:
1. getSharedPreferences() 
2. getPreferences()

*  the following code accesses the shared preferences file that's identified by the resource string R.string.preference_file_key and opens it using the private mode so the file is accessible by only your app:
```Context context = getActivity();
SharedPreferences sharedPref = context.getSharedPreferences(
        getString(R.string.preference_file_key), Context.MODE_PRIVATE);
```
## Write to shared preferences
* To write to a shared preferences file, create a SharedPreferences.Editor by calling edit() on your SharedPreferences.
* Pass the keys and values you want to write with methods such as putInt() and putString(). Then call apply() or commit() to save the changes.

## Read from shared preferences
* To retrieve values from a shared preferences file, call methods such as getInt() and getString(), providing the key for the value you want, and optionally a default value to return if the key isn't present. 




































