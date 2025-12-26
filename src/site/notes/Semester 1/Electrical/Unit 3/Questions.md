---
{"dg-publish":true,"permalink":"/semester-1/electrical/unit-3/questions/"}
---

# [[Semester 1/Electrical/Electrical\|Back]]
***
[[Semester 1/Electrical/Unit 3/Core Notes\|Core Notes]] | [[Semester 1/Electrical/Unit 3/Questions\|Questions]] | [[Semester 1/Electrical/Unit 3/pyqs\|PYQs]] | [[Semester 1/Electrical/Unit 3/mcqs\|MCQs]]
***

# Unit 3 Q&A: Three Phase Systems & Installations

Questions derived from the Assessment Question Bank.

## 1. Three Phase Balanced Systems (Theory)

### Lecture 40: Generation & Representation
**1. Discuss in brief how balanced three phase EMFs are generated. Draw a neat diagram representing balanced three phase EMFs.**
*   **Generation:** Three coils are placed 120° apart in space on a stator. When a magnetic field rotates inside them (or coils rotate inside a field) at constant speed, EMFs are induced in each coil. Since the coils are identical and spaced equally, the EMFs have equal magnitude and frequency but are phase-shifted by 120° ($2\pi/3$ rad) from each other.
*   **Equations:**
    *   $e_R = E_m \sin(\omega t)$
    *   $e_Y = E_m \sin(\omega t - 120^{\circ})$
    *   $e_B = E_m \sin(\omega t - 240^{\circ})$
*   **(Diagram Requirement):** Draw three sine waves displaced by 120°.

#### Additional Assignment Problems
**1. Discuss in brief how balanced three phase EMFs are generated. Draw a neat diagram representing balanced three phase EMFs.**
*   **Answer:**
    *   Three identical coils are placed 120 electrical degrees apart on the stator.
    *   A magnetic field (rotor) rotates at constant speed $\omega$ rad/s.
    *   EMFs induced are $e_R = E_m \sin \omega t$, $e_Y = E_m \sin(\omega t - 120^\circ)$, $e_B = E_m \sin(\omega t - 240^\circ)$.
    *   They have same amplitude and frequency but phase shifted by 120°.

### Lecture 42: Delta Connection
**1. Derive the relation between Line and Phase currents in a balanced delta connected three phase system.**
*   **Relation:** $I_L = \sqrt{3} I_{ph}$.
*   **Derivation:**
    *   In Delta, Line Voltage $V_L = V_{ph}$. Line Current $I_L$ is the phasor difference of two phase currents (e.g., $I_R = I_{RB} - I_{YR}$).
    *   Assuming balanced currents $I_{ph}$ spaced 120° apart.
    *   Using parallelogram law or phasor subtraction: $|I_R| = \sqrt{I_{ph}^2 + I_{ph}^2 + 2I_{ph}^2 \cos(60^{\circ})} = \sqrt{3} I_{ph}$.
    *   Phase current leads/lags line current by 30°.

**2. It is observed that second phase current in a balanced delta system is $10\sin(\omega t-60^{\circ})$ A. Express all three phase currents and line currents in time and phasor form.**
**Solution:**
*   Sequence R-Y-B. Second phase is Y (or Phase 2).
*   $i_{ph2}(t) = 10 \sin(\omega t - 60^{\circ})$. $\bar{I}_{ph2} = (10/\sqrt{2}) \angle -60^{\circ}$.
*   Phase 1 ($R$) leads Phase 2 by 120°: $\bar{I}_{ph1} = (10/\sqrt{2}) \angle (-60+120) = (10/\sqrt{2}) \angle 60^{\circ}$.
*   Phase 3 ($B$) lags Phase 2 by 120°: $\bar{I}_{ph3} = (10/\sqrt{2}) \angle (-60-120) = (10/\sqrt{2}) \angle -180^{\circ}$.
*   **Line Currents:** $I_L$ lags $I_{ph}$ by 30° (Standard lag sequence). Magnitude $I_L = \sqrt{3} I_{ph} = 10\sqrt{3}$.
    *   $i_{L1}$ lags $i_{ph1}$ by 30°: Phase $60 - 30 = 30^{\circ}$. $i_{L1}(t) = 10\sqrt{3} \sin(\omega t + 30^{\circ})$.
    *   $i_{L2}$ lags $i_{ph2}$ by 30°: Phase $-60 - 30 = -90^{\circ}$. $i_{L2}(t) = 10\sqrt{3} \sin(\omega t - 90^{\circ})$.
    *   $i_{L3}$ lags $i_{ph3}$ by 30°: Phase $-180 - 30 = -210^{\circ}$ (or $150^{\circ}$). $i_{L3}(t) = 10\sqrt{3} \sin(\omega t - 210^{\circ})$.

#### Additional Assignment Problems
**1. Derive relation between Line and Phase currents in balanced delta.**
*   **Answer:** $I_L = \sqrt{3} I_{ph}$. Line current is phasor difference of two phase currents ($I_R = I_{RB} - I_{YR}$). Resultant magnitude is $2 I_{ph} \cos(30^\circ) = \sqrt{3} I_{ph}$. $I_L$ lags $I_{ph}$ by 30^0$.

**2. Second phase current is $10\sin(\omega t - 60^\circ)$ A. Express currents.**
*   See Q2 above (Identical Solution).

### Lecture 43: Definitions
**1. Define i) Balanced Star Load ii) Balanced Delta Load.**
*   **Balanced Star Load:** Three identical impedances (same magnitude and phase angle) connected in a 'Y' or Star configuration. A neutral point exists.
*   **Balanced Delta Load:** Three identical impedances connected in a '$\Delta$' or Mesh configuration (end-to-end loop). No neutral point.

**2. In a balanced delta load, phase current is 10A and leads phase voltage 200V by 60°. Find P, Q, S.** (Note: Text says "lags" in QB, but let's assume "lags" as per standard).
**Solution:**
*   $I_{ph} = 10$ A. $V_{ph} = 200$ V. $\phi = 60^{\circ}$ Lag.
*   **P (Active Phase):** $P_{ph} = V_{ph} I_{ph} \cos \phi = 200 \times 10 \times 0.5 = 1000$ W. Total $P = 3 \times 1000 = 3000$ W = 3 kW.
*   **Q (Reactive Phase):** $Q_{ph} = V_{ph} I_{ph} \sin \phi = 2000 \times 0.866 = 1732$ VAR. Total $Q = 3 \times 1732 = 5196$ VAR = 5.2 kVAR.
*   **S (Apparent Phase):** $S_{ph} = V_{ph} I_{ph} = 2000$ VA. Total $S = 6000$ VA = 6 kVA.

#### Additional Assignment Problems
**1. Define Balanced Star and Delta Loads.**
*   **Star:** 3 Identical impedances connected to a common neutral point.
*   **Delta:** 3 Identical impedances connected in series loop (mesh).

**2. Balanced delta, Phase current 10A lags 200V by 60°. Find P, Q, S.**
*   **Solution:** Same as previous example. $P=3$ kW, $Q=5.2$ kVAR, $S=6$ kVA.

---

## 2. Three Phase Calculations (Star/Delta)

### Lecture 41: Star Connection Problems
**1. Balanced star-connected load 100kW takes leading current of 80A from 1100V, 50Hz supply. Find circuit constants.**
**Solution:**
*   $P = 100$ kW. $I_L = 80$ A (Lead). $V_L = 1100$ V.
*   Star: $I_{ph} = I_L = 80$ A. $V_{ph} = 1100 / \sqrt{3} = 635.1$ V.
*   Impedance $Z = V_{ph} / I_{ph} = 635.1 / 80 \approx 7.94 \, \Omega$.
*   $P = 3 I_{ph}^2 R \implies 100000 = 3 (80)^2 R \implies R = 100000 / 19200 = 5.21 \, \Omega$.
*   $X_C = \sqrt{Z^2 - R^2} = \sqrt{7.94^2 - 5.21^2} \approx 5.99 \, \Omega$.
*   $C = 1/(2\pi f X_C) = 1/(100\pi \times 5.99) \approx 531 \, \mu F$.

**2. Balanced star load $(8+j6) \Omega$ per phase, 400V, 50Hz. Calculate $I_L$, pf, P, Q.**
**Solution:**
*   $Z_{ph} = 8+j6 = 10 \angle 36.9^{\circ} \, \Omega$.
*   $V_L = 400$ V $\implies V_{ph} = 400/\sqrt{3} = 230.9$ V.
*   $I_{ph} = V_{ph} / Z_{ph} = 230.9 / 10 = 23.09$ A. Star: $I_L = 23.09$ A.
*   pf $= \cos(36.9^{\circ}) = 0.8$ Lagging.
*   $P = \sqrt{3} V_L I_L \cos \phi = \sqrt{3}(400)(23.09)(0.8) \approx 12.8$ kW.
*   $Q = \sqrt{3} V_L I_L \sin \phi = \sqrt{3}(400)(23.09)(0.6) \approx 9.6$ kVAR.

#### Additional Assignment Problems
**1. Balanced star-connected load 100 kW takes leading current of 80 A, 1100 V, 50 Hz. Find circuit constants.**
*   **Solution:**
    *   $P = 100$ kW. $I_L = 80$ A (Lead). $V_L = 1100$ V.
    *   Star: $I_{ph} = I_L = 80$ A. $V_{ph} = 1100 / \sqrt{3} = 635.1$ V.
    *   $Z_{ph} = V_{ph} / I_{ph} = 7.94 \Omega$.
    *   $P = 3 I_{ph}^2 R \implies 100000 = 3(6400)R \implies R = 5.21 \Omega$.
    *   $X_C = \sqrt{Z^2 - R^2} = \sqrt{7.94^2 - 5.21^2} = 5.99 \Omega$.
    *   $C = 1/(2\pi f X_C) = 1/(314 \times 5.99) = 531 \mu F$.

**2. Balanced star load $(8+j6) \Omega$, 400 V, 50 Hz. Calculate Line current, pf, P, Q.**
*   **Solution:**
    *   $Z = \sqrt{8^2+6^2} = 10 \Omega$. $V_{ph} = 400/\sqrt{3} = 230.9$ V.
    *   $I_{Line} = I_{ph} = 230.9 / 10 = 23.09$ A.
    *   pf $= R/Z = 8/10 = 0.8$ Lagging.
    *   $P = \sqrt{3} V_L I_L \cos \phi = \sqrt{3}(400)(23.09)(0.8) = 12.79$ kW.
    *   $Q = \sqrt{3} V_L I_L \sin \phi = \sqrt{3}(400)(23.09)(0.6) = 9.59$ kVAR.

### Lecture 44: Star Impedance
**1. Balanced 3ph star, 400V. Current 30A, lags 30°. Find Z and P.**
**Solution:**
*   $I_L = 30$ A. $V_L = 400$ V. $\phi = 30^{\circ}$ Lag.
*   Star: $V_{ph} = 230.9$ V. $I_{ph} = 30$ A.
*   (i) Impedance $Z = V_{ph} / I_{ph} = 230.9 / 30 \approx 7.7 \, \Omega$. Coordinate: $7.7 \angle 30^{\circ} = 6.66 + j3.85 \, \Omega$.
*   (ii) Total Power $P = \sqrt{3} V_L I_L \cos 30^{\circ} = \sqrt{3}(400)(30)(0.866) \approx 18$ kW.

**2. 415V, 50Hz, Star impedances: $R=15\Omega, C=177\mu F, L=0.1H$ series. Find pf, I, P, Q, S.**
**Solution:**
*   $X_L = 100\pi(0.1) \approx 31.42 \, \Omega$.
*   $X_C = 1/(100\pi \times 177 \times 10^{-6}) \approx 18.0 \, \Omega$.
*   $Z_{ph} = 15 + j(31.42 - 18.0) = 15 + j13.42 \, \Omega$.
*   $|Z| = \sqrt{15^2 + 13.42^2} \approx 20.13 \, \Omega$.
*   Angle $\phi = \arctan(13.42/15) \approx 41.8^{\circ}$.
*   (a) pf $= \cos(41.8^{\circ}) \approx 0.745$ Lag.
*   (b) $V_{ph} = 415/\sqrt{3} \approx 239.6$ V. $I_{ph} = 239.6 / 20.13 \approx 11.9$ A.
*   (c) Star $\implies I_L = 11.9$ A.
*   (d) $P = 3 I_{ph}^2 R = 3(11.9^2)(15) \approx 6.37$ kW.
*   (e) $Q = P \tan \phi = 6.37 \tan(41.8) \approx 5.7$ kVAR.
*   (f) $S = \sqrt{P^2+Q^2} \approx 8.55$ kVA.

#### Additional Assignment Problems
**1. Balanced Star 400V, Current 30A lags 30°. Find Impedance and Power.**
*   **Solution:**
    *   $V_{ph} = 230.9$ V. $I_{ph} = 30$ A.
    *   $Z = 230.9/30 = 7.7 \Omega$.
    *   $P = \sqrt{3}(400)(30)(0.866) = 18$ kW.

**2. 415V Star. R=15, C=177uF, L=0.1H series. Find pf, I, P, Q, S.**
*   **Solution:** Same as Question 2 above.

### Lecture 45: Delta Problems
**1. Balanced delta $(8-j6) \Omega$ per phase, 230V, 50Hz. Calculate $I_L$, pf, Q.**
**Solution:**
*   $Z_{ph} = 8-j6 = 10 \angle -36.9^{\circ} \, \Omega$.
*   Delta: $V_{ph} = V_L = 230$ V.
*   $I_{ph} = V_{ph} / Z = 230 / 10 = 23$ A.
*   (i) Line Current $I_L = \sqrt{3} I_{ph} = 23\sqrt{3} \approx 39.84$ A.
*   (ii) pf $= \cos(-36.9^{\circ}) = 0.8$ Leading.
*   (iii) $Q = \sqrt{3} V_L I_L \sin \phi = \sqrt{3}(230)(39.84)(0.6)$
    *   Alternatively $3 V_{ph} I_{ph} \sin \phi = 3(230)(23)(0.6) = 9522$ VAR $\approx 9.52$ kVAR.

**2. Delta load $(25+j40) \Omega$. Fed from Star Transformer (Phase Voltage 240V). Find Currents, Voltage, Transformer I.**
**Solution:**
*   Transformer (Source) is Star. Phase Volts $V_{ph(S)} = 240$ V.
*   Source Line Voltage $V_L = \sqrt{3} \times 240 \approx 415.7$ V.
*   Load is Delta. Load Phase Voltage $V_{ph(L)} = V_L = 415.7$ V.
*   (ii) Voltage across load phase: $415.7$ V.
*   Load Impedance $Z = 25+j40 \approx 47.17 \angle 58^{\circ}$.
*   (i) Current in load phase $I_{ph(L)} = 415.7 / 47.17 \approx 8.81$ A.
*   (iv) Power to load $P = 3 I_{ph(L)}^2 R = 3(8.81^2)(25) \approx 5.82$ kW.
*   (iii) Transformer Secondary Current is the Line Current. $I_L = \sqrt{3} I_{ph(L)} = \sqrt{3}(8.81) \approx 15.26$ A.

#### Additional Assignment Problems
**1. Balanced Delta $(8-j6)$, 230V. Find IL, pf, Q.**
*   **Solution:**
    *   $Z = 10 \Omega$. $V_{ph}=230$ V. $I_{ph} = 23$ A.
    *   $I_L = \sqrt{3}(23) = 39.84$ A.
    *   pf $= 0.8$ Lead.
    *   $Q = 3 V_{ph} I_{ph} \sin \phi = 3(230)(23)(0.6) = 9.52$ kVAR.

**2. Delta load $(25+j40)$. Fed from Star Transformer (Phase Voltage 240V).**
*   **Solution:** Identical to Solution 2 above.

---

## 3. Power Measurement (Two Wattmeter Method)

### Lecture 46: Theory
**1. Show that two wattmeters are sufficient to measure active power in a 3-phase system.**
*   **Proof:** Instantaneous power $p = v_R i_R + v_Y i_Y + v_B i_B$. Using $i_R + i_Y + i_B = 0$ (neutral current 0 in balanced/unbalanced 3-wire), substitute $i_B = -(i_R+i_Y)$.

#### Assignments
**1. When three identical coils are connected in delta across a 3 phase, 400 V, 50 Hz supply the line current is 27.72 A and the total power consumed is 15.36kW. Find the resistance and the inductance of the coils.**
*   **Solution:**
    *   Delta: $I_{ph} = I_L / \sqrt{3} = 27.72 / \sqrt{3} = 16$ A.
    *   $P = 3 I_{ph}^2 R \implies 15360 = 3 \times (16)^2 \times R \implies 15360 = 768 R$.
    *   $R = 20 \Omega$.
    *   $V_{ph} = 400$ V. $Z_{ph} = V_{ph} / I_{ph} = 400/16 = 25 \Omega$.
    *   $X_L = \sqrt{Z^2 - R^2} = \sqrt{25^2 - 20^2} = 15 \Omega$.
    *   $L = X_L / 2\pi f = 15 / (100\pi) = 0.0477$ H $= 47.7$ mH.

### Lecture 46: Two Wattmeter Method
*   $p = v_R i_R + v_Y i_Y - v_B (i_R+i_Y) = i_R(v_R-v_B) + i_Y(v_Y-v_B)$.
*   $(v_R-v_B) = v_{RB}$ (Line voltage). This corresponds to Wattmeter 1 (Current coil in R, Potential across RB).
*   Similarly for Wattmeter 2. Sum of readings equals total instantaneous power. Avgs holds true.

### Lecture 47, 49: Wattmeter Readings Problems
**1. Readings of two wattmeters: 8kW and 0.8kW (reversed). Find pf, P, Q.**
**Solution:**
*   $W_1 = 8$ kW. $W_2 = -0.8$ kW (Reversed implies negative).
*   Sum $P = W_1 + W_2 = 8 - 0.8 = 7.2$ kW.
*   Difference $W_1 - W_2 = 8 - (-0.8) = 8.8$ kW.
*   $\tan \phi = \sqrt{3} \frac{W_1 - W_2}{W_1 + W_2} = \sqrt{3} \frac{8.8}{7.2} \approx 1.732 \times 1.22 = 2.11$.
*   $\phi = \arctan(2.11) \approx 64.7^{\circ}$.
*   pf $= \cos(64.7^{\circ}) \approx 0.427$ Lag.
*   $Q = P \tan \phi = 7.2 \times 2.11 = 15.2$ kVAR. (Or $\sqrt{3}(8.8) = 15.24$).

**2. Two wattmeters read 3kW and 1kW. Star load R-C series, 400V, 50Hz. Find R, C.**
**Solution:**
*   $W_1 = 3$ kW, $W_2 = 1$ kW. (Assume positive).
*   $P = 4$ kW. $\tan \phi = \sqrt{3} \frac{2}{4} = \frac{\sqrt{3}}{2} = 0.866$.
*   $\phi = 40.9^{\circ}$. pf $= 0.756$.
*   $P = \sqrt{3} V_L I_L \cos \phi \implies 4000 = \sqrt{3}(400) I_L (0.756)$.
*   $4000 = 523.8 I_L \implies I_L \approx 7.64$ A.
*   Star: $I_{ph} = 7.64$ A. $V_{ph} = 230.9$ V.
*   $Z = 230.9 / 7.64 \approx 30.2 \, \Omega$.
*   $R = Z \cos \phi = 30.2 \times 0.756 \approx 22.8 \, \Omega$.
*   $X_C = Z \sin \phi = 30.2 \times 0.655 \approx 19.8 \, \Omega$.
*   $C = 1/(100\pi \times 19.8) \approx 160 \, \mu F$.

#### Additional Assignment Problems
**1. Wattmeters read 8kW and 0.8kW (reversed). Find pf, P, Q.**
*   **Solution:**
    *   $W_1=8, W_2=-0.8$. Sum $P=7.2$ kW. Diff $D=8.8$ kW.
    *   $\tan \phi = \sqrt{3}(8.8/7.2) = 2.11 \implies \phi = 64.7^\circ$.
    *   pf $= 0.427$. $Q = 15.2$ kVAR.

**2. Wattmeters 3kW and 1kW. Star RC load 400V.**
*   **Solution:** Identical to Solution 2 above.

### Lecture 48: Delta Wattmeter Problem
**1. Balanced delta load $(14-j14) \Omega$, 200V supply. Find Wattmeter readings, currents, powers.**
**Solution:**
*   $Z = 14-j14 = 19.8 \angle -45^{\circ}$.
*   Delta: $V_{ph} = 200$ V. $I_{ph} = 200 / 19.8 = 10.1$ A.
*   $I_L = \sqrt{3}(10.1) = 17.5$ A.
*   pf $= \cos(-45) = 0.707$ Lead.
*   Total $P = \sqrt{3}(200)(17.5)(0.707) \approx 4.28$ kW.
*   Readings $W_1, W_2$:
    *   $W_1 = V_L I_L \cos(30 - \phi)$ (For lead, $\phi$ is negative, so $30+\phi$). Or careful with assignment.
    *   For Lead $\phi=-45$. $W_1 = V_L I_L \cos(30 - (-45)) = VL IL \cos(75)$.
    *   $W_2 = V_L I_L \cos(30 + (-45)) = VL IL \cos(-15)$.
    *   $W_1 = 200 \times 17.5 \times 0.259 \approx 0.9$ kW.
    *   $W_2 = 200 \times 17.5 \times 0.966 \approx 3.38$ kW.
    *   (Sum $3.38+0.9 = 4.28$, correct).

#### Additional Assignment Problems
**1. Delta $(14-j14)$, 200V. Wattmeter readings.**
*   **Solution:** Identical to Solution 2 above. Readings: 3.38 kW & 0.9 kW.

**2. 3 Phase Motor, 400V, 25 HP output, Eff 87%, pf 0.82. Find Line and Phase currents (Delta).**
*   **Solution:**
    *   $P_{out} = 25 \times 746 = 18.65$ kW.
    *   $P_{in} = 18.65 / 0.87 = 21.44$ kW.
    *   $P_{in} = \sqrt{3} V_L I_L \cos \phi \implies 21440 = \sqrt{3}(400) I_L (0.82)$.
    *   $I_L = 21440 / 568.1 = 37.74$ A.
    *   Delta Phase Current $I_{ph} = 37.74 / \sqrt{3} = 21.79$ A.

### Lecture 50: Specialized Wattmeter connections
**1. Wattmeter reading. Load Star $(20+j15) \Omega$, 400V. connection shown (presumed 1-wattmeter reactive?).**
*   **Note:** Without figure, usually implies Reactive Power setup (Current coil in one line, Potential across other two).
*   If so, Reading $W = V_{Line} I_{Line} \sin(\text{angle between})$. Usually $W \propto Q$.
*   Standard reactive connection reads $V_L I_L \sin(\phi+90)$? No.

#### Assignments
**1. Two wattmeters indicate 50kW each. If pf changes to 0.866 lead (same total power), find new readings.**
*   **Solution:**
    *   Original: $W_1=W_2 \implies$ Unity pf. $P = 100$ kW.
    *   New: $P=100$ kW. $\text{pf} = 0.866 \implies \phi = 30^\circ$ Lead.
    *   For Lead, angles switch roles or just compute:
    *   Reading $W_1 = V_L I_L \cos(30+\phi)$. Reading $W_2 = V_L I_L \cos(30-\phi)$.
*   Usually $W_2$ is the higher reading (smaller angle) for lagging pf. $W_2 > W_1$.
    *   $P = \sqrt{3} V_L I_L \cos \phi \implies 100000 = \sqrt{3} V_L I_L (0.866) \implies V_L I_L = 100000 / 1.5 = 66666.67$ VA.
    *   For leading pf, $\phi = -30^\circ$.
    *   $W_1 = V_L I_L \cos(30^\circ - (-30^\circ)) = V_L I_L \cos(60^\circ) = 66666.67 \times 0.5 = 33333.33$ W $\approx 33.33$ kW.
    *   $W_2 = V_L I_L \cos(30^\circ + (-30^\circ)) = V_L I_L \cos(0^\circ) = 66666.67 \times 1 = 66666.67$ W $\approx 66.67$ kW.
    *   Check: $W_1 + W_2 = 33.33 + 66.67 = 100$ kW. (Matches)

**2. Two wattmeters ratio 2:1. Line current 10A, 400V. Find readings.**
*   **Solution:**
    *   Ratio 2:1 implies pf $= 0.866$.
    *   $P = \sqrt{3} V_L I_L \cos \phi = \sqrt{3} \times 400 \times 10 \times 0.866 = 6$ kW.
    *   $W_1 + W_2 = 6$. $W_1 = 2 W_2$.
    *   $W_2 = 2$ kW, $W_1 = 4$ kW.
*   Assuming standard "One Wattmeter on balanced load" finding Reactive Power: Reading = $Q/\sqrt{3}$.
*   Let's solve for $P, Q$ first.
*   $Z = 20+j15 = 25 \angle 36.9^{\circ}$.
*   Star: $V_{ph} = 231$ V. $I_{L} = 231/25 = 9.24$ A. Use $\phi=36.9^{\circ}$.
*   This needs figure to give specific answer.

**2. Two wattmeters on Star load $(9-j5) \Omega$, 200V. W1 (CC in R, PC on RY). W2 (CC in B, PC on BY).**
**Solution:**
*   Supply 200V. Star. $Z = 9-j5 = 10.3 \angle -29^{\circ}$.
*   $I_L = (200/\sqrt{3}) / 10.3 = 11.2$ A. Lead pf $\phi = -29^{\circ}$.
*   W1 (R, RY): Reads $V_{RY} I_R \cos(\text{angle between})$.
    *   $V_{RY}$ leads $V_{RN}$ by 30. $I_R$ leads $V_{RN}$ by 29.
    *   Angle between $V_{RY}$ and $I_R$ is $30 - 29 = 1^{\circ}$.
    *   $W_1 = 200 \times 11.2 \times \cos(1^{\circ}) \approx 2240$ W = 2.24 kW.
*   W2 (B, BY): Reads $V_{BY} I_B \cos(\text{angle between})$.
    *   $V_{BY}$ lags $V_{BN}$ by 30? No, $V_{BY} = V_{BN} - V_{YN}$. Vector $V_{BY}$ lags $V_{BN}$ by 30 deg? (Check phasor). $V_{YB}$ leads $V_{YN}$ by 30. $V_{BY}$ is opposite.
    *   Angle $(V_{BY}, I_B) = 30 - \phi$?
    *   Standard formula: $W_2 = V_L I_L \cos(30-\phi) = 200 \times 11.2 \times \cos(30 - (-29)) = 2240 \times \cos(59) \approx 1153$ W = 1.15 kW.

#### Additional Assignment Problems
**1. Wattmeter reading for Star $(20+j15)$, 400V connected as per figure.**
*   (Figure missing, but likely Reactive Power connection).

**2. Two wattmeters Star $(9-j5)$, 200V. Connections specified.**
*   **Solution:** Identical to Solution 2 above. Readings 2.24 kW & 1.15 kW.

---

## 4. Electrical Installations

### Lecture 51-53: Safety & Components
**1. What is a fuse? Advantages and Disadvantages.**
*   **Fuse:** A protective device containing a wire that melts and breaks the circuit when excessive current flows.
*   **Advantages:** Cheapest protection, simple, fast operation for high short circuits, no maintenance.
*   **Disadvantages:** Must be replaced after operation (one-time use), cannot handle small overloads precisely.

**2. Difference between MCB and MCCB.**
*   **MCB (Miniature Circuit Breaker):** Rated current up to ~100A. Adjustable trip settings usually not available. Used for domestic/light commercial.
*   **MCCB (Molded Case Circuit Breaker):** Rated current up to ~1000A+. Adjustable trip settings. Used for industrial applications.

**3. Write short notes on Plate Earthing and Pipe Earthing.**
*   **Plate Earthing:** A copper or GI plate is buried vertically in a pit (usually >1.5m deep) filled with charcoal and salt. Surface area provides path to ground.
*   **Pipe Earthing:** A perforated GI pipe is driven vertically into the ground. Charcoal and salt are layered around it. Water can be poured for moisture. Most common and cost-effective method.

---

## 5. Domestic Wiring & Tariff

### Lecture 54-55: Consumption Calculations
**1. Define kWhr.**
*   **Definition:** Kilo-Watt Hour (Unit). The energy consumed when a device of 1000 Watts (1 kW) runs for 1 Hour. 1 kWh = 3.6 MJ.

#### Additional Assignment Problems
**1. Define kWhr.** (Same as above).
**2. 1kW Geyser, 30 mins.** (Same as above, Answer 0.5 Units).
**3. 20W LED, 1kWhr usage.** (Same as above, Answer 50 hours).

**2. A 1kW Geyser runs for 30 mins. Energy?**
*   $E = P \times t = 1 \text{ kW} \times 0.5 \text{ h} = 0.5$ kWh (0.5 Units).

**3. LED 20W. How many hours to consume 1 kWh?**
*   $E = P \times t \implies 1000 \text{ Wh} = 20 \text{ W} \times t$.
*   $t = 1000 / 20 = 50$ Hours.

### Lecture 55: Tariff Calculation Example
**1. Determine the monthly bill for the following household consumption (Assume 3kW Sanctioned Load):**
*   **Appliance Wattage & Usage:**
    *   Lights (280W, 5h), Fans (120W, 10h), Geyser (2000W, 0.5h), Mixer (750W, 0.33h), Fridge (100W, 15h), Freezer (300W, 4h), Washing Machine (325W, 1h), Iron (1000W, 0.5h), Motor 1hp (746W, 1h), TV (100W, 10h), Laptop (120W, 2h), Mobile (15W, 2h), Modem (8W, 24h), Microwave (900W, 1h), Vacuum (350W, 1h).
*   **Step 1: Energy Per Day**
    *   Total Wh/day $= 1400 + 1200 + 1000 + 250 + 1500 + 1200 + 325 + 500 + 746 + 1000 + 240 + 30 + 192 + 900 + 350 = 10833$ Wh.
    *   **Total kWh/day = 10.833 Units.**
*   **Step 2: Energy Per Month**
    *   $10.833 \times 30 = 325$ Units.
*   **Step 3: Bill Calculation**
    *   **Fixed Charges (3kW Load):**
        *   First kW: Rs. 50.
        *   Next 2 kW: $2 \times 60 = 120$.
        *   Total FC = Rs. 170.
    *   **Energy Charges (325 Units):**
        *   0-30 Units @ Rs. 3.50: $30 \times 3.5 = 105$.
        *   31-100 Units @ Rs. 4.95: $70 \times 4.95 = 346.5$.
        *   101-200 Units @ Rs. 6.50: $100 \times 6.5 = 650$.
        *   201-300 Units @ Rs. 7.55: $100 \times 7.55 = 755$.
        *   301-325 Units @ Rs. 7.60: $25 \times 7.6 = 190$.
        *   Total EC = Rs. 2046.5.
    *   **Fuel Adjustment Charges (FAC):**
        *   $325 \times 0.14 = 45.5$ Rs.
    *   **Total Amount (Excl Tax):** $170 + 2046.5 + 45.5 = 2262$ Rs.
    *   **Tax (7.3%):** $2262 \times 0.073 = 165.13$ Rs.
    *   **Grand Total:** Rs. 2427.13.

***
***