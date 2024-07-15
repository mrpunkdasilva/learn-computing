## Introdução 

Um **Sistema Operacional** é uma interface que interliga o **hardware** e o **software**, fazendo o gerenciamento dos dois mundos do computador.

> A inexistência, de um **SO** resulta em um impedimento de uma interação natural com o computador.

Como todo grande projeto complexo caímos em uma operação em que deve ser bem definida em como o **SO** irá trabalhar, quais são seus requisitos.

E o **SO** tem algumas funções básicas que é:
- dar partida no sistema
- gerenciar memoria 
- gerenciar dispositivos E/S

--- 
### O que os Sistemas Operacionais fazem
Um **sistema computadorizado** ou só computador, pode ser *dividido em quatro partes*:
- [[Hardware]]
- Sistema Operacional
- [[Programas Aplicativos]]
- [[Usuários]]

##### Hardware
O hardware, quando falo desse componente se trata das **[[Partes Físicas]].** 

> Hardware é aquilo que você chuta

###### Partes Físicas
Tais partes entregam as funcionalidades computacionais básicas:
- [[Unidade Central de Processamento]] (CPU em ingres baby)
- [[Memoria]]
- [09 - IO Devices](09%20-%20IO%20Devices.md)

###### Programas Aplicativos
Tais programas são as partes em que não são físicas e são usados para diversos assuntos. Como: planilhas de textos.

- **[[Programas Aplicativos]]** (Aplicativos)

**Também podemos considerar que um sistema computadorizado é composto por:**

```
										   	
	[0101] |                             | [  ] -> Finge que é um PC
	[010]  |--: Dados        Hardware :--| |==| 
 	[01]   |       |             |       | ----
			       -- Software----
					     |
					     |
					|--------|
					|  WIN95 |
					|--------|     
```



- **Exemplo de Funcionamento de um Sistema Operacional**

```
+---------+   +---------+   +---------+   +---------+
| usuário |   | usuário |   | usuário |   | usuário |
|    1    |   |    2    |   |    3    |   |    n    |
+---------+   +---------+   +---------+   +---------+
     |             |             |             |
     |             |             |             |
   +------------+ +----------+ *----------+  *----------+
   | compilador | | montador | | editor de | | sistema |
   |            | |          | | textos   | | de banco|
   |            | |          | |          | | de dados|
   +------------+ +----------+ +----------+ +--------+
                        |
                        |
                    +----------+
                    | programas|
                    | de sistema|
                    | e aplicat-|
                    | ivos     |
                    +----------+
                        |
                        |
                    +----------+
                    | sistema   |
                    | operacional|
                    +----------+
                        |
                        |
                    +----------+
                    | hardware do|
                    | computador |
                    +----------+
```


---

## Operação do Computador

Ao desligar o computador e ligar, o que será que acontece? Como ele "chama" o Sistema Operacional.
Para  o  computador começar a funcionar ele chama um programa básico, chamado de **boostrap** normalmente está alocado na memoria apenas de leitura (**[ROM]()**) ou então é salva na memoria de somente leitura apagavel programavelmente (**[EEPROM]()**).
Esse programa é conhecido como **([Firmware]())** porque está instalado diretamente no hardware, assim ele inicializa todos os aspectos ddo sistema que vão dos registradores da CPU até a dispositivos e conteúdo na memoria.

Para carregar o SO ele precisa localizar o **[Kernel]()** que é o nucleo do sistema operacional, assim que carregado na memoria do computador ele chama um processo chamado **init** que espera uma interrupção do sistema ou do hardware, os dois casos:
- Se for pelo hardware, ele manda uma interrupção por sinal para a CPU, via normalmente barramento do sistema;
- Se for por software, ele pode fazer de duas maneiras ou chamando o **[system call]()** (chamada do sistema) ou usando o **[monitor call]()** (monitor de chamada) elas são operações especiais execcutadas para realizar a interrupção disparando um sinal para a CPU.
Assim que a CPU  recebe alguma interrupção ela para o que está fazendo:
![](Pasted%20image%2020240712151644.jpg)

E a CPU manda a execução para uma **locação fixa de memoria**, tal locação contem o **endereço inicial** que está localizada a rotina para **atender a essa interrupção.**
Essas **interrupções** podem ser tratadas de diferentes  maneiras e cada computador possui seu proprio mecanimo. Um método simples para isso, seria tratar a transferencia chamando uma rotina generica.

Para dar mais enfoque em velocidade pode ser usada uma **tabela de ponteiros a pontanto para as interrupçõe**s, já que elas devem ser predefinidas. E**ssa tabela é armazenada em memoria baixa**, sendo ela a primeira parte ou locação da memoria.

Esse **vetor de interrupção** vai ser indexado exclusivamente pelo número do dispositivo, forneccido com a requisição da interrupção para gerar o endereço do tratamento da interrupção:
```
┌───────────────────────────────────────────────┐
│                  Interrupção 🔔               │
└───────────────────────────────────────────────┘
   ┌───────────────────────────────────────────┐
   │     CPU manda execução para local         │
   │      fixo na 💾, com endereço da          │
   │     rotina de tratamento. 🏃‍♂️              │
   └───────────────────────────────────────────┘
        ┌───────────────────────────────┐
        │  Diferentes formas de tratar  │
        │   interrupções, cada 🖥️       │
        │   com seu próprio jeito.      │
        └───────────────────────────────┘
             ┌───────────────────────┐
             │    Método simples:    │
             │  Transfere para uma   │
             │   rotina genérica. 🔁 │
             └───────────────────────┘
                  ┌───────────────────────┐
                  │   Método rápido:      │
                  │  📋 Tabela de         │
                  │  ponteiros para       │
                  │  interrupções, em     │
                  │  memória baixa. 🔽    │
                  └───────────────────────┘
                       ┌───────────────────┐
                       │  📋 Vetor usa     │
                       │ 📟 dispositivo    │
                       │ para gerar        │
                       │ endereço do       │
                       │ tratamento. 🔍    │
                       └───────────────────┘
```

A arquitetura de interrupção **precisa salvar o endereço da instrução interrompida**, em projetos:
- Em alguns antigos armazenam o endereço da interrupção de **maneira fixa ou local indexado** por um numero do dispositivo;
- Em arquiteturas modernas, eles armazenam em **pilhas do sistema**;
Se a rotina de interrupção precisar modificar algum estado do processador, por exemplo alterando os valores do **registrador**:
- Ela vai **salvar** o estado atual, explicitamente;
- Depois **carregar** e **restaurar** esse estado para depois **retornar**;
- Em seguida será carregado para o contador de programa o endereço do retorno e o processador que foi interrompido continua como se nada tivesse acontecido

```
    📟 Detecção de Interrupção 📟
               ⬇️
    Verifica o tipo de arquitetura
               ⬇️
       ┌────────────┬─────────────┐
       ⬇️           ⬇️            ⬇️
  Arquiteturas    Arquiteturas    Modernas
    Antigas         Antigas       ⬇️
    ⬇️              ⬇️           Armazena 
 Armazena      Armazena        endereço na 
endereço em    endereço      pilha do 
 local fixo     indexado        sistema
    ⬇️              ⬇️           ⬇️
  Processamento da Interrupção 🔄
               ⬇️
  Salvamento do Estado do Processador 💾
               ⬇️
     ┌─────────────────────────┐
     ⬇️                         ⬇️
Se modificar o estado do   Caso 
 processador               contrário
     ⬇️                         ⬇️
  Salvar o estado atual ⬅️ 📝
     ⬇️                         ⬇️
 Executar a rotina de interrupção 🔄
     ⬇️                         ⬇️
   Restaurar o estado salvo 📂
     ⬇️                         ⬇️
 Carregar o endereço de retorno 📡
  para o contador de programa
     ⬇️                         ⬇️
  Processador continua a execução 🚀
```





---
[Sistemas Operacionais](Sistemas%20Operacionais.md) <- Anterior | Próximo -> [[Capitulo 2]]