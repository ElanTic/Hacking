## Descripcion
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Pistas 
To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
****** 
## Solucion
```
nano level3.py 
```
---
```python

#level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]

for n in pos_pw_list:
        if(hash_pw(n) == correct_pw_hash):
                print(n)


```
---

```
jt@jt-VirtualBox:~/Desktop/seguridad$ python3 level3n.py 
2295
jt@jt-VirtualBox:~/Desktop/seguridad$ python3 level3.py 
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
```
## bandera
picoCTF{m45h_fl1ng1ng_6f98a49f}

## Notas adicionales 

## Referencias