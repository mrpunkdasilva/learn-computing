## Modelagem
O que vamos fazer é verificar se a lógica está correto.
Ou seja, transformar para a lógica proposiciona algoque não é e verificar se é SAT (Satisfazivel).

**Vamos usar esse exemplo para entender:**

![](ExemploSatisfatibilidade.png)

Assim, para **verificar** se esses argumentos (o texto acima) possui **satisfatibilidade** temos **alguns passos a seguir:**
1. Definir as proposições
2. Traduzir o texto da Linguagem Natural para a Linguagem Proposicional
3. Realizar a conjunção e resolver a tabela verdade para verificar se é satisfazivel ou não

**Resolvendo:**
1. **Definição**:
![](../Resources/ModelagemLogica/Definição.png)
```
p : João e Jóse tem a mesma idade
q : João é mais velho que Jóse
r : Pedro e João não tem a mesma idade
s : Jão é mais velho que Maria  
```

2.  **Tradução**:
$A = p  \vee  q$
$B = p \to \lnot r$
$C = q \to s$
$D = \lnot r \vee s$

3.  **Verificação** -> primeiro devo fazer a conjunção das proposições, caso encontrar um valor verdade ele vai ser SAT:
- Fazendo a conjunção:
$(p  \vee q) \land (p \to \lnot r) \land (p \to s) \land (\lnot r \vee s)$ 

- Fazendo a tabela verdade:

| $p$ | $q$ | $r$ | $s$ | $(\lnot r)$ | $(p  \vee q)$ | $(p \to \lnot r)$ | $(q \to s)$ | $(\lnot r \vee s)$ | F1    |
| --- | --- | --- | --- | ----------- | ------------- | ----------------- | ----------- | ------------------ | ----- |
| T   | T   | T   | T   | F           | T             | F                 | T           | T                  | F     |
| T   | T   | T   | F   | F           | T             | F                 | F           | F                  | F     |
| T   | T   | F   | T   | **T**       | **T**         | **T**             | **T**       | **T**              | **T** |
| T   | T   | F   | F   | T           | T             | T                 | F           | T                  | F     |
| T   | F   | T   | T   | F           | T             | F                 | T           | T                  | F     |
| T   | F   | T   | F   | F           | T             | F                 | T           | F                  | F     |
| T   | F   | F   | T   | **T**       | **T**         | **T**             | **T**       | **T**              | T     |
| T   | F   | F   | F   | **T**       | **T**         | **T**             | **T**       | **T**              | T     |
| F   | T   | T   | T   | **T**       | **T**         | **T**             | **T**       | **T**              | T     |
| F   | T   | T   | F   | F           | T             | T                 | F           | F                  | F     |
| F   | T   | F   | T   | **T**       | **T**         | **T**             | **T**       | **T**              | **T** |
| F   | T   | F   | F   | T           | T             | T                 | F           | T                  | F     |
| F   | F   | T   | T   | F           | F             | T                 | T           | T                  | F     |
| F   | F   | T   | F   | F           | F             | T                 | T           | F                  | F     |
| F   | F   | F   | T   | T           | F             | T                 | T           | T                  | F     |
| F   | F   | F   | F   | T           | F             | T                 | T           | T                  | F     |
