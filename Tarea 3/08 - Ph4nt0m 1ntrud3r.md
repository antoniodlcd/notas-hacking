## Descripción
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap) and try to get the flag.
## Solución
Usé la herramienta wireshark para visualizar los paquetes, puse un filtro de tiempo y los paquetes con valor positivo incluyendo 0.0 tenían un pedazo de texto cifrado en base 64 al último. Los ordené del más pequeño al más grande y los descifré usando la terminal, lo que me dio la bandera:
```
picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3}
```
## Notas
## Referencias
