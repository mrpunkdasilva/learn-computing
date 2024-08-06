## Propriedades 

### Contradição
É a proposição em que **tudo é falso**, ou seja, na tabela verdade a proposição resulta em tudo sendo falso.

**EXEMPLO:**

| p   | ¬p  | p ^ ¬ p |
| --- | --- | ------- |
| T   | F   | F       |
| T   | F   | F       |
| F   | T   | F       |
| F   | T   | F       |

> Paradoxo X Contradição
> O paradOoxo -> é aquele que ainda pode haver verdade
>  A contradição -> é aquele que não existe verdade, é impossível possuir verdade

### Tautologia
é a proposição em que é **tudo verdadeiro**, ou seja, independente dos valores de entrada (premissas) a proposição sempre resulta em verdadeiro.

**EXEMPLO:**

| p   | ¬p  | p v ¬ p |
| --- | --- | ------- |
| T   | F   | T       |
| T   | F   | T       |
| F   | T   | T       |
| F   | T   | T       |

#### Contingencia
É quando a proposição resulta em **ao menos um verdadeiro**.
Aqui está a tabela-verdade com a formatação em Markdown:

**EXEMPLO:*

| p   | q   | p ∧ q | (p ∧ q) ∨ q |
| --- | --- | ----- | ----------- |
| F   | F   | F     | F           |
| F   | V   | F     | V           |
| V   | F   | F     | F           |
| V   | V   | V     | V           |

### Satisfatibilidade 
Uma **FBF** (Formula Bem Formada) é satisfazivel quando se tem **pelo menos um resultado verdadeiro**.
O problema que vai determinar se um expressão é satisfazivel é chamado de **SAT**.

```
	Tautologia e Contradiçãao = Satisfazivel
	Contradição = Insatisfazivel
```

### Tabelas Verdades dos Operadores
| Conjunção (E) |     |       |
| ------------- | --- | ----- |
| A             | B   | A ∧ B |
| T             | T   | T     |
| T             | F   | F     |
| F             | T   | F     |
| F             | F   | F     |

| Disjunção (OU) |     |       |
| -------------- | --- | ----- |
| A              | B   | A ∨ B |
| T              | T   | T     |
| T              | F   | T     |
| F              | T   | T     |
| F              | F   | F     |

| Condicional (SE...ENTÃO) |         |         |
|--------------------------|---------|---------|
|           A             |    B    |   A → B |
|           T             |    T    |    T    |
|           T             |    F    |    F    |
|           F             |    T    |    T    |
|           F             |    F    |    T    |

| Bicondicional (SE E SOMENTE SE) |     |       |
| ------------------------------- | --- | ----- |
| A                               | B   | A ↔ B |
| T                               | T   | T     |
| T                               | F   | F     |
| F                               | T   | F     |
| F                               | F   | T     |

---

 [05 - Arvore de Formação](05%20-%20Arvore%20de%20Formação.md) <- Anterior | Próximo -> [07 - Relações](07%20-%20Relações.md)