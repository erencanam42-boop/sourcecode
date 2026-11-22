# AgasMo — "Aga sa Gamot Mo"

> *"HOOT-HOOT!! You must take your pill!"*

**AgasMo** is a warm, playful, 100% offline Android medicine reminder app built with **Kotlin**, **Jetpack Compose**, and **Material 3**. Designed with big, rounded, easy-to-read typography for **Lola & Lolo** as well as younger users, AgasMo replaces boring hospital-style trackers with cute talking animal companions, 5 Philippine & international languages, and reliable background alarms.

---

## Author
- **Name:** Caman, Rene W.
- **Section:** BS-INTE 2A

---

## Key Features
- **5 Supported Languages (Instant Switch, No Restart):**
  - Tagalog (Default), English, Taglish, Bisaya / Cebuano, and Ilocano (Bambang, Cagayan Valley).
  - Translates all screens, notifications, and companion voice alerts instantly.
- **5 Cute Talking Companions (Unique Voices & Personalities):**
  - **Lumi the Owl** (Purple, Makulit & Bubbly Owl)
  - **Bram the Bear** (Brown, Cuddly Gentle Bear — great for Lola/Lolo)
  - **Mimi the Cat** (Pink, Super Cute Kitty)
  - **Kiko the Dog** (Orange, Bouncy Hyper Pup)
  - **Tala the Fox** (Teal, Chill & Cool Fox)
- **100% Working Offline Notification & Alarm System:**
  - Exact alarms via `AlarmManager.setExactAndAllowWhileIdle()`, paired with a `WorkManager` backup worker and `BootReceiver` so alarms survive app closure, battery saver, and device restarts.
  - Lock-screen high-priority notifications with **Take Now / Inumin Na**, **Snooze 10m**, and **Skip / Laktawan** actions.
  - **MAX SHOUT** escalation repeats every 10 minutes if a dose goes untaken after 30 minutes.
  - **TextToSpeech** companion voice playback (`VoiceAlertService` + WakeLock).
- **Complete Daily Tracking & History:**
  - **Today / Home:** Next Medicine countdown hero card, search bar, progress bar, mood-aware companion avatar, notification-off warning banner, and 2-hour late emergency SMS alert shortcut.
  - **Add / Edit Medicine:** Multiple daily times with Material 3 Time Picker, frequency, duration, color, optional photo via Android Photo Picker, and MAX SHOUT toggle.
  - **History & Streak:** Interactive monthly calendar, streak counter, weekly adherence %, and **Export to Doctor** share report.
  - **Companion Mood & Badges:** Animated companion with Happy/Angry/Sleepy moods and achievement badges.
  - **Clean Expandable Profile & Settings:** Accordion-style expandable sections for Language, Companion, Notifications & Battery Saver, Theme (Pink / Light / Dark), and Emergency Contact.

---

## Tech Stack
- **Language:** Kotlin
- **UI:** Jetpack Compose, Material Design 3, Fredoka & Nunito Fonts
- **Local Persistence:** Room Database + Preferences DataStore (100% offline)
- **Background & Alarms:** AlarmManager, BroadcastReceivers, WorkManager, Foreground Service (`mediaPlayback`), TextToSpeech
- **Media:** Coil + Android Photo Picker (`PickVisualMedia`)

---

## How to Install & Run (Android Studio)
1. **Requirements:**
   - Android Studio (Ladybug / Meerkat or newer) with JDK 11+
   - Android SDK 36 (minimum supported device: Android 7.0+ / recommended Android 10+)
2. **Open the Project:**
   - Launch **Android Studio** → **Open** → select the `AgasMo` project folder.
   - Wait for Gradle Sync to finish automatically.
3. **Run on Emulator or Physical Device:**
   - Connect an Android phone (with USB Debugging enabled) or start an Android Emulator (API 29+ recommended).
   - Click **Run ▶** (`app` configuration).
4. **Permissions on First Launch:**
   - Choose your preferred **Language** and **Companion** during onboarding.
   - Allow **Notifications** when prompted by your companion so reminders, sounds, and voice alerts work properly.
   - *(Optional, recommended on physical phones)* In **Profile → Notifications**, tap **Ignore Battery Optimization** so aggressive phone battery savers do not delay background alarms.
5. **Run Unit Tests (Optional):**
   - Run `./gradlew :app:testDebugUnitTest` (or `gradle :app:testDebugUnitTest`) in the Android Studio terminal.
