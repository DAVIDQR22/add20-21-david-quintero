
# Acceso remoto SSH

# 2 Instalación del servicio SSH en Linux

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion2-1.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion2-1-1.PNG)
Verificamos que el servicios esta funcionando.

### 2.2 Primera conexión SSH desde cliente GNU/Linux
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion2-2.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion2-2-1.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion2-2-2.PNG)
Hacemos las debidas conexiones por ssh desde los clientes (Asegurarse de tener creados los usuarios respectivos para la conexión por ssh).

# 3. Cambiamos la identidad del servidor

### 3.2 Comprobamos
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion3-2.PNG)
Comprobación de la conexión del cliente al servidor desde Linux.

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion3-2-windows.PNG)
Comprobación de la conexión del cliente al servidor desde Windows.

# 5. Autenticación mediante claves públicas
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion5-1.PNG)
Creamos un par de claves para usuarios desde el cliente en el cual haremos la autenticación de claves.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion5-2.PNG) 
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion5-3.PNG)

Copiamos la clave y vemos que podemos conectarnos desde el cliente a quintero4 sin necesidad de perdir la contraseña.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion5-4.PNG)
Vemos que en Windows cliente nos sigue piediendo la clave.

# 6. Uso de SSH como túnel para X
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion6-1.PNG)
Instalamos en el servidor una aplicacion APP1, en mi caso geany.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion6-2.PNG)
Nos metemos en el archivo de configuración de sshd para decirle en una linea que si, para permitir la ejecución de aplicaciones gráficas.

![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion6-3.PNG)

Reiniciamos el servicio ssh.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion6-4.PNG)
Nos metemos en un cliente y comprobamos que podemos abrir Geany.

# 8. Restricciones de uso
### 8.1 Restricción sobre un usuario
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion8-1.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U1/Practica2/ssh/imagenes/comprobacion8-1-1.PNG)

Bloqueamos el usuario quintero2 (ya que lo cambie en el archivo del ssh), para que nadie pueda acceder a este 




