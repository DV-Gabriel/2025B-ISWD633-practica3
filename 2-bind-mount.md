# BIND MOUNT
En un bind mount mapeamos (montar) un directorio o archivo específico del sistema de archivos del host con una parte del sistema de ficheros del contenedor.

```
docker run -d --name <nombre contenedor> -v <ruta carpeta host>:<ruta carpeta contenedor> <imagen> 
```
ó
```
docker run -d --name <nombre contenedor> --mount type=bind,source=<ruta carpeta host>,target=<ruta carpeta contenedor> <imagen>
```
- destination, dst, target: La ruta donde se monta el archivo o directorio en el contenedor.
- source, src: El origen del montaje.
  
### En tu computador crear una carpeta llamada nginx y dentro de esta carpeta crea otra llamada html. Como se aprecia en la figura.
![Volúmenes](directorio.PNG)

### Crear un contenedor con la imagen nginx:alpine, mapear todos por puertos, para la ruta carpeta host colocar el directorio en donde se encuentra la carpeta html en tu computador y para la ruta carpeta contenedor: /usr/share/nginx/html (esta ruta se obtiene al revisar la documentación de la imagen)
![Volúmenes](volumen-host.PNG)
<img width="938" height="407" alt="image" src="https://github.com/user-attachments/assets/cb23760a-b695-4bae-b5fb-42a27661440e" />


### ¿Qué sucede al ingresar al servidor de nginx?
Se muestra en el servidor lo que se ingreso en el archivo HTML creado anteriormente.

### ¿Qué pasa con el archivo index.html del contenedor?
Es el archivo que se mostrara en la pagina web, es decir si lo podemos modificar para realizar li que querramos.

### Ir a https://html5up.net/ y descargar un template gratuito, descomprirlo dentro de tu computador en la carpeta html
### ¿Qué sucede al ingresar al servidor de nginx?
Se muestra el template descargado como pagina web.

### Eliminar el contenedor

<img width="919" height="115" alt="image" src="https://github.com/user-attachments/assets/025b8d34-91ac-4ed4-92cc-a77cbab20847" />

como usamos rm al crear el contedor, este se elimino al momento. 

### ¿Qué sucede al crear nuevamente un contenedor montado al directorio definidos anteriormente?
Se vuelve a crear si problemas. 

