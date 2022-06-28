# **Expo Starter**

## **EXPO _"tabs"_ TEMPLATE STRUCTURE**

#### **_`.expo/`_**

- `devices.json`
  - _contains information about devices that have recently opened this project. This is used to populate the "Development sessions" list in your development builds._
- `packager-info.json`
  - _contains port numbers and process PIDs that are used to serve the application to the mobile device/simulator._
- `settings.json`
  - _contains the server configuration that is used to serve the application manifest._

#### **_`.expo-shared/`_**

#### **_`.vscode/`_**

- _user's Visual Studio Code settings_

#### **_`assets/`_**

- `fonts/`
  - _installed fonts_
- `images/`
  - `adaptive-icon.png`
  - `favicon.png`
  - `icon.png`
  - `splash.png`
    - _used on app-load_

#### **_`components/`_**

- `__tests__`
  - `StyledText-test.js`
- `EditScreenInfo.tsx`
- `StyledText.tsx`
  _example: manually-styled custom `<Text/>` component_
- `Themed.tsx`
  _example: custom components styled using user's device or defined theme variants_

#### **_`constants/`_**

- `Colors.ts`
  - _theme color tokens_
- `Layout.ts`
  - _theme layout tokens using React Native [`Dimensions`](https://reactnative.dev/docs/dimensions) API_

#### **_`hooks/`_**

- `useCachedResources.ts`
  - _prevents `SplashScreen` from auto-hiding until required app resources are loaded_
- [`useColorScheme.ts`](https://reactnative.dev/docs/usecolorscheme)
  - _core React Native hook that returns & subscribes to user's device appearance preferences via the [`Appearance`](https://reactnative.dev/docs/appearance) module_

#### **_`navigation/`_**

- `index.tsx`
  - _root [`NavigationContainer`](https://reactnavigation.org/docs/navigation-container) with configured `linking` & `theme` props set_
- `LinkingConfiguration.ts`
  - _deep-linking configuration_

##### **_//////////////////// ISSUE /////////////////////_**

```
TS2786: <NavComponent> cannot be used as a JSX component
```

**_[SOLUTION](https://medium.com/@bseleng/3-steps-to-fix-stack-navigator-61f22d60dba2)_**

add to `package.json`

```json
"resolutions": {
  "@types/react": "^17"
}
```

then

```shellscript
yarn install
```

[`yarn why`](https://classic.yarnpkg.com/lang/en/docs/cli/why/) --> info about WHY a pkg is installed

/////////////////////////////////////////

#### **_`screens/`_**

- _various example screens_

#### **_`.gitignore`_**

#### **_[`app.json`](https://docs.expo.dev/workflow/configuration/)_**

- _non-code app configs_

#### **_`App.tsx`_**

- _app entry file_
- [`import { StatusBar } from 'expo-status-bar'`](https://docs.expo.dev/versions/v45.0.0/sdk/status-bar/)
  - _platform-dependent interface for controlling the device's status bar_
- [`import { SafeAreaProvider } from 'react-native-safe-area-context'`](https://github.com/th3rdwave/react-native-safe-area-context)
  - _Context for playing inside a device's "safe area"_

#### **_[`babel.config.js`](https://babeljs.io/docs/en/configuration)_**

- _Babel JavaScript compiler config file_

#### **_[`package.json`](https://docs.npmjs.com/cli/v6/configuring-npm/package-json)_**

- _project's package management file where you can modify stuff like [configs](https://docs.npmjs.com/cli/v6/using-npm/config) & [scripts](https://docs.npmjs.com/cli/v6/using-npm/scripts)_

#### **_[`tsconfig.json`](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html)_**

- _TypeScript config file: `tsconfig.json` [reference](https://www.typescriptlang.org/tsconfig)_

#### **_`types.tsx`_**

- _[navigation](https://reactnavigation.org/docs/typescript/) types_
