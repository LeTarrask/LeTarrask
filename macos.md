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

[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/MacOS_Projects/SwiftUI/02_Odd_One_Out/Odd%20One%20Out)

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

## Project #1:

### 1- Techniques:

- 

### 2- Step-by-step:

### 3- Challenges:

***
