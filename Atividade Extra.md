Vamos supor que você trabalhe no desenvolvimento de modelos para uma empresa meteorológica e que você precise modelar os dados de temperatura mensal média para a cidade de São Paulo, Brasil. Os dados oficiais são:

| Mês   | Jan  | Fev  | Mar  | Abr  | Mai  | Jun  | Jul  | Ago  | Set  | Out  | Nov  | Dez  |
| ----- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| T(ºC) | 24,2 | 24,5 | 23,7 | 22,2 | 19,5 | 18,7 | 18,3 | 19,2 | 20,3 | 21,6 | 22,1 | 23,6 |

Você deve modelar estes dados segundo a função $T(x) = Acos⁡(B(x−C)) + D$, onde $T(x)$ é a temperatura em graus Celsius e $x$, o número do mês correspondente. As outras constantes são:

- $A$ é a amplitude definida como $A = (T_{max}−T_{min)} / 2$
- $B$ é a divisão do arco completo pelos 12 meses do ano, ou seja, $B = 2 π 12$
- $C$ é o intervalo temporal, ou seja, é igual a unidade.
- $D = T_{min} + A$, onde $A$ é a amplitude definida acima.

A partir destas informações apresente as seguintes soluções:

a) Desenvolva a função de acordo com os dados acima e apresente o gráfico dos dados juntamente com o gráfico da função.

```python
```

![[Atividade Extra.png]]















b) Encontre a taxa de variação da temperatura com relação ao tempo (por mês) e determine os meses aonde temos os pontos críticos (temperaturas máximas e mínimas da série temporal) a partir da função encontrada. Apresentar os cálculos a mão. 

c) Encontre a área da curva da função obtida ao longo dos 12 meses de dados. Apresentar os cálculos a mão. 

