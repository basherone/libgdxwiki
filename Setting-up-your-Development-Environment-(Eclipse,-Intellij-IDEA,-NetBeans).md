Libgdx projects use [Gradle](http://www.gradle.org/) to manage dependencies, the build process, and IDE integration. This allows you to develop your app with whatever development environment you prefer. Best of all: your team mates can use a different dev environment while working on the same project! Just don't commit your IDE specific files to your source control. The `.gitignore` file contained in libgdx projects will take care of that if you use Git.

### Setup for iOS development
Regardless of your development environment of choice, here's what you'll need for iOS:

  * A Mac with Mac OS X and Xcode 7
  * An [Apple developer account](https://developer.apple.com/membercenter/index.action) if you want to test on device or deploy to the App Store. Please direct all hatred towards Apple.
  * [A free RoboVM license](http://www.badlogicgames.com/wordpress/?p=3762)
     * [Sign-up for a RoboVM trial key](https://account.robovm.com/#/register)
     * Activate your trial key (see below)
     * [Apply for the free indie program](https://docs.google.com/forms/d/1wbne7JNXDz4ea2I6GFfIIyjHyHofaKLvCwYiqboBpKw)

The RoboVM trial key will be valid for 30 days, so you can start developing immediately. Once you applied for the free indie program, your trial key will be upgraded to a full indie license within 30 days. You will receive an e-mail once that happens.

With your RoboVM indie key you can develop as many games as you want, commercial and non-commercial. The key will be valid [forever](http://www.gamefromscratch.com/image.axd?picture=image_thumb_2403.png). If you are a team, just have everyone sign up for a key separately. If your indie team is larger than 3 devs, contact [hello@robovm.com](mailto:hello@robovm.com). RoboVM just wants to check that you aren't a AAA studio trying to exploit the indie program. Those AAA studios will have to pay for a license, indie teams of any size get licenses for free.

Depending on your development environment, you can activate the key as outlined below. **Note:** you can only activate your license key on Mac OS X, just like you can only compile for iOS on Mac OS X.

**Gradle**
In your project's root directory, execute the following in the terminal:

```
./gradlew :activateLicense -Probovm.licenseKey=your-key-here
```

**Eclipse**
After installing the [RoboVM Eclipse plugin](http://docs.robovm.com/getting-started/eclipse.html), go to `RoboVM -> License Manager` and enter your key.

**IntelliJ IDEA/Android Studio**
After installing the [RoboVM IDEA plugin](http://docs.robovm.com/getting-started/intellij.html), go to `RoboVM -> License Manager` and enter your key.

### Setting up Eclipse 
To develop your application via Eclipse, you need to install the following pieces of software.

  * [Java Development Kit 7+ (JDK) (6 will not work!)](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
  * [Eclipse](http://www.eclipse.org/downloads/), the "Eclipse IDE for Java Developers" is usually sufficient.
  * [Android SDK](http://developer.android.com/sdk/installing.html), you only need the SDK, not the ADT bundle, which includes Eclipse. Install the latest stable platforms via the SDK Manager.
  * [Android Development Tools for Eclipse](http://developer.android.com/tools/sdk/eclipse-adt.html), aka ADT Plugin. Use this update site: https://dl-ssl.google.com/android/eclipse/
  * [Eclipse Integration Gradle](https://github.com/spring-projects/eclipse-integration-gradle/), use this update site: http://dist.springsource.com/snapshot/TOOLS/gradle/nightly (for Eclipse 4.4) or http://dist.springsource.com/release/TOOLS/gradle (for Eclipse < 4.4)

To additionally target iOS

  * A Mac, iOS Development does not work on Windows/Linux thanks to Apple.
  * The latest XCode, which you can get from the Mac OS X App Store for free
  * [RoboVM Eclipse plugin](http://docs.robovm.com/getting-started/eclipse.html), simply install the Eclipse plugin. Make sure to update the plugin frequently!


Once all of these tools are installed, proceed to [[creating your project|Project Setup Gradle]]

### Setting up Intellij IDEA
To develop your application via Intellij IDEA, you need to install the following pieces of software.

  * [Java Development Kit 7+ (JDK) (6 will not work!)](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
  * [Intellij IDEA 14.+](http://www.jetbrains.com/idea/download/), the Community edition is sufficient. Warning: the newly released IntelliJ 15.0.0 has blocking issues regarding Gradle Android projects (see this [forum topic](http://www.badlogicgames.com/forum/viewtopic.php?f=11&t=20987) for more information), if you want to develop for Android it is recommended to use the previous 14.1.5 version for now.
  * [Android SDK](http://developer.android.com/sdk/installing.html), you only need the SDK, not the ADT bundle, which includes Eclipse. Install the latest stable platform via the [SDK Manager](http://developer.android.com/tools/help/sdk-manager.html). You also have to create an environment variable called ANDROID_HOME, which points at your Android SDK installation directory!

To additionally target iOS

  * A Mac, iOS Development does not work on Windows/Linux thanks to Apple.
  * The latest XCode, which you can get from the Mac OS X App Store for free
  * [RoboVM IntelliJ IDEA/Android Studio plugin](http://docs.robovm.com/getting-started/intellij.html)

Once all of these tools are installed, proceed to [[creating your project|Project Setup Gradle]]

### Setting up Android Studio
To develop your application via Android Studio, you need to install the following pieces of software.

  * [Java Development Kit 7+ (JDK) (6 will not work!)](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
  * [Android Studio] (https://developer.android.com/sdk/index.html) Android Studio already comes packaged with the Android SDK so contrary to Eclipse or Intellij IDEA you do not need to install this component.

Here is a good [tutorial](http://www.todroid.com/android-gdx-game-creation-part-i-setting-up-up-android-studio-for-creating-games/) on how to install libGDX using a tool provided by Bad Logic.


To additionally target iOS

  * A Mac, iOS Development does not work on Windows/Linux thanks to Apple.
  * The latest XCode, which you can get from the Mac OS X App Store for free
  * [RoboVM IntelliJ IDEA/Android Studio plugin](http://docs.robovm.com/getting-started/intellij.html)

Once all of these tools are installed, proceed to [[creating your project|Project Setup Gradle]]


### Setting up NetBeans
To develop your application via NetBeans, you need to install the following pieces of software.

  * [Java Development Kit 7+ (JDK) (6 will not work!)](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
  * [NetBeans 7.3+](https://netbeans.org/downloads/), the "Java SE" is sufficient
  * [Android SDK](http://developer.android.com/sdk/installing.html), you only need the SDK, not the ADT bundle, which includes Eclipse. Install the latest stable platform via the SDK Manager. You also have to create an environment variable called ANDROID_HOME, which points at your Android SDK installation directory!
  * [NBAndroid](http://www.nbandroid.org), use this update center: http://nbandroid.org/updates/updates.xml
  * [Gradle Support for NetBeans](https://github.com/kelemen/netbeans-gradle-project), use the NetBeans IDE Update Center.

To additionally target iOS

  * A Mac, iOS Development does not work on Windows/Linux thanks to Apple.
  * The latest XCode, which you can get from the Mac OS X App Store for free

Once all of these tools are installed, proceed to [[creating your project|Project Setup Gradle]]