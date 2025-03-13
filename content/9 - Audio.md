
Legend:

<font color="#0070c0">tldr</font>

<font color="#00b050">Useful to Remember/Examples</font>

<font color="#ff0000">A Must to Memorize </font>
## Agenda

- #AudioInGames
- #AudioSource
- #AudioClip
- #AudioListeners
- #PlayingAudioProgramatically


## Audio In Games

Any Game would be incomplete without Audio!

The Audio can be in the form of SFXs or BGMs.


## Audio Source

The Audio Source  Component <font color="#ff0000">allows sound to be played in the scene.</font>

It can play the Audio Clip at the Object's  location for audio listeners to  hear.

#### There are 2 ways to add the Audio Source 

1. Right click on the Empty Space in the hierarchy, Click Audio, then Audio Source

2. Go to hierarchy and click the plus sign, followed by audio then audio source


### Play on Awake( )

When you have the audio source component, there is an unchecked box called Play on Awake( ).

When Play on Awake( ) is turned on, the audio clip <font color="#ff0000">automatically plays once the object is Active.</font>

This is helpful for sounds such as explosions, BGMs etc.


#### Adding Audio  Clip to Audio Source 

Drag and Drop the Audio Clip into the Audio Component

There will be loop box unchecked, this loop refers to the repetition of a sound material



## Audio Clip

The Audio Clip is and<font color="#ff0000"> Asset representing a sound file,</font>

It is dragged into the Audio Source and is typically <font color="#ff0000">the actual  audio file that the Audio Source plays.</font>

The Clip can be changed programmatically as per the game play.

Unity can only import the following audio formats:

- AIFF
- WAV
- MP3
- Ogg


### Reverb Zones

This<font color="#ff0000"> takes the audio clip and distorts it.</font> However, it <font color="#ff0000">depends on where the Audio listener is located within the zone.</font>

This is typically <font color="#ff0000">used when you want to change from a point where there is on ambient effect to a place that has one.</font>

An <font color="#00b050">Example</font> would be Entering a Cave with ambient effect.




## Audio Listener

The Audio Listener <font color="#ff0000">acts as a microphone, receiving input from the Audio Source and plays sounds through the speaker.</font>

In most games the listener is attached to the main camera by default. And there should only be 1 Listener per scene.


## Playing  Audio using Programming

Below is and <font color="#00b050">Example </font>where jump sound is played when spacebar is pressed. 

    public AudioSource JumpSound;

     Void Update( )
     {
         if(Input.GetKeyDown(KeyCode.SpaceBar))
         {
             JumpSound.Play( );
         }
     }



## <font color="#002060">TLDR</font> for audio 

3 Different things in Audio in Unity

- Audio Listener: A Component that stimulates the ear of the character/camera in a Scene

- AudioSource: A Component that simulates the speaker

- AudioClip: Not a Component but rather a Sound File played by the AudioSource
