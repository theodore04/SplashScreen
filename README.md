# SplashScreen
SplashScreen Animation

1. Pembuatan Projek
Buat projeknya terlebih dahulu

2. Copy logo ke drawable
Silakan pilih untuk logonya dan disimpan ke folder drawable

3. Tambahkan implementation splashscreen pada build.gradle.kts (Module:app)
Setelah ditambahkan jangan lupa dilakukan sync

// Splashscreen Implementation
implementation("androidx.core:core-splashscreen:1.0.1")

4. Tambahkan color (bebas pilihannya pada values/color)

<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
    <color name="green">#4CAF50</color> // Custom warna pilihan Anda
</resources>

5. Tambahan theme khusus untuk style splashscreen

  // sesuaikan ya namenya, dibuat "app" agar lebih mudah saja
    <style name="Theme.App.SplashScreen" parent="Theme.SplashScreen">
        <item name="windowSplashScreenAnimatedIcon">@drawable/codestrokelogo</item> // Ini untuk logonya
        <item name="windowSplashScreenBackground">@color/green</item> // Ini untuk background splashscreennya
        <item name="postSplashScreenTheme">@style/Theme.SplashScreen</item> // ini untuk style atau theme setelah splashscreen
    </style>

6. Tambahkan keterangan themenya pada android manifest

// Tambahkan ini pada android manifest
   android:theme="@style/Theme.App.SplashScreen"

// Contohnya
        <activity
            android:name=".MainActivity"
            android:theme="@style/Theme.App.SplashScreen"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>

  
