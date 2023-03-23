## Descripcion
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.

## Pistas 
****** 
## Solucion
```python
nums = input()
arr = nums.split(" ")
base = int(input())
for i in arr:
	print(chr(int(i,base)), end = "")
	
print()
```
```
jt@jt-VirtualBox:~/Downloads$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
lamp
Please give the 01101100 01100001 01101101 01110000 as a word.
...
you have 45 seconds.....

Input:
lamp
Please give me the  156 165 162 163 145 as a word.
Input:
nurse
Please give me the 636f6e7461696e6572 as a word.
Input:
container
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}

```
## bandera
picoCTF{learning_about_converting_values_00a975ff}

## Notas adicionales 

## Referencias