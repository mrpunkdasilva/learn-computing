# Arquitetura do Sistema

Agora falaremos da categorização dos sistemas computadorizados que é feita com base no numero de processadores que ele possui isto é falando de computadores de uso geral.

## Sistema mono processador

Esses sistemas como o nome diz, tem um único processador e foi muito utilizado, como PDAs até os mainframes. Assim nestes sistemas contêm uma única CPU que pode realizar diversas instruções de uso geral, assim como os processos do usuário.

> A maioria dos sistema usam um processador de uso especifico, como por exemplo, para processamento gráfico com os controladores gráficos ou como nos mainframes com os processadores de E/S

Esses tipos todos de processadores específicos não executam  processos do usuário e somente executam instruções especificas e limitadas
- Por vezes o sistema operacional controla este componente, pois o sistema envia informações sobre sua próxima tarefa e monitora o seu status

Vamos a um exemplo:
- Um processador controlador de disco recebe uma sequencia de requisições da CPU principal 
- Implementa a sua própria fila de disco e algoritmo de escalonamento

> Com isso temos um alivio da carga de processo do escalonamento de disco que seria jogado para a CPU principal.

O sistema operacional não pode se comunicar com esses processadores que estão em um baixo nivel, como por exemplo, em teclados temos um microprocessador que faz essa conversão de toque na tecla em códigos que serão enviados para a CPU principal. Assim esses processadores realizam suas tarefas anonimas já que não conseguem se comunicar diretamente com o SO.

Assim temos que mesmo com o uso desses processadores o sistema não será visto como multprocessado já que para ser um sistema de processador unico é quando se tem uma unica CPU de uso geral, lembrando que esses processadores foram falados anteiormente são de uso especifico.


## Sistema poli processador
Esse tipo de sistema em que temos mais de um processador, de uso geral, dentro de um mesmo sistema computadorizado tem ganhado cada vez mais espaço por diversas razões o lugar dos sistema mono processador.

Os sistemas multiprocessados, ou também conhecidos como: sistemas paralelos (parallel system) ou sistema fortemente acoplado (tightly coupled system) fazem um compartilhamento perfeito de perifericos, relogio do computador, barramento do computador para vários processadores de modo que a comunicação entre eles é perfeita.

Podemos escalar três grandes vantagens a cerca desse tipo de arquitetura para sistemas:
- Maior vazão:
- Economia de escala:
- Maior confiabilidade: