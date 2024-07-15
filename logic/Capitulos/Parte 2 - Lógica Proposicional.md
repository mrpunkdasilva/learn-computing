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