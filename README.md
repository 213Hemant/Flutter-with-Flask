# flutterflasktemplate

A starting point for Flutter Apps with Flask as their backend Framework

## Getting Started

Steps :
1. Create 4 Terminals: 2 normal for flutter and 2 venv for the new backend folder
2. Create a virtual environment (if you are not cloning this repo directly) in the new backend folder and activate it in the two terminals
3. Include the run_server.bat file in the backend folder
4. Include the run_flutter.bat file in the main project folder
5. Include http package in the dependencies of pubspec.yaml
6. If you have cloned this repository, then delete the venv folder by first deactivating it.
7. In flask terminal run deactivate.
8. Then run Remove-Item -Recurse -Force venv (Powershell) or rmdir /s /q venv (bash)
9. Create new venv by python -m venv backend
10. Activate it .\backend\Scripts\activate
11. Pip install flask
12. In flask terminal (ensure venv activated) pip install flask
13. Check the main.dart and app.py files
14. In flask terminal run run_server.bat
15. In flutter terminal run run_flutter.bat


Note: This project was created in Android Studio by clicking on new Flutter Project button (flutter plugin).
Note : If you are getting errors after running the flutter app saying that they are due to JDK 21, Please follow following steps:

1. Basically, you need this in app\build.gradle:

android {
    ndkVersion "25.1.8937393"

    compileOptions {
        sourceCompatibility JavaVersion.VERSION_17
        targetCompatibility JavaVersion.VERSION_17
    }
    kotlinOptions {
        jvmTarget = 17
    }
}

2. This in settings.gradle:

id "com.android.application" version "8.3.2" apply false
id "org.jetbrains.kotlin.android" version "2.0.20" apply false

3. And this in gradle-wrapper.properties:

distributionUrl=https\://services.gradle.org/distributions/gradle-8.10.2-all.zip
