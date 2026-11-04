# CS110 Action 11A — My seminar and engine experiment

Learner / folder: Rodolfo Sierra-Trujillo
Engine route: unity
Work mode: team
My personal repository / one Canvas submission link: https://github.com/rsierratrujillo4553-byte/cs110-week11
Team repository: https://github.com/Lexicon-Lexxie/CS110-Awayzo

## GitHub checks before and after work

Before work, local project / remote / latest push checked: Checked and working: opened my local CS110 folder, remote is github.com/rsierratrujillo4553-byte/cs110-week11.
Personal repository URL and file/image/link check result: Checked and working: GitHub shows my latest files.
Team repository / member links checked: Checked and working: team repo https://github.com/Lexicon-Lexxie/CS110-Awayzo.
Final push and instructor-access check result: Final push done to https://github.com/rsierratrujillo4553-byte/cs110-week11. Opened the repo in a private browser window and it works.
## 1. Our Attention Accord — shared plan/reference

Huddle start / end (at least 10 minutes): 2:00 PM to 2:30 PM (30 minutes)
Team / lead / production purpose: Team Awayzo (Lexxie, Nico, Paulina, Rudy, Sam). Lexxie leads. Before we build our game, we need to understand how a class becomes engine behavior, how values reach the visible object, and how reusable setups differ from live instances. Each person investigates one piece and returns evidence we use to choose our movement and object-setup approach.
Plan file, board photo or shared-document link: https://github.com/Lexicon-Lexxie/CS110-Lexxie/blob/main/Week11/11A/Evidence/Whiteboard/whiteboard-01-team-accord.jpg (team board photo, copy saved at Week11/11A/Evidence/Whiteboard/).
Return-to-team time and how we will use the findings: Return to the team at 2:40 PM. We choose our movement behavior from Lexxie's and Paulina's findings, our setup approach from Sam's and Rudy's, and our extension ideas from Nico's boundary and Rudy's jump tests.
Member	Focus question	Capture method	Promised contribution
Lexxie (lead, Git)	Who calls Update, and how does Time.deltaTime turn a rate into this frame's motion?	Annotated copy of TranslateObject; Speed 0/1/2 test log	Annotated example, prediction vs. result, recommendation for our movement behavior; repo structure and team repo access check
Nico (whiteboard, prototype)	How does a class become engine behavior, and how do values reach the visible object?	Whiteboard sketch: class → object → data/property → method → visible result	Whiteboard photos before and after revision; prototype idea for the team
Paulina (evidence, review)	Why does changing Tint after Start not reapply it, and why does the Inspector not call the setter?	Test notes, screenshots, evidence checklist	Explanation with proof, a mistake investigated, team index of everyone's links
Rudy (bounded AI check, QA)	What does an AI answer about one engine API get right or wrong against official docs and my test?	Question log: question, checked source, keep/change/reject	The log, plus correction of the false claim that a prefab means extra instances use no runtime memory
Sam (reuse and physics)	How do prefabs, live instances and pooling differ, and what does each cost?	Prefab vs. instance vs. pooling guide; small physics test on a copy	Guide, two-instance comparison, Transform vs. physics trap note
These are focus areas for this assignment, not ranks or permanent roles. We rotate them in later work.

## My personal attention brief

I will investigate:
How Unity uses C# scripts, classes, and components to control GameObjects.

I need to understand:
How the Start() and Update() functions work, how scripts are attached to objects, and how the Inspector displays their properties.

I will capture:
Screenshots of my C# script, the Unity Inspector, and a GameObject with its attached components.

I will return with:
An explanation of how C# scripts connect to GameObjects and how Unity uses Start() and Update() to control what happens in a game.

My evidence will be saved at:
My named project folder inside the Unity project's Assets folder, including my Scripts folder and screenshots.

How this helps our team build:
This will help our team understand how to organize our Unity project, create reusable scripts, and make GameObjects move, rotate, and change colors.

## 2. My seminar notes

During today's seminar, my professor explained how game development connects to what we already learned in C# and Visual Studio. He talked about how classes are blueprints for objects, variables store information, and functions perform actions.

We also learned about Unity's interface and how the Hierarchy, Inspector, Scene view, and Project window work together. The professor showed us how to create a GameObject, add components, and attach C# scripts to control objects.

Another important topic was organizing our Unity project. We should create folders for our scenes, scripts, prefabs, and other assets to keep everything organized, especially when working with a team.

The professor also demonstrated how to make an object move, rotate, and change colors using C# scripts. He explained how we can change variables in the Inspector to test different behaviors.

One important thing I learned is that changes made during Play Mode usually reset when we stop the game. I also learned that understanding the programming concepts we already know makes learning a new game engine easier.

Overall, the seminar helped me understand how Unity works and how I can use my C# knowledge to start creating games.
## My host translation

Engine / version / language:
Unity 6000.6.7f1 / C#

Familiar C# idea → engine equivalent:
Classes are blueprints for objects. In Unity, GameObjects use components, and C# scripts can be attached to them to give them different functions and behaviors. Variables and properties can also appear in the Unity Inspector.

Who calls initialization and repeated updates?
Unity calls `Start()` one time when the object starts, and `Update()` repeatedly every frame through the game loop.

One discovery I shared with the team:
I learned that Unity uses prefabs to create multiple objects while referencing the same original asset. This helps keep the game organized and saves resources. I also learned that keeping folders organized is important when working with a development team.

## 3. My individual base

My source files / scene:
MainScene (TeamProject/Scenes), Cube named Player, scripts TranslateObject.cs, RotateObject.cs, and ChangeColor.cs in TeamProject/Scripts, all attached to the Player cube.

Starting values and prediction:
Speed = 2, Degrees Per Second = 90, Change Speed = 1. I predicted the cube would move right along the world X axis at 2 units per second, spin around the Y axis once every 4 seconds (360 / 90), and cycle through the full color spectrum about every 10 seconds (hue advances 0.1 per second at Change Speed 1).

Actual movement / rotation / color result:
The cube moved to the right along the world X axis, rotated steadily around the Y axis, and cycled through colors continuously. This matched my prediction. 

Frustration or error, and how I investigated:
I had no errors. All three scripts compiled and worked on the first run. The only thing I had to watch for was not making any changes while in play mode. To check my work, I made sure to run every test twice.

## 4. My experiment and return to the team

**My question / prediction:**
I wanted to see how changing the movement and rotation speeds would affect two cubes in Unity. I predicted that the cube with higher values would move and rotate faster.

**Change beyond the base:**
I created two cubes and changed the second cube's movement speed to 4 and rotation speed to 100 degrees per second. I also created a prefab so I could reuse my GameObject.

**Observed result or exact error / next step:**
Both cubes successfully moved, rotated, and changed colors when I ran the game. The second cube moved and rotated faster than the first cube, just like I predicted. I didn't have any errors during my final test.

**Prefab or saved scene and two-instance comparison:**
I saved my work in 11A-Unity.unity and created a prefab instance. My first cube has a movement speed of 2 and a rotation speed of 90 degrees per second. My second cube has a movement speed of 4 and a rotation speed of 100 degrees per second. When I tested them, the second cube moved and rotated faster.

**What I promised → what I actually returned:**
I promised to investigate how C# scripts and components work in Unity. I successfully created two cubes, attached C# scripts, changed their settings, and tested their behaviors. I also created a prefab and saved my evidence.

**My interpretation/recommendation and supporting evidence:**
I learned that the same C# scripts can control multiple GameObjects with different settings. I recommend testing different values in the Inspector to see how they affect each object. My Unity scene and screenshots are my supporting evidence.

**How the team will use it; what I learned from someone else:**
My team can use my experiment to understand how C# scripts control multiple GameObjects and how prefabs can be reused. From my professor's lecture, I learned how components, properties, and the Unity game loop work together.

**Checked source or supplied-claim correction:**
I used my professor's Unity lecture to understand how GameObjects, components, and prefabs work. I also learned that changes made during Play Mode usually reset when the game stops, so important settings should be changed outside Play Mode.
## Source and evidence

For my individual project, I used Unity 6.6 and C# to practice what we learned during the seminar. I created two cubes and used C# scripts to make them move, rotate, and change colors.

**My project and evidence:**
- Personal GitHub repository: https://github.com/rsierratrujillo4553-byte/cs110-week11
- Evidence folder: https://github.com/rsierratrujillo4553-byte/cs110-week11/tree/main/11A/Evidence
- Unity scene: MainScene
- C# scripts: TranslateObject.cs, RotateObject.cs, and ChangeColor.cs
- Team repository: https://github.com/Lexicon-Lexxie/CS110-Awayzo
- Checked source: My professor's Unity seminar

**My individual engine base status:**
Working — I successfully created my cube and used three C# scripts to make it move, rotate, and change colors. All three functions worked when I tested the game.

**My individual extension status:**
Working — I added a second cube to my Unity scene. Both cubes move, rotate, and change colors. My next step is to compare their settings and record the differences.

**Help received:**
I used my professor's lecture to help me understand Unity, C# scripts, and how to organize my project.

**What I learned:**
I learned how to use C# scripts to control GameObjects in Unity. I also learned how components work and how to test different behaviors using the Inspector.

My project files, screenshots, and other evidence are organized in my personal GitHub repository.
