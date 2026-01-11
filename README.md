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

--- 
# Project 4 — Foliage Tool Workflow & Instance Control

## 🖼️ Preview

![Foliage Tool Workflow](Media/4.gif)

## 🧱 Features

**Dedicated Foliage Test Levels**

- Blank level created specifically for foliage experimentation  
- Separate test level used to isolate and demonstrate Fill Mode behavior  
- Clean environments ensure foliage behavior is easy to observe and compare  

**Foliage Type Asset Setup**

- Multiple Foliage Type assets created for controlled testing  
- Individual meshes assigned per foliage type  
- Enables comparison between single-asset and multi-asset foliage workflows  

**Paint Tool Workflows**

- Single foliage asset painted independently for baseline behavior  
- Multiple foliage assets painted together to demonstrate combined placement  
- Highlights how different foliage types interact during painting  

**Erase and Remove Tool Usage**

- Erase tool used to remove foliage instances broadly  
- Remove tool used to target and clear specific foliage types  
- Demonstrates precise control over foliage cleanup and iteration  

**Single Instance Placement & Selection Cycling**

- Single Instance Mode used for manual foliage placement  
- Cycle Through Selected used to review individual instances  
- Allows inspection and adjustment without repainting  

**Fill Mode Testing and Cleanup**

- Fill Mode used to populate areas automatically with foliage  
- Remove tool applied to clear all fill-generated instances  
- Shows how to rapidly iterate without rebuilding the level  

**Reapply Tool for Instance Updates**

- Reapply tool used to modify existing foliage without repainting  
- Bush scale adjusted from 1 to 3 after instances were already placed  
- Demonstrates non-destructive updates to painted foliage  

## 🚀 Result

This project provides a practical walkthrough of Unreal Engine’s Foliage Tool, covering asset setup, painting workflows, instance selection, fill behavior, and non-destructive updates. By isolating each tool in controlled test levels, the workflow becomes predictable, repeatable, and easy to apply in real production environments.

--- 

# Project 5 — Sketchfab Asset Import & Blueprint Setup

## 🖼️ Preview

![Sketchfab Asset Import](Media/5.gif)

## 🧱 Features

**Sketchfab Asset Import Workflow**

- Sketchfab model downloaded using the glTF format  
- Asset imported into Unreal Engine with original mesh structure preserved  
- Import settings reviewed to understand mesh combination tradeoffs  

**Mesh Organization and Evaluation**

- Imported static meshes filtered and placed into the level for inspection  
- Differences between combined and non-combined meshes compared in practice  
- Visual artifacts identified on small details when meshes are combined  

**Controlled Mesh Merging**

- Meshes merged using Unreal Engine’s Merge Actors tool after inspection  
- Merge performed intentionally to balance organization and visual fidelity  
- Minor shading issues observed on detailed components such as the front emblem  

**Blueprint Conversion**

- Merged mesh converted into a reusable Actor Blueprint  
- Separate Blueprint created from non-merged meshes for lighter components  
- Blueprint setup allows independent control over body and accessory elements  

**Basic Interaction Testing**

- Simple input-driven color swap implemented on the merged body Blueprint  
- Headlight glow behavior set up on the lighting Blueprint for demonstration  
- Confirms imported assets are fully manipulatable once converted to Blueprints  

## 🚀 Result

The Sketchfab asset is transformed from a raw download into organized, reusable Blueprints that can be interacted with and extended inside Unreal Engine. The project demonstrates how proper import decisions, mesh handling, and Blueprint setup turn external assets into flexible, production-ready components.

## 📄 Credits

"2019 Chevrolet Corvette C8 Stingray" (https://skfb.ly/ooPvp) by Hari Prasath R is licensed under Creative Commons Attribution (http://creativecommons.org/licenses/by/4.0/).

--- 

# Project 6 — Media Player Video Playback with Level Sequence

## 🖼️ Preview

![Media Player Video Playback](Media/6.gif)

## 🧱 Features

**Media Player Asset Setup**

- File Media Source created and linked directly to an MP4 video  
- Media Player asset configured with auto-generated Media Texture  
- Video stored in Movies folder following Unreal Engine conventions  

**In-World Screen Rendering**

- Simple screen mesh created using a scaled cube  
- Media Texture applied directly to the mesh surface  
- Allows video playback on any static mesh or display surface  

**Level Sequence Media Control**

- Level Sequence created to manage video playback timing  
- Media Track added and bound to the File Media Source  
- Media Texture assigned in track properties for correct rendering  
- Sequence length adjusted to match video duration  

**Runtime Playback Logic**

- Level Blueprint uses Create Level Sequence Player on BeginPlay  
- Sequence Player triggered with Play Looping  
- Loop count set to infinite for continuous playback  

**Reusable Workflow**

- Works with any mesh, environment, or screen type  
- Suitable for TVs, kiosks, intro screens, and looping displays  
- Media logic remains asset-agnostic and easily reusable  

## 🚀 Result

A clean and reliable video playback system using Unreal Engine’s Media Player and Level Sequence tools. Videos play correctly at runtime with full control over looping and timing, making this setup ideal for in-world screens, showcase displays, and cinematic environments.
