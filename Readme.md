## Useful Phonegap command for Windows

#### generate keystore file 
```keytool -genkey -v -keystore PROJECT-NAME.keystore -alias YOUR-ALIAS-NAME -keyalg RSA -keysize 2048 -validity 10000```

#### generate facebook key hash
`keytool -exportcert -alias YOUR-ALIAS-NAME -keystore "[path-to-keystore]\PROJECT-NAME.keystore" | "C:\Program Files (x86)\Git\bin\openssl.exe" sha1 -binary |"C:\Program Files (x86)\Git\bin\openssl.exe" base64`

#### release apk 
`.\platforms\android\cordova\build.bat --release`


#### sign apk file 
`jarsigner -storepass YOUR-PASSWORD -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore PROJECT-NAME.keystore PROJECT-NAME-release-unsigned.apk ALIAS-NAME`

#### zip align apk file for production release 
`zipalign -v 4 YOUR_PROJECT_NAME-unaligned.apk YOUR_PROJECT_NAME-aligned.apk`


#### Get the device name of your emulator (Example "emulator-5554") by running:
`.\platforms\android\cordova\lib\list-devices.bat`

#### To emulate to the device, run this command: 
`cordova emulate --target=emulator-5554 android`

