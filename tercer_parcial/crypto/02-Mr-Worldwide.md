## Descripcion
A musician left us a [message](https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt). What's it mean?

## Pistas
## Solucion
```
pip install geopy
```

```python
from geopy.geocoders import Nominatim
geolocator = Nominatim(user_agent="picoctf")
lugares = ["35.028309, 135.753082 ", "46.469391, 30.740883 ", "39.758949, -84.191605 ", "41.015137, 28.979530 ", "24.466667, 54.366669 ", "3.140853, 101.693207 ", "9.005401, 38.763611 ", "-3.989038, -79.203560 ", "52.377956, 4.897070 ", "41.085651, -73.858467 ", "57.790001, -152.407227 ", "31.205753, 29.924526 "]
#lugar = input()
for lugar in lugares:
    location = geolocator.reverse(lugar)
    address = location.raw['address']
    print (address.get('city', '') + " or " + address.get('town', ''))
```

```
jt@jt-VirtualBox:~/Desktop/repos/files$ python3 coordinates.py 
京都市 or 
Одеса or 
Dayton or 
İstanbul or Fatih
المَنهَل or 
Kuala Lumpur or 
አዲስ አበባ / Addis Ababa or 
Loja or 
Amsterdam or 
 or Village of Sleepy Hollow
 or Kodiak
الإسكندرية or 
```

```
tomar la primer letra de la ciudad o pueblo
KODIAKALASKA
```
## bandera
picoCTF{KODIAK_ALASKA}

## Notas adicionales 

## Referencias