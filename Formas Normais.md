# Normalização Formas Normais

A normalização se baseia em dois pilares:

```
				     Formalização
╭──────────────────────────╮───────────────────────────╮
│          Menos           │          Menos            │
│        Dependência       │        Redundância        │
│         ╱    ╲           │         ╱    ╲            │
│        ╱      ╲          │        ╱      ╲           │
│       ╱        ╲         │       ╱        ╲          │
│      ╱          ╲        │      ╱          ╲         │
│     ╱            ╲       │     ╱            ╲        │
│    ╱              ╲      │    ╱              ╲       │
│   ╱                ╲     │   ╱                ╲      │
│  ╱                  ╲    │  ╱                  ╲     │
│ ╱                    ╲   │ ╱                    ╲    │
│╱                      ╲  │╱                      ╲   │
╰──────────────────────────╯───────────────────────────╯
```

Ou seja, a normalizar uma base de dados (tabelas) visa deixar o banco menos: 
- **redundante**   =>  muitas informações iguais 
- **dependência** =>  menos dependência entre tabelas
Assim devemos fazer a verificação (ou seja, a normalização) no modelo lógico.

---


## Formas

### Antes de tudo
Vamos praticar com um exemplo de um sistema para uma universidade

|     | Departamento     |           |
| --- | ---------------- | --------- |
| PK  | COD_DEPARTAMENTO | NUMERO    |
|     | NOM_DEPARTAMENTO | CARACTERE |

|     | Professor           |           |
| --- | ------------------- | --------- |
| PK  | COD_PROFESSOR       | NUMERO    |
|     | NOME_PROFESSOR      | CARACTERE |
|     | SOBRENOME_PROFESSOR | CARACTERE |
|     | STATUS              | BOOLEAN   |
| FK  | COD_DEPARTAMENTO    | NUMERO    |
| PK  | COD_DEPARTAMENTO    | NUMERO    |

|     | Professor           |           |
| --- | ------------------- | --------- |
| PK  | COD_PROFESSOR       | NUMERO    |
|     | NOME_PROFESSOR      | CARACTERE |
|     | SOBRENOME_PROFESSOR | CARACTERE |
|     | STATUS              | BOOLEAN   |
| FK  | COD_DEPARTAMENTO    | NUMERO    |

> No campo `COD_DEPARTAMENTO`dependendo dos requisitos pode ser que um professor faça parte de um ou mais departamento, logo teriamos um atributo multivalorado e esse tipo de atributo não respeita a primeira forma, assim teria que aplicar a **1FN**

|     | Turma         |           |
| --- | ------------- | --------- |
| PK  | COD_TURMA     | NUMERO    |
|     | PERIODO       | CARACTERE |
|     | NUMERO_ALUNOS | NUMERO    |
|     | DATA_INICIO   | DATA      |
|     | DATA_FIM      | DATA      |
| FK  | COD_CURSO     | NUMERO    |

> Na turma também temos uma questão dependendo do requisito, podemos ter varios valores para as datas, assim teriamos um campo multivalorado e como bem sabe deveríamos então aplicar a **1FN** neste campo, isto se nossa regra de negocio pedisse, mas ela não pede então deixaremos, assim como no campo `COD_DEPARTAMENTO`

|     | Curso            |           |
| --- | ---------------- | --------- |
| PK  | COD_CURSO        | NUMERO    |
|     | NOME_CURSO       | CARACTERE |
| FK  | COD_DEPARTAMENTO | NUMERO    |

> Em geral tabelas menores costumam já estar na **1FN**

|     | Aluno           |           |
| --- | --------------- | --------- |
| PK  | RA              | NUMERO    |
|     | NOME_ALUNO      | CARACTERE |
|     | SOBRENOME_ALUNO | CARACTERE |
|     | NOME_RUA        | CARACTERE |
|     | NUMERO_RUA      | NUMERO    |
|     | CEP             | CARACTERE |
|     | STATUS          | BOOLEAN   |
|     | FILIACAO        | CARACTERE |
|     | SEXO            | CARACTERE |
|     | CONTATO         | CARACTERE |
|     | CPF             | CARACTERE |
|     | TELEFONE        | CARCTERE  |
|     | CPF             | CARACTERE |
| FK  | COD_CURSO       | NUMERO    |
| FK  | COD_TURMA       | NUMERO    |

> Tabelas maiores tem mais chances de não estarem nas formas normais

|            | Curso_Disciplina |        |
| ---------- | ---------------- | ------ |
| PK, <br>FK | COD_DISCIPLINA   | NUMERO |
| PK,<br>FK  | COD_CURSO        | NUMERO |

|     | Historico          |        |
| --- | ------------------ | ------ |
| PK  | COD_HISTORICO      | NUMERO |
|     | PERIODO_REALIZACAO | DATA   |
| FK  | RA                 | NUMERO |

---

### Forma 1
Para um tabela atingir a primeira forma normal, deve-se seguir as regras:
- **EXISTE** uma chave primaria
- Somente **POSSUI** valores atomicos (atributos simples) 
- As relações também **NÃO** possui os atributos multivalorados ou relações aninhadas 
	- relações aninhadas são tabela dentro de outras tabelas
- Relação **NÃO** possui atributos compostos

#### Aplicando 
Como na tabela `Aluno` temos o campo `FILIACAO`que por sua vez é um capo que pode guardar mais de um valor, ou seja, filiação diz de quem você é filho e isso resulta em ter um pai e uma mão => dois valores. 
- Logo precisamos desmembrar o campo `FILIACAO` -> por ele ser um campo multivalorado
- Assim deixaremos a tabela na 1FN

E temos o mesmo na tabela `Aluno` no campo `CONTATO`que pode receber tanto email, ou  whatsapp ou outra forma de contato

Agora se olharmos para a tabela `Historico` temos o campo `PERIODO_REALIZACAO` que se refere a data de inicio e fim, ou seja, um campo com dois valores


---

### Forma 2

### Forma 3

