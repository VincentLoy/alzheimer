# Install ionic

-  `npm install -g cordova ionic`
- `sudo aptitude install lib32z1 lib32ncurses5 openjdk-7-jdk`

1. install openjdk
  `sudo apt-get install openjdk-7-jdk`
  
2. install `android sdk`
  ### download android sdk
  - `wget http://dl.google.com/android/android-sdk_r24.2-linux.tgz`
  - `tar -xvf android-sdk_r24.2-linux.tgz`
  - `cd android-sdk-linux/tools`

  ### install all sdk packages
  - `./android update sdk`

3. set PATH in `~/.zshrc` 
  - `PATH=${PATH}:$HOME/bin/Android/platform-tools:$HOME/bin/Android/tools:$HOME/bin/Android/build-tools/25.0.2/`

4. install the desired Android platforms
  - `/home/[user]/bin/Android/Sdk/tools/android sdk`

5. install Android images
  - `/home/[user]/bin/Android/Sdk/tools/android avd`

6. add Android platform to Ionic
  - `ionic platform add android`

7. Run emulator
  - `ionic emulate android`

8. Enable your phone for development mode
  go to `Settings > More > About` and tab `Build number` 7 times
  go to `Settings > More > Developer Options` and enable `USB debugging`
  
9. Run Ionic app on Android phone natively
  connect Android phone to PC via USB
  run `ionic run android`
  
10. Debug the app running on the phone
   with the app running on the device open Chrome and navigate to `chrome://inspect/#devices`
   find your device and click `Inspect`
