# Repository-4-Helical-Gear-Design

## Overview

This project is a Python-based engineering tool developed for the preliminary design and analysis of a helical gear. The program calculates gear geometry, loading conditions, and basic structural strength parameters from user-defined inputs. It also provides a simple graphical visualization of tooth positions around the gear circumference using Matplotlib.

The code demonstrates the application of machine design principles, gear geometry calculations, force analysis, and basic stress evaluation in a structured object-oriented framework.

---

## Features

### Geometry Analysis

The program computes:

* Transverse Module
* Pitch Diameter
* Base Diameter
* Addendum
* Dedendum
* Whole Depth
* Outside Diameter
* Root Diameter
* Clearance
* Transverse Pressure Angle
* Transverse Pitch
* Axial Pitch

### Loading Analysis

The program calculates:

* Tangential Force
* Radial Force
* Axial Force
* Resultant Force

based on user-specified torque and rotational speed.

### Strength Analysis

The program estimates:

* Bending Stress
* Factor of Safety

using the calculated tangential load and material strength.

### Visualization

A Matplotlib-based plot displays the approximate tooth positions around the circumference of the designed helical gear.

---

## Theory

### Pitch Diameter

d = z × m_t

where:

* d = Pitch Diameter
* z = Number of Teeth
* m_t = Transverse Module

### Tangential Force

F_t = 2T / d

where:

* T = Applied Torque
* d = Pitch Diameter

### Radial Force

F_r = F_t tan(φ_t)

where:

* φ_t = Transverse Pressure Angle

### Axial Force

F_a = F_t tan(β)

where:

* β = Helix Angle

### Resultant Force

F_r = √(F_t² + F_r² + F_a²)

### Factor of Safety

FoS = Material Strength / Bending Stress

---

## Code Structure

### HelicalGearGeometry

Responsible for:

* Gear geometric calculations
* Diameter calculations
* Tooth geometry parameters

### GearLoading

Responsible for:

* Tangential load calculations
* Radial load calculations
* Axial thrust calculations
* Resultant force calculations

### GearStrength

Responsible for:

* Bending stress estimation
* Factor of safety calculation

---

## Inputs (Example)

| Parameter         | Unit    |
| ----------------- | ------- |
| Module            | mm      |
| Number of Teeth   | -       |
| Helix Angle       | Degrees |
| Pressure Angle    | Degrees |
| Torque            | N·mm    |
| Speed             | RPM     |
| Material Strength | MPa     |
| Face Width        | mm      |

Data given:

```python
module = 4
number_of_teeth = 20
helix_angle = 15
pressure_angle = 20

torque = 3000
speed = 1500

material_strength = 300
face_width = 40
```

---

## Output (Example)

### Gear Geometry

```text
Pitch Diameter = 82.82 mm
Base Diameter = 77.83 mm
Addendum = 4.00 mm
Dedendum = 5.00 mm
Whole Depth = 9.00 mm
```

### Gear Forces

```text
Tangential Force        : 72.44 N
Radial Force            : 27.30 N
Axial Force             : 19.41 N
Resultant Force         : 79.81 N
```

### Strength Analysis

```text
Bending Stress          : 174.94 MPa
Factor of Safety        : 1.71
```

---

## Visualization

The program generates a Matplotlib plot showing the angular positions of the gear teeth around the circumference.

The plot provides a simple visual representation of:

* Pitch Circle
* Tooth Distribution
* Gear Symmetry

---

## Installation

Install the required dependencies:

```bash
pip install matplotlib
```

---

## Running the Program

```bash
python helical_gear.py
```

---

## Limitations

Current implementation uses simplified analytical equations and is intended for educational and preliminary design purposes.

The following are not currently implemented:

* AGMA Design Standards
* ISO 6336 Design Verification
* Hertzian Contact Stress
* Wear Analysis
* Dynamic Loading Effects
* Fatigue Analysis
* Finite Element Validation

---

## Future Improvements

Planned developments include:

* AGMA-based design calculations
* Contact stress evaluation
* Material database integration
* Automatic gear sizing
* 3D gear visualization
* CAD model export
* FEA integration using ANSYS

---

## Author

Muskan Borgohain

* Mechanical Design
* Computational Engineering
