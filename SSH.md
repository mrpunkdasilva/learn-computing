Abrir conexão SSH com outra máquina: 

```sh
ssh gjesus@192.168.1.6 -p 2223
```

Mandar do local para o remoto

```sh
scp -r ./Downloads/vampetaco.jpg kassanmoor@34.82.248.149:/home/kassanmoor/teste.jpg
```

Mandar do remoto para o local

```sh
scp -r kassanmoor@34.82.248.149:/home/kassanmoor/teste.jpg ./Downloads/vampetaco.jpg 
```

> O -r é para fazer de modo recursivo