# Servidor de impresión

# 2. Servidor de Impresión

* Instalar el sistema de impresión CUPS para GNU/Linux.
* `systemctl status ...`, verificar que el servicio está en ejecución.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion2-1.png)
* Configurar CUPS `/etc/cups/cupsd.conf` (Ver vídeo):
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion2-2.png)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion2-3.png)
* A continuación, conectar a la interfaz web de CUPS.
* Acceder a la sección de `Administración` con el usuario/clave de root. Desde ahí acceder a la sección `Ver archivo de registro de accesos`.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion2-4.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion2-5.PNG)
---
# 3. Imprimir de forma local

Ahora vamos a usar una impresora de forma local en el servidor de impresión.

* Instalar el paquete `cups-pdf` que nos permite hacer uso de una impresora virtual PDF local. Usaremos esta impresora virtual para las pruebas en caso de no disponer de una impresora real.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion3-1.PNG)
* Crear una archivo TXT o ODT con algún contenido.
* Imprimir el documento en la impresora local.
* Comprobar el resultado. Los trabajos de impresión de la impresora virtual PDF se guardan en alguno de estos directorios:
```
/home/usuario/PDF
/var/spool/cups-pdf/anonymous
```
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion3-2.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion3-3.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion3-4.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion3-5.PNG)
---
# 4. Imprimir de forma remota

Ir al servidor.
* Habilitamos la impresora como recurso de red compartido.
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion4-1.PNG)
> Es importante que el cliente tenga una IP definida en la cláusula Allow del servidor.
Ir a un cliente.
* Agregar impresora de red. Primero la buscamos en IP del servidor y nos debe aparecer automáticamente
(Por ejemplo `ipp://ip-server:631/printes/CUPS-PDF`).
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion4-2.PNG)
![](https://github.com/DAVIDQR22/add20-21-david-quintero/blob/master/U3/Practica1/imagenes/impresion4-3.PNG)
* Crear una archivo TXT o ODT con algún contenido.
* Imprimir el documento en la impresora remota.
* Ir al servidor.
* Comprobamos que se ha realizado la impresión remota.
