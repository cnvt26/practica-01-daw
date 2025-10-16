# Instalación de la pila LAMP en Ubuntu Server

Para realizar dicha instalación, realizaremos los siguientes pasos:

## Creación de la instancia EC2

La instancia se creó a partir de una imagen de Ubuntu Server. El modelo elegido fue el **t2.micro**, con **2 GB de RAM** y **30 GB de disco**. Los puertos SSH, HTTP y HTTPS quedaron abiertos en el cortafuegos. Para el acceso SSH, se utilizó el par de claves **vockey.pem** de AWS. También le asignamos una IP elástica para que la dirección de la instancia permanezca fija a lo largo de nuestras pruebas.

### Paso a paso:

1. Se accedió a la consola de AWS EC2 y se seleccionó **Lanzar instancia**.
![Acceso a la consola de AWS](images/image-1.png)
![Acceso a EC2](images/image-2.png)
![Selección de "Lanzar instancia"](images/image-3.png)

2. Se eligió la Community AMI de **Ubuntu Server**.
![Configuración de la Community AMI](images/image-4.png)

3. El tipo de instancia fue configurado como **t2.micro** y se creó o seleccionó un **par de claves** (ej.vockey.pem) para la conexión SSH..
![Configuración del tipo de instancia y del par de claves](images/image-5.png)

### Configuración de Red y Seguridad (Grupo de Seguridad)

Durante la configuración de la instancia, se creó un Grupo de Seguridad para actuar como firewall virtual. Este grupo de seguridad permite el tráfico entrante a través de los siguientes puertos TCP, esenciales para el proyecto:

![Configuración del Grupo de Seguridad](images/image-6.png)
