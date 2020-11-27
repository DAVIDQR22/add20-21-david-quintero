# Servicio de Directorio con comandos

## Entrega
* 2.4 Comprobar contenido del DS LDAP 
* 3.3 Comprobar nuevo usuario
* 4.3 Comprobar los usuarios creados
# 2. Instalar el Servidor LDAP

## 2.4 Comprobamos el acceso al contenido del LDAP

* `ldapsearch -b "dc=ldapXX,dc=curso2021" -x | grep dn`, muestra el contenido de nuestra base de datos LDAP. "dn" significa nombre distiguido, es un identificador que tiene cada nodo dentro del árbol LDAP.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U4/Practica1/Imagenes/ldap2.png)
* `ldapsearch -H ldap://localhost -b "dc=ldapXX,dc=curso2021" -W -D "cn=Directory Manager" | grep dn`, en este caso hacemos la consulta usando usuario/clave.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U4/Practica1/Imagenes/ldap2-2.PNG)

# 3. Añadir usuarios LDAP por comandos

## 3.3 Comprobar el nuevo usuario

* `ldapsearch -W -D "cn=Directory Manager" -b "dc=ldapXX,dc=curso2021" "(uid=*)"`, para comprobar si se ha creado el usuario correctamente en el LDAP.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U4/Practica1/Imagenes/ldap3-1.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U4/Practica1/Imagenes/ldap3-2.PNG)

# 4. Contraseñas encriptadas

## 4.3 Comprobar los usuarios creados

* Ir a la MV cliente LDAP.
* `nmap -Pn IP-LDAP-SERVER`, comprobar que el puerto LDAP del servidor está abierto.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U4/Practica1/Imagenes/ldap4-1.PNG)
Si no aparecen los puertos abiertos, entonces revisar el cortafuegos.
* `ldapsearch -H ldap://IP-LDAP-SERVER -W -D "cn=Directory Manager" -b "dc=ldapXX,dc=curso2021" "(uid=*)" | grep dn` para consultar los usuarios LDAP que tenemos en el servicio de directorio remoto.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U4/Practica1/Imagenes/ldap4-2.PNG)
