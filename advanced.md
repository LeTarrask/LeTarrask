# Advanced Swift
Started on 16/06/2021 and added to the repo:
[github repo](https://github.com/LeTarrask/HackingWithSwift)

***

## Project #1: Happy Days
A memory recording project that uses AVAudio and ImagePicker for UIKit, but I'm doing it for SwiftUI for a better challenge

[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Advanced_Swift_Projects/One/01_Happy_Days)

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

## Project #2: TimeShare

This is a Messages extension app. First we used storyboards (I'm not hating it anymore). And then started coding. It's kinda strange, and couldn't make it run on Simulator. There's some weird bug here.

[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Advanced_Swift_Projects/One/02_TimeShare)

### 1- Techniques:

- Storyboard
- Messages

***

## Project #3: ChooseCruise

This is a SiriKit app, so creating the project is already different.

[repo]()

### 1- Techniques:

- Intent Handler
- INRidesharingDomainHandling (deprecated)
- Adding this Intent Handler thing into Maps
- Adding SiriKit

### 2- Step-by-step:

First thing is thata INRidesharingDomainHandling is already deprecated, so this tutorial is kinda old. The techniques in this book are all to be handled with care. We simply had to conform to the protocols in the RidesharingDomainHandling, to allow maps to book a car ride, and then conform to a few SiriKit protocols to allow Siri to work her magic. The technique is quite simple, but using it for other projects will require using something completely different. Paul's words: "The current implementation of Siri is limited to only a handful of app types, which is going to keep the vast majority of app developers away. However, Apple have a long history of working incrementally: developing a new feature that’s somewhat limited, then expanding it over time based on feedback."

***

## Project #4: Polyglot

This is an Extension app that shows a word in two languages on the lock screen.

[repo]()

### 1- Techniques:

- Extensions
- 

### 2- Step-by-step:

Doing it in SwiftUI. Got into a debugging stupidity because I didn't declare words as Published. It uses Alert to get input text fields, but I'd rather do it in a SwiftUI sheet. Finished a basic UI that's similar to the UIKit tutorial version. Now to the Extension. There's no Today extension in current XCode, so I created a Widget target, hoping it works. It doesn't. Template code is broken.

