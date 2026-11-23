# পকেটকাট স্টুডিও (PocketCut Studio v1.1) 🎬📱🎵🎙️
**অল-ইন-ওয়ান মাল্টি-ক্লিপ, মিউজিক ও ভয়েসওভার Reels / TikTok মোবাইল ভিডিও এডিটর (Flutter — Android & iOS)**  
**ভাষা সাপোর্ট:** বাংলা + English (অ্যাপের ভেতরেই এক ট্যাপে পরিবর্তনযোগ্য)

---

## ✨ প্রধান ফিচারসমূহ (Key Features)

1. **মাল্টি-ক্লিপ জোড়া লাগানো ও প্রতিটি ক্লিপ আলাদা ট্রিম (Multi-Clip Merge & Trim):**
   - গ্যালারি থেকে একসাথে একাধিক ভিডিও ক্লিপ নিয়ে জোড়া লাগানো (`concat`) এবং এডিটরের ভেতর থেকেও নতুন ক্লিপ (`+ ক্লিপ যোগ`) যুক্ত করা যায়।
   - ক্লিপগুলোর ক্রম (বামে `◀` / ডানে `▶`) পরিবর্তন, যেকোনো ক্লিপ ডিলিট এবং প্রতিটি ক্লিপ আলাদাভাবে শুরু ও শেষ অংশ ট্রিম (`RangeSlider`) করার সুবিধা।
   - কোনো ক্লিপে অডিও না থাকলেও স্বয়ংক্রিয়ভাবে সাইলেন্স স্ট্রিম (`anullsrc`) তৈরি করে নিখুঁতভাবে জোড়া দেয়—ফলে এক্সপোর্টে কখনোই ক্র্যাশ হয় না।
2. **ব্যাকগ্রাউন্ড মিউজিক যোগ ও ৩-চ্যানেল অডিও মিক্সার (Background Music & Mixer):**
   - ফোন থেকে যেকোনো **MP3 / M4A / WAV** গান বা ব্যাকগ্রাউন্ড মিউজিক যোগ করা যায় (`file_picker`)।
   - গানটি ভিডিওর দৈর্ঘ্য অনুযায়ী স্বয়ংক্রিয়ভাবে লুপ (`-stream_loop -1`) ও ট্রিম হয়।
   - আলাদা ভলিউম স্লাইডার দিয়ে **ভিডিওর আসল সাউন্ড** এবং **ব্যাকগ্রাউন্ড মিউজিক ভলিউম** নিখুঁতভাবে ব্যালেন্স করা যায়।
3. **সরাসরি ভয়েসওভার রেকর্ডিং (Live Microphone Voiceover Dubbing):**
   - এডিটরের **🎙️ ভয়েসওভার রেকর্ড** ট্যাব থেকে ভিডিও চালিয়ে দেখার সাথে সাথেই মাইক্রোফোনে ভয়েসওভার রেকর্ড (`.m4a` AAC) করা যায় (`record` প্লাগইন)।
   - টাইমলাইনের যে পজিশন থেকে রেকর্ড শুরু করবেন, ঠিক সেই সময় (`adelay`) থেকেই ভয়েসওভার সিঙ্ক হয়।
   - ভয়েসওভার প্রিভিউ শোনা, ডিলিট/পুনরায় রেকর্ড এবং ভলিউম বুস্ট (`0%–150%`) করার সুবিধা।
4. **৯:১৬ Reels / TikTok সহ মাল্টি-রেশিও ক্যানভাস (Aspect Ratios):**
   - **9:16** (1080×1920 — Reels, TikTok, Shorts), **4:5**, **1:1** এবং **16:9** (YouTube)।
5. **সিনেমাটিক ফিল্টার ও কালার অ্যাডজাস্টমেন্ট:**
   - ৮টি প্রিসেট ফিল্টার (*আসল, উজ্জ্বল, সিনেমা, গোধূলি, শীতল নীল, ভিন্টেজ, সাদাকালো, নিয়ন পপ*) + ম্যানুয়াল **Brightness, Contrast, Saturation** স্লাইডার।
6. **ভাঙনহীন বাংলা টেক্সট ও স্টিকার ওভারলে:**
   - বাংলা বা ইংরেজি টেক্সট ও ১৬টি ইমোজি স্টিকার আঙুল দিয়ে টেনে ভিডিওর ওপর বসানো যায়।
   - `RepaintBoundary` PNG ওভারলে প্রযুক্তির কারণে মোবাইলে বাংলা যুক্তাক্ষর ১০০% নিখুঁতভাবে রেন্ডার হয়।
7. **স্পিড কন্ট্রোল (0.5x Slow-Mo থেকে 2.0x Fast) ও 1080p Full HD এক্সপোর্ট:**
   - গ্যালারির `PocketCut` অ্যালবামে স্বয়ংক্রিয় সেভ (`gal`) এবং সরাসরি Reels / TikTok / WhatsApp-এ শেয়ার (`share_plus`)।

---

## 📂 প্রজেক্ট ফোল্ডার স্ট্রাকচার (Project Structure)

```text
pocketcut_flutter/
├── pubspec.yaml                       # Flutter প্যাকেজসমূহ (FFmpegKit, FilePicker, AudioPlayers, Record, Gal)
├── analysis_options.yaml              # Dart লিন্ট কনফিগারেশন
├── .github/workflows/build_apk.yml    # পিসি ছাড়াই ফ্রি ক্লাউড APK বিল্ডার (GitHub Actions)
├── android/app/src/main/
│   └── AndroidManifest.xml            # ভিডিও, অডিও (BGM), ক্যামেরা ও মাইক্রোফোন পারমিশন
├── ios/Runner/
│   └── Info.plist                     # iOS Photo Library, Camera ও Microphone পারমিশন
├── lib/
│   ├── main.dart                      # অ্যাপ এন্ট্রি পয়েন্ট ও ডার্ক Material 3 থিম
│   ├── l10n/
│   │   └── app_strings.dart           # সম্পূর্ণ বাংলা + English ভাষার ডিকশনারি
│   ├── models/
│   │   ├── video_clip_item.dart       # মাল্টি-ক্লিপ আইটেম ও আলাদা ট্রিম মডেল
│   │   ├── editor_project.dart        # মাল্টি-ক্লিপ concat, BGM ও Voiceover amix FFmpeg জেনারেটর
│   │   ├── video_filter_preset.dart   # ৮টি ফিল্টারের ColorMatrix ও FFmpeg eq/colorbalance
│   │   └── overlay_item.dart          # ড্র্যাগেবল টেক্সট ও স্টিকার মডেল
│   ├── services/
│   │   └── video_export_service.dart  # মাল্টি-ক্লিপ অডিও প্রোবিং + PNG ক্যাপচার + FFmpeg রেন্ডার
│   ├── screens/
│   │   ├── home_screen.dart           # একক ও মাল্টি-ক্লিপ প্রজেক্ট শুরু করার হোম স্ক্রিন
│   │   └── editor_screen.dart         # ৭-ট্যাব অল-ইন-ওয়ান Reels ভিডিও ও অডিও এডিটর
│   └── widgets/
│       ├── export_modal.dart          # 720p/1080p এক্সপোর্ট প্রগ্রেস ও শেয়ার শিট
│       └── text_editor_dialog.dart    # বাংলা/ইংরেজি টেক্সট স্টাইলিং ডায়ালগ
└── test/
    └── editor_project_test.dart       # মাল্টি-ক্লিপ, BGM, Voiceover adelay/amix ও ভাষা ইউনিট টেস্ট
```

---

## 🚀 কীভাবে মোবাইলের জন্য APK তৈরি ও ইনস্টল করবেন?

### পদ্ধতি ১: পিসি ছাড়াই শুধুমাত্র মোবাইল ফোন থেকে ফ্রি APK তৈরি (GitHub Actions)
1. GitHub-এ একটি নতুন রিপোজিটরি খুলে এই `pocketcut_flutter` ফোল্ডারের সব ফাইল আপলোড করুন।
2. রিপোজিটরির **Actions** ট্যাবে যান — **"Build PocketCut Android APK"** ওয়ার্কফ্লো স্বয়ংক্রিয়ভাবে চালু হয়ে আপনার জন্য রেডি `.apk` তৈরি করে দেবে।
3. **Artifacts** থেকে `PocketCut-Android-APK` ডাউনলোড করে ফোনে ইনস্টল করুন!

### পদ্ধতি ২: কম্পিউটারে Flutter SDK দিয়ে রান ও APK বিল্ড
```bash
cd pocketcut_flutter
cp android/app/src/main/AndroidManifest.xml /tmp/AndroidManifest.xml
cp ios/Runner/Info.plist /tmp/Info.plist
flutter create . --platforms=android,ios --org com.pocketcut.editor --project-name pocketcut_editor
cp /tmp/AndroidManifest.xml android/app/src/main/AndroidManifest.xml
cp /tmp/Info.plist ios/Runner/Info.plist
# android/app/build.gradle(.kts)-এ minSdk = 24 নিশ্চিত করুন
flutter pub get
flutter build apk --release --split-per-abi
```
