# Processos

O processo em sí é **um programa em execução**.
Seria assim:
- Ao ligar o PC você **abriu** o Chrome para assistir um video, logo podemos dizer que o **Chrome é um processo**, já que é um programa que está em execução.


### Diagrama

```mermaid
mindmap
  root(( Processos ))
	Processo
	  "  Programa em execução  "
	  Componentes
		"  Seção de Texto  "
		"  Atividade atual  "
		"  Contador de Programa  "
		"  Pilha Stack  "
		"  Heap Memória Dinâmica  "

	Representação na Memória
	  "  Seção de Texto 📄  "
	  "  Dados 📁  "
	  "  Heap 🗂  "
	  "  Pilha 🛢  "

	Execução de Processos
	  "  Clique duplo no arquivo  "
	  "  Linha de comando  "

	Estados do Processo
	  "  Novo - Criando  "
	  "  Executando - Rodando  "
	  "  Esperando - WaitinProcessos﻿
Last modified: 23 February 2025
O processo em sí é um programa em execução. Seria assim:

Ao ligar o PC você abriu o Chrome para assistir um video, logo podemos dizer que o Chrome é um processo, já que é um programa que está em execução.

Diagrama﻿
Um processo vai além de apenas códigos em execução está parte é conhecida como section text (seção de texto) isto é um processo possui também:

Atividade atual ⇾ que é representada por um valor do Contador de Programas

Pilha (Stack) de processo ⇾ que contém os dados temporaries do processo:

Endereços de retorno

Variáveis locais

Parametros de metodos

Uma pilha heap-> uma memória alocada dinamicamente, seria o armazenamento que o processo vai precisar enquanto está sendo executado

Representação da estrutura de um processo na memoria:

┌───────────┐
│    🔝max
├───────────┤
│   🛢pilha
├───────────┤
│    🔽
├───────────┤
│   🗂heap
├───────────┤
│   📁dados
├───────────┤
│   📄texto
└───────────┘
Representação de como funcionaria uma chamada do sistema até a alocação do processo na memoria:

Estrutura do processo na memoria
Assim temos que um programa por si só é uma **entidade passiva:

Um arquivo com algumas instruções Já um processo é uma entidade ativa:

Um arquivo com instruções (código) e, além disso, um contador de programa que vai dizer qual a proxima instrução a ser executada Sempre em mente que um processo é um arquivo executavel colocado na memoria

Só um atendo, essa memória que está sendo falada é a memoria RAM, já que estamos falando de alocação dinâmica, mas não só ela acaba trabalhando temos também nesse meio os Registadores e os Caches

Podemos dizer que existem duas formas de subir um processo ou melhor executar um arquivo executavel:

Clique duplo no icone do arquivo

Chamada do nome do arquivo por linha de comando

┌───────────────────────────────────┐
│          🖥️ Executar Arquivo 🖥️
└───────────────────────────────────┘
        │                    │
        ▼                    ▼
┌───────────────┐ ┌───────────────┐
│ 🖱️ Clique Duplo│ │ 💻 Linha Comando
└───────────────┘ └───────────────┘
        │                    │
        ▼                    ▼
┌───────────────────────────────────┐
│            🗄️ Arquivo.exe 🗄️
└───────────────────────────────────┘
Mesmo que um usuario ou varios usuarios executem o mesmo programa em dois processos, ou seja, você abriu duas vezes o Chrome serão criados dois processos distintos, mesmo que os componentes abaixo sejam o mesmo:

Seção de texto

A pilha

Heap

Processos

Estados dos processos﻿
Da chamada de execução do processo até o fechamento do processo, ele passa por alguns estados que são eles:

Novo (new)-> processo sendo criado, ou seja, quando você clica no browser

Executando (running)-> o processo está tendo a seção de texto sendo executada, ou seja, o sistema está fazendo as instruções do texto

Esperado (Waiting)-> o processo está esperando algum evento (como uma entrada ou saida do sistema ou então recebimento de algum sinal)

Pronto (ready)-> o processo está esperando ser atribuído para algum processador

Terminado (Terminated)-> o processo finalizou sua execução

Representação dos estados do processo:

Estados do processo
Esses nomes são arbitrarios, ou seja, podem ou não ser usados em algum sistema operacional, pórem os estados ou seja o que eles significam existem em todos os sistemas operacionais.

Vale ressaltar que apenas um processo pode estar em running (executando) em determinado instante em qualquer processador

Bloco de Controle de Processo﻿
Esse PCB (Process Control Block) é uma tabela onde estão as informações associadas ao processo.

Ele pode ser conhecido também como: bloco de controle da tarefa

Representação do PCB:

┌───────────────────┐
│ estado do processo
├───────────────────┤
│número do processo
├───────────────────┤
│contador de programa
├───────────────────┤
│   registradores
├───────────────────┤
│ limites de memória
├───────────────────┤
│lista de arquivos abertos
├───────────────────┤
│         ...       │
└───────────────────┘
Estado do processo: --> o estado atual do processo vá em Estados do Processo

Contador de programa (program counter)-> o contador é aquele que vai indicar qual o endereço da próxima instrução a ser executada pelo processo

Registradores da CPU--> os registradores são de vaios tipos e funções, eles possuem:

Acumuladores

Registradores de indices

Ponteiros de pilha

Registradores de uso geral

Além de qualquer outra informação

Junto com o contador de programa a informação do estado precisa ser armazenado quando ocorre alguma interrupção, para que ao ser iniciado de novo possar ser executado corretamente.

Representação da troca de um processo para outro na CPU:

Essa é uma outra forma:

Troca cpu processo2
Essa é uma forma mais gostosinha:

Troca cpu processo1
Informações que o PCB possui:

Informação de Escalonamento de CPU--> são usados para o trabalho do **Escalonador**:

Prioridade de escalonamento, define qual processo vai usar mais a CPU, ou melhor, o valor processo tem prioridade de uso da CPU

Informação de gêrencia de memoria-> define as informações de quanta memoria e para qual se destinada o processo, possuindo:

O valor dos registradores de base e limite

As Tabelas de páginas ou tabelas de segmento (vai depender do sistema que está usando)

Informação contábil--> define os dados sobre:

Uso de CPU como: quantidade de CPU e o tempo de leitura a ser utilizado

Limites de tempo

Número da conta

Números de processos ou tarefas

Informações de status de E/S--> define as informações sobre os dispositivos de entrada e saida e sobre arquivos alocados para aquele processo, entre outros:

Dispositivos E/S alocados ao processo

Uma lista de arquivos abertos

Threads﻿
Com o que foi discutido agora, pensemos assim: o modelo empregado até agora foi um processo que trabalha apenas com uma thread, ou seja, isso implica que o processo consegue executar apenas uma unica tarefa por vez, jpa que tem apenas uma unica thread é como se tivesse apenas um único trabalhador.

Assim ,se aplicarmos isso para entender melhor no contexto de um browser, ele só pode abrir uma única aba. já que dentro desse processo só existe uma única thread (trabalhador).

Representação de um modelo single thread:

Single thread
No cenário atual, os sistemas operacionais utiliza uma arquitetura de threads diferente: como existia essa limitação a cerca dos processos então foi criado essa arquitetura voltada a multi-threads que é um processo possuir mais de uma thread. Ou seja, ele consegue fazer mais de uma tarefa por vez.

Representação de um modelo multi thread:

Multi thread
Porem, para isso ocorrer deve haver mudanças estruturais na forma como os processos e outros componentes são organizados:

Para o PCB há uma mudança de que ele é expandido para possuir informações dessas outras threads.

Outras partes do sistemas se alteram

Escalonamento de processos﻿
Objetivo primordial da multiprogramação é ter a capacidade das mulheres de fazer mais de um processo, assim ele parte do principio que deve ter um processo rodando o tempo todo para melhorar o uso da CPU.

Então se tem um objetivo que é o compartilhamento do tempo de uso da CPU entre os processos isto é feito por um outro processo que no qual é um programa que fica rodando o tempo todo assim os programas ficam alternando com uma frequência tão alta que os usuários nem notem essa alternância e consigam interagir com cada programa.

Tal que, para atender a essas demandas precisa que o Escalonador de Processos (Process Scheduler) selecione um programa disponivel (dentro da sua lista de possíveis processos disponíveis), para que ocorra a execução do programa na CPU.

Representação do Escalonador de Processos:

Escalonamento de processos1
Se olharmos para um processador único em um sistema isso não será possivel e o que vai acontecer é que um programa entrara em execução enquanto os outros estarão na fila de espera de execução, até que a CPU esteja disponível para atender a chamada

Exemplo de API Padrão: O bloco de controle de processo no sistema operacional Linux é representado pela estrutura task_struct que consegue representar todas as informações dos processos:

Estado do processo

Informações de escalonamento

Gerência de memória

Lista de arquivos abertos e dispositivos E/S alocados para o processo

Ponteiros para o pai do processo:

O pai do processo é aquele que o criou

E para qualquer um de seus filhos:

São outros processos que são criados pelo processo pai (ou seja, outro processo)

Alguns campos da estrutura:

pid_t pid; // identificador de processo
long state; // estado do processo
unsigned int time_slice; // informação de escalonamento
struct task_struct *parent; // processo pai
struct list_head children; // lista de processos filhos
struct files_struct *files; // informações de arquivos abertos
struct mm_struct *mm; // informações de espaço de endereços
Assim temos que no exemplo, o estado do processo é representado por state, vemos também que nessa estrutura há uma lista duplamente interligada de task_struct E o Kernel mantem um ponteiro para processo ativo no momento (current) para o processo que está sendo executado no momento:

Processo atualmente em execucao
Então se caso mudar o estado do processo o Kernel faria o seguinte: current->state = new_state

Sendo que curren**t é um ponteiro para o processo em execução e alteraria um unico processo que está sendo apontado por current**, lembrando que ele seria uma estrutura do tipo : task_struct por isso poderia ser manipulada desse jeito.

Filas de Escalonamento﻿
Ao programa ser executado e se tornar um programa ele entra para a fila de tarefas (job queue) sendo ela a fila que contem todos os processos do sistema.

Os processos que estão:

Na memoria principal (RAM)

Prontos

E esperando serem chamados para a execução São colocados na fila de prontos (ready queue).

Esta sendo em geral uma lista interligada que possui no cabeçalho ponteiros para o primeiro e ultimo PCB da lista.

Cada PCB possui um ponteiro que indica para o próximo PCB na fila de prontos:

Filas de prontos e filas de dispositivos
Segunda representação:

Fila de pronto e de dispositivos2
A lista de processos esperando por determinado dispositivo de E/S é chamada de: fila de dispositivos ela sendo a fila que vai guardar os processos que já receberam alocação da CPU, mas precisa usar um dispositivo:

Um diagrama de filas, ajuda a entender como o escalonador de processos trabalha com as listas:

Um processo criado inicialmente é colocado na fila de pronto. Ele espera até que vá para a execução (ou seja, até que seja despachado). Quando o processo já recebeu o tempo de CPU, está alocado nela e está executando. Logo então podem ocorrer um desses eventos:

O processo pode fazer uma requisição de um dispositivo de E/S e então ser alocado para a fila de dispositivo (sendo para a fila respectiva a do dispositivo que se requisitou).

O processo pode criar um subprocesso e esperar que ele termine

O processo pode ser removido a força da CPU por uma interrupção e acabar sendo movido de novo para a fila de pronto

Nos dois primeiros casos, os processos passam para o estado de espera para o estado de pronto e depois é colocado de vota na fila de pronto. Esse ciclo se repete até que o processo termine ele então saí de todas as filas que está e a alocação do PCB e seus recursos são removidos.g  "
	  "  Pronto - Ready  "
	  "  Terminado - Finalizado  "

	Bloco de Controle de Processo PCB
	  "  Estado do Processo  "
	  "  Número do Processo  "
	  "  Contador de Programa  "
	  "  Registradores  "
	  "  Limites de Memória  "
	  "  Lista de Arquivos Abertos  "

	Threads
	  "  Single Thread - Apenas uma tarefa  "
	  "  Multi Thread - Múltiplas tarefas simultâneas  "

	Escalonamento de Processos
	  "  Multiprogramação  "
	  "  Compartilhamento de CPU  "
	  "  Escalonador de Processos  "

	Filas de Escalonamento
	  "  Fila de Tarefas - Job Queue  "
	  "  Fila de Prontos - Ready Queue  "
	  "  Fila de Dispositivos - I/O Queue  "

```



Um **processo** vai além de apenas **códigos em execução** está parte é conhecida como **section text** (seção de texto) isto é um processo possui também:
- **Atividade atual** ⇾ que é representada **por um valor do Contador de Programas**
- **Pilha (Stack) de processo** ⇾ que contém os **dados temporaries** do processo:
	- Endereços de retorno
	- Variáveis locais
	- Parametros de metodos
- **Uma pilha heap** -> uma **memória alocada dinamicamente**, seria o armazenamento que o processo vai precisar enquanto está sendo executado

**Representação da estrutura de um processo na memoria:**

```
┌───────────┐
│    🔝max  
├───────────┤
│   🛢pilha 
├───────────┤
│    🔽     
├───────────┤
│   🗂heap  
├───────────┤
│   📁dados 
├───────────┤
│   📄texto 
└───────────┘
```

**Representação de como funcionaria uma chamada do sistema até a alocação do processo na memoria:**

![](EstruturaDoProcessoNaMemoria.png)

Assim temos que um programa por si só é uma **entidade passiva:
- Um arquivo com algumas instruções
Já um processo é uma **entidade ativa**:
- Um arquivo com instruções (código) e, além disso, um **contador de programa** que vai dizer qual a proxima instrução a ser executada
Sempre em mente que um processo é um arquivo executavel colocado na memoria

> Só um atendo, essa memória que está sendo falada é a memoria RAM, já que estamos falando de alocação dinâmica, mas não só ela acaba trabalhando temos também nesse meio os Registadores e os Caches
> {style="note"}

Podemos dizer que existem duas formas de subir um processo ou melhor executar um arquivo executavel:
- **Clique duplo** no icone do arquivo
- **Chamada do nome** do arquivo por linha de comando
```
┌───────────────────────────────────┐
│          🖥️ Executar Arquivo 🖥️   
└───────────────────────────────────┘
        │                    │
        ▼                    ▼
┌───────────────┐ ┌───────────────┐
│ 🖱️ Clique Duplo│ │ 💻 Linha Comando
└───────────────┘ └───────────────┘
        │                    │
        ▼                    ▼
┌───────────────────────────────────┐
│            🗄️ Arquivo.exe 🗄️            
└───────────────────────────────────┘
```

Mesmo que um usuario ou varios usuarios executem **o mesmo programa** em dois processos, ou seja, você abriu duas vezes o Chrome serão criados **dois processos distintos**, mesmo que os **componentes abaixo** sejam o mesmo:
- Seção de texto
- A pilha 
- Heap

---
<a id="EstadosDoProcesso">
 </a>
## Estados dos processos


Da chamada de execução do processo até o fechamento do processo, ele **passa por alguns estados** que são eles:
- **Novo (new)** -> processo sendo **criado**, ou seja, quando você clica no browser
- **Executando (running)** -> o processo  está tendo a seção de texto sendo executada, ou seja, o sistema está **fazendo** as instruções do texto
- **Esperado (Waiting)** -> o processo **está esperando algum evento** (como uma entrada ou saida do sistema ou então recebimento de algum sinal)
- **Pronto (ready)** -> o processo está **esperando ser atribuído** para algum processador
- **Terminado (Terminated)** -> o processo **finalizou** sua execução

**Representação dos estados do processo:**
![](EstadosDoProcesso.png)

> Esses nomes são arbitrarios, ou seja, podem ou não ser usados em algum sistema operacional, pórem os estados ou seja o que eles significam existem em todos os sistemas operacionais.

> Vale ressaltar que apenas **um processo** pode estar em **running**(executando) em determinado instante **em qualquer processador**

---

## Bloco de Controle de Processo 
Esse **PCB (Process Control Block)** é uma tabela onde estão as informações associadas ao processo.
- Ele pode ser conhecido também como: **bloco de controle da tarefa**

**Representação do PCB:**
```
┌───────────────────┐
│ estado do processo
├───────────────────┤
│número do processo 
├───────────────────┤
│contador de programa
├───────────────────┤
│   registradores   
├───────────────────┤
│ limites de memória 
├───────────────────┤
│lista de arquivos abertos
├───────────────────┤
│         ...       │
└───────────────────┘
```

- **Estado do processo**: --> o estado atual do processo vá em [Estados do Processo](#EstadosDoProcesso)
- **Contador de programa (program counter)** -> o contador é aquele que **vai indicar qual o endereço da próxima instrução** a ser executada pelo processo
- **Registradores da CPU** --> os registradores são de vaios tipos e funções, eles possuem:
	- Acumuladores
	- Registradores de indices
	- Ponteiros de pilha 
	- Registradores de uso geral
	- Além de qualquer outra informação
	
Junto com o contador de programa a informação do estado precisa ser armazenado quando ocorre alguma interrupção, para que ao ser iniciado de novo possar ser executado corretamente.

**Representação da troca de um processo para outro na CPU:**
- Essa é uma outra forma:
![](TrocaCPUProcesso2.png)
- Essa é uma forma mais *gostosinha*:
![](TrocaCPUProcesso1.png)

**Informações que o PCB possui:**
- **Informação de Escalonamento de CPU** --> são usados para o trabalho do [**Escalonador]()**: 
	- Prioridade de escalonamento, define qual processo vai usar mais a CPU, ou melhor, o *valor processo tem prioridade de uso da CPU*
- **Informação de gêrencia de memoria** -> define as informações de quanta memoria e para qual se destinada o processo, possuindo:
	- O valor dos *registradores de base e limite*
	- As *Tabelas de páginas ou tabelas de segmento* (vai depender do sistema que está usando)
- **Informação contábil** --> define os dados sobre: 
	- Uso de CPU como: *quantidade de CPU* e o *tempo de leitura* a ser utilizado
	- *Limites* de tempo
	- Número da *conta*
	- Números de *processos* ou *tarefas*
- **Informações de status de E/S** --> define as informações sobre os dispositivos de entrada e saida e sobre arquivos alocados para aquele processo, entre outros:
	- *Dispositivos E/S* alocados ao processo
	- Uma *lista de arquivos abertos* 

---

## Threads

Com o que foi discutido agora, pensemos assim: o modelo empregado até agora foi um processo que trabalha apenas com **uma thread**, ou seja, isso implica que o processo consegue executar apenas uma unica tarefa por vez, jpa que tem apenas uma unica **thread** é como se tivesse apenas um único trabalhador.

Assim ,se aplicarmos isso para entender melhor no contexto de um browser, ele só pode abrir **uma única aba**. já que dentro desse processo só existe **uma única thread (trabalhador)**.

**Representação de um modelo single thread:**
![](SingleThread.png)

No cenário atual, os  **sistemas operacionais** utiliza uma **arquitetura de threads diferente**: como existia essa limitação a cerca dos processos então foi criado essa arquitetura voltada a **multi-threads** que é um processo possuir **mais de uma thread**. Ou seja, ele consegue fazer **mais de uma tarefa por vez**.

**Representação de um modelo multi thread:**
![](MultiThread.png)


Porem, para isso ocorrer deve  haver mudanças estruturais na forma como os processos e outros componentes são organizados:
- Para o PCB há uma mudança de que ele é **expandido para possuir informações dessas outras threads.**
- Outras partes do sistemas se alteram

---
## Escalonamento de processos

Objetivo primordial da multiprogramação é ter a capacidade das mulheres de fazer mais de um processo, assim ele parte do principio que **deve ter um processo rodando o tempo todo para melhorar o uso da CPU**.

Então se tem um objetivo que é o **compartilhamento do tempo de uso da CPU** entre os processos isto é feito por um outro processo que no qual é um programa que fica **rodando o tempo todo assim os programas ficam alternando** com uma frequência tão alta que os **usuários nem notem essa alternância e consigam interagir com cada programa**.

Tal que, para atender a essas demandas precisa que o **Escalonador de Processos** (Process Scheduler) **selecione um programa disponivel** (dentro da sua lista de possíveis processos disponíveis), **para que ocorra a execução do programa na CPU**.

**Representação do Escalonador de Processos:**
![](EscalonamentoDeProcessos1.jpg)

> Se olharmos para um processador único em um sistema isso não será possivel e o que vai acontecer é que um programa entrara em execução enquanto os outros estarão na fila de espera de execução, até que a CPU esteja disponível para atender a chamada
{style="note"}


**Exemplo de API Padrão:**
O bloco de controle de processo no sistema operacional Linux é representado pela estrutura `task_struct` que consegue representar todas as informações dos processos:
- Estado do processo
- Informações de escalonamento
- Gerência de memória
- Lista de arquivos abertos e dispositivos E/S alocados para o processo
- Ponteiros para **o pai do processo**:
	- O pai do processo é aquele que o criou
- E para qualquer um de **seus filhos**:
	- São outros processos que são criados pelo processo pai (ou seja, outro processo)

**Alguns campos da estrutura:**
```c
pid_t pid; // identificador de processo 
long state; // estado do processo  
unsigned int time_slice; // informação de escalonamento 
struct task_struct *parent; // processo pai 
struct list_head children; // lista de processos filhos 
struct files_struct *files; // informações de arquivos abertos 
struct mm_struct *mm; // informações de espaço de endereços
```

Assim temos que no exemplo, o estado do processo é representado por `state`, vemos também que nessa estrutura há uma lista duplamente interligada de `task_struct`
E o **Kernel** mantem **um ponteiro para  processo ativo no momento** (current) para o processo que está sendo executado no momento:

![](ProcessoAtualmenteEmExecucao.png)

Então se caso mudar o estado do processo o Kernel faria o seguinte:  `current->state = new_state`
- Sendo que `curren**t` é um ponteiro para o processo em execução e alteraria um unico processo que está sendo apontado por `current`**, lembrando que ele seria uma estrutura do tipo : `task_struct` por isso poderia ser manipulada desse jeito.

### Filas de Escalonamento
Ao programa ser executado e se tornar um programa ele **entra para a fila de tarefas (job queue)** sendo ela a fila **que contem todos os processos do sistema**.

Os processos que **estão**: 
- Na memoria principal (RAM)
- Prontos
- E esperando serem chamados para a execução
São colocados na **fila de prontos (ready queue)**. 

Esta sendo em geral **uma lista interligada** que possui no cabeçalho **ponteiros para o primeiro e ultimo PCB da lista**.

Cada PCB  possui **um ponteiro que indica para o próximo PCB** na fila de prontos:

- ![](FilasDeProntosEFilasDeDispositivos.png)

**Segunda representação:**

![](FilaDeProntoEDeDispositivos2.png)

A lista de processos esperando por determinado dispositivo de E/S é chamada de: **fila de dispositivos** ela sendo a fila que vai guardar os **processos que já receberam alocação da CPU**, mas precisa usar um dispositivo:

Um **diagrama de filas**, ajuda a entender  como o escalonador de processos trabalha com as listas:

Um **processo criado inicialmente é colocado na fila de pronto**. Ele espera até que vá para a execução (ou seja, **até que seja despachado**).
Quando o processo já recebeu o tempo de CPU, está alocado nela e  está executando. Logo então *podem ocorrer um desses eventos*:
- O processo pode fazer uma **requisição de um dispositivo de E/S** e então ser **alocado para a fila de dispositivo** (sendo para a fila respectiva a do dispositivo que se requisitou).
- O processo **pode criar um subprocesso** e **esperar que ele termine**
- O processo pode ser **removido  a força da CPU por uma interrupção** e acabar sendo **movido de novo para a fila de pronto**

Nos dois primeiros casos, os processos passam para **o estado de espera para o estado de pronto** e depois **é colocado de vota na fila de pronto**. 
Esse ciclo se repete até que o processo termine **ele então saí de todas as filas que está e a alocação do PCB e seus recursos são removidos.**
