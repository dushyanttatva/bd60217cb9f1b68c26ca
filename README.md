# Engineer.ai

### Definition:

1. Periodically (every 10 seconds) poll for new posts from this API https://hn.algolia.com/api/v1/search_by_date?tags=story&page=0 via a GET request.
2. New posts fetched after 10 seconds will be added to old posts.
3. Increase page count in each subsequent get request.
4. Implement pagination when the list is scrolled.
5. The pagination and periodic request both should work mutually exclusive i.e for each request page number will be increased. Request with the same page number should never be made.
6. Display the title, URL, created_at, and author of each post in a table.
7. Upon selecting a row in the table, the user is taken to a new page that displays the raw JSON.
8. Generate APK and IPA files.

Currently includes:

- React Native
- React Navigation
- Redux
- Saga
- And more!

## Quick Start

The project's structure will look similar to this:

```
bd60217cb9f1b68c26ca
├── src
│   ├── components
│   ├── config
│   ├── constants
│   ├── utils
│   ├── redux
│   ├── sagas
│   ├── navigation
│   ├── screens
│   ├── services
│   ├── App.js
├── README.md
├── android
│   ├── app
│   │   ├── build.gradle
│   │   └── .keystores
│   ├── build.gradle
│   ├── gradle
│   ├── gradle.properties
│   ├── gradlew
│   ├── gradlew.bat
│   └── settings.gradle
├── index.js
├── ios
│   ├── engineerai
│   ├── engineerai-tvOS
│   ├── engineerai-tvOSTests
│   ├── engineerai.xcodeproj
│   └── engineeraiTests
├── app.json
└── package.json

```

### ./src directory

Project source code is in the `src` directory.

The inside of the src directory looks similar to the following:

```
app
│── components
│── config
├── constants
├── navigation
├── screens
├── services
├── sagas
├── redux
├── utils
└── App.js
```

**components**
This is where your React components will live. Each component will have a directory containing the `.js` file. The app will come with some commonly used components like Button.

**config**
This is where your have translations will live if you are using `i18n-js and react-native-localize`.

**redux**
This is where your app's redux component will live such as actions, reducers & store.

**sagas**
This is where your app's api call side effects will be handled.

**navigation**
This is where your `@react-navigation/native` navigators will live.

**screens**
This is where your screen components will live. A screen is a React component which will take up the entire screen and be part of the navigation hierarchy. Each screen will have a directory containing the `.js` file, along with styles files.

**services**
Any services that interface with the outside world will live here (think REST APIs, Push Notifications, etc.).

**constants**
Here lives your application API_URL and other constants & colors constants.

**utils**
This is a great place to put miscellaneous helpers and utilities. Things like date helpers, formatters, etc. are often found here. However, it should only be used for things that are truely shared across your application. If a helper or utility is only used by a specific component or model, consider co-locating your helper with that component or model.

**index.js** This is the entry point to your app. This is where you will find the main App component which renders the rest of the application.
