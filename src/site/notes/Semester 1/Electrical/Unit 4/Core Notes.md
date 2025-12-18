---
{"dg-publish":true,"permalink":"/semester-1/electrical/unit-4/core-notes/"}
---

# [[Semester 1/Electrical/Electrical\|Back]]
***
[[Semester 1/Electrical/Unit 4/Core Notes\|Core Notes]] | [[Semester 1/Electrical/Unit 4/Questions\|Questions]] | [[Semester 1/Electrical/Unit 4/pyqs\|PYQs]] | [[Semester 1/Electrical/Unit 4/mcqs\|MCQs]]
***

# Unit 4: Electromagnetism & Electrical Machines

## 1. Electromagnetism Basics

### 1.1 Magnetic Quantities
*   **Magnetic Flux ($\phi$)**: The total magnetic lines of force produced by a magnet. Unit: **Weber (Wb)**.
*   **Magnetic Flux Density ($B$)**: Flux per unit area normal to the flux. $B = \phi / A$. Unit: **Tesla (T)** or $Wb/m^2$.
*   **Magnetizing Force ($H$)**: The force exerted by a unit pole placed at a point in the field. Also called Magnetic Field Intensity. $H = NI / l$. Unit: **Ampere-turns/meter (AT/m)**.
*   **Magneto Motive Force (MMF)**: The driving force that sets up flux. $MMF = N \times I$. Unit: **Ampere-turns (AT)**.

### 1.2 Reluctance and Permeability
*   **Reluctance ($S$)**: Opposition offered by a magnetic circuit to the magnetic flux. Analogous to Resistance in electric circuits.
    $$ S = \frac{l}{\mu_0 \mu_r A} $$
    Where $l$ is length, $A$ is area, $\mu_0$ is permeability of free space ($4\pi \times 10^{-7}$), $\mu_r$ is relative permeability.
*   **Relation between B and H**:
    $$ B = \mu H = \mu_0 \mu_r H $$

### 1.3 B-H Curve and Hysteresis
The **B-H Curve** (Magnetization Curve) plots Flux Density ($B$) vs Magnetizing Force ($H$).
*   **Saturation**: The point where increasing $H$ yields no significant increase in $B$.
*   **Hysteresis Loop**: The loop formed by the B-H curve when a magnetic material is magnetized, demagnetized, and re-magnetized in the opposite direction.

    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" height="400" width="Hysteresis Loop"><path d="M0 0v400h800V0z" fill="#fff"/><path d="M508.59 193.69c-1.295 64.668-1.998 154.014-38.004 165.35v.002c218.997.747 213.749-56.53 218.014-122.902m0 0c1.295-64.667 1.998-154.013 38.005-165.35-218.998-.748-213.75 56.528-218.015 122.9M188.59 193.69c-9.86 64.92-10.752 150.095-118.004 165.35v.002c119.4-.02 124.933-57.033 138.014-122.902m0 0c9.86-64.92 10.752-150.094 118.005-165.35-119.4.018-124.933 57.032-138.015 122.9" fill="#f2f2f2"/><g id="a"><path stroke-width="2" fill="none" d="M18.384 216.88h314.833" stroke="#000" stroke-linecap="round" stroke-linejoin="round"/><g stroke="#000" stroke-linecap="round" stroke-linejoin="round"><path d="M240.381 111.863l3.744 21.444h-7.488z" transform="translate(-41.98 -93.5)"/><path stroke-width="2" fill="none" d="M198.402 384.46V38.064"/></g><path d="M354.92 216.88l-21.444 3.745v-7.489z" stroke="#000" stroke-linecap="round" stroke-linejoin="round"/><g font-family="serif" stroke-linecap="square" stroke-miterlimit="10" stroke-width="1.292"><text x="185.805" y="91.886" font-size="12" style="line-height:0%" transform="translate(31.21 81.382) scale(1.7037)">B</text><text x="194.338" y="95.446" font-size="10.258" style="line-height:0%" transform="translate(31.21 81.382) scale(1.7037)">err</text></g><g stroke-width="1.292" stroke-miterlimit="10" stroke-linecap="square" font-family="serif"><text style="line-height:0%" font-size="12" y="91.886" x="185.805" transform="translate(-174.372 -115.191) scale(1.7037)">B</text><text style="line-height:0%" font-size="10.258" y="95.446" x="194.338" transform="translate(-174.372 -115.191) scale(1.7037)">ges</text></g><text style="line-height:0%" font-size="20.444" y="238.351" x="179.536" font-family="serif" stroke-width="2.202" stroke-linecap="square" stroke-miterlimit="10">0</text><text x="179.536" y="238.351" font-size="20.444" style="line-height:0%" font-family="serif" stroke-width="2.202" stroke-linecap="square" stroke-miterlimit="10">0</text></g><use height="100%" width="100%" transform="translate(400)" xlink:href="#a"/><path id="b" fill="none" d="M208.6 236.14c9.86-64.92 10.752-150.094 118.005-165.35v0c-119.4.018-124.933 57.032-138.015 122.9" stroke="red" stroke-width="4" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="4" stroke-dasharray="none"/><use height="100%" width="100%" transform="rotate(180 198.595 214.916)" xlink:href="#b"/><path d="M688.6 236.14c1.295-64.667 1.998-154.013 38.005-165.35v0c-218.998-.748-213.75 56.528-218.015 122.9" fill="none" id="c" stroke="red" stroke-width="4" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="4" stroke-dasharray="none"/><use height="100%" width="100%" transform="rotate(180 598.595 214.916)" xlink:href="#c"/><text x="185.805" y="91.886" font-size="12" style="line-height:0%" transform="translate(-300.93 -123.17) scale(1.7037)" font-family="serif" stroke-linecap="square" stroke-miterlimit="10" stroke-width="1.292"><tspan style="-inkscape-font-specification:sans-serif" font-weight="400" font-family="sans-serif">(a)</tspan></text><text style="line-height:0%" font-size="12" y="91.886" x="185.805" transform="translate(99.07 -123.17) scale(1.7037)" stroke-width="1.292" stroke-miterlimit="10" stroke-linecap="square" font-family="serif"><tspan style="-inkscape-font-specification:sans-serif" font-weight="400" font-family="sans-serif">(b)</tspan></text></svg>
    > Hysteresis loops for soft and hard ferromagnetic materials.

    *   **Retentivity**: The amount of magnetism remaining ($B$) when the external field $H$ is reduced to zero (Residual Magnetism).
    *   **Coercivity**: The reverse magnetizing force ($H$) required to reduce the residual magnetism ($B$) to zero.
    *   **Hysteresis Loss**: The energy lost as heat due to the reversal of magnetization, proportional to the area of the hysteresis loop.

### 1.4 Electromagnetic Induction Rules
*   **Faraday's Laws**:
    1.  Whenever flux linking a coil changes, an EMF is induced.
    2.  Magnitude of induced EMF is proportional to the rate of change of flux. $e = -N \frac{d\phi}{dt}$.
*   **Lenz's Law**: The direction of induced EMF is such that it opposes the cause producing it (hence the negative sign).
*   **Fleming's Right Hand Rule** (Generator Rule): Used to find direction of **induced EMF/Current**. Thumb = Motion, Forefinger = Field, Middle Finger = Induced Current.
*   **Fleming's Left Hand Rule** (Motor Rule): Used to find direction of **Force/Motion**. Thumb = Force, Forefinger = Field, Middle Finger = Current.

***

## 2. Transformer (Single Phase)

### 2.1 Principle and Construction
A static device transferring electrical energy between two circuits via mutual induction without changing frequency.
*   **Core Type**: Windings surround the core. Easier insulation.
*   **Shell Type**: Core surrounds the windings. Stronger mechanical support.

![Attachments/transformer_winding.jpg|Transformer Winding Formats](/img/user/Semester%201/Electrical/Unit%204/Attachments/transformer_winding.jpg)
> (a) Core Type Transformer (b) Shell Type Transformer Windings

### 2.2 EMF Equation and Ratios
**Induced EMF Equation**:
$$ E = 4.44 f \phi_m N $$
*   **Derivation Logic**:
    *   Average EMF per turn = $4 f \phi_m$ (Flux changes from 0 to $\phi_m$ in time $T/4$. Rate = $\phi_m / (1/4f) = 4f\phi_m$).
    *   RMS value = Form Factor $\times$ Average Value.
    *   For a sinusoidal flux, Form Factor ($K_f$) = $1.11$.
    *   $E_{rms} = 1.11 \times 4 f \phi_m N \approx 4.44 f \phi_m N$.

Where $f$ is frequency, $\phi_m$ is max flux, $N$ is turns.
**Transformation Ratio ($K$)**:
$$ K = \frac{E_2}{E_1} = \frac{N_2}{N_1} = \frac{I_1}{I_2} $$
*   $K > 1$: Step-up.
*   $K < 1$: Step-down.

### 2.3 Losses and Efficiency
1.  **Core (Iron) Losses**:
    *   **Hysteresis Loss**: Reduced by using soft silicon steel.
    *   **Eddy Current Loss**: Reduced by using **laminated** cores.
    *   Constant irrespective of load. Found via **Open Circuit (OC) Test**.
2.  **Copper Losses**: $I^2 R$ losses in windings. Varies with load square. Found via **Short Circuit (SC) Test**.

**Efficiency ($\eta$)**:
$$ \eta = \frac{\text{Output Power}}{\text{Input Power}} = \frac{x VI \cos\phi}{x VI \cos\phi + P_i + x^2 P_{cu(FL)}} $$
**Condition for Max Efficiency**: when **Iron Loss = Copper Loss** ($P_i = P_{cu}$).

***

## 3. DC Machines

### 3.1 Construction
Same for Generator and Motor:
*   **Stator (Field System)**: Yoke, Poles, Field Winding. Produces magnetic field.
*   **Rotor (Armature)**: Armature Core (laminated), Armature Winding (Lap/Wave), Commutator.
    *   **Lap Winding**: Parallel paths $A = P$. For high current.
    *   **Wave Winding**: Parallel paths $A = 2$. For high voltage.
*   **Commutator**: Converts AC induced in armature to DC (Generator) or limits constant torque direction (Motor).

![Attachments/dc_motor.png|DC Machine Construction](/img/user/Semester%201/Electrical/Unit%204/Attachments/dc_motor.png)
> Cross-section of a DC Machine

### 3.2 DC Generator
*   **Principle**: Dynamically induced EMF.
*   **EMF Equation**:
    $$ E_g = \frac{\phi Z N P}{60 A} $$
    Where $P$ = poles, $Z$ = total conductors, $N$ = speed (rpm), $A$ = parallel paths.

### 3.3 DC Motor
*   **Principle**: Lorentz force on a current-carrying conductor in a magnetic field.
*   **Back EMF ($E_b$)**: The act of rotation induces an EMF opposing the supply voltage.
    $$ V = E_b + I_a R_a $$
*   **Torque Equation**:
    $$ T = \frac{\phi Z I_a P}{2\pi A} \approx 0.159 \phi Z I_a \frac{P}{A} $$
*   **Significance**: Torque is proportional to Flux ($\phi$) and Armature Current ($I_a$).

***

## 4. Three Phase Induction Motor

### 4.1 Principle and Construction
*   **Stator**: Carries 3-phase winding. When supplied with 3-phase AC, produces a **Rotating Magnetic Field (RMF)** of constant magnitude ($1.5 \phi_m$) rotating at **Synchronous Speed ($N_s$)**.
    $$ N_s = \frac{120 f}{P} $$
*   **Rotor**:
    *   **Squirrel Cage**: Bars shorted by end rings. Rugged, low starting torque.
    *   **Slip Ring (Wound)**: Winding connected to slip rings. Allows external resistance for high starting torque.

### 4.2 Operation and Slip
Rotor rotates in the direction of RMF to catch up, but never acts synchronous speed (otherwise induction stops).
*   **Slip ($s$)**:
    $$ s = \frac{N_s - N}{N_s} $$
*   **Rotor Frequency**: $f_r = s \times f$ (at stand still $s=1$, $f_r = f$).

***

## 5. Special Electrical Machines

### 5.1 Brushless DC Motor (BLDC)
*   **Construction**:
    *   **Stator**: 3-phase winding (star connected).
    *   **Rotor**: Permanent Magnets (e.g., NdFeB).
    *   **Sensors**: Hall Effect sensors to detect rotor position.
    *   **Controller**: ESC (Electronic Speed Controller) performs electronic commutation.
*   **Advantages over Combined DC**: Higher efficiency (no brush friction), no sparking, longer life, quieter, higher power density.
*   **Applications**: Drones, EVs, Computer fans, Medical devices.

### 5.2 Stepper Motor
*   **Introduction**: Digital electromechanical device rotating in discrete steps.
*   **Types**:
    1.  **Variable Reluctance**: No permanent magnets, simple, audible noise.
    2.  **Permanent Magnet**: PM on rotor, higher torque.
    3.  **Hybrid**: Best of both.
*   **Operation**: Stator coils are energized in a sequence (A, B, C, D) attracting rotor poles to align. Step angle depends on pole configuration.
*   **Micro-stepping**: Energizing two phases partially to achieve smaller intermediate steps.
*   **Applications**: Printers, Disk drives, Robotics, Position control.
