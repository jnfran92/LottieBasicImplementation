# LottieBasicImplementation
The simplest example of AirBnB Lottie library. Simple example showing a JSON file in an Android Activity (Batteries included).

<img src="https://media.giphy.com/media/2A4yGLexsUCE3lvBE2/giphy.gif" alt="">

## Requirements

- Android Studio
- After Effects
- Bodymovin (`extension`, the easiest way is getting it from Adobe Cloud Repository 
https://www.adobeexchange.com/creativecloud.details.12557.bodymovin.html).

## Steps

First, create an animation in **After Effects** (`SpeakLizTest1.aep`), in this case, we used a single `.png` 
file rotating (https://www.flaticon.com/free-icon/siren_1548321#term=siren&page=1&position=2). 

<img src="https://imgur.com/lpaMs6q.png" alt="">

After, using **Bodymovin** , export the necessary files (temporary name for this project: `anim1`) using the next puling's setup:

<img src="https://imgur.com/7Uyv9bx.png" alt="">

This creates a folder with the following files:

<img src="https://imgur.com/7uxeWsx.png" alt="">

A recent preview can be seen in `demo.html`. In Android, add the `images` folder to `assets`(Android), and `.json`
file in `raw` folder(Android). Lastly, in Android layout's activity add:

    <com.airbnb.lottie.LottieAnimationView
        android:id="@+id/animation_view"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"

        android:layout_marginStart="8dp"

        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginBottom="8dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:lottie_autoPlay="true"
        app:lottie_loop="true"
        app:lottie_imageAssetsFolder="images"
        app:lottie_rawRes="@raw/anim"
        />

The important thing is adding the **LottieAnimationView** and:

        app:lottie_imageAssetsFolder="images"
        app:lottie_rawRes="@raw/anim"


## Extra things

Lottie library version: 

    implementation 'com.airbnb.android:lottie:3.0.0'


Gradle settings

    android.useAndroidX=true
    android.enableJetifier=true
   
   
 
