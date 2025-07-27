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

Example

    adb shell monkey -p com.android.chrome -c android.intent.category.LAUNCHER 1

Adjust Brightness

    adb shell settings put system screen_brightness 2000

Install Apk

    adb install -r /path/to/your_app.apk

Uninstall application

    adb uninstall <package_name>



