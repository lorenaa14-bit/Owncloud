# owncloud
## Instal·lació i configuració d'aplicacions web
Per instal·lar una aplicació web, primer cal descarregar-ne el codi font i col·locar-lo al directori principal del nostre servidor d'aplicacions, que en aquest cas és Apache2. Quan instal·lem Apache2, es crea automàticament una carpeta anomenada (/var/www/html), que funciona com a directori principal per defecte del servidor web.
Així doncs, si col·loquem la nostra aplicació dins del directori (/var/www/html), podrem accedir-hi des d’un navegador utilitzant l’adreça (http://localhost).
### Actualitzar la màquina
Primer, cal assegurar-nos que el sistema està al dia, actualitzant la llista de paquets i els paquets instal·lats. 
 **Copiar código sudo apt update sudo apt upgrade**
 
# Instal·lació del servidor web Apache2
 Apache2 és el servidor web que servirà les aplicacions als usuaris. Per instal·lar-lo, executem: 
 **Copiar código sudo apt install -y apache2** 

 # Instal·lació del servidor de bases de dades MySQL
Moltes aplicacions web necessiten una base de dades per emmagatzemar informació. Instal·lem el servidor de bases de dades MySQL amb la següent comanda:
**Copiar código sudo apt install -y mysql-server**

# Instal·lació de PHP i llibreries necessàries
 PHP és el llenguatge de programació que utilitzen moltes aplicacions web. A més del nucli de PHP, instal·larem algunes llibreries addicionals que sovint són necessàries per a la funcionalitat completa de les aplicacions: 
 **Copiar código sudo apt install -y php libapache2-mod-php sudo apt install -y php-fpm php-common php-mbstring php-xmlrpc php-soap php-gd php-xml php-intl php-mysql php-cli php-ldap php-zip php-curl**

 # Reiniciar el servidor Apache2
 Després de la instal·lació de PHP i les seves extensions, cal reiniciar el servidor Apache perquè reconegui la nova configuració i llibreries: 
 **Copiar código sudo systemctl restart apache2** 

! [IMG_6368.HEIC][img1]

