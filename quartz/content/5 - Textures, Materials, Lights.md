3 things to focus on here, and they're all in the title.

# Materials
The purpose of materials are to define how a game object would look in game, and how its surface would be rendered. A material itself is a file that contains info about the lighting of an object. Both [[#Shaders|shaders]] and materials define how a 3D object looks in terms of colors, reflectivity and textures.

## Shaders
A shader is a program that defines how every pixel is drawn on screen. They contain logic that tells the computer how to render each pixel.


## Creating a Material

To create a material:
- Right click an empty space in the asset window (Unity's file explorer)
	- Click "Create"
		- Click "Material"
			- Type a name out for the material

Properties of the material are controlled via the inspector window. Actually, these properties come from the shader that the material uses.


# Textures
These are bitmap images applied over a mesh surface. It gives the fine details of an object.

## Importing Textures
These bitmap images can be created via Photoshop, or any other digital image content creation application.

The image will then be imported into Unity and assigned to a newly created material.

There are different texture maps, and we'll be going through each of these next. They might be a lot, so bear with me here.


## Diffuse Map
Displays textures that has __base color information__; which color, texture or pattern of the material will be shown on the model itself.

## Normal Map
These are a special kind of texture that allow you to add kinds of surface details such as **bumps, grooves and scratches**. These details catch light, as if represented by real geometry, essentially making it look like they are part of the model itself.

It turns color channels into a format suitable for real-time normal mapping.

## Occlusion Map
Used to provide info about which areas of the model **should recieve higher or lower indirect lighting**. Indirect lighting comes from ambient lighting and reflections, so parts like cracks and folds should not receive much indirect lighting.

## Height Map
AKA Parallax Mapping, it works in conjunction with [[#Normal Map|normal maps]] to give extra definition to surfaces.

If you have a brick wall texture, this makes each brick pop out as it would look realistically.![[Pasted image 20250312125132.png]]


# Light Types

There are 4 types of lights in Unity.

- Directional
- Point
- Spot
- Area

## Directional Light
This represents **large, distant sources** of light that come from **outside of the game world**. Sound familiar?

Yeah, this is usually used as the __sun__ in games. Moons too, I suppose. This light **simulates the sun/moon** on a scene.

The **position of the light does not matter**, and the rotation of the light affects the angle of the sun, which changes the position and angle of shadows.

## Point Light
This one is located in a **specific point in space** and **equally sends out light in all directions**. It has a **specified range** which can be changed in the Inspector. It is indicated by the yellow circles around the light.

These are mostly used to simulate lightbulbs, lamps, and campfires.

## Spot Light
Similar to [[#Point Light]], this one also covers a specific location. However, spotlights emits **light in one direction** and is constrained to a **specific angle**, resulting in a **cone shape** of a light.

This conic shape is similar to, well... spotlights, in real life.

## Area Light
Area lights are projected **only on one side**, and emits light in a **rectangular shape**. However, they need to be **baked** before they can take effect.

Examples are TV screens, computer screens and ceiling lights.

---
And that's it from me! Jabriel will be taking the rest. Good luck for your exams!

\- Mikhail
