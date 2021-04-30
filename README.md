## Cómo configurar Raspberry Pi 4 por primera vez sin monitor, mouse y teclado.

## 1.Material necesario

Aquí aprenderás sobre Raspberry Pi, qué cosas necesitas para usarla y cómo configurarla.

Por lo general es necesario usar un teclado ⌨️, un ratón 🖱️ y un monitor 🖥️ para comenzar a utilizar Raspberry Pi para tus proyectos. En esta guía utilizaremos la versión más actual de software a abril 2021. Y solo necesitaremos una laptop 💻, una Raspberry Pi 4 y su fuente de alimentacion.

Hay varios modelos de Raspberry Pi. Raspberry Pi 4 Model B es el más nuevo, rápido y fácil de usar.


Raspberry Pi 4 viene con 2GB, 4GB u 8GB de RAM. Para la mayoría de los propósitos educativos, proyectos de aficionados de la cultura maker y para usar como computadora de escritorio, 2GB es suficiente.
 
Como mencione lo que necesitaremos es:
 
*   Laptop
*   Raspberry Pi 4
*   Fuente de alimentacion (De preferencia adquirir junto con tu Raspberry la fuente oficial para no tener ningun problema, si es que no tienes mucha experiencia [USB-C Power Supply](https://www.raspberrypi.org/products/type-c-power-supply/))
* Smartphone con función Mobile Hotspot
*  Tarjeta Micro SD 
 
Una parte muy importante antes de iniciar es la seleccion de una tarjeta Micro SD, ya que cargaremos el sistema operativo en ella, en las figuras podemos observar una memoria micro SD donde tomaremos en cuenta los recuadros negros, esta simbologia nos indica en la tabla las clasificaciones de las tarjetas micro SD actuales, es muy importante tener en cuenta que la velocidad minima que deberia ser usada en una Raspberry Pi es 10 Mb/seg y con una capacidad de al menos 8GB.
 
Se notará en la velocidad de encendido y de la ejecución de algunas tareas. No es tan importante tener la SD más cara para tener un mejor funcionamiento en la Raspberry, pero tener una buena tarjeta puede extender su vida útil ya que las Raspberry Pi hace uso intenso sobre las tarjetas y terminan estropeadas lo que significa comprar otra.

Muchos vendedores incluyen tarjetas SD para Raspberry Pi que ya están configuradas con el sistema operativo Raspberry Pi y listas para usar con kits pero suelen venir con NOOBS.
 
NOOBS es una aplicación que facilita la instalación de diversas distribuciones Linux en el pequeño ordenador.
 
NOOBS hace innecesario el acceso a Internet durante la instalación, y tan solo tendremos que descargar NOOBS y descomprimirlo en una tarjeta SD de al menos 4 GB de capacidad. Al hacerlo se nos dará la opción de instalar soluciones como Raspbian, Arch Linux, RaspBMC, el recién salido Pidora u OpenELEC sin problemas. La instalación permitirá más tarde iniciar nuestro Raspberry Pi de forma normal con esa nueva distribución, pero NOOBS quedará residente en memoria y podremos acceder a esta aplicación siempre que queramos mediante la pulsación de la tecla Shift durante el proceso de arranque.
 
Como preferencia personal, me parece mejor comprar una memoria de alguna marca como SanDisk y hacer la instalación como muestro a continuación.


**Nota: Se debe evitar desconectar la fuente de energía sin tener apagada la Raspberry esto puede dañar la memoria al momento y se perdería todo, ni formateando la memoria podría ser utilizada de nuevo**

##2.Instalación del sistema operativo Raspberry Pi OS a través de Raspberry Pi Imager
 
El uso de Raspberry Pi Imager es la forma más sencilla de instalar el sistema operativo 
Raspberry Pi en su tarjeta SD. **Nota: Raspberry Pi OS no es el único sistema operativo que 
puede ser instalado.** Los pasos que se describen a continuación pueden ser utilizados para 
instalar otros sistemas operativos compatibles con Raspberry Pi, pero la configuración inicial 
al encender será diferente. Para más información de otros sistemas operativos visite [installing operating system images](https://www.raspberrypi.org/documentation/installation/installing-images/README.md).
Para Descargar y ejecuta Raspberry Pi Imager visite la página de [Raspberry Pi downloads 
page](https://www.raspberrypi.org/downloads) . 
Haga clic en el enlace de la Raspberry Pi Imager que coincida con su sistema operativo.

Cuando finalice la descarga, haz clic en él para iniciar el instalador.
Cuando inicia el instalador, su sistema operativo puede intentar bloquear su ejecución (En ese caso hay que dar en **more info** dentro de la ventana del instalador para seguir y dar click en **Run anyway**).
 
Una vez instalado Raspberry Pi imager 
 
1. Inserte su tarjeta SD en la ranura para tarjeta SD de la computadora o computadora 
portátil.
 
2. En Raspberry Pi Imager, seleccione el sistema operativo que desea instalar ❶ y 
la tarjeta SD en la que desea instalarlo ❷ (Ver Figura).
**Nota: Deberá estar conectado a Internet la primera vez para que Raspberry Pi Imager descargue el sistema operativo que elija. Ese sistema operativo se almacenará para su uso futuro sin conexión. Estar en línea para usos posteriores significa que el generador de imágenes Raspberry Pi siempre le proporcionará la última versión**



En caso de tener alguna tarjeta con otro sistema operativo anterior o con algunos archivos podemos utilizar el Raspberry Pi Imager para formatear y dejarla como nueva.
 
Seleccionaremos "CHOOSE OS" y daremos clic en Erase, regresaremos a la ventana principal seleccionaremos "CHOOSE SD CARD" y seleccionaremos nuestra tarjeta, se habilita "WRITE", daremos clic, nos aparecerá una ventana donde confirmaremos y listo tenemos lista nuestra tarjeta para ser sobreescribir con el sistema operativo de Raspberry.


Para jugar con las opciones avanzadas que nos permitirán acceder a nuestra Raspberry de manera remota, deben presionar la secuencia de teclas:
 
"Ctrl-Mayús-X"
 
Que desplegará una ventana en la que seleccionaremos la casilla "Enable SSH" también solicitará que ingresemos una contraseña para el usuario pi que es el usuario que viene por default en Raspberry pi, por lo general la contraseña es Raspberry para este usuario, pero con esta opción puedes ingresar la que sea de tu agrado.


Bajando más en esta ventana podremos encontrar la casilla "configure wifi" donde ingresamos el nombre de la red y la contraseña, como antes mencione utilizaremos un smartphone, que nos funcionara como modem (en mi caso utilizo un teléfono Samsung, que tiene la opción de Hotspot, cuando un dispositivo se conecta a mi telefono me aparece en dispositivos conectados y al hacer clic en el dispositivo me da la dirección IP), más adelante hablaremos de la IP, como último en esta ventana al final nos permite elegir el país en el que estamos para algunas configuraciones de lenguaje, al finalizar daremos clic en save y regresaremos a la ventana principal.


Ahora seleccionaremos el sistema operativo dando click en "CHOOSE OS" para quien está iniciando con una Raspberri se recomienda utilizar la primera opción, ya para usuarios más experimentados la segunda nos permite elegir la versión lite que es recomendada para algunos proyectos en específico.


Ahora daremos clic en "CHOOSE SD CARD" para seleccionar nuestra tarjeta, dando click regresaremos a la ventana principal. Se habilita el botón "WRITE" damos clic y nos aparecerá un mensaje donde solicita la confirmación de la escritura del sistema operativo.


Al finalizar la escritura del sistema operativo en la tarjeta nos aparecerá la siguiente ventana con esto tendremos lista la memoria micro SD para conectarla en nuestra Raspberry Pi.



Para conectar la tarjeta sd es muy fácil por la parte de abajo de nuestra Raspberry puedes encontrar el slot donde se coloca.



Por último conectaremos la fuente de poder primero a nuestra Raspberry y después a un enchufe. **En caso de conectar primero al enchufe y luego a la Raspberry podríamos causar pequeños cortos que podrían afectar la vida útil de nuestra tarjeta**.


##3.SSH Windows
 
Puedes acceder a la línea de comando de una Raspberry Pi de forma remota desde otra computadora o dispositivo en la misma red usando SSH. La Raspberry Pi actuará como un dispositivo remoto: puede conectarse usando un cliente en otra máquina. Solo tiene acceso a la línea de comandos, no al entorno de escritorio completo. 
Para un escritorio remoto completo, más adelante consulte VNC y su guía de instalación [How to Remote Desktop to your Raspberry 
Pi with VNC Viewer](https://www.raspberrypi.org/documentation/remote-access/vnc/).

**Nota: En las versiones más recientes de Raspberry Pi OS, solamente se necesita habilitar VNC, así que no es necesario instalar el servidor como muestra el enlace de VNC**
 
Con los pasos anteriores ya habilitamos el SSH en nuestra Raspberry ahora accederemos por primera vez para comenzar a trabajar.
 
Anteriormente mencionamos sobre la IP en caso de no contar con la funcion hotspot puedes revisar otras formas de obtenerlas en [IP Raspberry](https://www.raspberrypi.org/documentation/remote-access/ip-address.md)
 
Necesitaremos instalar Putty, es un cliente SSH desarrollado  para Windows. PuTTY es un software de código abierto que está disponible con código fuente. Para descargar visita [Putty](https://www.putty.org/)
 
Al instalar Putty nos aparecerá lo siguiente y tenemos que seleccionar lo que se muestra marcado en la imagen.
