## AI Use Declaration


AI tools were used as development assistance during the project.


**AI tools used:** Google gemini


AI assistance was used for the following tasks, where applicable:


Unity setup and configuration
C# code modification
Understanding the grabb
ing, releasing, and throwing implementation
The team reviewed and tested the implementation to understand how the interaction works and to prepare to explain the code during project validation.


### Relevant Prompts

The prompts that influenced the final implementation are documented below.


1. **Prompt:** For a Unity virtual reality project that will be deployed to Meta Quest headsets, which type should I choose, the 3D Built-in Render Pipeline, or something else?
   - **AI contribution:** You should use URP (Universal Render Pipeline).

Why is URP the right choice for Meta Quest?
Performance on mobile hardware: Meta Quest headsets (Quest 2, 3, 3S, Pro) are standalone devices that run Android on Snapdragon XR2 mobile processors. URP is specifically designed to maintain the high frame rates required for virtual reality (72 to 120 FPS) without causing the headset to overheat.

Key optimizations for VR:

Single Pass Instanced Rendering: Processes the scene for both eyes in a single pass, drastically reducing draw calls and CPU load.

SRP Batcher: Optimizes the management of materials and shaders on screen.

Official support: Modern SDKs—such as the Meta XR All-in-One SDK and the OpenXR / XR Interaction Toolkit standard—are primarily geared toward and optimized for URP.

2. **Prompt:** How do I configure the XR Interaction Toolkit in Unity so that a grabbed cube preserves its velocity, rotation, and throwing momentum when released on Meta Quest 3 for a physics-based challenge mode?
   - **AI contribution:** You should configure the `XR Grab Interactable` component on the cube to use `Velocity Tracking` for movement and enable `Throw On Detach` with full velocity scale.

Why is Velocity Tracking essential for VR physics throwing?
Realistic inertia transfer: Setting the Movement Type to `Velocity Tracking` moves the object using physics forces rather than directly locking its transform to the hand. This tracks the controller's exact movement speed and direction prior to release.

Key physics settings configured:

- **Throw On Detach:** Ensures that linear velocity ($v$) and angular velocity ($\omega$) are captured at the exact moment the Grip/Trigger button is released, transferring that momentum to the object's `Rigidbody`.

- **Throw Velocity Scale (1.0):** Transfers 100% of the linear movement speed from the user's hand toss directly into the physics force of the thrown cube.

- **Throw Angular Velocity Scale (1.0):** Maintains natural rotation and spin when the object is released in mid-air.
