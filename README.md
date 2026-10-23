# VR Cube Challenge

## Project Overview

The **VR Cube Challenge** is a virtual reality interaction developed in Unity for the Meta Quest 3 headset. The project allows users to grab, release, and throw a cube in a 3D environment using VR interaction techniques.

The main objective is to create a natural and responsive throwing experience in which the cube reacts to the user's hand movements.

## Features

- **Grab:** The user can grab the cube using a VR interaction method.
- **Release:** The user can release the cube at any time.
- **Throw:** The cube can be thrown by moving the user's hand and releasing it.
- **Physics:** The cube uses physics to simulate realistic movement after being released.
- **Rotation:** The cube can maintain its angular movement after release.
- **Meta Quest 3 Compatibility:** The interaction is designed to run and be tested on the Meta Quest 3 headset.

## Technologies Used

- Unity
- C#
- Meta Quest 3

## How It Works

### Grabbing the Cube

The cube is configured as an interactable object in the Unity scene. The user can grab it through the selected VR interaction system. While the cube is held, its movement is controlled by the user's hand.

### Releasing the Cube

When the user releases the cube, the interaction system ends the grabbing interaction and allows the cube to move independently in the virtual environment.

### Throwing the Cube

The throwing behavior uses the movement of the user's hand to determine the cube's motion after release. The cube's velocity determines its direction and speed, while its angular velocity determines its rotation.

This allows different hand movements to produce different throwing results, making the interaction feel more natural.

## Project Setup

1. Clone or download this repository.
2. Open Unity Hub.
3. Open the project using the Unity version specified in `ProjectSettings/ProjectVersion.txt`.
4. Make sure the required packages and Meta Quest 3 development tools are installed.
5. Connect the Meta Quest 3 headset and configure the appropriate Android and XR settings.
6. Open the main scene located at `[Scene Path]`.
7. Build and run the project on the Meta Quest 3 headset.

**Note:** The project must be configured for the appropriate Meta Quest 3 build settings before running it on the headset.

## Testing

The interaction is intended to be tested directly on the Meta Quest 3 headset.

The main tests include:

- Confirming that the user can grab the cube.
- Confirming that the cube can be released correctly.
- Verifying that the cube can be thrown.
- Checking that different hand movements produce different throwing speeds and directions.
- Verifying that the cube maintains its movement and rotation after release.
- Confirming that the interaction runs correctly on the headset.

## Demo Video

A short video demonstrating the interaction running on the Meta Quest 3 will be available here:

**Video:** [Insert demo video link]

## Team Members

| Team Member | GitHub Username 
|---|---|---|
| Fátima Sofía Walls Fernández | fatimawalls (https://github.com/fatimawalls) 
| Regina López Almodovar | 0262370 (https://github.com/0262370) 

Both team members contributed to the project through meaningful code, documentation, testing, or other identifiable repository contributions.

## Repository Contents

- `Assets/` — Unity scenes, scripts, and project assets.
- `Packages/` — Unity package dependencies.
- `ProjectSettings/` — Unity project configuration.
- `README.md` — Project documentation.
- `AI_declaration.md` — AI-use declaration and relevant prompts, if submitted separately.

**Platform:** Meta Quest 3  
**Engine:** Unity  
**Language:** C#
