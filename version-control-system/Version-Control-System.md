![](./Resources/american-pie.gif)
# Git Pie: O último Stifler

## Nota do Autor
Olá pessoas, nesse texto irei falar sobre VCS (Sistema de Versionamento de Código, sigla em inglês) ou melhor, como o tema é mais conhecido -  falarei sobre Git.
Já aviso que usarei como analogias uma das maiores franquias de filmes dos últimos tempos, o famigerado: ***American Pie***.

---
## Introdução
Antes de falar sobre o **Git** precisamos entender o que seriam alguns conceitos básicos como Versionamento de Código.

### Versionamento de Código
Versionamento é um conceito muito simples e usado no dia a dia de forma que nem percebemos. Por exemplo:
Estamos em um projeto onde temos dois desenvolvedores:
- **Stifler**
> ![[stifler-dude-no.gif]]
- **Jim**
>![[warm-american-pie.gif]]

Esses dois desenvolvedores estão fazendo o "Milfs Go" uma especie revolucionaria e inovadora, além do tempo sendo um *app* para acharem a "milfs".

>Aqui está uma *milf* para aqueles não habituados com o termo:
>
>![[american-pie-good-stuff.gif]]
>

Assim eles começaram a projetar o aplicativo e vão para a parte prática, Stifler decidiu ficar o *backend* e Jim com o *frontend*, então depois que um deles termina sua *feature* (algo novo no sistema) ele zipa e envia para o outro e assim por diante. Não só isso, eles usam o **Drive** para guardar as versões do software. Além disso possuem uma pasta para as versões corretas e as de teste, tudo em "zip".

Pronto, agora você sabe o que é versionamento de código, é exatamente isto que os dois estão fazendo. Versionar é manipular versões tanto criá-las  como acessa-las.

#### Controle de Versão
Versionamento é o ato de manipular versões, agora o Controle de Versão é um sistema que vai registrar as mudanças tanto num arquivo como em um projeto gigante ao longo do tempo. 

#### Importância
Talvez agora você levante uma questão de o porque aprender "este trem" - como diria um amigo mineiro. Logo, a resposta é simples: esse tipo de ferramenta é essencial para o desenvolvimento já que nos entrega um poder de não somente trabalhar em conjunto de forma assíncrona e sem medo de acabar perdendo o que já foi feito.

#### Tipos
Com tudo que foi falado em mente agora precisamos entender que existem diferentes tipos de versionamentos, em que eles variam de acordo com a sua arquitetura.

##### Sistemas Locais 
Esse tipo de sistema é mantido em uma maquina. Por exemplo, Jim vai fazer o versionamento da sua parte do *frontend*, onde ele possui um arquivo de *checkout* que vai servir para conferir/adicionar as versões e um banco de dados (poderia ser um outro arquivo) contento as versões que ele salvou.

> ![[Version-Control-System-sistema-local.png]]
> - Diagrama de um sistema local

##### Sistemas Centralizados
Estes sistemas nascem com a problemática que o Sistema Local trás que é justamente um não compartilhamento simultâneo, já que como no nosso exemplo esses dois teriam problemas de versões já que estarão em computadores diferentes

Mas se usarem um CVCSs (sigla em inglês para Sistemas Centralizados de Controle de Versão), com isso eles terão um repositório compartilhado em que todas as versões estarão e teremos os clientes que são os dois desenvolvedores

Com isso, temos um grande ponto fraco que é justamente o fato de dependermos de um único servidor, caso o servidor caía, todas as versões iram cair. 

> ![[Version-Control-System-sistema-compartilhado.png]]
> -  Diagrama de um sistema compartilhado

##### Sistemas Distribuídos
Com isso os DVCS (Sistemas de Controle de Versão Distribuídos) se tornam um protagonista, já que os clientes não somente clonam os estados atuais, mas também fazem uma cópia completa de todo o repositório localmente.

Assim temos: 
- Os servidores, que vão guardar as versões e serviram como pilares para centralizar as versões
- Os clientes que se tornam servidores também, já que eles podem pegar tudo do servidor principal

> ![[Version-Control-System-sistemasdistribuidos.png]]
> - Diagrama de um sistema distribuído

---

## Git

### Senta que lavem historia
![[version-control-system/Resources/the-simpsons-homer.gif]]

Para começar a historia do Git é até bem curta e direta. A comunidade do Linux usava um VCS distribuído chamado **BitKeeper** só que ele é proprietario

Sim, um sistema open source usando um proprietário. Claramente isso era algo que causava um estranhamento na comunidade .
>![[stifler-kiss.gif]]

Que por sua vez chegou ao ápice quando o BitKeeper se tornou pago, logo a comunidade do Linux ficou alerta já que eles teriam que fazer o versionamento do núcleo do Linux em outro sistema.

Assim então a comunidade começou a criar seu próprio VCS que fosse:
- Simples
- Veloz
- Não linear, ou seja, que aceite vários ramos (***branchs***) de modificação
- Capaz de lidar com grandes projetos, afinal, Linux é gigante

E assim nasceu o  Git, exatamente em 2005 e até hoje está em evolução sendo um dos VCS mais utilizados em todo o mundo de desenvolvimento.

> Ou seja, tudo nasceu de uma revolta popular
> 
> ![[cachorro-comuna.png]]

### O básico
Vamos agora entender como o Git funciona internamente. Que por sinal trabalha de forma diferente de outros VCS.

Em um outro VCS ele terá os arquivos e quando houver alteração eles criam uma lista somente  das alterações: 

> ![[Version-Control-System-basico-outros-vcs.png]]

Agora com o Git ele faz diferente, já que vai tirando *snapshots* que são como fotos quando ocorre uma mudança e caso tenha algum arquivo que não foi alterado será guardado uma referencia para ele, assim pode ser recuperado.

> Esta forma que o Git trabalha com os dados é chamada de ***stream of snapshots***
> ![[Version-Control-System-stream-of-snapshots.png]]

### Integridade
No Git todas as operações passam primeiro por uma ***checksum*** (soma de verificações) antes mesmo das alterações serem armazenadas, sendo referenciado por esse mesmo checksum. E para o checksum o Git usa o hash SHA-1.

> - Logo, é impossível que algum arquivo seja alterado sem que o Git saiba
> - O SHA-1 é uma sequencia composta de 40 caracteres hexadecimais tal sequencia é calculada pela estrutura de bastas

Este hash estará em todo lugar o Git e ele não guarda o nome do arquivo e sim esse hash.

### Estados 







