# Organização do Processador
A **CPU** é responsavel pelo processamento e execução de programas que estão armazenados na **CPU**.  
Sendo dividida em três partes:
1. Unidade Central (UC);
2. Registradores;
3. Unidade Lógica Aritmetica (ULA ou UAL);

Podendo ser dividida em duas partes funcionais:
- Unidade Funcional de Controle;
    - UC
- Unidade Funcional de Processamento;
    - ULA e Registradores

## Diagrama de Funcionamento da CPU

```
           Unidade Funcional de Processamento
  -------                -----------------        
  | ULA |                | Registradores |         
  ---|---                | (RISC e CISC) |         
     |                   -----|--------|--         
     |                        |        |           
     |                        |        |           
==== | ====================== | ====== | =================================
     |     -------------      |        |
     |-----| Barramento |-----|        |     
     |-----|  Interno   |-------|------|--|-----------|O------------|
     |     -------------        |         |           |             |
     |                          |         |           |             | 
     |                          |         |           |             |
==== | ======================== | ======= | ========= | =========== | ====
     |                          |         |      -----|------   ---------
     |                          |         |      | B.       |   | B.    |  
     |----|---------------|   --|--    ---|--    | Endereço |   | Dsdos |
     |    | Decodificador |---| RI |---| CI |    -----|------   ----|---- 
     |    | de Instruções |   -----    ------    REM  |         RDM |
     |----|---------------|                           |             | 
     |                                                |             |
   --|---                                      |------O------|      | 
   | UC |--------------------------------------|   Memoria   O------|
   ------                                      |  Principal  |
                                               |-------------|                                      
        Unidade funcional de Controle                                          

- REM => Registro de Endereços Memoria
- RDM => Registro de Dados Memoria
```

## Unidade Funcional de Processamento
Todo sistema operacional possui uma unica função de existencia, ou seja, o por que dele existir e a função para esses sistemas são: **entrar com dados**, **processar dados**, **saída de dados processados**, assim nasce a Unidade Funcial de Processamento.

Logo a UFP, possui realiza algumas operações básicas:
- Operações Aritmeticas 
- Algebra Booleana
- Movimentação de Dados entre a CPU e a Memoria

### ULA
É a parte central da CPU já que é onde as operações lógicas e aritmeticas irão ser feitas.
Ela não recebe as instruções direto e sim as instruções são processadas pela UC assim que processado é enviado para a ULA que realiza o que se pede e retorna o resultado.

### Registradores
É o tipo de memoria que é rápida e com pouco armazenamento.
Sendo que varia em sua função e quantidade de acordo com o modelo do processador.
A maioria dos processadores utilizam a arquitetura baseada em registratores de processos gerais (RISC/CISC)
- **RISC (Reduced Instructions Set Computer):**
    - Caracterizado pela **simplicidade e eficiéncia** nas execuções de instruções (voltado mais para dispositivos que exigem menos processamento como dispositovs moveis e laptops);

- **CISC (Complex Instructions Set Computer):**
    -Caracterizado por um conjunto de instruções mais **complexas e abrangentes** (voltado para dispositivos que exigem maia poder de processamentos como desktops e servidores);


## Unidade Funcional de Controle
Executa algumas funções:
- Busca de instrução a serem executadas e armazenadas em um registrador da CPU;
- Interpretar as instruçõex para serem envoadas a ULA 
    - Gerar sinais de controle, ao interpretar vai gerar um sinal para a ULA dizendo qual das operações devem ser executadas;

### Contador de Instruções (CI)
O Contador de Instruções é aquele que vai registrar a contagem para sequenciamento das intruções ou seja montar aquela fila de fichas, onde cada ficha possui oum numero de ordem de chamada para que se possa ter o controle das ordens de instruções.

### Registrador de Instruções (RI)
Este Registrador de Instruções possui a função sr armazenar a instrução que deve ser executada para a CPU.

### Decodificador de Instruçôes
O **RI** irá passar uma _sequencia de bits_ representando a instrução a ser executadapara o **Decodificador de Instruções** que por sua vez ira interpretar essa sequencoa de bits e relacionar com a operação qie deve ser feita. Em seguida mandar essa insteução já interpretada para a **UC**, assim ela manda ps sinais necesaarios para a ULA, por exemplo do que deve ser feito.

- Diagrama de funcionamento RI e Decod. Instruc.
```
    ------     _____________      ______
    | UC |o----| Decod.    |o-----| RI |
    ------     | Instrução |      ------
               -------------
```

### RDM e REM
- RDM (Registrador de Dados em Memoria): sendo o registrador que _armazena os dados que estão sendo transmitidos_ da CPU e para a Memoria e vice versa

- REM (Registrador de Endereços de Memoria): sua função é _armazenar o endereço de acesso a memoria_ para que seja necessario a leutura e a escrita da de dasos.

> Ambos os registradores, possuem registro temporario dos dados que são gravados nelas.

```
    --------------
    | Barramento o-----|----------|
    |  Interno   |------|         |
    --------------      |         |
                     ---|---   ---|---
                     | RDM |   | REM |
                     -----|-   ---|---
                          |       |
                         -o-------o-
                         | Memoria |
                         -----------

o =>significa o fluxo de direção os dados
```
