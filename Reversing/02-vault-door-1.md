## Descripcion
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/29b91e638ccbd76aaa8c0462d1c64d8d/VaultDoor1.java)

## Pistas 
****** 
## Solucion
```
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ nano flag.txt 
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ cat flag.txt | sort
password.charAt(00)  == 'd' &&
               password.charAt(01)  == '3' &&
               password.charAt(02)  == '5' &&
               password.charAt(03)  == 'c' &&
               password.charAt(04)  == 'r' &&
               password.charAt(05)  == '4' &&
               password.charAt(06)  == 'm' &&
               password.charAt(07)  == 'b' &&
               password.charAt(08)  == 'l' &&
               password.charAt(09)  == '3' &&
               password.charAt(10) == '_' &&
               password.charAt(11) == 't' &&
               password.charAt(12) == 'H' &&
               password.charAt(13) == '3' &&
               password.charAt(14) == '_' &&
               password.charAt(15) == 'c' &&
               password.charAt(16) == 'H' &&
               password.charAt(17) == '4' &&
               password.charAt(18) == 'r' &&
               password.charAt(19) == '4' &&
               password.charAt(20) == 'c' &&
               password.charAt(21) == 'T' &&
               password.charAt(22) == '3' &&
               password.charAt(23) == 'r' &&
               password.charAt(24) == '5' &&
               password.charAt(25) == '_' &&
               password.charAt(26) == 'f' &&
               password.charAt(27) == 'f' &&
               password.charAt(28) == '6' &&
               password.charAt(29) == '3' &&
               password.charAt(30) == 'b' &&
               password.charAt(31) == '0';
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ cat flag.txt | sort | awk '{print($3)} | tr -d "'" | tr -d "\n"
> ^C
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ cat flag.txt | sort | awk '{print($3)}' | tr -d "'" | tr -d "\n"
d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0;jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ ^C
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ javac VaultDoor1.java 
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ java VaultDoor1
Enter vault password: d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0
Access denied!
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ java VaultDoor1
Enter vault password: picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0}
Access granted.
jt@jt-VirtualBox:~/Desktop/repos/files/reversing$ 

```

## bandera
picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_ff63b0}
## Notas adicionales 

## Referencias