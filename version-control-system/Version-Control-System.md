![](./Resources/american-pie.gif)
# Git Pie: Aprenda sobre VCS

## Nota do Autor
Olá pessoas, nesse texto irei falar sobre VCS (Sistema de Versionamento de Código, sigla em inglês) ou melhor, como o tema é mais conhecido -  falarei sobre Git.

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

---
#### Tipos
Com tudo que foi falado em mente agora precisamos entender que existem diferentes tipos de versionamentos, em que eles **variam de acordo com a sua arquitetura**.

##### Sistemas Locais 
Esse tipo de sistema é mantido em uma maquina. Por exemplo, Jim vai fazer o versionamento da sua parte do *frontend*, onde ele possui um arquivo de *checkout* que vai servir para conferir/adicionar as versões e um banco de dados (poderia ser um outro arquivo) contento as versões que ele salvou.

> ![[Version-Control-System-sistema-local.png]]
> - Diagrama de um sistema local

##### Sistemas Centralizados
Estes sistemas nascem com a problemática que o Sistema Local trás que é justamente um não compartilhamento simultâneo, já que como no nosso exemplo esses dois teriam problemas de versões já que estarão em computadores diferentes

Mas se usarem um CVCSs (sigla em inglês para Sistemas Centralizados de Controle de Versão), com isso eles **terão um repositório compartilhado em que todas as versões estarão e teremos os clientes que são os dois desenvolvedores.**

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

### Senta que lavem história

![[version-control-system/Resources/the-simpsons-homer.gif]]

Para começar a historia do Git é até bem curta e direta. A comunidade do Linux usava um VCS distribuído chamado **BitKeeper** só que ele é proprietário

Sim, um sistema open source usando um proprietário. Claramente isso era algo que causava um estranhamento na comunidade .

>![[stifler-kiss.gif]]

Que por sua vez chegou ao ápice quando o BitKeeper se tornou pago, logo a comunidade do Linux ficou alerta já que eles teriam que fazer o versionamento do núcleo do Linux em outro sistema.

Assim então a comunidade começou a criar seu próprio VCS que fosse:
- Simples
- Veloz
- Não linear, ou seja, que aceite vários ramos (***branches***) de modificação
- Capaz de lidar com grandes projetos, afinal, Linux é gigante

E assim nasceu o  Git, exatamente em 2005 e até hoje está em evolução sendo um dos VCS mais utilizados em todo o mundo de desenvolvimento de gambiarras (softwares).

> Ou seja, tudo nasceu de uma revolta popular
> 
> 
> ![[cachorro-comuna.png]]

### O básico
Vamos agora entender como o Git funciona internamente. Que por sinal trabalha de forma diferente de outros VCS.

Em um outro VCS ele terá os arquivos e quando houver alteração eles criam uma lista somente  das alterações: 

> ![[Version-Control-System-basico-outros-vcs.png]]

Agora com o Git ele faz diferente, já que vai tirando *snapshots* que são como fotos quando ocorre uma mudança e caso tenha algum arquivo que não foi alterado será guardado uma referencia para ele, assim pode ser recuperado.

> Esta forma que o Git trabalha com os dados é chamada de ***stream of snapshots***
> 
> ![[Version-Control-System-stream-of-snapshots.png]]

### Integridade
No Git todas as operações passam primeiro por uma ***checksum*** (soma de verificações) antes mesmo das alterações serem armazenadas, sendo referenciado por esse mesmo checksum. E para o checksum o Git usa o hash SHA-1.

> Logo:
> - É impossível que algum arquivo seja alterado sem que o Git saiba
> - O SHA-1 é uma sequencia composta de 40 caracteres hexadecimais tal sequencia é calculada pela estrutura de bastas

Este hash estará em todo lugar o Git e ele não guarda o nome do arquivo e sim esse hash.

### Estados 

>![[Version-Control-System-states-of-matter.png]]

Agora vamos para uma das partes cruciais no Git, os estados (states) é como o Git está olhando para os arquivos, ou seja, **como os seus arquivos vão estar**.
Podendo estar em **três estados**:
- **Commited**
- **Modified**
- **Staged**

##### Commited
Commited (comitado) é quando os seus dados estão já armazenados (de forma segura) no teu banco de dados local.

##### Modified
O modified (modificado) significa que teu arquivo foi modificado, mas ainda não foi para o estado commited, ou seja, não foi salvo no banco de dados.

##### Staged
O staged (preparado) é o estado intermediário entre o modificado e o comitado, sendo ele quando você adiciona os arquivos para serem comitados.

Assim temos dois níveis principais:
- Diretório de trabalho
- Área de preparo
- Diretório `.git` que vai ser o repositório ou banco de dados local

> ![[Version-Control-System-fluxodetrabalho.png]]
> Diretórios quando se trabalha com Git

- O diretório de trabalho é só uma cópia  de uma versão do projeto.
- A área de trabalho é um arquivo dentro do diretório `.git` que vai armazenar as informações do seu próximo commit (o que será guardado)
- O diretório `.git` é onde vão ficar os metadados e o banco de dados dos objetos do seu projeto (os snapshots)

###### Fluxo básico

```
Diretorio
de            Area
Trabalho      de Preparo     Repositorio .git 

|--|           |--|          |--| 
|--| --------> |--| -------> |--|
 modified         staged      commited
```

---

### Agora vai 1.0

> ![[jim-american-pie.gif]]

#### Instalação

- Caso for **Windows**: 
	- https://git-scm.com/downloads/win
- Caso for distros **Fedora**: 
```bash
sudo yum install git-all
```
- Caso for distros **Debian**: 
```bash
 sudo apt-get install git-all
```

#### Configuração

##### Você não é o Douglas, eu  sou Douglas:
Agora vamos definir a sua identidade já que é preciso disso porque as informações de usuário e e-mail para carimbar essas credenciais nos *commits*.
- Faça assim:
```console
git config --global user.name "Power Guido"
git config --global user.email jalinrapei@exemplo.br
```

> O `--global` significa que o escopo dessas identificações serão usadas em todos os projetos

##### Definir a ferramenta:
Precisa apenas executar este comando em seu terminal:
```bash
 git config --global core.editor vim
```

##### Pedir um help:
```bash
git help <verb>
git <verb> --help
man git-<verb>
```

---
### Agora vai 2.0 versão final

> ![[nadia-scene-american-pie.gif]]
#### Iniciar o repositório
Devemos o comando abaixo para iniciar o repositório para que o Git consiga ver os arquivos.

- Nisso primeiro acessamos a pasta que é a raiz do repositório, no caso do Jim é o `MilfsGo`, então seria:
```bash
md MilfsGo # Cria a pasta
cd MilfsGo # acessa a pasta
```

- Em seguida já inicia o repositório Git
```bash
git init
```

Assim ele vai criar um subdiretório com algumas informações básicas e um esqueleto do seu projeto.

> Mas ainda o Git não estará monitorando seu projeto ainda.

---
#### Fazendo alterações 
Agora vamos fazer alterações básicas como adicionar um *README* para o projeto.

> README são arquivos geralmente em markdown (.md) para registrar a documentação do repositório com informações importantes como:
> - Nome
> - Descrição
> - Como usar
> - Etc

Vamos agora primeiro verificar o status do nosso repositório, antes de criar o README:
```bash
# Vai exibir o status do repositorio como arquivos motivicados ou no estado de preparo
git status
```

> ![[Version-Control-System-gitstatus.png]]
> Resultado da execução do comando 


**Com isso vamos agora criar o arquivo README:** 
> ![[Pasted image 20241024171253.png]]
> REDME.md

**Fazendo a mesma verificação de statust teremos:**
> ![[Version-Control-System-gitstatus2.png]]

Assim temos o `README.md` na lista "Untracked files" que é quando ele não foi comitado ainda.

**Para isso usaremos um outro comando para adiconar ele ao estado "staged":**
```bash
git add .
```

> ![[Version-Control-System-gitadd.png]]

Note que o comando `add` não retorna nada, mas ele adicionou todos os arquivos ao estado `staged`

> O asterisco serve para indicar que vai ser adicionado todos os arquivos que estão modificado, mas você pode colocar o caminho do arquivo ou o nome, como:
> - `git add README.md`

**Com isso podemos usar o status para ver o que temos:**
> ![[Version-Control-System-gitstatus2-1.png]]

Temos o `README` no estado de `stage`, ou seja, preparado para ser comitado.
Assim podemos finalizar o estado e comitar:

```bash
git commit -m "Adicionando o README"
```

Tome que:
- o argumento `-m` significa que você vai passar uma mensagem
- o que estiver dentro das aspas é a mensagem

Como você pode ver, Jim conseguiu fazer o **commit**.

> ![[Version-Control-System-adicionando-commit.png]]
> **commit** é salvar a alteração no banco de dados (repositório do git) 

**Agora vamos verificar o *log*, usando o comando abaixo:**
```bash
git log
```

**Assim veremos o histórico de commits do repositório:** 
> ![[Version-Control-System-log.png]]
> Quando aparecer está tela, apenas a parte `q` para sair dela

> Log é o registro de algo, neste caso é o log dos commits

**Relembrando o fluxo do que aconteceu:**
> ![[Version-Control-System-fluxo-git.png]]

---
#### Branches
Agora vamos ver sobre *branches* são essenciais para o desenvolvimento quando usamos o Git, uma branch é uma ramificação do repositório, ou seja, é uma copia do independente.

> E usamos elas para conseguirmos colaboração em conjunto, para testarmos alguma funcionalidade que precise estar isolada ainda de estar em uso na aplicação e etc;

Ela é independente pois o que fazemos nela não influencia em uma outra.

> Todo repositório começa com uma branch principal
> - Normalmente é chamada de `main` ou `mater`

**Com isso, Stifler quer ver as branchs que tem no projeto:**
```bash
# Exibira uma lista de todas as branches do repositorio
# E também vai destacar em qual branch você está
git branch -l 
```

> ![[Version-Control-System-git-branch-l.png]]
> - Para sair dessa tela basta apertar `q`
> - A branch com asterisco é a atual

**Agora vamos criar uma branch:**
```bash
git branch nova-branch
```
> ![[Version-Control-System-git-branch.png]]

**Agora veremos as branches criadas:**
> ![[Version-Control-System-git-branch-l-2.png]]

**Logo vamos trocar para essa nova branch:**
```bash
git checkout -m nova-branch
```
- O checkout consegue fazer algumas coisas e uma delas quando passamos o argumento `-m` é para criar uma nova branch baseada na que estamos

> ![[Version-Control-System-git-checkout-b.png]]
> - Fizemos a troca da branch com sucesso

**Para fazer uma troca de branches podemos usar o comando abaixo também:** 
```bash
git switch nova-branch
```

**Agora vamos adicionar um arquivo neste repositorio:**
> ![[Version-Control-System-add-imagens.png]]

**Veremos o status:**
> ![[Version-Control-System-status2.png]]
 
**O arquivo ainda não foi comitado então teremos que fazer isso:**
> ![[Version-Control-System-add3.png]]

Tome como nota que como foi falado as branches são independentes logo o que está na branch `nova-branch` não está na branch `main`. Vamos testar isso trocando de branch:
> ![[Version-Control-System-switch1.png]]

Como o esperado não há a pasta `imagens` na branch `main`:
> ![[Version-Control-System-imagens2.png]]

###### Recapitulando o fluxo
- **Criação de branches:**
> ![[Version-Control-System-fluxo-criacao.png]]
- **Troca de branches**
> ![[Version-Control-System-fluxo-mudanca.png]]

---

##### Juntando tudo
Agora vamos juntar as branches que é fazer um merge (ou seja, mesclar):
![[Version-Control-System-merg.png]]

Isto é o fluxo de mesclagem do repositório, onde estamos em um branch e pegamos o que temos em outra branch e jogamos tudo que ela tem de novo na ramificação atual.
Deveremos usar o comando: 

```bash
git merge nova-branch
```

> ![[Version-Control-System-merge.png]]
> 
> - Conseguimos fazer o merge, agora tudo de novo que tem na segunda branch tem na atual

---
#### Se conectando com o mundo...

> ![[stiflerway.gif]]

Conectar com o "mundo", ou seja, usar repositórios remotos

> Repositórios são todos aqueles que não estão na sua máquina

Para esses repositórios existem sistemas como o **GitLab** que serve para guardarmos nossos repositórios e é onde Jim e Stifler vão guardar o "Milfs Go".

> Assim precisamos fazer uma conta, nisso procure um vídeo no youtube que você acha caso precise

##### Criar Repositório
Com a conta criada, agora precisamos criar um repositório:
1. Clicamos em "New Project"
> ![[Version-Control-System-newproject.png]]
2. Vamos em "Create blank project":
> ![[Version-Control-System-gitlab-2.png]]
3. Definimos informações básicas:
> ![[Version-Control-System-gitlab3.png]]
4. Definir a origem remota:
- Devemos primeiro pegar a url ssh:
> ![[Version-Control-System-gitlab4-1.png]]
 
 -  Depois adicionamos localmente essa origem remota:
```bash
git remote add origin git@gitlab.com:MrNulus/milfsgo.gitdar
```
5. Usar chave SSH 
- Caso não tenha rode o comando:
```bash
ssh-keygen  
```
> ![[Version-Control-System.png]]
- Quando tiver, basta agora pegar a chave:
```bash
# Faça no diretorio raiz
cat .ssh/id_ed25519.pub
```
- Copie a chave que aparece na tela
6. Colocar a chave no GitLab:
> ![[Version-Control-System-ssh-addgitlab.png]]

---
##### Push 
7. Agora vamos fazer um `push`que é emburrar os commits locais para o remoto:
- Como é o primeiro `push` que daremos no GitLab precisamos rodar esses comandos, que vai todas as branches e tags
```bash
git push --set-upstream origin --all
git push --set-upstream origin --tags
```

> ![[Version-Control-System-git-push.png]]

- Depois dessa vez basta usar: 
```bash
# Usado para quando não queremos definir a origem remota e nem a branch
git push
# Para quando definimos tanto a origem quanto a branch
git push origin main
```

- E pronto, agora o Stifler e o Jim tem:
> ![[Version-Control-System-repo-gitlab-sucesso.png]]

---
##### Pull
Agora temos uma ultima questão, como fazemos para pegar as mudanças do repositório remoto (GitLab). Vamos ver isso então:
```bash
# Vai puxar tudo que tem na origem em determinada branch
git pull origin main
```

Como fiz alterações no README lá no GitLab, preciso pegar essas alterações e puxar para minha branch main:
> ![[Version-Control-System-gitlab-5.png]]

Agora vamos pensar em um cenario onde não temos o Repositorio e precisamos clonar ele do GitLab, para isso copiamos a URL:

> ![[Version-Control-System-clone.png]]

- Agora pegamos essa URL e usamos com esse comando:
```bash
git clone <url_clone>
```

> ![[Version-Control-System-clone-2.png]]

---

## Cheat Sheet (Tabela de preguiçoso)

> ![[american-pie-its-not-what-it-looks-like.gif]]

Essa tabela fornece uma visão geral dos principais comandos Git e suas funcionalidades básicas. 

| Comando Git                                | Descrição                                                           |
| ------------------------------------------ | ------------------------------------------------------------------- |
| `git init`                                 | Inicializa um novo repositório Git                                  |
| `git add <arquivo>`                        | Adiciona um arquivo modificado à área de stage                      |
| `git add .`                                | Adiciona todos os arquivos modificados à área de stage              |
| `git commit -m "Mensagem do commit"`       | Cria um novo commit com a mensagem especificada                     |
| `git status`                               | Exibe o status atual do repositório                                 |
| `git log`                                  | Exibe o histórico de commits                                        |
| `git checkout <branch/commit>`             | Navega para a branch ou commit especificado                         |
| `git branch <nome-da-branch>`              | Cria uma nova branch                                                |
| `git merge <branch>`                       | Mescla a branch especificada com a branch atual                     |
| `git push`                                 | Envia os commits locais para o repositório remoto                   |
| `git pull`                                 | Baixa as últimas alterações do repositório remoto                   |
| `git clone <url-do-repositório>`           | Clona um repositório remoto para o computador local                 |
| `git reset HEAD~1`                         | Remove o último commit, mantendo as alterações                      |
| `git revert HEAD`                          | Cria um novo commit desfazendo as alterações do último commit       |
| `git diff`                                 | Exibe as diferenças entre o diretório de trabalho e a área de stage |
| `git rm <arquivo>`                         | Remove um arquivo do repositório                                    |
| `git mv <arquivo-original> <arquivo-novo>` | Renomeia ou move um arquivo no repositório                          |

----

## Links
- GIT-SCM.COM. Git - Documentation. Disponível em: [https://git-scm.com/doc](https://git-scm.com/doc).

- YOUTUBE. YouTube. Disponível em: [https://www.youtube.com/watch?v=un8CDE8qOR8](https://www.youtube.com/watch?v=un8CDE8qOR8). 

- GITLAB. GitLab Documentation. Disponível em: [https://docs.gitlab.com/](https://docs.gitlab.com/).
 
 - GITHUB. Git Cheat Sheet. Disponível em: [https://education.github.com/git-cheat-sheet-education.pdf](https://education.github.com/git-cheat-sheet-education.pdf).

---

## Nota final 
Adeus e até mais, espero que tenha sido útil esse conteúdo.

> ![[horny-trumpet.gif]]