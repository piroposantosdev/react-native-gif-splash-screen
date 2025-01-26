# React Native GIF Splash Screen

## Overview
This repository provides a simple and efficient implementation of a custom splash screen using animated GIFs in React Native applications.

## Features
- Easy integration with React Native projects
- Support for custom GIF animations
- Cross-platform compatibility (iOS and Android)
- Configurable display duration

## Installation
```bash
npm install react-native-gif-splash-screen
# or
yarn add react-native-gif-splash-screen
```

## Usage
```javascript
import SplashScreen from 'react-native-gif-splash-screen';

// Display splash screen
SplashScreen.show({
  gif: require('./path/to/splash.gif'),
  duration: 3000 // Optional duration in milliseconds
});

// Hide splash screen when ready
SplashScreen.hide();
```

## Configuration Options
- `gif`: Path to your splash screen GIF
- `duration`: Custom display time (default: automatic)
- `fullScreen`: Toggle full-screen display

## Requirements
- React Native 0.60+
- iOS 12+
- Android 5.0+

## Contributing
Contributions are welcome! Please read our [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
