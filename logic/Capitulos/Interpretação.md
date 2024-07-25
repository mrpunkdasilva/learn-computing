Na semantica dos elementos da logica proposicional **é determinada por uma funçãoi binaria total**.
Pense assim: a cada proposição atribuimos apenas **um único valor verdade**: `{T, F}` ou `{0, 1}`

Em portugues mais claro: 
- Interpretação -> é o dominio (conjunto) I
	- tal que os elementos são as formulas e/ou variveis 
- Contradominio -> é o conjunto binario de valores verdades (T, F)
Assim a interpretação estabelece **uma função binaria total** => algo como "muitos para um"
```
|---------|         |---------|
|	p     |-------->|    F    |
|   p ^ q |-------->|    F    | 
|   q     |-------->|    T    |
|---------|         |---------|
```

Então a interpretação é o valor do operador ou  é um valor fixo (valor verdade), sendo uma interpretação de dois tipos possiveis:
- Simbolos Verdades: 
	- `I[True] = T e I[False] = F`
- Simboloes proposicionais:
	- $I[p] \in {T, F}$

> I -> i maiusculo é a representação de interpretação


## Tabela verdade
Para cada proposição numa tabela verdade é necessario duas linhas com valores (Verdadeiro e Falso),  já que toda proposição pode assumir  um desses dois valores.
Logo, se tivermos 2 variaveis (proposições) devo ter 2 linhas para cada o que é um total de: 4 linhas
Então podemos resumir isso em uma formula: 
- $L = 2^n$
	- em que n -> é a quantidade de variaveis
	- L -> numero de linhas
	- 2 -> número de valores verdade possiveis (T, F)
	
### Para fazer

1. Fazer a Tabela Verdade  
(a) ( a → b ) → a  
(b) a → (b → a)  
(c) (p ∧ q)∨ r →p∧( q ∨ r)  
(d) A→ ( B → C ) ( A ∧ B)→ C  
(e) ¬(P ∧ Q) ∧ ¬(¬R∧P)∧¬(R∧¬Q)→¬P

---
[[Arvore de Formação]] <- Anterior | Próximo -> [[Regra Formal]]