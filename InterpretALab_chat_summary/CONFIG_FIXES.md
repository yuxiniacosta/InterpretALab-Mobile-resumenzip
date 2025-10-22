CONFIG_FIXES.md

1) gradle.properties (en %USERPROFILE%\.gradle\gradle.properties)
-----------------------------------------
systemProp.http.proxyHost=
systemProp.http.proxyPort=
systemProp.https.proxyHost=
systemProp.https.proxyPort=
org.gradle.daemon=true
org.gradle.jvmargs=-Xmx2048m

2) build.gradle (Project-level)
-----------------------------------------
buildscript {
    ext.kotlin_version = '1.9.0'
    repositories {
        google()
        mavenCentral()
    }
    dependencies {
        classpath "com.android.tools.build:gradle:8.4.1"
        classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:$kotlin_version"
    }
}

allprojects {
    repositories {
        google()
        mavenCentral()
    }
}

task clean(type: Delete) {
    delete rootProject.buildDir
}

3) gradle-wrapper.properties
-----------------------------------------
distributionUrl=https\://services.gradle.org/distributions/gradle-8.7-all.zip
