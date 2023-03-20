## Descripcion
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090

## Pistas 
Have you heard of JWT?
****** 
## Solucion
```
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  ilovepico  
)

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.a8E7FfNLdNxsriYIhadtielnLFyrI4kexDXEphhA3CQ


```
## bandera
picoCTF{jawt_was_just_what_you_thought_f859ab2f}

## Notas adicionales 

## Referencias