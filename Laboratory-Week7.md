1. **Encontrar o comprimento do arco da curva $f\left(x\right)=\frac{4}{3}x^{3/2}$ no intervalo $[0,1]$.**

$$
f(x)=\frac{4}{3}x^{3/2} \text{ ; } [0, 1] 
$$
$$
\frac{4}{3} \cdot \frac{3}{2} \cdot x^{\frac{3}{2} - {1}}
$$
$$
\frac{12}{6} \cdot x^{\frac{3}{2} - {1}} 
$$
$$
\frac{3}{2} - {1} = \frac{3 - 2}{2} = \frac{1}{2} 
$$
$$
\frac{12}{6} = \frac{12^{\dot{.}2}}{6^{\dot{.}2}} = \frac{6^{\dot{.}3}}{3^{\dot{.}2}} = \frac{2}{1}
$$
$$
f(x) = 2 \times x^{\frac{1}{2}}
$$
$$
L = \int_{0}^{1}\sqrt{ 1 +(x^{\frac{1}{2}})^{2} } dx
$$
$$
(x^{\frac{1}{2}})^{2} = x ^{\frac{2}{2}} = x^{1}
$$
$$
= \int_{0}^{1} \sqrt{ 1 + x } \text{ dx }
$$
$$
= \int(1+x)^{\frac{1}{2}} dx
$$
$$
u = 1 + x \text{ ; } \frac{du}{dx} = 1 \text{ ; } du = dx 
$$
$$
= \frac{u^{\frac{1}{2} + 1}}{\frac{1}{2} + 1} + C
$$
$$
= \frac{u^{\frac{3}{2}}}{\frac{3}{2}} + C = \frac{2}{3} \sqrt{ u^{3} } + C = \frac{2}{3}\sqrt{ (1 + x)^{3} } + C  
$$
$$
L = \frac{2}{3}\sqrt{ (1+x)^{3} } \bracevert_{0}^{1} 
$$
$$
= \frac{2}{3} [\sqrt{ (1 + 1)^{3} } - \sqrt{ (1 - 0)^{3} }] 
$$
$$
\sqrt{ 2^{3} } = \sqrt{ 2 \cdot 4 } = \sqrt{ 2 } \cdot \sqrt{ 4 } = 2 \sqrt{ 2 }
$$
$$
= \frac{2}{3}[\sqrt{ 2^{3} } - \sqrt{ 1 }] = \frac{2}{3}[2\sqrt{ 2 } - 1]
$$
$$
L = \frac{2}{3}[2\sqrt{ 2 } - 1]
$$


2. **Com o método de disco, determine o volume gerado ao rotacionar a função $f(x) = 2$ no intervalo $x=0$ e $x=5$.**
> $$V = \pi \int_{a}^{b}[f(x)]^{2}dx$$ 
$$
V = \pi \int_{0}^{5}[2]^{2}dx
$$
$$V = 4 \pi \int_{0}^{5}dx$$
$$
V = 4 \pi x \bracevert_{0}^{5}
$$
$$
V = 4 \pi [5 - 0]
$$
$$
V = 20 \pi \text{ uv}
$$


3. **Com o método da arruela, determine o volume da região gerada ao rotacionar as funções $f(x) = 9$ e $g(x) = 4$, no intervalo $[0,5]$ no eixo x.**

> $$ V = \pi \int_{a}^{b} [f(x)]^{2} - [g(x)]^{2} dx $$

$$
V = \pi \int_{0}^{5} [9]^{2} - [4^{2}] dx
$$
$$
= \pi \int_{0}^{5} (81 - 16) dx
$$
$$
= \pi \int_{0}^{5} 65 dx
$$
$$
= \int_{0}^{5} 65 dx = 65x \bracevert_{0}^{5} = 65 [5 - 0] = 65 \cdot 5 = 325
$$
$$
V = 325 \pi \text{ uv}
$$


4. **Determine o volume da região gerada ao rotacionar a função $y = x^{2} − 3x + 2$ no eixo x, no intervalo $[1,3]$.**
> $$V = \pi \int_{a}^{b}[f(x)]^{2}dx$$
$$
V = \pi \int_{1}^{3}( x^{2} - 3x + 2  )^{2} dx
$$
$$
( x^{2} - 3x + 2  )^{2} = (x^{2}−3x+2)(x^{2}−3x+2)
$$
$$
= x^{4}−3x^{3}+2x^{2}−3x^{3}+9x^{2}−6x+2x^{2}−6x+4
$$
$$
= x^{4}−6x^{3}+13x^{2}−12x+4
$$
$$
\int_{1}^{3} (x^{4}−6x^{3}+13x^{2}−12x+4)dx
$$
$$
= \frac{ x^{5} }{5} - \frac{6x^{4}}{4} + \frac{13x^{3}}{3} - \frac{12x^{2}} {2}+  4x + C = \frac{x^5}{5} - \frac{3x^4}{2} + \frac{13x^3}{3} - 6x^2 + 4x + C 
$$
$$
\left[ \frac{x^{5}}{5} - \frac{3x^{4}}{2} + \frac{13x^{3}}{3} - 6x^{2} + 4x \right]_{1}^{3}
$$
$$
= \frac{3^{5}}{5} - \frac{3 \cdot 3^{4}}{2} + \frac{13 \cdot 3^{3}}{3} - 6 \cdot 3^{2} + 4 \cdot 3
$$
$$
= \frac{243}{5} - \frac{243}{2} + 39 - 54 + 12 = 48,6 − 121,5 − 3 = 48,6 − 124.5 = −75,9
$$
$$
= \frac{1^{5}}{5} - \frac{3 \cdot 1^{4}}{2} + \frac{13 \cdot 1^{3}}{3} - 6 \cdot 1^{2} + 4 \cdot 1
$$
$$
= \frac{1}{5} - \frac{3}{2} + \frac{13}{3} - 6 + 4
$$
$$
0,2 - 1.5 + 4,33 - 6 + 4 \approx 1,23
$$
$$−75,9 − 1,23 = −77,13$$
$$
V \approx -77.13\pi \text{ uv} 
$$

5. **Com o método da casca, determine o volume do sólido de revolução ao girar a função $f\left(x\right)=\frac{1}{2x}$ $f(x) = 12x$, no eixo $y$, no intervalo onde $x = 1$ e $x = 3$.**

   > $$ V = 2\pi \int_{a}^{b} x \cdot f(x) \, dx $$

$$
V = 2\pi \int_{1}^{3} x \cdot \left( \frac{1}{2x} \right) \, dx
$$

$$
V = 2\pi \int_{1}^{3} \frac{1}{2} \, dx = \pi \int_{1}^{3} 1 \, dx
$$

$$
\int 1 \, dx = x

$$
$$
\int_{1}^{3} 1 \, dx = \left[ x \right]_{1}^{3} = 3 - 1 = 2
$$

$$
V = \pi \cdot 2 = 2\pi
$$

$$V = 2\pi \text{ uv}
$$