# Gishushu Intersection Traffic Light System

## Overview

This project models the traffic light system at the Gishushu intersection, a complex and busy traffic hub. The system controls traffic flow from multiple directions, including North-South, South-North, East-West, West-East, East-South, and South-East. The purpose of this model is to simulate the sequence and synchronization of traffic lights to ensure efficient traffic management and pedestrian safety.

## Traffic Light Sequence Specification

Each direction in the intersection follows a specific light sequence: **Green** (Go) → **Yellow** (Prepare to Stop) → **Red** (Stop). Only one direction is allowed to have a Green light at any given time to prevent cross-traffic and ensure safety.

### Directional States and Durations

The system handles six directions, each as a composite state containing its own light sequence:

1. **North-South**
   - **Green**: 60 seconds
   - **Yellow**: 5 seconds
   - **Red**: Waits until the full cycle of other directions completes

2. **South-North**
   - **Green**: 60 seconds
   - **Yellow**: 5 seconds
   - **Red**: Waits until the full cycle of other directions completes

3. **East-West**
   - **Green**: 60 seconds
   - **Yellow**: 5 seconds
   - **Red**: Waits until the full cycle of other directions completes

4. **West-East**
   - **Green**: 60 seconds
   - **Yellow**: 5 seconds
   - **Red**: Waits until the full cycle of other directions completes

5. **East-South**
   - **Green**: 60 seconds
   - **Yellow**: 5 seconds
   - **Red**: Waits until the full cycle of other directions completes

6. **South-East**
   - **Green**: 60 seconds
   - **Yellow**: 5 seconds
   - **Red**: Waits until the full cycle of other directions completes

### Overall Light Cycle

The system follows a sequential cycle:
- After the North-South direction completes its Green-Yellow-Red sequence, control passes to the East-West direction.
- Each direction follows a similar sequence, passing control to the next until it cycles back to the North-South direction.

### Pedestrian Synchronization (Optional for Future Expansion)

To ensure pedestrian safety, the Red light for each direction can be synchronized with pedestrian crossing signals. This allows pedestrians to cross the road safely when the corresponding traffic direction has a Red light.


## Usage

This model can be used to:
- Simulate and optimize traffic light systems at complex intersections.
- Test timing adjustments for improved traffic flow.
- Ensure synchronization between vehicular and pedestrian signals.
