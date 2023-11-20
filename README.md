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

The code above will make the ball fly upwards.

## Force Modes
Force modes are modes that determine how force is applied to a physical object. 

Force modes can be used to control the behavior of physical objects in various situations.

There are four force modes available in Unity:

1. Force mode Acceleration
   
    This mode specifies the desired acceleration directly, and the physics engine will apply the appropriate force to the object to achieve that acceleration.

    This mode is very useful when you want to control the acceleration of an object independently of its mass.

    > For example, if you want to make two objects with different masses accelerate at the same rate, you would use Acceleration force mode. 

    Example :
    ```bash
    // Make a ball accelerate upwards at a constant speed.
    
    // Object initialization
    GameObject ball = new GameObject("Ball");
    Rigidbody rigidbody = ball.GetComponent<Rigidbody>();
    
    // Set physical properties
    rigidbody.mass = 1;
    
    // Add force
    rigidbody.AddForce(Vector3.up * 10f, ForceMode.Acceleration);
    ```
2. Force mode Force

   This mode is the default mode. A force is applied to the object directly, and the object will move according to the force.

   Example :
   ```bash
   // Make a ball shoot forward when pushed.
  
    // Object initialization
    GameObject ball = new GameObject("Ball");
    Rigidbody rigidbody = ball.GetComponent<Rigidbody>();
    
    // Set physical properties
    rigidbody.mass = 1;
    rigidbody.velocity = Vector3.zero;
    
    // Add force
    rigidbody.AddForce(Vector3.forward * 100);
    ```
3. Force mode Impulse

   This mode applies force suddenly. This force can be used to make the object move quickly or to change the direction of the object's movement.

   Example :
   ```bash
   // Make a ball bounce when it hits the floor.

    // Object initialization
    GameObject ball = new GameObject("Ball");
    Rigidbody rigidbody = ball.GetComponent<Rigidbody>();
    // Set physical properties
    rigidbody.mass = 1;
    // Add impulse
    rigidbody.AddImpulse(Vector3.down * 100f, ForceMode.Impulse);
   ```
   
4. Force mode Velocity Change

   This mode sets the speed of the object, which will cause it to accelerate or decelerate depending on the change in speed.

   Example :
   ```bash
   // Make the ball stop when its velocity is changed to zero.

    // Object initialization
    GameObject ball = new GameObject("Ball");
    Rigidbody rigidbody = ball.GetComponent<Rigidbody>();
    // Set physical properties
    rigidbody.mass = 1;
    // Change velocity
    rigidbody.velocity = Vector3.zero;
   ```

## Physics Materials

## Physics Joints

## Raycasting
