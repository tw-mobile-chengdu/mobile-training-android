# Intro to Android Studio

The Android Studio provide everything you need to develop an Android application.

In this session, we will walk through a demo project in `./demo` to learn basic usage.

## Setup Android SDK and Simulator

- Download Android Studio from Android developer website.
- Android Platform (Recommand least version)
<img src="./images/01-android-platform.png" width=700 />
- SDK Tools
<img src="./images/01-sdk-tools.png" width=700 />
- Simulator
<img src="./images/01-avd.png" width=700 />

## Walking through the Android Studio

### Create a new empty activty project

<img src="./images/01-new-project.png" width=700 />
<img src="./images/01-project-setting.png" width=700 />

### Main Window of Android Studio
<img src="./images/01-main-window.png" width=700 />
1. The toolbar lets you carry out a wide range of actions, including running your app and launching Android tools.
2. The navigation bar helps you navigate through your project and open files for editing. It provides a more compact view of the structure visible in the Project window.
3. The editor window is where you create and modify code. Depending on the current file type, the editor can change. For example, when viewing a layout file, the editor displays the Layout Editor.
4. The tool window bar runs around the outside of the IDE window and contains the buttons that allow you to expand or collapse individual tool windows.
5. The tool windows give you access to specific tasks like project management, search, version control, and more. You can expand them and collapse them.
6. The status bar displays the status of your project and the IDE itself, as well as any warnings or messages.

Then you should see simulator started and show a blank screen.

## Exercise: helloworld project

### Add some elements on to the screen

- Show some words (`UILabel`)
  - Click the following button to create UI elements.
  - Select the element you want.
  - Drag it to the position you want to put it.
  - Edit its attributes to make it looks like what we want. Change the text to `Hello, World!`.

<img src="./images/05-xcode-create-label.png" width=700 />
<img src="./images/05-xcode-create-label.gif" width=700 />

- Input field (`UITextField`)
  - Same step to create a label, just select different type of UI element and drag to the view.
  - Set the placeholder to `Input your name`
- Button (`UIButton`)
  - Set the button title to `Say Hello`
- Run the app, you should see the following screen in simulator.

<img src="./images/06-xcode-build-init-ui.png" width=300 />

### Link up UI elements between code and IB

<img src="./images/07-xcode-viewcontroller.png" width=300 />

Add `IBOutlet` and UI elements properties in the `ViewController` in above file.

```swift
@IBOutlet weak var helloLabel: UILabel!
@IBOutlet weak var nameTextField: UITextField!
@IBOutlet weak var helloButton: UIButton!
```

Then click the following button, and you should see two code panel and then you can connect the code and UI elements in IB by draging.

<img src="./images/08-xcode-show-two-code-panel.png" width=300 />
<img src="./images/09-xcode-two-panel-mode.png" width=700 />
<img src="./images/10-xcode-connect-ui-element-with-code.gif" width=700 />

### Write the logic code

- Update the label to `Hello, $your_name` when you click the say hello button using the name in the text field.

## What's next?

Though the next modules, we'll learn about most of the elements of the demo search property listings app:

- Enough of the Swift languge to get you going
- Using UIKit and Auto Layout to build the UI for the app
- Retrieving data from the network
- Displaying listings in a scrolling table
- Testing and debugging your application
- Submitting the app to the store

## Further reading

- Apple's documentation https://developer.apple.com/library/archive/documentation/ToolsLanguages/Conceptual/Xcode_Overview/
- Shortcuts https://swifteducation.github.io/assets/pdfs/XcodeKeyboardShortcuts.pdf
- Ray Wenderlich Tutorials, eg. Your First iOS App
- A large list of iOS learning resources and blogs: https://github.com/sanketfirodiya/iOS-learning-resources
