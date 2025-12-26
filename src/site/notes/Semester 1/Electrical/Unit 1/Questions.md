---
{"dg-publish":true,"permalink":"/semester-1/electrical/unit-1/questions/"}
---

# [[Semester 1/Electrical/Electrical\|Back]]
***
[[Semester 1/Electrical/Unit 1/Core Notes\|Core Notes]] | [[Semester 1/Electrical/Unit 1/Questions\|Questions]] | [[Semester 1/Electrical/Unit 1/pyqs\|PYQs]] | [[Semester 1/Electrical/Unit 1/mcqs\|MCQs]]
***

# Unit 1 Q&A: DC Circuits

Questions derived from the Assessment Question Bank.

## 1. Fundamental Concepts & Basic Laws

### Lecture 1: Definitions & Basic calculations
**1. Define (i) Electric Current, Potential Difference & Electric Power (ii) KCL & KVL (iii) Active & Passive Elements & Sign conventions**
*   **(i) Basic Quantities**
    *   **Electric Current ($I$):** The rate of flow of electric charge across a cross-section of a conductor. $I = dq/dt$. Unit: Ampere (A).
    *   **Potential Difference ($V$):** The work done in moving a unit positive charge from one point to another. $V = dw/dq$. Unit: Volt (V).
    *   **Electric Power ($P$):** The rate at which electrical energy is absorbed or supplied. $P = VI$. Unit: Watt (W).
*   **(ii) Kirchhoff's Laws**
    *   **KCL:** The algebraic sum of currents entering a node is zero ($\sum I = 0$). Conservation of charge.
    *   **KVL:** The algebraic sum of voltages around a closed path is zero ($\sum V = 0$). Conservation of energy.
*   **(iii) Elements & Conventions**
    *   **Active Elements:** Supply energy (e.g., Voltage/Current sources). Current leaves the positive terminal.
    *   **Passive Elements:** Absorb energy (e.g., Resistors, L, C). Current enters the positive terminal.

**2. Find the voltage $V_{AB}$ in the network shown.**
![Q&A-1.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-1.png)
**(Ans: 26V)**
**Solution:**
1.  **Identify Loops:** Let's assume two loops or apply KVL to the path from A to B.
2.  **KVL Path:** $V_A - V_{drop} + V_{rise} ... = V_B$.
3.  *Detailed steps depend on image.* Based on KVL principles: $V_{AB} = \sum V_{sources} - \sum IR$.
4.  Given Answer: **26V**.

#### Assignments
**1. In the network shown in figure below, calculate:**
*   (i) The unknown currents
*   (ii) The value of the unknown resistance X
*   (iii) The equivalent resistance between the points A and B
**(Ans: $I_1 = 2A, I_2 = 1A, I_3 = 2A$; $X = 15\Omega$; $R_{eq} = 3\Omega$)**

#### Notes/Slides Examples
**1. Find the current through 8$\Omega$ resistor in the network given.**
*   **Solution:**
    *   Apply KVL: $+10 - 8I - 6 - 8 + 12 = 0$
    *   $8 = 8I \implies I = 1A$.

---

### Lecture 2: Series Circuits & Power
**1. A 100W, 120V lamp is connected in series with another lamp of 40W, 120V and the combination is connected across 240V supply mains. Calculate the value of the resistance to be connected across the second lamp, so that each lamp may get the proper current at rated voltage.**
**(Ans: 240 $\Omega$)**
**Solution:**
1.  **Rated Currents:**
    *   Lamp 1 (100W): $I_1 = P_1/V_1 = 100/120 = 0.833 A$.
    *   Lamp 2 (40W): $I_2 = P_2/V_2 = 40/120 = 0.333 A$.
2.  **Circuit Analysis:**
    *   Total voltage is 240V. Since both lamps are rated 120V, they should share the voltage equally (120V each).
    *   The series current must be the higher of the two required currents to power Lamp 1: $I_{total} = I_1 = 0.833 A$.
    *   Lamp 2 only requires $0.333 A$. The excess current must bypass Lamp 2 via a parallel resistor (shunt).
    *   Excess Current $I_{shunt} = I_{total} - I_2 = 0.833 - 0.333 = 0.5 A$.
3.  **Calculate Resistance:**
    *   Voltage across shunt = Voltage across Lamp 2 = 120V.
    *   $R = V / I_{shunt} = 120 / 0.5 = 240 \Omega$.

**2. For the circuit shown, find $V_1$ and $V_2$ and also the power dissipated in each of the resistors. Given $I_1 = 5mA$ and $I_2 = 3mA$.**
![Q&A-2.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-2.png)
**(Ans: V = 9.412V; Powers = 41.78mW, 20.89mW & 10.44 mW)**
**Solution:**
1.  **Apply Nodal Analysis or KCL** at the junction.
    *   Sum of currents entering = Sum of currents leaving.
2.  **Calculate Voltages:** Use Ohm's Law $V = IR$.
    *   *Assuming parallel/series structure based on currents.*
3.  **Calculate Power:** $P = I^2 R$ or $P = V^2 / R$.

#### Assignments
**1. Find the current through 500$\Omega$ resistor in the given network.**
**(Ans: 1.25mA)**

#### Notes/Slides Examples
**1. Find the equivalent resistance between A & B.**
*   **Solution:**
    *   Combine 2$\Omega$ and 4$\Omega$ in series: $R_{s1} = 6\Omega$.
    *   Combine 3$\Omega$ and 6$\Omega$ in parallel: $R_{p1} = 2\Omega$.
    *   Combine with series elements... $R_{eq} = 4\Omega$. (Refer to Notes Class 2).

---

### Lecture 4: Switch Operations
**1. In the circuit shown, current in the network is 50 A & 70 A when the switch is in position 1 and 2 respectively and 25 A with switch open. Find the value of resistors.**
![Q&A-4.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-4.png)
**(Ans: R1 = 1.43$\Omega$, R2 = 0.57$\Omega$, R3 = 2$\Omega$)**
**Solution:**
1.  **Case 1 (Switch Open):**
    *   Current = 25A. Circuit is likely Series combination of some resistors.
    *   $V / R_{eq1} = 25$.
2.  **Case 2 (Position 1):**
    *   Current = 50A. Switch bypasses/adds resistors. $V / R_{eq2} = 50$.
3.  **Case 3 (Position 2):**
    *   Current = 70A. $V / R_{eq3} = 70$.
4.  **Solve System:** Set up simultaneous equations for $R_1, R_2, R_3$ and solve.

#### Assignments
**1. Find the resistance between A & B.**
**(Ans: $R_{AB} = 4\Omega$)**

#### Notes/Slides Examples
**1. Find the equivalent resistance between X & Y for different switch cases:**
*   (i) $R_a = \infty, R_b = \infty$ (Open): All in series. $R_{XY} = 28\Omega$.
*   (ii) $R_a = 0, R_b = \infty$: $R_a$ shorted. $R_{XY} = 18\Omega$.
*   (iii) $R_a = 0, R_b = 0$: Bridge/Series-Parallel reduction. $R_{XY} = 5.143\Omega$.

---

### Lecture 5: Measurements & Switches
**1. A current of 20A flows through two ammeters A and B joined in series. Across A the potential difference is 0.2V and across B it is 0.3V. Find how the same current will divide between A and B when they are joined in parallel.**
**(Ans: $I_A = 12A$, $I_B = 8A$)**
**Solution:**
1.  **Calculate Internal Resistances:**
    *   $R_A = V_A / I = 0.2 / 20 = 0.01 \Omega$.
    *   $R_B = V_B / I = 0.3 / 20 = 0.015 \Omega$.
2.  **Parallel Connection:**
    *   Total Current $I = 20A$.
    *   Using Current Divider Rule:
        *   $I_A = I \times \frac{R_B}{R_A + R_B} = 20 \times \frac{0.015}{0.01 + 0.015} = 20 \times \frac{0.015}{0.025} = 12A$.
        *   $I_B = I \times \frac{R_A}{R_A + R_B} = 20 \times \frac{0.01}{0.025} = 8A$.

**2. Find the value of Voltage $V_{AB}$, if the current through 15 $\Omega$ resistor is 3A when the switch S is (i) Closed and (ii) Open.**
![Q&A-5.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-5.png)
**(Ans: $V_{AB}$ = 77V with S Closed; $V_{AB}$ = 105V with S Open)**
**Solution:**
1.  **Case (i) Closed:**
    *   Analyze mesh with 15$\Omega$. $I_{15} = 3A$.
    *   Calculate drops and find $V_{AB}$.
2.  **Case (ii) Open:**
    *   Re-calculate currents with the open branch.
    *   Find $V_{AB}$.

#### Assignments
**1. Find the current in all the branches in the network shown.**
**(Ans: Refer to solution in assignments)**

#### Notes/Slides Examples
**1. A current of 8 A is shared between two resistors in the network shown. Calculate the current in the 2 $\Omega$ resistor, given that (a) $R_1 = 2 \Omega$; (b) $R_1 = 4 \Omega$.**
*   **Solution:** Use Current Divider Rule.
    *   (a) Equal resistors $\implies$ Equal current $4A$.
    *   (b) Inverse ratio.

**2. Calculate $V_{AB}$ for the network shown.**
*   **Solution:**
    *   Find voltages at nodes relation to reference.
    *   $V_{AB} = V_A - V_B$.

---

### Lecture 8: Equivalent Resistance (I)
**1. Find the equivalent resistance between the terminals A and B in the given network.**
![Q&A-9.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-9.png)
**(Ans: $R_{AB}$ = 9.65$\Omega$)**

**2. Find the equivalent resistance between the terminals A & B in network shown.**
![Q&A-10.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-10.png)
**(Ans: $R_{AB}$ = 6.31$\Omega$)**

#### Assignments
**1. Find current delivered by 4V battery in the network shown using star-delta transformations.**
**(Ans: 0.623A)**

#### Notes/Slides Examples
**1. Find the equivalent resistance between the terminals A & B in the given network.**
*   **Solution:**
    *   Transform Delta (or Star) to reduce the network.
    *   Combine Series/Parallel resistors.
    *   $R_{eq} = 1.4R$. (Refer to Notes Class 8, Example 1).

**2. Find the equivalent resistance between the terminals A & B.**
*   **Solution:**
    *   Result: $R_{AB} = 24.83\Omega$. (Refer to Notes Class 8, Example 2).

---

### Lecture 9: Equivalent Resistance (II)
**1. Find the equivalent resistance between the terminals A and B.**
![Q&A-11.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-11.png)
**(Ans: $R_{AB}$ = 24.83$\Omega$)**

**2. Find the equivalent resistance between the terminals A & B.**
![Q&A-12.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-12.png)
**(Ans: $R_{AB}$ = 29.765$\Omega$)**

#### Assignments
**1. Find the equivalent resistance between the terminals A & B in the given network.**
**(Ans: $R_{AB} = 3.78\Omega$)**

#### Notes/Slides Examples
**1. Using Star and Delta transformation determine the equivalent resistance between the terminals A & B.**
*   **Solution:** Refer to Notes Class 9.

---

## 2. DC Circuit Analysis Techniques

### Lecture 3: Source Transformation (Intro)
**1. Write a short note on source transformation.**
*   **Definition:** A technique to simplify circuits by replacing a voltage source in series with a resistor by an equivalent current source in parallel with the same resistor, and vice-versa.
*   **Condition:** $V_s = I_s \times R$ or $I_s = V_s / R$. The resistance $R$ remains the same.
*   **Utility:** Useful for reducing complex networks to single loops or node pairs.

**2. Find the current $i_{out}$ when $R_{out} = 3 k\Omega$ using source transformation.**
![Q&A-3.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-3.png)
**(Ans: $i_{out}$ = 8.75mA)**

#### Assignments
**1. Plot the following curves:**
*   (i) V-I Characteristic of a Practical Voltage Source
*   (ii) I-V Characteristic of a Practical Current Source

#### Notes/Slides Examples
**1. Numerical Example on Source Transformation: Find the current through 5$\Omega$ resistor.**
*   **Solution:**
    *   Replace 3A source & 2$\Omega$ (parallel) $\to$ 6V source & 2$\Omega$ (series).
    *   Replace 2A source & 1$\Omega$ (parallel) $\to$ 2V source & 1$\Omega$ (series).
    *   Apply KVL: $+6 - 2I - 5I - 1I + 2 = 0$.
    *   $8 - 8I = 0 \implies I = 1A$.

---

### Lecture 6: Source Transformation (Application)
**1. Apply Source Transformation to find the current flowing through branch AB in the given network.**
![Q&A-6.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-6.png)
**(Ans: 1A)**
**Solution:**
1.  Convert Voltage/Current sources step-by-step.
2.  Reduce the circuit to a single loop containing branch AB.
3.  Calculate current $I = V_{eq} / R_{eq}$.

#### Assignments
**1. Two batteries A and B are connected in parallel and a load of 10$\Omega$ is connected across them. Battery A has an emf of 9V and internal resistance of 0.5$\Omega$ and B has an emf of 12V and internal resistance of 1$\Omega$. Determine i) the magnitude and the direction of current flowing through load resistance, ii) current supplied by each battery and iii) potential difference across the load resistance.**
**(Ans: i) 0.967A; ii) A absorbs 1.34A, B delivers 2.33A; iii) 9.67V)**

#### Notes/Slides Examples
**1. Using source transformation find the current $I_L$ when $R_L = 2\Omega$.**
*   **Solution:**
    *   Apply Source Transformation to simplify network.
    *   Apply KVL: $32 - 10I_L - 6 = 0 \implies I_L = 2.6A$. (Refer to Notes Class 6).

---

### Lecture 7: Star-Delta Transformation
**1. Derive how a delta set of resistors is transformed to its equivalent star.**
*   **Concept:** Equate the resistance between any two terminals (e.g., AB) in the Delta network to the resistance between the same leads in the Star network.
*   **Result:** $R_A = \frac{R_{AB} R_{CA}}{R_{AB} + R_{BC} + R_{CA}}$. (Product of adjacent arms / Sum of all arms).

**2. Transform the given delta to equivalent star.**
![Q&A-7.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-7.png)
**(Ans: $R_a = 0.5\Omega, R_b = 0.33\Omega, R_c = 1\Omega$)**

**3. Transform the given star to equivalent delta.**
![Q&A-8.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-8.png)
**(Ans: $R_{ab} = 3.67\Omega, R_{bc} = 11\Omega, R_{ca} = 5.5\Omega$)**

#### Assignments
**1. Prove that equal delta connected resistors when transformed to equivalent star become one-third each.**
**2. Prove that equal star connected resistors when transformed to equivalent delta become thrice each.**

---

### Lecture 10: Mesh Analysis (I)
**1. Find the current supplied by the battery using Mesh Analysis.**
![Q&A-13.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-13.png)
**(Ans: $I_{supply} = 0.66 A$)**
**Solution:**
1.  Define mesh currents $I_1, I_2, I_3$.
2.  Write KVL matrix.
3.  Solve for currents: $I_1 = 0.66 A, I_2 = 0.24 A, I_3 = 0.26 A$.
4.  Current supplied = Current leaving the source = $I_1 = 0.66A$.

#### Assignments
**1. Explain by an example, the difference between Loop & Mesh.**
**2. Find the current through 4$\Omega$ resistor in the network shown using Mesh Analysis.**
**(Ans: $I_1 = 4A, I_2 = 3.5A \implies I_{4\Omega} = 0.5A$)**

#### Notes/Slides Examples
**1. Obtain current through 6$\Omega$ resistor using Mesh Analysis.**
*   **Solution:**
    *   Identify 3 meshes. Write KVL equations.
    *   $I_1 = 5A, I_2 = -8A, I_3 = 2A$.
    *   Current through 6$\Omega$ = $I_3 - I_2 = 10A$.

**2. Find the current through 5$\Omega$ resistor using Mesh Analysis.**
**(Ans: Refer to solution in notes)**

**2. Find the current through 5$\Omega$ resistor using Mesh Analysis.**
![Q&A-14.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-14.png)

---

### Lecture 11: Mesh Analysis (II)
**1. Find the current through the 2$\Omega$ resistor.**
![Q&A-15.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-15.png)
**(Ans: 3A)**

**2. Find the current through 6$\Omega$ resistor using Mesh Analysis.**
![Q&A-16.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-16.png)
**(Ans: 2.999 A)**

#### Assignments
**1. Why can’t we apply KVL in a Mesh containing current sources?**
**2. Find current in 5$\Omega$ resistor using Mesh Analysis.**
**(Ans: 1A)**

#### Notes/Slides Examples
**1. Obtain current through 4$\Omega$ resistor using Mesh Analysis.**
*   **Solution:**
    *   Meshes with current sources -> Current equations.
    *   $I_1 = 9.26A, I_2 = 2.79A, I_3 = -3.97A, I_4 = -8A$.
    *   $I = I_1 - I_2 = 6.47A$.

**2. Obtain voltage across 3$\Omega$ resistor using Mesh Analysis.**
*   **Solution:**
    *   $I_2 = 5.83A, I_3 = 5A$.
    *   $V_{3\Omega} = (I_2 - I_3) \times 3 = 2.49V$.

---

## 3. DC Network Theorems

### Lecture 12: Superposition Theorem (I)
**1. State and explain Superposition Theorem.**
*   **Statement:** In any linear bilateral network containing two or more independent sources, the response (current or voltage) in any element is the algebraic sum of the responses caused by each source acting alone, while all other independent sources are replaced by their internal resistances (Voltage sources shorted, Current sources opened).

**2. Find the current through 1$\Omega$ resistor in the circuit shown.**
![Q&A-17.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-17.png)
**(Ans: 4A)**
**Solution:**
1.  **Source 1 (4V) alone:** Find $I'$. ($I' = 1.33A$).
2.  **Source 2 (3A) alone:** Find $I''$. ($I'' = 2A$).
3.  **Source 3 (1A) alone:** Find $I'''$. ($I''' = 0.67A$).
4.  **Total:** $I = I' + I'' + I''' = 1.33 + 2 + 0.67 = 4A$.

#### Assignments
**1. Using Superposition Theorem, Find current through 8$\Omega$ resistor in the network below.**
**(Ans: 1A)**

#### Notes/Slides Examples
**1. Obtain current through 1$\Omega$ resistor using Superposition Theorem.**
*   **Solution:**
    *   $I' (6V) = 1A$.
    *   $I'' (4A) = 2A$.
    *   $I''' (22V) = -2.44A$.
    *   Total $I = 0.56A$.

---

### Lecture 13: Superposition Theorem (II)
**1. Find the voltage across 7$\Omega$ resistor using Superposition Theorem.**
![Q&A-18.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-18.png)
**(Ans: 21.73V)**

**2. Find the voltage $V_{AB}$ using Superposition Theorem.**
![Q&A-19.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-19.png)
**(Ans: 16V)**

#### Assignments
**1. Using Superposition Theorem, Find current through 4$\Omega$ resistor in the network below.**
**(Ans: 4.28A)**

#### Notes/Slides Examples
**1. Obtain voltage ‘V’ using Superposition Theorem.**
*   **Solution:**
    *   $V' (32V) = 6.4V$.
    *   $V'' (6A) = -192V$.
    *   $V''' (20V) = -4V$.
    *   $V'''' (3A) = 0V$.
    *   Total $V = -189.6V$.

---

### Lecture 14: Thevenin's Theorem (I)
**1. State Thevenin’s Theorem. Draw Thevenin’s Equivalent network.**
*   **Statement:** Any linear, steady-state DC network with two terminals can be replaced by an equivalent circuit consisting of a single voltage source ($V_{th}$) in series with a single resistor ($R_{th}$). $V_{th}$ is the open-circuit voltage across the terminals, and $R_{th}$ is the equivalent resistance seen from the terminals with all independent sources deactivated.

**2. Find the current through the 1 $\Omega$ resistor using Thevenin’s Theorem.**
![Q&A-20.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-20.png)
**(Ans: $V_{th}=12V, R_{th}=2\Omega \implies I=4A$)**
**Solution:**
1.  **Find $V_{th}$:** Remove 1$\Omega$ resistor. Calculate Open Circuit Voltage.
2.  **Find $R_{th}$:** Deactivate sources. Calculate equivalent resistance ($2\Omega$).
3.  **Equivalent Circuit:** 12V source in series with 2$\Omega$ and the load 1$\Omega$.
4.  **Current:** $I = 12 / (2+1) = 4A$.

#### Assignments
**1. Using Thevenin’s Theorem, find the range of voltage across $R_L$ as it varies from 10k$\Omega$ to 20k$\Omega$.**
**(Ans: 15.3V to 20V)**

#### Notes/Slides Examples
**1. Using Thevenin’s Theorem, calculate the range of current flowing through the resistance R, as it varies from 6$\Omega$ and 36$\Omega$.**
*   **Solution:**
    *   $V_{TH} = 20V, R_{TH} = 44\Omega$.
    *   Range: 0.25A to 0.4A.

---

### Lecture 15: Thevenin's Theorem (II)
*(Missing text description in source, but implied by Answer Key)*
**1. Find the Thevenin Equivalent.**
![Q&A-21.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-21.png)
**(Ans: $V_{th}=1V, R_{th}=2.75\Omega$)**

#### Assignments
**1. Using Thevenin’s Theorem, find the magnitude and direction of current in the branch BD.**
**(Ans: 0.207A from B to D)**

---

### Lecture 16: Thevenin's Theorem (III)
*(Missing text description in source, but implied by Answer Key)*
**1. Find the Thevenin Equivalent.**
![Q&A-22.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-22.png)
**(Ans: $V_{th}=4V, R_{th}=6\Omega$)**

#### Assignments
**1. Using Thevenin’s Theorem, find range of current through R.**
**(Ans: 3.16A to 6A)**

---

### Class 17: Thevenin's Practice
**1. Using Thevenin’s Theorem, obtain the current through 10$\Omega$ resistor in the network shown.**
![Q&A-26.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-26.png)
**(Ans: See solution)**
**Solution:**
1.  **Remove Load (10$\Omega$):** Calculate $V_{th}$ across open terminals.
    *   Left loop: $5A \to 4\Omega \implies 20V$.
    *   Right loop: $10A \to 6\Omega \implies 60V$.
    *   $V_{th} = 20 - (-60) = 80V$.
2.  **Calculate $R_{th}$:** Open current sources.
    *   $R_{th} = 4 + 6 = 10\Omega$.
3.  **Calculate Current:**
    *   $I = V_{th} / (R_{th} + R_L) = 80 / (10+10) = 4A$.

**2. Obtain Thevenin’s equivalent across the terminals A & B in the network below:**
![Q&A-27.png](/img/user/Semester%201/Electrical/Unit%201/Q&A-27.png)