# Flutter Development

### Requirements
- Android Studio

### How to

#### Edit App Icons
##### Generate different app icon sizes for all platforms
- Go to https://appicon.co/
- Drag & drop your chosen icon into the space
- Ensure only the `iPhone` & `Android` boxes are ticked
- Click `Generate`
- Extract all from the folder: `AppIcons` that has been generated
##### Replace default Flutter icon with your chosen icon
###### Android
- In `Android Studio`, Starting the root of your directory go to `android[name of your project]` > `app` > `src` > `main`, right click on `res`, and open it's file location
- Have `res`, and `AppIcons` directories open next to each other
- Open `res`, and delete all directories with `minimap` as their prefix
- In `AppIcons`, open `android` and move all directories with `minimap` as their prefix to the `res` directory
###### IOS
- In `Android Studio`, Starting the root of your directory go to `ios` > `runner`, right click on `Assets.xcassets`, and open it's file location
- Have `Runner`, and `AppIcons` directories open next to each other
- Delete the `Assets.xcassets` directory
- In `AppIcons`, Move the `Assets.xcassets` directory to the `Runner` directory
##### X
- In `Android Studio`, Right click on the root of the directory (this should also be the name of your application)
- Go to `Flutter` > `Open Android module in Android Studio` > `New window`
- Under `App`, right click `res`, and select `New` > `image Asset`
- Ensure you are on the `Foreground Layer` tab
- Now change `Source Asset` > `Path` to your chosen icon image (the icon image you used to generate the `AppIcons` directory on https://appicon.co/)
- [optional] Resize the image to perfectly fit in the circle, as this is how it will display across different platforms
- [optional] visit the `Background Layer` tab to change the background
- Click `Next`, `Finish`

### Known Issues

#### Andriod emulator is running but unable to locate it
- Open `Device manager`
- On the chosen emulator, click the drop down arrow on the right
- Click `Show on disk`
- Find the file named exactly: `hardware-qemu.ini.lock`, and delete it
- The emulator should now be shut down, and you can now relaunch it
