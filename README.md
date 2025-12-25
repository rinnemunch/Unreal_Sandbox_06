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
