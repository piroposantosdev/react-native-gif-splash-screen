# React Native GIF Splash Screen

## Overview
This repository provides a simple and efficient implementation of a custom splash screen using animated GIFs in React Native applications.

## Features
- Easy integration with React Native projects
- Support for custom GIF animations
- Cross-platform compatibility (iOS and Android)
- Configurable display duration

## Usage
You need to create a new .js or .tsx file and insert the code below. You need to set your app home page to this authoring view.
Using this idea, you can even create a loading page for your apps by just calling this View while your apps are loading some data in another one, just use your creativity

```
const Splash = ({navigation}) => {    
    setTimeout(() => navigation.navigate("Welcome"), 5000); //Set your initial page after the splash screen, and the timeout
    return (
        <View
            style={{
                flex: 1,
                backgroundColor: '#498b89', //Background color you want
                justifyContent:'center',
                alignItems: 'center',
            }}
        >
             <Image
                source={require("../../assets/images/YourGif.gif")} // Here you can set your gif file... For better experience, use local files. 
                style={{
                    position: 'absolute',
                    zIndex: 1,
                    width: '100%', //Adjust as your needs
                    height: '100%, //Adjust as your needs                    
                    padding: 0
                }}
             />
        </View>
    )
}
```

## Configuration
- `allow gif`: If you are facing problems to load .gif files in Android <Image> component, you must add this in your android/app/build.gradle dependencies:
  ```
    [...]
    implementation 'com.facebook.fresco:animated-gif:3.2.0'
  ```
- `remove android splash screen`: To completely remove the default Android splash screen, you must add this to your android/app/src/main/res/values/styles.xml:
  ```
    [...]
    <item name="android:windowDisablePreview">true</item>
    <item name="android:windowIsTranslucent">true</item>
  ```
- `IOS adjust`: Open your ios/ProjectName/LaunchScreen.storyboard in xcode and remove all texts from the screen. To have a better view, change the background color of this view to the same color of your Splash view. To do it, just click in View Controller Scene -> View Controller -> View. In the right bar you will see an option to change the View background color. 

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
