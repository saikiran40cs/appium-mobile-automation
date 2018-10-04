# Installing App on Emulator {#installing-app-on-emulator}

Once your emulator is ready and you have the android path set up properly, the next action would be to install an app on the Emulator which would become your application under test.

The first step is to run the emulator on which you want to install the app.

```
emulator -avd <AVD_Name>
```

This would launch the emulator and the command would be running in the terminal.

There are couple of ways to install the app:

* install via adb command
* drag and drop

**Install via adb command:**

* Download the apk and put it in some folder
* Run the following command

```
  adb install path/to/your/app.apk

```

when more than one emulator is open, run the following command

`adb -s serial-number-of-device install path/to/your/app.apk`

**Drag and Drop**

* You can alternately drag the apk file and drop on to the emulator.



