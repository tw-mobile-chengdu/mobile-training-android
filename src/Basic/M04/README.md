# Weibo Workshop Preparation

### Story

#### Context
When we start a new project, most of time we will create Iteration 0 to setup the project structure.

#### Scope

* Project init
* Mock server setup
* Add 3rd Library

#### Acceptance Criteria

| Given | When | Then |
| :--- | :--- | :--- |
| I am a developer | I use Android Studio import the project | I can see the main project already set up done, and there is a MainActivity |
| I am a developer | I use the command line tool start the mock server | I can see the http server has been started |
| I am a developer | I use Android Studio import the project | I can see the MVP architecture already set up |
| I am a developer | I user Android Studio import the project | I can see the unit test & functional test already set up |
| I am a developer | I user Android Studio import the project | I can see the network connectivity already set up |


### Create the Andorid Project

Use empty activity phone and tablet template create the project:

* Name: Mini weibo
* Package Name: com.thoughtworks.miniweibo
* Language: Kotlin
* Minimum API level: API 19: Android 4.4(KitKat)

After empty project created, you can use git init a repo, and add your first commit.

### Add Libraries

#### Gradle

Android application use gradle as the build tool.
[Configure your build](https://developer.android.com/studio/build)
[Gradle tips and recipes](https://developer.android.com/studio/build/gradle-tips)

#### Architecture Guide

Android provide the official best practice architecture guide.

[Architecture Guide](https://developer.android.com/jetpack/docs/guide)
Your can refer this guide to set up your project gradle build and write your first activity.

* [LiveData](https://developer.android.com/topic/libraries/architecture/livedata)
* [ViewBinding](https://developer.android.com/topic/libraries/view-binding)
* [DataBinding](https://developer.android.com/topic/libraries/data-binding)
* [Room](https://developer.android.com/topic/libraries/architecture/room)
* [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel)

If you are first develop the android app, you should better use the old way to build a demo activity to familiarize the activity, fragment and service components.

You also need add 3rd libraries, you should add dependencies into `build.gradle` file.

* Add dependencies in `build.gradle`
  * [Dagger](https://dagger.dev/android) and [Retrofit](https://square.github.io/retrofit/)

#### Use TDD write your first API Service

* Create new Kotlin test file "WeiboServiceTest.kt" in test "com.thoughtworks.miniweibo.api"
* Add test `get home timeline post`
* Most time when we set up the project, we need add some helper/util class first, and these module may be created by your previous project or you can refer to the [android architecture simple](https://github.com/android/architecture-components-samples/tree/master/GithubBrowserSample), or check the [commit](https://github.com/tw-mobile-chengdu/android-miniweibo/commit/f69bf7e815b6563f26d4d10cf415d28ffa7506e0)

Tips:

* You should study [TDD](https://martinfowler.com/bliki/TestDrivenDevelopment.html), [Junit](https://junit.org/junit5/docs/current/user-guide/) first.

