![alt text](img/Pasted_image_20250322234715.png)

On est sur le server : 

![alt text](img/Pasted_image_20250323002447.png)

Dans les fichiers on a des indices sur le fait que c'est un chat IRC : 

![alt text](img/Pasted_image_20250323002507.png)

Pour se connecter dessus, je vais utiliser l'outil : **HexChat** 

Je le configure mais cela ne fonctionne pas for now 

Ok faut juste prendre l'IP données : 
Mettre a jour le /etc/hosts maybe ?

![alt text](img/Pasted_image_20250323003149.png)

Puis changer le port sur le **HexChat**
![alt text](img/Pasted_image_20250323003128.png)

avec **/list** on a la liste des channels : 
![alt text](img/Pasted_image_20250323003424.png)

Mais le channel secret need une clé  'normal' :D
![alt text](img/Pasted_image_20250323003440.png)

Je join le channel General : 

![alt text](img/Pasted_image_20250323003817.png)

Hum > Avec **Hash-identifier** > il me dit que c'est du MD5
![alt text](img/Pasted_image_20250323010426.png)

Lest find out sur **hashcat** 
![alt text](img/Pasted_image_20250323010508.png)

Nothing, :: 
![alt text](img/Pasted_image_20250323012511.png)

Toujours impossible de mettre un !nickname

---

On peut lister les **membres**
![alt text](img/Pasted_image_20250323012923.png)

On decrypt en refaisant le cryptage !
![alt text](img/Pasted_image_20250323013452.png)
Donc si on poste le message crypter alors on aura le message décrypté en clair 

Mais ce putain de chan IRC me casse les couilles avec son **!nick** !!!!!!!!!!!!!
![alt text](img/Pasted_image_20250323013437.png)
.... je ne vois pas :'()....
