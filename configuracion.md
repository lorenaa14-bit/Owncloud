# Configuracion de MySQL
## Acceder a MySQL como root:

**sudo mysql**

## Crear la base de datos:

**CREATE DATABASE bbdd**

## Crear un usuario:

**CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password'**

## Dar privilegios al usuario:

**GRANT ALL ON bbdd.* TO 'usuario'@'localhost'**

## Salir de MySQL:

**exit**

## Probar la conexión: Con otro terminal, conecta con el usuario creado:

**mysql -u usuario -p**

## Copiar l'arxiu zip al directori /var/www/html:
 Copiem el fitxer descarregat (en aquest cas, app-web.zip) al directori on s'ubiquen els fitxers web d'Apache:

**sudo cp ~/Baixades/app-web.zip /var/www/html**

## Accedir al directori /var/www/html:

**cd /var/www/html**

##Descomprimir l'arxiu zip:

**sudo unzip app-web.zip**

## Copiar els fitxers a /var/www/html: Copiem els fitxers descomprimits al directori correcte:

**sudo cp -R app-web/. /var/www/html**

## Eliminar la carpeta creada pel unzip:

**sudo rm -rf app-web/**

## Eliminar el fitxer index.html per defecte d'Apache2:

**sudo rm -rf /var/www/html/index.html**

## Aplicar permisos als fitxers: Assegurem-nos que els permisos i propietats són correctes per permetre l'accés i gestió dels fitxers:

**cd /var/www/html**
**sudo chmod -R 775**
**sudo chown -R usuario:www-data**
