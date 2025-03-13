
Legend:

<font color="#0070c0">tldr</font>

<font color="#00b050">Useful to Remember/Examples</font>

<font color="#ff0000">A Must to Memorize </font>

## Agenda

- #Intro
- #ImportanceOfGamePhysicsInGame
- #GamePhysicsConcepts
- #CollisionDetection
- #TriggerDetection


## Intro to Game Physics

A Game's Physics<font color="#ff0000"> refers to the computing motion of objects in virtual scene</font>(e.g. player, avatars npc).

These Physics are important for computing mechanical interactions of objects, because it <font color="#ff0000">provides a wonderful means for allowing a player to immerse themselves within a game.</font>



### Why is it Important?

These Physics <font color="#ff0000">improves immersion and supports new gameplay elements in a game.</font>



## Game Physics Concepts

### Kinematics

Kinematics refers to t<font color="#ff0000">he study of motion of objects/bodies without mass or force.</font>

The basic quantities of kinematics are position and time.


### Rigidbody 

Rigidbody is a <font color="#ff0000">system of particles that remain fixed distances from one another with no relative translation or rotation among them.</font>

A Rigidbody does not change its shape as it moves.


## Collision Detection

A computational Geometry problem involving <font color="#ff0000">the determination of whether and where two or more objects have collided.</font>

Common Practice to use simple shapes for collision detection that we overlay on top of the original object.

Devs can check for collisions based on simple shapes, this makes codes easier and saves on performance

<font color="#00b050">Examples</font> of such collision shapes  are circles, rectangles, spheres and boxes. Because they are a lot simpler to work with.



## Colliders and Triggers in Unity

Colliders are <font color="#ff0000">Components added to a GameObject  to detect collision</font>

A Rigidbody Component is also attached for physics properties

Primitive shapes of colliders Box, Sphere, Capsule, Circle

### Collision detection using scripting 

This is mainly used for solid interactions.

    private void OnCollisionEnter(Collision collision)
    {
         if(collision.gameobject.tag == "Goal")
         {
             Destroy(collsion.gameobject):
         }
    }

#### There are 3 Collision Events!

- OnCollsionStay( )
- OnCollisionEnter( )
- OnCollisionExit( )


YOU MUST HAVE <font color="#ff0000">RIGIDBODY AND COLLIDER</font> IN YOU GAMEOBJECT<font color="#ff0000"> IN ORDER FOR THE SCRIPT TO DETECT COLLISION!</font>


## Trigger Detection

Triggers <font color="#ff0000">gives GameObjects the ability to trigger events when an overlap happens.</font>

When a trigger is turned on the 2 objects wont collide anymore and passthrough each other.


### OnTriggerEnter( )

    private void OnTriggerEnter(Collider collision)
    {
         if(collision.gameobject.tag == "Trap")
         {
             Destroy(collision.gameObject);
         } 
    }

#### Three Trigger Events

- OnTriggerStay( )
- OnTriggerEnter( )
- OnTriggerEnter( )

MUST HAVE <font color="#ff0000">RIGIDBODY AND COLLIDER</font> IN YOUR GAMEOBJECT IN ORDER <font color="#ff0000">FOR SCRIPT TO DETECT TRIGGER EVENTS!</font>

