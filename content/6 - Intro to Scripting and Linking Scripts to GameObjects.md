Legend:

<font color="#0070c0">tldr</font>

<font color="#00b050">Useful to Remember</font>

<font color="#ff0000">A Must to Memorize </font>
## Agenda 

- #WhatIsScriptingInUnity
- #CreateScriptsInUnity
- #Classes
- #Functions/Methods
- #System/UserFunctions

## What is Scripting in Unity?

A Scene is made of many GameObjects, these GameObjects are made up of Components consisting of Scripts.

The Scripts defines how the GameObject behaves by the logics in the Scripts.

Gameplay of a Game is based on the Scripts and Components attached to the GameObjects.

***tldr:*** 
<font color="#0070c0">Gameplay is dependent on Scripts and Components from various GameObjects, which are defined by the logics of said scripts attached to them</font>

## Script using Assets Explorer/ From a GameObject

**First in the Asset Explorer**, the Script is first created then attached to the GameObject.

How to Create?: <font color="#ff0000">Right click on the empty space of the assets window and create the C# Script, I'm sure we alr know right?</font>

But how about in the GameObject itself?

How to Create?:(By now we should also know about this)

- <font color="#ff0000">Click on the GameObject you want the Script to reside in</font>
- <font color="#ff0000">Click on Add Component</font>
- <font color="#ff0000">Type a Name for the Scrip</font>
- <font color="#ff0000">Select New Script</font>
- <font color="#ff0000">Lastly, Click Create and Add</font>


## What are Classes?

<font color="#ff0000">Each Script in Unity is already considered a Class, these Classes help to structure the code and contains a collection of variables and methods/functions.</font>

###  What are Variables?

They are declared at the top of functions

Examples include:

public int score

- public = accessibility
- int = data type
- score = variable name

## What are Functions in Unity?

These Functions, also known as Methods, are <font color="#ff0000">a collection of codes that perform a specific operation</font>. Their names in Unity <font color="#ff0000">always starts with an Uppercase Letter</font>, and the codes within said Functions <font color="#ff0000">can be reused multiple times in the program</font>.

## Common Functions/Methods

- **Awake()**
- **Start()**
- **Update()**

## Awake()

The Awake() Method is the <font color="#ff0000">first method to be called</font>.

<font color="#ff0000">If the GameObject is inactive it will not be enabled</font>, whereas if the <font color="#ff0000">Component script is not enabled but GameObject is active</font> , Awake() <font color="#ff0000">can be used to initialize all the variables declared.</font>

However, with a GameObject with a Script already existing in the scene when scene starts,<font color="#ff0000"> Awake() will be called before Start() immediately</font>.


## Start()

The Start() Method will be <font color="#ff0000">called when the GameObject with the Script Component are active</font>, this method is called before the start of the Update() loop.


## Update()

Codes within this Method will be <font color="#ff0000">executed every frame when the GameObject is Enabled(Active).</font>

So if you are running a game in 60fps, Update() will run 60 times a second


## Writing your own Functions/Methods

These Functions must be Written with the Curly Braces within the  **{ and }** of a class.

**Consisting of the Following in order:**

<font color="#ff0000">1. Access Modifier(public/internal/private)</font>
<font color="#ff0000">2. Return Type(void, int, float, string, bool)</font>
<font color="#ff0000">3. Function Name</font>
<font color="#ff0000">4. Arguments(Variables within the () )</font>

An Example would include:

- Access Modifier(default internal)
- Return Type(void)
- Function Name(scoreUpdate())
- Arguments none

## Calling Functions

In order to call a Function you must have a Function written.

In order to differentiate a Function call and the Function itself, the Function Call  ends with a Semi-Colon( **;** ) and the Function itself has **{ and }** 