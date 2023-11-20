# unity-physics-engine

## Tim-Berlake

| No. | Anggota               | NRP          |
|-----|----------------------------|--------------|
| 1   | Muhammad Daffa Harits      | 5025211005  |
| 2   | Aida Fitrania Prabasati    | 5025211033  |
| 3   | Syukra Wahyu Ramadhan      | 5025211037   |

## Colliders
A collider is a component that helps define the shape and size of an object's hitbox for the purposes of collision detection during gameplay. Unity offers various types of colliders to simulate different shapes and behaviors when objects interact. Here's a brief rundown of how to use colliders in Unity for basic physics interactions:

### Adding Colliders to Game Objects:
1. Selecting the GameObject: In Unity's Hierarchy or Scene view, select the GameObject to which you want to add a collider.
2. Adding a Collider Component: In the Inspector panel, click "Add Component" and search for the collider type you want to add. Some of the common collider types are:<br>
![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/78089862/275171b0-41a4-4c4a-8311-9948c42c92cb)

   - Box Collider: Simulates a rectangular box shape.
   - Sphere Collider: Simulates a spherical shape.
   - Capsule Collider: Simulates a capsule shape.
   - Mesh Collider: Uses an object's mesh for collision detection.
   - Wheel Collider: is specifically designed for vehicle wheels and their interactions with the ground, simulating realistic driving behavior.
   - Terrain Collider: is tailored for Unity's Terrain system, enabling GameObjects to interact with terrains in a physics-based manner.
  
3. Adjusting Collider Properties: Once added, you can adjust the collider's properties such as size, position, and orientation to fit your object accurately.<br>
![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/78089862/ca826920-d62b-4847-9964-aa76d85a9060)

## Triggers
Triggers are a way to detect when objects intersect or pass through a defined area without physically interacting or causing collisions. Triggers are commonly used to create gameplay events, detect when a player enters a specific area, activate/deactivate mechanisms, or initiate scripted actions.

![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/78089862/987a8361-86c3-46fd-96b9-3930262b1aff)

### Setting Up Triggers:
1. Collider Component Setup: To create a trigger, attach a Collider component to a GameObject. This collider needs to have the "Is Trigger" checkbox enabled in the Inspector window. This setting tells Unity that this collider will act as a trigger rather than a physical collider.
2. Rigidbody (Optional): If you want the GameObject with the trigger collider to detect triggers, ensure it has a Rigidbody attached. Rigidbodies are required for collision detection in Unity.

## Rigidbody
A Rigidbody is a component that allows GameObjects to be affected by physics simulations. It enables objects to respond to forces like gravity, collisions, and applied forces, creating realistic movements and interactions within the game world.

### Basics of Rigidbody:
1. Adding a Rigidbody: To add a Rigidbody to a GameObject, select the GameObject in the Unity Editor and click "Add Component" in the Inspector window. Then search for and add the "Rigidbody" component.

2. Properties:
   
   ![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/78089862/4e034be0-8513-4593-9f3a-3c7f3098d43f)

   - Mass: The mass of the object affects how it responds to forces. Heavier objects generally require more force to move.
   - Drag and Angular Drag: These properties simulate air resistance and affect how quickly an object slows down.
   - Use Gravity: Determines if the object is affected by gravity.
   - Is Kinematic: When checked, the object is not affected by physics forces but can be moved programmatically.
   - Interpolate: Smooths object movement between physics steps, reducing visual jitter.
   - Collision Detection: Determine how accurately Unity detects collisions, influencing the reliability of collision interactions in the game.

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

## Physics Material
Controls how the frictions of surfaces interact with other surfaces.  Custom Materials can be applied to Physics Colliders.  You can specify the values for: Dynamic Friction, Static Friction, and Bounciness, as well as customize the parameters for: Friction Combine, and Bounce Combine.  To create a custom Physics Material, select from the top menu drop-down: Assets > Create > Physics Material, and add it to your GameObject by selecting the newly created Physic Material in the Project window, and dragging it to the GameObject’s Material property in the Inspector.  
![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/90988646/537b38c2-7d40-4a9a-94d3-aee13919f9dd)
In Physics Material you can set the dynamic friction, static friction, and bounciness
  - Dynamic Friction is force that control the movespeed of an object
  - Static Friction is a force that can prevent an object from sliding down a sloped surface.
  - Bounciness is a variable that controll the bounciness of an object

## Joints
A Joint Component connects a Rigidbody to another Rigidbody or a fixed point in space. Joints
apply forces that move rigid bodies. Joint limits also can restrict certain movements.  The types of Physics Joints include Character Joint, Configurable Joint, Fixed Joint, Hinge Joint, and Spring Joint (
  - Fixed Joint : Restricts the movement of a Rigidbody to follow the movement of the Rigidbody it is attached to. This is useful when you need Rigidbodies that easily break apart from each other, or you want to connect the movement of two Rigidbodies without parenting in a Transform hierarchy.
    ![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/90988646/434aba0f-c43b-4fb9-bdf5-ba07ce14b79b)
  - Spring Joint : Keeps Rigidbodies apart from each other but lets the distance between them stretch slightly. The spring acts like a piece of elastic that tries to pull the two anchor points together to the exact same position.
    ![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/90988646/a7f6cb25-2f81-44f5-b035-170df45e049f)
  - Hinge Joint: Attaches a Rigidbody to another Rigidbody or a point in space at a shared origin and allows the Rigidbodies to rotate around a specific axis from that origin. Useful for emulating doors and finger joints.
    ![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/90988646/11ecbf73-68fd-438e-a82e-78cc31be85e1)
  - Character Joint Emulates a joint of a character, such as a hip or shoulder joint.  This constrains Rrigidbody movement along all linear degrees of freedom, and enables all angular freedoms. Rigidbodies attached to a Character Joint orient around each axis and pivot from a shared origin.
    ![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/90988646/a6967a0c-565a-458c-b563-ef3d3fe2b2a0)
  - Configure Joint : Emulates any skeletal joint, such as the joints in a ragdoll. You can configure this joint to force and restrict Rigidbody movement in any degree of freedom.
    ![image](https://github.com/cg20231c/unity-graphics-tim-berlake/assets/90988646/a523dbc2-4a41-4ece-a78b-3497f583b1fb)

