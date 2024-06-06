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

- REM => Registro Em Memoria
- RDM => Registro De Memoria
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



