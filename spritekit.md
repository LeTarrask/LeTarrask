# Hacking With Swift SpriteKit Projects
Completed all projects in **/04/2021, and added to [github repo](https://github.com/LeTarrask/HackingWithSwift)

***

### Project #11: Pachinko
Dive into SpriteKit to try your hand at fast 2D games.
(repo)[https://github.com/LeTarrask/HackingWithSwift/tree/main/SpriteKit_Projects/11_Pachinko/pachinko]

## 1-  Techniques:
**Sprite Kit**
- SpriteKit
- Reseting the project
- didMove (equivalent of ViewDidLoad pra GameKit)
- addChild (para adicionar objetos à cena)
- physicsBody
- physicsWorld.contactDelegate
- SKLabelNode (tipo um label)
- touchesBegan (pra interpretar os toques na tela)
- physicsBody?.isDinamic (to make the physicsBody respond to contacts and touches and etc)
- SKEmitterNode (to use particles)
- Particles editor

## 2- Step-by-step:
Created a Pachinko app. It creates a ball that falls into different holes, and if they're right, it adds points. The game is quite boring, but shows how the game features work.

## 3- Challenges:
First was to choose different colors randomly when the ball is created. Just created an array that holds all the filenames and picks a randomElement(); Second was to add an if to change ball drop location to be always over 640 points; Third was more complex: contact has to destroy the box barriers, had to add a name to them and then, when they're contacted, they're destroyed.

***

### Project #14: Whack-a-Penguin
Build a game using SKCropNode and a sprinkling of Grand Central Dispatch.
**Sprite Kit**
(repo)[https://github.com/LeTarrask/HackingWithSwift/tree/main/SpriteKit_Projects/14_Whack-a-Penguin/Whack%20a%20Penguin]

## 1-  Techniques:
- SpriteKit
- DispatchQueue
- SKCropNode
- SKAction
- SKNode subclasses

## 2- Step-by-step:
Created a simple whack game that detects touches and interprets it according to whatever reaction we wanted. It also plays sounds and counts. It uses a SKNode subclass that holds different images, and has its own reactions and properties.

## 3- Challenges:
First challenge is to add customized audio, didn't do because I don't want to record my voice; Second was to add a SKLabelNode with the final score when the game ends; Third, to add a smoke like effect when penguins are hit, I've reused the fire effect from previous project instead.


***

### Project #17: Space Race
Dodge space debris while you learn about per-pixel collision detection.
**Sprite Kit**
(repo)[https://github.com/LeTarrask/HackingWithSwift/tree/main/SpriteKit_Projects/17_Space%20Race/Space%20Race]

## 1-  Techniques:
- SpriteKit
- per-pixel collision
- Timer
- Contact with didBegin
- physicsBody properties

## 2- Step-by-step:
It's a super quick project, with less than 100 lines, to teach a few SpriteKit concepts.

## 3- Challenges:
First challenge I think I completed, but can't test in simulator; Second was to add an increaser every 20 debris created, did it using the score variable; Third challenge is just to invalidate the timer when player dies.

***

## Milestone #7: Extensions and Debugging
Make a shooting gallery game using SpriteKit: create three rows on the screen, then have targets slide across from one side to the other. If the user taps a target, make it fade out and award them points.
**Sprite Kit**
[repo]()

### 1- Techniques:

-

### 2- Step-by-step:

### 3- Challenges:


***

### Project #20: Fireworks Night
Learn about timers and color blends while making things go bang!
**Sprite Kit**
(repo)[]

## 1-  Techniques:
- SpriteKit
- follow() - this SKAction is very interesting for the SuperSprint project, as its input is a path that the object must follow, orienting it's facing direction.
- motionBegan() to detect movement
- for case let

## 2- Step-by-step:
Game tutorials are simpler than the other ones. We created the Timer that automatically creates groups of 5 fireworks, and then add a override method to main view controller that explode the fireworks.

## 3- Challenges:
First, add a score label. Second, end the game after a few launches, just adding a variable to count and invalidate Timer. Third, use SKAction.wait(forDuration: 1) to delay and then remove the emitter particles from Scene.

***

### Project #23: Swifty Ninja
Learn to draw shapes in SpriteKit while making a fun and tense slicing game.
**Sprite Kit**
(repo)[]

## 1-  Techniques:
- SpriteKit

## 2- Step-by-step:

## 3- Challenges:



***

### Project #26: Marble Maze
Respond to device tilting by steering a ball around a vortex maze.
**Sprite Kit**
(repo)[]

## 1-  Techniques:
- SpriteKit

## 2- Step-by-step:

## 3- Challenges:



***

### Project #29: Exploding Monkeys
Remake a classic DOS game and learn about destructible terrain and scene transitions.
**Sprite Kit**
(repo)[]

## 1-  Techniques:
- SpriteKit

## 2- Step-by-step:

## 3- Challenges:



***

### Project #34: Four in a Row
Let iOS take over the AI in your games using GameplayKit AI.
**Sprite Kit**
(repo)[]

## 1-  Techniques:
- GKGameModel

## 2- Step-by-step:

## 3- Challenges:




***

### Project #35: Random Numbers
Let GameplayKit help you generate random numbers in ways you soon won't be able to live without.
**Sprite Kit**
(repo)[]

## 1-  Techniques:
- GameplayKit

## 2- Step-by-step:

## 3- Challenges:


***

### Project #36: Crashy Plane
Ever wanted to make a Flappy Bird clone? Now you can do it in under an hour thanks to SpriteKit.
**Sprite Kit**
(repo)[]

## 1-  Techniques:
- SpriteKit

## 2- Step-by-step:

## 3- Challenges:
