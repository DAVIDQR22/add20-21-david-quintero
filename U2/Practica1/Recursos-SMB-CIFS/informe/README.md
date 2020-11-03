# Practica 1 Recursos SMB/CIFS

## 1. Servidor Samba (Linux)
### 1.4 Configurar el servidor Samba
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba2.png)

cp /etc/samba/smb.conf /etc/samba/smb.conf.bak, hacer una copia de seguridad del fichero de configuración antes de modificarlo.

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba1.4-1.png)

Yast -> Samba Server
Workgroup: curso2021
Sin controlador de dominio.

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba1.4-2.png)

En la pestaña de Inicio definimos
Iniciar el servicio durante el arranque de la máquina.
Ajustes del cortafuegos -> Abrir puertos

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba1.4-3.png)

## 1.5 Crear los recursos compartidos de red
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba1.5-1.PNG)

Editando directamente el ficher /etc/samba/smb.conf o 
Yast -> Samba Server -> Recursos compartidos -> Configurar.

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba1.5-2.png)

testparm, verificar la sintaxis del fichero de configuración.

# 2. Windows
## 2.1 Cliente Windows GUI
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba2.1-1.PNG)

Escribimos \\192.168.1.31 y vemos lo siguiente:

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba2.1-2.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba2.1-3.PNG)

Acceder al recurso compartido castillo con el usuario soldado.
net use para ver las conexiones abiertas.
net use * /d /y, para borrar todas las conexión SMB/CIFS que se hayan realizado.

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba2.1-5.PNG)

Acceder al recurso compartido barco con el usuario pirata.
Ir al servidor Samba.

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba2.1-4.PNG)

smbstatus, desde el servidor Samba.
lsof -i, desde el servidor Samba.


## 2.2 Cliente Windows comandos
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/enviar2.2-1.PNG)

net view \\192.168.1.31, para ver los recursos del servidor remoto.

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/enviar2.2-2.PNG)

Montamos el recurso barco de forma persistente.

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/enviar2.2-3.PNG)

sudo smbstatus, desde el servidor Samba.
lsof -i, desde el servidor Samba.

# 3 Cliente GNU/Linux
## 3.1 Cliente GNU/Linux GUI
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba3.1-1.PNG)

Probar a crear carpetas/archivos en castillo

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba3.1-2.PNG)

Probar a crear carpetas/archivos en barco

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba3.1-3.PNG)



![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba3.1-4.PNG)



![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba3.1-5.PNG)



![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U2/Practica1/Recursos-SMB-CIFS/imagenes/samba3.1-6.PNG)
