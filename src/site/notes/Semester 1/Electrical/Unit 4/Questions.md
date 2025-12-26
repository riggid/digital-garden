---
{"dg-publish":true,"permalink":"/semester-1/electrical/unit-4/questions/"}
---

# [[Semester 1/Electrical/Electrical\|Back]]
***
[[Semester 1/Electrical/Unit 4/Core Notes\|Core Notes]] | [[Semester 1/Electrical/Unit 4/Questions\|Questions]] | [[Semester 1/Electrical/Unit 4/pyqs\|PYQs]] | [[Semester 1/Electrical/Unit 4/mcqs\|MCQs]]
***

# Unit 4 Q&A: Electromagnetism & Machines

Questions derived from the Assessment Question Bank.

## 1. Electromagnetism & Magnetic Circuits

### Lecture 59: Definitions
**1. Define i) MMF ii) Magnetic Field Intensity iii) Magnetic Flux iv) Flux Density v) Reluctance.**
*   **MMF (Magnetomotive Force):** The varying magnetic field strength produced by the current flowing through a coil. $MMF = N \times I$. Unit: Ampere-Turns (AT).
*   **Magnetic Field Intensity (H):** The force experienced by a unit north pole. $H = MMF / Length = NI/l$. Unit: AT/m.
*   **Magnetic Flux ($\phi$):** The total number of magnetic field lines passing through a surface. Unit: Weber (Wb).
*   **Magnetic Flux Density (B):** Flux per unit area. $B = \phi / A$. Unit: Tesla (T) or Wb/m².
*   **Magnetic Reluctance (S):** Opposition to the magnetic flux. $S = l / (\mu A) = MMF / \phi$. Unit: AT/Wb.

#### Additional Assignment Problems
**1. Define MMF, Magnetic Field Intensity, Flux, Flux Density, Reluctance.**
*   (Definitions provided above cover all these terms).

### Lecture 60: Laws & Analogy

### Lecture 60: Laws & Analogy
**1. Compare analogy between electrical and magnetic circuits.**
*   **EMF** vs **MMF**: Driving force.
*   **Current (I)** vs **Flux ($\phi$)**: Flow quantity.
*   **Resistance (R)** vs **Reluctance (S)**: Opposition.
*   **Conductivity ($\sigma$)** vs **Permeability ($\mu$)**: Material property.
*   **Ohm’s Law ($V=IR$)** vs **Rowland’s Law ($MMF = \phi S$)**.
*   *Difference:* Current involves physical flow of electrons; Flux is a state of the medium (no flow). Resistance dissipates energy; Reluctance stores energy.

**2. Write short notes on: i) Faraday’s Laws ii) Lenz’s Law.**
*   **Faraday's First Law:** Whenever magnetic flux linked with a coil changes, an EMF is induced.
*   **Faraday's Second Law:** The magnitude of induced EMF is proportional to the rate of change of flux linkage. $e = -N (d\phi/dt)$.
*   **Lenz's Law:** The direction of induced EMF is such that it opposes the cause producing it (the change in flux). Hence the negative sign.

**3. Define i) Dynamically induced EMF ii) Statically induced EMF.**
*   **Dynamically Induced:** EMF induced due to relative motion between conductor and magnetic field (e.g., Generator). $e = Blv \sin\theta$.
*   **Statically Induced:** EMF induced due to change in flux without relative motion (e.g., Transformer). Can be Self or Mutually induced.

#### Assignments
**1. A circular iron ring of mean diameter 25 cm and cross-sectional area 9 cm$^2$ is wound with a coil of 100 turns and carries a current of 1.5 A. The relative permeability of iron is 2000. Calculate the amount of flux produced in the ring.**
*   **Solution:**
    *   $l = \pi d = \pi \times 0.25 = 0.785$ m.
    *   Area $A = 9 \times 10^{-4}$ m$^2$. $\mu_r = 2000$.
    *   Reluctance $S = l / (\mu_0 \mu_r A) = 0.785 / (4\pi \times 10^{-7} \times 2000 \times 9 \times 10^{-4})$.
    *   $S = 347222$ AT/Wb.
    *   $MMF = NI = 100 \times 1.5 = 150$ AT.
    *   Flux $\phi = MMF / S = 150 / 347222 = 0.000432$ Wb = **0.432 mWb**.

---

## 2. Transformers

### Lecture 61-62: Construction & Theory
**1. Write short notes on Construction and Principle of Transformer.**
*   **Principle:** Mutual Induction. An AC current in the primary creates an alternating flux in the core, which links the secondary winding, inducing an EMF.
*   **Construction:** Laminated Steel Core (to reduce eddy currents) and Copper Windings (Primary/Secondary). Types: Core-Type (Windings surround core) and Shell-Type (Core surrounds windings).

#### Additional Assignment Problems
**1. Derive the EMF equation of a single-phase transformer.**
*   **Derivation:**
    *   Flux $\phi = \phi_m \sin \omega t$.
    *   Induced EMF $e = -N \frac{d\phi}{dt} = -N \frac{d}{dt}(\phi_m \sin \omega t) = -N \omega \phi_m \cos \omega t$.
    *   $e = N \omega \phi_m \sin(\omega t - 90^\circ)$. Max value $E_{max} = N \omega \phi_m = N (2\pi f) \phi_m$.
    *   RMS Value $E = E_{max} / \sqrt{2} = \frac{2\pi}{\sqrt{2}} f N \phi_m = 4.44 f N \phi_m$.
    *   $E_1 = 4.44 f N_1 \phi_m$ and $E_2 = 4.44 f N_2 \phi_m$.

**2. 125 kVA Transformer, Primary 2000V, 60Hz. N1=182, N2=40. Calculate i) E2 ii) Currents iii) Max Flux.**
**Solution:**
*   $V_1 = 2000$ V. $N_1=182, N_2=40$. $S = 125000$ VA.
*   (i) **Transformation Ratio** $K = N_2/N_1 = 40/182 \approx 0.22$.
    *   $E_2 = V_1 \times K = 2000 \times (40/182) \approx 439.6$ V.
*   (ii) **Full Load Currents**:
    *   $I_1 = S / V_1 = 125000 / 2000 = 62.5$ A.
    *   $I_2 = S / V_2 = 125000 / 439.6 \approx 284.4$ A.
*   (iii) **Max Flux ($\phi_m$)**:
    *   $E_1 = 4.44 f N_1 \phi_m$.
    *   $2000 = 4.44 \times 60 \times 182 \times \phi_m$.
    *   $\phi_m = 2000 / (48484.8) \approx 0.0412$ Wb $= 41.2$ mWb.

**3. 20 kVA, N1=1000, N2=2500. Core Area $100 cm^2$. Primary 500V, 50Hz. Find Bm, E2, Currents.**
**Solution:**
*   $N_1=1000, N_2=2500$. $V_1=500$. $A = 0.01 m^2$.
*   (ii) **Secondary Voltage**: $E_2 = V_1 (N_2/N_1) = 500 (2500/1000) = 1250$ V.
*   (i) **Max Flux Density ($B_m$)**:
    *   $E_1 = 4.44 f N_1 \phi_m = 4.44 f N_1 (B_m A)$.
    *   $500 = 4.44 \times 50 \times 1000 \times B_m \times 0.01$.
    *   $500 = 2220 \times B_m$.
    *   $B_m = 500 / 2220 \approx 0.225$ T.
*   (iii) **Full Load Currents**:
    *   $I_1 = 20000 / 500 = 40$ A.
    *   $I_2 = 20000 / 1250 = 16$ A.

#### Assignments
**1. A 5 kVA, 50 Hz single phase transformer has primary and secondary turns of 120 and 80 respectively. At a certain flux density, the induced EMF per turn in the primary is 2.5 V. Determine i) Primary/Secondary voltages ii) Currents on FL.**
*   **Solution:**
    *   $E/turn = 2.5$ V.
    *   $E_1 = N_1 \times 2.5 = 120 \times 2.5 = 300$ V.
    *   $E_2 = N_2 \times 2.5 = 80 \times 2.5 = 200$ V.
    *   $I_1 = 5000 / 300 = 16.67$ A.
    *   $I_2 = 5000 / 200 = 25$ A.

**2. 1000/400 turns, 1250V primary. Area 60 cm$^2$. Find E2 and Bm.**
*   **Solution:**
    *   $E_2 = 1250 \times (400/1000) = 500$ V.
    *   $E_1 = 4.44 f N_1 B_m A \implies 1250 = 4.44 \times 50 \times 1000 \times B_m \times 0.006$.
    *   $1250 = 1332 B_m \implies B_m = 0.938$ T.

### Lecture 63-64: Efficiency
**1. Derive condition for maximum efficiency.**
*   Efficiency $\eta = \frac{VI \cos\phi}{VI \cos\phi + P_i + I^2 R}$.
*   Differentiating wrt $I$ and equating to zero: Condition is **Variable Losses ($I^2 R$) = Constant Losses ($P_i$)**. i.e., Copper Loss = Iron Loss.

#### Additional Assignment Problems
**1. How are OC and SC tests conducted?**
*   **Open Circuit (OC) Test:** Finds Iron Loss ($P_i$).
    *   HV winding is kept open. Rated Voltage is applied to LV winding.
    *   Wattmeter reads Iron Loss (since Cu loss is negligible at no load).
*   **Short Circuit (SC) Test:** Finds Full Load Copper Loss ($P_{cu}$).
    *   LV winding is shorted. Low Voltage (variable) is applied to HV winding to circulate rated current.
    *   Wattmeter reads Full Load Copper Loss.

**2. 5 kVA, 1000/200V. Tests: OC (LV): 90W. SC (HV): 110W. Find Efficiency at FL 0.8 lag.**
**Solution:**
*   Iron Loss $P_i$ (from OC test) = 90 W.
*   FL Copper Loss $P_{cu}$ (from SC test) = 110 W.
*   Full Load Output $P_{out} = S \cos \phi = 5000 \times 0.8 = 4000$ W.
*   Total Losses $P_{loss} = P_i + P_{cu(FL)} = 90 + 110 = 200$ W.
*   $\eta = P_{out} / (P_{out} + P_{loss}) = 4000 / 4200 = 0.952$ or **95.2%**.

#### Assignments
**1. 25 kVA, 2000/200 V transformer. Iron loss 350W, FL Cu loss 400W. Efficiency at i) FL 0.8 lag ii) Half Load 0.8 lag.**
*   **Solution:**
    *   (i) FL: $x=1$. $P_{out} = 25000 \times 0.8 = 20$ kW.
    *   Losses = $350 + 400 = 750$ W.
    *   $\eta = 20000 / (20000 + 750) = 0.9638$ or **96.38%**.
    *   (ii) Half Load: $x=0.5$. $P_{out} = 12500 \times 0.8 = 10$ kW.
    *   Cu Loss = $0.5^2 \times 400 = 100$ W. Total Loss = $350 + 100 = 450$ W.
    *   $\eta = 10000 / (10000 + 450) = 0.9569$ or **95.69%**.

---

## 3. DC Generators

### Lecture 65: Construction & Windings
#### Assignments
**1. A 6-pole armature is wound with 498 conductors. Avg EMF/cond = 2V. Current/cond = 120A. Find Total Current, EMF and Power for a) Wave b) Lap.**
*   **Solution:**
    *   (a) **Wave:** $A=2$.
        *   Total Current $I_a = I_{cond} \times A = 120 \times 2 = 240$ A.
        *   Total EMF $E_g = E_{cond} \times (Z/A) = 2 \times (498/2) = 498$ V.
        *   Power $P = 498 \times 240 = 119.52$ kW.
    *   (b) **Lap:** $A=P=6$.
        *   Total Current $I_a = 120 \times 6 = 720$ A.
        *   Total EMF $E_g = 2 \times (498/6) = 166$ V.
        *   Power $P = 166 \times 720 = 119.52$ kW.

#### Additional Assignment Problems
**1. Write a short note on construction details of a DC Machine.**
*   **Stator (Field System):** Yoke (Frame), Pole Cores/Shoes (Support Coils, Spread Flux), Field Windings (Produce Flux).
*   **Rotor (Armature):** Armature Core (Laminated slots), Armature Winding (Lap/Wave), Commutator (AC to DC conversion), Brushes (Collect current).

### Lecture 66: Principle of Operation
**1. Principle of DC Generator/Motor.**
*   **Generator:** Dynamically Induced EMF. Conductor cuts magnetic lines of force $\implies$ EMF induced (Fleming's Right Hand Rule).
*   **Motor:** Lorentz Force. Current carrying conductor in magnetic field $\implies$ Force experienced (Fleming's Left Hand Rule).

### Lecture 67: EMF Equation
**1. Derive EMF expression for DC Generator.**
*   $E_g = \frac{\phi Z N P}{60 A}$ Volts.
    *   $\phi$: Flux/pole. $Z$: Total conductors. $N$: Speed (rpm). $P$: Poles. $A$: Parallel paths.
*   Derivation: Flux cut per rev = $\phi P$. Time per rev = $60/N$. EMF/cond = $d\phi/dt = \phi P / (60/N) = \phi P N / 60$. Total EMF = (EMF/cond) $\times$ (Conds in series per path) = $(\phi P N / 60) \times (Z/A)$.

**2. Draw Equivalent Circuit of DC Generator and governing equations.**
*   **Circuit:** Armature represented as $E_g$ in series with $R_a$. Connected to Load ($V_t$). Field winding separate (for separately excited) or shunt/series.
*   **Equation:** $E_g = V_t + I_a R_a + V_{brush}$.

#### Assignments
**1. 8 pole lap connected armature, 40 slots, 12 conds/slot. Voltage 200V. Speed 1250 rpm. Find Flux per pole.**
*   **Solution:**
    *   $Z = 40 \times 12 = 480$. $P=8, A=8$ (Lap).
    *   $E_g = \frac{\phi Z N P}{60 A} \implies 200 = \frac{\phi \times 480 \times 1250 \times 8}{60 \times 8}$.
    *   $200 = \phi \times 10000 \implies \phi = 0.02$ Wb $= 20$ mWb.

### Lecture 69: Generator Problems
**1. 6 pole Lap, 51 slots, 18 conds/slot. Flux 35 mWb. Speed 750 rpm. Find EMF.**
**Solution:**
*   $P=6$. Lap $\implies A=P=6$.
*   $Z = 51 \times 18 = 918$. $\phi = 0.035$ Wb. $N=750$.
*   $E_g = \frac{0.035 \times 918 \times 750 \times 6}{60 \times 6} = \frac{24097.5}{60} \approx 401.6$ V.

**2. 4 pole Lap, 40 slots. 1500 rpm. Flux 30 mWb. EMF 180V. Find conductors per slot.**
**Solution:**
*   $P=4, A=4$. $N=1500, \phi=0.03$. $E_g=180$.
*   $180 = \frac{0.03 \times Z \times 1500 \times 4}{60 \times 4} = \frac{45 Z}{60} = 0.75 Z$.
*   $Z = 180 / 0.75 = 240$.
*   Conductors per slot = $240 / 40 = 6$.

**3. 4 pole, 12 kW, 240V Gen (Wave). Reconnected to Lap. Calculate new rating.**
**Solution:**
*   **Wave (A=2):** $V=240$ V. $I_L = P/V = 12000/240 = 50$ A.
    *   Current per path $I_{path} = I_L / A = 50 / 2 = 25$ A.
    *   Inducted Voltage $E \propto 1/A$.
*   **Lap (A=4):** New paths = 4.
    *   New Voltage $V' = V \times (A_{old}/A_{new}) = 240 \times (2/4) = 120$ V.
    *   New Current $I' = I_{path} \times A_{new} = 25 \times 4 = 100$ A.
    *   New Power $P' = 120 \times 100 = 12$ kW. (Power remains constant).

#### Assignments
**1. 8 pole DC Generator, 650 conductors. Flux 20 mWb. Wave wound. Speed 1200 rpm. Find EMF. Also find speed for same EMF if Lap wound.**
*   **Solution:**
    *   (i) **Wave (A=2):**
        *   $E_g = \frac{0.02 \times 650 \times 1200 \times 8}{60 \times 2} = 1040$ V.
    *   (ii) **Lap (A=8):** $E_g = 1040$ V.
        *   $1040 = \frac{0.02 \times 650 \times N \times 8}{60 \times 8} = \frac{13 N}{60} = 0.2166 N$.
        *   $N = 4800$ rpm.

---

## 4. DC Motors

### Lecture 68: Principle & Torque
**1. Derive Torque Equation.**
*   $T = 0.159 \phi Z I_a (P/A)$ Nm.
*   Derivation: Electrical Power $E_b I_a$ = Mechanical Power $T \omega$.
*   $(\phi Z N P / 60 A) \times I_a = T \times (2\pi N / 60)$.
*   $\phi Z P I_a / A = T \times 2\pi$.
*   $T = \frac{1}{2\pi} \phi Z I_a \frac{P}{A}$.

**2. Draw Equivalent Circuit of DC Motor and governing equations.**
*   **Circuit:** Supply $V_t$ driving current $I_a$ into Armature ($E_b + R_a$).
*   **Equation:** $V_t = E_b + I_a R_a$.

### Lecture 69: Motor Problems
**1. 200V, 4 pole Lap, 800 conds. Ra=0.5. Current 20A. Flux 30 mWb. Speed and Gross Torque.**
**Solution:**
*   $V=200, I_a=20, R_a=0.5$.
*   Back EMF $E_b = V - I_a R_a = 200 - (20 \times 0.5) = 190$ V.
*   Speed: $E_b = \frac{\phi Z N P}{60 A}$. Lap $\implies P=A$.
    *   $190 = \frac{0.03 \times 800 \times N}{60}$.
    *   $190 = 0.4 N \implies N = 190 / 0.4 = 475$ rpm.
*   Torque: $P_{mech} = E_b I_a = 190 \times 20 = 3800$ W.
    *   $\omega = 2\pi(475)/60 \approx 49.74$ rad/s.
    *   $T = 3800 / 49.74 \approx 76.4$ Nm.

#### Assignments
**1. 4 pole DC motor, 500V. Current 80A. Ra=0.4. Wave wound 522 conductors. Flux 25 mWb. Find Eb, Speed, Torque.**
*   **Solution:**
    *   $E_b = V - I_a R_a = 500 - (80 \times 0.4) = 500 - 32 = 468$ V.
    *   Wave $A=2$. $E_b = \frac{\phi Z N P}{60 A} \implies 468 = \frac{0.025 \times 522 \times N \times 4}{60 \times 2}$.
    *   $468 = 0.435 N \implies N = 1075.8$ rpm.
    *   $T = 0.159 \phi Z I_a (P/A) = 0.159 \times 0.025 \times 522 \times 80 \times (4/2) = 331.99 \approx 332$ Nm.

---

## 5. Induction & Special Machines

### Lecture 70-71: 3-Phase IM
**1. Principle of operation of 3-Phase IM.**
*   **Principle:** When 3-phase supply is given to stator, a Rotating Magnetic Field (RMF) is produced ($N_s$). This field cuts the rotor conductors, inducing EMF and current (Faraday's Law). The current-carrying rotor conductors in the magnetic field experience a torque (Lorentz Force) and start rotating in the direction of the field (Lenz's Law).

#### Additional Assignment Problems
**1. Construction of 3-Phase Induction Motor.**
*   **Stator:** Steel frame, Laminated core with slots, 3-phase distributed winding.
*   **Rotor:**
    *   **Squirrel Cage:** Copper/Aluminum bars shorted by end rings. Robust, constant speed.
    *   **Slip Ring (Wound):** Winding similar to stator connected to slip rings. External resistance can be added for starting torque.

**2. Advantages of 3-Phase IM.**
*   Self-starting, Robust construction (Cage), High efficiency, Low maintenance, Simple.

**2. 8 pole Alternator (750 rpm) supplies 4 pole IM. Rotor current freq 1.5 Hz. Find Motor Speed & Slip.**
**Solution:**
*   Alternator Frequency $f = P N / 120 = (8 \times 750) / 120 = 50$ Hz.
*   Motor Supply Freq $f_{mot} = 50$ Hz.
*   Motor Sync Speed $N_s = 120 f / P = 120 \times 50 / 4 = 1500$ rpm.
*   Slip $s = f_{rotor} / f = 1.5 / 50 = 0.03$.
*   Motor Speed $N = N_s (1 - s) = 1500 (1 - 0.03) = 1500 \times 0.97 = 1455$ rpm.

### Lecture 72-74: Special Motors
**1. Construction/Operation of BLDC Motor.**
*   **Construction:** Permanent Magnet Rotor, Stator with windings (Trapezoidal Back EMF). Rotor position sensors (Hall effect) trigger electronic commutation.
*   **Operation:** Electronic controller switches stator phases based on rotor position to maintain torque angle close to 90°.

**2. Construction/Operation of Stepper Motor.**
*   **Construction:** Toothed stator with concentrated windings, toothed rotor (Variable Reluctance or Hybrid).
*   **Operation:** Moves in discrete steps. Stator phases are energized in sequence, aligning rotor teeth with energized stator teeth for minimum reluctance path.


***
***