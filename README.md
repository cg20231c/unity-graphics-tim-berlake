# unity-physics-engine

## Tim-Berlake

| No. | Anggota               | NRP          |
|-----|----------------------------|--------------|
| 1   | Muhammad Daffa Harits      | 5025211005  |
| 2   | Aida Fitrania Prabasati    | 5025211033  |
| 3   | Syukra Wahyu Ramadhan      | 5025211037   |

## Colliders

## Triggers

## Rigidbody

## Scripting
Scripting can be used to control the physical behavior of objects in the game.

Scripting can be used to do things like:

- Set the physical properties of objects, such as mass, speed, and position.
- Adding forces or powers to objects
- Configuring interactions between objects, such as friction and collisions.

Here are some specific examples of how scripting can be used for physics in Unity:

1. Controlling object motion: Scripting can be used to control object motion by adding forces or torques to objects.
2. Simulate interactions between objects: Scripting can be used to simulate interactions between objects, such as friction and collisions.
3. Adding special physical effects: Scripting can be used to add special physical effects, such as reverse gravity or magnetic fields.

Some commonly used methods and properties include:

- AddForce(): Adds a force to the object.
- AddTorque(): Adds torque to the object.
- SetMass(): Sets the mass of the object.
- SetVelocity(): Sets the velocity of the object.
- SetPosition(): Sets the position of the object.

Example :

```bash
// Object Initialization
GameObject ball = new GameObject("Ball");
Rigidbody rigidbody = ball.GetComponent<Rigidbody>();

// Set physical properties
rigidbody.mass = 1;
rigidbody.velocity = Vector3.forward * 10;

// Add force
rigidbody.AddForce(Vector3.up * 100);
```

## Force Modes

## About Updates

## Physics Materials

## Physics Joints

## Raycasting
