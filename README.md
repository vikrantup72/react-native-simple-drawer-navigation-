                       <!-- Add some code in Main Application.java <ProjectName>\android\app\src\main\java\com\simplenavigation\MainApplication.java -->

import com.facebook.react.bridge.JSIModulePackage;           <h3>// <- add this package</h3>
import com.swmansion.reanimated.ReanimatedJSIModulePackage;  <h3>// <- add this package</h3>

@Override
      protected JSIModulePackage getJSIModulePackage() {
      return new ReanimatedJSIModulePackage();               <h3>// <- add this module</h3>
      }


                                                          <!-- \<ProjectName>\android\app\build.gradle -->

project.ext.react = [
  enableHermes: true                                         <h3>// <- here | clean and rebuild if changing</h3>
]

                                                                <!-- <ProjectName>\babel.config.js -->

module.exports = {
  presets: ['module:metro-react-native-babel-preset'],
  plugins: ['react-native-reanimated/plugin'],
};

