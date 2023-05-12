## Descripcion
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/cd51b2c95be9f3626db6fe6665afb5a3/need-for-speed).
## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ chmod +x need-for-speed 
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ gdb -q need-for-speed 

```


```asm
(gdb) disassemble main
Dump of assembler code for function main:
   0x000055555540091a <+0>:	push   %rbp
   0x000055555540091b <+1>:	mov    %rsp,%rbp
=> 0x000055555540091e <+4>:	sub    $0x10,%rsp
   0x0000555555400922 <+8>:	mov    %edi,-0x4(%rbp)
   0x0000555555400925 <+11>:	mov    %rsi,-0x10(%rbp)
   0x0000555555400929 <+15>:	mov    $0x0,%eax
   0x000055555540092e <+20>:	call   0x5555554008d8 <header>
   0x0000555555400933 <+25>:	mov    $0x0,%eax
   0x0000555555400938 <+30>:	call   0x55555540082f <set_timer>
   0x000055555540093d <+35>:	mov    $0x0,%eax
   0x0000555555400942 <+40>:	call   0x55555540087d <get_key>
   0x0000555555400947 <+45>:	mov    $0x0,%eax
   0x000055555540094c <+50>:	call   0x5555554008ac <print_flag>
   0x0000555555400951 <+55>:	mov    $0x0,%eax
   0x0000555555400956 <+60>:	leave  
   0x0000555555400957 <+61>:	ret    
End of assembler dump.
(gdb) call (int) header()
Keep this thing over 50 mph!
============================

$1 = 2
(gdb) call (int) get_key()
Creating key...
Finished
$2 = 9
(gdb) call (int) print_flag()
Printing flag:
PICOCTF{Good job keeping bus #24c43740 speeding along!}
$3 = 56
(gdb) 
```

## bandera
`PICOCTF{Good job keeping bus #24c43740 speeding along!}
## Notas adicionales 

## Referencias