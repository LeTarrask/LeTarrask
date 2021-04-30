# Hacking With Swift UIKit Projects & Milestones
Completed all projects in 27/04/2021, and added to [github repo](https://github.com/LeTarrask/HackingWithSwift)

***

## Milestone #1: Learning the Swift Language
Fizz Buzz test
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Milestone_Projects/1_FizzBuzz/FizzBuzz.playground)

### 1- Techniques:

- A quick explanation of swift language.

### 2- Step-by-step:

### 3- Challenges:

Basically, fizzbuzz exercise. I remember from Pro Swift that it can be done with a switch, and that will be my solution, although not very original. Funcionou, mas eu precisava relembrar a maneira de escrever a tuple de entrada e de comparação dos casos.


***

## Project #1: Storm Viewer
Get started coding in Swift by making an image viewer app and learning key concepts.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/1_Storm%20Viewer/Storm%20Viewer)

### 1- Techniques:

- FileManager
- UIViewController

### 2- Step-by-step:

We create a TableViewController, connect it to a tableview in storyboard, create a DetailViewController and also connect it to storyboard, and automatically create the method that links the two of them. It was a mix of a revival of old tutorials past, and also a wake-up call of how easier SwiftUI is.

### 3- Challenges:

Use Interface Builder to select the text label inside your table view cell and adjust its font size to something larger (did by changing it in storyboard inspector); In your main table view, show the image names in sorted order, so “nssl0033.jpg” comes before “nssl0034.jpg” (did it by calling sort() in the pictures array just in the end of viewDidLoad method); Rather than show image names in the detail title bar, show “Picture X of Y” (passed it as a string to detail view).


***

## Project #2: Guess the flag
Make a game using UIKit, and learn about integers, buttons, colors and actions.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/2_Guess%20the%20flag/Guess%20the%20Flag)

### 1- Techniques:

- asset catalogs
- buttons, layers actions, random numbers, alerts

### 2- Step-by-step:

A simple project where we create 3 buttons with storyboard and add a simple game logic. It's simpler than SwiftUI, but SwiftUI's result is more complex.

### 3- Challenges:

Try showing the player’s score in the navigation bar, alongside the flag to guess. (did a string interpolation into the title); Keep track of how many questions have been asked, and show one final alert controller after they have answered 10. This should show their final score. (added a resetGame method, and a questions counter); When someone chooses the wrong flag, tell them their mistake in your alert message –
something like “Wrong! That’s the flag of France,” for example (added a message string, just like the title, that gets the correct value and capitalizes it.)

***

## Project #3: Social Media
Let users share to Facebook and Twitter by modifying project 1.
Code in project #1

### 1- Techniques:

- Simple project to create an ActivityViewController and genereate a share screen

### 2- Step-by-step:

### 3- Challenges:

Try adding the image name to the list of items that are shared. The activityItems parameter is an array, so you can add strings and other things freely (It's just a matter of adding the string to the array); Add a bar button item to the main view controller that recommends the app (it's just a matter of repeating the tutorial); Add a bar button item that shows their score when tapped (this challenge is also a practice one).


***

## Milestone #2: Welcome to UIKit
create an app that lists various world flags in a table view
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Milestone_Projects/2_FlagDetail/FlagDetail)

### 2- Step-by-step:

Repeating a lot of techniques from the previous 3 projects, we load flag images from the bundle, show them in a tableview in a TableViewController, show it larger in a DetailView and then share it with the tap of a button. This exercise is more of a memorization thing.


***

## Project #4: Easy Browser
Embed Web Kit and learn about delegation, KVO, classes and UIToolbar.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/4_Easy%20Browser/Easy%20Browser)

### 1- Techniques:

- WebView
- KVO (key value observation, observing a value and changing it, something that's probable better solved with Combine now.)

### 2- Step-by-step:

We create a WebView (I'm pretty sure there's a simpler SwiftUI way to code it), and use a UIKit ProgressView to show the loading progress of the page.

### 3- Challenges:

If users try to visit a URL that isn’t allowed, show an alert saying it’s blocked (using UIAlertController); making two new toolbar items with the titles Back and Forward (did it and created a couple of selectors and @objc functions); try changing the initial view controller to a table view like in project 1, where users can choose their website from a list rather than just having the first in the array loaded up front (it wasn't particularly hard, but a lot of steps that I had to get from other code). These projects all sound like more training and remembering, which is good for me now, but drag a little bit.


***

## Project #5: Word Scramble
Create an anagram game while learning about closures and booleans.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/5_Word%20Scramble/Word%20Scramble)

### 1- Techniques:

- txt file reading

### 2- Step-by-step:

We reuse a lot of knowledge here, like AlertController, actions, tableview. In the SwiftUI project, it's a lot more simpler to simply generate a list and edit it.

### 3- Challenges:

Disallow answers that are shorter than three letters or are just our start word (the tip is almost the answer); Refactor all the else statements we just added so that they call a new method called showErrorMessage(). This should accept an error message and a title, and do all the UIAlertController work from there; Add a left bar button item that calls startGame(); BONUS: fix a bug.


***

## Project #6: Auto Layout
Get to grips with Auto Layout using practical examples and code.
[repo]()

**can skip for now**
### 1- Techniques:

-

### 2- Step-by-step:

### 3- Challenges:


***

## Milestone #3: WebKit and Closures
create an app that lets people create a shopping list by adding items to a table view
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Milestone_Projects/3_Shopping%20List)

### 1- Techniques:

- Delegation
- UIAlertController
- UIBarButtonItems
- KVO
- contentsOf to read files
- contains(), remove(at: ), firstIndex(of:)
- AutoLayout (I skipped it.)
- try?, try!, and unwrapping optionals.

### 2- Step-by-step:

Create a tableview, insert elements into it, update it's values when they change (missing SwiftUI already), sharing it with a popoverPresentationController


***

## Project #7: Whitehouse Petitions
Make an app to parse Whitehouse petitions using JSON and a tab bar.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/7_Whitehouse%20Petitions/Whitehouse%20petitions)

### 1- Techniques:

- JSON
- Codable
- TabViewController, which is deprecated in SwiftUI
- Turning a few strings into html to show in a WebView
- Some AppDelegate shenaningans for TabView (it probably is not working anymore in new XCode)

### 2- Step-by-step:

We simply create another tableview, and populate it with structs that are codable. It's pretty similar to other tutorials. Apparently there's something not working with the tabview in the appdelegate, which I should try to debug, but since it's something that should not be used from now on, I'm moving on.

### 3- Challenges:

The challenges are exercises: adding another alert that should come from an UIBarButtomItem (stuff I've done a few times, I'll leave to improve in a next time); Allow to filter petitions (stuff that can be simply done with Codable and Combine easier than with UIKit), and customizing the HTML that shows the data.


***

## Project #8: 7 Swifty Words
Build a word-guessing game and master strings once and for all.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/8_7%20Swifty%20Words/7%20Swifty%20Words)

### 1- Techniques:

- UIKit programmatically
- Build a view without storyboard (it's a pain)
- property observers: didSet
- addTarget()
- enumerated(), joined(), replacingOccurrences() and other String methods.

### 2- Step-by-step:

A lot of pages to build one single view (still missing SwiftUI, will do forever, I guess). Code is kind of complicated, because it's a game, but has several nice string editing tricks.

### 3- Challenges:

draw a thin gray line around the buttons view (with code from project 2); If the user enters an incorrect guess, show an alert telling them they are wrong (also simple, with code from previous project); deduct points for wrong answers and update the level up rules.


***

## Project #9: Grand Central Dispatch
Learn how to run complex tasks in the background with GCD.
Project done in other projects, so it doesn't have any code.

### 1- Techniques:

- DispatcQueue
- .async
- All the theory explaining queues, threads, and which kind of instructions should run in which threads, backgrounds, etc.
- .main, .userInitiated, .userInteractive, .utility, .background (eram as mesmas em SwiftUI? R: não, não tinha GCD nos tutoriais de SwiftUI.) A razão parece ter sentido com o Combine: as operações em background são quase sempre feitas com dados, que devem correr em threads de background. A UI é que deve ser sempre atualizada na main thread. Porém, com Combine, as UI se atualizam automaticamente, quando percebem alguma alteração nas fontes de dados publicadas).
- Easy GCD using performSelector(inBackground:)

### 2- Step-by-step:

Implemented GCD in project 7, by adding a selector to fetch the JSON in the background, and whenever it updates, it comes back to the main thread and updates UI. It's a very simple project.

### 3- Challenges:

The challenges are to implement the same solution to other 3 projects: 1, 8, and 7 (to the filtering option).
Number 1 was quite simple.
NUmber 8, as well.
Filtering option not implemented in #7.


***

## Milestone #4: JSON and GCD
Make a hangman game using UIKit
[repo]()

### 1- Techniques:
- JSONDecoder
- DispatchQueue

### 2- Step-by-step:
Did it in SwiftUI to simplify. Used the dictionary of words from project 7, and DispatchQueue'd loading it. Found a very weird bug in new XCode.

### 3- Challenges:


***

## Project #10: Names to Faces
Get started with UICollectionView and the photo library.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/10_Names%20to%20Faces/Names%20to%20faces)

### 1- Techniques:

- UICollectionViewController
- UIImagePickerController

### 2- Step-by-step:

Criamos um UICollectionView e preenchemos com uma foto tirada da memória ou da câmera.

### 3- Challenges:

O primeiro challenge é só colocar um Alert Controller; o segundo é usar a câmera, escolhendo um picker diferente na hora de escolher a imagem; o terceiro é para modificar o primeiro projeto inteiramente, para usar um CollectionView instead of a table. I'm gonna table it for now, since it's SwiftUI time, baby.


***

## Project #12: UserDefaults
Learn how to save user settings and data for later use.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/12_UserDefaults)

### 1- Techniques:

- NSCoding
- Codable
- UserDefaults

### 2- Step-by-step:

We save the data from project 10 using NSCoding, and store it in UserDefaults. After that, we do the same thing, but instead turning the Model into a Codable, which is quite easier, because we don't have to explain to it how to do its job.

### 3- Challenges:

The challenges are to apply this knowledge int old projects. Project 1 so that it remembers how many times each storm image was shown; Project 2 so that it saves the player’s highest score (could do it, but would deprecate the game over situation); Project 5 so that it saves the current word and all the player’s entries to UserDefaults.


***

### Milestone #5: Collection Views and SpriteKit
let users take photos of things that interest them, add captions to them, then show those photos in a table view.
(repo)[]

## 1-  Techniques:
- LazyVGrid
- Showing a UIViewController in SwiftUI
- Storing images and text in a JSON file using Codable to code and decode.

## 2- Step-by-step:
I did it with SwiftUI, so instead of rebuilding a UITableView, I did a LazyVGrid that holds the images.
Used Codable to store data as JSON into the bundle. Having some trouble storing the images into the bundle and recovering it, debugged it. Had to do some array magic to allow user to update the description for the model, and all is working now.

***

## Project #13: Instafilter
**There's a SwiftUI version**
Make a photo manipulation program using Core Image filters and a UISlider.
[repo]()

### 1- Techniques:

-

### 2- Step-by-step:

### 3- Challenges:


***

## Project #15: Animation
**There's a SwiftUI version**
Bring your interfaces to life with animation, and meet switch/case at the same time.
[repo]()

### 1- Techniques:
-

### 2- Step-by-step:

### 3- Challenges:


***

## Milestone #6: Core Image and Core Animation
make an app that contains facts about countries: show a list of country names in a table view, then when one is tapped bring in a new screen that contains its capital city, size, population, currency, and any other facts that interest you. The type of facts you include is down to you – Wikipedia has a huge selection to choose from.
[repo]()

### 1- Techniques:
-

### 2- Step-by-step:

### 3- Challenges:


***

## Project #16: Capital Cities
Teach users about geography while you learn about MKMapView and annotations.
**There's a SwiftUI version**
[repo]()

### 1- Techniques:

- MapKit

### 2- Step-by-step:

### 3- Challenges:


***

## Project #18: Debugging
Everyone hits problems sooner or later, so learning to find and fix them is an important skill.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/18_Debugging/Debugging)

### 1- Techniques:

- XCode Use
- assert
- break points and how to customize and analise them

### 2- Step-by-step:

This project is just about to see the debugging tools we have in XCode. Stuff I'm not currently using too much: assert inside my code (don't worry, this doesn't go to production code, just in XCode debugging), and break points to see WTF is wrong with the code I write.

### 3- Challenges:

The challenges are to use the techniques: add an exception breakpoint into project 1, adding an assert in project 1 as well, and add a conditional breakpoint if the user does something wrong. These challenges don't change final code output though, so won't be commited.


***



## Project #19: JavaScript Injection
Extend Safari with a cool feature for JavaScript developers.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/19_JavaScript%20Injection/Javascript%20Injection)

### 1- Techniques:

- Add new target build
- add code from other Language

### 2- Step-by-step:

Apparently I did something very wrong in the tutorial, and created an extension for MacOS, instead of iPhone. In any case, the tutorial is kinda deprecated, because there are new templates for specific uses, such as Safari Extensions, Safari Extensions for Mac, iOS, etc. Skipping from now on, then.

### 3- Challenges:


***

## Project #21: Local Notifications
Send reminders, prompts and alerts even when your app isn't running.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/21_Local%20Notifications/Local%20Notifications)

### 1- Techniques:

- UNUserNotificationCenter
- getting user responses to notifications
-

### 2- Step-by-step:

We created a template for notification center and a method that receives the info the user can pass on to us, so we can act accordingly.

### 3- Challenges:

Challenges are to apply this into old projects.


***

## Milestone #8: Maps and Notifications
recreate the iOS Notes app[repo]()

### 1- Techniques:
-

### 2- Step-by-step:

### 3- Challenges:


***

## Project #22: Detect-a-Beacon
Learn to find and range iBeacons using our first project for a physical device.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/22_Detect-a-Beacon)

### 1- Techniques:

- Core Location
- Location permissions and it's tricky privacy properties
- detecting beacon with a method

### 2- Step-by-step:
Read through this tutorial, since I can't build it in two devices to test. It's pretty straight-forward a way of generating beacons and reading it's input. Copied Paul Hudson's template into the folder, in case I need to build something related to it in the future.

### 3- Challenges:
Challenges are related to animating and creating alerts to this app when the results change, which are not beacon-related.


***

## Project #24: Swift Strings
Dive deep into how strings work in Swift, and learn how to add formatting on top.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/24_Swift%20Strings/Swift_Strings.playground)

### 1- Techniques:

- NSAttributedString and it's properties.

### 2- Step-by-step:

This is not a project, but a playground where we do some experimentation with NSAttributedString methods, and a few String ones, such as isEmpty, and adding extensions to remove prefixes and suffixes.

### 3- Challenges:

Create a String extension that adds a withPrefix() method. If the string already contains the prefix it should return itself; if it doesn’t contain the prefix, it should return itself with the prefix added; Create a String extension that adds an isNumeric property that returns true if the string holds any sort of number; Create a String extension that adds a lines property that returns an array of all the lines in a string.

***

## Milestone #9: Beacons and extensions
implement three Swift language extensions using what you learned in project 24[repo]()

### 1- Techniques:

-

### 2- Step-by-step:

### 3- Challenges:


***

## Project #25: Selfie Share
Make a multipeer photo sharing app in just 150 lines of code.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/25_Selfie%20Share/Selfie%20Share)

### 1- Techniques:

- Review of CollectionView like project 10 (we basically redo project 10)
- implement ImagePicker
- MCSession
- Connection betweet 2 apple device
- extension to ViewController (I did it, wasn't in the project)
- MCSessionDelegate and it's 6 necessary methods

### 2- Step-by-step:

We cloned project 10, and then implemented the MCSession features so the image is automagically shared with other apple devices that run the same apps and are connected with us.

### 3- Challenges:

Show an alert when a user has disconnected from our multipeer network; Try sending text messages across the network (Didn't); Add a button that shows an alert controller listing the names of all devices currently connected to the session – use the connectedPeers property (Didn't).


***

## Project #27: Core Graphics
Draw 2D shapes using Apple's high-speed drawing framework.
**can skip for now**
[repo]()

### 1- Techniques:

- Core Graphics

### 2- Step-by-step:

### 3- Challenges:


***

## Milestone #10: Core Motion and Core Graphics
Create a meme generation app using UIImagePickerController, UIAlertController, and Core Graphics
[repo]()

### 1- Techniques:

-

### 2- Step-by-step:

### 3- Challenges:


***

## Project #28: Secret Swift
Save user data securely using the device keychain and Touch ID.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/28_Secret%20Swift/Secret%20Swift)

### 1- Techniques:

- iOS Keychain
- Hide and show views in UIKit
- Code for keyboard resign first responder

### 2- Step-by-step:

Added a textview, then a few methods to hide and show it, according to user authentication using LocalAuthentication.

### 3- Challenges:

Done button as a navigation bar item that causes the app to re-lock immediately rather than waiting for the user to quit; Create a password system for your app so that the Touch ID/Face ID fallback is more useful (can be something interesting to be reused); Go back to project 10 (Names to Faces) and add biometric authentication so the user’s pictures are shown only when they have unlocked the app (this too).


***

## Project #30: Instruments
Become a bug detective and track down lost memory, slow drawing and more.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/30_Instruments)

### 1- Techniques:

- XCode Use
- cmd+I to launch Instruments

### 2- Step-by-step:

We run through a series of weird problems that can be detected by using instruments and then fix them.

### 3- Challenges:

Apply these instruments readings in projects 29, 30, and other projects.


***

## Milestone #11: Secrets and Explosions
Create a memory pairs game that has players find pairs of cards – it’s sometimes called Concentration, Pelmanism, or Pairs
[repo]()

### 1- Techniques:

-

### 2- Step-by-step:

### 3- Challenges:


***

## Project #31: MultiBrowser
Get started with UIStackView and see just how easy iPad multitasking is.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/31_MultiBrowser/MultiBrowser)

### 1- Techniques:

- UIStackView
- App Transport Security (Apple prevents loading sites that aren't https)
- Handling iPad multitasking with other screens.
- iPad size classes

### 2- Step-by-step:

Create an iPad project, set the view in storyboard, add some navbuttons, added webviews inside the UIStackView, delegate to control it, and then use iPad size classes to adjust the view sizes whenever it updates.

### 3- Challenges:

Test if user typed address has https as a prefix, if not, try to convert it to URL; add a descriptive label.


***

## Project #32: SwiftSearcher
Add your app's content to iOS Spotlight and take advantage of Safari integration.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/32_SwiftSearcher/SwiftSearcher)

### 1- Techniques:

- UITableViewCells
- NSAttributedString
- SafariServices
- SFSafariViewController (a safari view mode which we can't control via code)
- tableView.isEditing and .allowsSelectionDuringEditing
- tableView(_:commit:forRowAt:)
- UITableViewCell.EditingStyle
- CoreSpotlight
- MobileCoreServices
- CoreSearchableItem

### 2- Step-by-step:

Loaded an array with Hacking with Swift projects, show it in a tableview, customize the view, allow user to choose one, and open an url that has the project. Storing favorites in UserDefaults. Then we do a lot of tableView customization. Now we go to something completely different: using Core Spotlight, to show the apps features in iOS/MacOS Spotlight. CoreSearchableItem its an object that stores information about an item for Spotlight, such as titles, description images, picture info, etc.
I did a quick hack to make the final step work, because AppDelegate is different from when tutorial was made, not sure if it's perfectly working and should be tested more.

### 3- Challenges:

Make it more reusable by using a viewmodel instead of an array of strings; format the stored data differently, change dynamic type size, to make the app more customizable. These challenges are interesting if we want to apply this technique into a project. Maybe for Dualogue.


***

## Project #33: What's that Whistle
Build a crowd-sourced song recognition app using Apple's free platform as a service: CloudKit.
**Cloud Kit - requires working Apple Developer Account**
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/33_What's%20that%20Whistle/What's%20that%20Whistle)

### 1- Techniques:

- AVAudioRecorder
- CloudKit

### 2- Step-by-step:

### 3- Challenges:


***

## Project #37: Psychic Tester
Are you psychic? Of course not. But what if we could use our coding skills to make a game to fool your friends into thinking otherwise?
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/37_Psychic%20Tester/Psychic%20Tester)

### 1- Techniques:

- Watch app
- Storyboard
- CAEmmiterLayer
- IBDesignable, IBInspectable

### 2- Step-by-step:

We create a bunch of cards as subviews of a view, add a subclass of view to hold a GradientView, add audio capabilities, then start the fun stuff: adding 3D touch recognition, Apple Watch connectivity, create a watch app using storyboard, and present an instructions screen when we load the app.

### 3- Challenges:

The challenges here are to run the app and make the gimmicks for it to be fun. No Apple Watch to test, though, and I'd guess making the app in SwiftUI would be a little easier.


***

## Project #38: GitHub Commits
Get started with Core Data by building an app to fetch and store GitHub commits for Swift.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/38_GitHub%20communications/Github%20Commits)

### 1- Techniques:

- Core Data
- SwiftyJSON package, to decode JSON (now it's simpler to use more recent codable stuff, I'd guess)

### 2- Step-by-step:

We load a JSON and use SwiftyJSON framework to decode it (now I'd rather use Codable, but anyways), and then build a complex Core Data project. It's tricky.

### 3- Challenges:

Challenges are to go deep into Core Data as well. Actually, he suggests to study more. Will do that with Donny Wals' book, and probably finish Dualogue.

***

## Project #39: Unit testing with XCTest
Learn how to write unit tests and user interface tests using Xcode's built-in testing framework.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/Classic_Projects/39_Unit%20testing%20with%20XCTest/Unit%20Testing)

### 1- Techniques:

- XCTest
- filter, sort, map functions used for the first time, I'd guess
- measure {} in testing is very interesting.
- encapsulation of the filtering function is pretty interesting
- recording a UI test

### 2- Step-by-step:

We create a simple app that loads a list of words, and test its speed, and a few functions, to see if it works. The cool part is the functional programming that is presented for the first time here.

### 3- Challenges:

The challenges are to review other stuff to test, and implement them in apps.
