---
summary: About obfuscation of the logs in native mobile app builds. 
tags: support-mobile
locale: en-us
guid: 1578fb0f-f45d-4b74-8f2c-f9e958d45535
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Obfuscation and retracing logs of mobile builds

If you use OutSystems AppShield plugin, MABS obfuscates native code from the shell and supported plugins. An app crash from an obfuscated code generates an obfuscated stack trace.

## How to retrace Android obfuscated logs

The purpose of the obfuscation is to make the app harder to reverse-engineer. During the obfuscation process, the platform creates a mapping with the old and new names of methods and classes.

In an obfuscated app, an error stack trace might look like this:

![Obfuscation example](images/obfuscated.png)

**Prerequisites**

These are the prerequisites to deobfuscate the logs.

* Android Studio on Mac, Linux, or Windows.
* The **mapping.txt** file from the build. Please reach Support and request the mapping file. 
* A stack trace to deobfuscate and retrace.

**Steps**

1. Have the mapping file ready.
1. Locate the proguard tools, located under your Android SDK folder, usually in `$ANDROID_HOME/tools/proguard/bin`.
1. Inside, you should have the retrace cli, or the proguardgui.

    With **retrace cli**. Use the retrace command, followed by the path to the mapping file and the file with the stack trace. Or, run the command without the stack trace file and then paste the log content. 

    With **proguardgui**. Click the **ReTrace** button in the left pane and locate your mapping file. Paste the obfuscated stack trace and click **ReTrace!**.

    ![Proguard UI](images/proguard-log.png) 

<div class="warning" markdown="1>

The lines for the purposes of parsing can't have the timestamp, which is what logcat tools usually produce. Instead, the lines must start with the **at** keyword.

</div>

For more information about logs, see:

* [Write and View Logs with Logcat](https://developer.android.com/studio/debug/am-logcat#format)
* [ReTrace](https://www.guardsquare.com/en/products/proguard/manual/retrace)
* [ProGuard](https://www.guardsquare.com/en/products/proguard)

## Obfuscation with customized plugins

Customized and non-supported mobile plugins might not work correctly with obfuscation. Unexpected results, app errors or a crashes, might occur because of obfuscation with any of the following:

* A misconfigured dependency
* Java code plugins or code from libraries imported using Gradle or JAR/AAR file
* Reflection to perform operations based on class/method name 

For example, different class names can cause a ClassNotFound exception, or different method names can cause a MethodNotFound exception. Getting a `ClassNotFoundException` or `MethodNotFoundException` at runtime is a sign you're missing classes or methods. The class or method name might be obfuscated or missing because of some misconfigured dependencies.

The following are examples of obfuscated exceptions.

```
java.lang.ClassNotFoundException: com.example.SomeClass
    at java.lang.Class.classForName(Native Method)
    at java.lang.Class.forName(Class.java:454)
    at java.lang.Class.forName(Class.java:379)
    ...
```

```
java.lang.ClassNotFoundException: Didn't find class "com.example.SomeClass" on path: DexPathList[[zip file "/data/app/..., /system/lib, /system_ext/lib]]
    at dalvik.system.BaseDexClassLoader.findClass(BaseDexClassLoader.java:207)
    at java.lang.ClassLoader.loadClass(ClassLoader.java:379)
    at java.lang.ClassLoader.loadClass(ClassLoader.java:312)
    ...
```

```
java.lang.NoSuchMethodException: com.example.SomeClass.someMethod [class java.lang.String, int]
    at java.lang.Class.getMethod(Class.java:2072)
    at java.lang.Class.getMethod(Class.java:1693)
    ...
```

```
java.lang.AssertionError: illegal type variable reference
    at libcore.reflect.TypeVariableImpl.resolve(TypeVariableImpl.java:111)
    at libcore.reflect.TypeVariableImpl.getGenericDeclaration(TypeVariableImpl.java:125)
    at libcore.reflect.TypeVariableImpl.hashCode(TypeVariableImpl.java:47)
    at com.google.gson.reflect.TypeToken.[init](TypeToken.java:64)
    ...
```
