# CFD Analysis of Flow through a 4-Cylinder Exhaust Manifold

This project presents a Computational Fluid Dynamics (CFD) analysis of a 4-cylinder exhaust manifold under steady-state flow and thermal conditions. The objective was to evaluate internal flow behavior and heat transfer of high-temperature exhaust gases (Nitrogen Oxide Plus, NO⁺) to ensure realistic engine performance and durability.

---

## Project Overview

**Timeline:** June 2025 – July 2025  
**Tools Used:**
- Autodesk Inventor – 3D CAD Modeling  
- ANSYS Fluent (Workbench) – CFD Simulation  
- CFD Post – Visualization & Analysis  

---

## Objective

To analyze flow velocity, pressure distribution, and thermal characteristics inside a 4-cylinder exhaust manifold using CFD, ensuring:
- Balanced flow merging from all cylinders  
- Realistic exhaust thermal behavior  
- Accurate heat transfer into aluminum walls for durability  

---

## Workflow Breakdown

### 1️. CAD Modeling
- Designed a 4-cylinder exhaust manifold in **Autodesk Inventor**, featuring four runners merging into a single outlet.
- Exported the CAD model as **`.STEP`** for simulation.

### 2️. Preprocessing in ANSYS Fluent

#### Geometry Preparation
- Extracted **fluid volume** using the Fill Tool.
- Defined two domains:
  - **Fluid Body:** Exhaust gas region
  - **Solid Body:** Aluminum manifold walls

#### Named Selections
`Inlet_1`, `Inlet_2`, `Inlet_3`, `Inlet_4`, `Outlet`, `Fluid_Body`, `Solid_Body`

#### Meshing
- Global element size: `5 × 10⁻³ m`
- Type: High-quality tetrahedral  
- Boundary layer refinement: **3 inflation layers**

---

## 3. Solver Setup

| Setting | Choice |
|--------|--------|
| Solver | Pressure-Based |
| Flow Type | Steady-State |
| Turbulence Model | SST k-ω |
| Energy Equation | Enabled |
| Precision | Double |

### 🔧 Material Properties
| Domain | Material |
|--------|----------|
| Fluid | Nitrogen Oxide Plus (NO⁺) |
| Solid | Aluminum (Temperature-dependent) |

### Boundary Conditions

| Boundary | Type | Condition |
|----------|------|-----------|
| Inlet_1–4 | Velocity Inlet | **30 m/s**, **800 K** |
| Outlet | Pressure Outlet | Gauge Pressure = 0 Pa, **Reverse Flow Temp = 750 K** |
| Solid–Fluid Interface | Coupled Wall | Fluid–Solid Conjugate Heat Transfer |
| Outer Wall | Convection | **h = 60 W/m²·K**, **T∞ = 300 K** |

---

## 4. Solution Setup

- Initialization: **Hybrid Initialization**
- Pressure–Velocity Coupling: **SIMPLE**
- Iterations: **1000**
- Monitored Parameters: Residuals, Max Velocity, Max Temperature
- Convergence Achieved When:
  - Energy residuals < `10⁻⁶`
  - Flow & temperature stabilized

---

## Results 

---
<img width="880" height="723" alt="View2" src="https://github.com/user-attachments/assets/23a6c7ee-a1dc-4bd6-8f7f-ccff680c950a" />
<img width="1075" height="790" alt="View1" src="https://github.com/user-attachments/assets/c012e098-e96f-4c51-a4f6-9011d6e2daf9" />
<img width="1756" height="856" alt="View" src="https://github.com/user-attachments/assets/c5c23e04-2f0f-4546-894e-85e97fd15ad8" />
<img width="1528" height="690" alt="Solid Body" src="https://github.com/user-attachments/assets/b2737d08-d27b-43de-b070-1d4de2320acf" />
<img width="1138" height="605" alt="Screenshot 2025-11-22 115842" src="https://github.com/user-attachments/assets/68786149-e25a-4979-ac29-5117e58ba22b" />
<img width="1144" height="601" alt="Screenshot 2025-11-22 115746" src="https://github.com/user-attachments/assets/2a866a4c-f5bf-4835-ad5e-253a6976d323" />
<img width="1141" height="600" alt="Screenshot 2025-11-22 115721" src="https://github.com/user-attachments/assets/0b67865b-f985-4786-bedf-8e56cfe04838" />
<img width="1142" height="605" alt="Screenshot 2025-11-22 115653" src="https://github.com/user-attachments/assets/8e24f8ff-db4c-4100-976a-3a858908904c" />
<img width="1140" height="600" alt="Screenshot 2025-11-22 115621" src="https://github.com/user-attachments/assets/69c9163e-07fd-4140-bdae-d8e4154300c9" />
<img width="1144" height="607" alt="Screenshot 2025-11-22 115535" src="https://github.com/user-attachments/assets/c5e65e0a-8353-46ef-8f10-29ca31bb58fa" />
<img width="1143" height="606" alt="Screenshot 2025-11-22 115330" src="https://github.com/user-attachments/assets/2360ff47-e700-44be-becc-2b1331d19681" />
<img width="1142" height="601" alt="Screenshot 2025-11-22 115323" src="https://github.com/user-attachments/assets/39d5991f-2eac-4e37-ac04-66a9526817d1" />
<img width="1141" height="612" alt="Screenshot 2025-11-22 115314" src="https://github.com/user-attachments/assets/88f8901b-41b2-4739-b015-7d4a8da70239" />
<img width="1530" height="668" alt="Named Selection" src="https://github.com/user-attachments/assets/cf063d28-7d99-4155-ab6a-c47b2c201045" />
<img width="1528" height="662" alt="Mesh3" src="https://github.com/user-attachments/assets/5c71ec77-3e01-4c45-84cf-58868c8aa044" />
<img width="1273" height="630" alt="Mesh1" src="https://github.com/user-attachments/assets/628b4b38-14f6-495a-8664-47d5a0f9e22b" />
<img width="1225" height="774" alt="Mesh" src="https://github.com/user-attachments/assets/60ff4f9a-e04f-46a9-bbca-2f52f3175e2b" />
<img width="1919" height="1029" alt="Geometry" src="https://github.com/user-attachments/assets/94c322f3-a63b-4054-83bf-f5b2b80ea909" />
<img width="1531" height="663" alt="Fluid Body" src="https://github.com/user-attachments/assets/6bef8fe0-c3ce-46b2-ac62-e3198eb26835" />
<img width="1919" height="1032" alt="View4" src="https://github.com/user-attachments/assets/c3c64400-7ee9-46f7-bc97-38da4eb3c8b8" />
<img width="966" height="677" alt="View3" src="https://github.com/user-attachments/assets/34f53d64-30be-4928-a59a-be935a8628ef" />


---


## 5. Post-Processing & Results

### Visualizations
- Contours of **velocity**, **static pressure**, **temperature**
- Wall **shear stress** patterns
- **Relative total pressure** loss
- Conjugate (fluid + solid) **wall temperature** distribution

### Key Observations
- Peak velocity near merge: **≈ 132 m/s**
- Max exhaust temperature stabilized at **≈ 800 K**
- Temperature gradually reduced through heat loss to convection
- Smooth pressure drop toward outlet → efficient flow merging

---

## Conclusion

The CFD simulation demonstrated realistic exhaust flow behavior under high-temperature steady-state conditions. Updated engine-like boundary conditions produced:
- Accurate internal mixing and merging of exhaust flow  
- Realistic thermal distribution within the manifold  
- Predictable pressure drop and wall heating characteristics  

This validated model can be extended to a **transient pulsating exhaust simulation** for engine firing sequence analysis.

---

### Author
**Mohammad Haris**  
Final Year B.Tech – Mechanical Engineering  
VIT-AP,Amaravati   
[Linkedin Profile](https://linkedin.com/in/mohammad-haris-13032002) | [Email](mailto:mohammaddharis1303@gmail.com)

---


