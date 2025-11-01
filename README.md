# CFD Analysis of Flow through a 4-Cylinder Exhaust Manifold

This project presents a **Computational Fluid Dynamics (CFD)** analysis of a 4-cylinder exhaust manifold under **steady-state flow and thermal conditions**. The primary objective was to study **velocity, pressure, and temperature distribution** of exhaust gases (Nitrogen Oxide Plus, NO⁺) within the manifold and evaluate its performance and heat transfer characteristics.

---

## Project Overview

**Timeline:** June 2025 – July 2025
**Tools Used:**

* Autodesk Inventor – 3D Modeling
* ANSYS Workbench & Fluent – Simulation Environment
* CFD Post – Visualization and Analysis

**Objective:**
To evaluate **internal flow behavior and thermal distribution** in a 4-cylinder exhaust manifold using CFD to ensure balanced exhaust flow and realistic thermal effects for improved engine performance and durability.

---

## Workflow Breakdown

### 1. **CAD Modeling**

* Designed a 4-cylinder exhaust manifold in **Autodesk Inventor**, featuring four inlets merging into a single outlet.
* Exported the model as a **STEP file** for simulation.

### 2. **Preprocessing in ANSYS Fluent**

* **Geometry Preparation:**

  * Imported the STEP file and used the *Fill Tool* to extract the **fluid domain**.
  * Created two separate domains:

    * **Fluid Body:** Represents exhaust gas volume.
    * **Solid Body:** Represents aluminum manifold walls.

* **Named Selections:**

  * `Inlet_1`, `Inlet_2`, `Inlet_3`, `Inlet_4`, `Outlet`, `Solid_Body`, `Fluid_Body`.

* **Meshing:**

  * Element Size: **5e-3 m**
  * Mesh Type: High-quality tetrahedral mesh with **3 inflation layers** on the fluid body.
  * Ensured smooth boundary layer resolution near walls.

---

### 3. **Solver Setup**

* **Solver Type:** Pressure-based
* **Flow Type:** Steady-state
* **Turbulence Model:** SST k-ω
* **Energy Equation:** Enabled
* **Precision:** Double

**Material Properties:**

* Fluid: *Nitrogen Oxide Plus (NO⁺)*
* Solid: *Aluminum*

**Boundary Conditions:**

| Boundary  | Type            | Condition   |
| --------- | --------------- | ----------- |
| Inlet_1–4 | Velocity Inlet  | 3 m/s, 60°C |
| Outlet    | Pressure Outlet | Ambient     |
| Walls     | Convection      | 60 W/m²·K   |

---

### 4. **Solution Setup**

* **Initialization:** Hybrid Initialization
* **Pressure-Velocity Coupling:** SIMPLE Scheme
* **Iteration Count:** 200
* **Monitored Parameters:** Residuals, Velocity, Temperature

---

### 5. **Post-Processing**

* **Contours:** Velocity, Temperature, and Pressure to analyze flow uniformity.
* **Vectors:** Indicated flow direction and mixing from all four inlets.
* **Pathlines:** Verified smooth flow merging and minimal recirculation zones.
* **Convergence:** Achieved with stable residuals and consistent outlet parameters.

---

## Key Results

* Flow from all four inlets merged **uniformly** with minimal turbulence.
* Outlet velocity and temperature remained within **expected physical limits**.
* The applied **convection boundary** accurately represented heat loss to the environment.
* Visualization confirmed smooth streamline convergence and realistic exhaust behavior.

---

## Skills & Tools Demonstrated

* **CFD Simulation** using ANSYS Fluent
* **CAD Modeling** using Autodesk Inventor
* **Mesh Quality Optimization** and Boundary Setup
* **Turbulence Modeling (SST k-ω)**
* **Post-Processing & Flow Visualization**
* **Engineering Problem Solving & Thermal Analysis**

---

## Results

<img width="1919" height="1032" alt="View4" src="https://github.com/user-attachments/assets/4f0828e3-54f4-49c6-a6b2-483ad9cd50f9" />
<img width="966" height="677" alt="View3" src="https://github.com/user-attachments/assets/3771fa26-78f1-40a4-b3da-ce058c2913e8" />
<img width="880" height="723" alt="View2" src="https://github.com/user-attachments/assets/d9f37613-b65b-4808-a91c-cea9202869af" />
<img width="1075" height="790" alt="View1" src="https://github.com/user-attachments/assets/08970d3e-9c15-4a49-894a-737767f2f6eb" />
<img width="1756" height="856" alt="View" src="https://github.com/user-attachments/assets/aa2f9f64-95c1-40d4-a5ab-e71b0427a536" />
<img width="1193" height="766" alt="Velocity" src="https://github.com/user-attachments/assets/8e7e600d-fce8-4565-8de6-a11331dea8a8" />
<img width="1227" height="812" alt="Velocity Vectore VM" src="https://github.com/user-attachments/assets/2026dda1-848d-4aac-8033-aae5f5726f45" />
<img width="1228" height="818" alt="Velocity Vectore ST" src="https://github.com/user-attachments/assets/46723897-eef7-49d8-bb29-a1cc25fd3434" />
<img width="1225" height="820" alt="Velocity Vectore SP" src="https://github.com/user-attachments/assets/c5afa2fd-bcb1-43c1-9be6-0314e9a899f9" />
<img width="1226" height="753" alt="Temperature" src="https://github.com/user-attachments/assets/f336bbdf-6afe-4363-80b5-3e2820d3263d" />
<img width="1528" height="690" alt="Solid Body" src="https://github.com/user-attachments/assets/b9116b97-7b15-41a1-b554-c5567eec6532" />
<img width="1308" height="642" alt="Scaled Residuals" src="https://github.com/user-attachments/assets/41ce5006-7b60-455d-83c0-b67142ddd1e8" />
<img width="1227" height="815" alt="Pathlines VM" src="https://github.com/user-attachments/assets/4a4bf1df-c27f-4dc5-ac7f-dc381d7b9f8b" />
<img width="1228" height="822" alt="Pathlines ST " src="https://github.com/user-attachments/assets/1ed0966e-4a64-4c03-9c9a-8660b2fec6ff" />
<img width="1228" height="812" alt="Pathlines SP" src="https://github.com/user-attachments/assets/973c20d3-7695-4183-90f1-b0542a125c04" />
<img width="1530" height="668" alt="Named Selection" src="https://github.com/user-attachments/assets/fe52b291-ec38-4bdb-ad81-1f8fc9c8a285" />
<img width="1528" height="662" alt="Mesh3" src="https://github.com/user-attachments/assets/350e85da-9017-4289-a7a8-bd2caf2ca568" />
<img width="1273" height="630" alt="Mesh1" src="https://github.com/user-attachments/assets/accb7f26-d5de-4d67-8d5a-84418e814a9f" />
<img width="1225" height="774" alt="Mesh" src="https://github.com/user-attachments/assets/e3bc5ca5-ca38-4ed4-be8e-2cd617684700" />
<img width="1919" height="1029" alt="Geometry" src="https://github.com/user-attachments/assets/43ced933-8767-429a-aee4-148b0a489f41" />
<img width="1531" height="663" alt="Fluid Body" src="https://github.com/user-attachments/assets/a3b22810-25cf-4cba-a131-f90d4493558c" />
<img width="1227" height="811" alt="Contours Of Static Pressure1" src="https://github.com/user-attachments/assets/91904ea5-3b44-4f95-9712-cde3355fc062" />
<img width="1223" height="816" alt="Contours Of Static Pressure" src="https://github.com/user-attachments/assets/eba8d63c-f5eb-4413-a9ba-a0ed15e1c78f" />
<img width="1228" height="794" alt="Contour Of Velocity Magnitude" src="https://github.com/user-attachments/assets/0999b186-25a4-4fdd-97d7-a3ca429ac64c" />
<img width="1226" height="773" alt="Contour of Static Pressure" src="https://github.com/user-attachments/assets/c77ec160-6367-4246-bdfe-3aa9174a3574" />

---

## 🏁 Conclusion

The CFD simulation of the 4-cylinder exhaust manifold successfully demonstrated **realistic internal flow and thermal behavior** under engine-like steady-state conditions. The setup ensured reliable predictions of **pressure drop, temperature rise, and velocity distribution**, validating the design’s efficiency and flow uniformity.

---


### Author
**Mohammad Haris**  
Final Year B.Tech – Mechanical Engineering  
VIT-AP,Amaravati   
[Linkedin Profile](https://linkedin.com/in/mohammad-haris-13032002) | [Email](mailto:mohammaddharis1303@gmail.com)


---
