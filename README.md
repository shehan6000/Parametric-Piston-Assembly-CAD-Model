# Parametric Piston Assembly CAD Model

A multi-component parametric CAD model and motion assembly of an internal combustion engine piston mechanism. Built using top-down design principles, this project demonstrates clean sketching, structural component modeling, fastener integration, and mechanical joint assignment.
---

## Component Breakdowns & Modeling Workflow

The design process follows a systematic, top-down modeling workflow to maintain strict dimensional relationships between intersecting moving parts.

### 1. Architectural Strategy & Component Initialization

* Established a global coordinate system and initialized a component hierarchy to prevent cross-talk between component timelines.
* Enforced parametric constraints right from the start to allow for sweeping adjustments to bore, stroke, and pin diameters seamlessly.

### 2. The Piston Engine Core

* **Piston Head Architecture:** Developed the crown profile using advanced symmetric sketching and a primary `Revolve` operation.
* **Internal Geometry:** Cleared weight pockets and drafted the internal structural ribs using targeted `Extrude` operations with taper angles.
* **Precision Bores:** Executed multi-step cuts for the compression ring grooves, oil scraper rings, and the high-tolerance wrist pin bore.

### 3. Linkage & Structural Design

* **Connecting Rod:** Modeled a high-strength structural rod profile. Utilized mirrored web sections to achieve an optimized weight-to-strength ratio, transitioning smoothly into the small-end and big-end bores.
* **Connecting Rod Cap:** Designed the split-journal cap profile featuring precision counterbores engineered specifically to sit flush with standard industrial fasteners.
* **Wrist Pin:** Modeled a precision-clearance, hollow cylindrical pin optimized to balance mass reduction with shear-stress distribution.

### 4. Fastener Integration & COTS Parts

* Imported and constrained industrial **12-Point Screws** (via McMaster-Carr / standard components catalog) to secure the rod cap to the connecting rod body, ensuring correct pitch and thread alignment.

---

## Assembly & Mechanical Motion

Components are bound using localized mechanical joints rather than absolute positioning, allowing for kinematic validation of the assembly:

| Joint Name | Component A | Component B | Motion Type | Degrees of Freedom |
| --- | --- | --- | --- | --- |
| **Wrist Pin - Piston** | Piston Pin Bore | Wrist Pin | Rigid / Cylindrical | 0 / 2 DoF |
| **Rod - Wrist Pin** | Connecting Rod Small-End | Wrist Pin | Revolute | 1 DoF (Rotation) |
| **Rod - Cap Link** | Connecting Rod Big-End | Rod Cap | Rigid | 0 DoF |
| **Cap Fasteners** | Rod Cap Bores | 12-Point Screws | Rigid | 0 DoF |

---
<img width="1740" height="732" alt="Screenshot 2026-05-16 125643" src="https://github.com/user-attachments/assets/2325533d-b473-4781-8faa-b07697e90770" />
<img width="440" height="317" alt="Screenshot 2026-05-16 130157" src="https://github.com/user-attachments/assets/5d63e1ed-53a4-4c04-a2bc-6938cf9c30a1" />
<img width="387" height="261" alt="Screenshot 2026-05-16 130139" src="https://github.com/user-attachments/assets/322dd8be-77c5-48be-9ad7-3c12109abaf4" />
<img width="511" height="485" alt="Screenshot 2026-05-16 130116" src="https://github.com/user-attachments/assets/6c377c88-9dc2-41df-b3d2-d8dca4eea083" />
<img width="536" height="402" alt="Screenshot 2026-05-16 130047" src="https://github.com/user-attachments/assets/7a1a5217-0bab-4e5b-b337-d2b050d27d0d" />


https://github.com/user-attachments/assets/c2cdf07a-1db1-4f38-8538-18d565cd89f7





