# Dispositivos de E/S
Os dispositivos de entrada e saída são os por fazer essa integração da maquina com o humano para que se possa tanto inserir dadose para receber esses dados processados.
Possuindo funções:
- Receber e Enviar informações para o meio
- Converter as informaçõe recebidas e enviadas para possuirem um formato intelegivel para o computador e para o usuario. 

Exemplo: teclado, mouse, hd, ssd, etc

## Classificação de Dispositivos 
### Entrada
Eles entram com os dados, ou seja, um teclado é um dispo. de entrada.

### Saída 
Eles saem com os dados, ou seja, um monitor é um dispo; de saída.

### Entrada e Saída 
Eles são os severinos da vida, fazem tanto a entrada e saída de dados, uma impressdoara se enquandra nesses dispositivos, já que entra com o que se quer imprimir e se tem uma saida daquilo  impresso. 

## Comunicação 
Os E/S precisam se comunicar com a CPU e para isso existem algumas tcnologias de comunicação

### Serial  
- Enviado bita bit. 
```

 Gabinete
-----            --------------
| CPU |----------| Controlador | 
------           | ----------- |         ---------
                 |    Buffer   |--------| Teclado |
                  -------------          --------- 
```
- O controlador também pode ser chamado de `driver`.
- Buffer = é a área que vai armazenar temporariamente e fazer a sincronia de velocidade. 

#### USB
Uma das formas de fazer a comunicação de dispositivos, é o Universal Serial Bus (USB)
possuindo alguns tipos como:
- micro usb: mais lento e comum em carregadores
- usb a: usado de forma super comum em conectar laptops, desktops, etc
- usb c: rapido, carrega pode-se usar os dois lados para carregar, por exemplo
- usb b: usado em impressoras

#### Bluetooth
É uma forma de conexão feita por ondas de rádio , simples, sem fio e rapída.

#### Wi-Fi
Conexão feita por sinais sem fio.


## Gerencia dos Dispositivos 
Eixstem lgumas formas de genciamentop:
- pulling: antiga forma de gerenciamento, ele faz com que a cpu fique constantemente entranto em contarto com os E/S para verificar se estão de boas ou precisando de uma caipirinha.
- interrupção: ele vaideixar a cpu ouvindo um dispositivo e quando tiver terminado vai se interromper o processo
- dma: permite o acesso direto a memoria principal para transferir dados, sem enrolaçõa da CPU em cada processo

