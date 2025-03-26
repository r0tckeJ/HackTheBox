![alt text](img/Pasted_image_20250322114635.png)

nmap : 
![alt text](img/Pasted_image_20250322114811.png)

web : 
![alt text](img/Pasted_image_20250322114743.png)

lets try to DL : index.php 
![alt text](img/Pasted_image_20250322114848.png)

On remarque un truc sympa en bas : 

![alt text](img/Pasted_image_20250322115155.png)
 search:displayname=Downloads&subquery=
 ```python
${window.location.hostname}@${window.location.port}\\3fe1690d955e8fd2a0b282501570e1f4\\resumes\\
```

Essayons de DL ce fichier : 

`wget 94.237.49.230:37891/3fe1690d955e8fd2a0b282501570e1f4/resumes`

![alt text](img/Pasted_image_20250322115354.png)

![alt text](img/Pasted_image_20250322115431.png)


On vois un PDF lets DL it : **Nothing.. fausse route** 
On remonte le parent Directory et on trouve : **resumesS**

![alt text](img/Pasted_image_20250322115534.png)

Stegano sur **PDF** : 

file : 
![alt text](img/Pasted_image_20250322120419.png)

strings : 
![alt text](img/Pasted_image_20250322120355.png)
![alt text](img/Pasted_image_20250322120412.png)

exiftools : 
![alt text](img/Pasted_image_20250322120345.png)

ZIP file hidden ? 
![alt text](img/Pasted_image_20250322120549.png)
NON...

Binwalk : 
![alt text](img/Pasted_image_20250322120715.png)

J'ai DL l'image du baron : >

![alt text](img/Pasted_image_20250322211013.png)

Ya un truc >> faut lire ça : 
![alt text](img/Pasted_image_20250322211950.png)

Ce qui me fait revenir sur le site et.. Juste à aller dans **/configs/client.py**
![alt text](img/Pasted_image_20250322211915.png)![alt text](img/Pasted_image_20250322211925.png)

