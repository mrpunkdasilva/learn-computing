# Formas Normais

**Table of Contents**

- [Normalização](#normaliza%C3%A7%C3%A3o)
- [Dependências](#depend%C3%AAncias)
	- [Dependência Funcional](#depend%C3%AAncia-funcional)
	- [Dependência Funcional Parcial](#depend%C3%AAncia-funcional-parcial)
	- [Dependência Funcional Transitiva](#depend%C3%AAncia-funcional-transitiva)
- [Formas](#formas)
	- [Antes de tudo](#antes-de-tudo)
	- [Forma 1](#forma-1)
		- [Aplicando](#aplicando)
			- [Tabela Aluno](#tabela-aluno)
			- [Tabela Historico](#tabela-historico)
	- [Forma 2](#forma-2)
		- [Aplicando](#aplicando)
			- [Exemplo:](#exemplo)
			- [Aluno](#aluno)
				- [Telefone](#telefone)
				- [Endereço](#endere%C3%A7o)
	- [Forma 3](#forma-3)
- [Referencias](#referencias)

---
## Normalização

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

Ou seja, a normalização de uma base de dados (tabelas) visa deixar o banco menos: 
- **redundante**   =>  muitas informações iguais 
- **dependência** =>  menos dependência entre atributos
Assim devemos fazer a verificação (ou seja, a normalização) no modelo lógico.

---

## Dependências

As dependências são importantes conceitos que deve ser entendido e se trata daquela musica que o Cirilo canta: *"Não existo longe de você"*;
É a mesma coisa que acontece quando um campo tem dependência em outro
 
![[cirilo2.png]]

### Dependência Funcional

É dito quando tenho um atributo A e um B, tal que o B depende funcionalmente

Nessa dependência um atributo faz com que todos os outros sejam dependentes dele, por exemplo, em uma dependência funcional (DF) de uma entidade (ou tabela) alunos temos: 

Matricula -> Nome
Matricula  -> Sexo
Matricula  -> Celular

Assim, precisamos saber a matricula para saber os atributos Nome, Sexo e Celular do Aluno

> O inverso não funciona, já que sexo, celular e nem nome identifica a matricula do aluno
> ❗Lembre-se que a **Matricula** é um identificador que consegue identificar outros atributos

### Dependência Funcional Parcial

É quando temos uma chave composta e os atributos tem uma dependência por parte da chave.

Por exemplo, para os dados de médicos: 

> CRM + SinglaEstado -> Nome, Sexo, EstadoEmissor
 
Note que a chave composta é: *CRM + SiglaEstado*. E o campo `EstadoEmissor` depende parcialmente da chave composta já que só precisa da `SiglaEstado` 

> :luc_lightbulb: Quando temos apenas uma chave primaria simples, ela não terá dependência funcional parcial

### Dependência Funcional Transitiva

É definido como uma dependência de um atributo não chave com outro atributo não chave.

Exemplo de DFT com dados de alunos:

> Matricula -> Nome, CodCurso, NomeCurso

> Tal que o campo não chave `NomeCurso` depende diretamente do campo não chave `CodCurso` 
> O campo chave neste exemplo é a `Matricula`


---

## Formas
Existem cinco formas e elas são um conjunto de passos para aplicar nas tabelas (modelo lógico).

> :luc_lightbulb: A 4FN e a 5FN não são usadas muito

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

> No campo `COD_DEPARTAMENTO`dependendo dos requisitos pode ser que um professor faça parte de um ou mais departamento, logo teríamos um atributo multivalorado e esse tipo de atributo não respeita a primeira forma, assim teria que aplicar a **1FN**

|     | Turma         |           |
| --- | ------------- | --------- |
| PK  | COD_TURMA     | NUMERO    |
|     | PERIODO       | CARACTERE |
|     | NUMERO_ALUNOS | NUMERO    |
|     | DATA_INICIO   | DATA      |
|     | DATA_FIM      | DATA      |
| FK  | COD_CURSO     | NUMERO    |

> Na turma também temos uma questão dependendo do requisito, podemos ter vários valores para as datas, assim teríamos um campo multivalorado e como bem sabe deveríamos então aplicar a **1FN** neste campo, isto se nossa regra de negocio pedisse, mas ela não pede então deixaremos, assim como no campo `COD_DEPARTAMENTO`

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

|           | Disciplina       |           |
| --------- | ---------------- | --------- |
| PK,<br>FK | COD_DISCIPLINA   | NUMERO    |
|           | NOME_DISCIPLINA  | CARACTERE |
|           | DESCRICAO        | CARACTERE |
|           | NUMERO_ALUNOS    | NUMERO    |
|           | CARGA_HORARIA    | NUMERO    |
| FK        | COD_DEPARTAMENTO | NUMERO    |

|           | Aluno_Disciplina |        |
| --------- | ---------------- | ------ |
| PK,<br>FK | RA               | NUMERO |
| PK,<br>FK | COD_DISCIPLINA   | NUMERO |

|           | Disciplina_Historico |        |
| --------- | -------------------- | ------ |
| PK,<br>FK | RA                   | NUMERO |
| PK,<br>FK | COD_DISCIPLINA       | NUMERO |
|           | NOTA                 | NUMERO |
|           | FREQUENCIA           | NUMERO |

---

### Forma 1

> 🥇 Para estar no 1FN:
> **Tem que ter um atributo único** -> cada tabela deve ter sua PK  

> 	![[FormasNormais-1FN.png]]

> **Não aceitamos fragmentados** -> não ter campos multivalorados ou compostos  e se tiver é só desmembrar os campos 
>	:luc_pen_tool: É como dizia Jack Estripador: Corte sempre em picadinhos 
>	![[FormasNormais-1FN-2.png]]

Para um tabela atingir a primeira forma normal, deve-se seguir as regras:
- **EXISTE** uma chave primaria
- Somente **POSSUI** valores atômicos (atributos simples) 
- As relações também **NÃO** possui os atributos multvalorados ou relações aninhadas 
	- relações aninhadas são tabela dentro de outras tabelas
- Relação **NÃO** possui atributos compostos

#### Aplicando 

##### Tabela Aluno
Como na tabela `Aluno` temos o campo `FILIACAO`que por sua vez é um capo que pode guardar mais de um valor, ou seja, filiação diz de quem você é filho e isso resulta em ter um pai e uma mãe => dois valores. 
- Logo precisamos desmembrar o campo `FILIACAO` -> por ele ser um campo multivalorado
- Assim deixaremos a tabela na 1FN

E temos o mesmo na tabela `Aluno` no campo `CONTATO`que pode receber tanto email, ou  whatsapp ou outra forma de contato. 

No campo `TELEFONE`acontece o mesmo. Já que teremos o telefone residencial e celular

**Assim a nova tabela ficara:**

|     | Aluno                |           |
| --- | -------------------- | --------- |
| PK  | RA                   | NUMERO    |
|     | NOME_ALUNO           | CARACTERE |
|     | SOBRENOME_ALUNO      | CARACTERE |
|     | NOME_RUA             | CARACTERE |
|     | NUMERO_RUA           | NUMERO    |
|     | CEP                  | CARACTERE |
|     | STATUS               | BOOLEAN   |
|     | NOME_MAE             | CARACTERE |
|     | NOME_PAI             | CARACTERE |
|     | SEXO                 | CARACTERE |
|     | EMAIL                | CARACTERE |
|     | WHATSAPP             | CARACTERE |
|     | CPF                  | CARACTERE |
|     | TELEFONE_RESIDENCIAL | CARCTERE  |
|     | TELEFONE_CELULAR     | CARCTERE  |
| FK  | COD_CURSO            | NUMERO    |
| FK  | COD_TURMA            | NUMERO    |

##### Tabela Historico
Agora se olharmos para a tabela `Historico` temos o campo `PERIODO_REALIZACAO` que se refere a data de inicio e fim, ou seja, um campo com dois valores.

Assim a nova tabela ficara:
- Tiramos o campo `PERIODO_REALIZACAO` e adicionamos dois campos:
	- DATA_INICIO
	- DATA_FIM

|     | Historico     |        |
| --- | ------------- | ------ |
| PK  | COD_HISTORICO | NUMERO |
|     | DATA_INICIO   | DATA   |
|     | DATA_FIM      | DATA   |
| FK  | RA            | NUMERO |

---

### Forma 2

 > 🥈 Para estar no 2FN tem que:
 >  **Ser dependente do Spotify PK (Chave Primaria)** -> caso contrario está fora
 > 		![[FormasNormais-2FN-1.png]]


**Regras da 2FN:**
- Estar na 1FN
- Todos os atributos simples são funcionalmente dependentes de todas as partes da chave primaria
- Não deve existir dependência parcial => ou seja. depende da PK e de outro campo
- Atributos não dependem de chaves candidatas

Caso isso não estiver sendo atingido devemos fazer então uma nova tabela para os dados.

> Um atributo-chave é um que é uma PK (Chave Primaria) ou é a parte de uma Chave Composta 


#### Aplicando

Para aplicar devemos nos perguntar primeiro:

**Tal campo, depende da PK?**
- *Caso positivo, então ta okay*
>![[taokay.png]]
- *Caso negativo, é cilada bino*
> ![[eCiladaBino.png]]

##### Exemplo:
Por exemplo na tabela  `Professor`:
- **Podemos nos perguntar** -> `NOME_PROFESSOR`, `SOBRENOME_PROFESSOR` e `STATUS` depende de `COD_PROFESSOR`?
	- Positivo => logo a tabela `Professor` está na 2FN

|     | Professor           |           |
| --- | ------------------- | --------- |
| PK  | COD_PROFESSOR       | NUMERO    |
|     | NOME_PROFESSOR      | CARACTERE |
|     | SOBRENOME_PROFESSOR | CARACTERE |
|     | STATUS              | BOOLEAN   |
| FK  | COD_DEPARTAMENTO    | NUMERO    |

> Só devemos aplicar essa lógica nos atributos não chave (ou seja. em FK ou PK não aplicamos isso)


#####  Aluno
Os campos `Nome da Rua`, `Numero da Rua` e `CEP`, não pendependem do `RA` do `Alunos`, eles não variam mesmo se o RA variar.

Se olharmos para Telefone_Residencial temos um problema, já que se mudar o RA pode ter a caso do telefone não mudar, então seria melhor colocar em outra tabela;

> ❗ Lembrando que podemos ou não fazer, isto é, o que estamos fazendo é uma convenção:  é melhor fazer mas não é obrigatório

###### Telefone
Para obedecermos a 2FN iremos criar uma tabela para telefones dos alunos e para o tipo de telefone

|     | Telefone_Aluno     |        |
| --- | ------------------ | ------ |
| PK  | COD_TELEFONE_ALUNO | NUMERO |
| FK  | RA                 | NUMERO |
| FK  | COD_TIPO_TELEFONE  | NUMERO |
|     | NUMERO_TELEFONE    | NUMERO |
|     |                    |        |

|     | Tipo_Telefone     |           |
| --- | ----------------- | --------- |
| PK  | COD_TIPO_TELEFONE | NUMERO    |
|     | TIPO_TELEFONE     | CARACTERE |

###### Endereço
Como os campos que são do endereço ficam de forma parcialmente dependente do Aluno logo devemos criar uma tabela para o Endereço.

|     | Endereco_Aluno      |           |
| --- | ------------------- | --------- |
| PK  | COD_ENDERECO_ALUNO  | NUMERO    |
|  FK | RA                  | NUMERO    |
| FK  | COD_TIPO_LOGRADOURO | NUMERO    |
|     | CEP                 | CARACTERE |
|     | NUMERO_RUA          | NUMERO    |
|     | NOME_RUA            | CARACTERE |
|     | COMPLEMENTO         | CARACTERE |

|     | Tipo_Logradouro     |           |
| --- | ------------------- | --------- |
| PK  | COD_TIPO_LOGRADOURO | NUMERO    |
|     | TIPO_LOGRADOURO     | CARACTERE |

**Agora a tabela Aluno ficara assim:**

|     | Aluno           |           |
| --- | --------------- | --------- |
| PK  | RA              | NUMERO    |
|     | NOME_ALUNO      | CARACTERE |
|     | SOBRENOME_ALUNO | CARACTERE |
|     | STATUS          | BOOLEAN   |
|     | NOME_MAE        | CARACTERE |
|     | NOME_PAI        | CARACTERE |
|     | SEXO            | CARACTERE |
|     | EMAIL           | CARACTERE |
|     | WHATSAPP        | CARACTERE |
|     | CPF             | CARACTERE |
| FK  | COD_CURSO       | NUMERO    |
| FK  | COD_TURMA       | NUMERO    |


----

### Forma 3

 > 🥉 Para estar na 3FN tem que:
 >  **A pessoa deve ser dependente do estado (PK) e não de outra pessoa, ou seja não podemos ter atributos comuns que dependem de outros atributos comuns** -> caso contrario está fora;
 >  Ou então pense em classes, a classe dos operários devem ser dependentes dos patrões  e não podem se juntar -> **senão vão para outra tabela**
 > ![[nosso1.png]]

**Regras:**
- Estar na 2FN
- Não existe dependências transitivas
- Nenhuma coluna não chave depender de outra coluna que não é uma chave

> Dependência transitiva -> lembre-se que é quando se tem um atributo que não é PK ou FK  que depende de outro atributo que não é PK e nem FK também

Caso não obedeça devemos criar uma nova tabela.

Como na 2FN, devemos nos perguntar, mas agora a pergunta muda um pouco já que devemos questionar se um atributo simples é dependente de um outro atributo simples, ou seja:

Por exemplo na tabela  `Professor`:
- **Podemos nos perguntar** -> `NOME_PROFESSOR` é dependente de `STATUS`?
	- Vemos que não, já que se o status mudar o nome do professor não muda e vice-versa;

No caso, no exemplo ele já está na terceira forma normal. Então não precisa mexer com mais nada.

---
## Referencias

- https://youtu.be/u6JYYOR_o6E?si=E2MJuCg87PWLMtCF
- https://www.youtube.com/watch?v=-2xK-fkqagI
- https://www.youtube.com/watch?v=XhLmF3-Ew8c
- https://learn.microsoft.com/pt-br/office/troubleshoot/access/database-normalization-description
- https://www.alura.com.br/artigos/normalizacao-banco-de-dados-estrutura?srsltid=AfmBOorWZZuuFq0g6ToGPC2OF-n8TMuQHE0z9QbJ3EXa_qUvSrr554gE