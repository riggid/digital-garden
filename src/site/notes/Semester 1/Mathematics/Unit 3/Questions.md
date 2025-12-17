---
{"dg-publish":true,"permalink":"/semester-1/mathematics/unit-3/questions/"}
---

# [[Semester 1/Mathematics/Mathematics\|Back]]
***
[[Semester 1/Mathematics/Unit 3/Core Notes\|Core Notes]] | [[Semester 1/Mathematics/Unit 3/Examples\|Examples]] | [[Semester 1/Mathematics/Unit 3/Questions\|Questions]]

# Unit 3 Questions: Partial Differential Equations

## 1. Formation of PDE
*   **1. Form the PDE from $z = y^2 + 2f(1/x + \log y)$.**
    *   **Answer**: $x^2 p + yq = 2y^2$. See [[Semester 1/Mathematics/Unit 3/Examples#Example 2: Formation by Eliminating Arbitrary Functions\|Examples]].
*   **2. Form the PDE from $z = (x+y)f(x^2 - y^2)$.**
    *   **Answer**: $py + qz = z$.
*   **3. Form the PDE from $z = f(x+at) + g(x-at)$.**
    *   **Answer**: $\frac{\partial^2 z}{\partial t^2} = a^2 \frac{\partial^2 z}{\partial x^2}$ (Wave Equation).
*   **4. Form the PDE by eliminating arbitrary function from $f(x^2+y^2, z-xy) = 0$.**
    *   **Answer**: $xq - yp = x^2 - y^2$.

***

## 2. Linear PDEs (Lagrange's Method)
*   **5. Solve $pz - qz = z^2 + (x+y)^2$.**
    *   **Answer**: $\phi [x+y, \log(x^2+y^2+z^2+2xy) - 2x] = 0$.
*   **6. Solve $2yzp + zxq = 3xy$.**
    *   **Answer**: $\phi(x^2 - 2y^2, 3y^2 - z^2) = 0$. See [[Semester 1/Mathematics/Unit 3/Examples#Example 3: Lagrange's Method - Grouping\|Examples]].
*   **7. Solve $y^2 p - xyq = x(z-2y)$.**
    *   **Answer**: $\phi(x^2+y^2, y(z-y)) = 0$.
*   **8. Solve $2p + q = \frac{z}{y} \sin(x-2y)$.**
    *   **Answer**: $\phi(x-2y, y - z \sin(x-2y)) = 0$. Note: Question text adjusted for clarity based on context.
*   **9. Solve $xzp + yzq = xy$.**
    *   **Answer**: $\phi(x/y, xy - z^2) = 0$.

***

## 3. Separation of Variables
*   **10. Solve $x^2 \frac{\partial u}{\partial x} + y^2 \frac{\partial u}{\partial y} = 0$.**
    *   **Answer**: $u = c e^{k(1/x - 1/y)}$. See [[Semester 1/Mathematics/Unit 3/Examples#Example 6: Separation of Variables - Heat Eq\|Examples]].
*   **11. Solve $4 \frac{\partial u}{\partial x} + \frac{\partial u}{\partial y} = 3u$, given $u(0, y) = 2e^{5y}$.**
    *   **Answer**: $u = 2 e^{-\frac{1}{2}x + 5y}$.

***

## 4. Higher Order Linear PDEs
*   **12. Solve $(D^4 - 2D^2 D'^2 + D'^4)z = 0$.**
    *   **Answer**: $z = \phi_1(x-y) + x\psi_1(x+y) + \dots$ (Check characteristic roots). Roots are $m = \pm 1$ repeated. $z = x\phi_1(x+y) + \phi_2(x+y) + x\psi_1(x-y) + \psi_2(x-y)$.
*   **13. Solve $(D^2 + DD' - 2D'^2)z = 5e^{x+2y}$.**
    *   **Answer**: $z = \phi_1(x+y) + \phi_2(2x-y) - e^{x+2y}$. See [[Semester 1/Mathematics/Unit 3/Examples#Example 5: Higher Order PDE Solution\|Examples]].
*   **14. Solve $(3D^2 + 10DD' + 3D'^2)z = e^{x-y}$.**
    *   **Answer**: C.F. roots from $3m^2+10m+3=0 \implies (3m+1)(m+3)=0$. $z = \phi_1(x-3y) + \phi_2(3x-y) - \frac{1}{4}e^{x-y}$.
*   **15. Solve $(2D^2 + 5DD' - 3D'^2)z = \sin(2x-y)$.**
    *   **Answer**: $z = \phi_1(3x-y) + \phi_2(x+2y) + \frac{1}{5}\sin(2x-y)$.
*   **16. Solve $(D^2 + 3DD' + 2D'^2)z = 84 \cos(x+3y)$.**
    *   **Answer**: $z = \phi_1(x-y) + \phi_2(2x-y) - 3 \cos(x+3y)$.
*   **17. Solve $(2D^2 - 7DD' + 6D'^2)z = x^3 y$.**
    *   **Answer**: $z = \phi_1(2x+y) + \phi_2(3x+2y) + \frac{1}{96}(x^3 8y + 7x)$.
*   **18. Solve $(D^2 - DD' - 2D'^2)z = 16 x e^{2y}$.**
    *   **Answer**: $z = \phi_1(x-y) + \phi_2(2x+y) + \frac{1}{2}(1-4x)e^{2y}$.