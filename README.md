This set of adb(Android Debug Bridge) commands usefull when developing android application

Take screenshot and store in android mobile:

    adb shell screencap -p /sdcard/screen.png

Pull that screenshot to your system:

    adb pull /sdcard/screen.png ~/Desktop/

this can pull the screenshot from android device and save it to Desktop
