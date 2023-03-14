## Descripcion
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/37821/` ([link](https://jupiter.challenges.picoctf.org/problem/37821/)) or http://jupiter.challenges.picoctf.org:37821
## Pistas 
****** 
## Solucion
```js
 <script type="text/javascript">
  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') { //1
      if (checkpass.substring(split*6, split*7) == 'a3c8') {//7
        if (checkpass.substring(split, split*2) == 'CTF{') {//2
         if (checkpass.substring(split*4, split*5) == 'ts_p') {//5
          if (checkpass.substring(split*3, split*4) == 'lien') {//4
            if (checkpass.substring(split*5, split*6) == 'lz_1') {//6
              if (checkpass.substring(split*2, split*3) == 'no_c') {//3
                if (checkpass.substring(split*7, split*8) == '9}') { //8
                  alert("Password Verified")
                  }
                }
              }
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
    
  }
</script>
```
## bandera
picoCTF{no_clients_plz_1a3c89} 

## Notas adicionales 

## Referencias