
## Intro

Os sistemas computadorizados possuem uma **finalidade principal de executar programas**. Logo, esses programas vão precisar dá memoria, necessariamente estar na memoria, pelo menos em parte para ser executado.

Assim, a importância se dá em que para a execução e armazenamento é preciso não apenas a memoria para armazenamento é preciso de um sistema para gerenciar as questões da memoria.

## Memoria Principal

A memoria, sendo ela uma parte essencial para os sistemas computadorizados.
Sendo que a essência mais básica de uma memoria é ser formada por uma grande seguem cia de **words** e **bytes** , cada uma das partes com seu proprio endereço. 
A **CPU pega as instruções da memoria a partir do valor o contador do programa**.

Tais instruções podem fazer com que:
- Carregamento adicional 
- Alocação em endereços específicos da memoria

Um ciclo comum de execução de instrução, seria:
- **Pega** uma instrução da memoria
- **Decodifica** a instrução e faz os operandos serem buscados na memoria
- Depois de **executar**  a instrução **sobre** os operandos 
- Resultado é **guardado** de volta na memoria

![](CicloComumDeExecucaoDeInstrucaoNaMemoria.drawio%20(1).svg)

> A memoria, ou melhor, a unidade de memoria **vê apenas um fluxo de memoria** e não como são gerados pelo contador de programas, etc


## Hardware básico 

A **memoria principal** e os **registradores embutidos** no proprio processador são as **unicas unidades de armazenamento ligadas diretamente a CPU**, ou seja, somente essas unidades (memorias) conseguem ter acesso diretamente a CPU.

Algumas instruções pegam o **endereço de memoria** como argumentos, mas elas não podem acessar **endereços de disco**. Assim os dados que serão usados pelas instruções em execução, **precisam estar em um dos dispositivos**: memoria principal ou registradores embutidos no processador eles **estando ligados diretamente com a CPU**.

Portanto, caso um dado não esteja lá na memoria, **eles precisaram ser movidos para ela antes da CPU possa fazer algo** com eles.

Registradores internos da CPU **são acessiveis normalmente**  por um **ciclo de clock (rélogio)** da CPU.
Maioria das CPUs podem **decodificar e executar as instruções na velocidade de uma ou mais clock tick**

