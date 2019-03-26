# Carreira
App com recursos voltados a fidelizar clientes

## Android build debug
# manually create the bundle for a debug build.
$ react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res
$ cd android

# Create debug build:
$ ./gradlew assembleDebug

# Create release build:
$ ./gradlew assembleRelease #Generated `apk` will be located at `android/app/build/outputs/apk`

## iOS build
$ react-native bundle --entry-file='index.js' --bundle-output='./ios/Carreira/main.jsbundle' --dev=false --platform='ios' --assets-dest='./ios'

#troubleshooting
- quando der erro de "ENOSPC" ao executar "react-native start"
$ echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
