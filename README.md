# NostalMovieMaker (stage 1)

A simple native Android video editor inspired by classic storyboard-style movie makers.
Kotlin, Jetpack Compose, and Media3 (ExoPlayer for preview, Transformer for export).

## What works in stage 1
- Import one or more videos with the system photo picker
- Storyboard strip: tap a clip to select it, move it earlier or later, or remove it
- Trim each clip with a range slider (minimum length 0.5 s)
- Preview the whole storyboard in order, with trims applied
- Publish to an H.264/AAC MP4 saved in Movies/NostalMovieMaker

## Getting the APK

### Option A: Android Studio (about 5 minutes)
1. Open this folder in Android Studio (Koala or newer) and let Gradle sync.
2. Menu: Build > Build Bundle(s) / APK(s) > Build APK(s).
3. Click "locate" in the popup. The file is app/build/outputs/apk/debug/app-debug.apk.
4. Copy it to your phone and open it. Android will ask you to allow installs from that source.

### Option B: GitHub Actions (no Android Studio needed)
1. Create a new GitHub repository and upload everything in this folder, including the
   hidden .github folder.
2. Open the repository's Actions tab, pick "Build APK" and press "Run workflow"
   (it also runs on every push to main).
3. When it finishes, open the run and download the "NostalMovieMaker-debug-apk" artifact.
   Unzip it to get app-debug.apk.

The debug APK is signed with the standard Android debug key, so it installs normally on
any phone with Android 10 (API 29) or newer. It is fine for personal use, but it isn't a
release build for the Play Store.

## Planned next
- Stage 2: fade and crossfade transitions, split at playhead
- Stage 3: effects (sepia, black and white, brightness), title text, music track

If a build fails, send the error text and it can be fixed from there.
