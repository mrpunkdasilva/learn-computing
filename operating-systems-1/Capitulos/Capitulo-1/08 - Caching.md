## Caching
O entendimento de  **caching** é muito importante para entender como sistemas computadorizados funcionam.

Primeiro pensemos que as **informações são armazenadas** em algum **dispositivos de armazenamento** como a memoria principal, assim **conforme são usadas** essas informações elas **são copiadas para uma memoria mais rápida de modo temporário** (que até mesmo a memoria principal).
 - Tal memoria é o -> ***cache***

## Como funciona?
**Primeiro** ao precisarmos de alguma informação **o sistema busca no cache**:
- Se tiver **usamos as informações dali mesmo**.
- Caso não tenha, **o sistema irá carregar a informação de alguma outra memoria lenta** (principal ou mesmo de massa(secundaria)) e em seguida **fara a copia destas informações para a cache de modo temporário**
	-  Para que assim em uma **outra tentativa de achar o dado no cache ele consiga**, isso logo **diminuirá as muitas consultas lentas que seriam feitas usando a memoria principal**.

Indo além, registradores responsaveis por comunicação com a memoria principal como registradores de índice , **o programador ou compilador faz a implementação do algoritmo de alocação e substituição de registradores*.

Esses **algoritmos** servem para **definir quais informações** serão **mantidas nos registradores** e quais **serão mandadas para a memoria principal**.

Também existem  os hardwares voltados para **serem implementados totalmente no hardware**.

A maioria dos sistemas, possui em seu cerne um **cache de instruções** -> voltado para servir de **armazenamento das próximas instruções a serem executadas**.

**Sem isso, a CPU** teria que **levar vários e vários ciclos** para que ela **buscasse na memoria principal** pela **informação da próxima instrução** que **deve ser executada**.

Por essa e outros benefícios, os sistemas (em sua maioria**) possui em sua base vários caches de dados de alta velocidade** -> tal que os caches estão no top #2 da [Hierarquia de Memorias](05%20-%20Types%20of%20Memory.md).

Mas como os caches possuem um **tamanho reduzido** o aspecto de **gerenciamento de cache** se torna **fundamental**. Esse gerenciamento se dá em **alguns aspectos importantes**, como:
- Quanto de **tamanho** o cache terá 
- Qual será sua **politica de substituição** 

Tais aspectos podem **causar um melhor desempenho da memoria** (cache).

**A memoria principal** pode ser vista  **como um cache veloz para o armazenamento secundario**, **porque os dados nessa memoria precisam ser copiados para a memoria principal.**
De modo reciproco, para serem **movidos** para a **memoria secundaria**, precisam **antes estar na memoria principal** (feito isso para a proteção).

O sistema de arquivos vê os dados permanentemente gravados no armazenamento secundario **são vistos de modo hierarquico**, de forma que que existem **diversos niveis na hierarquia*:
- No nivel mais alto ->  o **sistema operaciona**  pode **manter** um **cache do sistema de arquivos na memoria principal**.

Também é **possivel que as memorias RAM como disco de estado solido** (ou então discos eletronicos de RAM) podem ser usados para **armazenamento de alta velocidade**, dos quais **são acessados pela interface do sistema de arquivos**, ou seja, é necessária a comunicação direta com a interface ou melhor o sistema de arquivos.

Temos que a maior parte do **armazenamento terciario** são os **HDs ou SSDs** (pelo menos em 2024 ~~kkkkk~~).


## Niveis e o cache

Os **movimentos** de informações entre os **niveis de hierarquias das memorias** (armazenamento) podem ser de dois tipos: **explicitos** e **implicitos**. De modo que depende apenas da forma como se vai construir o **hardware** e qual é o **software** de controle do sistema operacional.
Podemos exemplificar essa questão:
- A **transferência de dados entre a cahce e a CPU e seus registradores**  -> se dá pelo **hardware**, sem o SO fazer isso.
- A **transferência dos dados dos disco para a memoria (RAM)** -> em geral tem como controlador o **sistema operacional**.

Como nessa estrutura de armazenamento hierarquico, os mesmos dados podem aparecer em diferentes niveis de armazenamento, como por exemplo:
- Supunhetamos que um texto em um arquivo `A` **deverá ser mudado para uma outra palavra que está no arquivo `B`, que reside no HD**
- A operação de mudança  **deve primeiro emitir uma operação de E/S para copiar o bloco de disco de `A` em questão, para a memoria principal.**
- Essa operação é seguida por A sendo **copiado para o cache, registradores internos da CPU**
- Tal que a **cópia de  `A` será vista existente em vários níveis**:
```
Registradores
	|
Cache
	|
Memoria Principal
	|
Memoria Secundaria
```
- Assim que ocorre a mudança nos registradores internos da CPU, os a valores de `A` se **diferem nos outros niveis de armazenamentos, os outros niveis não mudam**
- Após isso, se o **registrador chegar a gravar a mudança no disco rígido**, ou seja, na memoria secundaria **os valores nos niveis serão iguais** (e então a mudança se torna efetiva).


### Threads e cores e sistemas distribuidps
Num ambiente com uma unica threads, ou seja, que executa apenas uma tarefa por vez esse esquema hierárquico todo funciona perfeitamente, já quando o valor é alterado nos registradores ou então o acesso ao disco se torna da seguinte forma:
- Vai do nível mais alto ao baixo numa unica "pista", sem haver nenhum confronto de dados, já que todos os níveis conseguem chegar a se atualizarem pelos valores da unica tarefa sem problema.

Mas quando nos deparamos num sistema multcore, temos que varias threads (tarefa) acessando o mesmo arquivo `A` tem que se torram muito cuidado para que todos os cores consigam pegar os valores de `A` atualizados, senão haverá um extravio dos dados (threads terão valores de `A` diferentes e então será uma bagunça).

Isso se torna mais problemático com um ambiente com multiprocessadores, em que temos um registrador interno tem também caches locais. Assim `A` pode existir em diversos caches de modo simultâneo  e precisa-s que o valor mais recente de `A` seja refletido em todos os núcleos que ele reside.
- Tal situação é chamada de **Coerência de cache** -> tal problema é resolvido de forma baixo nível do sistema operacional, já que é uma questão do hardware

Tudo isso só se torna mais complexo num sistema distribuído, já que diversas a cópias de `A` existem em diversos computadores que estão distribuídos em determinado espaço, logo para resolver essa questão os sistemas deve garantir que as alterações ao arquivo devem ser refletidas nas outras maquinas o mais cedo possível.
- Existem diversas formas de chegar nesse numa solução para esse problema.