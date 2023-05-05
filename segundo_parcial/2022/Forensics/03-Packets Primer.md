## Descripcion
Download the packet capture file and use packet analysis software to find the flag.

-   [Download packet capture](https://artifacts.picoctf.net/c/194/network-dump.flag.pcap)
## Pistas 
****** 
## Solucion
```
 wireshark network-dump.flag.pcap
 
```
Follow TCF Stream (tcp.stream eq 0)

```
p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ c e c c a a 7 f }
```

```
jt@jt-VirtualBox:~/Desktop/repos/files/parciaal2$ echo p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ c e c c a a 7 f } | tr -d " "
picoCTF{p4ck37_5h4rk_ceccaa7f}
```
## bandera
picoCTF{p4ck37_5h4rk_ceccaa7f}
## Notas adicionales 

## Referencias