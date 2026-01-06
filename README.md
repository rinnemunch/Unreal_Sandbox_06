# Project 1 – Walk Through Chaos Fracture Debris

## 🖼️ Preview

![Walk Through Chaos Fracture Debris](Media/1.gif)

## 🧱 Features

**Chaos Geometry Collection Setup**

- Static mesh converted into a Chaos Geometry Collection using Fracture Mode
- Cluster Fracture applied multiple times to generate layered debris
- Damage Threshold values tuned per fracture level for responsive destruction

**Reusable Actor Blueprint**

- Custom Actor Blueprint created to encapsulate Geometry Collection behavior
- Geometry Collection component assigned via Rest Collection
- Blueprint-based setup allows easy reuse across levels and projects

**Physics-Only Collision Profile**

- Custom collision preset configured to disable query collision
- Pawn, Camera, and Visibility channels ignored
- Fracture debris continues simulating physics without blocking player movement

**Per-Level Collision Control**

- Collision Profile Per Level used to separate root cluster and fractured pieces
- Root cluster retains default collision before breaking
- Child fracture levels switch to physics-only collision after destruction

## 🚀 Result

The Geometry Collection fractures naturally under physics simulation while allowing the player to move cleanly through debris. Gameplay remains smooth and responsive, with realistic Chaos destruction that no longer interferes with player movement. 

---

# Project 2 — Crouch System (Enhanced Input)

## 🖼️ Preview

![Crouch System](Media/2.gif)

## 🧱 Features

**Enhanced Input**
- Dedicated crouch input action created using Enhanced Input  
- Toggle-based crouch behavior instead of hold input  
- Key binding handled through the default input mapping context  

**Character Movement**
- Built-in Character Movement crouch support enabled  
- Custom crouched capsule half height for cleaner collision  
- Reduced crouched walk speed for grounded movement feel  
- Airborne check prevents crouching while jumping or falling  

**Crouch Toggle Logic**
- Boolean toggle tracks crouch state cleanly  
- Single input switches between crouch and stand  
- UnCrouch handled safely when space above is clear  

**Camera Smoothing**
- Camera lag enabled dynamically during crouch  
- Prevents hard snapping when capsule height changes  
- Maintains smooth visual transitions during state changes  

**Animation Blueprint Integration**
- Dedicated crouched idle and crouched walk animation states  
- Transition rules driven by movement state  
- Looping crouch walk animation for continuous motion  

**State Aliases**
- Centralized entry and exit points for crouch transitions  
- Clean transitions from idle and walk into crouch  
- Unified return path back to standing states  

**Animation Sync**
- Crouch state pulled directly from Character Movement  
- Animation Blueprint updated every frame  
- Ensures animation state always reflects true movement state  

## 🚀 Result

A clean, reusable crouch system built on Unreal Engine’s native movement features, enhanced input, and readable animation logic — ready to drop into future third-person projects without rework.

--- 

# Project 3 — Chaos Vehicle Configuration Tuning

## 🖼️ Preview

![Chaos Vehicle Configuration Tuning](Media/3.gif)

## 🧱 Features

**Multi-Vehicle Configuration Comparison**

- Three distinct vehicle types configured and tested: sports car, SUV, and box truck  
- Identical baseline values applied initially to expose behavior differences  
- Per-vehicle tuning performed to demonstrate how configuration must adapt to scale and intent  

**Wheel Configuration and Ground Contact**

- Wheel radius adjusted per vehicle to ensure proper ground contact  
- Front and rear wheels tuned independently where necessary  
- Wheel mass adjusted to influence suspension response and vertical movement  

**Vehicle Mass and Center of Mass Control**

- Vehicle mass tuned per platform to reflect real-world weight expectations  
- Center of mass overrides used to stabilize acceleration and braking behavior  
- Mesh-level center of mass offsets refined to reduce exaggerated pitch and lift  

**Engine and Torque Curve Tuning**

- Torque curves reshaped to control how power is delivered across RPM ranges  
- Progressive torque delivery used to prevent traction loss and instability  
- Engine output scaled appropriately for vehicle type rather than relying on top speed alone  

**Transmission and Acceleration Behavior**

- Gear ratios adjusted to control responsiveness and launch characteristics  
- Shorter gearing used for lighter vehicles to improve acceleration  
- Slower, delayed power delivery applied to heavier vehicles to preserve realism  

**Traction and Handling Adjustments**

- Rear wheel friction multipliers increased where necessary to reduce wheel spin  
- Traction tuned alongside torque and transmission changes  
- Focus placed on controllability over arcade-style responsiveness  

**Reusable Tuning Workflow**

- Configuration process structured for repeatability across new assets  
- Changes isolated per vehicle to prevent shared-value conflicts  
- Provides a clear framework for diagnosing vehicle behavior issues  

## 🚀 Result

Each vehicle now behaves in a way that aligns with its intended role. The sports car delivers responsive acceleration with controlled traction, the SUV maintains a heavier and more compliant ride, and the box truck accelerates gradually while preserving realistic weight and momentum. Together, these configurations demonstrate how thoughtful tuning of Chaos Vehicle systems can produce predictable, controllable, and vehicle-appropriate behavior across a wide range of assets.
