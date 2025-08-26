This set of adb(Android Debug Bridge) commands usefull when developing android application

Take screenshot and store in android mobile:

    adb shell screencap -p /sdcard/screen.png

Pull that screenshot to your system:

    adb pull /sdcard/screen.png ~/Desktop/

this can pull the screenshot from android device and save it to Desktop

Open Camera

    adb shell am start -a android.media.action.IMAGE_CAPTURE
    adb shell am start -a android.media.action.VIDEO_CAPTURE

Take image

    adb shell input keyevent 27

Open Specific application

    adb shell monkey -p <package_name> -c android.intent.category.LAUNCHER 1
    adb shell monkey -p com.google.android.youtube 1
    adb shell monkey -p com.android.settings -c android.intent.category.LAUNCHER 1

Example

    adb shell monkey -p com.android.chrome -c android.intent.category.LAUNCHER 1

Adjust Brightness

    adb shell settings put system screen_brightness 2000

Install Apk

    adb install -r /path/to/your_app.apk

Uninstall application

    adb uninstall <package_name>

Click the power button

    adb shell input keyevent 26

Swipe the screen

    adb shell input swipe 300 1000 300 500

Enter password

    adb shell input text "123456"

Turn On Wifi

    adb shell svc wifi enable

Turn off wifi

    adb shell svc wifi disable

Get the Screen Resolution

    adb shell wm size






