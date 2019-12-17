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

### Create Mock Server

Most the mobile app will use the HTTP/HTTPS protocol to communicate with the server, we will setup a mock server to help us do the app develop:

* setup mock server because sometime the server delivery with app at the same time, we can change our app point to local mock server, then you can start the develop/debug.
* we will setup the functional test for the app, we also need this mock server, it more stable then the real server.

There are a lot of mock server library, e.g. [mountbank](http://www.mbtest.org/), [nock](https://github.com/nock/nock). in this workshop we choose [json-server](https://github.com/typicode/json-server).

* Change the Project type from "Android" to "Project", and in root folder, create a new folder `mock`.
<img src="./images/04-mock-folder.png" width=700 />

* In terminal, cd to `mock` folder, run command `npm init`, every question you can keep default value.
* In terminal, run command `npm install json-server` to install node module.
* In `mock` folder, create new file `db.json`, and add some content.

```json
{
  "home_timeline": [
    {
      "created_at": "Tue May 31 17:46:55 +0800 2011",
      "id": 11488058246,
      "text": "求关注。",
      "reposts_count": 8,
      "comments_count": 9,
      "user": {
        "id": 1404376560,
        "screen_name": "zaku",
        "name": "zaku"
      }
    }
  ],
  "comments": [
    {
      "created_at": "Wed Jun 01 00:50:25 +0800 2011",
      "id": 12438492184,
      "text": "love your work.......",
      "user": {
        "id": 1404376560,
        "screen_name": "zaku",
        "name": "zaku"
      }
    }
  ]
}
```

* open the package.json file, in `scrips` setion add `start: "json-server --watch db.json"`.
* In termimal, run command `npm start` to start the mock server.
* Then you can see the mock server info in terminal:
<img src="./images/04-mock.png" width=700 />

* Add `node_modules` and `.idea` into `.gitignore`, then add a new git commit.
<img src="./images/04-gitignore.png" width=700 />

Two Tips:
* Use google search to setup the Node environment in you local machine.
* Use google search to get some HTTP/HTTPS document to read.