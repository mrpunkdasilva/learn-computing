Agora veremos o **calculo proposicional** ou então **álgebra proposicional**.
- Nada mais é que usar as proposições  e conectivos lógicos (operadores booleanos), para manipular elas e conseguir valores.

## Sintaxe
- Define uma representação correta de uma abstração;
- Exemplo:
```
┌───────────────────────────────┐
│ p: Todo humano é mortal.      │
│ q: Sócrates é humano          │
│ p ∧ q (Todo humano é mortal e │
│     Sócrates é humano)        │
└───────────────────────────────┘
```

#### Alguns Operadores Lógicos
```
┌───────────────────────────────┬───────────────┐
│         Operadores Lógicos    │   Símbolos    │
├───────────────────────────────┼───────────────┤
│           Conjunção           │       ∧       │
│           Disjunção           │       ∨       │
│            Negação            │      ¬, ~     │
│          Condicional          │       →       │
│         Bicondicional         │       ↔       │
└───────────────────────────────┴───────────────┘
```

- Exemplo de uso do calculo proposicional:
```
┌───────────────────────────────────────┐
│ (p ∧ q) ∨ (q ∧ ¬r)                    │
└───────────────────────────────────────┘
```


## Semântica
- Define as interpretações possíveis das formulas.
- Exemplo - usaremos a formula anterior:
```
┌─────────┐
│ p ∧ q   │
└─────────┘

- Para que seja verdadeira, as duas proposições devem ser verdadeiras.
```

## Fórmula Bem Formada

- **fbf** ou **wff** ~~(whata fuckin fucking kkkk~~) as formulas bem formadas são aquelas que seguem o uso correto da sintaxe;
- Casos em que são **fbf**:
1. Qualquer letra do alfabeto é uma fbf  
2. Se α é uma fbf, **¬ α** também é.  
3. Se α e β são fbfs, **α ∧ β, α ∨ β, α → β e α <→ β** também  
são.

```
┌───────────────────────────────────────┐
│       Símbolos e cadeia de símbolos   │
└───────────────────────────────────────┘
         ┌───────────────────┐
         │       fbf         │
         └───────────────────┘
           ┌───────────┐
           │ Teoremas  │
           └───────────┘
```


---

[[Regra Formal]] <- Anterior | Próximo -> [[Propriedades e Relações entre fórmulas]]