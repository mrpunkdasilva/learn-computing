# Barramentos
Barramentos são as **interconecções** dos componentes computacionais.

## Tipos de Barramentos
São divididos em três categorias:
- Estrutura
    - Dados 
    - Endereço
    - Controle
- Hierarquia 
    - Local
    - Sistema
    - Expansão

### Estrutra 
É formado por três tipos seguinbtes de Barrramentos:
```
    CPU   MP  E/S
     |    |    |
--------------------  Barramnto Dados
     |    |    | 
-------------------- Barramento Endereços
     |    |    |
-------------------- Barramento Controle
```

#### Barramento de  Dados 
Esse barramento _interliga o RDM (Registrador de Dados em Memoria) com à memoria principal_, para a **transferencia de instruções** ou **dados a serem executados**.

Sendo um barramento bidirecional: 
    - Já que pode tanto ir dá _CPU a Memoria_, assim realizando uma **operação de escrita**;
    - E também consegue ir dá _Memoria a CPU_, assim realizando uma **operação de leitura**;
 
A **largura do barramento** está diretamente ligado ao **desempenho da máquina**, já que quanto mais envio de dados (bits) maior será a velocidade e poder de processamento, tal que por conjseguencia o desempenho irá aumentar. Os primeiros PCs continham apenas 8 bits de largura do seu barramento, hoje temos algo entorno ou maior que 128 bits

#### Barramento de Endereços 
Feito para interligar a _REM (Registrador de Endereços de Memoria) com a Memoria Principal_ que ir **fazer a transferencia de bits que vão representar endereços de memoria** das **instruções ou dados a serem executados**. 
Tem seu sentido **unidirecional**, já que somente a CPU aciona a memoria principal para fazer operações de leitura e escrita.
     
#### Barramento de Controle
Irá _interligar a UC com os outros componentes_. 
Sendo **bidirecional**, pois consegue enviar sinais de controle para a Memoria e receber dela sinais do tipo wait(espere), para que possa terminar a execução da tarefa para começar outra.

Asssim os **barramentos** compartilha os ados por vias que são fisicas por meio de fios de cobres e conectam todos os componentes.

### Hierarquia de Barramentos
A Hierarquia está ligada a **velocidade** de tráfego desses barramentos.

#### Barramento Local ou Interno
É o barramento mais rápido já que está dentro da área da CPU e funcionando no mesmo tempo do relogio do processador, ou seja, está na mesma velocidade de clock do processador.

#### Barramnto Sistema
Tem por finalidade fazer a conecção entre o barramento local com os outros componentes do sistema, como por exemplo: memoria principal, chache l2, e/s. Ele faz uso do _chipset norte_ da placa-mãe. 

Um Circuito Integrao (chipset) cuida de fazer a integração desse barramento deste modo:

```
      |----------|
      | Placa de |   |-----------|      |------| 
      |  Video   |   | Memoria|  |      | CPU  |
      |---|------|   | Principal |      |--|---|
          |          |-----|-----|         | 
          |                | Barramento    |
          |                | de Memoria    |
          |           |----|--|            |                         
          |-----------| Ponte |------------|
       Barramento     | Norte |   Barramento Externo
         AGPU         |-------|
```

#### Barramento de Expansão (ou E/S)
Sendo o barramento que **interliga os dispositivos de E/S com os outros componentes** do computador. Tal integração ocorre por meio do chipset (circuito integrado) chamado de: **ponte sul**.

```
            
                    
                    Barramento 
           |------|    PCI     |-------|     
           | Pont |------------- Algum |
           | Sul  |            |  E/S  |
           |--|---|            |-------| 
              |  
              | Barramento ATA ou IDE
              |
            |-|------|
            | Disco  |
            | Rigido |
            |--------|
```
> Em Discos Rigidos os dois tipos ATA e IDE podem ser integrados irá variar do tipo de memoria escolhida.

## Slots
Os slots nada mais são que as entradas que os barramentos possuem (asboquinhas que tem na placa-mão para conectar os fios). 
Slots variam de acordo com modelo de placa-mãe.


