# Guia Estelar de Programação
<br>

## 🤨 Como funciona a Web?

	web == teia ou rede em tradução livre

É a forma de estruturar a comunicação entre computadores, através da internet.

Ou seja uma ferramenta de troca de informações.

De modo geral, pense assim:
Você está com seu PC (ou, Mac para os finos), e quer assistir aquele clip da Ariana Grande que acabou de lançar.
Assim que fica sabendo desse video, fica louco para ver logo, então, abre o Chrome (sei que você com certeza usa), vai na barra de pesquisa e digita:

	youtube.com

Nesse instante que aperta `enter` em seu teclado, o navegador magicamente se comunica com outras dezenas de maquinas por detras da internet. E em questão de minutos 🎉 você entrou no YouTube. Logo vai para a barra de pesquisa e digita: 

	novo video clip ariana grande

E adivinha senhores (as), em mais uma questão de segundos (se sua provedora não for Vivo), aparecem dezenas de resultados que você proucurava, uma porrada de anuncios e mais varios videos recomendados meio 'sem sentido' 😏.

Deve estar se pergunando: **O que isso tem haver com o assunto principal, ou seja, funcionamento da WEB?**

Simples meu caro ou minha cara, assim que entrar em seu navegador (#TeamChrome) e faz sua pesquisa pela Internet usa protocolos que a Web prové para a troca de informações entre a maquina servidor (`server-side`, ou seja, maquina que tem os arquivos dos sites e sistemas) e a maquina cliente (client-side, ou seja, tua maquina que vai fazer `requisições` a esse servidor e receber respostas do mesmo);


<br>
### @> Glossario

**->** Requisições - são 'pedidos' (ou seja, ações). Que a maquina cliente ou servidor envia um para o outro.

**->** Respostas - chamadas também como 'response', é a resposta do que foi pedido para o client-side ou server-side.

**Todas as request e responses retornam um código de Status, sendo um número de 100 a 510**

- Visite, para saber mais: [https://httpstatusdogs.com/](https://httpstatusdogs.com/)
<br><br><br>


## O que é programar🐱‍💻?

![What is Programming?](./programming.gif)


**Programar, o que é?**

* É entender de Algoritmos
<br>

**Algoritmos** => sequencia de passos lógicos, finitos. Sendo passos a serem sequidos para resolver um problema.

*Exemplos:*

- Levantar da cama

- Beber cafê

- Fritar um ovo
<br>

**Lógica de programação** => é a forma de aplicação dos passos, sendo a construção de Algoritmos.
<br>

**Como o computador pensa/entende:**

- Ele não pensa, mas sim processa e calcula;

- Só recebe ordens;

	- O computador só entende essas ordens, através de uma **Linguagem de Programação**. É a forma como de se comunicar com essas marquinas.

- Você entende o problema e dá as ordens para resolver um problema;
<br>

**Ou seja** => programar é Dar Instruções

- Como uma receita de Bolo ou de muse de maracuja;

- Nessas instruções esão sendo lidas e exibidas informações
	- Sendo de diversos tipos diferentes, sendo esses tipos de dados (data types):
		+ String = cadeia de caracteres (tudo entre aspas: simples, duplas ou mesmo crase);

		+ Numerico = numeros, exp |> 1, 2, 1.2;

		+ Booleano = tipo logico, tendo dois valores possiveis: true ou false;

	!= Lembrando que existem diversos tipos, mas esses são os tipos primitivos tipos (**fundamentais**) de qualquer linguagem. =!

- Ao dar instruções se faz a manipulação de dados;

- Afinal, programar é resolver problemas computacionalmente

	+ Logo entender o problema é sempre a chave, para resolver;

	+ Se não entender o problema, não se resolve;
<br><br><br>


## Por debaixo dos panos da web
Você quer acesssar um site (da Rockeseat), esse seria o que acontece debaixo dos panos:

- [X] **Você digita a URL: https://rocketseat.com.br**

- Utiliza o protocolo HTTP (HyperText Transfer Protocol) - conjunto de regras

	+ Função: trocar mensagens entre computadores;

	+ Mensagm **->** a mensagem é quebrada em diversos pedaços (chuncks);

- E tem a URL (Uniform Resource Locator)

	+ Localizador e identificador de um recurso;

	+ Recurso nesse caso é o proprio site;

- [X] **É iniciada uma linha de comunicação com o protocolo TCP, entre o servidor que possui o recurso e o cliente**

- Cliente 

	+ O computador, dispositivo ou aplicativo.

		- Nesse caso o browser (tua maquina)

- Servidor

	+ Maquina configurada para receber e enviar respostas aos pedidos.

- TCP (Transmissino Control Protocol)

	+ Função: Garantir que os chunks (pacotes) cheguem corretamente ao seu destino.

- [X] **O endereçõ é convertido em um IP (76.76.21.21) através do DNS**

- IP (Internet Protocol)

	+ Função: Endereçamento dos computadores, garantindo um dialogo `universal` entre as maquinas, gerando uma melhor comunicação.

- DNS (Domain Name Servers)
	+ Função: converter um Domínio em um endereço de IP.

- [X] **Seu pedido está percorrendo diversos proxies**

- Proxy
	
	+ Qualquer dispositivo no meio do caminho da comunicação

	+ Modem, Roteador, ou outros computadores

		+ Função: Encaminhamento dos pacotes (chuncks)

- [x] **Seu pedido chega ao servidor**

- [X] **Servidor analisa seu pedido e encaminha uma resposta nesse caso, positiva**

- [X] **O caminho de volta e semelhante do de ida, passando pela linha de comunicação que foi criada**

- [X] **O browser recebe os `chunks` (os pedacinhos) e monta o site para o usúario**

- [X] **Sendo que esse processo acontece diversas vezes já que para cada recurso (nesse caso: html, css, javascript, imagens) é feita uma nova conexão**
