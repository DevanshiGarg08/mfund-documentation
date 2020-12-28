# Mfund Flutter App

## Mfund-app :

### Clone Repositories

Mfund Flutter app is a mono repo git project. We need to clone four repositories for flutter app.

* mfund-app 
* mfund-api-service : Contains all repositories and API call for flutter app.
* mfund-framework : Contains BloCs , States and Events.
* mfund-common-modules : Contains services, utils and common widgets for both mfund-app and mfund-dashboard-app. 
* mfund-dashboard-app : 

```text
mkdir mfund-flutter-app
cd mfund-flutter-app
git clone <URL for mfund-app>
git clone <URL for mfund-api-service>
git clone <URL for mfund-framework>
git clone <URL for mfund-common-modules>
```

### Setup for Firebase in mfund-app

* Create Firebase Storage by following this documentation - [https://firebase.google.com/docs/storage/android/start](https://firebase.google.com/docs/storage/android/start)
* Setup firebase for IOS app using following documentation - [https://firebase.google.com/docs/flutter/setup?platform=ios](https://firebase.google.com/docs/flutter/setup?platform=ios)
* Setup firebase for Android app using following documentation - [https://firebase.google.com/docs/flutter/setup?platform=android](https://firebase.google.com/docs/flutter/setup?platform=android)

### Run the mfund-app

```text
cd mfund-flutter-app
flutter run
```

## Mfund-dashboard-app :

### Clone Repositories

We need to clone four repositories for mfund-dashboard-app as we did in mfund-app

* mfund-dashboard-app
* mfund-api-service
* mfund-framework
* mfund-common-modules

```text
mkdir mfund-flutter-dashboard
cd mfund-flutter-dasboard
git clone <URL for mfund-dashboard-app>
git clone <URL for mfund-api-service>
git clone <URL for mfund-framework>
git clone <URL for mfund-common-modules>
```

### Run the mfund-dashboard-app

```text
cd mfund-flutter-dasboard
flutter run
```

