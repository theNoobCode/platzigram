# Platzigram

Platzigram es un sitio web en el cual puedes como usuario: compartir una foto y establecerle un titulo, editar nuestro perfil, ver pubicaciones de otros usuarios.
Este proyecto es realizado en Platzi con el fin de aprender python y el desarrollo de sitios web con framework Django.

## Tabla de Contenido
* Requisitos
* Guia de instación de python3, en los sistemas operativos Windows y Ubuntu
* Configuración de ambiente local

## Requisitos.
  ver el archivo requeriments.txt

## Instalación de python3 (windows/ubuntu)

**Instalar Python en Windows**

1. Nos dirigiremos al sitio oficial de python. En su apartado de descargas
[python 3.8.2](https://www.python.org/downloads/release/python-382/).

2. Al final de la página [python 3.8.2](https://www.python.org/downloads/release/python-382/)
habrá una sección llamada Files, en ella seleccionamos el link correspondiente  a la arquitectura de nuestro equipo
en el que estemos trabajando. Asegurarnos de dar click al instalador ejecutable.

3. En este punto se te descargá un archivo .exe, lo ejecutaremos cómo administrador y se nos abrirá
una ventana de diálogo y seguiremos los siguientes pasos:

* selecciona el checkbox que dice: agregar python al path.
* selecciona la opción instalación personalizada.
* al final, en opciones avanzadas podrás cambiar el lúgar de instalación y si deseas que sea para todos los usuarios.
* una vez finalice la instalación, ve a su ruta de instalación y ejecuta el interprete de python, así confirmas sí
  la instalación fue correcta o no.

**Instalar Python en Ubuntu**

1. Nos dirigiremos al sitio oficial de python. En su apartado de descargas
[python 3.8.2](https://www.python.org/downloads/release/python-382/).

2. Con la misma dirección compartida del sitio oficial, nos dirigeremos al final de la pagina en su sección Files.

3. Seleccionaremos el link de desacarga "XZ compressed source tarball" , este nos descargará una carpeta comprimida
con extensión tar.xz

 4. una vez descargado y moviendolo al lugar deseado de instalación ejecutaremos los siguientes comandos:
* $ tar xf nombreCarpetaTarDesacargada

Este comando se ha encargado de descomprimir la carpeta, ahora dentro de la carpeta descomprimida instalemos
las librerias de desarrollo para python zlib1g-dev:
* sudo apt-get update
* sudo apt-get install -y zlib1g-dev
* $ ./configure
* make
* sudo make install

## Configuración de Ambiente.

Para ejecutar el proyecto a nivel local, debemos seguir los siguientes pasos:

* Descargar el proyecto manualmente (download) ó sí manejamos git con el comando clone: 
   git clone https://github.com/xbrayan98x/desarrollo_empresarial.git (Ubicados en la carpeta de trabajo) 

**Crear ambiente virtual:**
* Abriremos una linea de comandos en nuestro sistema operativo, ubicados en la carpeta de trabajo
    y ejecutamos el siguiente comando:
    
* python3 –m venv nombre_ambiente_virtual

* Una vez ejecutado el comando, y este nos haya creado nuestro ambiente virtual procedemos a activarlo.

**En windows:**

* cd C:\usuarios\Documentos\proyecto\”nombre_ambiente_virtual”\Scripts
    una vez dentro ejecutamos el comando: activate

**En ubuntu:**

user:~/doucuments/proyecto/$ source nombre_ambiente_virtual/bin/activate

* Una vez activado el ambiente, procedemos a instalar con pip las librerias necesarias para trabajar en el ambiente.

En este caso se deben instalar las dependencias que contiene el proyecto en el archivo requeriments.txt .

Procedemos a ejecuar el siguiente comando con pip:
* pip3 install -r requeriments.txt

Pip es una manejador de paquetes, librerias o dependencias que maneja python. Cuándo nostros instalamos python3 este
nos instala pip.

Una vez hecho esto procedemos a levantar localmente el servidor que nos proporciona Django, pero primero
ejecutaremos las migraciones para que tome los cambios en base de datos.

dentro de la carpeta del proyecto, ejecutaremos el comando:
* python3 manage.py migrate

Comando ejecución server local:
* python3 manage.py runserver
