# xcode-key-bindings

Since Xcode has to be one of the worst IDE's out there, it comes as no surprise even setting custom key bindings requires some extra work.

#### Here's how I've done it
1. Open up ```/Applications/Xcode-Beta.app/Contents/Frameworks/IDEKit.framework/Resources/IDETextKeyBindingSet.plist``` in a text editor
2. Paste this to the end of the file (or any other custom commands you want)
```
<key>Custom</key>
<dict>
    <key>Cut Current Line</key>
    <string>selectLine:, copy:, deleteBackward:</string>
    <key>Insert and Move to New Line Below</key>
    <string>moveToEndOfLine:, insertNewline:</string>
    <key>Duplicate Current Line</key>
    <string>moveToBeginningOfLine:, deleteToEndOfLine:, yank:, insertNewline:, moveToBeginningOfLine:, yank:</string>
</dict>
```
3. <b>Restart</b> Xcode
4. Inside Xcode go to `Preferences` -> `Key Bindings` and search for `Cut Current Line` (or any other key you added previously)
5. Add the desired shortcut (`Ctrl X` in my case)
