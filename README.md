                       <!-- Add some code in Main Application.java <ProjectName>\android\app\src\main\java\com\simplenavigation\MainApplication.java -->

<h5>// <- add this package</h5>
  
import com.facebook.react.bridge.JSIModulePackage;           
import com.swmansion.reanimated.ReanimatedJSIModulePackage;  

<h5>// <- add this module</h5>
  
@Override
      protected JSIModulePackage getJSIModulePackage() {
      return new ReanimatedJSIModulePackage();               
      }


                                      <!-- \<ProjectName>\android\app\build.gradle -->

<h5>// <- here | clean and rebuild if changing</h5>
  
project.ext.react = [
  enableHermes: true                                        
]

                                      <!-- <ProjectName>\babel.config.js -->

module.exports = {
  presets: ['module:metro-react-native-babel-preset'],
  plugins: ['react-native-reanimated/plugin'],
};

