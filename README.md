# Gishushu TrafficLights State Machine

**Gishushu Traffic Light State Machine Overview**
This state machine diagram represents a basic sequence of traffic light states for an intersection with two main directions: North-South and East-West. The system uses timers to control the flow of traffic in each direction and moves through a cycle of states to manage traffic safely.    

**States and Transitions**
Initial State - "North and South Red"

**Description**:
This is the starting point of the system.
***North-South direction shows RED lights***.
Vehicles on North-South roads must stop.
The East-West direction will be allowed to move next.
First Transition - "East and West Green"

***Transition:*** The system moves from "North and South Red" to "East and West Green."
East-West direction receives a GREEN light, allowing vehicles to flow.
North-South remains RED, stopping all North-South traffic.
Trigger: Initiated by the system's internal timer.
Timer Expiration & Yellow Warning - "East and West Yellow"   

****Transition****: After the green timer for East-West traffic expires, the system moves to "East and West Yellow."
East-West direction changes to YELLOW, signaling to vehicles that the light will soon turn red.
This state warns East-West traffic to prepare to stop.
Trigger: Occurs when the East-West green timer expires.
Complete Stop Phase - "East and West Red"   

***Transition:**** After the yellow timer expires for East-West traffic, the system transitions to "East and West Red."
East-West direction shows RED lights.
All East-West traffic must stop completely.
The system prepares to allow North-South traffic flow.
Trigger: Triggered by the expiration of the yellow timer.
Directional Switch - "North and South Green"   

****Transition:**** The system transitions from "East and West Red" to "North and South Green."
North-South direction receives a GREEN light, allowing vehicles to flow.
East-West remains RED, stopping all East-West traffic.
Trigger: Initiated after East-West has completely stopped.
Final Transition - "North and South Yellow"   

****Transition:**** When the green timer for North-South traffic expires, the system moves to "North and South Yellow."
North-South direction changes to YELLOW, warning vehicles to prepare to stop.
East-West remains RED.
Trigger: Occurs after the North-South green timer expires.
Back to Start - "North and South Red"   

****Transition:**** After the yellow timer for North-South expires, the system returns to the initial state, "North and South Red."
Both directions are RED, ensuring a complete stop before the cycle restarts.
The system then prepares to give the East-West direction a green light again.
Trigger: Triggered by the expiration of the yellow timer for North-South traffic.  
