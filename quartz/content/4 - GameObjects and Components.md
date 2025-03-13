This one is a pretty short and easy chapter, which... thank god. Anyway, we have only 2 things to cover here.

1. Relationship Between Game Objects and Components
2. Components Declaration and Integration


# Relationship Between Game Objects and Components

The greatest yaoi.

As you all know, Game Objects are objects in a game. The player, the enemies, the guns, the bullets, that one crate, the world, they're all just game objects in a scene.

However, each of these game objects have components (presumably). Components are things that make the objects themselves do the things that they do. They are the functional pieces of a game object.

In Unity, all game objects have a transformation component when crafted, which lets it have a position.

To add a component, you'd select a game object, move your focus to the bottom of the inspector window and click the "Add Component" button, where you can add any component that Unity has.

You can attach any number of components to a single game object. Components are also flexible by design, meaning that there are specific values that pertain to that specific component that you can change yourself. An example would be the mass of a rigidbody, or the size of a box collider.

Examples of components include:
- Renderer
	- For rendering objects to be visible in a game. If you want an object to be there and invisible, turn this component off.
- Collider
	- Defines the collision boundary area of an object. If you want the object to not detect any collision at all (including ground, player, enemy, projectile, etc.), turn this component off.
- Rigidbody
	- Defines physics i.e weight, gravity, etc.
- Animator
	- Controls which animation plays depending on the state that the object is in. Holds multiple animations within the component.
- Light
	- Defines the type of light source (directional, spot, point, area) in a game.

# Components Declaration and Integration

In a script, you can have control over these components. Of course, the first thing you need to do is to create a variable to store these components into.

Remember how variables need to have their type declared? That still applies here. Luckily for us, the variable type is the same as the component name. For example, if we wanted to create a variable for us to store our player animator component into, we can do...
```
public Animator playerAnim;
```

If the variable is public, like the example shown above, we can just drag the game object that contains the animator into the variable slot in the inspector. However, we can still get the component if the variable is private using the GetComponent method.


If the script and the component are on the same game object, then...
```
private Animator playerAnim;

public void Start()
{
	playerAnim = GetComponent<Animator>();
}
```



However, if the script and the component are on two different game objects, then you'll need to get the game object with the component and store it in a variable too.
```
public GameObject player;
private Animator playerAnim;

public void Start()
{
	playerAnim = player.GetComponent<Animator>();
}
```


---
Like I said, pretty short chapter.

\- Mikhail

Next Chapter: [[5 - Textures, Materials, Lights]]