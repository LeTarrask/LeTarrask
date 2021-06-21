# Hacking with MacOS
Started on 17/06/2021 and added to the repo:
[github repo](https://github.com/LeTarrask/HackingWithSwift)

Just like the iOS version, there's a few projects that are exclusive for SwiftUI, and much more that use UIKit. I've started with SwiftUI, and will skip the same ones on the UIKit version.

***

## SwiftUI

## Project #1: Cows and Bulls
A simple game that uses a list and input, with a very simple game logic.

[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/MacOS_Projects/SwiftUI/01_Cows_and_bulls/Cows%20and%20Bulls)

### 1- Techniques:

- SwiftUI
- List
- Input
- window.title

### 2- Step-by-step:

Created a list, an input form, organized the UI, and did a few methods that make the game work.

### 3- Challenges:

The tutorial still used SwiftUI 1, which uses AppDelegate, so had to Google the updated solution, which is actually simpler. Added an animation when we add an input. Added onCommit to the textfield, so users can input pressing Enter. Also added some app info in the touchBar.

***

## Project #2: Odd One Out
A game to use more complex layout options for SwiftUI.

[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/MacOS_Projects/SwiftUI/02_Odd_One_Out/Odd%20One%20Out)

### 1- Techniques:

- SwiftUI
- VStacks, HStacks, ZStacks
- contextMenu
- basic game logic

### 2- Step-by-step:

Created the UI and a simple game logic, and there are not many differences from iOS, maybe a few issues with title and window, which are managed in AppDelegate in SwiftUI 1, and not in SwiftUI 2.

### 3- Challenges:

Created a special message when the user ran out of tries and loses the game.

***

## Project #3: Tailoring for macOS
A project to see what are the differences between iOS and macOS

[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/MacOS_Projects/SwiftUI/03_MacTechnique)

### 1- Techniques:

- NSWorkspace.shared.open(URL(string: "https://
www.apple.com")!) to open links in browser
- Other input options: Toggle, Button, Date Picker, Radio Group and Menus
- UX: hover, pressing delete and escape
- IBAction to create app menus (which will be deprecated in this SwiftUI app format)
- Create new windows

### 2- Step-by-step:

This tutorial is not an app, just several different techniques to create interfaces and react to users actions.

### 3- Challenges:

***

## UIKit

This book has several projects that are in the iOS book as well, and also has chapters about Swift, (types of data, loops, enums, etc) which are the same, so I won't be repeating them from the start. It could be interesting to get these XCode projects which I already did and make a MacOS version of them inside it, instead of creating a new one.

## Project #1: Storm Viewer

### 1- Techniques:

- NSViewController
- NSTableView
- NSImageView

### 2- Step-by-step:

The logic is almost the same as the previous Storm Viewer, and I didn't do the iOS UIKit version. The only thing that's new is drawing the app in UIKit for Mac, which is kind of slower and has more concepts we need to understand in order to make it work.

### 3- Challenges:

The challenge is to make a custom cell in the table view, which is very UIKit-y, and I'm going to lazy it out.

***

## Project #2: Cows and Bulls

There's a SwiftUI version, which I already finished. Skipping for now.

***

## Project #3: Social Media

This project is about adding social media sharing into the project #1. The adding of the button is very, very complex in storyboard. Left it in half.

***

## Project #4 - Grid Browser

There's a iOS version of it. Nothing new, I'd guess.

***

## Project #5 - Capital Cities

There's a iOS version of it. The only interesting thing here is MapKit.

***

## Project #6 - Auto Layout

Technique project. There's a iOS version of it, and it's for UIKit. SwiftUI is completely different. Skipping.

***

## Project #7 - Photo Memories

I've read the first part, that shows how to do a Collection View, and a Drag and Drop, which will be different in SwiftUI, and then the second part is very interesting, about using AVFoundation to generate a video, and which can be the solution for Felipe's Jiu Jitsu idea.

***

## Project #8 - Odd One Out

There's a SwiftUI version, which I already finished. Skipping for now.

***

## Project #9 - GCD

Technique project. This is not an interface project, so don't need to do it again. Just re-read. It's identical to iOS, and then, async/await will change everything.

***

## Project #10 - Weather Bar

This is an app that reads a JSON using CGD, and creates a Status Bar App. I did one (the lorem ipsum generator) a while ago, and JSON can be decoded better with Codable nowadays.

***

## Project #11 - Bubble Trouble

SpriteKit Project, first one for Mac OS. I'll do it because it will be my first step into Mac OS Games. :)

### 1- Techniques:

- SKTexture
- SKSpriteNode
- Tracking mouse action

### 2- Step-by-step:

It's a simple element creation game, which has one simple interaction. It was an introduction to making the game in SpriteKit in Mac OS, which was neat.

### 3- Challenges

The challenges are adding other game stuff, like alerts for gameovers, invalidating the timer, etc.

***

## Project #12 - Animation

UIKit Mac Os animation is being skipped for this time.

***

## Project #13 - Screenable

Longest project of the book. It's a document based project, which is very useful for MacOS.

### 1- Techniques:

- Document-based app

### 2- Step-by-step:

***

## Project #14 - Shooting Gallery

Second game. Animations, new levels and custom mouse cursor.
It was a quick and interesting project, to make a shooter. In the end, SpriteKit is mostly a matter of game organization, and conquering and dividing. And it has little to nothing that's specifically for Cocoa or Mac OS, except the cursor part.

***

## Project #15 - Undo Manager

Adds undo functionality to Screenable.

***

## Project #16 - Bookworm

This project is to teach the Bindigns technique. It's basically a Storyboards thing.

***

## Project #17 - Match Three

Build a ball-matching game with SpriteKit, while learning about shape nodes and particle emitters. This was another fun game that could work in any other platform, since it's about SpriteKit capabilities. The game can be super tuned and changed into something else.

***

## Project #18 - Bindings

Another bindings technique project, that uses KVC and KVO.

