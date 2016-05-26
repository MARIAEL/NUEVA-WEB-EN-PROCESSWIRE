# NUEVA-WEB-EN-PROCESSWIRE
Nueva página web en servidor (PW, WP)  
#0.- Conectar con putty a nuestro servidor.  
#1.- Descargar el módulo que deseamos.  

NOTA: En los enlaces veremos el comando wget que sirve para descargar un fichero al servidor.

Todos los módulos.  

https://bitnami.com/stack/lamp/modules  

Enlace para Processwire:  

wget https://bitnami.com/redirect/to/100724/bitnami-processwire-2.7.2-1-module-linux-x64-installer.run  

Enlace para Wordpress:  

wget https://bitnami.com/redirect/to/101272/bitnami-wordpress-4.5-1-module-linux-x64-installer.run  


#2.- Dar permisos de ejecución al archivo anterior  

chmod a+x bitnami-wordpress-VERSION-module-linux-x64-installer.run  


#3.- Ejecutar para empezar la instalación  

NOTA:   

si nos pide durante la instalación un directorio que contenga una instalación de bitnami, ponemos  
/opt/bitnami   
Si nos pide password de la base de datos, lo encontramos en la consola de bitnami.  

Donde pone "newbloname" ponemos el nombre de nuestra página, por ejemplo recetas  

sudo ./bitnami-wordpress-VERSION-module-linux-x64-installer.run --wordpress_instance_name newblogname  


#4.- Para entrar en nuestra página ponemos nuestra dirección del servidor + /newbloname  



#5.- REVISION  

En Putty poner  

```
# Debemos asegurarnos de estar en la ruta correcta (/home/bitnami), vamos a comprobarlo
$ cd   
$ pwd          #debemos estar en /home/bitnami

# Descargamos una sola vez el script para crear la estructura de la web y BD
$ wget https://raw.githubusercontent.com/manviny/EC2/master/PwScripts.sh && sudo chmod +x PwScripts.sh  && ./PwScripts.sh
```

Luego crear la web:  

```
# Ahora podemos crear una nueva web con: sudo ./creaPW.sh seguido de nombreWeb y DBpass
$ sudo ./creaPW.sh miweb dbpass  (dbpass es tu contraseña de bitnami)
```  
