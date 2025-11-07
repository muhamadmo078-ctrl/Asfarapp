Asfar App - Android Studio Project (Prototype WebView wrapper)
-------------------------------------------------------------
What this is:
- An Android Studio project that wraps the prototype HTML (assets/index.html) inside a WebView.
- This is a prototype-only wrapper (no server integration).

How to build an APK (step-by-step):
1. Install Android Studio on your PC (Windows/Mac/Linux).
2. Open Android Studio -> Choose 'Open an existing Android Studio project' and select this folder.
3. Android Studio will sync the Gradle files. If asked, install the suggested SDK components.
4. Once sync completes, go to 'Build' -> 'Build Bundle(s) / APK(s)' -> 'Build APK(s)'.
5. After the build finishes, click 'locate' to find the generated APK (usually in app/build/outputs/apk/debug/app-debug.apk).
6. Transfer the APK to your Android phone and install it (you may need to enable 'Install unknown apps' for your file manager).

Notes:
- If you prefer, I can provide a signed release APK, but that requires a keystore (private).
- I could also automate building via a CI service (GitHub Actions) if you want a hosted build.
- This project is set up with Kotlin and modern Gradle plugin versions; Android Studio 2022+ recommended.
