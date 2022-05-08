# instalación-de-LAMP-en-Linux

Escribir en la Consola los siguientes comandos.

```busca actualizaciones en el sistema```
>sudo apt update 

```actualizar el sistema operativo```
>sudo apt upgrade 

**#instalacion de paquetes**

```instala el servidor de apache```
>sudo apt install apache2 

```para saber el estado del servidor```
>sudo systemctl status apache2 

```instala el sistema de php```
>sudo apt-get install php 

```**(si hay cortafuegos hacer lo siguiente nota solo funciona en plataformas de servidores)**```

>sudo ufw app list

```(se sabe el estado del servidor de apache en el cortafuego)```
>sudo ufw app info "Apache Full" 

```(se habilita el servidor de apache en el cortafuego)```
>sudo ufw allow in "Apache Full"

```(rectificamos el estado de apache)```
>sudo ufw app info "Apache" (rectificamos el estado de apache)

``` Probar el servidor web Apache ``` 

```** Ahora, abra su navegador web y acceda a la página de prueba de Apache navegando a http: // localhost / o http: // IP-Address / . **```

``` (seguimos con la instalación de paquetes) ```

``` (instalamos mysql server en dado caso no les funcione ejecutar la siguiente línea)```
>sudo apt install mysql-server 
``` (instala mariadb server) ```
>sudo apt install mariadb-server 

``` (ejecutamos los siguientes comandos para la configuración de mysql)``` 

>sudo mysql_secure_installation

``` (Se le preguntará si desea configurar el componente "VALIDATE PASSWORD" o no. Este componente permite a los usuarios configurar una contraseña segura para las credenciales de la base de datos. Si está habilitado, comprobará automáticamente la seguridad de la contraseña y obligará a los usuarios a establecer solo aquellas contraseñas que sean lo suficientemente seguras. Es seguro dejarlo desactivado. Sin embargo, debe utilizar una contraseña segura y única para las credenciales de la base de datos. Si no desea habilitar este componente, simplemente presione cualquier tecla para omitir la parte de validación de contraseña y continuar con el resto de los pasos. ``` 

``` **Ingrese "y" si desea configurar el componente VALIDATE PASSWORD: )**```
```** ingresamos la nueva contraseña y a lo demás le damos en sí**```

``` Ahora ejecutamos los siguientes comandos``` 

>sudo mysql

>SELECT user,authentication_string,plugin,host FROM mysql.user;

``` El comando que viene es para poder colocarle contraseña a my sql y asi poder acceder de manera segura. la variable "$root" la cambian por la contraseña que mejor les paresca```
>ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password BY '$root';

>FLUSH PRIVILEGES;

>SELECT user,authentication_string,plugin,host FROM mysql.user;

>exit
```para recftificar la que tengamos la contraseña ingresamos de la diguiente forma:```
>sudo mysql -u root -p
```Colocamos la contraseña```
>sudo apt install phpmyadmin

```** Seleccionamos apache2 parándonos encima de él y presionando la barra de espacio;**``` 
``` **seleccionamos 'yes';**``` 
``` **colocamos la nueva contraseña**```

>sudo mysql -u root -p (ingresamos nuevamente como root)

>GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost' IDENTIFIED BY 'root' WITH GRANT OPTION;

>exit

```** las contraseñas de las bases de datos es: root y la contraseña es: root**```
``` está todo listo ahora podemos configurar nuestras páginas web en local con interfaz gráfica en la configuración de las bases de datos``` 
