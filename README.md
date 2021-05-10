**Time To Build An Instant Chat App For Android With CONTUS MirrorFly**

Well, when it comes to building a messaging chat, voice, and video solution, every chat app provider follows their own protocols. Moreoless, all of them would be checking out to give out something best.

This section is all about the involvement of CONTUS MirrorFly when it comes to building chat applications for Android, iOS and web apps.

But here, I am going to give you an understanding of creating a chat app for Android platform. The exciting part is that this solution can be integrated easily into your application. Moreover, when it comes to the client-side, you can have them initialized as well as configured as per your need with minimal effort.


On the other hand with regards to server-side, CONTUS MirrorFly focuses mainly on the reliability within the application.  It allows the space for all server setup-related documents to be downloaded from the control panels’ download section.

This later with initialization page gives the Chat SDK’s structure and installation procedure. Once everything is done, it moves across the preliminary steps of implementing the Chat SDK in your own project.

**Requirements**

Let’s have a look at some of the minimal requirements for Chat SDK for Android
1) Android Lollipop 5.0 (API Level 21) or above
2) Java 7 or higher
3) Gradle 4.1.0 or higher

**SDK License Key**

As an initial process, it is essential to see that the SDK is authenticated by CONTUS MirrorFly server using License Key. In this, you can make use of the master License Key in your dashboard while generating an account. 
But, one thing that needs to be noticed is that the master API token can not be revoked or changed later.

**Installation**

To begin with, you need to check whether the SDK has already been compiled into an AAR file or not? This is so as to use the SDK, the below AAR file has to be imported into the project. However, the support of kotlin is needed for the chat SDK in the project to move ahead.

Step 1 : First have to download the latest SDK from CONTUS MirrorFly Control Panel Download’s section.
Step 2 : Extract the files from downloaded zip file.
Step 3 : Create a new Android project.

**Step 4 : Add the file libraries in app/libs folder in the project,**

appbase.aar
flycommons.aar
flynetwork.aar
flydatabase.aar
compression.aar
xmpp.aar

**Step 5 : Add The Following Dependencies In App/Build.Gradle File**


implementation files('libs/appbase.aar')
implementation files('libs/flycommons.aar')
implementation files('libs/flynetwork.aar')
implementation files('libs/flydatabase.aar')
implementation files('libs/compression.aar')
implementation files('libs/xmpp.aar')


**Step 6 : Add The Below Required Dependencies By The SDK In App/Build.Gradle**

//For lifecycle listener
implementation 'android.arch.lifecycle:extensions:1.1.1'
annotationProcessor 'android.arch.lifecycle:compiler:1.1.1'

//For GreenDao
implementation 'de.greenrobot:greendao:2.1.0'

//For gson parsing
implementation 'com.google.code.gson:gson:2.8.1'

//for smack implementation
implementation 'org.igniterealtime.smack:smack-android:4.2.4'
implementation 'org.igniterealtime.smack:smack-tcp:4.2.4'
implementation 'org.igniterealtime.smack:smack-im:4.2.4'
implementation 'org.igniterealtime.smack:smack-extensions:4.2.4'
implementation 'org.igniterealtime.smack:smack-sasl-provided:4.2.4'

implementation 'androidx.localbroadcastmanager:localbroadcastmanager:1.0.0'
implementation 'androidx.multidex:multidex:2.0.1'
implementation 'com.google.android.gms:play-services-location:17.0.0'

implementation 'com.facebook.stetho:stetho:1.3.1'
implementation 'com.hypertrack:hyperlog:0.0.10'

//for mobile number formatting
implementation 'io.michaelrocks:libphonenumber-android:8.9.14'

//Dagger Dependencies
api 'com.google.dagger:dagger:2.25.2'
kapt 'com.google.dagger:dagger-compiler:2.25.2'
api 'com.google.dagger:dagger-android:2.25.2'
api 'com.google.dagger:dagger-android-support:2.25.2'
kapt 'com.google.dagger:dagger-android-processor:2.25.2'

//coroutines
implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.3'
implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-test:1.3.3'

//apicalls
implementation 'com.squareup.retrofit2:retrofit:2.6.1'
implementation 'com.squareup.retrofit2:converter-gson:2.6.1'
implementation 'com.squareup.okhttp3:okhttp:4.2.0'
implementation 'com.jakewharton.retrofit:retrofit2-kotlin-coroutines-adapter:0.9.2'

//stetho interceptor
implementation 'com.facebook.stetho:stetho-okhttp3:1.3.1'

//okhttp interceptor
implementation 'com.squareup.okhttp3:logging-interceptor:3.14.3'

**Step 7 : Add The Below Code In The App-Level Build.Gradle**

plugins {
    ...
    id 'kotlin-android'
    id 'kotlin-kapt'
}

android {
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }

    kotlinOptions {
        jvmTarget = '1.8'
    }

    packagingOptions {
        exclude 'META-INF/AL2.0'
        exclude 'META-INF/DEPENDENCIES'
        exclude 'META-INF/LICENSE'
        exclude 'META-INF/LICENSE.txt'
        exclude 'META-INF/license.txt'
        exclude 'META-INF/NOTICE'
        exclude 'META-INF/NOTICE.txt'
        exclude 'META-INF/notice.txt'
        exclude 'META-INF/ASL2.0'
        exclude 'META-INF/LGPL2.1'
        exclude("META-INF/*.kotlin_module")
    }

}

**Step 8 : Open The AndroidManifest.Xml And Add Below Permissions**


<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.RECORD_AUDIO" />
<uses-permission android:name="android.permission.DISABLE_KEYGUARD" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.READ_PHONE_STATE" />
<uses-permission android:name="android.permission.WAKE_LOCK" />

These are the technical steps that are required to have the best chat app.

Also Read : https://blog.mirrorfly.com/build-chat-app-for-android/
