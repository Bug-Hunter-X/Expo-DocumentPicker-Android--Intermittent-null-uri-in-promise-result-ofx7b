# Expo DocumentPicker Android: Intermittent null `uri` issue

This repository demonstrates a bug in Expo's DocumentPicker library on Android.  Occasionally, after a file is successfully selected using `DocumentPicker.getDocumentAsync()`, the returned promise resolves with a `uri` property that is null. This prevents access to the selected file.

## Steps to Reproduce

1. Run the provided `bug.js` example on an Android device or emulator.
2. Select a file using the DocumentPicker.
3. Observe that the `uri` is sometimes null, leading to errors.

## Solution

The `bugSolution.js` file provides a potential workaround to address the inconsistent `uri` behavior.  It incorporates additional error handling to gracefully handle the cases where the `uri` is unexpectedly null.  It's recommended to implement robust error handling for such scenarios in your applications to avoid app crashes and enhance user experience.