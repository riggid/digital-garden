---
{"dg-publish":true,"permalink":"/semester-1/physics/unit-3/core-notes/"}
---


# [[Semester 1/Physics/Physics\|Back]]
***
[[Semester 1/Physics/Unit 3/Core Notes\|Core Notes]] | [[Semester 1/Physics/Unit 3/Examples\|Examples]] | [[Semester 1/Physics/Unit 3/Q&A\|Questions]]
***
# Unit 3: Quantum Mechanical Treatment of Electron Transport and Magnetic Materials

## 1. Classical Free Electron Theory (CFET)

The **Classical Free Electron Theory (CFET)** was proposed by Drude and Lorentz (1904) to explain the electrical and thermal conductivity of metals. It models conduction electrons as a gas of free particles.

### **1.1 Review: Electrical Conduction in CFET**

#### **1.1.1 Basic Assumptions of CFET**
The basic assumptions of the Classical Free Electron Theory are:
*   **Free Electrons**: Valence electrons become free electrons and move randomly within the metal, like molecules in an ideal gas.
*   **Fixed Ion Cores**: Positive ion cores (the atomic nuclei plus core electrons) form a fixed array. Their direct electric field effect on electrons is considered constant or negligible, but they act as scattering centers for the electrons.
*   **Negligible Electron-Electron Repulsion**: Electrostatic repulsion between the free electrons themselves is neglected, simplifying the dynamics to electron-ion core interactions only.
*   **Classical Statistics**: Electrons obey classical Maxwell-Boltzmann statistics, implying a continuous distribution of energies and no restrictions on quantum states.
*   **Collisions**: Electrons collide with stationary positive ion cores. These collisions are the primary cause of electrical resistance. The average time an electron travels between two successive collisions is called the **relaxation time ($\tau$)**.

#### **1.1.2 Distribution Functions**
A **distribution function** is a mathematical function that describes how particles (or states, or properties) are distributed across different values of a relevant variable (e.g., energy, velocity, momentum) within a system. In statistical mechanics, these functions quantify the probability of finding a particle in a particular state or energy level at a given temperature. They are fundamental for characterizing the statistical behavior of large ensembles of particles.

#### **1.1.3 Maxwell-Boltzmann Distribution Function (Review)**
The **Maxwell-Boltzmann (MB) distribution function** is a classical statistical distribution used to describe the energies or speeds of distinguishable particles (like atoms or molecules in an ideal gas) at thermal equilibrium.
*   **Key Features**:
    *   **Classical Particles**: Applies to classical particles where quantum effects and inter-particle interactions (like the Pauli Exclusion Principle) are negligible. Particles are considered distinguishable.
    *   **Energy Distribution**: The probability $P(E)$ of a particle being in a state with energy $E$ is proportional to $e^{-E/k_B T}$, where $k_B$ is the Boltzmann constant and $T$ is the absolute temperature. This implies that higher energy states are exponentially less likely to be occupied than lower energy states.
    *   **No State Limit**: There is no restriction on how many particles can occupy the same energy state.
*   **Application in CFET**: CFET assumed electrons behave as a classical ideal gas. This leads to the prediction that the average kinetic energy of an electron is $\frac{3}{2}k_B T$, which implies a high thermal velocity.

#### **1.1.4 Electrical Parameters and Expression for Conductivity (CFET)**
1.  **Thermal Velocity ($\mathbf{v_{th}}$)**: This is the average speed of electrons due to their thermal energy (temperature).
    $$v_{th} = \sqrt{\frac{3k_B T}{m}}$$
    At typical room temperatures (like 300K), this velocity is quite high, around $10^5 \text{ m/s}$. This random thermal motion does *not* contribute to the net electric current because electrons move in all directions equally.
2.  **Drift Velocity ($\mathbf{v_d}$)**: When an external **electric field ($\vec{E}$)** is applied, electrons acquire a net average velocity in a direction opposite to $\vec{E}$. This is the velocity component that *does* contribute to the current. Due to collisions, electrons don't accelerate indefinitely.
    The force equation for an electron (mass $m$, charge $e$) balances electric force with a scattering term, leading to the steady-state drift velocity:
    $$\mathbf{v_d} = \frac{-e\tau}{m}\vec{E}$$
3.  **Electron Mobility ($\mu$)**: Mobility measures how "mobile" electrons are in an electric field. It's the magnitude of drift velocity per unit electric field.
    $$\mu = \frac{|\mathbf{v_d}|}{E} = \frac{e\tau}{m}$$
4.  **Electrical Conductivity ($\sigma$) and Resistivity ($\rho$)**:
    The current density ($\vec{J}$) is related to free electron concentration ($n$), charge ($e$), and drift velocity ($v_d$):
    $$\vec{J} = n e \mathbf{v_d}$$
    Substituting $\mathbf{v_d} = \frac{-e\tau}{m}\vec{E}$ (ignoring the negative sign for positive current direction, focusing on magnitude):
    $$\vec{J} = n e \left(\frac{e\tau}{m}\vec{E}\right) = \frac{ne^2\tau}{m}\vec{E}$$
    By Ohm's Law in microscopic form, $\vec{J} = \sigma \vec{E}$. Comparing this to the above expression, the **dc electrical conductivity ($\sigma$)** in CFET is:
    $$\sigma = \frac{ne^2\tau}{m}$$
    Where $n$ is the free electron concentration (number of free electrons per unit volume).
    **Resistivity ($\rho$)** is the inverse of conductivity:
    $$\rho = \frac{1}{\sigma} = \frac{m}{ne^2\tau}$$
    > See also: [Examples](Examples.md#Example%207:%20Relaxation%20Time%20in%20a%20Metal)
5.  **Mean Free Path ($\lambda$)**: The average distance an electron travels between successive collisions with ion cores or other scattering centers. It is related to the relaxation time ($\tau$) and the electron's velocity ($v_{th}$): $\lambda = v_{th} \tau$.

#### **1.1.5 Derivation of Thermal Conductivity (CFET)**
While superseded by QFET, for completeness within the classical framework, thermal conductivity ($K$) can be derived using the classical kinetic theory of gases:
$$K = \frac{1}{3} C_v \langle v \rangle \lambda$$
Where:
*   $C_v = \frac{3}{2} n k_B$ is the classical electronic specific heat per unit volume for a 3D gas of $n$ electrons.
*   $\langle v \rangle$ is the average thermal velocity ($v_{th}$).
*   $\lambda$ is the mean free path ($\lambda = v_{th}\tau$).
Substituting these values leads to similar issues of overestimation as for electronic specific heat.

#### **1.1.6 Experimental Temperature Dependence of Resistivity**
Experimental results show that resistivity of pure metals increases roughly linearly with temperature: $\rho \propto T$.
For alloys or impure metals, **Matthiessen's Rule** states that total resistivity is the sum of residual resistivity ($\rho_{res}$) and scattering resistivity ($\rho_{sc}$):
$$\rho = \rho_{res} + \rho_{sc}$$
*   $\rho_{res}$: Independent of temperature, due to impurities and structural defects.
*   $\rho_{sc}$: Temperature dependent, due to electron scattering by lattice vibrations.
This implies an effective relaxation time: $1/\tau = 1/\tau_{res} + 1/\tau_{sc}$.

### **1.2 Failures of Classical Free Electron Theory**

1.  **Incorrect Temperature Dependence of Resistivity**:
    *   **CFET Prediction**: $\rho = \frac{m}{ne^2\tau}$. If $\tau \propto \lambda/v_{th}$ and $v_{th} \propto \sqrt{T}$ (assuming `mean free path ($\lambda$)` is constant), CFET predicts $\rho \propto v_{th} \propto \sqrt{T}$.
    *   **Experimental observation**: For most pure metals, resistivity increases *linearly* with temperature ($\rho \propto T$).
    *   **Conclusion**: CFET fails to explain the correct temperature dependence.
2.  **Vastly Overestimated Specific Heat of Electrons ($\mathbf{C_{el}}$)**:
    *   **CFET Prediction**: According to classical Boltzmann statistics, each free electron should contribute $\frac{3}{2}k_B$ to the specific heat. For 1 mole, $C_{el} = \frac{3}{2}N_A k_B = \frac{3}{2}R$.
    *   **Experimental observation**: The electronic contribution to specific heat is found to be only about 1-2% of the classical prediction at room temperature and decreases differently with temperature ($C_{el} \propto T$).
    *   **Conclusion**: CFET vastly overestimates $C_{el}$.
3.  **Inconsistent Conductivity Variations with Electron Concentrations**:
    *   **CFET Prediction**: $\sigma \propto n$, so metals with higher free electron concentration ($n$) should be better conductors.
    *   **Experimental observation**: Metals like copper (1 valence electron per atom) have higher conductivity than aluminum (3 valence electrons per atom), which contradicts the simple proportionality.
    *   **Conclusion**: CFET cannot explain the varying conductivities based solely on electron concentration.
4.  **Inability to Explain Positive Hall Coefficient**:
    *   **CFET Prediction**: Since current is carried only by negatively charged electrons, CFET predicts a *negative* Hall coefficient for all metals.
    *   **Experimental observation**: Some metals (e.g., Zinc, Cadmium) exhibit a *positive* Hall coefficient, implying charge carriers are positive (*holes*), which CFET cannot account for.

---

## 2. Quantum Free Electron Theory (QFET)

The significant failures of CFET at a quantitative level (and some qualitative aspects) ultimately necessitated incorporating quantum mechanics, leading to the **Quantum Free Electron Theory (QFET)**. The key changes are treating electrons as quantum particles governed by Fermi-Dirac statistics and the Pauli Exclusion Principle.

### **2.1 Concepts of Quantum Free Electron Gas**

#### **2.1.1 Defining Features of a Quantum Free Electron Gas**
The defining features of a quantum free electron gas, which fundamentally distinguish it from a classical gas, are:
1.  **Energy Quantization for a Particle in a Box**: Electrons are treated as particles confined within the metal's volume, which is approximated as a three-dimensional potential well (or "box"). Solving the Schrödinger equation for such a system demonstrates that the electron's energy can only take on discrete, quantized values, rather than a continuous range. These allowed energy levels form the fundamental energy landscape for electrons in the metal.
    *   **Significance**: This quantization critically changes how electrons occupy energy states compared to classical particles, whose energy can be continuous.
2.  **Application of the Pauli Exclusion Principle**: Electrons are fundamental particles classified as fermions, meaning they possess half-integer spin. Fermions obey the Pauli Exclusion Principle, which states that no two identical fermions can occupy the *exact same quantum state simultaneously* (a quantum state is defined by its energy, momentum, and spin).
    *   **Significance**: This principle dictates that, even at absolute zero temperature (0 K), electrons cannot all collapse into the lowest energy level. Instead, they must fill available energy levels sequentially, starting from the lowest energy up to a certain maximum energy called the **Fermi energy ($E_f$)**. This creates a "Fermi sea" of electrons, where electrons possess high kinetic energy even at 0 K, a concept entirely absent in classical physics.

#### **2.1.2 Fermions vs. Bosons**
Particles in the universe are fundamentally classified into two groups based on their intrinsic spin and the statistical laws they obey. These are Fermions and Bosons.

| Feature                | Fermions                                        | Bosons                                                |
| :--------------------- | :---------------------------------------------- | :---------------------------------------------------- |
| **Spin**               | Half-integer spin (e.g., 1/2, 3/2, 5/2, ...)    | Integer spin (e.g., 0, 1, 2, ...)                     |
| **Statistics obeyed**  | Fermi-Dirac statistics                          | Bose-Einstein statistics                              |
| **Pauli Exclusion Principle** | **Obey**: No two identical fermions can occupy the same quantum state simultaneously. | **Do not obey**: Multiple identical bosons can occupy the same quantum state. |
| **Wave Function Symmetry** | Anti-symmetric upon particle exchange           | Symmetric upon particle exchange                      |
| **Behavior at Low T**  | Tend to occupy distinct energy states, forming a "Fermi sea." | Tend to condense into the lowest energy quantum state (Bose-Einstein Condensation). |
| **Examples**           | Electrons, Protons, Neutrons, Quarks, Neutrinos | Photons, Phonons, Gluons, Higgs boson, Cooper pairs |
*   Electrons, being fermions, are subject to the Pauli Exclusion Principle, which has profound implications for their energy distribution in metals, giving rise to the concepts of Fermi energy and the Fermi sea.

### **2.2 DoS, Fermi Energy, Velocity and Temperature, Fermi Factor**

#### **2.2.1 Fermi-Dirac Statistics and Fermi Factor**
*   **Fermi-Dirac Distribution Function ($F_d(E)$)**: Gives the probability that an energy state $E$ is occupied by an electron at temperature $T$. This distribution is crucial for quantum systems of fermions.
    $$F_d(E) = \frac{1}{e^{(E-E_f)/k_B T} + 1}$$
    Where $E_f$ is the **Fermi energy** and $k_B$ is the Boltzmann constant.
    > See also: [Examples](Examples.md#Example%201:%20Fermi%20Factor%20Calculation)
*   **Interpretation of $\mathbf{F_d(E)}$**:
    *   **At T=0K**: (Absolute Zero Temperature)
        *   If $E < E_f$: The exponent $(E-E_f)/k_B T \rightarrow -\infty$. So $F_d(E) = \frac{1}{e^{-\infty} + 1} = \frac{1}{0+1} = 1$. This means all energy states below the Fermi energy are completely filled.
        *   If $E > E_f$: The exponent $(E-E_f)/k_B T \rightarrow +\infty$. So $F_d(E) = \frac{1}{e^{\infty} + 1} = \frac{1}{\infty+1} = 0$. This means all energy states above the Fermi energy are completely empty.
    *   **At T > 0K**: (Finite Temperatures)
        *   If $E = E_f$: The exponent $(E-E_f)/k_B T = 0$. So $F_d(E) = \frac{1}{e^0 + 1} = \frac{1}{1+1} = 0.5$. The Fermi energy level (at $E_f$) has a 50% probability of being occupied.
        *   For $E$ close to $E_f$: The sharp step function observed at 0K begins to soften. Some electrons just below $E_f$ (within an energy range of a few $k_B T$) are thermally excited to states just above $E_f$, leaving unoccupied states below $E_f$ and occupying states above $E_f$. This indicates that only a small fraction of electrons near the Fermi level are thermally active.
    **Description of Plot (Fermi Factor):** The plot shows the Fermi-Dirac distribution function $F_d(E)$ as a function of energy $E$. At $T=0K$, it is a perfectly sharp step function: the occupation probability is 1 for all energies $E < E_f$ and drops discontinuously to 0 for all energies $E > E_f$. As temperature $T$ increases ($T_1 < T_2$), the sharp step at $E_f$ softens and becomes a smooth, S-shaped curve. This rounding indicates that thermal energy allows some electrons below $E_f$ to be excited to states above $E_f$. For all temperatures, the curve passes through $F_d(E)=0.5$ precisely at $E=E_f$.
    <?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<!-- Created with matplotlib (http://matplotlib.sourceforge.net/) -->
<svg width="283pt" height="282pt" viewBox="0 0 283 282"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:xlink="http://www.w3.org/1999/xlink"
   version="1.1"
   id="svg1">
<filter id="colorAdd"><feComposite in="SourceGraphic" in2="BackgroundImage" operator="arithmetic" k2="1" k3="1"/></filter>
<g id="figure1">
<g id="patch1">
<path style="fill: #ffffff; stroke: #ffffff; stroke-width: 1.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000"  d="M0.000000 282.078125L283.260937 282.078125L283.260937 0.000000
L0.000000 0.000000z"/>
</g>
<g id="axes1">
<g id="patch2">
<path style="fill: none; opacity: 0.000000"  d="M46.425000 241.200000L269.625000 241.200000L269.625000 10.800000
L46.425000 10.800000z"/>
</g>
<g id="line2d1">
<defs>
  <clipPath id="pc00436fc3cafe1fa0aef664171630eda">
<rect x="46.425000" y="10.800000" width="223.200000" height="230.400000"/>
  </clipPath>
</defs><path style="fill: none; stroke: #00bfbf; stroke-width: 2.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000" clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)" d="M46.425000 30.000000L48.679545 30.000000L50.934091 30.000000
L53.188636 30.000000L55.443182 30.000000L57.697727 30.000000
L59.952273 30.000000L62.206818 30.000000L64.461364 30.000000
L66.715909 30.000000L68.970455 30.000000L71.225000 30.000000
L73.479545 30.000000L75.734091 30.000000L77.988636 30.000000
L80.243182 30.000000L82.497727 30.000001L84.752273 30.000139
L87.006818 30.021633L89.261364 33.318968L91.515909 170.743664
L93.770455 221.553109L96.025000 221.997131L98.279545 221.999982
L100.534091 222.000000L102.788636 222.000000L105.043182 222.000000
L107.297727 222.000000L109.552273 222.000000L111.806818 222.000000
L114.061364 222.000000L116.315909 222.000000L118.570455 222.000000
L120.825000 222.000000L123.079545 222.000000L125.334091 222.000000
L127.588636 222.000000L129.843182 222.000000L132.097727 222.000000
L134.352273 222.000000L136.606818 222.000000L138.861364 222.000000
L141.115909 222.000000L143.370455 222.000000L145.625000 222.000000
L147.879545 222.000000L150.134091 222.000000L152.388636 222.000000
L154.643182 222.000000L156.897727 222.000000L159.152273 222.000000
L161.406818 222.000000L163.661364 222.000000L165.915909 222.000000
L168.170455 222.000000L170.425000 222.000000L172.679545 222.000000
L174.934091 222.000000L177.188636 222.000000L179.443182 222.000000
L181.697727 222.000000L183.952273 222.000000L186.206818 222.000000
L188.461364 222.000000L190.715909 222.000000L192.970455 222.000000
L195.225000 222.000000L197.479545 222.000000L199.734091 222.000000
L201.988636 222.000000L204.243182 222.000000L206.497727 222.000000
L208.752273 222.000000L211.006818 222.000000L213.261364 222.000000
L215.515909 222.000000L217.770455 222.000000L220.025000 222.000000
L222.279545 222.000000L224.534091 222.000000L226.788636 222.000000
L229.043182 222.000000L231.297727 222.000000L233.552273 222.000000
L235.806818 222.000000L238.061364 222.000000L240.315909 222.000000
L242.570455 222.000000L244.825000 222.000000L247.079545 222.000000
L249.334091 222.000000L251.588636 222.000000L253.843182 222.000000
L256.097727 222.000000L258.352273 222.000000L260.606818 222.000000
L262.861364 222.000000L265.115909 222.000000L267.370455 222.000000
L269.625000 222.000000"/>
</g>
<g id="line2d2">
<path style="fill: none; stroke: #0000ff; stroke-width: 2.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000" clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)" d="M46.425000 30.008716L48.679545 30.014443L50.934091 30.023932
L53.188636 30.039654L55.443182 30.065701L57.697727 30.108846
L59.952273 30.180299L62.206818 30.298583L64.461364 30.494268
L66.715909 30.817653L68.970455 31.351126L71.225000 32.228605
L73.479545 33.665000L75.734091 35.997930L77.988636 39.739077
L80.243182 45.617793L82.497727 54.566727L84.752273 67.551680
L87.006818 85.139693L89.261364 106.865660L91.515909 130.844367
L93.770455 154.231997L96.025000 174.448550L98.279545 190.178897
L100.534091 201.445988L102.788636 209.046296L105.043182 213.967884
L107.297727 217.071055L109.552273 218.994915L111.806818 220.175181
L114.061364 220.894601L116.315909 221.331393L118.570455 221.595954
L120.825000 221.755965L123.079545 221.852657L125.334091 221.911055
L127.588636 221.946314L129.843182 221.967598L132.097727 221.980445
L134.352273 221.988199L136.606818 221.992878L138.861364 221.995702
L141.115909 221.997406L143.370455 221.998435L145.625000 221.999055
L147.879545 221.999430L150.134091 221.999656L152.388636 221.999792
L154.643182 221.999875L156.897727 221.999924L159.152273 221.999954
L161.406818 221.999972L163.661364 221.999983L165.915909 221.999990
L168.170455 221.999994L170.425000 221.999996L172.679545 221.999998
L174.934091 221.999999L177.188636 221.999999L179.443182 222.000000
L181.697727 222.000000L183.952273 222.000000L186.206818 222.000000
L188.461364 222.000000L190.715909 222.000000L192.970455 222.000000
L195.225000 222.000000L197.479545 222.000000L199.734091 222.000000
L201.988636 222.000000L204.243182 222.000000L206.497727 222.000000
L208.752273 222.000000L211.006818 222.000000L213.261364 222.000000
L215.515909 222.000000L217.770455 222.000000L220.025000 222.000000
L222.279545 222.000000L224.534091 222.000000L226.788636 222.000000
L229.043182 222.000000L231.297727 222.000000L233.552273 222.000000
L235.806818 222.000000L238.061364 222.000000L240.315909 222.000000
L242.570455 222.000000L244.825000 222.000000L247.079545 222.000000
L249.334091 222.000000L251.588636 222.000000L253.843182 222.000000
L256.097727 222.000000L258.352273 222.000000L260.606818 222.000000
L262.861364 222.000000L265.115909 222.000000L267.370455 222.000000
L269.625000 222.000000"/>
</g>
<g id="line2d3">
<path style="fill: none; stroke: #ff0000; stroke-width: 2.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000" clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)" d="M46.425000 52.886961L48.679545 55.002785L50.934091 57.282655
L53.188636 59.733399L55.443182 62.361038L57.697727 65.170559
L59.952273 68.165683L62.206818 71.348623L64.461364 74.719846
L66.715909 78.277849L68.970455 82.018950L71.225000 85.937122
L73.479545 90.023869L75.734091 94.268162L77.988636 98.656445
L80.243182 103.172713L82.497727 107.798680L84.752273 112.514020
L87.006818 117.296690L89.261364 122.123321L91.515909 126.969664
L93.770455 131.811069L96.025000 136.622987L98.279545 141.381464
L100.534091 146.063612L102.788636 150.648031L105.043182 155.115176
L107.297727 159.447649L109.552273 163.630410L111.806818 167.650908
L114.061364 171.499131L116.315909 175.167581L118.570455 178.651188
L120.825000 181.947163L123.079545 185.054817L125.334091 187.975344
L127.588636 190.711590L129.843182 193.267809L132.097727 195.649431
L134.352273 197.862825L136.606818 199.915085L138.861364 201.813836
L141.115909 203.567051L143.370455 205.182900L145.625000 206.669613
L147.879545 208.035370L150.134091 209.288209L152.388636 210.435950
L154.643182 211.486139L156.897727 212.446006L159.152273 213.322431
L161.406818 214.121929L163.661364 214.850640L165.915909 215.514320
L168.170455 216.118350L170.425000 216.667742L172.679545 217.167150
L174.934091 217.620881L177.188636 218.032917L179.443182 218.406926
L181.697727 218.746284L183.952273 219.054092L186.206818 219.333192
L188.461364 219.586188L190.715909 219.815459L192.970455 220.023180
L195.225000 220.211336L197.479545 220.381735L199.734091 220.536026
L201.988636 220.675709L204.243182 220.802148L206.497727 220.916584
L208.752273 221.020143L211.006818 221.113849L213.261364 221.198632
L215.515909 221.275333L217.770455 221.344719L220.025000 221.407482
L222.279545 221.464250L224.534091 221.515592L226.788636 221.562026
L229.043182 221.604018L231.297727 221.641992L233.552273 221.676330
L235.806818 221.707379L238.061364 221.735454L240.315909 221.760839
L242.570455 221.783791L244.825000 221.804542L247.079545 221.823304
L249.334091 221.840266L251.588636 221.855601L253.843182 221.869465
L256.097727 221.881999L258.352273 221.893329L260.606818 221.903573
L262.861364 221.912833L265.115909 221.921204L267.370455 221.928772
L269.625000 221.935613"/>
</g>
<g id="line2d4">
<path style="fill: none; stroke: #bfbf00; stroke-width: 2.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000" clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)" d="M46.425000 81.636753L48.679545 83.565389L50.934091 85.537559
L53.188636 87.552152L55.443182 89.607902L57.697727 91.703384
L59.952273 93.837010L62.206818 96.007039L64.461364 98.211575
L66.715909 100.448569L68.970455 102.715831L71.225000 105.011032
L73.479545 107.331712L75.734091 109.675291L77.988636 112.039081
L80.243182 114.420292L82.497727 116.816051L84.752273 119.223411
L87.006818 121.639366L89.261364 124.060870L91.515909 126.484844
L93.770455 128.908201L96.025000 131.327853L98.279545 133.740734
L100.534091 136.143811L102.788636 138.534101L105.043182 140.908684
L107.297727 143.264719L109.552273 145.599455L111.806818 147.910246
L114.061364 150.194560L116.315909 152.449987L118.570455 154.674253
L120.825000 156.865223L123.079545 159.020910L125.334091 161.139479
L127.588636 163.219249L129.843182 165.258699L132.097727 167.256466
L134.352273 169.211346L136.606818 171.122294L138.861364 172.988421
L141.115909 174.808989L143.370455 176.583410L145.625000 178.311241
L147.879545 179.992177L150.134091 181.626044L152.388636 183.212796
L154.643182 184.752506L156.897727 186.245358L159.152273 187.691643
L161.406818 189.091747L163.661364 190.446146L165.915909 191.755400
L168.170455 193.020142L170.425000 194.241072L172.679545 195.418951
L174.934091 196.554593L177.188636 197.648858L179.443182 198.702648
L181.697727 199.716896L183.952273 200.692567L186.206818 201.630644
L188.461364 202.532132L190.715909 203.398047L192.970455 204.229414
L195.225000 205.027262L197.479545 205.792621L199.734091 206.526519
L201.988636 207.229976L204.243182 207.904007L206.497727 208.549612
L208.752273 209.167782L211.006818 209.759488L213.261364 210.325688
L215.515909 210.867320L217.770455 211.385302L220.025000 211.880531
L222.279545 212.353885L224.534091 212.806215L226.788636 213.238354
L229.043182 213.651109L231.297727 214.045263L233.552273 214.421577
L235.806818 214.780787L238.061364 215.123606L240.315909 215.450722
L242.570455 215.762801L244.825000 216.060486L247.079545 216.344395
L249.334091 216.615127L251.588636 216.873255L253.843182 217.119333
L256.097727 217.353893L258.352273 217.577447L260.606818 217.790486
L262.861364 217.993482L265.115909 218.186888L267.370455 218.371138
L269.625000 218.546648"/>
</g>
<g id="GridlinesCollection1">
<defs>
<path id="coll0_0_3264fef2ae5a08129d412c2f516847ed" d="M46.425000 -40.878125L46.425000 -271.278125"/>
<path id="coll0_1_d2d09df3bc7841ca72bf19026e16179f" d="M91.065000 -40.878125L91.065000 -271.278125"/>
<path id="coll0_2_cabfeef48d57e228686605de5854562f" d="M135.705000 -40.878125L135.705000 -271.278125"/>
<path id="coll0_3_e605d2d9baf326b2ad1ed663210f1270" d="M180.345000 -40.878125L180.345000 -271.278125"/>
<path id="coll0_4_689ee0fc43ee2216c52f0fc173e531ce" d="M224.985000 -40.878125L224.985000 -271.278125"/>
<path id="coll0_5_42a1867eddec2cf9e1855265d55628e4" d="M269.625000 -40.878125L269.625000 -271.278125"/>
<path id="coll0_6_30e27a2f9a8c45fa5489e27261a90dc8" d="M46.425000 -60.078125L269.625000 -60.078125"/>
<path id="coll0_7_d34f5521550e19a38db4ef697b3728c4" d="M46.425000 -98.478125L269.625000 -98.478125"/>
<path id="coll0_8_e4f4ee87c35080e6b0a620438fcf0113" d="M46.425000 -136.878125L269.625000 -136.878125"/>
<path id="coll0_9_214c8a3012d6dccf30de293176349a33" d="M46.425000 -175.278125L269.625000 -175.278125"/>
<path id="coll0_a_e69e03b38cee649a6b65a16298fb08a8" d="M46.425000 -213.678125L269.625000 -213.678125"/>
<path id="coll0_b_21e758eb90076800bbae665182468a9c" d="M46.425000 -252.078125L269.625000 -252.078125"/>
</defs>
<g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_0_3264fef2ae5a08129d412c2f516847ed" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_1_d2d09df3bc7841ca72bf19026e16179f" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_2_cabfeef48d57e228686605de5854562f" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_3_e605d2d9baf326b2ad1ed663210f1270" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_4_689ee0fc43ee2216c52f0fc173e531ce" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_5_42a1867eddec2cf9e1855265d55628e4" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_6_30e27a2f9a8c45fa5489e27261a90dc8" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_7_d34f5521550e19a38db4ef697b3728c4" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_8_e4f4ee87c35080e6b0a620438fcf0113" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_9_214c8a3012d6dccf30de293176349a33" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_a_e69e03b38cee649a6b65a16298fb08a8" x="0.000000" y="282.078125"/>
</g><g clip-path="url(#pc00436fc3cafe1fa0aef664171630eda)"><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt; stroke-dasharray: 1.000000,3.000000; stroke-dashoffset: 0.000000; opacity: 1.000000" xlink:href="#coll0_b_21e758eb90076800bbae665182468a9c" x="0.000000" y="282.078125"/>
</g></g>
<g id="mpl_toolkits.axisartist.axis_artist1">
<g id="line2d5">
<path style="fill: none; stroke: #000000; stroke-width: 1.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000"  d="M46.425000 241.200000L46.425000 10.800000"/>
</g>
<defs><path id="m3400efa6b1638b3fea9e19e898273957" d="M0.000000 0.000000L4.000000 0.000000"/></defs>
<g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="222.000000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="222.000000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="183.600000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="183.600000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="145.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="145.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="106.800000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="106.800000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="68.400000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="68.400000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="30.000000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3400efa6b1638b3fea9e19e898273957" x="46.425000" y="30.000000"/>
</g><g id="text1">
<defs>
<path id="c_7a2040fe3b94fcd41d0a72c84e93b115" d="M31.781250 -66.406250q-7.609375 0.000000 -11.453125 7.500000q-3.828125 7.484375 -3.828125 22.531250q0.000000 14.984375 3.828125 22.484375q3.843750 7.500000 11.453125 7.500000q7.671875 0.000000 11.500000 -7.500000q3.843750 -7.500000 3.843750 -22.484375q0.000000 -15.046875 -3.843750 -22.531250q-3.828125 -7.500000 -11.500000 -7.500000M31.781250 -74.218750q12.265625 0.000000 18.734375 9.703125q6.468750 9.687500 6.468750 28.140625q0.000000 18.406250 -6.468750 28.109375q-6.468750 9.687500 -18.734375 9.687500q-12.250000 0.000000 -18.718750 -9.687500q-6.468750 -9.703125 -6.468750 -28.109375q0.000000 -18.453125 6.468750 -28.140625q6.468750 -9.703125 18.718750 -9.703125"/>
<path id="c_ed3e21196fb739f392806f09ca0594ef" d="M10.687500 -12.406250l10.312500 0.000000l0.000000 12.406250l-10.312500 0.000000z"/>
</defs>
<g style="fill: #000000; opacity: 1.000000" transform="translate(24.925000,226.367188)scale(0.120000)">
<use xlink:href="#c_7a2040fe3b94fcd41d0a72c84e93b115"/>
<use xlink:href="#c_ed3e21196fb739f392806f09ca0594ef" x="63.623047"/>
<use xlink:href="#c_7a2040fe3b94fcd41d0a72c84e93b115" x="95.410156"/>
</g>
</g>
<g id="text2">
<defs>
<path id="c_ed3f3ed3ebfbd18bcb9c012009a68ad1" d="M19.187500 -8.296875l34.421875 0.000000l0.000000 8.296875l-46.281250 0.000000l0.000000 -8.296875q5.609375 -5.812500 15.296875 -15.593750q9.703125 -9.796875 12.187500 -12.640625q4.734375 -5.312500 6.609375 -9.000000q1.890625 -3.687500 1.890625 -7.250000q0.000000 -5.812500 -4.078125 -9.468750q-4.078125 -3.671875 -10.625000 -3.671875q-4.640625 0.000000 -9.796875 1.609375q-5.140625 1.609375 -11.000000 4.890625l0.000000 -9.968750q5.953125 -2.390625 11.125000 -3.609375q5.187500 -1.218750 9.484375 -1.218750q11.328125 0.000000 18.062500 5.671875q6.734375 5.656250 6.734375 15.125000q0.000000 4.500000 -1.687500 8.531250q-1.671875 4.015625 -6.125000 9.484375q-1.218750 1.421875 -7.765625 8.187500q-6.531250 6.765625 -18.453125 18.921875"/>
</defs>
<g style="fill: #000000; opacity: 1.000000" transform="translate(25.331250,187.967188)scale(0.120000)">
<use xlink:href="#c_7a2040fe3b94fcd41d0a72c84e93b115"/>
<use xlink:href="#c_ed3e21196fb739f392806f09ca0594ef" x="63.623047"/>
<use xlink:href="#c_ed3f3ed3ebfbd18bcb9c012009a68ad1" x="95.410156"/>
</g>
</g>
<g id="text3">
<defs>
<path id="c_a0416418d96557a09b8c1332d34883ba" d="M37.796875 -64.312500l-24.906250 38.921875l24.906250 0.000000zM35.203125 -72.906250l12.406250 0.000000l0.000000 47.515625l10.406250 0.000000l0.000000 8.203125l-10.406250 0.000000l0.000000 17.187500l-9.812500 0.000000l0.000000 -17.187500l-32.906250 0.000000l0.000000 -9.515625z"/>
</defs>
<g style="fill: #000000; opacity: 1.000000" transform="translate(24.800000,149.567188)scale(0.120000)">
<use xlink:href="#c_7a2040fe3b94fcd41d0a72c84e93b115"/>
<use xlink:href="#c_ed3e21196fb739f392806f09ca0594ef" x="63.623047"/>
<use xlink:href="#c_a0416418d96557a09b8c1332d34883ba" x="95.410156"/>
</g>
</g>
<g id="text4">
<defs>
<path id="c_cc8d6d580d1b10c8632f7a42cd53db8a" d="M33.015625 -40.375000q-6.640625 0.000000 -10.531250 4.546875q-3.875000 4.531250 -3.875000 12.437500q0.000000 7.859375 3.875000 12.437500q3.890625 4.562500 10.531250 4.562500q6.640625 0.000000 10.515625 -4.562500q3.875000 -4.578125 3.875000 -12.437500q0.000000 -7.906250 -3.875000 -12.437500q-3.875000 -4.546875 -10.515625 -4.546875M52.593750 -71.296875l0.000000 8.984375q-3.718750 -1.750000 -7.500000 -2.671875q-3.781250 -0.937500 -7.500000 -0.937500q-9.765625 0.000000 -14.921875 6.593750q-5.140625 6.593750 -5.875000 19.921875q2.875000 -4.250000 7.218750 -6.515625q4.359375 -2.265625 9.578125 -2.265625q10.984375 0.000000 17.359375 6.671875q6.375000 6.656250 6.375000 18.125000q0.000000 11.234375 -6.640625 18.031250q-6.640625 6.781250 -17.671875 6.781250q-12.656250 0.000000 -19.343750 -9.687500q-6.687500 -9.703125 -6.687500 -28.109375q0.000000 -17.281250 8.203125 -27.562500q8.203125 -10.281250 22.015625 -10.281250q3.718750 0.000000 7.500000 0.734375q3.781250 0.734375 7.890625 2.187500"/>
</defs>
<g style="fill: #000000; opacity: 1.000000" transform="translate(24.893750,111.167188)scale(0.120000)">
<use xlink:href="#c_7a2040fe3b94fcd41d0a72c84e93b115"/>
<use xlink:href="#c_ed3e21196fb739f392806f09ca0594ef" x="63.623047"/>
<use xlink:href="#c_cc8d6d580d1b10c8632f7a42cd53db8a" x="95.410156"/>
</g>
</g>
<g id="text5">
<defs>
<path id="c_bef35738d52871942e50b9de9b122bab" d="M31.781250 -34.625000q-7.031250 0.000000 -11.062500 3.765625q-4.015625 3.765625 -4.015625 10.343750q0.000000 6.593750 4.015625 10.359375q4.031250 3.765625 11.062500 3.765625q7.031250 0.000000 11.078125 -3.781250q4.062500 -3.796875 4.062500 -10.343750q0.000000 -6.578125 -4.031250 -10.343750q-4.015625 -3.765625 -11.109375 -3.765625M21.921875 -38.812500q-6.343750 -1.562500 -9.890625 -5.906250q-3.531250 -4.359375 -3.531250 -10.609375q0.000000 -8.734375 6.218750 -13.812500q6.234375 -5.078125 17.062500 -5.078125q10.890625 0.000000 17.093750 5.078125q6.203125 5.078125 6.203125 13.812500q0.000000 6.250000 -3.546875 10.609375q-3.531250 4.343750 -9.828125 5.906250q7.125000 1.656250 11.093750 6.500000q3.984375 4.828125 3.984375 11.796875q0.000000 10.609375 -6.468750 16.281250q-6.468750 5.656250 -18.531250 5.656250q-12.046875 0.000000 -18.531250 -5.656250q-6.468750 -5.671875 -6.468750 -16.281250q0.000000 -6.968750 4.000000 -11.796875q4.015625 -4.843750 11.140625 -6.500000M18.312500 -54.390625q0.000000 5.656250 3.531250 8.828125q3.546875 3.171875 9.937500 3.171875q6.359375 0.000000 9.937500 -3.171875q3.593750 -3.171875 3.593750 -8.828125q0.000000 -5.671875 -3.593750 -8.843750q-3.578125 -3.171875 -9.937500 -3.171875q-6.390625 0.000000 -9.937500 3.171875q-3.531250 3.171875 -3.531250 8.843750"/>
</defs>
<g style="fill: #000000; opacity: 1.000000" transform="translate(24.956250,72.767188)scale(0.120000)">
<use xlink:href="#c_7a2040fe3b94fcd41d0a72c84e93b115"/>
<use xlink:href="#c_ed3e21196fb739f392806f09ca0594ef" x="63.623047"/>
<use xlink:href="#c_bef35738d52871942e50b9de9b122bab" x="95.410156"/>
</g>
</g>
<g id="text6">
<defs>
<path id="c_42baa63129a918535c52adb20d687ea7" d="M12.406250 -8.296875l16.109375 0.000000l0.000000 -55.625000l-17.531250 3.515625l0.000000 -8.984375l17.437500 -3.515625l9.859375 0.000000l0.000000 64.609375l16.109375 0.000000l0.000000 8.296875l-41.984375 0.000000z"/>
</defs>
<g style="fill: #000000; opacity: 1.000000" transform="translate(25.440625,34.367188)scale(0.120000)">
<use xlink:href="#c_42baa63129a918535c52adb20d687ea7"/>
<use xlink:href="#c_ed3e21196fb739f392806f09ca0594ef" x="63.623047"/>
<use xlink:href="#c_7a2040fe3b94fcd41d0a72c84e93b115" x="95.410156"/>
</g>
</g>
<defs><path id="mb39cfcf7402899e54c4d755745537394" d="M0.000000 0.000000L2.000000 0.000000"/></defs>
<g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="231.600000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="231.600000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="212.400000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="212.400000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="202.800000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="202.800000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="193.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="193.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="174.000000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="174.000000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="164.400000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="164.400000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="154.800000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="154.800000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="135.600000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="135.600000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="126.000000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="126.000000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="116.400000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="116.400000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="97.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="97.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="87.600000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="87.600000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="78.000000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="78.000000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="58.800000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="58.800000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="49.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="49.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="39.600000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="39.600000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="20.400000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="20.400000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="10.800000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#mb39cfcf7402899e54c4d755745537394" x="46.425000" y="10.800000"/>
</g><g id="text7">
<defs>
<path id="c_3df74f7e6714e1be4a23458a5075a645" d="M6.890625 -55.515625l0.000000 -3.468750l36.125000 0.000000l0.000000 3.468750z"/>
<path id="c_4e79783b4799b416f9678acefc53a48a" d="M7.718750 -1.703125q0.000000 -0.593750 0.093750 -0.890625l7.468750 -29.828125q0.734375 -2.781250 0.734375 -4.890625q0.000000 -4.296875 -2.921875 -4.296875q-3.125000 0.000000 -4.640625 3.750000q-1.515625 3.734375 -2.937500 9.437500q0.000000 0.296875 -0.296875 0.468750q-0.281250 0.171875 -0.531250 0.171875l-1.171875 0.000000q-0.343750 0.000000 -0.593750 -0.359375q-0.234375 -0.375000 -0.234375 -0.671875q1.078125 -4.343750 2.078125 -7.359375q1.000000 -3.031250 3.125000 -5.515625q2.125000 -2.500000 5.296875 -2.500000q3.750000 0.000000 6.625000 2.375000q2.890625 2.359375 2.890625 6.015625q2.984375 -3.906250 6.984375 -6.140625q4.000000 -2.250000 8.500000 -2.250000q3.562500 0.000000 6.140625 1.218750q2.593750 1.218750 4.031250 3.687500q1.453125 2.468750 1.453125 5.875000q0.000000 4.109375 -1.843750 9.921875q-1.828125 5.812500 -4.562500 12.984375q-1.406250 3.265625 -1.406250 6.000000q0.000000 2.984375 2.281250 2.984375q3.906250 0.000000 6.515625 -4.187500q2.625000 -4.203125 3.703125 -9.000000q0.187500 -0.578125 0.828125 -0.578125l1.171875 0.000000q0.390625 0.000000 0.656250 0.250000q0.265625 0.234375 0.265625 0.625000q0.000000 0.093750 -0.093750 0.296875q-1.375000 5.656250 -4.765625 10.453125q-3.390625 4.781250 -8.468750 4.781250q-3.515625 0.000000 -6.015625 -2.421875q-2.484375 -2.421875 -2.484375 -5.875000q0.000000 -1.859375 0.781250 -3.906250q1.265625 -3.281250 2.906250 -7.812500q1.640625 -4.546875 2.687500 -8.687500q1.046875 -4.156250 1.046875 -7.328125q0.000000 -2.796875 -1.156250 -4.750000q-1.140625 -1.953125 -3.875000 -1.953125q-3.656250 0.000000 -6.734375 1.625000q-3.078125 1.609375 -5.375000 4.265625q-2.296875 2.656250 -4.187500 6.328125l-6.796875 27.187500q-0.343750 1.375000 -1.546875 2.343750q-1.187500 0.984375 -2.656250 0.984375q-1.218750 0.000000 -2.093750 -0.781250q-0.875000 -0.781250 -0.875000 -2.046875"/>
</defs>
<g id="mathtext1">
<g style="fill: #000000" transform="translate(19.800000,130.000000)rotate(-90.0)">
<use xlink:href="#c_3df74f7e6714e1be4a23458a5075a645" transform="translate(0.171875,-1.921875)scale(0.120000)"/>
<use xlink:href="#c_4e79783b4799b416f9678acefc53a48a" transform="translate(0.000000,-1.781250)scale(0.120000)"/>
</g>
</g>
</g>
</g>
<g id="mpl_toolkits.axisartist.axis_artist2">
<g id="line2d6">
<path style="fill: none; stroke: #000000; stroke-width: 1.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000"  d="M46.425000 241.200000L269.625000 241.200000"/>
</g>
<defs><path id="m30e32995789d870ad79a2e54c91cf9c6" d="M0.000000 0.000000L0.000000 -4.000000"/></defs>
<g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="46.425000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="46.425000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="91.065000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="91.065000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="135.705000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="135.705000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="180.345000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="180.345000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="224.985000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="224.985000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="269.625000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m30e32995789d870ad79a2e54c91cf9c6" x="269.625000" y="241.200000"/>
</g><g id="text8">
<g style="fill: #000000; opacity: 1.000000" transform="translate(43.401562,254.106250)scale(0.120000)">
<use xlink:href="#c_7a2040fe3b94fcd41d0a72c84e93b115"/>
</g>
</g>
<g id="text9">
<g style="fill: #000000; opacity: 1.000000" transform="translate(88.455625,254.106250)scale(0.120000)">
<use xlink:href="#c_42baa63129a918535c52adb20d687ea7"/>
</g>
</g>
<g id="text10">
<g style="fill: #000000; opacity: 1.000000" transform="translate(132.923750,254.106250)scale(0.120000)">
<use xlink:href="#c_ed3f3ed3ebfbd18bcb9c012009a68ad1"/>
</g>
</g>
<g id="text11">
<defs>
<path id="c_3dcfa38a02242cb63ec6726c6e70be7a" d="M40.578125 -39.312500q7.078125 1.515625 11.046875 6.312500q3.984375 4.781250 3.984375 11.812500q0.000000 10.781250 -7.421875 16.703125q-7.421875 5.906250 -21.093750 5.906250q-4.578125 0.000000 -9.437500 -0.906250q-4.859375 -0.906250 -10.031250 -2.718750l0.000000 -9.515625q4.093750 2.390625 8.968750 3.609375q4.890625 1.218750 10.218750 1.218750q9.265625 0.000000 14.125000 -3.656250q4.859375 -3.656250 4.859375 -10.640625q0.000000 -6.453125 -4.515625 -10.078125q-4.515625 -3.640625 -12.562500 -3.640625l-8.500000 0.000000l0.000000 -8.109375l8.890625 0.000000q7.265625 0.000000 11.125000 -2.906250q3.859375 -2.906250 3.859375 -8.375000q0.000000 -5.609375 -3.984375 -8.609375q-3.968750 -3.015625 -11.390625 -3.015625q-4.062500 0.000000 -8.703125 0.890625q-4.640625 0.875000 -10.203125 2.718750l0.000000 -8.781250q5.625000 -1.562500 10.531250 -2.343750q4.906250 -0.781250 9.250000 -0.781250q11.234375 0.000000 17.765625 5.109375q6.546875 5.093750 6.546875 13.781250q0.000000 6.062500 -3.468750 10.234375q-3.468750 4.171875 -9.859375 5.781250"/>
</defs>
<g style="fill: #000000; opacity: 1.000000" transform="translate(177.470000,254.106250)scale(0.120000)">
<use xlink:href="#c_3dcfa38a02242cb63ec6726c6e70be7a"/>
</g>
</g>
<g id="text12">
<g style="fill: #000000; opacity: 1.000000" transform="translate(221.797500,254.106250)scale(0.120000)">
<use xlink:href="#c_a0416418d96557a09b8c1332d34883ba"/>
</g>
</g>
<g id="text13">
<defs>
<path id="c_1260a2df50f305f3db244e29828f968e" d="M10.796875 -72.906250l38.718750 0.000000l0.000000 8.312500l-29.687500 0.000000l0.000000 17.859375q2.140625 -0.734375 4.281250 -1.093750q2.156250 -0.359375 4.312500 -0.359375q12.203125 0.000000 19.328125 6.687500q7.140625 6.687500 7.140625 18.109375q0.000000 11.765625 -7.328125 18.296875q-7.328125 6.515625 -20.656250 6.515625q-4.593750 0.000000 -9.359375 -0.781250q-4.750000 -0.781250 -9.828125 -2.343750l0.000000 -9.921875q4.390625 2.390625 9.078125 3.562500q4.687500 1.171875 9.906250 1.171875q8.453125 0.000000 13.375000 -4.437500q4.937500 -4.437500 4.937500 -12.062500q0.000000 -7.609375 -4.937500 -12.046875q-4.921875 -4.453125 -13.375000 -4.453125q-3.953125 0.000000 -7.890625 0.875000q-3.921875 0.875000 -8.015625 2.734375z"/>
</defs>
<g style="fill: #000000; opacity: 1.000000" transform="translate(266.789062,254.106250)scale(0.120000)">
<use xlink:href="#c_1260a2df50f305f3db244e29828f968e"/>
</g>
</g>
<defs><path id="m3b2d125790092c17af877e29e2858cbc" d="M0.000000 0.000000L0.000000 -2.000000"/></defs>
<g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="57.585000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="57.585000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="68.745000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="68.745000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="79.905000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="79.905000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="102.225000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="102.225000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="113.385000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="113.385000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="124.545000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="124.545000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="146.865000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="146.865000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="158.025000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="158.025000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="169.185000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="169.185000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="191.505000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="191.505000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="202.665000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="202.665000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="213.825000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="213.825000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="236.145000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="236.145000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="247.305000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="247.305000" y="241.200000"/>
</g><g ><use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="258.465000" y="241.200000"/>
<use style="fill: none; stroke: #000000; stroke-width: 0.500000; stroke-linejoin: round; stroke-linecap: butt;  opacity: 1.000000" xlink:href="#m3b2d125790092c17af877e29e2858cbc" x="258.465000" y="241.200000"/>
</g><g id="text14">
<defs>
<path id="c_64ca7deae3ee0f53b2efe8e14c3e90ca" d="M12.312500 -14.109375q0.000000 3.359375 1.218750 6.250000q1.218750 2.875000 3.671875 4.609375q2.468750 1.734375 5.796875 1.734375q2.250000 0.000000 4.781250 -0.968750q2.546875 -0.984375 4.718750 -2.156250q2.171875 -1.171875 2.218750 -1.171875q0.531250 0.000000 0.843750 0.609375q0.328125 0.609375 0.328125 1.203125q0.000000 0.531250 -0.296875 0.671875q-6.250000 4.453125 -12.687500 4.453125q-5.281250 0.000000 -9.531250 -2.468750q-4.250000 -2.468750 -6.562500 -6.859375q-2.312500 -4.390625 -2.312500 -9.625000q0.000000 -5.171875 2.093750 -9.828125q2.093750 -4.671875 5.796875 -8.140625q3.718750 -3.468750 8.406250 -5.390625q4.687500 -1.921875 9.812500 -1.921875l5.671875 0.000000q1.515625 0.000000 1.515625 1.500000q0.000000 0.843750 -0.562500 1.437500q-0.562500 0.578125 -1.343750 0.578125l-5.468750 0.000000q-4.000000 0.000000 -7.250000 1.765625q-3.250000 1.750000 -5.453125 4.875000q-2.187500 3.125000 -3.406250 7.078125l17.671875 0.000000q0.687500 0.000000 1.093750 0.421875q0.421875 0.406250 0.421875 1.031250q0.000000 0.843750 -0.546875 1.437500q-0.531250 0.578125 -1.359375 0.578125l-18.218750 0.000000q-1.062500 5.171875 -1.062500 8.296875"/>
<path id="c_62db141412f5d9d8ddcda81385ac812d" d="M5.609375 23.000000q0.000000 -0.296875 0.109375 -0.390625l34.765625 -96.390625q0.187500 -0.578125 0.671875 -0.890625q0.500000 -0.328125 1.125000 -0.328125q0.890625 0.000000 1.437500 0.546875q0.562500 0.531250 0.562500 1.453125l0.000000 0.390625l-34.765625 96.390625q-0.578125 1.218750 -1.890625 1.218750q-0.843750 0.000000 -1.437500 -0.593750q-0.578125 -0.578125 -0.578125 -1.406250"/>
<path id="c_3260b495c6402fff66ed286585579e9c" d="M2.781250 18.796875q0.000000 -0.578125 0.093750 -0.781250l14.703125 -59.031250q0.437500 -1.421875 1.578125 -2.296875q1.156250 -0.875000 2.625000 -0.875000q1.265625 0.000000 2.140625 0.765625q0.890625 0.750000 0.890625 2.015625q0.000000 0.296875 -0.031250 0.468750q-0.031250 0.171875 -0.078125 0.359375l-5.906250 23.390625q-0.968750 4.156250 -0.968750 7.171875q0.000000 3.718750 1.750000 6.109375q1.765625 2.390625 5.328125 2.390625q7.265625 0.000000 12.796875 -9.078125q0.046875 -0.093750 0.062500 -0.140625q0.031250 -0.062500 0.031250 -0.156250l7.218750 -29.000000q0.343750 -1.328125 1.562500 -2.265625q1.218750 -0.953125 2.640625 -0.953125q1.171875 0.000000 2.078125 0.781250q0.906250 0.781250 0.906250 2.046875q0.000000 0.578125 -0.109375 0.781250l-7.171875 28.812500q-0.734375 2.828125 -0.734375 4.875000q0.000000 4.296875 2.937500 4.296875q3.125000 0.000000 4.703125 -3.859375q1.593750 -3.859375 2.765625 -9.328125q0.187500 -0.578125 0.828125 -0.578125l1.171875 0.000000q0.390625 0.000000 0.656250 0.312500q0.265625 0.312500 0.265625 0.656250q-1.750000 6.984375 -3.828125 11.218750q-2.078125 4.218750 -6.765625 4.218750q-3.312500 0.000000 -5.875000 -1.906250q-2.562500 -1.906250 -3.343750 -5.125000q-2.500000 3.125000 -5.843750 5.078125q-3.343750 1.953125 -7.046875 1.953125q-6.250000 0.000000 -9.828125 -2.937500l-5.078125 20.218750q-0.281250 1.421875 -1.453125 2.296875q-1.171875 0.875000 -2.640625 0.875000q-1.218750 0.000000 -2.125000 -0.765625q-0.906250 -0.750000 -0.906250 -2.015625"/>
</defs>
<g id="mathtext2">
<g style="fill: #000000" transform="translate(148.525000,271.278125)">
<use xlink:href="#c_64ca7deae3ee0f53b2efe8e14c3e90ca" transform="translate(0.000000,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_62db141412f5d9d8ddcda81385ac812d" transform="translate(4.857422,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_3260b495c6402fff66ed286585579e9c" transform="translate(10.857422,-3.000000)scale(0.120000)"/>
</g>
</g>
</g>
</g>
<g id="legend1">
<g id="line2d7">
<path style="fill: none; stroke: #00bfbf; stroke-width: 2.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000"  d="M175.185000 28.800000L195.345000 28.800000"/>
</g>
<g id="line2d8">
</g>
<g id="text15">
<defs>
<path id="c_7834f07fc511277fc3d27d854f452306" d="M5.328125 -1.812500q0.000000 -0.578125 0.093750 -0.875000l14.500000 -57.812500q0.390625 -1.703125 0.484375 -2.687500q0.000000 -1.609375 -6.484375 -1.609375q-1.031250 0.000000 -1.031250 -1.312500q0.046875 -0.250000 0.218750 -0.875000q0.171875 -0.640625 0.437500 -0.984375q0.265625 -0.343750 0.765625 -0.343750l13.468750 -1.078125l0.296875 0.000000q0.000000 0.109375 0.343750 0.281250q0.343750 0.156250 0.390625 0.218750q0.187500 0.484375 0.187500 0.781250l-10.500000 41.796875q3.625000 -1.515625 9.109375 -7.203125q5.500000 -5.687500 8.593750 -8.171875q3.109375 -2.500000 7.796875 -2.500000q2.781250 0.000000 4.734375 1.906250q1.953125 1.906250 1.953125 4.687500q0.000000 1.750000 -0.734375 3.250000q-0.734375 1.484375 -2.062500 2.421875q-1.312500 0.921875 -3.062500 0.921875q-1.609375 0.000000 -2.718750 -1.000000q-1.093750 -1.015625 -1.093750 -2.625000q0.000000 -2.390625 1.687500 -4.015625q1.687500 -1.640625 4.078125 -1.640625q-0.984375 -1.328125 -2.984375 -1.328125q-2.968750 0.000000 -5.734375 1.718750q-2.765625 1.703125 -5.968750 4.906250q-3.187500 3.203125 -5.828125 5.859375q-2.625000 2.656250 -4.875000 4.031250q5.906250 0.671875 10.250000 3.093750q4.343750 2.421875 4.343750 7.406250q0.000000 1.015625 -0.390625 2.578125q-0.875000 3.765625 -0.875000 6.015625q0.000000 4.484375 3.078125 4.484375q3.609375 0.000000 5.484375 -3.953125q1.890625 -3.953125 3.109375 -9.234375q0.187500 -0.578125 0.828125 -0.578125l1.171875 0.000000q0.390625 0.000000 0.656250 0.250000q0.265625 0.234375 0.265625 0.625000q0.000000 0.093750 -0.093750 0.296875q-3.765625 15.234375 -11.625000 15.234375q-2.828125 0.000000 -5.000000 -1.312500q-2.171875 -1.328125 -3.343750 -3.593750q-1.171875 -2.281250 -1.171875 -5.109375q0.000000 -1.609375 0.437500 -3.312500q0.296875 -1.171875 0.296875 -2.203125q0.000000 -3.859375 -3.421875 -5.859375q-3.421875 -2.000000 -7.812500 -2.437500l-5.078125 20.406250q-0.390625 1.515625 -1.515625 2.468750q-1.125000 0.953125 -2.578125 0.953125q-1.281250 0.000000 -2.187500 -0.859375q-0.890625 -0.859375 -0.890625 -2.078125"/>
<path id="c_4af9599587a0091f79c2f694637ff61b" d="M4.593750 -1.312500q0.046875 -0.250000 0.218750 -0.875000q0.171875 -0.640625 0.437500 -0.984375q0.265625 -0.343750 0.750000 -0.343750q8.593750 0.000000 11.390625 -0.484375q2.671875 -0.687500 3.218750 -2.890625l13.671875 -54.921875q0.437500 -1.218750 0.437500 -2.203125q0.000000 -0.781250 -3.515625 -0.781250l-5.812500 0.000000q-6.687500 0.000000 -10.328125 2.062500q-3.640625 2.046875 -5.343750 5.421875q-1.703125 3.359375 -4.390625 11.015625q-0.343750 0.890625 -1.031250 0.890625l-0.875000 0.000000q-1.031250 0.000000 -1.031250 -1.281250l7.125000 -20.703125q0.203125 -0.921875 0.984375 -0.921875l59.078125 0.000000q1.031250 0.000000 1.031250 1.312500l-3.328125 20.703125q0.000000 0.296875 -0.343750 0.593750q-0.328125 0.296875 -0.625000 0.296875l-0.937500 0.000000q-0.968750 0.000000 -0.968750 -1.281250q1.078125 -7.078125 1.078125 -10.000000q0.000000 -3.515625 -1.468750 -5.312500q-1.468750 -1.812500 -3.812500 -2.296875q-2.343750 -0.500000 -6.093750 -0.500000l-5.921875 0.000000q-2.671875 0.000000 -3.609375 0.500000q-0.921875 0.484375 -1.562500 2.921875l-13.718750 54.875000q-0.046875 0.203125 -0.078125 0.406250q-0.015625 0.187500 -0.109375 0.484375q0.000000 1.265625 1.500000 1.609375q2.593750 0.484375 11.093750 0.484375q0.968750 0.000000 0.968750 1.312500q-0.343750 1.421875 -0.546875 1.812500q-0.187500 0.390625 -1.109375 0.390625l-35.406250 0.000000q-1.015625 0.000000 -1.015625 -1.312500"/>
<path id="c_7bbc93c01755cdeb977d08bdfb9ce616" d="M7.515625 -13.281250q-0.828125 0.000000 -1.375000 -0.625000q-0.531250 -0.640625 -0.531250 -1.375000q0.000000 -0.828125 0.531250 -1.406250q0.546875 -0.593750 1.375000 -0.593750l62.796875 0.000000q0.734375 0.000000 1.265625 0.593750q0.546875 0.578125 0.546875 1.406250q0.000000 0.734375 -0.546875 1.375000q-0.531250 0.625000 -1.265625 0.625000zM7.515625 -32.718750q-0.828125 0.000000 -1.375000 -0.578125q-0.531250 -0.593750 -0.531250 -1.421875q0.000000 -0.734375 0.531250 -1.359375q0.546875 -0.640625 1.375000 -0.640625l62.796875 0.000000q0.734375 0.000000 1.265625 0.640625q0.546875 0.625000 0.546875 1.359375q0.000000 0.828125 -0.546875 1.421875q-0.531250 0.578125 -1.265625 0.578125z"/>
<path id="c_1a459ac34855d27ec37ccb0e66298d36" d="M9.281250 -0.000000l0.000000 -3.515625q12.500000 0.000000 12.500000 -3.171875l0.000000 -52.500000q-5.171875 2.500000 -13.093750 2.500000l0.000000 -3.515625q12.265625 0.000000 18.515625 -6.406250l1.406250 0.000000q0.343750 0.000000 0.656250 0.281250q0.328125 0.265625 0.328125 0.609375l0.000000 59.031250q0.000000 3.171875 12.500000 3.171875l0.000000 3.515625z"/>
<path id="c_f47f2818876b2f1a61c47f270461e46e" d="M25.000000 2.203125q-12.250000 0.000000 -16.671875 -10.078125q-4.421875 -10.093750 -4.421875 -24.015625q0.000000 -8.687500 1.578125 -16.343750q1.593750 -7.671875 6.296875 -13.015625q4.718750 -5.359375 13.218750 -5.359375q6.593750 0.000000 10.781250 3.234375q4.203125 3.218750 6.406250 8.328125q2.203125 5.093750 3.000000 10.937500q0.812500 5.828125 0.812500 12.218750q0.000000 8.593750 -1.593750 16.093750q-1.578125 7.500000 -6.218750 12.750000q-4.640625 5.250000 -13.187500 5.250000M25.000000 -0.390625q5.562500 0.000000 8.296875 -5.703125q2.734375 -5.718750 3.375000 -12.656250q0.640625 -6.937500 0.640625 -14.750000q0.000000 -7.515625 -0.640625 -13.859375q-0.640625 -6.359375 -3.359375 -11.500000q-2.703125 -5.156250 -8.312500 -5.156250q-5.656250 0.000000 -8.390625 5.187500q-2.734375 5.171875 -3.375000 11.500000q-0.640625 6.312500 -0.640625 13.828125q0.000000 5.562500 0.265625 10.500000q0.281250 4.937500 1.453125 10.187500q1.171875 5.250000 3.781250 8.843750q2.609375 3.578125 6.906250 3.578125"/>
</defs>
<g id="mathtext3">
<g style="fill: #000000" transform="translate(199.665000,36.840000)">
<use xlink:href="#c_7834f07fc511277fc3d27d854f452306" transform="translate(0.000000,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_4af9599587a0091f79c2f694637ff61b" transform="translate(6.240234,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_7bbc93c01755cdeb977d08bdfb9ce616" transform="translate(15.355078,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_3260b495c6402fff66ed286585579e9c" transform="translate(25.430859,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_62db141412f5d9d8ddcda81385ac812d" transform="translate(32.655469,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_1a459ac34855d27ec37ccb0e66298d36" transform="translate(38.655469,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_f47f2818876b2f1a61c47f270461e46e" transform="translate(44.655469,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_f47f2818876b2f1a61c47f270461e46e" transform="translate(50.655469,-3.000000)scale(0.120000)"/>
</g>
</g>
</g>
<g id="line2d9">
<path style="fill: none; stroke: #0000ff; stroke-width: 2.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000"  d="M175.185000 42.600000L195.345000 42.600000"/>
</g>
<g id="line2d10">
</g>
<g id="text16">
<g id="mathtext4">
<g style="fill: #000000" transform="translate(199.665000,50.640000)">
<use xlink:href="#c_7834f07fc511277fc3d27d854f452306" transform="translate(0.000000,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_4af9599587a0091f79c2f694637ff61b" transform="translate(6.240234,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_7bbc93c01755cdeb977d08bdfb9ce616" transform="translate(15.355078,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_3260b495c6402fff66ed286585579e9c" transform="translate(25.430859,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_62db141412f5d9d8ddcda81385ac812d" transform="translate(32.655469,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_1a459ac34855d27ec37ccb0e66298d36" transform="translate(38.655469,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_f47f2818876b2f1a61c47f270461e46e" transform="translate(44.655469,-3.000000)scale(0.120000)"/>
</g>
</g>
</g>
<g id="line2d11">
<path style="fill: none; stroke: #ff0000; stroke-width: 2.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000"  d="M175.185000 56.400000L195.345000 56.400000"/>
</g>
<g id="line2d12">
</g>
<g id="text17">
<defs>
<path id="c_1210e7f4d85518601ea3049211d562d0" d="M4.984375 -0.000000l0.000000 -2.687500q0.000000 -0.250000 0.187500 -0.531250l15.531250 -17.187500q3.515625 -3.812500 5.703125 -6.390625q2.203125 -2.593750 4.343750 -5.968750q2.156250 -3.375000 3.406250 -6.859375q1.250000 -3.484375 1.250000 -7.390625q0.000000 -4.109375 -1.515625 -7.843750q-1.515625 -3.734375 -4.515625 -5.984375q-3.000000 -2.250000 -7.250000 -2.250000q-4.343750 0.000000 -7.812500 2.625000q-3.468750 2.609375 -4.890625 6.750000q0.390625 -0.093750 1.078125 -0.093750q2.250000 0.000000 3.828125 1.515625q1.593750 1.515625 1.593750 3.906250q0.000000 2.296875 -1.593750 3.890625q-1.578125 1.578125 -3.828125 1.578125q-2.343750 0.000000 -3.937500 -1.625000q-1.578125 -1.640625 -1.578125 -3.843750q0.000000 -3.765625 1.406250 -7.046875q1.421875 -3.296875 4.078125 -5.859375q2.671875 -2.578125 6.015625 -3.937500q3.343750 -1.375000 7.093750 -1.375000q5.718750 0.000000 10.640625 2.421875q4.937500 2.421875 7.812500 6.843750q2.890625 4.406250 2.890625 10.328125q0.000000 4.343750 -1.906250 8.250000q-1.906250 3.906250 -4.890625 7.109375q-2.968750 3.187500 -7.609375 7.250000q-4.640625 4.046875 -6.093750 5.406250l-11.328125 10.890625l9.609375 0.000000q7.078125 0.000000 11.843750 -0.109375q4.765625 -0.125000 5.046875 -0.375000q1.171875 -1.265625 2.406250 -9.234375l2.921875 0.000000l-2.828125 17.828125z"/>
</defs>
<g id="mathtext5">
<g style="fill: #000000" transform="translate(199.665000,64.440000)">
<use xlink:href="#c_7834f07fc511277fc3d27d854f452306" transform="translate(0.000000,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_4af9599587a0091f79c2f694637ff61b" transform="translate(6.240234,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_7bbc93c01755cdeb977d08bdfb9ce616" transform="translate(15.355078,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_3260b495c6402fff66ed286585579e9c" transform="translate(25.430859,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_62db141412f5d9d8ddcda81385ac812d" transform="translate(32.655469,-3.000000)scale(0.120000)"/>
<use xlink:href="#c_1210e7f4d85518601ea3049211d562d0" transform="translate(38.655469,-3.000000)scale(0.120000)"/>
</g>
</g>
</g>
<g id="line2d13">
<path style="fill: none; stroke: #bfbf00; stroke-width: 2.000000; stroke-linejoin: round; stroke-linecap: square;  opacity: 1.000000"  d="M175.185000 70.200000L195.345000 70.200000"/>
</g>
<g id="line2d14">
</g>
<g id="text18">
<g id="mathtext6">
<g style="fill: #000000" transform="translate(199.665000,78.240000)">
<use xlink:href="#c_7834f07fc511277fc3d27d854f452306" transform="translate(0.000000,-3.671875)scale(0.120000)"/>
<use xlink:href="#c_4af9599587a0091f79c2f694637ff61b" transform="translate(6.240234,-3.671875)scale(0.120000)"/>
<use xlink:href="#c_7bbc93c01755cdeb977d08bdfb9ce616" transform="translate(15.355078,-3.671875)scale(0.120000)"/>
<use xlink:href="#c_3260b495c6402fff66ed286585579e9c" transform="translate(25.430859,-3.671875)scale(0.120000)"/>
</g>
</g>
</g>
</g>
</g>
</g>
</svg>


*   **Temperature Dependence of Fermi Energy**: The Fermi energy has a weak temperature dependence for typical metals. For temperatures well below the Fermi temperature ($T \ll T_f$), the Fermi energy slightly decreases with increasing temperature, given by:
    $$E_f(T) = E_{f0}\left[1 - \frac{\pi^2}{12}\left(\frac{k_B T}{E_{f0}}\right)^2\right]$$
    Where $E_{f0}$ is the Fermi energy at 0K. For normal operating temperatures, the term $(k_B T/E_{f0})^2$ is very small, so $E_f(T) \approx E_{f0}$. This implies that the Fermi level is largely independent of temperature for most purposes in metals.

#### **2.2.2 Concepts of Fermi Energy ($E_f$), Fermi Temperature ($T_f$), Fermi Velocity ($v_f$)**
*   **Fermi Energy ($E_f$)**: The highest occupied energy level by electrons in a material at absolute zero temperature (0 Kelvin). It represents the maximum kinetic energy an electron can have when all states below it are filled due to the Pauli Exclusion Principle. It defines the boundary between occupied and unoccupied electron states at 0K and is a measure of the typical kinetic energy of electrons in a metal.
*   **Fermi Temperature ($T_f$)**: Defined as $T_f = E_f/k_B$. It is a conceptual temperature, representing the temperature scale at which quantum effects become critical for the electron energy distribution. For most metals, $T_f$ is extremely high (e.g., $E_f \approx 7 \text{ eV}$ for copper gives $T_f \approx 81000 \text{ K}$). This indicates that thermal energy at room temperature ($300 \text{ K}$) is far too small to significantly affect the electron distribution around the Fermi level, which remains largely quantum-mechanical.
*   **Fermi Velocity ($v_f$)**: The velocity of an electron that possesses a kinetic energy exactly equal to the Fermi energy ($E_f$). It represents the maximum velocity an electron possesses at 0 Kelvin. It is calculated using the classical kinetic energy formula (though arising from quantum phenomena):
    $$E_f = \frac{1}{2}m v_f^2 \implies v_f = \sqrt{\frac{2E_f}{m}}$$
    For copper, $v_f \approx 1.6 \times 10^6 \text{ m/s}$, which is orders of magnitude higher than the classical thermal velocity ($~10^5 \text{ m/s}$). This substantial velocity at 0K is a direct consequence of the Pauli Exclusion Principle forcing electrons into high-energy states. These fast-moving electrons near the Fermi surface are primarily responsible for electrical and thermal conduction.
    > See also: [Examples](Examples.md#Example%203:%20Fermi%20Velocity%20Calculation)

### **2.3 Graphical Representations of g(E) and N(E) and Analysis**

To understand electron distribution and overall properties, we need the **density of states ($g(E)$)**, which is the number of available quantum states per unit energy interval per unit volume. The **total number of states ($N(E)$)** up to a given energy $E$ is also important. This is derived by considering electrons as particles confined in a "box," where energy levels are quantized, and then counting these states in wave vector (k) space.

#### **2.3.1 Density of States per Unit Volume ($g(E)$) for different dimensions**
*   **3D Case (Bulk Material - Volume V):**
    *   **Derivation Sketch**: Electrons are treated as particles in a 3D potential well (e.g., cubic box of side L). The allowed energy values are $E = \frac{\hbar^2 k^2}{2m}$, where $\mathbf{k} = \frac{\pi}{L}(n_x, n_y, n_z)$ with $n_x, n_y, n_z$ being positive integers. Each point in *k-space* represents a quantum state. Counting these states in a sphere (considering octant for positive integers) and accounting for spin degeneracy leads to $N(E) \propto E^{3/2}$. Differentiating $N(E)$ with respect to $E$ gives $g(E)$.
    *   **Expression**:
        $$g(E) = \frac{\pi}{2} \left(\frac{8m}{h^2}\right)^{3/2} E^{1/2}$$
    *   **Plot Description**: The plot of $g(E)$ versus energy $E$ for a 3D system starts at zero for $E=0$ and then increases parabolically as energy increases ($g(E) \propto E^{1/2}$). This monotonic increase indicates that more states become available per unit energy interval at higher energies.
    *   **Plot:**
        ![Density of States 3D](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cd/Density_of_states.svg/500px-Density_of_states.svg.png)
*   **2D Case (Quantum Well - Area A):**
    *   **Derivation Sketch**: Confinement in one dimension (e.g., width Lz) quantizes energy ($E_z \propto n_z^2$), while electrons are free to move in the other two dimensions (x, y). This leads to a series of 2D sub-bands. Within each sub-band, counting states in 2D k-space and differentiating reveals the DoS.
    *   **Expression**:
        $$g(E) = \frac{4\pi m}{h^2}$$
        For each sub-band, above its minimum energy.
    *   **Plot Description**: The plot of $g(E)$ versus energy $E$ for a 2D system shows a series of steps. Within each step, corresponding to a 2D sub-band (above a specific energy threshold for each quantized level), $g(E)$ is constant (independent of energy). The DoS jumps discontinuously when a new sub-band becomes available.
    *   **Plot:**
        ![Density of States 2D](https://www.tf.uni-kiel.de/matwis/ag_th/lectures/esm/esmfiles/image010.gif) *(Conceptual image for 2D DoS)*
*   **1D Case (Quantum Wire - Length L):**
    *   **Derivation Sketch**: Confinement in two dimensions (e.g., width Ly, Lz) quantizes energy ($E_y \propto n_y^2, E_z \propto n_z^2$), while electrons are free to move in only one dimension (x). This forms a series of 1D sub-bands. The DoS is then derived for these 1D components.
    *   **Expression**:
        $$g(E) = \frac{1}{h} \sqrt{\frac{2m}{E}}$$
        For each sub-band, above its minimum energy.
    *   **Plot Description**: The plot of $g(E)$ versus energy $E$ for a 1D system shows an inverse square root dependence, $g(E) \propto E^{-1/2}$. This means that the density of states is highest at low energies close to the bottom of each new 1D sub-band (where the curve spikes) and decreases sharply as energy increases within that sub-band.
    *   **Plot:**
        ![Density of States 1D](https://www.tf.uni-kiel.de/matwis/ag_th/lectures/esm/esmfiles/image009.gif) *(Conceptual image for 1D DoS)*

    > See also: [Examples](Examples.md#Example%204:%20Number%20of%20Electron%20States)

#### **2.3.2 Relation between Total Electron Concentration (n) and Fermi Energy (E_f)**
The total number of free electrons per unit volume ($n$) in a metal is found by integrating the density of states ($g(E)$) from $E=0$ up to $E_f$, given that at 0K, all states up to $E_f$ are completely filled and all states above $E_f$ are empty:
1.  **Fundamental Relation:**
    $$n = \int_0^{E_f} g(E) dE$$
2.  **Using 3D $g(E)$:** Substitute the expression for 3D $g(E)$ into the integral:
    $$n = \int_0^{E_f} \frac{\pi}{2} \left(\frac{8m}{h^2}\right)^{3/2} E^{1/2} dE$$
    $$n = \frac{\pi}{2} \left(\frac{8m}{h^2}\right)^{3/2} \left[ \frac{2}{3} E^{3/2} \right]_0^{E_f}$$
    $$n = \frac{\pi}{3} \left(\frac{8m}{h^2}\right)^{3/2} E_f^{3/2}$$
3.  **Solving for Fermi Energy ($E_f$):** Rearranging the equation to solve for $E_f$:
    $$E_f^{3/2} = n \frac{3}{\pi} \left(\frac{h^2}{8m}\right)^{3/2}$$
    Taking the $\frac{2}{3}$ power of both sides:
    $$E_f = \left(\frac{3n}{\pi}\right)^{2/3} \frac{h^2}{8m}$$
    This expression shows how the Fermi energy is directly related to the free electron concentration.

#### **2.3.3 Average Energy of Electrons at 0K**
The average energy of electrons in a metal at 0K (where all states up to $E_f$ are filled) is calculated by integrating $E \cdot g(E)$ up to $E_f$ and dividing by the total number of electrons $n$:
$$\langle E \rangle = \frac{\int_0^{E_f} E \cdot g(E) dE}{\int_0^{E_f} g(E) dE} = \frac{\int_0^{E_f} E \cdot g(E) dE}{n}$$
For a 3D system, this results in:
$$\langle E \rangle = \frac{3}{5} E_f$$
This indicates that the average kinetic energy of electrons in a metal at 0K is substantial, in stark contrast to the classical prediction of zero average kinetic energy at 0K.

#### **2.3.4 Relation of DoS to Nanomaterials' Special Properties**
The unique and often enhanced properties of nanomaterials (e.g., quantum dots, nanowires, thin films) arise directly from the modification of their electronic density of states due to **quantum confinement**.
*   **Quantum Confinement**: When the physical dimensions of a material (e.g., thickness, width, or length) become comparable to or smaller than the de Broglie wavelength of its electrons, the electron's motion in those confined dimensions becomes quantized. The continuous energy bands observed in bulk materials break down into discrete, atomic-like energy levels.
*   **Impact on DoS**: This dimensional restriction dramatically alters the shape of the density of states ($g(E)$):
    *   From a continuous $E^{1/2}$ dependence in 3D (bulk).
    *   To a step-like constant dependence in 2D (quantum wells/thin films).
    *   To sharp peaks ($E^{-1/2}$) in 1D (quantum wires/nanowires).
    *   To discrete delta functions in 0D (quantum dots/nanoparticles).
*   **Consequences for Nanomaterials**: These altered density of states profoundly affect:
    *   **Optical Properties**: Quantum dots exhibit size-dependent light absorption and emission (fluorescence), meaning their color can be tuned by changing their size. This is used in quantum dot displays and biosensors.
    *   **Electrical Properties**: Modified DoS influences electron mobility, conductivity, and thermoelectric properties, leading to materials suitable for advanced transistors or energy harvesting.
    *   **Chemical Reactivity**: The altered electronic structure can enhance catalytic activity and surface reactivity.

### **2.4 Merits of Quantum Free Electron Theory**

1.  **Correct Electronic Specific Heat ($C_{el}$)**:
    *   QFET correctly explains that only a small fraction of electrons (those within an energy range of a few $k_B T$ around the Fermi level) can be excited by thermal energy and thus contribute to specific heat. Electrons deep within the Fermi sea cannot absorb energy because there are no available empty states nearby due to the Pauli Exclusion Principle.
    *   The electronic specific heat per unit volume is predicted as:
        $$C_{el} = \frac{\pi^2}{2} n k_B \frac{k_B T}{E_f}$$
        For one mole, $C_{el} = \frac{\pi^2}{2} R \frac{k_B T}{E_f}$.
    *   This formula correctly predicts that $C_{el}$ is directly proportional to temperature ($C_{el} \propto T$) and is much smaller than the classical prediction (typically <1% at room temperature), resolving a major drawback of CFET.

2.  **Correct Temperature Dependence of Resistivity**:
    *   In QFET, the conduction electrons are those near the Fermi level, moving with high Fermi velocity ($v_f$), which is largely independent of temperature.
    *   Electron scattering primarily occurs due to lattice vibrations (phonons). The amplitude of these lattice vibrations increases with temperature, leading to a decrease in the mean free path ($\lambda \propto 1/T$) and thus relaxation time ($\tau \propto 1/T$). (For pure metals, $\lambda$ is limited primarily by phonons at high temperatures and by impurities at low temperatures).
    *   The conductivity is given by $\sigma = \frac{ne^2\tau}{m^*} = \frac{ne^2\lambda}{m^* v_f}$. Since $v_f$ is nearly constant and $\lambda \propto 1/T$, $\sigma \propto 1/T$, and thus resistivity $\rho \propto T$.
    *   This correctly explains the observed linear temperature dependence of resistivity in pure metals, successfully resolving another major drawback of CFET.

3.  **Wiedemann-Franz Law and Lorenz Number (L)**:
    *   The **Wiedemann-Franz law** states that for metals, the ratio of thermal conductivity ($K$) to electrical conductivity ($\sigma$) is directly proportional to the absolute temperature $T$. The constant of proportionality is the **Lorenz Number ($L$)**.
    *   Both electrical and thermal conduction in metals are predominantly due to the same population of electrons near the Fermi level.
    *   **Derivation of Thermal Conductivity (QFET)**:
        Thermal conductivity $K$ is derived from adapting classical kinetic theory using QFET parameters:
        $K = \frac{1}{3} C_v \langle v \rangle \lambda$.
        Substituting $C_v = \frac{\pi^2}{2} n k_B \frac{k_B T}{E_f}$, $\langle v \rangle = v_f$, and $\lambda = v_f \tau$ leads to:
        $$K = \frac{\pi^2 n k_B^2 T \tau}{3 m^*}$$
    *   **Derivation of Lorenz Number ($L$)**:
        Electrical conductivity is $\sigma = \frac{ne^2\tau}{m^*}$. Divide $K$ by $\sigma T$:
        $$L = \frac{K}{\sigma T} = \frac{\frac{\pi^2 n k_B^2 T \tau}{3 m^*}}{\left(\frac{ne^2\tau}{m^*}\right) T} = \frac{\pi^2 k_B^2}{3 e^2}$$
    *   **Significance**: This formula correctly predicts that $L$ is a constant, independent of the specific metal and temperature ($L \approx 2.44 \times 10^{-8} \text{ W}\Omega\text{ K}^{-2}$), which closely matches experimental data. This provides strong quantitative proof that both charge and heat transport in metals are primarily mediated by the same free electrons.

### **2.5 Demerits of Quantum Free Electron Theory**
While QFET significantly improved explanations for many metallic properties, it still has fundamental limitations:
*   **Inadequacy to account for Band Structure**: It completely neglects the periodic potential created by the positive ion cores in the crystal lattice. This periodic potential is crucial for explaining the very existence of allowed energy bands and forbidden band gaps.
*   **Cannot Differentiate Materials**: Since it assumes all electrons are "free" within a potential well, it cannot fundamentally explain why some materials are insulators, some are semiconductors, and others are conductors, solely based on electron concentration.
*   **Positive Hall Coefficient**: While an improvement, QFET (in its basic form) still primarily considers negative electron charge carriers and thus struggles to fully explain the *positive* Hall coefficient observed in certain metals (e.g., zinc, cadmium, bismuth), which is a clear indication of hole conduction.
*   **Assumes Bare Electron Mass**: It typically assumes that electrons move with their free space mass ($m_e$). However, in a crystalline environment, electrons effectively behave with an effective mass ($m^*$) that can differ greatly from $m_e$ and can even be negative or anisotropic.

---

## 3. Band Theory of Solids

To fully overcome QFET's shortcomings and provide a complete quantum mechanical description of electron behavior in crystalline solids, we must consider the periodic potential created by the arrangement of atoms in the lattice. This leads to the **Band Theory of Solids**.

### **3.1 Motion of Electron in Periodic Potential (One-Dimensional Treatment)**

#### **3.1.1 Bloch Theorem and Electron Wave Functions in a Periodic Potential**
The **Bloch Theorem** is a fundamental theorem that describes the behavior of electrons in a perfectly periodic potential, such as that found in a crystal lattice ($V(\mathbf{r}) = V(\mathbf{r} + \mathbf{R})$, where $\mathbf{R}$ is a lattice vector).
*   **Statement**: The wave function solution ($\psi_k(\mathbf{r})$) for an electron in a periodic potential can be written as a product of a plane wave ($e^{i\mathbf{k}\cdot\mathbf{r}}$) and a periodic function ($u_k(\mathbf{r})$) that has the same periodicity as the crystal lattice.
    $$\psi_k(\mathbf{r}) = e^{i\mathbf{k}\cdot\mathbf{r}} u_k(\mathbf{r})$$
    This wave function is called a **Bloch function**.
*   **Form of Bloch Functions**: A Bloch function is a modulated plane wave. The $e^{i\mathbf{k}\cdot\mathbf{r}}$ part describes the propagating nature of the electron wave, similar to a free electron with wave vector $\mathbf{k}$. The $u_k(\mathbf{r})$ part is a periodic function that takes into account the underlying crystal periodicity and the interaction of the electron with the atomic potential. It adjusts the plane wave to reflect the electron's "view" of the lattice.
*   **Physical Significance / Underpinning Electron Wavefunctions**:
    1.  **Free Propagation**: It implies that electrons can propagate freely through a perfect crystal lattice without scattering, even in the presence of strong atomic potentials. This explains the extremely high electrical conductivities and long mean free paths observed in pure metals.
    2.  **Wave-like Nature**: It highlights the wave-like nature of electrons within a crystal, with their properties determined by the wave vector $\mathbf{k}$ and the nature of the periodic function $u_k(\mathbf{r})$.
    3.  **Foundation for Band Structure**: This theorem is the rigorous mathematical basis for the existence of energy bands and gaps in solids.

#### **3.1.2 Kronig-Penney Model and Band Structure Emergence**
The **Kronig-Penney Model** is a simplified, one-dimensional mathematical model used to illustrate how energy bands and forbidden gaps arise when an electron moves in a periodic potential. It provides a qualitative understanding without the complexity of a real 3D crystal.
*   **Model Potential Profile**: The model approximates the complex, continuous periodic potential of a crystal into an idealized, simpler form: an infinite series of rectangular potential wells (representing the attractive potential of atomic nuclei) separated by rectangular potential barriers (representing the repulsive potential between them).
    **Description of Potential Profile:** The Kronig-Penney model approximates the periodic potential of a crystal as a series of rectangular potential wells (regions of lower potential energy, representing electron attraction to atomic nuclei) separated by rectangular potential barriers (regions of higher potential energy, representing the regions between nuclei). The width of the wells (`a`) and barriers (`b` or `c`), along with the height of the barriers (`V0`), are key parameters in the model. The overall periodicity is `a+c`.
    ![Kronig-Penney Model Potential Profile](https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Kronig-Penney_potential.svg/langja-480px-Kronig-Penney_potential.svg.png)
*   **Mathematical Result & Graphical Solution**: Applying the Schrödinger equation and Bloch's theorem to this periodic potential leads to a transcendental equation that relates the electron's energy $E$ to its wave vector $k$:
    $$\cos(ka) = P \frac{\sin(\alpha a)}{\alpha a} + \cos(\alpha a)$$
    Where $P = \frac{m a V_0 c}{\hbar^2}$ (a measure of barrier strength, often simplified) and $\alpha = \sqrt{2mE/\hbar^2}$.
*   **Emergence of Band Structure / Origin of Band Gaps**:
    1.  **Restriction on `k` values**: The left-hand side of the equation, $\cos(ka)$, is restricted to values between -1 and +1. Therefore, for a real solution for $k$ to exist, the right-hand side of the equation must also fall within this range.
    2.  **Allowed and Forbidden Energy Ranges**:
        *   For certain ranges of electron energies $E$, the right-hand side falls *within* the range [-1, +1]. These are the **allowed energy bands**, where electrons can propagate freely through the crystal.
        *   For other ranges of electron energies $E$, the right-hand side falls *outside* the range [-1, +1]. In this scenario, there is no real solution for $k$, meaning electrons with these energies cannot propagate through the crystal. These are the **forbidden energy bands (band gaps)**, where stable electron states cannot exist.
    3.  **Periodicity in k-space**: The $E-k$ relation (energy as a function of wave vector) is periodic in $k$-space, with the periodicity of the reciprocal lattice ($2\pi/a$).
    4.  **Discontinuities at Zone Boundaries**: The most striking feature of the E-k diagram is that at specific values of $k$ (the **Brillouin zone boundaries**, e.g., $k = \pm n\pi/a$), there are abrupt discontinuities in the energy. These discontinuities are precisely the energy gaps where electrons cannot exist. The energy value jumps from the top of one allowed band to the bottom of the next.
    *   **Origin of Energy Bands**: Conceptually, as isolated atoms come together to form a solid, their sharp, discrete atomic energy levels overlap and interact. The periodic potential of the crystal, combined with the Pauli Exclusion Principle, forces these discrete levels to broaden into continuous ranges of allowed energy, known as **energy bands**, separated by energy gaps.
*   **E-k Diagram (Energy-Wave Vector Diagram)**: The graph of energy ($E$) as a function of the wave vector ($k$) for a periodic potential, illustrating the allowed energy bands and forbidden band gaps.
    **Description of E-k Diagram:** A diagram would show the electron energy $E$ plotted against the wave vector $k$. In the free electron model (dashed parabola), $E$ is continuous and proportional to $k^2$. However, for the Kronig-Penney model (or any periodic potential, solid curves), the $E-k$ relation is periodic but exhibits discontinuities (gaps) at specific values of $k = \pm n\pi/a$. These are the boundaries of the Brillouin zones. The continuous segments within these regions are the allowed energy bands, and the vertical breaks represent the forbidden energy bands (band gaps).
    ![E-k Diagram for Periodic Potential vs Free Electron (Band Structure)](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/Kronig_penney.png/600px-Kronig_penney.png)

### **3.2 Brillouin Zones and E-k Diagrams**

#### **3.2.1 Brillouin Zones**
*   **Definition**: Brillouin zones are fundamental regions in **reciprocal space** (k-space), which is the Fourier transform space of the real crystal lattice. They are used to describe the allowed wave vectors ($k$) and corresponding energies ($E$) of electrons in a periodic crystal lattice. The **first Brillouin zone** is the smallest primitive cell in reciprocal space, centered at $k=0$. Higher Brillouin zones are larger regions constructed around this.
*   **Construction**: Brillouin zones are constructed by taking the reciprocal lattice and drawing perpendicular bisectors to the reciprocal lattice vectors from a chosen origin. The smallest volume enclosed by these bisectors forms the first Brillouin zone.
*   **Significance**:
    1.  **Periodicity in E-k Diagram**: The electron's energy-wave vector ($E-k$) relation in a crystal is inherently periodic in k-space, with the periodicity of the reciprocal lattice. Therefore, all unique information about the electron's energy and quantum states can be fully described within a single Brillouin zone, typically re-mapped to the first Brillouin zone (the "reduced zone scheme"), simplifying analysis.
    2.  **Origin of Energy Gaps**: The boundaries of the Brillouin zones (e.g., $k = \pm n\pi/a$ in 1D) are points in k-space where electron waves undergo Bragg reflection from the periodic crystal lattice. This strong reflection leads to the formation of standing waves and abrupt discontinuities in the $E-k$ dispersion curves, which manifest as **forbidden energy bands (band gaps)**. These gaps are crucial for determining a material's electrical properties.
    3.  **Electron Dynamics**: The way Brillouin zones are filled with electrons directly dictates the electrical properties of the material. A completely filled zone, separated from empty zones by a band gap, indicates an insulator. A partially filled zone, or overlapping zones, indicates a conductor.
    4.  **Crystal Momentum**: The wave vector $\mathbf{k}$ in a Bloch function is often referred to as the crystal momentum. The Brillouin zone defines the range of physically distinct crystal momentum states that an electron can occupy within the periodic potential.

#### **3.2.2 E-k Diagrams (Energy-Wave Vector Diagrams)**
*   **Definition**: An E-k diagram plots the energy ($E$) of an electron as a function of its wave vector ($k$) within the Brillouin zone. It is the most comprehensive way to visualize the band structure of a solid.
*   **Information Conveyed**:
    *   **Allowed Bands**: Regions where E(k) curves exist represent allowed energy bands.
    *   **Band Gaps**: Vertical gaps between these curves represent forbidden energy ranges.
    *   **Curvature**: The curvature of the E-k curves determines the effective mass of the electrons.
    *   **Location of Band Edges**: Minima and maxima of the bands are important, especially for semiconductors.

### **3.3 Classification of Materials Based on Band Theory**

The band theory provides a clear and powerful quantum mechanical explanation for the differences in electrical properties among various materials:

*   **Conductors (Metals)**:
    *   **Band Structure**: In conductors, the highest occupied energy band (valence band) is either **partially filled** with electrons, or the valence band **overlaps** with the next higher empty band (conduction band).
    *   **Fermi Level ($E_f$)**: The Fermi level (the highest occupied energy at 0K) lies within an allowed energy band.
    *   **Electrical Properties**: Because there are abundant empty energy states immediately adjacent to the occupied states, electrons require very little energy to move and accelerate. Even a infinitesimally small electric field can promote electrons to higher energy states within the same band. This allows for easy acceleration and leads to very high electrical conductivity.
*   **Semiconductors**:
    *   **Band Structure**: Semiconducting materials have a completely filled valence band and a completely empty conduction band (at 0K), separated by a **small energy gap ($E_g$)**. This gap is typically on the order of 0.5 eV to 2 eV (e.g., Silicon $E_g \approx 1.1 \text{ eV}$, Germanium $E_g \approx 0.7 \text{ eV}$).
    *   **Fermi Level ($E_f$)**: The Fermi level typically lies within the band gap.
    *   **Electrical Properties**: At absolute zero temperature (0K), semiconductors behave as perfect insulators because the valence band is full and electrons cannot move, and the conduction band is empty. However, at finite (room) temperatures, thermal energy ($k_B T$) is sufficient to excite a small number of electrons across the small band gap from the valence band into the conduction band. This leaves behind vacant states (known as **holes**) in the valence band. Both the electrons in the conduction band and the holes in the valence band become mobile charge carriers, leading to moderate electrical conductivity. The conductivity increases significantly with increasing temperature.
*   **Insulators**:
    *   **Band Structure**: Insulating materials have a completely filled valence band and a completely empty conduction band, separated by a **large energy gap ($E_g$)**. This gap is typically much greater than 5 eV (e.g., Diamond $E_g \approx 5.5 \text{ eV}$, SiO$_2 \approx 9 \text{ eV}$).
    *   **Fermi Level ($E_f$)**: The Fermi level lies within the large band gap.
    *   **Electrical Properties**: Due to the very large energy gap, even at high temperatures, thermal energy is insufficient to excite a significant number of electrons from the valence band to the conduction band. With no empty states in the valence band for electrons to move into, and virtually no electrons in the conduction band, electrons are tightly bound and cannot move freely. This results in extremely low electrical conductivity, classifying them as insulators.

### **3.4 Effective Mass of Charge Carriers ($m^*$) in a Periodic Potential**

*   **Concept**: When an electron moves through the periodic potential of a crystal lattice, its motion is influenced by the forces from the lattice atoms. This interaction makes the electron respond to external forces as if it had a mass different from its free rest mass ($m_e$). This modified inertial mass is called the **effective mass ($m^*$)**. It accounts for the dynamic effect of the lattice potential on the electron's motion.
*   **Derivation (Relation to E-k curvature using Group Velocity)**:
    1.  **Group Velocity ($v_g$)**: For an electron wave packet (Bloch wave) in an energy band, its velocity is the group velocity ($v_g$), which is related to the energy-wave vector ($E-k$) dispersion relation by:
        $$v_g = \frac{1}{\hbar} \frac{dE}{dk}$$
    2.  **Force and Wave Vector Change**: When an external force $F$ acts on the electron, it changes the electron's crystal momentum ($\hbar k$). According to quantum mechanics:
        $$F = \frac{d(\hbar k)}{dt} = \hbar \frac{dk}{dt}$$
    3.  **Acceleration ($a$)**: The acceleration of the electron is the time derivative of its group velocity:
        $$a = \frac{dv_g}{dt} = \frac{d}{dt} \left( \frac{1}{\hbar} \frac{dE}{dk} \right)$$
        Applying the chain rule, $\frac{d}{dt} = \frac{dk}{dt} \frac{d}{dk}$:
        $$a = \frac{1}{\hbar} \frac{d^2E}{dk^2} \frac{dk}{dt}$$
    4.  **Substituting for dk/dt**: Substitute the expression for $\frac{dk}{dt}$ from step 2:
        $$a = \frac{1}{\hbar} \frac{d^2E}{dk^2} \left(\frac{F}{\hbar}\right) = \frac{1}{\hbar^2} \frac{d^2E}{dk^2} F$$
    5.  **Newton's Second Law with Effective Mass**: By definition, for an effective mass $m^*$, the acceleration is related to the force by $F = m^* a$, so $a = F/m^*$.
    6.  **Equating Expressions**: Comparing the two expressions for acceleration:
        $$\frac{F}{m^*} = \frac{1}{\hbar^2} \frac{d^2E}{dk^2} F$$
        Therefore, the effective mass $m^*$ is given by:
        $$m^* = \frac{\hbar^2}{\frac{d^2E}{dk^2}}$$
    This elegant derivation shows that the effective mass is inversely proportional to the **second derivative (curvature) of the $E-k$ dispersion relation**.

*   **Physical Interpretation**:
    *   **Magnitude**:
        *   A high curvature (a large positive value of $d^2E/dk^2$) means a small effective mass. Such carriers are easily accelerated by external fields, leading to high mobility.
        *   A low curvature (a small positive value of $d^2E/dk^2$) means a large effective mass. Such carriers are "sluggish" and have low mobility.
    *   **Sign (Holes)**:
        *   In the conduction band, near its minimum (where electrons reside), the curvature $d^2E/dk^2$ is typically positive, leading to a positive effective mass for electrons.
        *   Near the top of the valence band (where electron energies are at a maximum), the curvature $d^2E/dk^2$ is negative. This would imply a negative effective mass for electrons. Physically, this is interpreted as the motion of a positively charged quasiparticle, a **hole**, with a positive effective mass.
*   **Significance**: The effective mass is a crucial parameter in all charge transport phenomena, dictating carrier mobility, contributing to density of states, and enabling the explanation of the positive Hall coefficient by accounting for hole conduction. It is fundamental to modeling semiconductor devices and metallic transport.

---

## 4. Hall Effect

The **Hall Effect** is the production of a voltage difference (the Hall voltage, $V_H$) across an electrical conductor, transverse to both an electric current ($I$) flowing through the conductor and a magnetic field ($\vec{B}$) applied perpendicular to the current. This effect is a powerful tool for characterizing charge carriers in materials.

### **4.1 Experimental Setup and Principle**
*   **Setup**: Consider a rectangular slab of a conductor or semiconductor of thickness $t$ and width $w$.
*   **Current Application**: An electric current $I$ is passed along the length of the sample (e.g., X-direction), typically by applying an electric field $E_x$. This current consists of charge carriers (electrons or holes) moving with an average drift velocity $v_d$.
*   **Magnetic Field Application**: A uniform magnetic field $B_z$ is applied perpendicular to both the current and the width of the sample (e.g., Z-direction).
*   **Lorentz Force**: As the charge carriers ($q$) move with drift velocity $v_d$ in the magnetic field $B_z$, they experience a Lorentz force ($F_L = q v_d B_z$) which deflects them towards one side of the sample (e.g., along the Y-direction).
*   **Charge Accumulation & Hall Field**: This deflection causes an accumulation of charge on opposite sides of the sample along the Y-axis. This charge separation creates an internal **Hall electric field ($E_H$ or $E_y$)** in the transverse direction (Y-direction).
*   **Equilibrium**: The Hall electric field exerts an opposing electrostatic force ($F_H = q E_H$) on the charge carriers. In a steady state, this electrostatic force balances the deflecting Lorentz force, causing the carriers to travel straight along the X-direction without further deflection.
*   **Hall Voltage**: The voltage measured across the width ($w$) of the sample, due to the Hall electric field, is the **Hall voltage ($V_H$)**.

**Schematic Diagram of Hall Effect:**
**Description of Diagram:** A rectangular block of conducting material is shown. Current ($I$) flows along the length (e.g., X-axis). A magnetic field ($B$) is applied perpendicular to the current (e.g., Z-axis). This causes charge carriers to deflect due to the Lorentz force, resulting in a buildup of charge on opposite sides of the sample. This charge separation creates a transverse Hall electric field ($E_H$) and a measurable Hall voltage ($V_H$) across the width (Y-axis). Arrows indicate the directions of current, magnetic field, Lorentz force, and the resulting Hall electric field.
![Hall effect schematic diagram](https://upload.wikimedia.org/wikipedia/commons/e/ec/Hall_effect_schematic.png)

### **4.2 Derivation of Hall Voltage and Hall Coefficient ($R_H$)**
Let's consider charge carriers of charge $q$ and density $n$.

1.  **Lorentz Force**: The force exerted by the magnetic field $B_z$ on a charge carrier moving with drift velocity $v_d$ (in x-direction) is the Lorentz force:
    $$F_L = q v_d B_z$$
    The direction of this force is perpendicular to both $v_d$ and $B_z$.

2.  **Hall Field Force**: The generated Hall electric field $E_H$ (or $E_y$) in the y-direction exerts a force on the charge carriers:
    $$F_H = q E_H$$

3.  **Equilibrium Condition**: In a steady state, the Lorentz force is balanced by the Hall field force:
    $$q v_d B_z = q E_H$$
    $$E_H = v_d B_z \quad (1)$$

4.  **Current Density ($J_x$)**: The current density in the x-direction is related to the carrier density and drift velocity:
    $$J_x = n q v_d$$
    From this, the drift velocity can be expressed as:
    $$v_d = \frac{J_x}{n q} \quad (2)$$

5.  **Hall Field in terms of Current Density and Magnetic Field**: Substitute equation (2) into equation (1):
    $$E_H = \frac{J_x B_z}{n q}$$

6.  **Hall Coefficient ($R_H$)**: The Hall coefficient is a material parameter defined as the ratio of the induced Hall electric field ($E_H$) to the product of the current density ($J_x$) and the magnetic field ($B_z$):
    $$R_H = \frac{E_H}{J_x B_z} = \frac{1}{n q}$$
    *   **For electrons**: If the charge carriers are electrons ($q = -e$), then $R_H = -\frac{1}{ne}$. The Hall voltage will be negative.
    *   **For holes**: If the charge carriers are holes ($q = +e$), then $R_H = +\frac{1}{ne}$. The Hall voltage will be positive.

7.  **Hall Voltage ($V_H$)**: The Hall voltage is the potential difference measured across the width ($w$) of the sample:
    $$V_H = E_H w = \frac{J_x B_z w}{n q}$$
    Since the current $I = J_x \cdot w \cdot t$ (where $t$ is the thickness of the sample), we have $J_x = \frac{I}{wt}$. Substituting this:
    $$V_H = \frac{I B_z w}{(wt) n q} = \frac{I B_z}{n q t} = R_H \frac{I B_z}{t}$$

### **4.3 Applications of Hall Effect**
The Hall effect is a versatile tool in condensed matter physics and technology:
1.  **Determination of Carrier Type**: The most significant application. The sign of the Hall voltage (and thus the Hall coefficient $R_H$) directly indicates whether the majority charge carriers in the material are electrons (negative $R_H$) or holes (positive $R_H$). This resolved a major shortcoming of CFET.
2.  **Determination of Carrier Concentration ($n$)**: Once $R_H$ is measured, the carrier concentration can be precisely calculated from $n = 1/(|R_H|q)$, where $q$ is the elementary charge ($e$).
3.  **Measurement of Magnetic Fields**: Hall effect sensors (Hall probes) are widely used to measure magnetic field strengths, as $V_H$ is directly proportional to $B_z$.
4.  **Determination of Carrier Mobility ($\mu$)**: Knowing both the electrical conductivity ($\sigma = n q \mu$) and the carrier concentration ($n$), the carrier mobility can be calculated: $\mu = \sigma |R_H|$.
5.  **Non-Contact Current Measurement**: Used in clamp-on ammeters.
6.  **Position, Speed, and Proximity Sensors**: Widely used in automotive (e.g., ABS, crankshaft sensors) and industrial applications.

### **4.4 Quantum Hall Effect (QHE)**

The **Quantum Hall Effect (QHE)** is a remarkable quantum mechanical phenomenon observed in **two-dimensional electron systems (2DES)** (e.g., inversion layers in MOSFETs, quantum wells) when subjected to strong magnetic fields and extremely low temperatures.

*   **Key Features**:
    1.  **Quantized Hall Resistance**: The Hall resistance ($R_H = V_H/I$) is found to be precisely quantized in integer multiples of a fundamental constant:
        $$R_H = \frac{h}{e^2} \frac{1}{\nu}$$
        Where $h$ is Planck's constant, $e$ is the elementary charge, and $\nu$ is an integer (for the Integer Quantum Hall Effect, IQHE) or a simple fraction with an odd denominator (for the Fractional Quantum Hall Effect, FQHE). The fundamental unit of quantized resistance, $R_K = h/e^2 \approx 25812.807 \Omega$, is known as the **von Klitzing constant**.
    2.  **Zero Longitudinal Resistance**: Simultaneously, the longitudinal resistance ($R_x$) (resistance along the current direction) drops to zero exactly at the plateaus where the Hall resistance is quantized.
    3.  **Tremendous Precision and Robustness**: The quantization is extremely accurate (parts per billion) and surprisingly insensitive to material properties, impurities, or the geometry of the sample.

*   **Significance**:
    1.  **Fundamental Constant Determination**: The QHE provides an extraordinarily precise method for determining fundamental physical constants, particularly the ratio $h/e^2$. The von Klitzing constant is now the primary standard for electrical resistance worldwide.
    2.  **New State of Matter**: The FQHE led to the revolutionary discovery of a new type of quantum fluid with elementary excitations that carry fractional elementary charge (known as **anyons**).
    3.  **Topological Physics**: The QHE is a prime experimental example and a cornerstone for the development of modern **topological physics** in condensed matter. The quantization is a topological invariant, meaning it is robust against local perturbations and related to deep mathematical properties of the quantum states. It has spurred research into topological insulators and superconductors.
    4.  **Basis for Metrology**: The QHE is utilized as a quantum standard for resistance measurements.

---

## 5. Magnetic Materials (Quantum Treatment)

Materials respond to external magnetic fields in various ways due to the quantum mechanical properties of their constituent atoms, particularly electrons and their spins.

### **5.1 Introduction to Magnetic Materials**
*   **Magnetic Field Strength ($\mathbf{H}$)**: The measure of an external magnetizing field. Unit: Amperes per meter (A/m). For a long solenoid with $n$ turns per unit length carrying current $I$, $H = nI$.
*   **Magnetization ($\mathbf{M}$)**: The magnetic dipole moment per unit volume induced in a material when placed in an external magnetic field. It represents the degree to which a material is magnetized. Unit: A/m or Weber per square meter (Wb/m²).
*   **Magnetic Flux Density ($\mathbf{B}$)**: The total magnetic field within a material. It includes both the applied external field and the field produced by the material's own magnetization.
    $$\mathbf{B} = \mu_0 (\mathbf{H} + \mathbf{M})$$
    Where $\mu_0$ is the permeability of free space ($4\pi \times 10^{-7} \text{ H/m}$). Unit: Tesla (T) or Wb/m².
*   **Magnetic Susceptibility ($\chi_m$)**: A dimensionless quantity indicating how much a material is magnetized in response to an applied magnetic field. It quantifies the ease with which a material can be magnetized.
    $$\chi_m = M/H$$
*   **Relative Permeability ($\mu_r$)**: Relates the total magnetic flux density to the applied magnetizing field. It is a measure of the degree of magnetization of a material in response to an internal field.
    $$\mu_r = 1 + \chi_m$$
    The **permeability of the material** is $\mu = \mu_0 \mu_r$.
*   **Classification of Magnetic Materials**: Materials are classified based on their $\chi_m$ value and characteristic behavior in a magnetic field.
    **Description of B-H Curves:** This diagram typically shows plots of magnetic flux density (B) against magnetic field strength (H) for different types of magnetic materials. Diamagnetic materials would show a very slight negative slope, indicating weak opposition to the field. Paramagnetic materials would show a very slight positive, but linear, slope, indicating weak alignment with the field. Ferromagnetic materials exhibit a highly non-linear curve with a distinctive hysteresis loop, indicating saturation, remanence, and coercivity, due to strong, permanent magnetic effects.
    ![Typical B-H curves for magnetic materials](https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/B-H_Curve.svg/1024px-B-H_Curve.svg.png)

### **5.2 Basic Electromagnetism Concepts Relevant to Magnetism**

#### **5.2.1 Maxwell's Equations involving Magnetic Field**
Maxwell's equations are a set of four fundamental partial differential equations that describe how electric and magnetic fields are generated by charges and currents, and how they interact with each other. Two of these equations specifically involve magnetic fields:

1.  **Gauss's Law for Magnetism:**
    $$\nabla \cdot \mathbf{B} = 0$$
    *   **Explanation**: This equation states that the divergence of the magnetic flux density ($\mathbf{B}$) is always zero. Physically, this means that magnetic field lines are always continuous closed loops; they have no starting points or ending points. Put another way, it implies that **magnetic monopoles (isolated North or South poles) do not exist** in classical electromagnetism. Magnetic fields are always associated with dipoles or higher-order multipoles, not individual charges.

2.  **Ampère-Maxwell Law (Maxwell's Modification of Ampère's Law):**
    $$\nabla \times \mathbf{H} = \mathbf{J} + \frac{\partial \mathbf{D}}{\partial t}$$
    *   **Explanation**: This law describes the fundamental sources of a magnetic field. It states that the curl (circulation) of the magnetic field intensity ($\mathbf{H}$) is produced by two components:
        *   **Conduction Current Density ($\mathbf{J}$):** This represents the conventional electric current flowing through conductors (e.g., current in a wire), as described by Ampère's original law.
        *   **Displacement Current Density ($\frac{\partial \mathbf{D}}{\partial t}$):** This is Maxwell's crucial addition. It represents a magnetic field generated by a time-varying electric displacement field ($\mathbf{D}$). This means that a changing electric field effectively acts as a source of magnetism, even in the absence of moving charges. This term was vital for completing the theory of electromagnetism and led to the prediction and understanding of electromagnetic waves.

#### **5.2.2 Solenoid Resembling a Bar Magnet**
A **solenoid** is a coil of wire (usually cylindrical) wound in a tightly packed helix. When an electric current flows through the turns of the wire, it creates a magnetic field.
*   **Field Inside the Solenoid**: For an ideal, long solenoid, the magnetic field lines inside the coil are uniform, parallel to the axis of the solenoid, and strong.
*   **Field Outside the Solenoid**: Outside the solenoid, the magnetic field lines emerge from one end of the coil, loop through the surrounding space, and re-enter the other end.
*   **Resemblance to a Bar Magnet**: The pattern of magnetic field lines produced by a current-carrying solenoid is virtually identical to the field lines produced by a permanent bar magnet. One end of the solenoid acts as a magnetic **North pole** (where field lines effectively emerge), and the other end acts as a magnetic **South pole** (where field lines effectively enter). The direction of the poles can be determined by the right-hand rule.
    **Description of Diagram:** This diagram shows a cylindrical solenoid with current flowing through its turns. Magnetic field lines are depicted inside and outside the solenoid. Inside, they are straight and parallel. Outside, they emerge from one end (labeled North pole), loop around, and enter the other end (labeled South pole), mirroring the classic field pattern of a bar magnet. This illustrates how electromagnetic fields can replicate static magnetic fields of permanent magnets.
    <?xml version='1.0' encoding='utf-8'?>
<svg xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg" version="1.1" baseProfile="full" width="800" height="600">
  <title>VFPt_cylindrical_coil_real</title>
  <desc>VFPt_cylindrical_coil_real
created with VectorFieldPlot 1.1
http://commons.wikimedia.org/wiki/User:Geek3/VectorFieldPlot

about: http://commons.wikimedia.org/wiki/File:VFPt_cylindrical_coil_real.svg
rights: GNU Free Documentation license,
        Creative Commons Attribution ShareAlike license
  </desc>
  <defs>
    <radialGradient id="white_spot" cx="0.65" cy="0.7" r="0.75">
      <stop stop-color="#ffffff" offset="0" stop-opacity="0.7"/>
      <stop stop-color="#ffffff" offset="0.1" stop-opacity="0.5"/>
      <stop stop-color="#ffffff" offset="0.6" stop-opacity="0"/>
      <stop stop-color="#000000" offset="0.6" stop-opacity="0"/>
      <stop stop-color="#000000" offset="0.75" stop-opacity="0.05"/>
      <stop stop-color="#000000" offset="0.85" stop-opacity="0.15"/>
      <stop stop-color="#000000" offset="1" stop-opacity="0.5"/>
    </radialGradient>
    <path id="arrow1" stroke="none" fill="#000000" transform="scale(0.01)" d="M 0.3,0 L -2.2,2.25 L 3.8,0 L -2.2,-2.25 L 0.3,0 Z"/>
  </defs>
  <rect id="background" x="0" y="0" width="800" height="600" fill="#ffffff"/>
  <g id="image" transform="translate(400.0,300.0) scale(100.0,-100.0)">
    <g id="fieldlines" fill="none" stroke="#000000" stroke-width="0.02" stroke-linejoin="round" stroke-linecap="round">
      <g id="fieldline1">
        <path d="M 0.0000,-0.7839 L 0.0151,-0.7827 L 0.0304,-0.7788 L 0.0462,-0.7720 L 0.0630,-0.7620 L 0.0813,-0.7477 L 0.1039,-0.7264 L 0.1524,-0.6763 L 0.1745,-0.6565 L 0.1943,-0.6419 L 0.2132,-0.6309 L 0.2319,-0.6229 L 0.2505,-0.6177 L 0.2690,-0.6150 L 0.2875,-0.6149 L 0.3060,-0.6173 L 0.3243,-0.6222 L 0.3426,-0.6298 L 0.3609,-0.6403 L 0.3795,-0.6539 L 0.3989,-0.6715 L 0.4209,-0.6953 L 0.4761,-0.7627 L 0.4973,-0.7853 L 0.5152,-0.8011 L 0.5313,-0.8123 L 0.5462,-0.8198 L 0.5600,-0.8241 L 0.5731,-0.8257 L 0.5857,-0.8247 L 0.5983,-0.8211 L 0.6110,-0.8147 L 0.6244,-0.8049 L 0.6392,-0.7907 L 0.6576,-0.7684 L 0.6958,-0.7154 L 0.7174,-0.6879 L 0.7356,-0.6683 L 0.7530,-0.6531 L 0.7702,-0.6413 L 0.7874,-0.6324 L 0.8047,-0.6262 L 0.8221,-0.6227 L 0.8393,-0.6217 L 0.8564,-0.6233 L 0.8732,-0.6274 L 0.8895,-0.6339 L 0.9052,-0.6430 L 0.9201,-0.6546 L 0.9340,-0.6687 L 0.9467,-0.6852 L 0.9580,-0.7041 L 0.9674,-0.7250 L 0.9746,-0.7472 L 0.9794,-0.7699 L 0.9816,-0.7924 L 0.9812,-0.8143 L 0.9784,-0.8354 L 0.9731,-0.8556 L 0.9654,-0.8752 L 0.9553,-0.8941 L 0.9426,-0.9122 L 0.9274,-0.9294 L 0.9098,-0.9456 L 0.8897,-0.9604 L 0.8673,-0.9738 L 0.8427,-0.9855 L 0.8156,-0.9955 L 0.7855,-1.0038 L 0.7508,-1.0105 L 0.6860,-1.0190 L 0.6512,-1.0246 L 0.6249,-1.0312 L 0.5999,-1.0401 L 0.5716,-1.0531 L 0.5234,-1.0794 L 0.4688,-1.1091 L 0.4276,-1.1288 L 0.3887,-1.1447 L 0.3498,-1.1579 L 0.3101,-1.1687 L 0.2687,-1.1772 L 0.2247,-1.1837 L 0.1761,-1.1882 L 0.1176,-1.1907 L 0.0061,-1.1914 L -0.1120,-1.1908 L -0.1721,-1.1884 L -0.2213,-1.1841 L -0.2655,-1.1778 L -0.3070,-1.1694 L -0.3468,-1.1588 L -0.3858,-1.1458 L -0.4248,-1.1300 L -0.4656,-1.1107 L -0.5179,-1.0825 L -0.5689,-1.0545 L -0.5979,-1.0409 L -0.6231,-1.0317 L -0.6493,-1.0250 L -0.6833,-1.0193 L -0.7496,-1.0107 L -0.7845,-1.0040 L -0.8146,-0.9958 L -0.8418,-0.9859 L -0.8665,-0.9742 L -0.8890,-0.9609 L -0.9091,-0.9461 L -0.9269,-0.9300 L -0.9421,-0.9128 L -0.9549,-0.8947 L -0.9651,-0.8759 L -0.9729,-0.8563 L -0.9783,-0.8361 L -0.9812,-0.8150 L -0.9816,-0.7932 L -0.9795,-0.7707 L -0.9748,-0.7480 L -0.9677,-0.7258 L -0.9583,-0.7048 L -0.9471,-0.6859 L -0.9345,-0.6692 L -0.9206,-0.6550 L -0.9058,-0.6434 L -0.8901,-0.6342 L -0.8738,-0.6275 L -0.8570,-0.6234 L -0.8399,-0.6218 L -0.8227,-0.6226 L -0.8053,-0.6261 L -0.7880,-0.6321 L -0.7708,-0.6409 L -0.7536,-0.6526 L -0.7362,-0.6677 L -0.7181,-0.6871 L -0.6967,-0.7142 L -0.6577,-0.7684 L -0.6391,-0.7908 L -0.6244,-0.8050 L -0.6110,-0.8147 L -0.5982,-0.8211 L -0.5857,-0.8247 L -0.5731,-0.8257 L -0.5600,-0.8241 L -0.5462,-0.8198 L -0.5313,-0.8123 L -0.5152,-0.8011 L -0.4973,-0.7853 L -0.4761,-0.7627 L -0.4209,-0.6954 L -0.3989,-0.6715 L -0.3795,-0.6539 L -0.3609,-0.6403 L -0.3426,-0.6298 L -0.3243,-0.6222 L -0.3060,-0.6173 L -0.2875,-0.6149 L -0.2690,-0.6150 L -0.2505,-0.6177 L -0.2319,-0.6229 L -0.2132,-0.6309 L -0.1943,-0.6419 L -0.1745,-0.6565 L -0.1524,-0.6763 L -0.1039,-0.7264 L -0.0813,-0.7477 L -0.0630,-0.7620 L -0.0462,-0.7720 L -0.0304,-0.7788 L -0.0151,-0.7827 L -0.0000,-0.7839 Z"/>
        <g id="arrows1">
          <use xlink:href="#arrow1" transform="translate(-0.0000,-1.1913) rotate(179.85) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline2">
        <path d="M 0.0000,-0.6449 L 0.0231,-0.6437 L 0.0472,-0.6397 L 0.0739,-0.6326 L 0.1076,-0.6206 L 0.1725,-0.5949 L 0.2039,-0.5848 L 0.2313,-0.5785 L 0.2572,-0.5750 L 0.2824,-0.5741 L 0.3075,-0.5758 L 0.3333,-0.5801 L 0.3604,-0.5873 L 0.3911,-0.5983 L 0.4456,-0.6221 L 0.4831,-0.6378 L 0.5103,-0.6468 L 0.5343,-0.6522 L 0.5567,-0.6548 L 0.5788,-0.6548 L 0.6012,-0.6523 L 0.6251,-0.6468 L 0.6524,-0.6378 L 0.7001,-0.6178 L 0.7392,-0.6017 L 0.7681,-0.5922 L 0.7938,-0.5863 L 0.8181,-0.5833 L 0.8416,-0.5828 L 0.8648,-0.5849 L 0.8879,-0.5896 L 0.9113,-0.5969 L 0.9355,-0.6073 L 0.9616,-0.6214 L 0.9940,-0.6423 L 1.0475,-0.6796 L 1.0751,-0.6964 L 1.0968,-0.7070 L 1.1163,-0.7138 L 1.1342,-0.7175 L 1.1512,-0.7186 L 1.1678,-0.7171 L 1.1845,-0.7130 L 1.2020,-0.7059 L 1.2219,-0.6948 L 1.2528,-0.6733 L 1.2858,-0.6498 L 1.3099,-0.6353 L 1.3309,-0.6253 L 1.3507,-0.6186 L 1.3697,-0.6147 L 1.3882,-0.6135 L 1.4060,-0.6149 L 1.4230,-0.6186 L 1.4391,-0.6248 L 1.4542,-0.6332 L 1.4679,-0.6437 L 1.4800,-0.6563 L 1.4904,-0.6708 L 1.4989,-0.6869 L 1.5053,-0.7046 L 1.5095,-0.7234 L 1.5112,-0.7434 L 1.5104,-0.7641 L 1.5070,-0.7855 L 1.5010,-0.8072 L 1.4921,-0.8293 L 1.4804,-0.8515 L 1.4656,-0.8739 L 1.4473,-0.8969 L 1.4244,-0.9212 L 1.3920,-0.9511 L 1.3345,-1.0008 L 1.2992,-1.0339 L 1.2673,-1.0676 L 1.2287,-1.1129 L 1.1358,-1.2291 L 1.0809,-1.2945 L 1.0316,-1.3492 L 0.9823,-1.4003 L 0.9321,-1.4486 L 0.8811,-1.4942 L 0.8294,-1.5371 L 0.7772,-1.5771 L 0.7248,-1.6142 L 0.6722,-1.6484 L 0.6193,-1.6798 L 0.5663,-1.7083 L 0.5131,-1.7341 L 0.4597,-1.7572 L 0.4061,-1.7776 L 0.3523,-1.7954 L 0.2983,-1.8107 L 0.2442,-1.8233 L 0.1900,-1.8334 L 0.1356,-1.8410 L 0.0811,-1.8460 L 0.0267,-1.8485 L -0.0279,-1.8485 L -0.0824,-1.8459 L -0.1368,-1.8408 L -0.1912,-1.8332 L -0.2454,-1.8231 L -0.2996,-1.8103 L -0.3535,-1.7950 L -0.4073,-1.7772 L -0.4609,-1.7567 L -0.5143,-1.7335 L -0.5675,-1.7077 L -0.6205,-1.6791 L -0.6734,-1.6477 L -0.7260,-1.6134 L -0.7784,-1.5763 L -0.8306,-1.5362 L -0.8823,-1.4932 L -0.9333,-1.4475 L -0.9834,-1.3991 L -1.0328,-1.3480 L -1.0821,-1.2932 L -1.1373,-1.2273 L -1.2283,-1.1133 L -1.2675,-1.0674 L -1.2995,-1.0337 L -1.3349,-1.0004 L -1.3916,-0.9515 L -1.4242,-0.9215 L -1.4471,-0.8971 L -1.4655,-0.8741 L -1.4803,-0.8517 L -1.4920,-0.8294 L -1.5009,-0.8074 L -1.5070,-0.7856 L -1.5104,-0.7643 L -1.5112,-0.7435 L -1.5095,-0.7236 L -1.5054,-0.7047 L -1.4990,-0.6871 L -1.4905,-0.6709 L -1.4801,-0.6564 L -1.4679,-0.6438 L -1.4543,-0.6332 L -1.4393,-0.6248 L -1.4231,-0.6187 L -1.4061,-0.6149 L -1.3883,-0.6135 L -1.3698,-0.6147 L -1.3508,-0.6186 L -1.3310,-0.6253 L -1.3100,-0.6352 L -1.2859,-0.6497 L -1.2531,-0.6731 L -1.2221,-0.6947 L -1.2021,-0.7059 L -1.1845,-0.7130 L -1.1678,-0.7171 L -1.1512,-0.7186 L -1.1342,-0.7175 L -1.1162,-0.7138 L -1.0968,-0.7070 L -1.0750,-0.6964 L -1.0475,-0.6796 L -0.9944,-0.6426 L -0.9619,-0.6216 L -0.9358,-0.6074 L -0.9115,-0.5970 L -0.8881,-0.5896 L -0.8650,-0.5850 L -0.8418,-0.5829 L -0.8183,-0.5833 L -0.7941,-0.5863 L -0.7684,-0.5921 L -0.7396,-0.6016 L -0.7006,-0.6176 L -0.6526,-0.6377 L -0.6252,-0.6468 L -0.6013,-0.6522 L -0.5789,-0.6548 L -0.5568,-0.6548 L -0.5344,-0.6522 L -0.5105,-0.6468 L -0.4833,-0.6378 L -0.4459,-0.6222 L -0.3912,-0.5983 L -0.3605,-0.5873 L -0.3333,-0.5801 L -0.3076,-0.5758 L -0.2824,-0.5741 L -0.2572,-0.5750 L -0.2313,-0.5785 L -0.2039,-0.5848 L -0.1725,-0.5949 L -0.1075,-0.6206 L -0.0738,-0.6326 L -0.0473,-0.6397 L -0.0232,-0.6436 L -0.0000,-0.6449 Z"/>
        <g id="arrows2">
          <use xlink:href="#arrow1" transform="translate(0.9567,-1.4246) rotate(-136.53) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-0.9568,-1.4247) rotate(135.68) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline3">
        <path d="M 0.0000,-0.5413 L 0.0362,-0.5401 L 0.0765,-0.5359 L 0.1457,-0.5250 L 0.2015,-0.5166 L 0.2426,-0.5128 L 0.2802,-0.5118 L 0.3175,-0.5133 L 0.3576,-0.5177 L 0.4089,-0.5263 L 0.4857,-0.5404 L 0.5256,-0.5456 L 0.5610,-0.5477 L 0.5959,-0.5472 L 0.6340,-0.5440 L 0.6874,-0.5363 L 0.7535,-0.5262 L 0.7934,-0.5223 L 0.8290,-0.5213 L 0.8631,-0.5229 L 0.8974,-0.5270 L 0.9343,-0.5342 L 0.9796,-0.5460 L 1.0581,-0.5684 L 1.0939,-0.5764 L 1.1248,-0.5808 L 1.1541,-0.5825 L 1.1842,-0.5816 L 1.2182,-0.5779 L 1.2777,-0.5675 L 1.3208,-0.5607 L 1.3522,-0.5581 L 1.3800,-0.5582 L 1.4056,-0.5608 L 1.4297,-0.5657 L 1.4526,-0.5729 L 1.4743,-0.5824 L 1.4948,-0.5942 L 1.5142,-0.6083 L 1.5324,-0.6246 L 1.5491,-0.6431 L 1.5645,-0.6639 L 1.5782,-0.6870 L 1.5903,-0.7123 L 1.6006,-0.7400 L 1.6091,-0.7701 L 1.6155,-0.8029 L 1.6199,-0.8387 L 1.6220,-0.8778 L 1.6216,-0.9212 L 1.6184,-0.9699 L 1.6121,-1.0255 L 1.6020,-1.0901 L 1.5874,-1.1653 L 1.5683,-1.2499 L 1.5455,-1.3387 L 1.5204,-1.4265 L 1.4936,-1.5114 L 1.4652,-1.5928 L 1.4353,-1.6709 L 1.4039,-1.7459 L 1.3710,-1.8181 L 1.3366,-1.8875 L 1.3006,-1.9543 L 1.2632,-2.0185 L 1.2244,-2.0801 L 1.1841,-2.1393 L 1.1425,-2.1960 L 1.0996,-2.2501 L 1.0554,-2.3018 L 1.0101,-2.3510 L 0.9636,-2.3978 L 0.9160,-2.4420 L 0.8674,-2.4838 L 0.8178,-2.5230 L 0.7673,-2.5597 L 0.7160,-2.5940 L 0.6639,-2.6257 L 0.6110,-2.6548 L 0.5575,-2.6815 L 0.5034,-2.7056 L 0.4488,-2.7272 L 0.3937,-2.7462 L 0.3381,-2.7628 L 0.2822,-2.7767 L 0.2261,-2.7882 L 0.1696,-2.7970 L 0.1131,-2.8034 L 0.0564,-2.8072 L -0.0004,-2.8084 L -0.0572,-2.8071 L -0.1139,-2.8033 L -0.1705,-2.7969 L -0.2269,-2.7880 L -0.2831,-2.7765 L -0.3390,-2.7625 L -0.3945,-2.7460 L -0.4496,-2.7269 L -0.5042,-2.7053 L -0.5583,-2.6811 L -0.6118,-2.6544 L -0.6647,-2.6252 L -0.7167,-2.5935 L -0.7681,-2.5592 L -0.8185,-2.5224 L -0.8681,-2.4831 L -0.9167,-2.4414 L -0.9643,-2.3971 L -1.0108,-2.3503 L -1.0561,-2.3011 L -1.1002,-2.2494 L -1.1431,-2.1951 L -1.1847,-2.1384 L -1.2250,-2.0792 L -1.2638,-2.0175 L -1.3012,-1.9533 L -1.3371,-1.8865 L -1.3715,-1.8170 L -1.4044,-1.7448 L -1.4358,-1.6698 L -1.4656,-1.5916 L -1.4940,-1.5102 L -1.5208,-1.4253 L -1.5459,-1.3373 L -1.5686,-1.2485 L -1.5877,-1.1640 L -1.6022,-1.0889 L -1.6122,-1.0248 L -1.6185,-0.9693 L -1.6216,-0.9207 L -1.6220,-0.8774 L -1.6198,-0.8383 L -1.6155,-0.8026 L -1.6090,-0.7698 L -1.6005,-0.7397 L -1.5902,-0.7121 L -1.5781,-0.6868 L -1.5643,-0.6637 L -1.5490,-0.6429 L -1.5322,-0.6244 L -1.5140,-0.6081 L -1.4946,-0.5941 L -1.4740,-0.5823 L -1.4523,-0.5728 L -1.4295,-0.5656 L -1.4054,-0.5607 L -1.3798,-0.5582 L -1.3520,-0.5581 L -1.3206,-0.5608 L -1.2775,-0.5675 L -1.2174,-0.5780 L -1.1836,-0.5817 L -1.1536,-0.5825 L -1.1243,-0.5808 L -1.0933,-0.5762 L -1.0572,-0.5681 L -0.9792,-0.5458 L -0.9340,-0.5341 L -0.8971,-0.5270 L -0.8628,-0.5228 L -0.8287,-0.5213 L -0.7931,-0.5223 L -0.7531,-0.5262 L -0.6875,-0.5363 L -0.6338,-0.5440 L -0.5959,-0.5472 L -0.5610,-0.5477 L -0.5256,-0.5456 L -0.4856,-0.5404 L -0.4099,-0.5265 L -0.3582,-0.5178 L -0.3180,-0.5134 L -0.2806,-0.5118 L -0.2431,-0.5128 L -0.2021,-0.5165 L -0.1468,-0.5248 L -0.0767,-0.5359 L -0.0363,-0.5400 L -0.0000,-0.5413 Z"/>
        <g id="arrows3">
          <use xlink:href="#arrow1" transform="translate(1.4860,-1.5333) rotate(-109.22) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(0.0000,-2.8078) rotate(179.50) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.4857,-1.5332) rotate(108.62) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline4">
        <path d="M -1.8033,-3.0100 L -1.8314,-2.9311 L -1.8574,-2.8506 L -1.8812,-2.7684 L -1.9028,-2.6847 L -1.9221,-2.5994 L -1.9392,-2.5128 L -1.9539,-2.4248 L -1.9663,-2.3355 L -1.9762,-2.2450 L -1.9837,-2.1534 L -1.9887,-2.0608 L -1.9912,-1.9674 L -1.9912,-1.8732 L -1.9886,-1.7786 L -1.9835,-1.6838 L -1.9758,-1.5893 L -1.9657,-1.4957 L -1.9532,-1.4036 L -1.9386,-1.3141 L -1.9220,-1.2283 L -1.9038,-1.1473 L -1.8844,-1.0718 L -1.8640,-1.0026 L -1.8429,-0.9395 L -1.8212,-0.8824 L -1.7990,-0.8308 L -1.7763,-0.7841 L -1.7531,-0.7421 L -1.7293,-0.7040 L -1.7050,-0.6698 L -1.6801,-0.6389 L -1.6545,-0.6112 L -1.6282,-0.5865 L -1.6013,-0.5645 L -1.5737,-0.5453 L -1.5454,-0.5285 L -1.5161,-0.5142 L -1.4859,-0.5022 L -1.4544,-0.4925 L -1.4212,-0.4849 L -1.3854,-0.4795 L -1.3450,-0.4761 L -1.2924,-0.4747 L -1.1913,-0.4746 L -1.1355,-0.4721 L -1.0799,-0.4669 L -0.9862,-0.4542 L -0.9174,-0.4456 L -0.8634,-0.4414 L -0.8107,-0.4398 L -0.7484,-0.4409 L -0.6261,-0.4462 L -0.5632,-0.4467 L -0.5021,-0.4443 L -0.4083,-0.4371 L -0.3310,-0.4320 L -0.2721,-0.4307 L -0.2106,-0.4320 L -0.0968,-0.4387 L -0.0286,-0.4415 L 0.0302,-0.4415 L 0.1031,-0.4383 L 0.2063,-0.4322 L 0.2688,-0.4307 L 0.3278,-0.4319 L 0.4037,-0.4367 L 0.5010,-0.4442 L 0.5630,-0.4467 L 0.6246,-0.4463 L 0.7413,-0.4412 L 0.8049,-0.4398 L 0.8580,-0.4411 L 0.9114,-0.4450 L 0.9776,-0.4530 L 1.0775,-0.4666 L 1.1341,-0.4720 L 1.1901,-0.4746 L 1.3010,-0.4748 L 1.3509,-0.4764 L 1.3905,-0.4801 L 1.4259,-0.4858 L 1.4588,-0.4937 L 1.4901,-0.5037 L 1.5202,-0.5160 L 1.5493,-0.5306 L 1.5775,-0.5477 L 1.6051,-0.5674 L 1.6319,-0.5897 L 1.6580,-0.6148 L 1.6835,-0.6429 L 1.7083,-0.6742 L 1.7326,-0.7090 L 1.7563,-0.7475 L 1.7795,-0.7902 L 1.8021,-0.8375 L 1.8242,-0.8898 L 1.8458,-0.9477 L 1.8668,-1.0116 L 1.8871,-1.0817 L 1.9064,-1.1579 L 1.9243,-1.2397 L 1.9407,-1.3261 L 1.9551,-1.4160 L 1.9672,-1.5083 L 1.9770,-1.6022 L 1.9843,-1.6967 L 1.9891,-1.7915 L 1.9913,-1.8861 L 1.9910,-1.9801 L 1.9882,-2.0735 L 1.9829,-2.1648 L 1.9752,-2.2552 L 1.9652,-2.3444 L 1.9527,-2.4325 L 1.9380,-2.5193 L 1.9210,-2.6048 L 1.9018,-2.6888 L 1.8803,-2.7715 L 1.8568,-2.8526 L 1.8311,-2.9321 L 1.8033,-3.0100"/>
        <g id="arrows4">
          <use xlink:href="#arrow1" transform="translate(-1.9905,-1.9861) rotate(90.87) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.0437,-0.4620) rotate(7.72) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.0437,-0.4618) rotate(-7.27) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.9905,-1.9861) rotate(-91.40) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline5">
        <path d="M -3.0255,-3.0100 L -3.0034,-2.8968 L -2.9788,-2.7837 L -2.9517,-2.6708 L -2.9220,-2.5582 L -2.8899,-2.4459 L -2.8553,-2.3341 L -2.8183,-2.2229 L -2.7789,-2.1124 L -2.7372,-2.0029 L -2.6932,-1.8944 L -2.6471,-1.7873 L -2.5989,-1.6818 L -2.5490,-1.5783 L -2.4974,-1.4772 L -2.4446,-1.3789 L -2.3908,-1.2841 L -2.3365,-1.1934 L -2.2821,-1.1073 L -2.2282,-1.0264 L -2.1751,-0.9512 L -2.1232,-0.8819 L -2.0727,-0.8185 L -2.0238,-0.7610 L -1.9765,-0.7090 L -1.9306,-0.6622 L -1.8861,-0.6202 L -1.8427,-0.5826 L -1.8003,-0.5491 L -1.7587,-0.5192 L -1.7176,-0.4928 L -1.6769,-0.4695 L -1.6364,-0.4492 L -1.5957,-0.4315 L -1.5546,-0.4164 L -1.5126,-0.4036 L -1.4690,-0.3930 L -1.4227,-0.3844 L -1.3713,-0.3775 L -1.3080,-0.3720 L -1.1378,-0.3626 L -0.9957,-0.3524 L -0.8951,-0.3459 L -0.8112,-0.3431 L -0.7005,-0.3428 L -0.5796,-0.3429 L -0.4633,-0.3402 L -0.3338,-0.3362 L -0.2332,-0.3355 L -0.0549,-0.3387 L 0.0549,-0.3387 L 0.2332,-0.3355 L 0.3338,-0.3362 L 0.4633,-0.3402 L 0.5796,-0.3429 L 0.7005,-0.3428 L 0.8112,-0.3431 L 0.8951,-0.3459 L 0.9957,-0.3524 L 1.1378,-0.3626 L 1.3080,-0.3720 L 1.3713,-0.3775 L 1.4227,-0.3844 L 1.4690,-0.3930 L 1.5126,-0.4036 L 1.5546,-0.4164 L 1.5957,-0.4315 L 1.6364,-0.4492 L 1.6769,-0.4695 L 1.7176,-0.4928 L 1.7587,-0.5192 L 1.8003,-0.5491 L 1.8427,-0.5826 L 1.8861,-0.6202 L 1.9306,-0.6622 L 1.9765,-0.7090 L 2.0238,-0.7610 L 2.0727,-0.8185 L 2.1232,-0.8819 L 2.1751,-0.9512 L 2.2282,-1.0264 L 2.2821,-1.1073 L 2.3365,-1.1934 L 2.3908,-1.2841 L 2.4446,-1.3789 L 2.4974,-1.4772 L 2.5490,-1.5783 L 2.5989,-1.6818 L 2.6471,-1.7873 L 2.6932,-1.8944 L 2.7372,-2.0029 L 2.7789,-2.1124 L 2.8183,-2.2229 L 2.8553,-2.3341 L 2.8899,-2.4459 L 2.9220,-2.5582 L 2.9517,-2.6708 L 2.9788,-2.7837 L 3.0034,-2.8968 L 3.0255,-3.0100"/>
        <g id="arrows5">
          <use xlink:href="#arrow1" transform="translate(-2.7801,-2.1168) rotate(69.60) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.8111,-0.5582) rotate(36.99) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-0.0000,-0.3387) rotate(-0.00) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.8111,-0.5581) rotate(-38.38) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(2.7802,-2.1168) rotate(-70.07) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline6">
        <path d="M -4.0100,-2.2056 L -3.9054,-2.0832 L -3.7993,-1.9630 L -3.6920,-1.8451 L -3.5835,-1.7297 L -3.4741,-1.6170 L -3.3640,-1.5071 L -3.2534,-1.4003 L -3.1428,-1.2969 L -3.0326,-1.1973 L -2.9233,-1.1018 L -2.8155,-1.0110 L -2.7100,-0.9253 L -2.6075,-0.8452 L -2.5086,-0.7710 L -2.4139,-0.7030 L -2.3238,-0.6413 L -2.2384,-0.5858 L -2.1577,-0.5362 L -2.0814,-0.4921 L -2.0092,-0.4532 L -1.9406,-0.4191 L -1.8751,-0.3892 L -1.8122,-0.3631 L -1.7513,-0.3406 L -1.6918,-0.3212 L -1.6331,-0.3047 L -1.5744,-0.2908 L -1.5145,-0.2792 L -1.4517,-0.2697 L -1.3827,-0.2620 L -1.2990,-0.2555 L -1.1316,-0.2469 L -0.9449,-0.2388 L -0.8102,-0.2352 L -0.5193,-0.2327 L -0.2870,-0.2297 L 0.0000,-0.2306 L 0.2870,-0.2297 L 0.5193,-0.2327 L 0.8102,-0.2352 L 0.9449,-0.2388 L 1.1316,-0.2469 L 1.2990,-0.2555 L 1.3827,-0.2620 L 1.4517,-0.2697 L 1.5145,-0.2792 L 1.5744,-0.2908 L 1.6331,-0.3047 L 1.6918,-0.3212 L 1.7513,-0.3406 L 1.8122,-0.3631 L 1.8751,-0.3892 L 1.9406,-0.4191 L 2.0092,-0.4532 L 2.0814,-0.4921 L 2.1577,-0.5362 L 2.2384,-0.5858 L 2.3238,-0.6413 L 2.4139,-0.7030 L 2.5086,-0.7710 L 2.6075,-0.8452 L 2.7100,-0.9253 L 2.8155,-1.0110 L 2.9233,-1.1018 L 3.0326,-1.1973 L 3.1428,-1.2969 L 3.2534,-1.4003 L 3.3640,-1.5071 L 3.4741,-1.6170 L 3.5835,-1.7297 L 3.6920,-1.8451 L 3.7993,-1.9630 L 3.9054,-2.0832 L 4.0100,-2.2056"/>
        <g id="arrows6">
          <use xlink:href="#arrow1" transform="translate(-3.3699,-1.5132) rotate(44.41) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.8679,-0.3866) rotate(22.89) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-0.0000,-0.2305) rotate(0.07) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.8679,-0.3867) rotate(-23.69) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(3.3699,-1.5132) rotate(-44.77) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline7">
        <path d="M -4.0100,-0.9033 L -3.7970,-0.8161 L -3.5881,-0.7332 L -3.3845,-0.6550 L -3.1875,-0.5820 L -2.9987,-0.5147 L -2.8199,-0.4534 L -2.6523,-0.3986 L -2.4970,-0.3504 L -2.3543,-0.3085 L -2.2235,-0.2726 L -2.1036,-0.2422 L -1.9932,-0.2167 L -1.8906,-0.1954 L -1.7941,-0.1779 L -1.7016,-0.1636 L -1.6111,-0.1521 L -1.5194,-0.1431 L -1.4214,-0.1360 L -1.3059,-0.1305 L -1.1183,-0.1250 L -0.8899,-0.1205 L -0.5769,-0.1183 L -0.2433,-0.1167 L 0.2433,-0.1167 L 0.5769,-0.1183 L 0.8899,-0.1205 L 1.1183,-0.1250 L 1.3059,-0.1305 L 1.4214,-0.1360 L 1.5194,-0.1431 L 1.6111,-0.1521 L 1.7016,-0.1636 L 1.7941,-0.1779 L 1.8906,-0.1954 L 1.9932,-0.2167 L 2.1036,-0.2422 L 2.2235,-0.2726 L 2.3543,-0.3085 L 2.4970,-0.3504 L 2.6523,-0.3986 L 2.8199,-0.4534 L 2.9987,-0.5147 L 3.1875,-0.5820 L 3.3845,-0.6550 L 3.5881,-0.7332 L 3.7970,-0.8161 L 4.0100,-0.9033"/>
        <g id="arrows7">
          <use xlink:href="#arrow1" transform="translate(-3.0462,-0.5316) rotate(19.63) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.0331,-0.1233) rotate(1.13) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.0331,-0.1233) rotate(-1.13) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(3.0462,-0.5316) rotate(-19.63) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline8">
        <path d="M -4.0100,0.0000 L 4.0100,0.0000"/>
        <g id="arrows8">
          <use xlink:href="#arrow1" transform="translate(-3.0075,0.0000) rotate(0.00) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.0025,0.0000) rotate(0.00) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.0025,0.0000) rotate(0.00) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(3.0075,0.0000) rotate(0.00) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline9">
        <path d="M -4.0100,0.9033 L -3.7970,0.8161 L -3.5881,0.7332 L -3.3845,0.6550 L -3.1875,0.5820 L -2.9987,0.5147 L -2.8199,0.4534 L -2.6523,0.3986 L -2.4970,0.3504 L -2.3543,0.3085 L -2.2235,0.2726 L -2.1036,0.2422 L -1.9932,0.2167 L -1.8906,0.1954 L -1.7941,0.1779 L -1.7016,0.1636 L -1.6111,0.1521 L -1.5194,0.1431 L -1.4214,0.1360 L -1.3059,0.1305 L -1.1183,0.1250 L -0.8899,0.1205 L -0.5769,0.1183 L -0.2433,0.1167 L 0.2433,0.1167 L 0.5769,0.1183 L 0.8899,0.1205 L 1.1183,0.1250 L 1.3059,0.1305 L 1.4214,0.1360 L 1.5194,0.1431 L 1.6111,0.1521 L 1.7016,0.1636 L 1.7941,0.1779 L 1.8906,0.1954 L 1.9932,0.2167 L 2.1036,0.2422 L 2.2235,0.2726 L 2.3543,0.3085 L 2.4970,0.3504 L 2.6523,0.3986 L 2.8199,0.4534 L 2.9987,0.5147 L 3.1875,0.5820 L 3.3845,0.6550 L 3.5881,0.7332 L 3.7970,0.8161 L 4.0100,0.9033"/>
        <g id="arrows9">
          <use xlink:href="#arrow1" transform="translate(-3.0462,0.5316) rotate(-19.63) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.0331,0.1233) rotate(-1.13) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.0331,0.1233) rotate(1.13) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(3.0462,0.5316) rotate(19.63) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline10">
        <path d="M -4.0100,2.2056 L -3.9054,2.0832 L -3.7993,1.9630 L -3.6920,1.8451 L -3.5835,1.7297 L -3.4741,1.6170 L -3.3640,1.5071 L -3.2534,1.4003 L -3.1428,1.2969 L -3.0326,1.1973 L -2.9233,1.1018 L -2.8155,1.0110 L -2.7100,0.9253 L -2.6075,0.8452 L -2.5086,0.7710 L -2.4139,0.7030 L -2.3238,0.6413 L -2.2384,0.5858 L -2.1577,0.5362 L -2.0814,0.4921 L -2.0092,0.4532 L -1.9406,0.4191 L -1.8751,0.3892 L -1.8122,0.3631 L -1.7513,0.3406 L -1.6918,0.3212 L -1.6331,0.3047 L -1.5744,0.2908 L -1.5145,0.2792 L -1.4517,0.2697 L -1.3827,0.2620 L -1.2990,0.2555 L -1.1316,0.2469 L -0.9449,0.2388 L -0.8102,0.2352 L -0.5193,0.2327 L -0.2870,0.2297 L -0.0000,0.2306 L 0.2870,0.2297 L 0.5193,0.2327 L 0.8102,0.2352 L 0.9449,0.2388 L 1.1316,0.2469 L 1.2990,0.2555 L 1.3827,0.2620 L 1.4517,0.2697 L 1.5145,0.2792 L 1.5744,0.2908 L 1.6331,0.3047 L 1.6918,0.3212 L 1.7513,0.3406 L 1.8122,0.3631 L 1.8751,0.3892 L 1.9406,0.4191 L 2.0092,0.4532 L 2.0814,0.4921 L 2.1577,0.5362 L 2.2384,0.5858 L 2.3238,0.6413 L 2.4139,0.7030 L 2.5086,0.7710 L 2.6075,0.8452 L 2.7100,0.9253 L 2.8155,1.0110 L 2.9233,1.1018 L 3.0326,1.1973 L 3.1428,1.2969 L 3.2534,1.4003 L 3.3640,1.5071 L 3.4741,1.6170 L 3.5835,1.7297 L 3.6920,1.8451 L 3.7993,1.9630 L 3.9054,2.0832 L 4.0100,2.2056"/>
        <g id="arrows10">
          <use xlink:href="#arrow1" transform="translate(-3.3699,1.5132) rotate(-44.41) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.8679,0.3866) rotate(-22.89) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-0.0000,0.2305) rotate(-0.07) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.8679,0.3867) rotate(23.69) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(3.3699,1.5132) rotate(44.77) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline11">
        <path d="M -3.0255,3.0100 L -3.0034,2.8968 L -2.9788,2.7837 L -2.9517,2.6708 L -2.9220,2.5582 L -2.8899,2.4459 L -2.8553,2.3341 L -2.8183,2.2229 L -2.7789,2.1124 L -2.7372,2.0029 L -2.6932,1.8944 L -2.6471,1.7873 L -2.5989,1.6818 L -2.5490,1.5783 L -2.4974,1.4772 L -2.4446,1.3789 L -2.3908,1.2841 L -2.3365,1.1934 L -2.2821,1.1073 L -2.2282,1.0264 L -2.1751,0.9512 L -2.1232,0.8819 L -2.0727,0.8185 L -2.0238,0.7610 L -1.9765,0.7090 L -1.9306,0.6622 L -1.8861,0.6202 L -1.8427,0.5826 L -1.8003,0.5491 L -1.7587,0.5192 L -1.7176,0.4928 L -1.6769,0.4695 L -1.6364,0.4492 L -1.5957,0.4315 L -1.5546,0.4164 L -1.5126,0.4036 L -1.4690,0.3930 L -1.4227,0.3844 L -1.3713,0.3775 L -1.3080,0.3720 L -1.1378,0.3626 L -0.9957,0.3524 L -0.8951,0.3459 L -0.8112,0.3431 L -0.7005,0.3428 L -0.5796,0.3429 L -0.4633,0.3402 L -0.3338,0.3362 L -0.2332,0.3355 L -0.0549,0.3387 L 0.0549,0.3387 L 0.2332,0.3355 L 0.3338,0.3362 L 0.4633,0.3402 L 0.5796,0.3429 L 0.7005,0.3428 L 0.8112,0.3431 L 0.8951,0.3459 L 0.9957,0.3524 L 1.1378,0.3626 L 1.3080,0.3720 L 1.3713,0.3775 L 1.4227,0.3844 L 1.4690,0.3930 L 1.5126,0.4036 L 1.5546,0.4164 L 1.5957,0.4315 L 1.6364,0.4492 L 1.6769,0.4695 L 1.7176,0.4928 L 1.7587,0.5192 L 1.8003,0.5491 L 1.8427,0.5826 L 1.8861,0.6202 L 1.9306,0.6622 L 1.9765,0.7090 L 2.0238,0.7610 L 2.0727,0.8185 L 2.1232,0.8819 L 2.1751,0.9512 L 2.2282,1.0264 L 2.2821,1.1073 L 2.3365,1.1934 L 2.3908,1.2841 L 2.4446,1.3789 L 2.4974,1.4772 L 2.5490,1.5783 L 2.5989,1.6818 L 2.6471,1.7873 L 2.6932,1.8944 L 2.7372,2.0029 L 2.7789,2.1124 L 2.8183,2.2229 L 2.8553,2.3341 L 2.8899,2.4459 L 2.9220,2.5582 L 2.9517,2.6708 L 2.9788,2.7837 L 3.0034,2.8968 L 3.0255,3.0100"/>
        <g id="arrows11">
          <use xlink:href="#arrow1" transform="translate(-2.7801,2.1168) rotate(-69.60) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.8111,0.5582) rotate(-36.99) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-0.0000,0.3387) rotate(0.00) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.8111,0.5581) rotate(38.38) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(2.7802,2.1168) rotate(70.07) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline12">
        <path d="M -1.8033,3.0100 L -1.8314,2.9311 L -1.8574,2.8506 L -1.8812,2.7684 L -1.9028,2.6847 L -1.9221,2.5994 L -1.9392,2.5128 L -1.9539,2.4248 L -1.9663,2.3355 L -1.9762,2.2450 L -1.9837,2.1534 L -1.9887,2.0608 L -1.9912,1.9674 L -1.9912,1.8732 L -1.9886,1.7786 L -1.9835,1.6838 L -1.9758,1.5893 L -1.9657,1.4957 L -1.9532,1.4036 L -1.9386,1.3141 L -1.9220,1.2283 L -1.9038,1.1473 L -1.8844,1.0718 L -1.8640,1.0026 L -1.8429,0.9395 L -1.8212,0.8824 L -1.7990,0.8308 L -1.7763,0.7841 L -1.7531,0.7421 L -1.7293,0.7040 L -1.7050,0.6698 L -1.6801,0.6389 L -1.6545,0.6112 L -1.6282,0.5865 L -1.6013,0.5645 L -1.5737,0.5453 L -1.5454,0.5285 L -1.5161,0.5142 L -1.4859,0.5022 L -1.4544,0.4925 L -1.4212,0.4849 L -1.3854,0.4795 L -1.3450,0.4761 L -1.2924,0.4747 L -1.1913,0.4746 L -1.1355,0.4721 L -1.0799,0.4669 L -0.9862,0.4542 L -0.9174,0.4456 L -0.8634,0.4414 L -0.8107,0.4398 L -0.7484,0.4409 L -0.6261,0.4462 L -0.5632,0.4467 L -0.5021,0.4443 L -0.4083,0.4371 L -0.3310,0.4320 L -0.2721,0.4307 L -0.2106,0.4320 L -0.0968,0.4387 L -0.0286,0.4415 L 0.0302,0.4415 L 0.1031,0.4383 L 0.2063,0.4322 L 0.2688,0.4307 L 0.3278,0.4319 L 0.4037,0.4367 L 0.5010,0.4442 L 0.5630,0.4467 L 0.6246,0.4463 L 0.7413,0.4412 L 0.8049,0.4398 L 0.8580,0.4411 L 0.9114,0.4450 L 0.9776,0.4530 L 1.0775,0.4666 L 1.1341,0.4720 L 1.1901,0.4746 L 1.3010,0.4748 L 1.3509,0.4764 L 1.3905,0.4801 L 1.4259,0.4858 L 1.4588,0.4937 L 1.4901,0.5037 L 1.5202,0.5160 L 1.5493,0.5306 L 1.5775,0.5477 L 1.6051,0.5674 L 1.6319,0.5897 L 1.6580,0.6148 L 1.6835,0.6429 L 1.7083,0.6742 L 1.7326,0.7090 L 1.7563,0.7475 L 1.7795,0.7902 L 1.8021,0.8375 L 1.8242,0.8898 L 1.8458,0.9477 L 1.8668,1.0116 L 1.8871,1.0817 L 1.9064,1.1579 L 1.9243,1.2397 L 1.9407,1.3261 L 1.9551,1.4160 L 1.9672,1.5083 L 1.9770,1.6022 L 1.9843,1.6967 L 1.9891,1.7915 L 1.9913,1.8861 L 1.9910,1.9801 L 1.9882,2.0735 L 1.9829,2.1648 L 1.9752,2.2552 L 1.9652,2.3444 L 1.9527,2.4325 L 1.9380,2.5193 L 1.9210,2.6048 L 1.9018,2.6888 L 1.8803,2.7715 L 1.8568,2.8526 L 1.8311,2.9321 L 1.8033,3.0100"/>
        <g id="arrows12">
          <use xlink:href="#arrow1" transform="translate(-1.9905,1.9861) rotate(-90.87) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.0437,0.4620) rotate(-7.72) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.0437,0.4618) rotate(7.27) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(1.9905,1.9861) rotate(91.40) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline13">
        <path d="M 0.0000,0.5413 L 0.0362,0.5401 L 0.0765,0.5359 L 0.1457,0.5250 L 0.2015,0.5166 L 0.2426,0.5128 L 0.2802,0.5118 L 0.3175,0.5133 L 0.3576,0.5177 L 0.4089,0.5263 L 0.4857,0.5404 L 0.5256,0.5456 L 0.5610,0.5477 L 0.5959,0.5472 L 0.6340,0.5440 L 0.6874,0.5363 L 0.7535,0.5262 L 0.7934,0.5223 L 0.8290,0.5213 L 0.8631,0.5229 L 0.8974,0.5270 L 0.9343,0.5342 L 0.9796,0.5460 L 1.0581,0.5684 L 1.0939,0.5764 L 1.1248,0.5808 L 1.1541,0.5825 L 1.1842,0.5816 L 1.2182,0.5779 L 1.2777,0.5675 L 1.3208,0.5607 L 1.3522,0.5581 L 1.3800,0.5582 L 1.4056,0.5608 L 1.4297,0.5657 L 1.4526,0.5729 L 1.4743,0.5824 L 1.4948,0.5942 L 1.5142,0.6083 L 1.5324,0.6246 L 1.5491,0.6431 L 1.5645,0.6639 L 1.5782,0.6870 L 1.5903,0.7123 L 1.6006,0.7400 L 1.6091,0.7701 L 1.6155,0.8029 L 1.6199,0.8387 L 1.6220,0.8778 L 1.6216,0.9212 L 1.6184,0.9699 L 1.6121,1.0255 L 1.6020,1.0901 L 1.5874,1.1653 L 1.5683,1.2499 L 1.5455,1.3387 L 1.5204,1.4265 L 1.4936,1.5114 L 1.4652,1.5928 L 1.4353,1.6709 L 1.4039,1.7459 L 1.3710,1.8181 L 1.3366,1.8875 L 1.3006,1.9543 L 1.2632,2.0185 L 1.2244,2.0801 L 1.1841,2.1393 L 1.1425,2.1960 L 1.0996,2.2501 L 1.0554,2.3018 L 1.0101,2.3510 L 0.9636,2.3978 L 0.9160,2.4420 L 0.8674,2.4838 L 0.8178,2.5230 L 0.7673,2.5597 L 0.7160,2.5940 L 0.6639,2.6257 L 0.6110,2.6548 L 0.5575,2.6815 L 0.5034,2.7056 L 0.4488,2.7272 L 0.3937,2.7462 L 0.3381,2.7628 L 0.2822,2.7767 L 0.2261,2.7882 L 0.1696,2.7970 L 0.1131,2.8034 L 0.0564,2.8072 L -0.0004,2.8084 L -0.0572,2.8071 L -0.1139,2.8033 L -0.1705,2.7969 L -0.2269,2.7880 L -0.2831,2.7765 L -0.3390,2.7625 L -0.3945,2.7460 L -0.4496,2.7269 L -0.5042,2.7053 L -0.5583,2.6811 L -0.6118,2.6544 L -0.6647,2.6252 L -0.7167,2.5935 L -0.7681,2.5592 L -0.8185,2.5224 L -0.8681,2.4831 L -0.9167,2.4414 L -0.9643,2.3971 L -1.0108,2.3503 L -1.0561,2.3011 L -1.1002,2.2494 L -1.1431,2.1951 L -1.1847,2.1384 L -1.2250,2.0792 L -1.2638,2.0175 L -1.3012,1.9533 L -1.3371,1.8865 L -1.3715,1.8170 L -1.4044,1.7448 L -1.4358,1.6698 L -1.4656,1.5916 L -1.4940,1.5102 L -1.5208,1.4253 L -1.5459,1.3373 L -1.5686,1.2485 L -1.5877,1.1640 L -1.6022,1.0889 L -1.6122,1.0248 L -1.6185,0.9693 L -1.6216,0.9207 L -1.6220,0.8774 L -1.6198,0.8383 L -1.6155,0.8026 L -1.6090,0.7698 L -1.6005,0.7397 L -1.5902,0.7121 L -1.5781,0.6868 L -1.5643,0.6637 L -1.5490,0.6429 L -1.5322,0.6244 L -1.5140,0.6081 L -1.4946,0.5941 L -1.4740,0.5823 L -1.4523,0.5728 L -1.4295,0.5656 L -1.4054,0.5607 L -1.3798,0.5582 L -1.3520,0.5581 L -1.3206,0.5608 L -1.2775,0.5675 L -1.2174,0.5780 L -1.1836,0.5817 L -1.1536,0.5825 L -1.1243,0.5808 L -1.0933,0.5762 L -1.0572,0.5681 L -0.9792,0.5458 L -0.9340,0.5341 L -0.8971,0.5270 L -0.8628,0.5228 L -0.8287,0.5213 L -0.7931,0.5223 L -0.7531,0.5262 L -0.6875,0.5363 L -0.6338,0.5440 L -0.5959,0.5472 L -0.5610,0.5477 L -0.5256,0.5456 L -0.4856,0.5404 L -0.4099,0.5265 L -0.3582,0.5178 L -0.3180,0.5134 L -0.2806,0.5118 L -0.2431,0.5128 L -0.2021,0.5165 L -0.1468,0.5248 L -0.0767,0.5359 L -0.0363,0.5400 L -0.0000,0.5413 Z"/>
        <g id="arrows13">
          <use xlink:href="#arrow1" transform="translate(1.4860,1.5333) rotate(109.22) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(0.0000,2.8078) rotate(-179.50) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-1.4857,1.5332) rotate(-108.62) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline14">
        <path d="M 0.0000,0.6449 L 0.0231,0.6437 L 0.0472,0.6397 L 0.0739,0.6326 L 0.1076,0.6206 L 0.1725,0.5949 L 0.2039,0.5848 L 0.2313,0.5785 L 0.2572,0.5750 L 0.2824,0.5741 L 0.3075,0.5758 L 0.3333,0.5801 L 0.3604,0.5873 L 0.3911,0.5983 L 0.4456,0.6221 L 0.4831,0.6378 L 0.5103,0.6468 L 0.5343,0.6522 L 0.5567,0.6548 L 0.5788,0.6548 L 0.6012,0.6523 L 0.6251,0.6468 L 0.6524,0.6378 L 0.7001,0.6178 L 0.7392,0.6017 L 0.7681,0.5922 L 0.7938,0.5863 L 0.8181,0.5833 L 0.8416,0.5828 L 0.8648,0.5849 L 0.8879,0.5896 L 0.9113,0.5969 L 0.9355,0.6073 L 0.9616,0.6214 L 0.9940,0.6423 L 1.0475,0.6796 L 1.0751,0.6964 L 1.0968,0.7070 L 1.1163,0.7138 L 1.1342,0.7175 L 1.1512,0.7186 L 1.1678,0.7171 L 1.1845,0.7130 L 1.2020,0.7059 L 1.2219,0.6948 L 1.2528,0.6733 L 1.2858,0.6498 L 1.3099,0.6353 L 1.3309,0.6253 L 1.3507,0.6186 L 1.3697,0.6147 L 1.3882,0.6135 L 1.4060,0.6149 L 1.4230,0.6186 L 1.4391,0.6248 L 1.4542,0.6332 L 1.4679,0.6437 L 1.4800,0.6563 L 1.4904,0.6708 L 1.4989,0.6869 L 1.5053,0.7046 L 1.5095,0.7234 L 1.5112,0.7434 L 1.5104,0.7641 L 1.5070,0.7855 L 1.5010,0.8072 L 1.4921,0.8293 L 1.4804,0.8515 L 1.4656,0.8739 L 1.4473,0.8969 L 1.4244,0.9212 L 1.3920,0.9511 L 1.3345,1.0008 L 1.2992,1.0339 L 1.2673,1.0676 L 1.2287,1.1129 L 1.1358,1.2291 L 1.0809,1.2945 L 1.0316,1.3492 L 0.9823,1.4003 L 0.9321,1.4486 L 0.8811,1.4942 L 0.8294,1.5371 L 0.7772,1.5771 L 0.7248,1.6142 L 0.6722,1.6484 L 0.6193,1.6798 L 0.5663,1.7083 L 0.5131,1.7341 L 0.4597,1.7572 L 0.4061,1.7776 L 0.3523,1.7954 L 0.2983,1.8107 L 0.2442,1.8233 L 0.1900,1.8334 L 0.1356,1.8410 L 0.0811,1.8460 L 0.0267,1.8485 L -0.0279,1.8485 L -0.0824,1.8459 L -0.1368,1.8408 L -0.1912,1.8332 L -0.2454,1.8231 L -0.2996,1.8103 L -0.3535,1.7950 L -0.4073,1.7772 L -0.4609,1.7567 L -0.5143,1.7335 L -0.5675,1.7077 L -0.6205,1.6791 L -0.6734,1.6477 L -0.7260,1.6134 L -0.7784,1.5763 L -0.8306,1.5362 L -0.8823,1.4932 L -0.9333,1.4475 L -0.9834,1.3991 L -1.0328,1.3480 L -1.0821,1.2932 L -1.1373,1.2273 L -1.2283,1.1133 L -1.2675,1.0674 L -1.2995,1.0337 L -1.3349,1.0004 L -1.3916,0.9515 L -1.4242,0.9215 L -1.4471,0.8971 L -1.4655,0.8741 L -1.4803,0.8517 L -1.4920,0.8294 L -1.5009,0.8074 L -1.5070,0.7856 L -1.5104,0.7643 L -1.5112,0.7435 L -1.5095,0.7236 L -1.5054,0.7047 L -1.4990,0.6871 L -1.4905,0.6709 L -1.4801,0.6564 L -1.4679,0.6438 L -1.4543,0.6332 L -1.4393,0.6248 L -1.4231,0.6187 L -1.4061,0.6149 L -1.3883,0.6135 L -1.3698,0.6147 L -1.3508,0.6186 L -1.3310,0.6253 L -1.3100,0.6352 L -1.2859,0.6497 L -1.2531,0.6731 L -1.2221,0.6947 L -1.2021,0.7059 L -1.1845,0.7130 L -1.1678,0.7171 L -1.1512,0.7186 L -1.1342,0.7175 L -1.1162,0.7138 L -1.0968,0.7070 L -1.0750,0.6964 L -1.0475,0.6796 L -0.9944,0.6426 L -0.9619,0.6216 L -0.9358,0.6074 L -0.9115,0.5970 L -0.8881,0.5896 L -0.8650,0.5850 L -0.8418,0.5829 L -0.8183,0.5833 L -0.7941,0.5863 L -0.7684,0.5921 L -0.7396,0.6016 L -0.7006,0.6176 L -0.6526,0.6377 L -0.6252,0.6468 L -0.6013,0.6522 L -0.5789,0.6548 L -0.5568,0.6548 L -0.5344,0.6522 L -0.5105,0.6468 L -0.4833,0.6378 L -0.4459,0.6222 L -0.3912,0.5983 L -0.3605,0.5873 L -0.3333,0.5801 L -0.3076,0.5758 L -0.2824,0.5741 L -0.2572,0.5750 L -0.2313,0.5785 L -0.2039,0.5848 L -0.1725,0.5949 L -0.1075,0.6206 L -0.0738,0.6326 L -0.0473,0.6397 L -0.0232,0.6436 L -0.0000,0.6449 Z"/>
        <g id="arrows14">
          <use xlink:href="#arrow1" transform="translate(0.9567,1.4246) rotate(136.53) scale(2.0)"/>
          <use xlink:href="#arrow1" transform="translate(-0.9568,1.4247) rotate(-135.68) scale(2.0)"/>
        </g>
      </g>
      <g id="fieldline15">
        <path d="M 0.0000,0.7839 L 0.0151,0.7827 L 0.0304,0.7788 L 0.0462,0.7720 L 0.0630,0.7620 L 0.0813,0.7477 L 0.1039,0.7264 L 0.1524,0.6763 L 0.1745,0.6565 L 0.1943,0.6419 L 0.2132,0.6309 L 0.2319,0.6229 L 0.2505,0.6177 L 0.2690,0.6150 L 0.2875,0.6149 L 0.3060,0.6173 L 0.3243,0.6222 L 0.3426,0.6298 L 0.3609,0.6403 L 0.3795,0.6539 L 0.3989,0.6715 L 0.4209,0.6953 L 0.4761,0.7627 L 0.4973,0.7853 L 0.5152,0.8011 L 0.5313,0.8123 L 0.5462,0.8198 L 0.5600,0.8241 L 0.5731,0.8257 L 0.5857,0.8247 L 0.5983,0.8211 L 0.6110,0.8147 L 0.6244,0.8049 L 0.6392,0.7907 L 0.6576,0.7684 L 0.6958,0.7154 L 0.7174,0.6879 L 0.7356,0.6683 L 0.7530,0.6531 L 0.7702,0.6413 L 0.7874,0.6324 L 0.8047,0.6262 L 0.8221,0.6227 L 0.8393,0.6217 L 0.8564,0.6233 L 0.8732,0.6274 L 0.8895,0.6339 L 0.9052,0.6430 L 0.9201,0.6546 L 0.9340,0.6687 L 0.9467,0.6852 L 0.9580,0.7041 L 0.9674,0.7250 L 0.9746,0.7472 L 0.9794,0.7699 L 0.9816,0.7924 L 0.9812,0.8143 L 0.9784,0.8354 L 0.9731,0.8556 L 0.9654,0.8752 L 0.9553,0.8941 L 0.9426,0.9122 L 0.9274,0.9294 L 0.9098,0.9456 L 0.8897,0.9604 L 0.8673,0.9738 L 0.8427,0.9855 L 0.8156,0.9955 L 0.7855,1.0038 L 0.7508,1.0105 L 0.6860,1.0190 L 0.6512,1.0246 L 0.6249,1.0312 L 0.5999,1.0401 L 0.5716,1.0531 L 0.5234,1.0794 L 0.4688,1.1091 L 0.4276,1.1288 L 0.3887,1.1447 L 0.3498,1.1579 L 0.3101,1.1687 L 0.2687,1.1772 L 0.2247,1.1837 L 0.1761,1.1882 L 0.1176,1.1907 L 0.0061,1.1914 L -0.1120,1.1908 L -0.1721,1.1884 L -0.2213,1.1841 L -0.2655,1.1778 L -0.3070,1.1694 L -0.3468,1.1588 L -0.3858,1.1458 L -0.4248,1.1300 L -0.4656,1.1107 L -0.5179,1.0825 L -0.5689,1.0545 L -0.5979,1.0409 L -0.6231,1.0317 L -0.6493,1.0250 L -0.6833,1.0193 L -0.7496,1.0107 L -0.7845,1.0040 L -0.8146,0.9958 L -0.8418,0.9859 L -0.8665,0.9742 L -0.8890,0.9609 L -0.9091,0.9461 L -0.9269,0.9300 L -0.9421,0.9128 L -0.9549,0.8947 L -0.9651,0.8759 L -0.9729,0.8563 L -0.9783,0.8361 L -0.9812,0.8150 L -0.9816,0.7932 L -0.9795,0.7707 L -0.9748,0.7480 L -0.9677,0.7258 L -0.9583,0.7048 L -0.9471,0.6859 L -0.9345,0.6692 L -0.9206,0.6550 L -0.9058,0.6434 L -0.8901,0.6342 L -0.8738,0.6275 L -0.8570,0.6234 L -0.8399,0.6218 L -0.8227,0.6226 L -0.8053,0.6261 L -0.7880,0.6321 L -0.7708,0.6409 L -0.7536,0.6526 L -0.7362,0.6677 L -0.7181,0.6871 L -0.6967,0.7142 L -0.6577,0.7684 L -0.6391,0.7908 L -0.6244,0.8050 L -0.6110,0.8147 L -0.5982,0.8211 L -0.5857,0.8247 L -0.5731,0.8257 L -0.5600,0.8241 L -0.5462,0.8198 L -0.5313,0.8123 L -0.5152,0.8011 L -0.4973,0.7853 L -0.4761,0.7627 L -0.4209,0.6954 L -0.3989,0.6715 L -0.3795,0.6539 L -0.3609,0.6403 L -0.3426,0.6298 L -0.3243,0.6222 L -0.3060,0.6173 L -0.2875,0.6149 L -0.2690,0.6150 L -0.2505,0.6177 L -0.2319,0.6229 L -0.2132,0.6309 L -0.1943,0.6419 L -0.1745,0.6565 L -0.1524,0.6763 L -0.1039,0.7264 L -0.0813,0.7477 L -0.0630,0.7620 L -0.0462,0.7720 L -0.0304,0.7788 L -0.0151,0.7827 L -0.0000,0.7839 Z"/>
        <g id="arrows15">
          <use xlink:href="#arrow1" transform="translate(-0.0000,1.1913) rotate(-179.85) scale(2.0)"/>
        </g>
      </g>
    </g>
    <g id="symbols">
      <g id="current_out1" transform="translate(-1.4,0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <circle cx="0" cy="0" r="4"/>
      </g>
      <g id="current_in2" transform="translate(-1.4,-0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <path d="M 8.6,-11.0 L 11.0,-8.6 L 2.6,0 L 11.0,8.6 L 8.6,11.0 0,2.6 L -8.6,11.0 L -11.0,8.6 L -2.6,0 L -11.0,-8.6 L -8.6,-11.0 L 0,-2.6 L 8.6,-11.0 Z" style="fill:#000000; stroke:none"/>
      </g>
      <g id="current_out3" transform="translate(-0.84,0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <circle cx="0" cy="0" r="4"/>
      </g>
      <g id="current_in4" transform="translate(-0.84,-0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <path d="M 8.6,-11.0 L 11.0,-8.6 L 2.6,0 L 11.0,8.6 L 8.6,11.0 0,2.6 L -8.6,11.0 L -11.0,8.6 L -2.6,0 L -11.0,-8.6 L -8.6,-11.0 L 0,-2.6 L 8.6,-11.0 Z" style="fill:#000000; stroke:none"/>
      </g>
      <g id="current_out5" transform="translate(-0.28,0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <circle cx="0" cy="0" r="4"/>
      </g>
      <g id="current_in6" transform="translate(-0.28,-0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <path d="M 8.6,-11.0 L 11.0,-8.6 L 2.6,0 L 11.0,8.6 L 8.6,11.0 0,2.6 L -8.6,11.0 L -11.0,8.6 L -2.6,0 L -11.0,-8.6 L -8.6,-11.0 L 0,-2.6 L 8.6,-11.0 Z" style="fill:#000000; stroke:none"/>
      </g>
      <g id="current_out7" transform="translate(0.28,0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <circle cx="0" cy="0" r="4"/>
      </g>
      <g id="current_in8" transform="translate(0.28,-0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <path d="M 8.6,-11.0 L 11.0,-8.6 L 2.6,0 L 11.0,8.6 L 8.6,11.0 0,2.6 L -8.6,11.0 L -11.0,8.6 L -2.6,0 L -11.0,-8.6 L -8.6,-11.0 L 0,-2.6 L 8.6,-11.0 Z" style="fill:#000000; stroke:none"/>
      </g>
      <g id="current_out9" transform="translate(0.84,0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <circle cx="0" cy="0" r="4"/>
      </g>
      <g id="current_in10" transform="translate(0.84,-0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <path d="M 8.6,-11.0 L 11.0,-8.6 L 2.6,0 L 11.0,8.6 L 8.6,11.0 0,2.6 L -8.6,11.0 L -11.0,8.6 L -2.6,0 L -11.0,-8.6 L -8.6,-11.0 L 0,-2.6 L 8.6,-11.0 Z" style="fill:#000000; stroke:none"/>
      </g>
      <g id="current_out11" transform="translate(1.4,0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <circle cx="0" cy="0" r="4"/>
      </g>
      <g id="current_in12" transform="translate(1.4,-0.7) scale(0.01,0.01)">
        <circle style="fill:#b0b0b0; stroke:none" cx="0" cy="0" r="14"/>
        <circle cx="0" cy="0" r="14" style="fill:url(#white_spot); stroke:#000000; stroke-width:2"/>
        <path d="M 8.6,-11.0 L 11.0,-8.6 L 2.6,0 L 11.0,8.6 L 8.6,11.0 0,2.6 L -8.6,11.0 L -11.0,8.6 L -2.6,0 L -11.0,-8.6 L -8.6,-11.0 L 0,-2.6 L 8.6,-11.0 Z" style="fill:#000000; stroke:none"/>
      </g>
    </g>
  </g>
</svg>
 *(Conceptual illustration)*
*   **Significance**: This resemblance highlights Ampere's original hypothesis that all magnetism originates from electric currents, whether macroscopic (in a wire) or microscopic (orbital/spin motion of electrons in atoms). It is the basis for electromagnets.

### **5.3 Atomic Origin of Magnetization (Atomistic)**

Magnetism in materials primarily originates from the fundamental quantum mechanical properties of their constituent electrons within atoms. Nuclear magnetic moments exist but are typically much weaker and usually negligible in macroscopic material magnetism.

*   **1. Orbital Magnetic Moment ($\mu_{orb}$)**:
    *   **Cause**: Electrons orbiting the atomic nucleus constitute a tiny, circulating electric current. According to Ampere's laws, any current loop generates a magnetic dipole moment. This is the electron's orbital magnetic moment.
    *   **Relation to Orbital Angular Momentum ($L$)**: The orbital magnetic moment is directly proportional to the orbital angular momentum of the electron ($\vec{L}$). For an electron with charge $e$ and mass $m_e$:
        $$\vec{\mu}_{orb} = -\frac{e}{2m_e} \vec{L}$$
        The negative sign indicates that for a negatively charged electron, the direction of the magnetic moment is opposite to the direction of its orbital angular momentum.
    *   **Gyromagnetic Ratio ($\gamma$)**: The ratio of the magnetic moment to its corresponding angular momentum is called the gyromagnetic ratio:
        $$\gamma = \frac{|\vec{\mu}_{orb}|}{|\vec{L}|} = \frac{e}{2m_e}$$
    *   **Quantization and Bohr Magneton ($\mu_B$)**: In quantum mechanics, orbital angular momentum is quantized in units of $\hbar$ ($L = \sqrt{l(l+1)}\hbar$, with $L_z = m_l \hbar$). The fundamental unit of magnetic moment associated with this quantization (when $L_z = \hbar$) is called the **Bohr magneton**:
        $$\mu_B = \frac{e\hbar}{2m_e} \approx 9.27 \times 10^{-24} \text{ J/T (or Am}^2\text{)}$$
        Atomic orbital magnetic moments are typically integer multiples of $\mu_B$.


*   **2. Spin Magnetic Moment ($\mu_{spin}$)**:
    *   **Cause**: This is a purely quantum mechanical intrinsic property of the electron, often conceptualized as the electron "spinning" on its axis. This intrinsic spin angular momentum ($\vec{S}$) gives rise to an intrinsic spin magnetic dipole moment ($\vec{\mu}_{spin}$). It has no classical analogue.
    *   **Relation to Spin Angular Momentum ($\vec{S}$)**: The spin magnetic moment is related to the spin angular momentum by:
        $$\vec{\mu}_{spin} = -g_e \frac{e}{2m_e} \vec{S} = -g_e \mu_B \frac{\vec{S}}{\hbar}$$
        Where $s=1/2$ is the spin quantum number, and $g_e \approx 2.0023$ is the electron g-factor (for a free electron, often approximated as 2).
    *   **Contribution**: The spin magnetic moment is a very significant contributor to the total atomic magnetic moment and is often the **dominant factor** in determining the magnetic properties of many materials, especially the strong magnetism found in ferromagnets.

*   **Total Atomic Magnetic Moment**: The total magnetic moment of an atom is the vector sum of the orbital and spin magnetic moments of all its electrons. In solids, the crystalline environment can affect these moments; for example, orbital motion is often "quenched" by interactions with neighboring atoms, leaving spin as the primary contributor.

### **5.4 Larmor Precession**

**Larmor Precession** is the precessional motion of a magnetic dipole moment (which is associated with an angular momentum) when placed in a uniform external static magnetic field. Instead of simply aligning with the magnetic field, the magnetic moment and its associated angular momentum vector rotate (precess) around the direction of the magnetic field, similar to how a spinning top precesses in a gravitational field.

*   **Effect of Torque**: A magnetic dipole moment $\vec{\mu}$ in an external magnetic field $\vec{B}$ experiences a torque $\vec{\tau}$ given by:
    $$\vec{\tau} = \vec{\mu} \times \vec{B}$$
    From classical mechanics, the rate of change of angular momentum $\vec{L}$ is equal to the applied torque:
    $$\frac{d\vec{L}}{dt} = \vec{\tau}$$
    Combining these, we get $\frac{d\vec{L}}{dt} = \vec{\mu} \times \vec{B}$.

*   **Derivation of Larmor Frequency ($\omega_L$)**:
    For the orbital magnetic moment of an electron, we have $\vec{\mu}_{orb} = -\frac{e}{2m_e} \vec{L}$.
    Substituting this into the torque equation:
    $$\frac{d\vec{L}}{dt} = \left(-\frac{e}{2m_e} \vec{L}\right) \times \vec{B}$$
    $$\frac{d\vec{L}}{dt} = -\left(\frac{eB}{2m_e}\right) (\hat{z} \times \vec{L})$$ (if $\vec{B}$ is along the z-axis)
    This equation describes a precessional motion where $\vec{L}$ precesses around the axis of $\vec{B}$ at a constant angular frequency. This angular frequency is the **Larmor frequency ($\omega_L$)**:
    $$\omega_L = \frac{eB}{2m_e}$$
    (For spin magnetic moments, a g-factor ($g$) is typically included, so $\omega_L = g \frac{eB}{2m_e}$).

*   **Induced Magnetic Moment (Diamagnetism)**: For electrons in their orbits, Larmor precession induces an additional magnetic moment. According to Lenz's law, this induced moment *always opposes* the external magnetic field. This induced moment is the classical explanation for diamagnetism.
    $$\mu_{ind} = -\frac{Ze^2\langle r^2 \rangle}{4m_e} B$$
    Where $Z$ is the number of electrons per atom and $\langle r^2 \rangle$ is the average square radius of the electron orbits.
*   **Applications**: Larmor precession is fundamental to understanding diamagnetism, and it forms the physical basis for important spectroscopic techniques like Nuclear Magnetic Resonance (NMR) and Electron Spin Resonance (ESR), which rely on resonance at the Larmor frequency.

### **5.5 Quantum Effects in Atomic Magnetism**

#### **5.5.1 Normal Zeeman Effect using Orbital Angular Momentum**
The **Zeeman effect** is the splitting of atomic spectral lines into several closely spaced components in the presence of an external static magnetic field. The **Normal Zeeman effect** is a specific case observed in atoms where the total electron spin is zero (or all spins are paired), meaning the magnetic moment of the atom arises solely from the orbital angular momentum of its electrons.

*   **Origin**: An electron in an orbital state has an orbital magnetic moment $\vec{\mu}_l$ that interacts with an external magnetic field $\vec{B}$ (assumed to be along the z-axis). The interaction energy (Zeeman energy) is $E_B = -\vec{\mu}_l \cdot \vec{B}$.
*   **Energy Levels Splitting**: Since $\vec{\mu}_l = -g_l \mu_B \frac{\vec{L}}{\hbar}$ (with $g_l=1$ for orbital motion), the interaction energy becomes $E_B = g_l \mu_B \frac{\vec{L} \cdot \vec{B}}{\hbar}$.
    In quantum mechanics, the component of the orbital angular momentum along the z-axis is quantized ($L_z = m_l \hbar$, where $m_l$ is the magnetic orbital quantum number, taking values from $-l, -(l-1), \dots, 0, \dots, +(l-1), +l$).
    Thus, the energy shift experienced by an electron in a state with magnetic quantum number $m_l$ is:
    $$E_B = \mu_B B m_l \quad (\text{since } g_l=1)$$
*   **Reduction of Degeneracy**: In the absence of a magnetic field, atomic energy levels are often degenerate with respect to $m_l$ (states with different $m_l$ values have the same energy). The application of an external magnetic field lifts this degeneracy. Each degenerate energy level splits into $(2l+1)$ distinct sub-levels, each corresponding to a different allowed value of $m_l$. These split energy levels result in observing multiple distinct frequencies (and thus spectral lines) instead of a single one during electron transitions. This provides direct experimental evidence for the quantization of angular momentum.

#### **5.5.2 Role of the Magnetic Moment Operator in ESR and NMR Spectroscopy**
In quantum mechanics, every measurable physical quantity (observable) is associated with an operator. The **magnetic moment operator ($\hat{\vec{\mu}}$)** precisely describes the intrinsic magnetic properties of a particle (electron or nucleus) and how it interacts with magnetic fields. Its role is fundamental in both Electron Spin Resonance (ESR) and Nuclear Magnetic Resonance (NMR) spectroscopy.

*   **Magnetic Moment Operator for Electron Spin ($\hat{\vec{\mu}}_S$)**: For an electron, the dominant magnetic moment is due to its spin: $\hat{\vec{\mu}}_S = -g_e \mu_B \frac{\hat{\vec{S}}}{\hbar}$, where $\hat{\vec{S}}$ is the spin angular momentum operator and $g_e \approx 2$ is the electron g-factor.
*   **Magnetic Moment Operator for Nuclear Spin ($\hat{\vec{\mu}}_I$)**: For a nucleus with spin: $\hat{\vec{\mu}}_I = g_N \mu_N \frac{\hat{\vec{I}}}{\hbar}$, where $\hat{\vec{I}}$ is the nuclear spin angular momentum operator and $\mu_N$ is the nuclear magneton.

*   **Role in **ESR (Electron Spin Resonance) Spectroscopy****:
    *   ESR specializes in studying materials with **unpaired electrons**. When a sample is placed in a static magnetic field ($\vec{B}_0$), the electron's spin magnetic moment interacts with $\vec{B}_0$. This interaction is governed by the electron spin magnetic moment operator and leads to the splitting of the electron's spin energy levels (Zeeman effect for spin).
    *   An oscillating electromagnetic field (typically microwaves) is then applied perpendicular to $\vec{B}_0$. When the frequency of this oscillating field matches the energy difference between the split spin states ($\hbar \omega = \Delta E$), the electron spins "flip," absorbing energy.
    *   The magnetic moment operator is central because it defines the exact energy levels (Hamiltonian $\hat{H} = -\hat{\vec{\mu}}_S \cdot \vec{B}_0$) and governs how the electron spin couples to the oscillating field to induce these transitions. By analyzing these resonance conditions, ESR reveals information about the electronic structure and environment of paramagnetic species.

*   **Role in **NMR (Nuclear Magnetic Resonance) Spectroscopy****:
    *   NMR focuses on nuclei with a non-zero spin angular momentum (e.g., $^1$H, $^{13}$C). These nuclei possess a nuclear magnetic moment.
    *   When placed in a static magnetic field ($\vec{B}_0$), the nuclear magnetic moments interact with $\vec{B}_0$, causing their nuclear spin energy levels to split. This interaction is described by the nuclear magnetic moment operator mentioned above.
    *   A radiofrequency (RF) pulse is then applied. When the RF frequency matches the energy difference between the split nuclear spin states, energy is absorbed, and nuclear spins "flip."
    *   The nuclear magnetic moment operator is crucial as it defines these energy level splittings and mediates the transitions between them. The precise resonance frequency is extremely sensitive to the local electronic environment around the nucleus (known as the "chemical shift"), making NMR an invaluable tool for determining molecular structure in chemistry and biochemistry, and for medical imaging (MRI).

### **5.6 Classification of Magnetic Materials Based on Susceptibility**

Magnetic materials are classified based on the nature and magnitude of their magnetic susceptibility ($\chi_m$) and their characteristic response to an applied magnetic field.

1.  **Diamagnetic Materials:**
    *   **Characteristics**: Very small, **negative** magnetic susceptibility ($\chi_m < 0$, typically in the range of $-10^{-6}$ to $-10^{-3}$). Relative permeability $\mu_r < 1$.
    *   **Behavior**: Are **weakly repelled** by magnetic fields. Field lines are slightly pushed out of the material.
    *   **Origin**: A universal effect present in all materials. It arises from the Larmor precession of electron orbits induced by an external magnetic field, which creates a moment opposing the field (Lenz's Law). Occurs even in materials with permanent moments, but is often masked.
    *   **Temperature Dependence**: Largely **temperature independent**.
    *   **Examples**: Water (H$_2$O), Copper (Cu), Bismuth (Bi), Silver (Ag), Gold (Au), Noble gases. Superconductors are perfect diamagnets ($\chi_m = -1$).

2.  **Paramagnetic Materials:**
    *   **Characteristics**: Small, **positive** magnetic susceptibility ($\chi_m > 0$, typically $10^{-5}$ to $10^{-3}$). Relative permeability $\mu_r > 1$.
    *   **Behavior**: Are **weakly attracted** by magnetic fields. Field lines are slightly concentrated within the material.
    *   **Origin**: Possess permanent atomic magnetic dipoles due to **unpaired electron spins** (and sometimes unquenched orbital moments). In the absence of an external field, these dipoles are randomly oriented due to thermal agitation. An external field causes partial alignment, producing a net positive magnetization.
    *   **Temperature Dependence**: Follows **Curie's Law** ($\chi_m = C/T$), meaning susceptibility is inversely proportional to the absolute temperature. As temperature increases, thermal agitation reduces the alignment, decreasing $\chi_m$.
    *   **Examples**: Aluminum (Al), Oxygen (O$_2$, liquid), Platinum (Pt), Transition metal ions (e.g., Mn$^{2+}$, Fe$^{3+}$), Alkali metals.

3.  **Ferromagnetic Materials:**
    *   **Characteristics**: Very large, **positive** magnetic susceptibility ($\chi_m \gg 0$, typically $10^3$ to $10^5$). Relative permeability $\mu_r \gg 1$.
    *   **Behavior**: Are **strongly attracted** by magnetic fields. Exhibit **spontaneous magnetization** (a net magnetic moment even without an applied external field).
    *   **Origin**: A strong **quantum mechanical exchange interaction** between adjacent electron spins causes them to align parallel to each other. This leads to long-range magnetic ordering within regions called **magnetic domains**.
    *   **Temperature Dependence**: Exhibit a critical temperature called the **Curie Temperature ($T_C$)**. Below $T_C$, they are ferromagnetic. Above $T_C$, thermal energy overcomes the exchange interaction, and the material loses its spontaneous magnetization, becoming paramagnetic. For $T > T_C$, susceptibility follows the **Curie-Weiss Law** ($\chi_m = C/(T - T_C)$).
    *   **Other Properties**: Exhibit **magnetic hysteresis** (non-linear M-H relationship, remanence, coercivity).
    *   **Examples**: Iron (Fe), Cobalt (Co), Nickel (Ni), Gadolinium (Gd), many alloys.

4.  **Antiferromagnetic Materials:**
    *   **Characteristics**: Small, positive magnetic susceptibility, which peaks at the **Néel temperature ($T_N$)**. Effectively zero net macroscopic magnetization.
    *   **Behavior**: Little or no net attraction to magnetic fields.
    *   **Origin**: Below $T_N$, the exchange interaction causes adjacent atomic magnetic moments to align **anti-parallel** and with **equal magnitudes**. This perfect anti-parallel alignment results in a complete cancellation of magnetic moments on a macroscopic scale.
    *   **Temperature Dependence**: Susceptibility increases with temperature up to $T_N$, then decreases above $T_N$ following a modified Curie-Weiss law.
    *   **Spin Arrangement**: Spins on two interpenetrating sublattices are anti-parallel and cancel out perfectly.
    *   **Examples**: Manganese Oxide (MnO), Chromium (Cr), Nickel Oxide (NiO).

5.  **Ferrimagnetic Materials:**
    *   **Characteristics**: Large, positive magnetic susceptibility ($\chi_m > 0$), but generally smaller than ferromagnets. Also exhibit spontaneous magnetization.
    *   **Behavior**: Strongly attracted by magnetic fields, similar to ferromagnets.
    *   **Origin**: Below a characteristic critical temperature ($T_C$ or $T_N$), the exchange interaction causes adjacent atomic magnetic moments to align **anti-parallel** but with **unequal magnitudes** (e.g., moments on different sublattices have different strengths). This unequal cancellation results in a net spontaneous magnetic moment for the material.
    *   **Temperature Dependence**: Similar to ferromagnets, they have a Curie temperature ($T_C$) above which they become paramagnetic.
    *   **Examples**: Ferrites (e.g., Fe$_3$O$_4$ (magnetite), NiFe$_2$O$_4$), Garnets.

### **5.7 Paramagnetism, Average Magnetization and the Brillouin Function (Quantum vs. Classical Ideas)**

#### **5.7.1 Quantum Theory of Paramagnetism**
The quantum theory of paramagnetism provides a more accurate and complete description than classical Langevin theory by incorporating spin and quantized angular momentum.
1.  **Origin of Moments**: Paramagnetic atoms possess a permanent magnetic dipole moment ($\vec{\mu}$) primarily due to unpaired electron spins (and sometimes unquenched orbital angular momentum). These moments are typically quantized in units of the Bohr magneton ($\mu_B$).
2.  **Interaction with Magnetic Field (Zeeman Effect)**: When an external magnetic field ($\vec{B}$) is applied, atomic energy levels split due to the interaction of the magnetic moment with the field (Zeeman effect). For a total angular momentum quantum number $J$, the energy in a magnetic field $B$ is $E = -m_J g \mu_B B$, where $m_J$ is the magnetic quantum number (from $-J$ to $+J$) and $g$ is the Landé g-factor. Each $m_J$ value corresponds to a specific orientation and energy.
3.  **Boltzmann Population**: At finite temperatures, the populations of these split energy levels follow the **Boltzmann distribution**. Lower energy states (moments more aligned with $\vec{B}$) are slightly more populated than higher energy states (moments more anti-aligned).
4.  **Net Magnetization**: This unequal population results in a net magnetization ($M$) in the direction of the applied field.

*   **Curie's Law (Low Field / High Temperature, $g\mu_B B \ll k_B T$)**:
    In this regime, thermal energy is significantly greater than the energy splitting due to the magnetic field. The net magnetization ($M$) is directly proportional to the field $H$ and inversely proportional to $T$. For $N$ atoms per unit volume, each with a magnetic moment, the susceptibility follows **Curie's Law**:
    $$\chi_m = \frac{C}{T}$$
    Where the Curie constant $C = \frac{N g^2 \mu_0 \mu_B^2 J(J+1)}{3 k_B}$. This correctly describes the observed inverse temperature dependence of paramagnetism.

*   **Brillouin Function (High Field / Low Temperature, $g\mu_B B \gg k_B T$)**:
    At very high magnetic fields and/or very low temperatures, the magnetic energy becomes comparable to or greater than the thermal energy. In this saturation regime, most magnetic moments align with the external field, and the magnetization no longer increases linearly but approaches a saturation value. The average magnetization per atom is described by the **Brillouin function ($B_J(x)$)**:
    $$\langle \mu_z \rangle = g \mu_B J B_J(x)$$
    Where $x = \frac{g \mu_B J B}{k_B T}$, and $B_J(x) = \frac{2J+1}{2J} \coth\left(\frac{2J+1}{2J}x\right) - \frac{1}{2J} \coth\left(\frac{x}{2J}\right)$.
    The total magnetization is $M = N \langle \mu_z \rangle$.
    *   **Cases**:
        *   **$J=1/2$ (e.g., free electron spin)**: The Brillouin function simplifies considerably for this fundamental case.
        *   **$J \rightarrow \infty$ (Classical Limit)**: In the limit of very large angular momentum, the Brillouin function approaches the classical **Langevin function ($L(x) = \coth x - \frac{1}{x}$, where $x=\mu B / k_B T$)**. This shows how classical mechanics emerges from quantum mechanics in the appropriate limit.

#### **5.7.2 Classical Ideas of Magnetic Moment (Langevin's Theory)**
As detailed in Section 6.1.3, Langevin's classical theory of paramagnetism models magnetic moments as classical dipoles free to rotate. It also leads to the Curie Law in the low field/high temperature limit ($\chi_m = C/T$, where $C = \frac{N \mu^2 \mu_0}{3 k_B}$). While successful for this specific limit, it fails to explain the quantum origin of moments and the saturation behavior correctly.

### **5.8 Weiss' Molecular Field, T-dependence of Susceptibilities, Ferromagnetic Behaviour**

#### **5.8.1 Weiss' Molecular Field Theory for Ferromagnetism**
The **Weiss Molecular Field Theory** (1907) is a phenomenological (not fully microscopic) theory that successfully explains the spontaneous magnetization and the Curie temperature in ferromagnetic materials.
*   **Concept**: Weiss postulated the existence of a very strong **internal molecular field ($H_w$)** within a ferromagnetic material. This field acts on each atomic magnetic moment, tending to align it parallel to its neighbors. This internal field is much stronger than any external field and is responsible for the spontaneous alignment of spins.
*   **Proportionality**: Weiss assumed that this internal field is directly proportional to the macroscopic magnetization ($M$) of the material itself:
    $$H_w = \lambda M$$
    where $\lambda$ is the dimensionless Weiss molecular field constant (a large positive value).
*   **Total Effective Field**: The total effective magnetic field ($H_{eff}$) acting on an atomic moment is the sum of the external applied field ($H_a$) and the molecular field: $H_{eff} = H_a + \lambda M$.
*   **Spontaneous Magnetization**: Even if $H_a=0$, if $\lambda M$ is sufficiently large, a non-zero $H_{eff}$ can exist and sustain the magnetization $M$, leading to spontaneous magnetization.
*   **Quantum Origin**: Later, the Weiss molecular field was identified as a macroscopic manifestation of the much stronger, microscopic **quantum mechanical exchange interaction** between electron spins.

#### **5.8.2 Temperature Dependence of Susceptibilities and Ferromagnetic Behaviour**
*   **Ferromagnetic State ($T < T_C$)**: Below the Curie temperature ($T_C$), the material exhibits spontaneous magnetization due to the strong exchange interaction. It is characterized by magnetic domains and hysteresis.
*   **Paramagnetic State ($T > T_C$)**: As the temperature increases and approaches $T_C$, the thermal agitation energy ($k_B T$) becomes comparable to the energy associated with the exchange interaction. Above $T_C$, thermal energy overcomes the alignment force of the molecular field, and the spontaneous magnetization disappears. The material transitions to a paramagnetic state.
*   **Curie-Weiss Law**: For temperatures above $T_C$, the susceptibility of a ferromagnetic material in its paramagnetic phase is described by the **Curie-Weiss Law**:
    $$\chi_m = \frac{C}{T - T_C}$$
    Where $C$ is the Curie constant (but derived considering the molecular field) and $T_C$ is the Curie temperature. This law effectively extends Curie's Law to account for the internal field in ferromagnets. It predicts that $\chi_m$ is very large just above $T_C$ and decreases as $T$ increases.

#### **5.8.3 Magnetic Domains**
Ferromagnetic materials are divided into microscopic regions called **magnetic domains**, typically micron-sized. Within each domain, all atomic magnetic moments are aligned parallel due to the exchange interaction, resulting in spontaneous saturation magnetization. The overall material may appear unmagnetized if these domains are randomly oriented. Domain walls (thin transition regions) separate these domains.
*   **Domain Formation Minimizes Total Energy**: The formation of domains is a key mechanism for a ferromagnet to minimize its total energy. A uniformly magnetized material would produce strong external magnetic fields, representing high **magnetostatic (demagnetization) energy**. By dividing into smaller domains with magnetizations pointing in different directions, the external stray fields are drastically reduced, lowering the magnetostatic energy. This gain in reduced magnetostatic energy outweighs the energy cost of forming domain walls (which have exchange and anisotropy energy).

#### **5.8.4 Hysteresis**
The **hysteresis** property is a defining characteristic of ferromagnetic materials, where the magnetization ($M$) of the material depends not only on the current applied magnetic field ($H$) but also on its magnetic history. This is graphically represented by a **Hysteresis Loop**.
*   **Description of Hysteresis Loop**: A plot of magnetization (M) versus applied magnetic field (H). Starting from an unmagnetized state (origin), as the external field H is increased, M increases non-linearly to a maximum value called **saturation magnetization ($M_s$)**. Upon reducing H to zero, M does not return to zero but retains a residual magnetization called **remanence or retentivity ($M_r$)**. To bring M to zero, a reverse magnetic field, called **coercivity ($H_c$)**, must be applied. Further cycling of the field completes the characteristic loop.
    ![Magnetic Hysteresis Loop](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/Hysteresis_loop_soft_magnetics.svg/800px-Hysteresis_loop_soft_magnetics.svg.png)
*   **Significance**: Hysteresis implies energy loss (proportional to the loop area) during each cycle of magnetization and demagnetization, and it gives ferromagnetic materials a "memory," which is crucial for data storage applications.

### **5.9 Antiferromagnetic and Ferrimagnetic Materials**

#### **5.9.1 Antiferromagnetic Materials**
*   **Characteristics**:
    *   Below a characteristic temperature called the **Néel temperature ($T_N$)**, the exchange interaction causes adjacent atomic magnetic moments to align **anti-parallel** to each other with **equal magnitudes**.
    *   This perfect anti-parallel alignment results in **zero net (spontaneous) macroscopic magnetization** for the material.
    *   Magnetic susceptibility is typically small and positive, increasing with temperature up to $T_N$, then decreasing above $T_N$.
*   **Spin Arrangement**: Spins effectively cancel each other out on a macroscopic scale (e.g., $\uparrow \downarrow \uparrow \downarrow$).
*   **Examples**: Manganese Oxide (MnO), Chromium (Cr), Nickel Oxide (NiO).

#### **5.9.2 Ferrimagnetic Materials**
*   **Characteristics**:
    *   Below a characteristic critical temperature ($T_C$ or $T_N$), the exchange interaction causes adjacent atomic magnetic moments to align **anti-parallel** to each other but with **unequal magnitudes** (e.g., different types of magnetic ions or different crystallographic sites might have different magnetic moments).
    *   This unequal cancellation results in a **net spontaneous macroscopic magnetization** for the material, although typically smaller than in ferromagnets. Ferrimagnets exhibit hysteresis.
*   **Difference from Ferromagnetism**: Ferromagnetism has all moments parallel, maximizing net magnetization. Ferrimagnetism has anti-parallel moments, but unequal strengths lead to a net moment.
*   **Examples**: Ferrites (e.g., Fe$_3$O$_4$ (magnetite), NiFe$_2$O$_4$), Garnets.

#### **5.9.3 Magnetic Susceptibility vs. Temperature (Summary)**

**Description of Susceptibility vs. Temperature Plot:** This plot typically shows how the magnetic susceptibility ($\chi_m$) of different materials changes with temperature ($T$).
*   **Diamagnetic**: Constant, small negative $\chi_m$, independent of $T$.
*   **Paramagnetic**: Follows Curie's law ($\chi_m \propto 1/T$), decreasing as $T$ increases.
*   **Ferromagnetic**: Very high $\chi_m$ below its Curie temperature ($T_C$), then sharply drops and follows the Curie-Weiss law ($\chi_m \propto 1/(T-T_C)$) above $T_C$.
*   **Antiferromagnetic**: $\chi_m$ increases with $T$ to a peak at $T_N$ (Néel temperature), then decreases.
*   **Ferrimagnetic**: Similar to ferromagnets, with high $\chi_m$ below a $T_C$, sharply dropping above it.
![Magnetic Susceptibility vs. Temperature](https://ars.els-cdn.com/content/image/3-s2.0-B978012803254500002X-f02-12-9780128032545.jpg)

### **5.10 Soft vs. Hard Magnetic Materials**

Ferromagnetic materials are further categorized based on their hysteresis loop characteristics, which dictate their suitability for different applications.

| Feature                | Soft Magnetic Materials                                       | Hard Magnetic Materials                                             |
| :--------------------- | :------------------------------------------------------------ | :------------------------------------------------------------------ |
| **Hysteresis Loop**    | **Narrow** and small area.                                    | **Wide** and large area.                                            |
| **Coercivity ($H_c$)** | **Low**. Easy to demagnetize (low reverse field needed).    | **High**. Difficult to demagnetize (large reverse field needed). |
| **Retentivity ($M_r$)** | Relatively **low** to moderate.                              | **High**. Retain strong magnetization after field removal.         |
| **Saturation ($M_s$)** | Often high (desirable for high flux).                         | Can be high, but the emphasis is on high $M_r$ and $H_c$.           |
| **Energy Loss/Cycle**  | **Low** (small loop area) – important for AC applications. | **High** (large loop area).                                         |
| **Permeability**       | Very **high** initial and maximum permeability.              | Low to moderate permeability.                                       |
| **Magnetic Behavior**  | Easily magnetized and demagnetized. Responsive to changing fields. | Resist magnetization but retain it strongly once magnetized. Ideal for permanent magnets. |
| **Microscopic Origin** | Low magneto-crystalline anisotropy; few crystal defects/impurities, allowing easy domain wall motion. | High magneto-crystalline anisotropy; many defects/impurities (to pin domain walls and resist demagnetization). |
| **Applications**       | **Temporary magnets**, devices operating under AC fields. Used in transformer cores, electromagnets, magnetic shielding, recording heads, pulse applications. | **Permanent magnets**, devices requiring retained magnetism. Used in loudspeakers, motors, generators, magnetic clutches, magnetic recording media (hard drives). |
| **Examples**           | Pure Iron, Silicon steel, Permalloy, Ferrites (some types).   | Alnico, Neodymium magnets (NdFeB), Cobalt steel, Ceramic magnets.   |

### **5.11 Applications of Magnetic Materials: Magnetoresistance and GMR**

*   **Magnetoresistance (MR)**: This is a general property of a material where its electrical resistance changes when an external magnetic field is applied. The change can be an increase or a decrease in resistance and can originate from various mechanisms. The **ordinary magnetoresistance** (OMR) in normal metals arises from the Lorentz force deflecting current paths.

#### **Giant Magnetoresistance (GMR) Device**
**Giant Magnetoresistance (GMR)** is an exceptionally strong magnetoresistance effect observed in specific multilayered nanostructures, where the electrical resistance of the structure changes significantly (up to 50% or more) depending on the relative orientation of the magnetization in adjacent ferromagnetic (FM) layers.
*   **Structure**: Typically consists of a superlattice of alternating thin ferromagnetic layers (e.g., Cobalt, Nickel-Iron alloys) and very thin non-magnetic, conducting spacer layers (e.g., Copper).
*   **Physical Origin (Spin-Dependent Scattering)**: The GMR effect is fundamentally a quantum mechanical phenomenon rooted in **spin-dependent scattering** of conduction electrons.
    1.  **Spin Polarization**: In a ferromagnetic material, the density of states at the Fermi level is different for spin-up and spin-down electrons. This means that electrons acquire a 'spin polarization' when passing through an FM layer, and their scattering probability within an FM layer (and at its interfaces) depends on whether their spin is parallel or anti-parallel to the layer's magnetization direction.
    2.  **Parallel Alignment (Low Resistance)**: When the magnetizations of two adjacent ferromagnetic layers are aligned **parallel** to each other (e.g., both up), electrons whose spins are parallel to this magnetization find a low-resistance path through both layers (they scatter less). Electrons with anti-parallel spins find a high-resistance path. The overall resistance is relatively low because one spin channel is highly conductive.
    3.  **Anti-parallel Alignment (High Resistance)**: When the magnetizations of the two ferromagnetic layers are aligned **anti-parallel** to each other (e.g., one up, one down), electrons with a specific spin orientation (e.g., up) will find a low-resistance path in the first FM layer but a high-resistance path in the second. Conversely, electrons with the opposite spin (down) find a high-resistance path in the first FM layer but a low-resistance path in the second. In effect, *both* spin channels experience significant scattering across the entire structure, leading to a much higher overall electrical resistance.
*   **Applications (Memory and Data Storage)**: GMR has revolutionized data storage and sensing.
    1.  **Hard Disk Drive (HDD) Read Heads**: This is its most significant application. GMR sensors are used as highly sensitive read heads in modern hard disk drives. Tiny magnetic bits (representing 0s and 1s) on the disk surface create minute magnetic fields. As the read head passes over these bits, the magnetic field from the bit causes the magnetization in one of the GMR layers (referred to as the "free layer") to switch, changing the relative alignment of the FM layers and thus altering the resistance of the sensor. This change in resistance is detected as an electrical signal, allowing for the precise and high-density reading of stored data bits. GMR technology enabled a massive increase in HDD storage density.
    2.  **Magnetic Field Sensors**: GMR sensors are utilized in various applications requiring high-sensitivity magnetic field detection, such as automotive sensors (e.g., for ABS or crankshaft position), current sensors, and magnetic encoders.

---

## 6. Phase Transitions

A **phase transition** is a phenomenon where a material changes its physical state (or phase) due to changes in external conditions such as temperature, pressure, or applied magnetic fields. **Order-disorder phase transitions** are a specific type where the arrangement of microscopic elements (atoms, spins, etc.) within a material changes from an ordered, regular configuration to a more random, disordered configuration, or vice versa.

### **6.1 Significance of Order-Disorder Phase Transitions**
Order-disorder phase transitions are profoundly significant for understanding materials science and condensed matter physics due to their impact on material properties and role in fundamental physics.

1.  **Fundamental Physics Insight**: They are key examples of cooperative phenomena, where localized microscopic interactions (e.g., exchange interactions between spins, bonding between atoms) lead to large-scale, collective changes in the material's state. Studies of these transitions are central to statistical mechanics and critical phenomena.
2.  **Dramatic Property Alteration**: These transitions often cause abrupt (or continuous) and significant changes in a material's physical properties:
    *   **Magnetic Properties**: A ferromagnetic material losing its strong magnetism and becoming paramagnetic above its Curie temperature ($T_C$) is a classic example.
    *   **Electrical Properties**: Changes in atomic ordering can lead to changes in electrical conductivity.
    *   **Structural Properties**: Changes in the arrangement of atoms (e.g., from an ordered alloy to a disordered one) can alter mechanical properties like hardness and ductility.
3.  **Technological Relevance**: Many modern technologies exploit these transitions:
    *   **Memory Devices**: Phase change memory (PCMs) in data storage relies on rapid, reversible transitions between amorphous (disordered) and crystalline (ordered) states.
    *   **Sensors and Actuators**: Materials exhibiting sharp transitions in properties (e.g., resistivity, magnetization) at certain temperatures are used in sensors and actuators.
    *   **Shape Memory Alloys**: These materials undergo reversible, solid-state structural order-disorder transitions (often martensitic transformations) that allow them to "remember" and recover a pre-set shape upon heating.

### **6.2 Examples of First Order and Second Order Phase Transitions**

Phase transitions are traditionally classified by the continuity of the Gibbs free energy and its derivatives at the transition point.

#### **6.2.1 First Order Phase Transitions**
*   **Characteristics**: These transitions involve a **discontinuity in the first derivatives** of the Gibbs free energy with respect to temperature and pressure (e.g., entropy, volume, magnetization). They are characterized by:
    *   **Latent Heat**: A finite amount of latent heat is absorbed (or released) during the transition. Energy is required to change the phase.
    *   **Phase Coexistence**: Two distinct phases (e.g., liquid and gas, or solid and liquid) can coexist in thermodynamic equilibrium at the transition temperature.
    *   **Abrupt Changes**: Properties like density, crystal structure, and entropy change abruptly at the transition point.
*   **Examples**:
    1.  **Melting (Solid to Liquid)**: The transition from ice to water at 0°C. There is a specific latent heat of fusion absorbed, and ice and water can coexist.
    2.  **Boiling (Liquid to Gas)**: The transition from liquid water to steam at 100°C. There is a latent heat of vaporization, and liquid and gas can coexist.
    3.  **Superconducting Transition (Type I in a field)**: The transition of a Type I superconductor from the superconducting state to the normal state in the presence of a magnetic field. This is considered a first-order transition because it involves a discontinuity in the magnetization and a latent heat associated with the magnetic energy.

#### **6.2.2 Second Order Phase Transitions**
*   **Characteristics**: These transitions involve a **continuity in the first derivatives** of the Gibbs free energy but a **discontinuity in the second derivatives** (e.g., specific heat, magnetic susceptibility, compressibility). They are characterized by:
    *   **No Latent Heat**: No latent heat is absorbed or released during the transition; the process occurs continuously.
    *   **No Phase Coexistence**: Only one phase exists at the critical temperature; there is no distinct interface between two phases.
    *   **Continuous Order Parameter**: The "order parameter" (a physical quantity that quantifies the degree of order in the system) continuously goes to zero at the critical point.
    *   **Critical Phenomena**: Often associated with critical exponents, power laws, and universal scaling behavior near the transition point.
*   **Examples**:
    1.  **Ferromagnetic to Paramagnetic Transition**: The transition of a ferromagnet (like Nickel or Cobalt) from the ordered ferromagnetic state to the disordered paramagnetic state above its Curie temperature ($T_C$). The spontaneous magnetization (the order parameter) continuously goes to zero at $T_C$.
    2.  **Superconducting Transition (Type II & Zero-field $T_C$)**: The transition of a Type II superconductor from the mixed/vortex state to the normal state at its upper critical field ($H_{C2}$). Also, the transition of any superconductor from the normal state to the superconducting state in zero magnetic field at $T_C$ is typically a second-order transition.
    3.  **Lambda Transition in Helium-4**: The transition of liquid Helium-4 from its normal fluid state (He-I) to a superfluid state (He-II) at 2.17 K, known as the lambda point.
    4.  **Order-Disorder Transitions in Alloys**: In some alloys (e.g., $\beta$-brass or CuZn), beyond a critical temperature, the different atom types arrange randomly (disordered state), but below it, they occupy specific lattice sites in an ordered superstructure (ordered state).

---

## 7. Superconductivity (Advanced Topic)

**Superconductivity** is a remarkable quantum mechanical phenomenon observed in certain materials, called superconductors, when they are cooled below a specific critical temperature ($T_C$). In this state, they exhibit two primary, unique characteristics: exactly zero electrical resistance and the complete expulsion of magnetic flux fields from their interior (the Meissner effect).

*   **Discovery**: The phenomenon was first discovered by Heike Kamerlingh Onnes in 1911 when he observed that the electrical resistance of mercury dropped abruptly to zero below 4.1 Kelvin.
*   **Critical Temperature ($T_C$)**: This is the characteristic temperature below which a given material transitions from its normal conducting state to the superconducting state. It varies widely among materials, from fractions of a Kelvin to over 130 K for high-temperature cuprate superconductors.
*   **Key Observations / General Properties of Superconductors**:
    *   **Zero Electrical Resistance**: Once current is established in a superconducting loop, it can flow indefinitely without any applied voltage or energy dissipation.
    *   **Perfect Diamagnetism (Meissner Effect)**: Superconductors expel all magnetic flux from their interior when cooled below $T_C$ in a magnetic field.
    *   **Persistent Currents**: The zero-resistance property allows for persistent currents, which can flow for extremely long durations (experiments have shown persistent currents lasting for over $10^5$ years).
    *   **Critical Fields and Currents**: Superconductivity is destroyed (the material reverts to its normal state) if:
        *   The temperature rises above $T_C$.
        *   An external magnetic field exceeds a critical value ($H_C$).
        *   The current flowing through the superconductor exceeds a critical current ($I_C$).
    *   **Material Types**: Superconductivity is not observed in monovalent metals (e.g., Cu, Ag, Au) or good ferromagnets/antiferromagnets. It is usually found in metals with 2-6 valence electrons, alloys, and certain ceramic compounds.

### **7.1 Meissner Effect**
*   **Statement**: The Meissner effect states that when a superconductor is cooled below its critical temperature ($T_C$) in the presence of an external magnetic field, it **actively expels all magnetic field lines from its interior**.
*   **Explanation**: This expulsion means that the magnetic flux density inside the superconductor becomes zero ($B=0$). This is not merely a consequence of zero resistance (which would only trap existing flux), but an active thermodynamic property of the superconducting state. The superconductor achieves this by generating surface currents that produce an internal magnetic field exactly equal and opposite to the external applied field.
*   **Perfect Diamagnetism**: Due to the Meissner effect, a superconductor behaves as a **perfect diamagnet**, with a magnetic susceptibility $\chi_m = -1$ and a relative permeability $\mu_r = 0$.
*   **Significance**: The Meissner effect is a distinguishing feature of superconductivity, demonstrating that the superconducting state is a distinct thermodynamic phase rather than simply a perfect electrical conductor without resistance. It is responsible for phenomena like magnetic levitation.

### **7.2 Critical Field ($H_C$)**
*   **Definition**: The **critical magnetic field ($H_C$)** is the maximum strength of an external magnetic field that a superconductor can withstand while remaining in the superconducting state, at a given temperature below $T_C$.
*   **Temperature Dependence**: The critical field is temperature-dependent. Its strength decreases as the temperature approaches $T_C$ and is maximum at 0 K. The empirical relationship is often given by:
    $$H_C(T) = H_0 \left[1 - \left(\frac{T}{T_C}\right)^2\right]$$
    Where $H_0$ is the critical field at 0K. If the magnetic field exceeds $H_C(T)$, the material transitions back to its normal, resistive state.

### **7.3 Type I and Type II Superconductors**
Superconductors are broadly categorized into two types based on their response to an external magnetic field:

| Feature                   | Type I Superconductors (Soft Superconductors)                                   | Type II Superconductors (Hard Superconductors)                                                                                          |
| :------------------------ | :------------------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------- |
| **Material Type**         | Typically pure metals (e.g., Aluminum (Al), Lead (Pb), Mercury (Hg), Tin (Sn)). | Typically alloys or compounds and complex ceramic materials (e.g., Niobium-Titanium (NbTi), Niobium-Tin (Nb3Sn), YBCO (YBa2Cu3O7-x)). |
| **Meissner Effect**       | Exhibit a **complete Meissner effect**. Magnetic field is completely expelled from the interior up to $H_C$.                          | Exhibit a complete Meissner effect only up to a lower critical field ($H_{C1}$). Between $H_{C1}$ and $H_{C2}$, magnetic flux partially penetrates (vortex state). |
| **Critical Field Behavior** | Have a **single critical magnetic field ($H_C$)**. Below $H_C$, they are superconducting. Above $H_C$, they abruptly become normal. | Have **two critical magnetic fields**: a lower critical field ($H_{C1}$) and an upper critical field ($H_{C2}$). Above $H_{C2}$, they fully revert to normal. |
| **Transition to Normal**  | An **abrupt** (first-order) transition from the superconducting to the normal state at $H_C$.                                 | A **gradual** (second-order-like) transition through a "mixed" or "vortex" state between $H_{C1}$ and $H_{C2}$, before becoming fully normal. |
| **Critical Current Density** | Typically have a **low** critical current density ($J_C$).                  | Typically have a **high** critical current density ($J_C$). Can carry much larger currents without resistance.                      |
| **Applications**          | Limited practical applications due to their low critical fields. Used in fundamental research, highly sensitive magnetometers (SQUIDs). | Widely used for high-field magnets in various technologies (e.g., MRI, Maglev trains, particle accelerators, fusion reactors) due to their high $H_{C2}$ and $J_C$. |

**Schematic Diagram of Critical Magnetic Field Behavior:**
**Description of Diagram:** This schematic diagram illustrates the phase boundaries separating the normal and superconducting states as a function of external magnetic field (H) and temperature (T).
For **Type I superconductors (blue curve)**, there is a single critical field curve $H_C(T)$ that defines the boundary. Below this curve, the material is in the superconducting state (zero resistance, complete Meissner effect). Above the curve, it reverts abruptly to the normal state. $H_C(0)$ is the maximum critical field at 0K, and $T_C$ is the critical temperature at zero field.
For **Type II superconductors (green curves)**, there are two distinct critical field curves: $H_{C1}(T)$ (lower critical field) and $H_{C2}(T)$ (upper critical field).
1.  **Meissner (Superconducting) State**: Below $H_{C1}(T)$, the material is fully superconducting with complete flux expulsion.
2.  **Mixed (Vortex) State**: Between $H_{C1}(T)$ and $H_{C2}(T)$, magnetic flux penetrates the material in quantized filaments (vortices), but the bulk remains superconducting and can carry a supercurrent. The Meissner effect is incomplete.
3.  **Normal State**: Above $H_{C2}(T)$, the material completely loses its superconducting properties.
Note that the maximum $H_{C2}$ for Type II superconductors is typically much higher than $H_C$ for Type I materials, making them suitable for high-field applications.
![Critical magnetic field behavior for Type I and Type II superconductors](https://qph.cf2.quoracdn.net/main-qimg-80dc48e7188b776a394b9f33333e680a-lq)

### **7.4 BCS Theory (Bardeen-Cooper-Schrieffer Theory) - Concise Ideas**
The **BCS theory** (developed by Bardeen, Cooper, and Schrieffer in 1957) is the microscopic theory that explains conventional superconductivity (Type I and some Type II superconductors).

*   **1. Cooper Pairs**: The central idea of BCS theory is that electrons, which normally repel each other due to their negative charge, can form weakly bound pairs called **Cooper pairs** despite this repulsion. This occurs through an indirect attractive interaction that is mediated by the vibrations of the crystal lattice (phonons). An electron moving through the lattice slightly distorts it, creating a momentary region of positive charge concentration. A second electron is then attracted to this region.
*   **2. Bosonic Behavior**: A Cooper pair consists of two electrons with opposite momenta and opposite spins ($\mathbf{k}\uparrow, -\mathbf{k}\downarrow$). Because the total spin of a Cooper pair is an integer (0 or 1), Cooper pairs behave as **bosons**. Unlike fermions (individual electrons) which obey the Pauli Exclusion Principle, many bosons can occupy the exact same lowest-energy quantum state.
*   **3. Collective Coherent State**: Below the critical temperature ($T_C$), a vast number of these Cooper pairs condense into a single, highly ordered, coherent ground quantum state. This forms a collective quantum fluid, often referred to as a "superfluid," where all Cooper pairs move in unison and cannot be individually scattering.
*   **4. Energy Gap**: The BCS theory predicts the existence of an **energy gap ($2\Delta$)** that separates the ground state of Cooper pairs from the lowest excited (unpaired) electron states. For A Cooper pair to break apart or scatter (which would lead to resistance), it must gain energy at least equal to this gap.
*   **5. Zero Resistance**: Below $T_C$, the ambient thermal energy ($k_B T$) is generally much smaller than the energy gap ($k_B T \ll 2\Delta$). Therefore, thermal fluctuations are insufficient to break Cooper pairs or scatter them. This allows the Cooper pairs to flow freely through the lattice without resistance.

### **7.5 Superconducting Qubits**
Superconducting circuits are one of the most promising and rapidly developing platforms for building **qubits**, the fundamental quantum bits of information in quantum computing.

*   **Josephson Junctions (JJ)**: These are the fundamental non-linear circuit elements that enable superconducting qubits. A Josephson junction consists of two superconducting electrodes separated by a very thin (typically ~1-2 nm) non-superconducting insulating barrier.
    *   **DC Josephson Effect**: Even with no applied voltage, a supercurrent (flow of Cooper pairs) can tunnel through the insulating barrier, up to a critical current ($I_c$), with exactly zero resistance.
    *   **AC Josephson Effect**: If a constant voltage $V$ is applied across the junction, an alternating current flows through it with a frequency $f = 2eV/h$. This means the junction acts as a perfect converter of DC voltage to AC current, and vice versa.
    *   **Role in Qubits**: JJs provide the necessary non-linearity (anharmonicity) in the energy levels of superconducting circuits, which is crucial for creating well-defined, addressable two-level quantum systems (qubits).
*   **Transmon Qubit**: The Transmon is a widely used type of superconducting qubit.
    *   **Realization**: It is typically realized as a superconducting circuit consisting of a Josephson junction connected in parallel (shunted) by a relatively large capacitor. This capacitance serves to reduce the sensitivity of the qubit to charge noise from the environment.
    *   **Working Principle**: The Josephson junction's inherent non-linearity creates an anharmonic potential for the circuit, meaning its energy levels are not equally spaced. This anharmonicity is critical for qubit operation; it allows microwave pulses to selectively excite the system from the ground state ($|0\rangle$) to the first excited state ($|1\rangle$) without inadvertently exciting higher energy states ($|2\rangle$, etc.). This selective excitation creates a reliable two-level system that can store quantum information. The large shunting capacitor increases the ratio of Josephson energy to charging energy ($E_J/E_C$), making the transmon insensitive to charge fluctuations, which enhances its coherence time.
*   **Advantages of Superconducting Qubits**:
    *   **Scalability**: Superconducting circuits can be fabricated using standard microfabrication techniques, offering paths towards integrating many qubits on a single chip.
    *   **Control**: Qubits can be precisely manipulated and entangled using microwave pulses, allowing for fast quantum gate operations.
    *   **Coherence**: While still a challenge, significant progress has been made in achieving long coherence times (the time before quantum information is lost) in superconducting qubits, especially with designs like the transmon.

### **7.6 Applications of Superconductivity**
The unique properties of superconductors offer vast potential for technological applications:
*   **Medical Imaging (MRI - Magnetic Resonance Imaging)**: Superconducting electromagnets are essential for MRI scanners. Their zero resistance allows them to generate exceptionally strong, stable, and uniform magnetic fields (e.g., 1.5 T, 3 T, 7 T) necessary for high-resolution imaging of soft tissues in the body, without dissipating large amounts of energy as heat.
*   **High-Sensitivity Detection (SQUIDs - Superconducting QUantum Interference Devices)**: SQUIDs are the most sensitive detectors of magnetic flux known. They utilize Josephson junctions and quantum interference to measure extremely weak magnetic fields (many orders of magnitude weaker than Earth's field).
    *   **Applications**: Used in biomagnetism (MEG for brain activity, MCG for heart activity), geophysics (detecting subtle magnetic anomalies), and materials science for characterizing magnetic properties.
*   **Magnetic Levitation (Maglev Trains)**: Superconducting magnets in Maglev trains generate strong magnetic fields that interact either with other magnets or with specialized track materials to produce an electromagnetic repulsive force, levitating the train above the guideway. This eliminates friction, enabling very high speeds and energy efficiency.
*   **Particle Accelerators**: Powerful superconducting magnets are crucial components in modern particle accelerators (e.g., the Large Hadron Collider at CERN). They are used to generate the strong and precise magnetic fields required to guide, bend, and focus high-energy particle beams.
*   **Fusion Reactors**: Future fusion reactors (e.g., ITER) will rely on large superconducting magnets to confine extremely hot plasma (at millions of degrees Celsius) within a "magnetic bottle," preventing it from touching the reactor walls.
*   **Quantum Computing**: Superconducting qubits (e.g., transmons) are a leading technology for developing quantum computers due to their scalability, controllability, and improving coherence properties.
*   **Power Transmission**: Superconducting power cables offer the potential for transmitting electricity with virtually zero energy loss, improving energy efficiency and reducing grid congestion. However, cooling requirements remain a challenge for widespread adoption.

---
# [[Semester 1/Physics/Physics\|Back]]