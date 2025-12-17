---
{"dg-publish":true,"permalink":"/semester-1/mathematics/unit-4/questions/"}
---


# [Back](../../Mathematics.md)
***
[Core Notes](Core%20Notes.md) | [Examples](Examples.md) | [Questions](Questions.md)

# Unit 4 Questions: Special Functions

## Beta and Gamma Functions
*   **1. Prove Legendre's Duplication Formula: $\Gamma(2p) \sqrt{\pi} = 2^{2p-1} \Gamma(p)\Gamma(p+1/2)$.**
    *   **Answer**: Use $\beta(p, p) = \frac{\Gamma(p)\Gamma(p)}{\Gamma(2p)}$ and $\beta(p, p) = 2 \int_0^{\pi/2} \sin^{2p-1}\theta \cos^{2p-1}\theta d\theta$. Substitute $\sin\theta \cos\theta = \frac{\sin 2\theta}{2}$ and change variables.
*   **2. Prove $\beta(p, 1/2) = 2^{2p-1} \beta(p, p)$.**
    *   **Answer**: Follows from duplication formula relations.
*   **3. Evaluate $\int_0^{\infty} (x^2 + 4) e^{-2x^2} dx$.**
    *   **Answer**: $\frac{17\pi}{8}$. (Separate into $\int x^2 e^{-2x^2}$ and $4 \int e^{-2x^2}$).
*   **4. Evaluate $\int_0^1 \frac{dx}{\sqrt{-\log x}}$.**
    *   **Answer**: $\sqrt{\pi}$. (Put $-\log x = t \implies x = e^{-t}$).
*   **5. Evaluate $\int_0^{\infty} 3^{-4x^2} dx$.**
    *   **Answer**: $\frac{\sqrt{\pi}}{4\sqrt{\log 3}}$.
*   **6. Evaluate $\int_0^1 x^4 (1-x)^3 dx$.**
    *   **Answer**: $\frac{1}{280}$. (Use $\beta(5, 4)$).
*   **7. Evaluate $\int_0^1 x^2 (1-x^5)^{-1/2} dx$.**
    *   **Answer**: $\frac{1}{5} \frac{\Gamma(3/5)\sqrt{\pi}}{\Gamma(1.1)}$ leads to complex form, simple answer in Gamma terms: $\frac{1}{5} \beta(3/5, 1/2)$.
*   **8. Show that $\int_0^{\infty} xe^{-x^2} dx \times \int_0^{\infty} \frac{e^{-x^2}}{\sqrt{x}} dx = \frac{\pi}{2\sqrt{2}}$.**
    *   **Answer**: Compute individual integrals ($\frac{1}{2}$ and $\Gamma(1/4)$ related).

## Bessel Functions
*   **9. Prove that $J_0'(x) = -J_1(x)$.**
    *   **Answer**: Use recurrence relation $\frac{d}{dx}[x^{-p}J_p] = -x^{-p}J_{p+1}$ with $p=0$.
*   **10. Prove that $J_{-1/2}(x) = \sqrt{\frac{2}{\pi x}} \cos x$.**
    *   **Answer**: Expand series with $p=-1/2$.
*   **11. Express $J_5(x)$ in terms of $J_0(x)$ and $J_1(x)$.**
    *   **Answer**: $J_5(x) = (\frac{384}{x^4} - \frac{72}{x^2} + 1)J_1(x) - \frac{192}{x^3}J_0(x) + \frac{12}{x}J_0(x)$ (simplify terms).
    *   Specific Reference Answer from source: $J_5 = (\frac{384}{x^4} - \frac{72}{x^2} + 1)J_1 - (\frac{192}{x^3} - \frac{12}{x})J_0$.
*   **12. Express $J_{-5/2}(x)$ in terms of sine and cosine.**
    *   **Answer**: $J_{-5/2}(x) = \sqrt{\frac{2}{\pi x}} [ \frac{3-x^2}{x^2}\sin x + \frac{3}{x}\cos x ]$.
*   **13. Evaluate $\int_0^{\pi/2} \sqrt{\tan x} \, dx$.**
    *   **Answer**: $\frac{\pi}{\sqrt{2}}$. (Use Beta function $\beta(3/4, 1/4)$).
