# CFD Analysis of Flow Through a 4-Cylinder Exhaust Manifold

This repository contains a **CFD simulation of a 4-cylinder automotive exhaust manifold** under **steady-state turbulent flow and conjugate heat transfer (CHT)** using **ANSYS Fluent**.  
The study evaluates exhaust **velocity behavior, heat transfer, pressure distribution, and wall shear stress** for realistic engine exhaust conditions.

---

## Software & Tools

| Software | Purpose |
|----------|--------|
| **Autodesk Inventor** | 3D CAD Modelling |
| **ANSYS Fluent (Workbench)** | Turbulent & Thermal CFD |
| **ANSYS Mesh** | Volume Meshing |
| **CFD-Post** | Post-processing & result visualization |

---

## Objective

To simulate exhaust gas flow inside the manifold to understand:

- **Heat transfer** to the aluminum walls (Conjugate Heat Transfer)
- **Velocity merging behavior** from four runners
- **Pressure drop & losses**
- **Wall shear stress regions**

---

## 1. CAD Modelling

The manifold geometry is created in Autodesk Inventor and exported as `.STEP`.


---

## 2. Geometry Preparation & Domain Setup

Using the **Fill tool**, the **fluid region** was extracted and **solid metal region** preserved for CHT.

**Extracted Domains**
- `Fluid_body` → Exhaust gas
- `Solid_body` → Aluminum manifold wall

 Named selections include: `Inlet_1...4`, `Outlet`, `Fluid_Body`, `Solid_Body`.

---

## 3. Meshing

| Property | Value |
|----------|-------|
| Mesh Type | Tetrahedral |
| Global Size | 5 × 10⁻³ m |
| Inflation Layers | 3 |
| Skewness | < 0.85 |


---

## 4. Solver Setup

| Setting | Value |
|--------|------|
| Solver | Pressure-Based |
| Flow Type | Steady-State |
| Turbulence Model | **SST k-ω** |
| Energy Equation | Enabled |
| Precision | Double |
| Initialization | Hybrid |
| Scheme | SIMPLE |

### Material Properties

| Region | Material |
|--------|----------|
| Fluid | Nitrogen Oxide Plus (NO⁺) |
| Solid | Aluminum (Temperature dependent) |

### Boundary Conditions

| Boundary | Type | Specification |
|----------|------|----------------|
| Inlet 1–4 | Velocity Inlet | 30 m/s, 800 K |
| Outlet | Pressure Outlet | 0 Pa, 750 K reverse flow |
| Walls | Conjugate Coupled | CHT enabled |
| Ambient Cooling | Convection | h = 60 W/m²·K, T∞ = 300 K |

---

## 5. Results & Post-Processing

### 🔷 Velocity Magnitude (m/s)

- Peak velocity near collector: **≈ 132 m/s**
- Strong acceleration where flows merge


---

### Static Temperature Distribution (K)

- Exhaust temp drops due to wall heat absorption
- Fluid: 800 K → 500–620 K  
- Wall: High temp zones at collector


---

### Wall Shear Stress (Pa)

- Maximum near collector → fatigue hotspot
- Important for material & weld design


---

### Relative Total Pressure (Pa)

- Predictable pressure drop from runners to outlet
- Minimum losses at outlet region


---


<img width="1919" height="1032" alt="View4" src="https://github.com/user-attachments/assets/e7f74370-b648-475b-98bc-a4c84d542a15" />
<img width="966" height="677" alt="View3" src="https://github.com/user-attachments/assets/c4b26347-8808-486d-b677-af770a8843cc" />
<img width="880" height="723" alt="View2" src="https://github.com/user-attachments/assets/758cd34a-032c-46f8-b865-ac5645e69fc1" />
<img width="1075" height="790" alt="View1" src="https://github.com/user-attachments/assets/a85af24b-2c37-4dcc-98aa-796a98ff13b0" />
<img width="1756" height="856" alt="View" src="https://github.com/user-attachments/assets/6d44c510-7dc5-4d10-8ade-43a72e2d505a" />
<img width="1530" height="668" alt="Named Selection" src="https://github.com/user-attachments/assets/bc77a839-286e-49dd-9604-5bb5e076e65d" />
<img width="1528" height="662" alt="Mesh3" src="https://github.com/user-attachments/assets/7b7c6888-6661-4b6f-861d-2a407f0c36df" />
<img width="1273" height="630" alt="Mesh1" src="https://github.com/user-attachments/assets/abe853e3-be50-4006-9c20-22224a387b7b" />
<img width="1528" height="690" alt="Solid Body" src="https://github.com/user-attachments/assets/48dab3fb-5fd3-4c30-968f-a319ee590140" />
<img width="1225" height="774" alt="Mesh" src="https://github.com/user-attachments/assets/b055755c-d960-427e-9062-97ad2b2b2faf" />
<img width="1919" height="1029" alt="Geometry" src="https://github.com/user-attachments/assets/cde1d6aa-85c0-4973-9a64-fcfa73746306" />
<img width="1531" height="663" alt="Fluid Body" src="https://github.com/user-attachments/assets/f173b1b5-b7b3-420d-b065-527e1f47fb7c" />
<img width="1138" height="605" alt="Screenshot 2025-11-22 115842" src="https://github.com/user-attachments/assets/f5bbfe60-3c08-4f37-b3b6-84b56003928a" />
<img width="1144" height="601" alt="Screenshot 2025-11-22 115746" src="https://github.com/user-attachments/assets/9bdbd41e-8454-49b4-b476-7134a3950be5" />
<img width="1141" height="600" alt="Screenshot 2025-11-22 115721" src="https://github.com/user-attachments/assets/a5610cca-e7ab-4b5d-855f-063a59a68000" />
<img width="1142" height="605" alt="Screenshot 2025-11-22 115653" src="https://github.com/user-attachments/assets/54f7c27f-520e-45c1-bd0e-179c4c314b0b" />
<img width="1140" height="600" alt="Screenshot 2025-11-22 115621" src="https://github.com/user-attachments/assets/a6aa8e72-9592-4559-b155-6790ccad95c5" />
<img width="1144" height="607" alt="Screenshot 2025-11-22 115535" src="https://github.com/user-attachments/assets/8fd9e8af-49bd-4275-ba8d-ffa2f7be47a0" />
<img width="1143" height="606" alt="Screenshot 2025-11-22 115330" src="https://github.com/user-attachments/assets/2999ffed-b25d-4467-a03f-eda484dfa41d" />
<img width="1142" height="601" alt="Screenshot 2025-11-22 115323" src="https://github.com/user-attachments/assets/4318e796-abc1-47ef-a660-b2dc6caeb5c4" />
<img width="1141" height="612" alt="Screenshot 2025-11-22 115314" src="https://github.com/user-attachments/assets/096c2465-ad27-4ef0-98ee-796cc7a40f42" />



---

## Conclusion

✔ Realistic exhaust flow merging  
✔ Accurate heat transfer prediction (solid + fluid)  
✔ Pressure & velocity trends match expected engine behavior  
✔ High wall shear zones identified for durability improvement


---

### Author
**Mohammad Haris**  
Final Year B.Tech – Mechanical Engineering  
VIT-AP,Amaravati   
[Linkedin Profile](https://linkedin.com/in/mohammad-haris-13032002) | [Email](mailto:mohammaddharis1303@gmail.com)

---


