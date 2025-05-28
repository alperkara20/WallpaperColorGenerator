# WallpaperColorGenerator

Generate all the solid color wallpapers from macOS (including Muted versions) right on your iPhone, and automate wallpaper shuffling using Shortcuts!

---

## Features

- 📱 Save exact macOS solid color and muted wallpapers to your Photos with one tap.
- 🎨 Includes all 12 standard macOS colors and their Muted versions (for a total of 23 wallpapers).
- 🔄 Easily set up an iOS Shortcuts automation to shuffle between these wallpapers on a schedule.

---

## How to Build & Run

1. **Clone this repo** or copy the source files into a new Xcode SwiftUI project.

2. **Update `Info.plist`:**  
   Add the following two keys so the app can save to your Photos:
   - `NSPhotoLibraryUsageDescription` (String)  
     _e.g.:_  
     `"This app saves wallpapers to your photo library so you can use them as backgrounds."`
   - `NSPhotoLibraryAddUsageDescription` (String)  
     _e.g.:_  
     `"This app saves wallpapers to your photo library."`

3. **Check your screen resolution**  
   In `ContentView.swift`, edit this line if needed:
   ```swift
   let wallpaperSize = CGSize(width: 1290, height: 2796) // e.g., iPhone 14 Pro Max
[Find your iPhone’s exact wallpaper size here.](https://www.ios-resolution.com/)

4. **Build & run on your iPhone**
   - The app will ask for permission to add to your Photos.
   - Tap any color to save a wallpaper-sized image to your Photos library.

---

## How to Shuffle Wallpapers Automatically

1. **Open the Shortcuts app on your iPhone.**
2. **Create a new Personal Automation:**
   - **Trigger:** Time of Day (e.g., every hour or day)
   - **Actions:**
     1. **Find Photos** (filter by Album: move your solid wallpapers to a dedicated album like “Solid Wallpapers”)
     2. **Get Random Item** (from the Find Photos list)
     3. **Set Wallpaper** (choose Lock Screen, Home Screen, or both)
   - On **iOS 17.2+**, you can turn off “Ask Before Running” for true automation.
   - On **iOS 16–17.1**, you’ll get a notification and need to tap it to confirm the wallpaper change.

---

## Credits

- Color HEX codes taken directly from macOS Ventura/Sonoma solid wallpapers.
- Muted versions generated to match macOS’s palette by lowering saturation and increasing brightness.
- Inspired by macOS and iOS built-in wallpaper shuffling.

---

## License

MIT License (feel free to use/modify/share!)
