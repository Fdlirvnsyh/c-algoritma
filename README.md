<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.onoy.child"
    android:versionCode="1"
    android:versionName="1.0" >

    <uses-sdk
        android:minSdkVersion="14"
        android:targetSdkVersion="20" />

    <uses-permission android:name="android.permission.GET_TASKS" />
    <uses-permission android:name="android.permission.REAL_GET_TASKS" />
    <uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED" />
    <uses-permission android:name="android.permission.INTERNET" />

    <application
        android:allowBackup="true"
        android:icon="@drawable/ic_launcher"
        android:label="@string/app_name"
        android:theme="@android:style/Theme.Holo.Light.NoActionBar" >
        <activity
            android:name=".LoginActivity"
            android:windowSoftInputMode="adjustPan|adjustResize"
            android:label="@string/app_name"
            android:launchMode="singleTask" >
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
        <activity
            android:name=".AppListActivity"
            android:label="@string/title_activity_applist" >
        </activity>

        <service android:name=".service.AppService" >
        </service>

        <receiver
            android:name=".service.ServiceReceiver"
            android:enabled="true"
            android:exported="false" >
            <intent-filter>
                <action android:name="android.intent.action.BOOT_COMPLETED" />
                <action android:name="android.intent.action.QUICKBOOT_POWERON" />
            </intent-filter>
        </receiver>

        <activity
            android:name=".WelcomeActivity"
            android:label="@string/title_activity_welcome"
            android:launchMode="singleTask" >
        </activity>
        <activity
            android:name=".SettingActivity"
            android:label="@string/title_activity_setting" >
        </activity>
        <activity
            android:name=".MainActivity"
            android:label="@string/title_activity_login" >
        </activity>
        <activity
            android:name=".QuestionActivity"
            android:label="@string/title_activity_question" >
        </activity>
        <activity
            android:name=".ResultActivity"
            android:label="@string/title_activity_result" >
        </activity>
    </application>

</manifest>
