<!-- Add some code in Main Application.java <ProjectName>\android\app\src\main\java\com\simplenavigation\MainApplication.java -->

import com.facebook.react.bridge.JSIModulePackage;    // <- add this package
import com.swmansion.reanimated.ReanimatedJSIModulePackage;  // <- add this package

@Override
      protected JSIModulePackage getJSIModulePackage() {
        return new ReanimatedJSIModulePackage(); // <- add this module
      }


<!-- \<ProjectName>\android\app\build.gradle -->

project.ext.react = [
  enableHermes: true  // <- here | clean and rebuild if changing
]

<!-- <ProjectName>\babel.config.js -->

module.exports = {
  presets: ['module:metro-react-native-babel-preset'],
  plugins: ['react-native-reanimated/plugin'],
};

