# Notes

## Installing React Native

1. npx react-native@latest init GalleryApp
2. Error with Ruby verions on my OS.

```
✔ Downloading template
✔ Copying template
✔ Processing template
✔ Installing Ruby Gems
ℹ Installing Ruby Gems
✖ Installing CocoaPods
error
✖ Installing CocoaPods
error An error occured while trying to install CocoaPods, which is required by this template.
Please try again manually: sudo gem install cocoapods.
```
4. Tried to install CocoaPods manually with `sudo gem install cocoapods` but I
   got an error.

```
Password:
ERROR:  Error installing cocoapods:
	There are no versions of cocoapods-downloader (>= 2.0) compatible with your Ruby & RubyGems. Maybe try installing an older version of the gem you're looking for?
	cocoapods-downloader requires Ruby version >= 2.7.4. The current ruby version is 2.6.10.210.
```

5. Needed to add the following to may .zshrc

```
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
export LDFLAGS="-L/opt/homebrew/opt/ruby/lib"
export CPPFLAGS="-I/opt/homebrew/opt/ruby/include"
export PKG_CONFIG_PATH="/opt/homebrew/opt/ruby/lib/pkgconfig"
```