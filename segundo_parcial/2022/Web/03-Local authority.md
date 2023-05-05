## Descripcion
Can you get the flag? Go to this [website](http://saturn.picoctf.net:55983/) and see what you can discover.

## Pistas 
****** 
## Solucion
Inspeccionar http://saturn.picoctf.net:55983/login.php
```
<form action="admin.php" method="post" id="hiddenAdminForm" hidden="">
      <input type="text" name="hash" required="" id="adminFormHash">
</form>
```
Revelar y pegar el hash
```js
if(loggedIn)
{
  document.getElementById('msg').innerHTML = "Log In Successful";
  document.getElementById('adminFormHash').value = "2196812e91c29df34f5e217cfd639881";
  document.getElementById('hiddenAdminForm').submit();
}
```

Forma 2
entrar a secure.js
```js
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```
## bandera
picoCTF{j5_15_7r4n5p4r3n7_a8788e61}
## Notas adicionales 

## Referencias