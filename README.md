# Shared Library Downloader for Plex - Safari

Based on [jkingsman's extension](https://github.com/jkingsman/plex-shared-library-downloader).

## How to use

### Requirements

**iOS**: iOS/iPadOS 15+  
_AND_  
**macOS**: macOS 11+ with Xcode 13+

### Installation (macOS)

- Clone this project and its submodules (`git clone --recurse-submodules <this-repo-url>`)
- Open it in Xcode
- Select scheme `Shared Library Downloader for Plex (macOS) > My Mac`
- Run it

First run only:
- Follow instructions in Note below
- Click on the in-app button
- Enable the extension an allow it wherever it's needed

**Note:** You need to enable local extensions in Safari each time you open it. To do so:
- In Safari, go to `Safari > Settings` then `Advanced > Show Development menu in menu bar`
- Then close settings and go to `Development > Allow unsigned extensions` (last item)

### Troubleshooot

Safari might be sometimes capricious and might not show the extension sometimes. If you've followed each step above **CAREFULLY** and it still doesn't show up, try this:

```sh
PATH=/System/Library/Frameworks/CoreServices.framework/Frameworks/LaunchServices.framework/Support:"$PATH" lsregister -f /Applications/Safari.app
```

(Credit to [this post](https://developer.apple.com/forums/thread/668416?answerId=669526022#669526022))
