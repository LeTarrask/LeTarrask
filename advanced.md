# Advanced Swift
Started on 16/06/2021 and added to the repo:
[github repo](https://github.com/LeTarrask/HackingWithSwift)

***

## Project #1: Happy Days
A memory recording project that uses AVAudio and ImagePicker for UIKit, but I'm doing it for SwiftUI for a better challenge

[repo]()

### 1- Techniques:

- SwiftUI
- Permissions
- Image Picker (actually reused some code from an older project)
- AVFoundation
- Speech (to transcribe the text)

### 2- Step-by-step:

Started trying to do UIKit, but then found it was too much of a hassle to redraw screen and navigation, so I decided to just copy the functionality for SwiftUI. Added image picker, created a sheet to ask for Permissions. Added an ObservableObject to be the storage-controller. Added the transcription into the Model, which I created. It also plays the audio recorded on the memory.

Could do:
- Test for bugs
- Interface that looks cooler, improve functionality. Basic stuff is all there.
- Store memory names.
- Implement Core Spotlight search, which I'm not using because of interface.

### 3- Challenges:

Fix a bug in Core Spotlight and add alternate transcription options, since it's a new Apple feature that's prone to incorrect transcriptions.

***
