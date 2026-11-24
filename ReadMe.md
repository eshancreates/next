# NEXT

Notch app for macOS (fork of Atoll / boring.notch, GPL-3.0).

## Install (build from source)
Requirements: macOS 14+, a notch MacBook, Xcode 15+ (free from the App Store).

1. `cd` into this folder and run `open DynamicIsland.xcodeproj`
2. Wait for Xcode to resolve Swift packages (first time takes a few minutes).
3. Click the project (blue icon) > target **DynamicIsland** > *Signing & Capabilities*:
   pick your Apple ID under **Team** (free account works) and let it auto-sign.
4. Select **My Mac** as the destination and press **⌘R**.
5. To install permanently: Product > Show Build Folder in Finder > Products > Debug (or Release),
   drag **NEXT.app** into **/Applications**.
6. First launch: right-click NEXT.app > Open if macOS blocks it, then grant permissions
   (Accessibility, Calendar, Screen Recording, Music...) and relaunch after granting.

Terminal alternative:
    xcodebuild -project DynamicIsland.xcodeproj -scheme DynamicIsland -configuration Release \
      -derivedDataPath build CODE_SIGN_IDENTITY="-" build
    cp -R build/Build/Products/Release/NEXT.app /Applications/
