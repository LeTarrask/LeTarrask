# Hacking With SwiftUI Projects
Completed all projects in 15/04/2021, and added to [github repo](https://github.com/LeTarrask/HackingWithSwift)

***

## Project #1: WeSplit
A check-splitting app

[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/1_WeSplit)

### 1- Techniques:

- Basic project structure
- Form
- @State
- Navigation View
- Picker
- .keyboardType(.decimalPad)
- Double formatting
- Computed properties

### 2- Step-by-step:

Basically, create a single view that computes some properties which are updated onscreen, using @State properties.

### 3- Challenges:

Add to the form, create another computed property, change the picker.

***

## Project #2: Guess the Flag
Build a game with stacks, images, and alerts
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/2_Guess%20the%20Flag)

### 1- Techniques:
- Stacks
- Gradients
- Alerts
- Image Modifiers

### 2- Step-by-step:
Basically, create a view that shows an image from an array randomly, and a property that adds or subtracts if the property is right. The view is composed with stacks and modifiers to make it look better.

### 3- Challenges:
Add a score property, show the score in a label below the flags, inform the name of the flag the player choose wrong.

***

## Project #3: Views and Modifiers
Dive deep into Swift's rendering system
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/3_Views%20and%20Modifiers)

### 1- Techniques:
- Types of views
- View Modifiers and how they work
- Custom containers is interesting. He shows an example which is basically a Grid, like VGrid or HGrid, before it was introduced in Swift 2.0
- View Builders - he shows how to create a builder of a custom view
- Generics

### 2- Step-by-step:
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


### 3- Challenges:
Create a view modifier, add a modifier to exercise 1, add another modifier to exercise 2.

***

## Project #4: BetterRest
Use machine learning to improve sleep
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/4_BetterRest)

### 1- Techniques:
- Date picker
- Picker
- Stepper again
- Date formatting
- ML
- Form

### 2- Step-by-step:
Create the form, the variables, a func to be called in code, some Date formatting

### 3- Challenges:
Turn VStacks into Form Sections, Replace a stepper with a picker, show a textview with the final result, without the calculate button

***

## Project #5: Word Scramble
Build a letter rearranging game with List
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/5_Word%20Scramble)

### 1- Techniques:
- List, onAppear(), Bundle, fatalError()
- Opening files
- String operations
- .trimmingCharacters(in: .whitespacesAndNewlines) -> to remove whitespaces and lines, for example, in a string
- UITextChecker()
- Character encoding
- .autocapitalization(.none)

### 2- Step-by-step:
Criar a lista, criar os inputs, quatro condicionais para checar as palavras, um método de init que abre o arquivo, profit.

### 3- Challenges:
Add checks for word lenght or if it's the same as initial word, add nav button to start game,

***

## Project #6: Animation
Spruce up your UI with springs, bounces, and more
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/6_Animation)

### 1- Techniques:
- scaleEffect, blur, easeOut, .interpolatingSpring(stiffness: 50, damping: 1)

### 2- Step-by-step:
There are a lot of animation parameters explained in this chapter. It's a mix between documentation and testing. For example, this:
.animation(Animation.easeInOut(duration: 2).repeatCount(3, autoreverses: true))
rotation3DEffect()
Created different views with all the animation exercises

### 3- Challenges:
In the Guess the Flag project, tap the correct flag, make it spin around 360 degrees on the Y axis; make the other two buttons fade out to 25% opacity; tap on the wrong flag (personally, I chose to make the background show a red rectangle.)

***

## Project #7: iExpense
Bring in a second view with this expense tracking app
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/7_iExpense)

### 1- Techniques:
- multiple screens, load and save user data, more complex user interfaces
- @ObservedObject property wrapper
- Presenting views with modal sheets
- using OnDelete
- UserDefaults
- Archiving objects with Codable

### 2- Step-by-step:
Pretty similar to some aspects of Mileage Tracker, and some solutions I found there, but a very barebones version of it.

### 3- Challenges:
add edit/done button to contentview, modify each expense layout according to value, add validation to addview, showing alert if wrong input


***

## Project #8: Moonshot
Teach users about space history with scroll views, Codable, and more
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/8_Moonshot)

### 1- Techniques:
- Geometry Reader
- ScrollView to work with scrolling Data
- NavigationLink
- Hierarchical Codable Data
- Loading Specific Codable Data

### 2- Step-by-step:
Decode the provided jsons and images to show them in an organized, structured way.

### 3- Challenges:
Add mission date to one view (trivial), Modify AstronautView to show all the missions this astronaut flew on (got super struck and had to ask for help), Make a bar button in ContentView that toggles between showing launch dates and showing
crew names (it was supposed to be hard, and found it kinda simple.)


***

## Project #9: Drawing
Use shapes, paths, colors, and more to create custom art for your app
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/9_Drawing)

### 1- Techniques:
- AffineTransform
- insettableShape
- Blurs and blending
- Animating shapes with animatableData

### 2- Step-by-step:
A tutorial for each of the techniques, all saved in the xcode project.

### 3- Challenges:
Draw an arrow with a triangle and a rectangle, change the outline of the arrow, make a colorcyclingrectangle like the circule we had.

***

## Project #10: Cupcake Corner
Build an app that sends and receives JSON from the internet
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/10_Cupcake%20Corner)

### 1- Techniques:
- Making a class compatible with codable by adding a required init and a CodingKeys enum for its value.
- Sending and receiving Codable data with URLSession and SwiftUI
- .disabled(-condition-) to hide a section in case something is not present

### 2- Step-by-step:
Start creating the screens, uses a single Class to hold all the data, that's passed around the views, and has all the data validation methods inside it. Complicated part is when we have to add Codable to the class. After that, did a url request to a mockup server, sending the order encoded in JSON and decoded the response as well.

### 3- Challenges:
Validate user input so it doesn't have empty spaces (did this by adding: .trimmingCharacters(in: .whitespacesAndNewlines) to the current checks), added an error message in case the response data is not what we're expecting, apologizing for the inconvencience, the third task is a complete refactor of the project, so I'll postpone it. (see if you can convert our data model from a class to a struct, then create an ObservableObject class wrapper around it that gets passed around. This will result in your class having one @Published property, which is the data struct inside it, and should make supporting Codable on the struct much easier.)


***

## Project #11: Bookworm
Use Core Data to build an app that tracks books you like
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/11_Bookworm)

### 1- Techniques:
- @Binding
- Size classes (@Environment(\.horizontalSizeClass) properties that can be used to return different views according to devices: .compact, for smaller ones or split screens, and .regular, for larger screens.)
- AnyView - a type erased wrapper (AnyView conforms to the same View protocol as Text, Color, VStack, and more, and it also contains inside it a view of a specific type. However, externally AnyView doesn’t expose what it contains – Swift sees our condition as returning either an AnyView or an AnyView, so it’s considered the same type. This is where the name “type erasure” comes from: AnyView effectively hides – or erases – the type of the views it contains.)
- Core Data
- Mocking data to preview Core Data objects in XCode preview
- FetchRequests
- NSSortDescriptors
- Create items, and save
- Delete items from moc
- Create one own's components to be reused
- Edit button to modify list

### 2- Step-by-step:
Let's start by creating stuff in Core Data. Created a basic core data input form, and a contentview that has a fetchrequest to show all the items. Then, a RatingsView that can be reused with Bindings. Then, we add items, delete items and fetch items, with a sort description.

### 3- Challenges:
It’s possible to select no genre for books - fix this, either by forcing a default, validating the form, or showing a default picture for unknown genres – you can choose. I've added "No genre" default value.; Modify ContentView so that books rated as 1 star have their name shown in red.; Add a new “date” attribute to the Book entity, assigning Date() to it so it gets the current
date and time, then format that nicely somewhere in DetailView.


***

## Project #12: Core Data
Take an in-depth tour of how SwiftUI and Core Data work together
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/12_Core%20Data)

### 1- Techniques:
- .self and ForEach, Hashable, how they are used to compare objects
- Creating NSManagedObject subclasses, to change how they work, and forego using XCode generated Code Data behavior.
- if self.moc.hasChanges { try? self.moc.save() }
- Using constraints to guarantee objects are unique in Core Data
- NSPredicate tem umas complicações, é uma mini query language cheia de pequenos truques.
- Filtrar os requests dinamicamente usando SwiftUI
- Object relationship in Code Data

### 2- Step-by-step:
O truque do if moc.hasChanges é bem interessante para evitar trabalho do Core Data, e os constraints para evitar dados duplicados.
This is basically a reading project, with small examples. The content here can be leveraged in my Mileage Tracker project.

### 3- Challenges:


***

## Project #13: Instafilter
Learn to link SwiftUI, UIKit, and Core Image in one app
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/13_Instafilter)

### 1- Techniques:
- Custom bindings
- CIFilters
- Wrapping a UIViewController in a SwiftUI View!
- ActionSheets
- Reutilizable ImageSaver class, with error handling

### 2- Step-by-step:
Creating the first view, and using a if to show there's a lack of image. Creating a UIImagePickerController to select an image. We end up with a reusable ImagePicker. Note for the future. Basic image filtering using Core Image. Modified the code to allow for customization of the CI filter value in the view. Created an ImageSaver class, that can also be reutilized. It also has error handling.

### 3- Challenges:
Making the Save button show an error if there was no image in the image view; make the Change Filter button change its title to show the name of the currently selected
filter; experiment with having more than one slider, to control each of the input keys you care about (POSTPONED). For example, you might have one for radius and one for intensity


***

## Project #14: Bucket List
Embed maps and make network calls in this life goals app
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/14_Bucket%20List)

### 1- Techniques:
- Codable
- URLSession
- Embed Maps with MapKit
- iOS storage
- Coordinators
- Adding conformance to Comparable for custom types
- File manager class to store stuff in app directory
- Switching view states with enums
- Touch ID and Face ID
- Querying Wikipedia for data using GPS location.
- Enum loading state
- Implement Comparable
- import LocalAuthentication to use FaceID

### 2- Step-by-step:
Created a specific project just with the embeded mapview for swiftui and all the properties, coordinator, and helpers added to the project, so I can reuse in the future.
After that, we do implement codable and a loading state to query from wikipedia and get data from nearby places, and then store all the info in a JSON file encrypted in memory. We also use FaceID or TouchID to secure the app's data.

### 3- Challenges:
Our + button is rather hard to tap. Try moving all its modifiers to the image inside the button (the answer is that only the + was the actionable view, and with all the modifiers inside the button, all of them are now clickable); Having a complex if condition in the middle of ContentView isn’t easy to read – can you rewrite it so that the MapView, Circle, and Button are part of their own view? (instead of putting MapView, Circle and Button in another view, I put the LocalAuthentication code in a view that's presented before, and if the @State value is changed, presents the ContentView. :) ); Add code to show those errors in an alert.


***

## Project #15: Accessibility
Learn how to make your apps available to everyone
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/15_Accessibility)

### 1- Techniques:
- .accesibility(label: Text()) - to simply tell over VoiceOver what something is
- .accessibility(hint:) - a long description that hints on the usage of something
- accesibility(addTraits: ) - to explain what that View is
- accesibility(removeTraits: .isImage) - to ignore describing an Image
- Image(decorative: ) - for something that doesn't need to be described in VoiceOver
- .accessibility(hidden: true) - makes something completely hidden to accessibility system
- .accessibilityElement(children: .combine) - to combine elements in a stack or group (like a few texts that shoulb be read together)
- .accessibilityElement(children: .ignore)
.accessibility(label: Text("Your score is 1000")) - can be used together to create a better reading experience
- .accessibility(value: Text("\(Int(estimate))")) - can be used to improve the reading of a slider, for example, and uses Int to be easier.

### 2- Step-by-step:
Fixing Guess the Flag.
Fixing Word Scramble.
Fixing Bookworm

### 3- Challenges:
Check out view in Cupcake Corner uses an image that doesn’t add anything to the UI (added the decorative: init to it); fix the steppers in BetterRest; full accessibility review of MoonShot (not today Satan).


***

## Project #16: Hot Prospects
Build an app for conferences with tabs, context menus, and more.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/16_Hot%20Prospects)

### 1- Techniques:
- Tab bars
- Context menus
- sharing custom data with the environment
- sending custom notifications
- .interpolation(.none) - to avoid blur in small images over expanded.
- .contextMenu, that creates a menu when users long press a view.
- Local Notifications
- Package import
- QR Code generation

### 2- Step-by-step:
Created a simple fetchrequest with result and network error enum project that's on the folder. Then implemented a .contextMenu. Then locally generated UserNotifications. Created a tabview. Created an environment object to hold codable class, an enum filtertype to filter the contacts in different views. Then we generate a QR code from simple data with Swift. Here I used .interpolation(.none) to make the QR Code not pixelated. Added TwoStraws code scanner package. This allows to scan the QR Code. Then we handle the result, turning it into name and email, and creating a Prospect in our Prospects array. Then we use a contextMenu to change whether the contact has been contacted or not (can be used in a ToDo list, for example.) Added possibility of notification in our context menu, scheduled with iOS notification center.

### 3- Challenges:
Add an icon to the “Everyone” screen showing whether a prospect was contacted or not. Use JSON and the documents directory for saving and loading our user data. Use an action sheet to customize the way users are sorted in each screen – by name or by
most recent.


***

## Project #17: Flashzilla
Use gestures and haptics to build a learning app.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/17_Flashzilla)

### 1- Techniques:
- gestures, haptics, timers
- .onTapGesture(count: 2) - for double taps
- .onLongPressGesture - for long press
- .onLongPressGesture(minimumDuration: 2) - minimum time of long press
- all the gesture structs: DragGesture, LongPressGesture, MagnificationGesture, RotationGesture, and TapGesture
- they all have special modifiers, such as onEnded() and sometimes onChanged(), so we can add actions during and after.
- simultaneousGesture (when we want to use gestures in child and view)
- UINotificationFeedbackGenerator
- Haptics kinds: .success, .erro, .warning
- to specify a tappable area: .contentShape(Rectangle())
- when you import SwiftUI we also implicitly import Combine
- Timer can be user as a Combine Publisher, so .onReceive(timer) { time in } - can be user to trigger actions
- timer.upstream.connect().cancel() - stops a timer
- timers have tolerance
- UIApplication.willResignActiveNotification - when app goes to background, can be used to pause, save data, etc. For example: .onReceive(NotificationCenter.default.publisher(for:
UIApplication.willResignActiveNotification)) { _ in
 print("Moving to the background!") }
- Other notifications: willEnterForegroundNotification - when app comes back, userDidTakeScreenshotNotification - when user takes screenshot, .significantTimeChangeNotification - when user changes clock or daylight savings time, .keyboardDidShowNotification - when keyboard comes to screen
- usability properties: @Environment(\.accessibilityDifferentiateWithoutColor) var
differentiateWithoutColor
- @Environment(\.accessibilityReduceMotion) var reduceMotion - reduces the uses of animation
- @Environment(\.accessibilityReduceTransparency) var
reduceTransparency - reduces the use of transparency

### 2- Step-by-step:
It's one of the largest projects, but it's very interesting. The possibility of creating a stack of cards with shades, movement and all was great. It is all full of accessibility elements, which area also nice.

### 3- Challenges:
Make something interesting for when the timer runs out (added an alert - not interesting, but I'm tired);


***

## Project #18: Layout and Geometry
Explore the inner workings of SwiftUI's layout system.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/18_Layout%20and%20Geometry)

### 1- Techniques:
- .lastTextBaseline
- alignmentGuide()
- GeometryReader
- custom alignment Modifiers

### 2- Step-by-step:
Just to create a few different views using the geometry reader and a few modifiers. They're stored in the project in the folder. The challenges are much more practices, in our current projects.

### 3- Challenges:
Change project 8 (Moonshot) so that when you scroll down in MissionView the mission badge image gets smaller;


***

## Project #19: SnowSeeker
Build an app for ski resorts that works great on iPad.
[repo](https://github.com/LeTarrask/HackingWithSwift/tree/main/SwiftUI_Projects_OK/19_SnowSeeker)

### 1- Techniques:
- NavigationView and how views work in split screens (ex: iPads)
- Showing alerts when optional properties are set. This is way simpler than the way we've been using alerts. For example, there's an optional error. It only will show the alert when the error is created.
- Using Group to merge several views and later define their layout.
- sizeClass: .compact (small devices)
- To initialize a view inside a VStack, for example: VStack(content: UserView.init)
- ListFormatter - same behavior as joining an array of strings, but adds an "and" before the last one.
- Spacer.frame(height: 0) - for a spacer only work in horizontal formats

### 2- Step-by-step:
We have a model, decode from JSON, show it. All stuff we've seen before. The fun part is how the navigation views work in different Apple devices, the large ones and the small ones. This is the more challenging stuff, that we've not seen before.
This project is also suggested as a template app, to show objects and its details.

### 3- Challenges:
Add a photo credit over the ResortView image; Fill in the loading and saving methods for Favorites; For a real challenge, let the user sort and filter the resorts in ContentView. For sorting
use default, alphabetical, and country, and for filtering let them select country, size, or price (postponed).
