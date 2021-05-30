# xcode_tips

# Xcode line duplicate

#### Bind keys to duplicate lines in Xcode

1. Open below directory in Finder with <kbd>Cmnd</kbd> + <kbd>Shift</kbd> + <kbd>G</kbd>

```
/Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Versions/A/Resources/
```

2. Open `IDETextKeyBindingSet.plist` with a text editor.


3. Add this in:

```xml
<key>Duplication</key>
<dict>
    <key>Duplicate Current Line</key>
    <string>moveToBeginningOfLine:, deleteToEndOfLine:, yank:, insertNewline:, moveToBeginningOfLine:, yank:</string>
    <key>Duplicate Lines</key>
    <string>selectLine:, copy:, moveToEndOfLine:, insertNewline:, paste:, deleteBackward:</string>
    <key>Delete Line</key>
    <string>selectLine:, deleteBackward:</string>
</dict>
```

4. Open Xcode and go to `Xcode preferences` -> `Key Bindings` -> `Text tab` -> Scroll till you see `Duplication`


5. Click on `Duplicate Current Line`, add a shortcut for it, eg. `Cmd + D` (remove any other bindings for this key)
