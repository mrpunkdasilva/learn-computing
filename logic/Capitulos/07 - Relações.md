# Relações entre fórmulas
Ao estudar as **FBFs** temos relações entre elas.

## Equivalência Lógica
São duas **proposições equivalentes ("iguais"**) => ou seja **possui todas** 
**as interpretações iguais**

$$
A \equiv B
$$
$$I(A \Leftrightarrow B) = T $$
$$\forall I \backslash I[A] = I[B]$$

Ou seja, para todas e **quaisquer interpretações** de $A$ o valor verdade 
será o mesmo que os valores verdades de $B$.


### Equivalências básicas
```
+---------------+---------------+----------------+
| A V B ⇔ B V A  | A Λ B ⇔ B Λ A  | Comutatividade |
+---------------+---------------+----------------+
| (A V B) V C ⇔ | (A Λ B) Λ C ⇔ | Associatividade|
| A V (B V C)    | A Λ (B Λ C)    |                |
+---------------+---------------+----------------+
| A V (B V C) ⇔ | A Λ (B V C) ⇔ | Distributividade|
| (A V B) Λ (A V| (A Λ B) V (A Λ|                |
| C)            | C)            |                |
+---------------+---------------+----------------+
```

**Leis de Morgan**
$\lnot(A \vee B) \equiv \lnot A \wedge \lnot B$
$\lnot(A \wedge B) \equiv \lnot A \vee \lnot B$

## Outras
![](TabelaDeEquivalencias.png)

## Equisatisfatibilidade
É quando tenho duas formulas e o A é satisfazivel (possui pelo menos uma verdade) se e somente se B é satisfazivel.
Ou seja A -> só é satisfazivel quando B for satisfazivel.

**Exemplo:**
$$ \begin{align*} A &: (p \vee q) \\ B &: (p \vee r) \land (q \vee \lnot r) \end{align*} $$

## Consequência Lógica
É quando todas as proposições verdadeiras de B são as de A
- Ou seja, pega A vai o se...então (->) de B e se o resultado der tautologia em todas as interpretações, então é consequência lógica
**Exemplo:**
$$
I(A \to B) = T
$$



---
[06 - Propriedades](06%20-%20Propriedades.md) <- Anterior | Próximo ->  [08.1  - Atributos Tautologias](08.1%20%20-%20Atributos%20Tautologias.md)