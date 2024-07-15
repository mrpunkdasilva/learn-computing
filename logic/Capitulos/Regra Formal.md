Definem algumas **regras**, para estabelecer conceitos para.

## Conceito Verdade:
Uma [[Proposição]] (premissa) só pode ser valorada em: 
- **Verdadeiro (V) ou Falso (F)**
	- Normalmente -usa em inglês mesmo, o que ficaria:
		- **True ou False: T ou F**
	-  Ou podemos usar de maneira mais universal, **usando 0 e 1**
```
                   ┌───────────────┐
                   │  Proposição   │
                   │   (Premissa)  │
                   └───────────────┘
                            ⬇️
            ┌───────────────────────────────────┐
            │                                   │
            │       Pode ser valorada em:       │
            │                                   │
            └───────────────────────────────────┘
                            ⬇️
       ┌───────────────┬───────────────┬───────────────┐
       │               │               │               │
       │               │               │               │
┌────────────┐   ┌────────────┐   ┌────────────┐   ┌────────────┐
│  Verdade   │   │  Falso     │   │  True      │   │  False     │
│  (V)       │   │  (F)       │   │  (T)       │   │  (F)       │
│  ✅        │   │  ❌        │   │  ✅        │   │  ❌        │
└────────────┘   └────────────┘   └────────────┘   └────────────┘
       ⬇️              ⬇️              ⬇️              ⬇️
 ┌────────────┐   ┌────────────┐   ┌────────────┐   ┌────────────┐
 │    1       │   │    0       │   │    1       │   │    0       │
 │  (Verdade) │   │  (Falso)   │   │  (Verdade) │   │  (Falso)   │
 └────────────┘   └────────────┘   └────────────┘   └────────────┘

```

## Operadores Booleanos:
Eles são **símbolos usados para manipular as proposições**, sendo eles om cada um uma regra especifica.

## Sistema Lógico
Sistema que **representa** as **proposições**, através de **combinação**. Tal sistema usa alguns axiomas:
- Consistencia: não há contradição, duas **premissas verdadeiras** **não devem** gerar uma **conlcusão falsa**;
```
         ╔══════════════════════╗
         ║      Consistência     ║
         ╚══════════════════════╝
                      │
                      │
         ╔══════════════════════╗
         ║ Premissa 1: Verdadeira║
         ╚══════════════════════╝
                      │
                      │
         ╔══════════════════════╗
         ║ Premissa 2: Verdadeira║
         ╚══════════════════════╝
                      │
                      │
         ╔══════════════════════╗
         ║  Conclusão: Verdadeira ║
         ╚══════════════════════╝
```

- Independência: não se pode provar que tal premissa é verdadeira;
```
╔═══════════════════════════════════════════════════════════╗
║                          Independência                    ║
╚═══════════════════════════════════════════════════════════╝
                               │
                               │
          ╔════════════════════════════════════════════════════╗
          ║ Premissa: "Existe vida extraterrestre inteligente" ║
          ║ não pode ser provada como verdadeira.              ║
          ╚════════════════════════════════════════════════════╝
```

- Corretude: se as premissas permitem conclusões, aquelas abertas não tem corretude;
```
╔══════════════════════════════════════════════════════════╗
║                           Corretude                      ║
╚══════════════════════════════════════════════════════════╝
                                         │
                                         │
          ╔══════════════════════════════════════════════╗
          ║ Premissas:                                   ║
          ║   1. Todos os mamíferos têm coluna vertebral.║
          ║   2. Baleias são mamíferos.                  ║
          ║ Conclusão:                                   ║
          ║   Baleias têm coluna vertebral.              ║
          ╚══════════════════════════════════════════════╝
```

- Completude: premissas conclusões verdadeiras;
```
╔══════════════════════════════════════════════════════════╗
║                          Completude                      ║
╚══════════════════════════════════════════════════════════╝
                                         │
                                         │
          ╔═════════════════════════════════════════════╗
          ║ Premissas:                                  ║
          ║   1. Todos os seres humanos são mortais.    ║
          ║ Conclusões:                                 ║
          ║   a) João é mortal.                         ║
          ║   b) Maria é mortal.                        ║
          ║   c) Ana é mortal.                          ║
          ║   d) Todos os seres vivos são mortais.      ║
          ╚═════════════════════════════════════════════╝

```


**visão Geral**
```
╔═══════════════╗          ╔═══════════════╗
║ Consistência  ║          ║ Independência ║
╚═══════════════╝          ╚═══════════════╝
   - Sem contradição       - Não se pode provar diretamente
   - Premissas verdadeiras   que a premissa é verdadeira
   não geram conclusão falsa

╔═══════════════╗           ╔═══════════════╗
║   Corretude   ║           ║   Completude  ║
╚═══════════════╝           ╚═══════════════╝
   - Premissas permitem    - Todas as conclusões
     conclusões corretas     verdadeiras são derivadas
   - Todas conclusões       das premissas
     verdadeiras

```


---
[Parte 1 - Lógica Proposicional](Parte%201%20-%20Lógica%20Proposicional.md) <- Anterior | Próximo -> [[Parte 2 - Lógica Proposicional]]