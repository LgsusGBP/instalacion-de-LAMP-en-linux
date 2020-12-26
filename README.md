# instalacion-de-LAMP-en-linux

Escribir en la Consola los siguientes comandos.

sudo apt update (busca actualizaciones en el sistema)
sudo apt upgrde (actualizar el sistema operativo)

#instalacion de paquetes 

sudo apt install apache2 (instala el servidor de apache)
sudo systemctl status apache2 (para saber el estado del servidor)
sudo apt-get install php (instala el sistema de php)

(si hay cortafuegos hacer lo siguiente nota solo funciona en plataformas de servidores)

sudo ufw app list 
sudo ufw app info "Apache Full" (se sabe el estado del servidor de apache en el cortafuegos)
sudo ufw allow in "Apache Full" (se habilita el servidor de apache en el cortafuegos)
sudo ufw app info "Apache" (rectificamos el estado de apache)

Probar el servidor web Apache
Ahora, abra su navegador web y acceda a la página de prueba de Apache navegando a http: // localhost / o http: // IP-Address / .

(seguimos con la instalacion de paquetes)
sudo apt install mysql-server (instalamos mysql server en dado caso no les funcione ejecutar la siguiente linea)
sudo apt install mariadb-server (instala mariadb server)

(ejecutamos los siguientes comandos para la configuracion de mysql)
sudo mysql_secure_installation
