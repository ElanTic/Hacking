## Descripcion
Can you figure out how this program works to get the flag?

Additional details will be available after launching your challenge instance.

The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/528/picker-IV).

## Pistas

## Solucion

```
(gdb) info functions
All defined functions:

Non-debugging symbols:
0x0000000000401000  _init
0x00000000004010e0  putchar@plt
0x00000000004010f0  puts@plt
0x0000000000401100  fclose@plt
0x0000000000401110  printf@plt
0x0000000000401120  fgetc@plt
0x0000000000401130  signal@plt
0x0000000000401140  setvbuf@plt
0x0000000000401150  fopen@plt
0x0000000000401160  __isoc99_scanf@plt
0x0000000000401170  exit@plt
0x0000000000401180  sleep@plt
0x0000000000401190  _start
0x00000000004011c0  _dl_relocate_static_pie
0x00000000004011d0  deregister_tm_clones
0x0000000000401200  register_tm_clones
0x0000000000401240  __do_global_dtors_aux
0x0000000000401270  frame_dummy
0x0000000000401276  print_segf_message
0x000000000040129e  win
--Type <RET> for more, q to quit, c to continue without paging--
0x0000000000401334  main
0x00000000004013d0  __libc_csu_init
0x0000000000401440  __libc_csu_fini
0x0000000000401448  _fini
(gdb) 
(gdb) 
(gdb) 
(gdb) 
(gdb) Q
Undefined command: "Q".  Try "help".
(gdb) q
jt@jt-VirtualBox:~/Desktop/repos/files/P3/picker$ echo 0040129e | nc saturn.picoctf.net 52815
Enter the address in hex to jump to, excluding '0x': You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}
jt@jt-VirtualBox:~/Desktop/repos/files/P3/picker$ 


```
## bandera
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}

## Notas adicionales 

## Referencias