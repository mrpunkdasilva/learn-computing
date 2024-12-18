
# Cálculo da Função \( T(x) = A \cos(B(x - C)) + D \)

## 1. Cálculo da Amplitude (\( A \))
A fórmula para a amplitude é:
$$
A = \frac{T_{\text{max}} - T_{\text{min}}}{2}
$$

- $( T_{\text{max}} = 24,5 \,^\circ\text{C} )$ (temperatura máxima)
- $( T_{\text{min}} = 18,3 \,^\circ\text{C} )$ (temperatura mínima)

Substituindo os valores:
$$
A = \frac{24,5 - 18,3}{2} = \frac{6,2}{2} = 3,1
$$

---

## 2. Cálculo do Fator \( B \)
A fórmula para \( B \) é:
$$
B = \frac{2\pi}{12}
$$

Aqui, \( 12 \) é o número de meses no ano. Calculando:
$$
B = \frac{2\pi}{12} = \frac{\pi}{6} \quad \text{(ou aproximadamente \( 0,5236 \))}
$$

---

## 3. Cálculo do Intervalo Temporal (\( C \))
De acordo com o enunciado:
$$
C = 1
$$

Isso significa que a função começa no primeiro mês (janeiro).

---

## 4. Cálculo do Valor Médio (\( D \))
A fórmula para \( D \) é:
$$
D = T_{\text{min}} + A
$$

Substituímos $( T_{\text{min}} = 18,3 \) e \( A = 3,1 )$:
$$
D = 18,3 + 3,1 = 21,4
$$

---

## 5. Função Final
Agora substituímos os valores calculados (\( A \), \( B \), \( C \), \( D \)) na fórmula geral:
$$
T(x) = A \cos(B(x - C)) + D
$$

Substituindo:
$$
T(x) = 3,1 \cos\left(\frac{\pi}{6}(x - 1)\right) + 21,4
$$

---

## Resumo dos Valores Calculados:
- **Amplitude (\( A \))**: \( 3,1 \)
- **Fator (\( B \))**: \( \frac{\pi}{6} \) ou \( 0,5236 \)
- **Deslocamento (\( C \))**: \( 1 \)
- **Valor Médio (\( D \))**: \( 21,4 \)

Portanto, a função que modela a temperatura média mensal para a cidade de São Paulo é:
$$
T(x) = 3,1 \cos\left(\frac{\pi}{6}(x - 1)\right) + 21,4
$$