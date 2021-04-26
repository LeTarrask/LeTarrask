# Swift Learning Path

My idea is to speed run through these projects, assessing what I already know, building super fast whatever it is, and also writing down what I don't know. For the tenth time, instead of doing it in three months, I'll do it in one.

All the projects will be stored in one single repo.

## Hacking With SwiftUI Projects
Completed all projects in 15/04/2021, and added to [github repo](https://github.com/LeTarrask/HackingWithSwift)

### Project #1: WeSplit
A check-splitting app
1- Techniques:
[] - Basic project structure
[] - Form
[] - @State
[] - Navigation View
[] - Picker
[] - .keyboardType(.decimalPad)
[] - Double formatting
[] - Computed properties

2- Step-by-step:
Basically, create a single view that computes some properties which are updated onscreen, using @State properties.

3- Challenges:
Add to the form, create another computed property, change the picker.

### Project #2: Guess the Flag
Build a game with stacks, images, and alerts
1- Techniques:
[] - Stacks
[] - Gradients
[] - Alerts
[] - Image Modifiers

2- Step-by-step:
Basically, create a view that shows an image from an array randomly, and a property that adds or subtracts if the property is right. The view is composed with stacks and modifiers to make it look better.

3- Challenges:
Add a score property, show the score in a label below the flags, inform the name of the flag the player choose wrong.

### Project #3: Views and Modifiers
Dive deep into Swift's rendering system
1- Techniques:
[] - Types of views
[] - View Modifiers and how they work
[] - Custom containers is interesting. He shows an example which is basically a Grid, like VGrid or HGrid, before it was introduced in Swift 2.0
[] - View Builders - he shows how to create a builder of a custom view
[] - Generics

2- Step-by-step:
Interesting code:

Template for View Modifier:
struct Title: ViewModifier {
   func body(content: Content) -> some View {
      content
         .font(.largeTitle)
         .foregroundColor(.white)
         .padding()
         .background(Color.blue)
         .clipShape(RoundedRectangle(cornerRadius: 10))
       }
}

We can now use that with the modifier() modifier – yes, it’s a modifier called “modifier”, but it lets us apply any sort of modifier to a view, like this:

Text("Hello World")
   .modifier(Title())

When working with custom modifiers, it’s usually a smart idea to create extensions on View that make them easier to use. For example, we might wrap the Title modifier in an extension such as this:

extension View {
   func titleStyle() -> some View {
      self.modifier(Title())
   }
 }

 We can now use the modifier like this:

 Text("Hello World")
   .titleStyle()


3- Challenges:
Create a view modifier, add a modifier to exercise 1, add another modifier to exercise 2.

### Project #4: BetterRest
Use machine learning to improve sleep
1- Techniques:
[] - Date picker
[] - Picker
[] - Stepper again
[] - Date formatting
[] - ML
[] - Form

2- Step-by-step:
Create the form, the variables, a func to be called in code, some Date formatting

3- Challenges:
Turn VStacks into Form Sections, Replace a stepper with a picker, show a textview with the final result, without the calculate button

### Project #5: Word Scramble
Build a letter rearranging game with List
1- Techniques:
[] - List, onAppear(), Bundle, fatalError()
[] - Opening files
[] - String operations
[] - .trimmingCharacters(in: .whitespacesAndNewlines) -> to remove whitespaces and lines, for example, in a string
[] - UITextChecker()
[] - Character encoding
[] - .autocapitalization(.none)

2- Step-by-step:
Criar a lista, criar os inputs, quatro condicionais para checar as palavras, um método de init que abre o arquivo, profit.

3- Challenges:
Add checks for word lenght or if it's the same as initial word, add nav button to start game,

### Project #6: Animation
Spruce up your UI with springs, bounces, and more
1- Techniques:
[] - scaleEffect, blur, easeOut, .interpolatingSpring(stiffness: 50, damping: 1)

2- Step-by-step:
There are a lot of animation parameters explained in this chapter. It's a mix between documentation and testing. For example, this:
.animation(Animation.easeInOut(duration: 2).repeatCount(3, autoreverses: true))
rotation3DEffect()
Created different views with all the animation exercises

3- Challenges:
In the Guess the Flag project, tap the correct flag, make it spin around 360 degrees on the Y axis; make the other two buttons fade out to 25% opacity; tap on the wrong flag (personally, I chose to make the background show a red rectangle.)

### Project #7: iExpense
Bring in a second view with this expense tracking app
1- Techniques:
[] - multiple screens, load and save user data, more complex user interfaces
[] - @ObservedObject property wrapper
[] - Presenting views with modal sheets
[] - using OnDelete
[] - UserDefaults
[] - Archiving objects with Codable

2- Step-by-step:
Pretty similar to some aspects of Mileage Tracker, and some solutions I found there, but a very barebones version of it.

3- Challenges:
add edit/done button to contentview, modify each expense layout according to value, add validation to addview, showing alert if wrong input


### Project #8: Moonshot
Teach users about space history with scroll views, Codable, and more
1- Techniques:
[] - Geometry Reader
[] - ScrollView to work with scrolling Data
[] - NavigationLink
[] - Hierarchical Codable Data
[] - Loading Specific Codable Data

2- Step-by-step:
Decode the provided jsons and images to show them in an organized, structured way.

3- Challenges:
Add mission date to one view (trivial), Modify AstronautView to show all the missions this astronaut flew on (got super struck and had to ask for help), Make a bar button in ContentView that toggles between showing launch dates and showing
crew names (it was supposed to be hard, and found it kinda simple.)


### Project #9: Drawing
Use shapes, paths, colors, and more to create custom art for your app
1- Techniques:
[] - AffineTransform
[] - insettableShape
[] - Blurs and blending
[] - Animating shapes with animatableData

2- Step-by-step:
A tutorial for each of the techniques, all saved in the xcode project.

3- Challenges:
Draw an arrow with a triangle and a rectangle, change the outline of the arrow, make a colorcyclingrectangle like the circule we had.

### Project #10: Cupcake Corner
Build an app that sends and receives JSON from the internet
1- Techniques:
[] - Making a class compatible with codable by adding a required init and a CodingKeys enum for its value.
[] - Sending and receiving Codable data with URLSession and SwiftUI
[] - .disabled(-condition-) to hide a section in case something is not present

2- Step-by-step:
Start creating the screens, uses a single Class to hold all the data, that's passed around the views, and has all the data validation methods inside it. Complicated part is when we have to add Codable to the class. After that, did a url request to a mockup server, sending the order encoded in JSON and decoded the response as well.

3- Challenges:
Validate user input so it doesn't have empty spaces (did this by adding: .trimmingCharacters(in: .whitespacesAndNewlines) to the current checks), added an error message in case the response data is not what we're expecting, apologizing for the inconvencience, the third task is a complete refactor of the project, so I'll postpone it. (see if you can convert our data model from a class to a struct, then create an ObservableObject class wrapper around it that gets passed around. This will result in your class having one @Published property, which is the data struct inside it, and should make supporting Codable on the struct much easier.)


### Project #11: Bookworm
Use Core Data to build an app that tracks books you like
1- Techniques:
[] - @Binding
[] - Size classes (@Environment(\.horizontalSizeClass) properties that can be used to return different views according to devices: .compact, for smaller ones or split screens, and .regular, for larger screens.)
[] - AnyView - a type erased wrapper (AnyView conforms to the same View protocol as Text, Color, VStack, and more, and it also contains inside it a view of a specific type. However, externally AnyView doesn’t expose what it contains – Swift sees our condition as returning either an AnyView or an AnyView, so it’s considered the same type. This is where the name “type erasure” comes from: AnyView effectively hides – or erases – the type of the views it contains.)
[] - Core Data
[] - Mocking data to preview Core Data objects in XCode preview
[] - FetchRequests
[] - NSSortDescriptors
[] - Create items, and save
[] - Delete items from moc
[] - Create one own's components to be reused
[] - Edit button to modify list

2- Step-by-step:
Let's start by creating stuff in Core Data. Created a basic core data input form, and a contentview that has a fetchrequest to show all the items. Then, a RatingsView that can be reused with Bindings. Then, we add items, delete items and fetch items, with a sort description.

3- Challenges:
It’s possible to select no genre for books - fix this, either by forcing a default, validating the form, or showing a default picture for unknown genres – you can choose. I've added "No genre" default value.; Modify ContentView so that books rated as 1 star have their name shown in red.; Add a new “date” attribute to the Book entity, assigning Date() to it so it gets the current
date and time, then format that nicely somewhere in DetailView.


### Project #12: Core Data
Take an in-depth tour of how SwiftUI and Core Data work together
1- Techniques:
[] - .self and ForEach, Hashable, how they are used to compare objects
[] - Creating NSManagedObject subclasses, to change how they work, and forego using XCode generated Code Data behavior.
[] - if self.moc.hasChanges { try? self.moc.save() }
[] - Using constraints to guarantee objects are unique in Core Data
[] - NSPredicate tem umas complicações, é uma mini query language cheia de pequenos truques.
[] - Filtrar os requests dinamicamente usando SwiftUI
[] - Object relationship in Code Data

2- Step-by-step:
O truque do if moc.hasChanges é bem interessante para evitar trabalho do Core Data, e os constraints para evitar dados duplicados.
This is basically a reading project, with small examples. The content here can be leveraged in my Mileage Tracker project.

3- Challenges:


### Project #13: Instafilter
Learn to link SwiftUI, UIKit, and Core Image in one app
1- Techniques:
[] - Custom bindings
[] - CIFilters
[] - Wrapping a UIViewController in a SwiftUI View!
[] - ActionSheets
[] - Reutilizable ImageSaver class, with error handling

2- Step-by-step:
Creating the first view, and using a if to show there's a lack of image. Creating a UIImagePickerController to select an image. We end up with a reusable ImagePicker. Note for the future. Basic image filtering using Core Image. Modified the code to allow for customization of the CI filter value in the view. Created an ImageSaver class, that can also be reutilized. It also has error handling.

3- Challenges:
Making the Save button show an error if there was no image in the image view; make the Change Filter button change its title to show the name of the currently selected
filter; experiment with having more than one slider, to control each of the input keys you care about (POSTPONED). For example, you might have one for radius and one for intensity


### Project #14: Bucket List
Embed maps and make network calls in this life goals app
1- Techniques:
[] - Codable
[] - URLSession
[] - Embed Maps with MapKit
[] - iOS storage
[] - Coordinators
[] - Adding conformance to Comparable for custom types
[] - File manager class to store stuff in app directory
[] - Switching view states with enums
[] - Touch ID and Face ID
[] - Querying Wikipedia for data using GPS location.
[] - Enum loading state
[] - Implement Comparable
[] - import LocalAuthentication to use FaceID

2- Step-by-step:
Created a specific project just with the embeded mapview for swiftui and all the properties, coordinator, and helpers added to the project, so I can reuse in the future.
After that, we do implement codable and a loading state to query from wikipedia and get data from nearby places, and then store all the info in a JSON file encrypted in memory. We also use FaceID or TouchID to secure the app's data.

3- Challenges:
Our + button is rather hard to tap. Try moving all its modifiers to the image inside the button (the answer is that only the + was the actionable view, and with all the modifiers inside the button, all of them are now clickable); Having a complex if condition in the middle of ContentView isn’t easy to read – can you rewrite it so that the MapView, Circle, and Button are part of their own view? (instead of putting MapView, Circle and Button in another view, I put the LocalAuthentication code in a view that's presented before, and if the @State value is changed, presents the ContentView. :) ); Add code to show those errors in an alert.


### Project #15: Accessibility
Learn how to make your apps available to everyone
1- Techniques:
[] - .accesibility(label: Text()) - to simply tell over VoiceOver what something is
[] - .accessibility(hint:) - a long description that hints on the usage of something
[] - accesibility(addTraits: ) - to explain what that View is
[] - accesibility(removeTraits: .isImage) - to ignore describing an Image
[] - Image(decorative: ) - for something that doesn't need to be described in VoiceOver
[] - .accessibility(hidden: true) - makes something completely hidden to accessibility system
[] - .accessibilityElement(children: .combine) - to combine elements in a stack or group (like a few texts that shoulb be read together)
[] - .accessibilityElement(children: .ignore)
.accessibility(label: Text("Your score is 1000")) - can be used together to create a better reading experience
[] - .accessibility(value: Text("\(Int(estimate))")) - can be used to improve the reading of a slider, for example, and uses Int to be easier.

2- Step-by-step:
Fixing Guess the Flag.
Fixing Word Scramble.
Fixing Bookworm

3- Challenges:
Check out view in Cupcake Corner uses an image that doesn’t add anything to the UI (added the decorative: init to it); fix the steppers in BetterRest; full accessibility review of MoonShot (not today Satan).


### Project #16: Hot Prospects
Build an app for conferences with tabs, context menus, and more.
1- Techniques:
[] - Tab bars
[] - Context menus
[] - sharing custom data with the environment
[] - sending custom notifications
[] - .interpolation(.none) - to avoid blur in small images over expanded.
[] - .contextMenu, that creates a menu when users long press a view.
[] - Local Notifications
[] - Package import
[] - QR Code generation

2- Step-by-step:
Created a simple fetchrequest with result and network error enum project that's on the folder. Then implemented a .contextMenu. Then locally generated UserNotifications. Created a tabview. Created an environment object to hold codable class, an enum filtertype to filter the contacts in different views. Then we generate a QR code from simple data with Swift. Here I used .interpolation(.none) to make the QR Code not pixelated. Added TwoStraws code scanner package. This allows to scan the QR Code. Then we handle the result, turning it into name and email, and creating a Prospect in our Prospects array. Then we use a contextMenu to change whether the contact has been contacted or not (can be used in a ToDo list, for example.) Added possibility of notification in our context menu, scheduled with iOS notification center.

3- Challenges:
Add an icon to the “Everyone” screen showing whether a prospect was contacted or not. Use JSON and the documents directory for saving and loading our user data. Use an action sheet to customize the way users are sorted in each screen – by name or by
most recent.


### Project #17: Flashzilla
Use gestures and haptics to build a learning app.
1- Techniques:
[] - gestures, haptics, timers
[] - .onTapGesture(count: 2) - for double taps
[] - .onLongPressGesture - for long press
[] - .onLongPressGesture(minimumDuration: 2) - minimum time of long press
[] - all the gesture structs: DragGesture, LongPressGesture, MagnificationGesture, RotationGesture, and TapGesture
[] - they all have special modifiers, such as onEnded() and sometimes onChanged(), so we can add actions during and after.
[] - simultaneousGesture (when we want to use gestures in child and view)
[] - UINotificationFeedbackGenerator
[] - Haptics kinds: .success, .erro, .warning
[] - to specify a tappable area: .contentShape(Rectangle())
[] - when you import SwiftUI we also implicitly import Combine
[] - Timer can be user as a Combine Publisher, so .onReceive(timer) { time in } - can be user to trigger actions
[] - timer.upstream.connect().cancel() - stops a timer
[] - timers have tolerance
[] - UIApplication.willResignActiveNotification - when app goes to background, can be used to pause, save data, etc. For example: .onReceive(NotificationCenter.default.publisher(for:
UIApplication.willResignActiveNotification)) { _ in
 print("Moving to the background!") }
[] - Other notifications: willEnterForegroundNotification - when app comes back, userDidTakeScreenshotNotification - when user takes screenshot, .significantTimeChangeNotification - when user changes clock or daylight savings time, .keyboardDidShowNotification - when keyboard comes to screen
[] - usability properties: @Environment(\.accessibilityDifferentiateWithoutColor) var
differentiateWithoutColor
[] - @Environment(\.accessibilityReduceMotion) var reduceMotion - reduces the uses of animation
[] - @Environment(\.accessibilityReduceTransparency) var
reduceTransparency - reduces the use of transparency

2- Step-by-step:
It's one of the largest projects, but it's very interesting. The possibility of creating a stack of cards with shades, movement and all was great. It is all full of accessibility elements, which area also nice.

3- Challenges:
Make something interesting for when the timer runs out (added an alert - not interesting, but I'm tired);


### Project #18: Layout and Geometry
Explore the inner workings of SwiftUI's layout system.
1- Techniques:
[] - .lastTextBaseline
[] - alignmentGuide()
[] - GeometryReader
[] - custom alignment Modifiers

2- Step-by-step:
Just to create a few different views using the geometry reader and a few modifiers. They're stored in the project in the folder. The challenges are much more practices, in our current projects.

3- Challenges:
Change project 8 (Moonshot) so that when you scroll down in MissionView the mission badge image gets smaller;


### Project #19: SnowSeeker
Build an app for ski resorts that works great on iPad.
1- Techniques:
[] - NavigationView and how views work in split screens (ex: iPads)
[] - Showing alerts when optional properties are set. This is way simpler than the way we've been using alerts. For example, there's an optional error. It only will show the alert when the error is created.
[] - Using Group to merge several views and later define their layout.
[] - sizeClass: .compact (small devices)
[] - To initialize a view inside a VStack, for example: VStack(content: UserView.init)
[] - ListFormatter - same behavior as joining an array of strings, but adds an "and" before the last one.
[] - Spacer.frame(height: 0) - for a spacer only work in horizontal formats

2- Step-by-step:
We have a model, decode from JSON, show it. All stuff we've seen before. The fun part is how the navigation views work in different Apple devices, the large ones and the small ones. This is the more challenging stuff, that we've not seen before.
This project is also suggested as a template app, to show objects and its details.

3- Challenges:
Add a photo credit over the ResortView image; Fill in the loading and saving methods for Favorites; For a real challenge, let the user sort and filter the resorts in ContentView. For sorting
use default, alphabetical, and country, and for filtering let them select country, size, or price (postponed).

***

## Hacking with Swift UIKit Projects & Milestones

### Milestone #1: Learning the Swift Language
Fizz Buzz test
1- Techniques:
[] - A quick explanation of swift language.

2- Step-by-step:

3- Challenges:
Basically, fizzbuzz exercise. I remember from Pro Swift that it can be done with a switch, and that will be my solution, although not very original. Funcionou, mas eu precisava relembrar a maneira de escrever a tuple de entrada e de comparação dos casos.


### Project #1: Storm Viewer
Get started coding in Swift by making an image viewer app and learning key concepts.

1- Techniques:
[] - FileManager
[] - UIViewController

2- Step-by-step:
We create a TableViewController, connect it to a tableview in storyboard, create a DetailViewController and also connect it to storyboard, and automatically create the method that links the two of them. It was a mix of a revival of old tutorials past, and also a wake-up call of how easier SwiftUI is.

3- Challenges:
Use Interface Builder to select the text label inside your table view cell and adjust its font size to something larger (did by changing it in storyboard inspector); In your main table view, show the image names in sorted order, so “nssl0033.jpg” comes before “nssl0034.jpg” (did it by calling sort() in the pictures array just in the end of viewDidLoad method); Rather than show image names in the detail title bar, show “Picture X of Y” (passed it as a string to detail view).


### Project #2: Guess the flag
**There's a SwiftUI version - can skip**
Make a game using UIKit, and learn about integers, buttons, colors and actions.
1- Techniques:
[] - asset catalogs
[] - buttons, layers actions, random numbers, alerts

2- Step-by-step:
A simple project where we create 3 buttons with storyboard and add a simple game logic. It's simpler than SwiftUI, but SwiftUI's result is more complex.

3- Challenges:
Try showing the player’s score in the navigation bar, alongside the flag to guess. (did a string interpolation into the title); Keep track of how many questions have been asked, and show one final alert controller after they have answered 10. This should show their final score. (added a resetGame method, and a questions counter); When someone chooses the wrong flag, tell them their mistake in your alert message –
something like “Wrong! That’s the flag of France,” for example (added a message string, just like the title, that gets the correct value and capitalizes it.)

### Project #3: Social Media
Let users share to Facebook and Twitter by modifying project 1.
1- Techniques:
[] - Simple project to create an ActivityViewController and genereate a share screen

2- Step-by-step:

3- Challenges:
Try adding the image name to the list of items that are shared. The activityItems parameter is an array, so you can add strings and other things freely (It's just a matter of adding the string to the array); Add a bar button item to the main view controller that recommends the app (it's just a matter of repeating the tutorial); Add a bar button item that shows their score when tapped (this challenge is also a practice one).

### Milestone #2: Welcome to UIKit
create an app that lists various world flags in a table view

2- Step-by-step:
Repeating a lot of techniques from the previous 3 projects, we load flag images from the bundle, show them in a tableview in a TableViewController, show it larger in a DetailView and then share it with the tap of a button. This exercise is more of a memorization thing.


### Project #4: Easy Browser
Embed Web Kit and learn about delegation, KVO, classes and UIToolbar.
1- Techniques:
[] - WebView
[] - KVO (key value observation, observing a value and changing it, something that's probable better solved with Combine now.)

2- Step-by-step:
We create a WebView (I'm pretty sure there's a simpler SwiftUI way to code it), and use a UIKit ProgressView to show the loading progress of the page.

3- Challenges:
If users try to visit a URL that isn’t allowed, show an alert saying it’s blocked (using UIAlertController); making two new toolbar items with the titles Back and Forward (did it and created a couple of selectors and @objc functions); try changing the initial view controller to a table view like in project 1, where users can choose their website from a list rather than just having the first in the array loaded up front (it wasn't particularly hard, but a lot of steps that I had to get from other code). These projects all sound like more training and remembering, which is good for me now, but drag a little bit.

### Project #5: Word Scramble
**There's a SwiftUI version - can skip**
Create an anagram game while learning about closures and booleans.
1- Techniques:
[] - txt file reading

2- Step-by-step:
We reuse a lot of knowledge here, like AlertController, actions, tableview. In the SwiftUI project, it's a lot more simpler to simply generate a list and edit it.

3- Challenges:
Disallow answers that are shorter than three letters or are just our start word (the tip is almost the answer); Refactor all the else statements we just added so that they call a new method called showErrorMessage(). This should accept an error message and a title, and do all the UIAlertController work from there; Add a left bar button item that calls startGame(); BONUS: fix a bug.


### Project #6: Auto Layout
Get to grips with Auto Layout using practical examples and code.
**can skip for now**
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Milestone #3: WebKit and Closures
create an app that lets people create a shopping list by adding items to a table view
1- Techniques:
[] - Delegation
[] - UIAlertController
[] - UIBarButtonItems
[] - KVO
[] - contentsOf to read files
[] - contains(), remove(at: ), firstIndex(of:)
[] - AutoLayout (I skipped it.)
[] - try?, try!, and unwrapping optionals.

2- Step-by-step:
Create a tableview, insert elements into it, update it's values when they change (missing SwiftUI already), sharing it with a popoverPresentationController


### Project #7: Whitehouse Petitions
Make an app to parse Whitehouse petitions using JSON and a tab bar.
1- Techniques:
[] - JSON
[] - Codable
[] - TabViewController, which is deprecated in SwiftUI
[] - Turning a few strings into html to show in a WebView
[] - Some AppDelegate shenaningans for TabView (it probably is not working anymore in new XCode)

2- Step-by-step:
We simply create another tableview, and populate it with structs that are codable. It's pretty similar to other tutorials. Apparently there's something not working with the tabview in the appdelegate, which I should try to debug, but since it's something that should not be used from now on, I'm moving on.

3- Challenges:
The challenges are exercises: adding another alert that should come from an UIBarButtomItem (stuff I've done a few times, I'll leave to improve in a next time); Allow to filter petitions (stuff that can be simply done with Codable and Combine easier than with UIKit), and customizing the HTML that shows the data.


### Project #8: 7 Swifty Words
Build a word-guessing game and master strings once and for all.
1- Techniques:
[] - UIKit programmatically
[] - Build a view without storyboard (it's a pain)
[] - property observers: didSet
[] - addTarget()
[] - enumerated(), joined(), replacingOccurrences() and other String methods.

2- Step-by-step:
A lot of pages to build one single view (still missing SwiftUI, will do forever, I guess). Code is kind of complicated, because it's a game, but has several nice string editing tricks.

3- Challenges:
draw a thin gray line around the buttons view (with code from project 2); If the user enters an incorrect guess, show an alert telling them they are wrong (also simple, with code from previous project); deduct points for wrong answers and update the level up rules.


### Project #9: Grand Central Dispatch
Learn how to run complex tasks in the background with GCD.
1- Techniques:
[] - DispatcQueue
[] - .async
[] - All the theory explaining queues, threads, and which kind of instructions should run in which threads, backgrounds, etc.
[] - .main, .userInitiated, .userInteractive, .utility, .background (eram as mesmas em SwiftUI? R: não, não tinha GCD nos tutoriais de SwiftUI.) A razão parece ter sentido com o Combine: as operações em background são quase sempre feitas com dados, que devem correr em threads de background. A UI é que deve ser sempre atualizada na main thread. Porém, com Combine, as UI se atualizam automaticamente, quando percebem alguma alteração nas fontes de dados publicadas).
[] - Easy GCD using performSelector(inBackground:)

2- Step-by-step:
Implemented GCD in project 7, by adding a selector to fetch the JSON in the background, and whenever it updates, it comes back to the main thread and updates UI. It's a very simple project.

3- Challenges:
The challenges are to implement the same solution to other 3 projects: 1, 8, and 7 (to the filtering option).
Number 1 was quite simple.
NUmber 8, as well.
Filtering option not implemented in #7.


### Milestone #4: JSON and GCD
Make a hangman game using UIKit
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Project #10: Names to Faces
Get started with UICollectionView and the photo library.
1- Techniques:
[] - UICollectionViewController
[] - UIImagePickerController

2- Step-by-step:
Criamos um UICollectionView e preenchemos com uma foto tirada da memória ou da câmera.

3- Challenges:
O primeiro challenge é só colocar um Alert Controller; o segundo é usar a câmera, escolhendo um picker diferente na hora de escolher a imagem; o terceiro é para modificar o primeiro projeto inteiramente, para usar um CollectionView instead of a table. I'm gonna table it for now, since it's SwiftUI time, baby.


### Project #11: Pachinko
Dive into SpriteKit to try your hand at fast 2D games.
1- Techniques:
**Sprite Kit**
[] - SpriteKit

2- Step-by-step:

3- Challenges:


### Project #12: UserDefaults
Learn how to save user settings and data for later use.
1- Techniques:
[] - NSCoding
[] - Codable
[] - UserDefaults

2- Step-by-step:
We save the data from project 10 using NSCoding, and store it in UserDefaults. After that, we do the same thing, but instead turning the Model into a Codable, which is quite easier, because we don't have to explain to it how to do its job.

3- Challenges:
The challenges are to apply this knowledge int old projects. Project 1 so that it remembers how many times each storm image was shown; Project 2 so that it saves the player’s highest score (could do it, but would deprecate the game over situation); Project 5 so that it saves the current word and all the player’s entries to UserDefalts.


### Milestone #5: Collection Views and SpriteKit
let users take photos of things that interest them, add captions to them, then show those photos in a table view.
**Sprite Kit**
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Project #13: Instafilter
**There's a SwiftUI version**
Make a photo manipulation program using Core Image filters and a UISlider.
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Project #14: Whack-a-Penguin
Build a game using SKCropNode and a sprinkling of Grand Central Dispatch.
**Sprite Kit**
1- Techniques:
[] - SpriteKit
[] - DispatcQueue

2- Step-by-step:

3- Challenges:



### Project #15: Animation
**There's a SwiftUI version**
Bring your interfaces to life with animation, and meet switch/case at the same time.
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Milestone #6: Core Image and Core Animation
make an app that contains facts about countries: show a list of country names in a table view, then when one is tapped bring in a new screen that contains its capital city, size, population, currency, and any other facts that interest you. The type of facts you include is down to you – Wikipedia has a huge selection to choose from.
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Project #16: Capital Cities
Teach users about geography while you learn about MKMapView and annotations.
**There's a SwiftUI version**

1- Techniques:
[] - MapKit

2- Step-by-step:

3- Challenges:


### Project #17: Space Race
Dodge space debris while you learn about per-pixel collision detection.
**Sprite Kit**
1- Techniques:
[] - SpriteKit

2- Step-by-step:

3- Challenges:


### Project #18: Debugging
Everyone hits problems sooner or later, so learning to find and fix them is an important skill.
1- Techniques:
[] - XCode Use
[] - assert
[] - break points and how to customize and analise them

2- Step-by-step:
This project is just about to see the debugging tools we have in XCode. Stuff I'm not currently using too much: assert inside my code (don't worry, this doesn't go to production code, just in XCode debugging), and break points to see WTF is wrong with the code I write.

3- Challenges:
The challenges are to use the techniques: add an exception breakpoint into project 1, adding an assert in project 1 as well, and add a conditional breakpoint if the user does something wrong. These challenges don't change final code output though, so won't be commited.


### Milestone #7: Extensions and Debugging
make a shooting gallery game using SpriteKit: create three rows on the screen, then have targets slide across from one side to the other. If the user taps a target, make it fade out and award them points.
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Project #19: JavaScript Injection
Extend Safari with a cool feature for JavaScript developers.
1- Techniques:
[] - Add new target build
[] - add code from other Language

2- Step-by-step:
Apparently I did something very wrong in the tutorial, and created an extension for MacOS, instead of iPhone. In any case, the tutorial is kinda deprecated, because there are new templates for specific uses, such as Safari Extensions, Safari Extensions for Mac, iOS, etc. Skipping from now on, then.

3- Challenges:


### Project #20: Fireworks Night
Learn about timers and color blends while making things go bang!
**Sprite Kit**
1- Techniques:
[] - SpriteKit

2- Step-by-step:

3- Challenges:




### Project #21: Local Notifications
Send reminders, prompts and alerts even when your app isn't running.
1- Techniques:
[] - UNUserNotificationCenter
[] - getting user responses to notifications
[] -

2- Step-by-step:
We created a template for notification center and a method that receives the info the user can pass on to us, so we can act accordingly.

3- Challenges:
Challenges are to apply this into old projects.


### Milestone #8: Maps and Notifications
recreate the iOS Notes app
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Project #22: Detect-a-Beacon
Learn to find and range iBeacons using our first project for a physical device.
1- Techniques:
[] - Core Location
[] - Location permissions and it's tricky privacy properties
[] - detecting beacon with a method

2- Step-by-step:
Read through this tutorial, since I can't build it in two devices to test. It's pretty straight-forward a way of generating beacons and reading it's input. Copied Paul Hudson's template into the folder, in case I need to build something related to it in the future.

3- Challenges:
Challenges are related to animating and creating alerts to this app when the results change, which are not beacon-related.


### Project #23: Swifty Ninja
Learn to draw shapes in SpriteKit while making a fun and tense slicing game.
**Sprite Kit**
1- Techniques:
[] - SpriteKit

2- Step-by-step:

3- Challenges:



### Project #24: Swift Strings
Dive deep into how strings work in Swift, and learn how to add formatting on top.
1- Techniques:
[] - NSAttributedString and it's properties.

2- Step-by-step:
This is not a project, but a playground where we do some experimentation with NSAttributedString methods, and a few String ones, such as isEmpty, and adding extensions to remove prefixes and suffixes.

3- Challenges:
Create a String extension that adds a withPrefix() method. If the string already contains the prefix it should return itself; if it doesn’t contain the prefix, it should return itself with the prefix added; Create a String extension that adds an isNumeric property that returns true if the string holds any sort of number; Create a String extension that adds a lines property that returns an array of all the lines in a string.

### Milestone #9: Beacons and extensions
implement three Swift language extensions using what you learned in project 24
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Project #25: Selfie Share
Make a multipeer photo sharing app in just 150 lines of code.
1- Techniques:
[] - Review of CollectionView like project 10 (we basically redo project 10)
[] - implement ImagePicker
[] - MCSession
[] - Connection betweet 2 apple device
[] - extension to ViewController (I did it, wasn't in the project)
[] - MCSessionDelegate and it's 6 necessary methods

2- Step-by-step:
We cloned project 10, and then implemented the MCSession features so the image is automagically shared with other apple devices that run the same apps and are connected with us.

3- Challenges:
Show an alert when a user has disconnected from our multipeer network; Try sending text messages across the network (Didn't); Add a button that shows an alert controller listing the names of all devices currently connected to the session – use the connectedPeers property (Didn't).


### Project #26: Marble Maze
Respond to device tilting by steering a ball around a vortex maze.
**Sprite Kit**
1- Techniques:
[] - SpriteKit

2- Step-by-step:

3- Challenges:


### Project #27: Core Graphics
Draw 2D shapes using Apple's high-speed drawing framework.
**can skip for now**
1- Techniques:
[] - Core Graphics

2- Step-by-step:

3- Challenges:


### Milestone #10: Core Motion and Core Graphics
Create a meme generation app using UIImagePickerController, UIAlertController, and Core Graphics
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Project #28: Secret Swift
Save user data securely using the device keychain and Touch ID.
1- Techniques:
[] - iOS Keychain
[] - Hide and show views in UIKit
[] - Code for keyboard resign first responder

2- Step-by-step:
Added a textview, then a few methods to hide and show it, according to user authentication using LocalAuthentication.

3- Challenges:
Done button as a navigation bar item that causes the app to re-lock immediately rather than waiting for the user to quit; Create a password system for your app so that the Touch ID/Face ID fallback is more useful (can be something interesting to be reused); Go back to project 10 (Names to Faces) and add biometric authentication so the user’s pictures are shown only when they have unlocked the app (this too).


### Project #29: Exploding Monkeys
Remake a classic DOS game and learn about destructible terrain and scene transitions.
**Sprite Kit**
1- Techniques:
[] - SpriteKit

2- Step-by-step:

3- Challenges:


### Project #30: Instruments
Become a bug detective and track down lost memory, slow drawing and more.
1- Techniques:
[] - XCode Use
[] - cmd+I to launch Instruments

2- Step-by-step:
We run through a series of weird problems that can be detected by using instruments and then fix them.

3- Challenges:
Apply these instruments readings in projects 29, 30, and other projects.


### Milestone #11: Secrets and Explosions
Create a memory pairs game that has players find pairs of cards – it’s sometimes called Concentration, Pelmanism, or Pairs
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


### Project #31: MultiBrowser
Get started with UIStackView and see just how easy iPad multitasking is.
1- Techniques:
[] - UIStackView
[] - App Transport Security (Apple prevents loading sites that aren't https)
[] - Handling iPad multitasking with other screens.
[] - iPad size classes

2- Step-by-step:
Create an iPad project, set the view in storyboard, add some navbuttons, added webviews inside the UIStackView, delegate to control it, and then use iPad size classes to adjust the view sizes whenever it updates.

3- Challenges:
Test if user typed address has https as a prefix, if not, try to convert it to URL; add a descriptive label.


### Project #32: SwiftSearcher
Add your app's content to iOS Spotlight and take advantage of Safari integration.
1- Techniques:
[] - UITableViewCells
[] - NSAttributedString
[] - SafariServices
[] - SFSafariViewController (a safari view mode which we can't control via code)
[] - tableView.isEditing and .allowsSelectionDuringEditing
[] - tableView(_:commit:forRowAt:)
[] - UITableViewCell.EditingStyle
[] - CoreSpotlight
[] - MobileCoreServices
[] - CoreSearchableItem

2- Step-by-step:
Loaded an array with Hacking with Swift projects, show it in a tableview, customize the view, allow user to choose one, and open an url that has the project. Storing favorites in UserDefaults. Then we do a lot of tableView customization. Now we go to something completely different: using Core Spotlight, to show the apps features in iOS/MacOS Spotlight. CoreSearchableItem its an object that stores information about an item for Spotlight, such as titles, description images, picture info, etc.
I did a quick hack to make the final step work, because AppDelegate is different from when tutorial was made, not sure if it's perfectly working and should be tested more.

3- Challenges:
Make it more reusable by using a viewmodel instead of an array of strings; format the stored data differently, change dynamic type size, to make the app more customizable. These challenges are interesting if we want to apply this technique into a project. Maybe for Dualogue.


### Project #33: What's that Whistle
Build a crowd-sourced song recognition app using Apple's free platform as a service: CloudKit.
**Cloud Kit - requires working Apple Developer Account**
1- Techniques:
[] - AVAudioRecorder
[] - CloudKit

2- Step-by-step:

3- Challenges:



### Project #34: Four in a Row
Let iOS take over the AI in your games using GameplayKit AI.
**Sprite Kit**
1- Techniques:
[] - GKGameModel

2- Step-by-step:

3- Challenges:



### Project #35: Random Numbers
Let GameplayKit help you generate random numbers in ways you soon won't be able to live without.
**Sprite Kit**
1- Techniques:
[] - GameplayKit

2- Step-by-step:

3- Challenges:



### Project #36: Crashy Plane
Ever wanted to make a Flappy Bird clone? Now you can do it in under an hour thanks to SpriteKit.
**Sprite Kit**
1- Techniques:
[] - SpriteKit

2- Step-by-step:

3- Challenges:


### Project #37: Psychic Tester
Are you psychic? Of course not. But what if we could use our coding skills to make a game to fool your friends into thinking otherwise?
1- Techniques:
[] - Watch app
[] - Storyboard
[] - CAEmmiterLayer
[] - IBDesignable, IBInspectable

2- Step-by-step:
We create a bunch of cards as subviews of a view, add a subclass of view to hold a GradientView, add audio capabilities, then start the fun stuff: adding 3D touch recognition, Apple Watch connectivity, create a watch app using storyboard, and present an instructions screen when we load the app.

3- Challenges:
The challenges here are to run the app and make the gimmicks for it to be fun. No Apple Watch to test, though, and I'd guess making the app in SwiftUI would be a little easier.


### Project #38: GitHub Commits
Get started with Core Data by building an app to fetch and store GitHub commits for Swift.
1- Techniques:
[] - Core Data
[] - SwiftyJSON package, to decode JSON (now it's simpler to use more recent codable stuff, I'd guess)

2- Step-by-step:
We load a JSON and use SwiftyJSON framework to decode it (now I'd rather use Codable, but anyways), and then build a complex Core Data project. It's tricky.

3- Challenges:
Challenges are to go deep into Core Data as well.


### Project #39: Unit testing with XCTest
Learn how to write unit tests and user interface tests using Xcode's built-in testing framework.
[] - XCTest
1- Techniques:
[] -

2- Step-by-step:

3- Challenges:


***

## My Projects
### Project #15: Pomodoro
[**Pomodoro**](https://github.com/LeTarrask/Pomodoro)

[] - Mac OS
[] - Status bar app
[] - User preference storage in UserDefaults
[] - EventMonitor to figure out clicks outside the app
[] - SwiftLint
[] - SwiftUI

### Project #14: 5ed SRD Reader for Mac
**Repo not started yet**

[] - Mac OS
[] - Web requests to API
[] - Decoding JSON

### Project #13: AE Euro Counter
[**Euro Counter**](https://github.com/LeTarrask/Euro-Counter)

[] - ML Training
[] - Vision - machine recognition OCR
[] - SwiftUI
[] - iOS
[] - Live camera feed (UIKit framework used in SwiftUI)
[] -

### Project #12: Mileage Tracker
[**Mileage Tracker**](https://github.com/LeTarrask/Mileage-Tracker)

[] - iOS
[] - SwiftUI
[] - Pods
[] - Google AdMob
[] - Onboarding System with pages and router
[] - Settings System
[] - Email sending
[] - URL display
[] - Localization
[] - Local storage
[] - JSON encoding/decoding for storage
[] - Export data into CSV
[] - CSV data storage
[] - Paid mode
[] - TabView with customized icons
[] - Animated pop up tab buttons
[] - Theme Color selection
[] - User preferences storage in UserDefaults
[] - EnumPicker
[] - Pickable typealias
[] - Graphic generation with Pod
[] - Pod
[] - Extension UI Device to simplify error reporting
[] - Extension UIApplication version
[] - View date-toString
[] - Extension double - clean and rounded for UI reasons
[] -

### Project #11: Dobble
[**Dobble**](https://github.com/LeTarrask/Dobble)

[] - Podfile
[] - AdMob via pod
[] - Localization
[] - Card Generation System that uses incidence Matrix
[] - extension Array to compare 2 and find generic similarElements
[] - Game state, dificulty (via time), score
[] - Multiplayer change capability
[] - Tests for card generation, match, and game controller creation
[] - iOS built
[] - SwiftUI

### Project #10: Tobem Ipsum
[**Tobem Ipsum**](https://github.com/LeTarrask/Tobem-Ipsum)

[] - Mac OS
[] - Status bar app
[] - Clipboard use
[] - User preference storage in UserDefaults
[] - Capability of choosing which vocabulary to use
[] - Enum Picker
[] - EventMonitor to figure out clicks outside the app
[] - SwiftLint
[] - SwiftUI

### Project #9: 2048
[**2048**](https://github.com/LeTarrask/2048)

[] - Podfile
[] - SwifLint via pod
[] - AdMob via pod
[] - Onboarding controller / multiple screens
[] - Loading screen animation
[] - Game data storage encoded/decoded in JSON to UserDefaults
[] - Neuemorphic design
[] - Game matrix in a 2D array
[] - Localization
[] - ViewModifier (for the tiles)
[] - Array extension to find index of element
[] - Color extension to get UIColor
[] - Several different and fun gradient extensions
[] - View extension to invert color content
[] - Tests for the game engine
[] - iOS built
[] - SwifUI

### Project #8: Paradoxes
[**Paradoxes**](https://github.com/LeTarrask/Paradoxes)

[] - Animation
[] - radius / sin, cos calculation to position balls in screen
[] - ternary conditionals
[] - SwiftUI

### Project #7: Mara:
**Private Repo**

[] - ML training / use in app
[] - Mac OS
[] - File system navigation with File Manager
[] - File moving
[] - File deleting
[] - SwiftUI

### Project #6: Creative Gym
[**Creative Gym**](https://github.com/LeTarrask/Creative-Gym)

[] - Complex data models
[] - iOS
[] - SwiftUI

### Project #5: Dualogue
[**Dualogue**](https://github.com/LeTarrask/Dualogue)

[] - Core Data
[] - Complex data models
[] - Generic Filtered List
[] - Color scheme
[] - Extension Date to string
[] - Environment object
[] - Fetch requests
[] - TabView
[] - iOS
[] - SwiftUI

### Project #4: Dreadline
[**Dreadline**](https://github.com/LeTarrask/Dreadline)

[] - Mac OS
[] - UIKit
[] - Text Editor
[] - Uses storyboard
[] - Email sending

### Project #3: Iniciativer
[**Iniciativer**](https://github.com/LeTarrask/Iniciativer)

[] - iOS
[] - SwiftUI

### Project #2: SwiftUI Placeholder
[**SwiftUI Placeholder**](https://github.com/LeTarrask/SwiftUI-Placeholder)

[] - SwiftUI
[] - Geometry Reader

### Project #1: 1 milhão de folhas
[**1 milhão de folhas**](https://github.com/LeTarrask/1-milh-o-de-folhas)

[] - Published project
[] - Random selection of text
[] - Storyboard UIKit
