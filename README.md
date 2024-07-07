# Electronics Task 1

## Design an algorithm to control 6 servo motors for robot movement.
### 1. Understanding Human Walking Biomechanics
The human walking gait is comprised of two phases. Phase 1 is the stance phase where one leg is on the ground supporting the body. Phase 2 is the swing phase when the other leg is lifted and moved forward. 

![The-gait-cycle-can-be-divided-into-the-stance-phase-weight-bearing-and-swing-phase](https://github.com/Alaa3172/ElectronicsTask1/assets/173661540/c5331473-f1e9-46e1-840f-13d3c161829a)

### 2. Mapping Servo Motors to Joint Movements
* hip joints (2 servos): control forward/backward movement
* knee joints (2 servos): control flexion/extension
* ankle/foot joints (2 servos): control dorsiflexion/plantarflexion
### 3. Key Movements
- Stance Leg (Supporting Leg): Hips, knees, and feet kept at 90 degree angle.
- Swing Leg (Moving Leg): Hips and feet move forward at 45 degree angle while knee bends backwards to 135 degree angle.
### 4. Algorithm 
__Initialization__:
Attach the servos to the corresponding pins for each joint: left hip, left knee, left ankle, right hip, right knee, right ankle.

__Main Loop__:
Begin a continuous loop to control the robot's movement sequence.

__Movement Sequence__:

_Step 1: Move Right Leg Forward_
* Adjust the right hip to move the leg forward.
* Bend the right knee.
* Adjust the right ankle.
* Maintain this position for a brief delay to simulate stepping.
  
_Step 2: Return Right Leg to Neutral_
* Return the right hip to the neutral position.
* Straighten the right knee.
*Return the right ankle to the neutral position.
* Maintain this position for a brief delay.

_Step 3: Move Left Leg Forward_
* Adjust the left hip to move the leg forward.
* Bend the left knee.
* Adjust the left ankle.
* Maintain this position for a brief delay.
  
_Step 4: Return Left Leg to Neutral_
* Return the left hip to the neutral position.
* Straighten the left knee.
* Return the left ankle to the neutral position.
* Maintain this position for a brief delay.
  
_Repeat:_
* Continuously repeat the movement sequence from Step 1 to Step 4.
