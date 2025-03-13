Legend:

<font color="#0070c0">tldr</font>

<font color="#00b050">Useful to Remember/Examples</font>

<font color="#ff0000">A Must to Memorize </font>

## Agenda

- #WhatIsUserInput
- #InputManagerInUnity
- #GetKey 
- #GetKeyUp
- #GetKeyDown 

## <font color="#ff0000">What is User Input?</font>

A User's Input is Very Important in a Game.

It <font color="#ff0000">helps to control the game using outlets such as Keyboards, Mouse, Controller etc.</font>


## Input Manager within Unity

The Input Manager in Unity <font color="#ff0000">allows the definition of various axes and game actions, enabling the project to access and utilize these inputs effectively.</font>

How to go to the Input Manager?:

- Go to Edit
- Then Project Settings
- Click on Input

### Input Manager (Axis)

The Input Manager in Unity <font color="#ff0000">allows us to access specific information about inputs without manually checking individual key presses</font>, Utilizing Unity's hierarchical structure displayed in the Input Manager, we can effectively manage inputs like the 'A' key.

This approach <font color="#ff0000">enables quicker access to basic controls such as the WASD keys</font> or the UP, DOWN, LEFT, RIGHT keys, <font color="#ff0000">enhancing overall efficiency</font>.


- Static Function <font color="#c3d69b">GetAxis</font>(<font color="#92cddc">axisName: string</font>) : <font color="#b2a2c7">float </font>

    - <font color="#c3d69b">Function</font> Name: GetAxis
    - <font color="#92cddc">Parameters:</font> axisName:string
    - <font color="#b2a2c7">Return Type:</font> float

-  <font color="#b2a2c7">Returns the value</font> of the virtual axis identified by <font color="#92cddc">axisName</font>


- The Value will be in the range -1 to 1 for Keyboard and Joystick Input


## Accessing the Input System

**A button will have 3 States:**

- <font color="#ff0000">GetKeyUp()</font> When Key Touches the bottom of the Keyboard(Once)
- <font color="#ff0000">GetKeyDown()</font> When Key Lifted off the Keyboard(Once)
- <font color="#ff0000">GetKey()</font> When Key is Touching the bottom of Keyboard(Repeated)


An <font color="#00b050">Example</font> would be shown Below:

    void Update()
    {
          if (Input.GetKeyDown(KeyCode.Space))
          {
              print("Pressed enter")
          }

        if (Input.GetKeyDown(KeyCode.A))
         {
             print("Pressed A")
         }
    } 


In the <font color="#00b050">Example </font>shown above;

- **Input** is the Namespace of the Input System
- **GetKeyDown( )** is the function name to detect a key touches the bottom of the keyboard
- **KeyCode.Space** is the Key detected when it touches the bottom


## Input System

### <font color="#ff0000">Input.GetKeyDown( )</font>

This Input will return true once during the frame  the user starts pressing sown the Specific Key.
### <font color="#ff0000">Input.GetKey( )</font>

This Input will Continuously return true while the user holds down the Specific Key. 
### <font color="#ff0000">Input.GetKeyUp(KeyCode.Space)</font>

This Input will only return true once during the frame the user releases the Specific Key.