## Descripcion
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

## Pistas 
****** 
## Solucion
```
wireshark capture.pcap &

Wireshark . Follow UDP Stream (udp.stream eq6) capture.pcap
```
## bandera
picoCTF{StaT31355_636f6e6e}

## Notas adicionales 

## Referencias