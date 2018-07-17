# Procedure to realize transferCL on you device (for dummies)

* Setup required
    * CrystalX NDK downloaded and extracted
    * Android studio
    * libOpenCL.so library pulled from your Android Device

## What is crystalX NDK and why do I need it?
Its a native development kit (same as what google provides) but many
dependencies built in (for example, boost library is already there)

Download it from https://www.crystax.net/download/crystax-ndk-10.3.2-linux-x86_64.tar.xz
Once downloaded, you need to build transferCL library

## How to build TransferCL library?
* First of all, make sure you have pulled the libOpenCL.so from your Android phone
* Put it inside /TransferCL_package/extra_libs
Then cd to jni folder, and build the library (Android.mk and Application.mk is already there)

## How to build the library?
while being inside jni folder, give command like this:
~/Downloads/crystalX/ndk-build -B
**Make sure that you replace Download/crystalX with something your crystalX NDK is present**

## What after building?
Now its the time to take the built libraries from libs folder (copy both armeabi and armeabi-v7a folders)
to MyApplication/app/src/main/jniLibs

Now, its time to build your application with android Studio

## What after installing the app? How to test it?
**First make sure app has sdcard permission, if not, then give it from app settings**
Now, copy the "character" folder to /sdcard/ of your phone. This is not SD Card, this is
the android directory I am talking.

Once, done, run the application.

## Are you facing any difficulty in any one of these steps?
Contact: bulletcross@gmail.com 
