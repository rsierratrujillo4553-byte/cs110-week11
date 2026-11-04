# CS110 Action 11A — My seminar and engine experiment

Learner / folder: Rodolfo Sierra-Trujillo
Engine route: unity
Work mode: team
My personal repository / one Canvas submission link: https://github.com/rsierratrujillo4553-byte/cs110
Team repository: https://github.com/Lexicon-Lexxie/CS110-Awayzo

## GitHub checks before and after work

Before work, local project / remote / latest push checked: Checked and working: opened my local CS110 folder, remote is github.com/rsierratrujillo4553-byte/cs110-week11.
Personal repository URL and file/image/link check result: Checked and working: GitHub shows my latest files.
Team repository / member links checked: Checked and working: team repo https://github.com/Lexicon-Lexxie/CS110-Awayzo.
Final push and instructor-access check result: Final push done to https://github.com/Lexicon-Lexxie/CS110-Lexxie/tree/main/Week11/11A. Opened the repo in a private browser window and it works.
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

[Not recorded yet — complete this section.]

## My host translation

Engine / version / language:
Unity 6.3.27f2 / C#

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

My question / prediction:
I want to see how C# scripts control GameObjects in Unity. I predict that changing the speed variable will make an object move faster or slower.

Change beyond the base:
I will change the movement speed and test different values to see how they affect the object.

Observed result or exact error / next step:
My next step is to attach my C# script to a cube, run the game, and test different movement speeds to see what changes.

Prefab or saved scene and two-instance comparison:
I will create a prefab of my cube and place two copies in the scene. I will give each cube a different speed to compare how they move.

What I promised → what I actually returned:
I promised to investigate how C# scripts and components work in Unity. I will return with screenshots, notes, and an example showing how a script controls a GameObject.

My interpretation/recommendation and supporting evidence:
I think using C# scripts and components makes it easier to control objects in Unity. I will use screenshots of my Inspector settings and movement tests as evidence.

How the team will use it; what I learned from someone else:
My team can use my findings to understand how scripts control objects. From the professor's demonstration, I learned that Unity uses Start() for initialization and Update() for repeated actions.

Checked source or supplied-claim correction:
I used my professor's Unity lecture as my source. I learned that changes made in the Inspector during Play Mode usually reset when the game stops, so important changes should be made outside Play Mode.

## Source and evidence

[Link my project, scene, whiteboard screenshots/photos, base/extension evidence and checked source. All my authored work belongs in this personal repository.]

My individual engine base status: [working / blocked — explain].
My individual extension status: [result / error and next step].
Help received: [describe].

Commit and push all my authored work, including board captures, notes, project and evidence, to my personal repository. Open the pushed files/images and test the personal URL and applicable team URL/member links. Submit the one personal repository URL in Canvas; this README contains the team link if applicable. This export is not Canvas submission.
