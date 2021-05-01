## Cómo configurar Raspberry Pi 4 por primera vez sin monitor, mouse y teclado.

## 1.Material necesario

Aquí aprenderás sobre Raspberry Pi, qué cosas necesitas para usarla y cómo configurarla.

Por lo general es necesario usar un teclado ⌨️, un ratón 🖱️ y un monitor 🖥️ para comenzar a utilizar Raspberry Pi para tus proyectos. En esta guía utilizaremos la versión más actual de software a abril 2021. Y solo necesitaremos una laptop 💻, una Raspberry Pi 4 y su fuente de alimentación.

Hay varios modelos de Raspberry Pi. Raspberry Pi 4 Model B es el más nuevo, rápido y fácil de usar.

![raspberry-pi](https://user-images.githubusercontent.com/79243784/116725445-86bb8180-a9a7-11eb-9737-83d1cb6611f7.png)

Raspberry Pi 4 viene con 2GB, 4GB u 8GB de RAM. Para la mayoría de los propósitos educativos, proyectos de aficionados de la cultura maker y para usar como computadora de escritorio, 2GB es suficiente.
 
Como mencione lo que necesitaremos es:
 
*   Laptop
*   Raspberry Pi 4
*   Fuente de alimentacion (De preferencia adquirir junto con tu Raspberry la fuente oficial para no tener ningun problema, si es que no tienes mucha experiencia [USB-C Power Supply](https://www.raspberrypi.org/products/type-c-power-supply/))
* Smartphone con función Mobile Hotspot
*  Tarjeta Micro SD 
 
Una parte muy importante antes de iniciar es la seleccion de una tarjeta Micro SD, ya que cargaremos el sistema operativo en ella, en las figuras podemos observar una memoria micro SD donde tomaremos en cuenta los recuadros negros, esta simbologia nos indica en la tabla las clasificaciones de las tarjetas micro SD actuales, es muy importante tener en cuenta que la velocidad minima que deberia ser usada en una Raspberry Pi es 10 Mb/seg y con una capacidad de al menos 8GB.
 
Se notará en la velocidad de encendido y de la ejecución de algunas tareas. No es tan importante tener la SD más cara para tener un mejor funcionamiento en la Raspberry, pero tener una buena tarjeta puede extender su vida útil ya que las Raspberry Pi hace uso intenso sobre las tarjetas y terminan estropeadas lo que significa comprar otra.

![sd](https://user-images.githubusercontent.com/79243784/116725537-9fc43280-a9a7-11eb-9cbf-9b0a78fb80ec.jpg)

![SDFAQ-UHS-2](https://user-images.githubusercontent.com/79243784/116725548-a357b980-a9a7-11eb-9001-005e23f84b4d.jpg)


Muchos vendedores incluyen tarjetas SD para Raspberry Pi que ya están configuradas con el sistema operativo Raspberry Pi y listas para usar con kits pero suelen venir con NOOBS.
 
NOOBS es una aplicación que facilita la instalación de diversas distribuciones Linux en el pequeño ordenador.
 
NOOBS hace innecesario el acceso a Internet durante la instalación, y tan solo tendremos que descargar NOOBS y descomprimirlo en una tarjeta SD de al menos 4 GB de capacidad. Al hacerlo se nos dará la opción de instalar soluciones como Raspbian, Arch Linux, RaspBMC, el recién salido Pidora u OpenELEC sin problemas. La instalación permitirá más tarde iniciar nuestro Raspberry Pi de forma normal con esa nueva distribución, pero NOOBS quedará residente en memoria y podremos acceder a esta aplicación siempre que queramos mediante la pulsación de la tecla Shift durante el proceso de arranque.
 
Como preferencia personal, me parece mejor comprar una memoria de alguna marca como SanDisk y hacer la instalación como muestro a continuación.


**Nota: Se debe evitar desconectar la fuente de energía sin tener apagada la Raspberry esto puede dañar la memoria al momento y se perdería todo, ni formateando la memoria podría ser utilizada de nuevo**

## 2.Instalación del sistema operativo Raspberry Pi OS a través de Raspberry Pi Imager
 
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

![imager1 5](https://user-images.githubusercontent.com/79243784/116725672-dc902980-a9a7-11eb-8a63-256c3c9a9bdb.png)

En caso de tener alguna tarjeta con otro sistema operativo anterior o con algunos archivos podemos utilizar el Raspberry Pi Imager para formatear y dejarla como nueva.
 
Seleccionaremos "CHOOSE OS" y daremos clic en Erase, regresaremos a la ventana principal seleccionaremos "CHOOSE SD CARD" y seleccionaremos nuestra tarjeta, se habilita "WRITE", daremos clic, nos aparecerá una ventana donde confirmaremos y listo tenemos lista nuestra tarjeta para ser sobreescribir con el sistema operativo de Raspberry.

![ERASEMEDIUM](https://user-images.githubusercontent.com/79243784/116725748-fd587f00-a9a7-11eb-9cb9-372214212224.png)

Para jugar con las opciones avanzadas que nos permitirán acceder a nuestra Raspberry de manera remota, deben presionar la secuencia de teclas:
 
"Ctrl-Mayús-X"
 
Que desplegará una ventana en la que seleccionaremos la casilla "Enable SSH" también solicitará que ingresemos una contraseña para el usuario pi que es el usuario que viene por default en Raspberry pi, por lo general la contraseña es Raspberry para este usuario, pero con esta opción puedes ingresar la que sea de tu agrado.

![enablesshraspberry](https://user-images.githubusercontent.com/79243784/116725836-1a8d4d80-a9a8-11eb-9d7c-fad1703848c3.png)

Bajando más en esta ventana podremos encontrar la casilla "configure wifi" donde ingresamos el nombre de la red y la contraseña, como antes mencione utilizaremos un smartphone, que nos funcionara como modem (en mi caso utilizo un teléfono Samsung, que tiene la opción de Hotspot, cuando un dispositivo se conecta a mi telefono me aparece en dispositivos conectados y al hacer clic en el dispositivo me da la dirección IP), más adelante hablaremos de la IP, como último en esta ventana al final nos permite elegir el país en el que estamos para algunas configuraciones de lenguaje, al finalizar daremos clic en save y regresaremos a la ventana principal.

![WIFIPASSWORDMEDIUM](https://user-images.githubusercontent.com/79243784/116725892-2da01d80-a9a8-11eb-8e96-ab92b30edb88.png)

Ahora seleccionaremos el sistema operativo dando click en "CHOOSE OS" para quien está iniciando con una Raspberri se recomienda utilizar la primera opción, ya para usuarios más experimentados la segunda nos permite elegir la versión lite que es recomendada para algunos proyectos en específico.

![chooseOSMEDIUM](https://user-images.githubusercontent.com/79243784/116726028-588a7180-a9a8-11eb-8354-54f56439f030.png)

Ahora daremos clic en "CHOOSE SD CARD" para seleccionar nuestra tarjeta, dando click regresaremos a la ventana principal. Se habilita el botón "WRITE" damos clic y nos aparecerá un mensaje donde solicita la confirmación de la escritura del sistema operativo.

![sdchooseMEDIUM](https://user-images.githubusercontent.com/79243784/116726065-64763380-a9a8-11eb-9a53-4b80c71dc335.png)

Al finalizar la escritura del sistema operativo en la tarjeta nos aparecerá la siguiente ventana con esto tendremos lista la memoria micro SD para conectarla en nuestra Raspberry Pi.

![succesOSwritemedium](https://user-images.githubusercontent.com/79243784/116726093-6dff9b80-a9a8-11eb-8851-94d40f4c5eac.png)

Para conectar la tarjeta sd es muy fácil por la parte de abajo de nuestra Raspberry puedes encontrar el slot donde se coloca.

![pi-sd](https://user-images.githubusercontent.com/79243784/116726123-77890380-a9a8-11eb-8a17-7006dd378c2c.png)

Por último conectaremos la fuente de poder primero a nuestra Raspberry y después a un enchufe. **En caso de conectar primero al enchufe y luego a la Raspberry podríamos causar pequeños cortos que podrían afectar la vida útil de nuestra tarjeta**.

![pi-power](https://user-images.githubusercontent.com/79243784/116726143-7e177b00-a9a8-11eb-99f8-b25aeff90cd3.png)

## 3.SSH Windows
 
Puedes acceder a la línea de comando de una Raspberry Pi de forma remota desde otra computadora o dispositivo en la misma red usando SSH. La Raspberry Pi actuará como un dispositivo remoto: puede conectarse usando un cliente en otra máquina. Solo tiene acceso a la línea de comandos, no al entorno de escritorio completo. 
Para un escritorio remoto completo, más adelante consulte VNC y su guía de instalación [How to Remote Desktop to your Raspberry 
Pi with VNC Viewer](https://www.raspberrypi.org/documentation/remote-access/vnc/).

**Nota: En las versiones más recientes de Raspberry Pi OS, solamente se necesita habilitar VNC, así que no es necesario instalar el servidor como muestra el enlace de VNC**
 
Con los pasos anteriores ya habilitamos el SSH en nuestra Raspberry ahora accederemos por primera vez para comenzar a trabajar.
 
Anteriormente mencionamos sobre la IP en caso de no contar con la funcion hotspot puedes revisar otras formas de obtenerlas en [IP Raspberry](https://www.raspberrypi.org/documentation/remote-access/ip-address.md)
 
Necesitaremos instalar Putty, es un cliente SSH desarrollado  para Windows. PuTTY es un software de código abierto que está disponible con código fuente. Para descargar visita [Putty](https://www.putty.org/)
 
Al instalar Putty nos aparecerá lo siguiente y tenemos que seleccionar lo que se muestra marcado en la imagen.

![puttymediumintal](https://user-images.githubusercontent.com/79243784/116726205-95eeff00-a9a8-11eb-888f-6ccdc74bf818.png)

Al iniciar nos aparecerá la siguiente ventana, en donde ingresamos la IP de nuestra Raspberry. Después daremos clic en open.
Nos arrojará un mensaje de alerta en el que daremos clic en Sí.

![puttyMEDIUM](https://user-images.githubusercontent.com/79243784/116726263-a69f7500-a9a8-11eb-877a-61de557b3cc3.png)

Después de dar clic en sí, aparecerá la ventana en donde se ingresará el usuario si no fue cambiada la contraseña y el usuario de fábrica viene como usuario pi y la contraseña que establecimos en los pasos anteriores como raspberry.

![loginuserMEDIUM](https://user-images.githubusercontent.com/79243784/116726299-b3bc6400-a9a8-11eb-9af8-af93e9c0e0f4.png)

Después de ingresar nuestro usuario nos pedirá la contraseña.

![passworduserMEDIUM](https://user-images.githubusercontent.com/79243784/116726317-b9b24500-a9a8-11eb-90e6-8d9ab857772d.png)

Una vez ingresada la contraseña nos mostrará la ventana como muestra la figura y tendremos acceso total al Shell de nuestra Raspberry. Ahora vamos a configurarla para obtener acceso a el escritorio.

![inMEDIUM](https://user-images.githubusercontent.com/79243784/116726393-d0f13280-a9a8-11eb-96a5-2c61ba9c3781.png)


## 4.VNC
 
A veces no es conveniente trabajar directamente en la Raspberry Pi. Quizás te gustaría trabajar en él desde otro dispositivo por control remoto como tu laptop. VNC es un sistema gráfico de uso compartido de escritorio que le permite controlar de forma remota la interfaz de escritorio de una computadora (con VNC Server) desde otra computadora o dispositivo móvil (con VNC Viewer). VNC Viewer transmite el teclado y el mouse o los eventos táctiles al VNC Server y, a cambio, recibe actualizaciones en la pantalla. Verás el escritorio de la Raspberry Pi dentro de una ventana en tu computadora o dispositivo móvil. Podrás controlarlo como si estuvieras trabajando en la propia Raspberry Pi. En pocas palabras es muy similar a usar TeamViewer.
Desde Putty ingresamos a la terminal de nuestra Raspberry. Una vez en nuestra terminal ingresamos el comando:
 
 
```
sudo raspi-config
```

![sudoraspiconfigMEDIUM](https://user-images.githubusercontent.com/79243784/116726482-f41be200-a9a8-11eb-9bd7-fdca2796dffc.png)


Nos dirigiremos a la siguiente ventana y seleccionaremos la opción 3 "Interface Options".

![SUDOINTERFACEOPTIONESMEDIUM](https://user-images.githubusercontent.com/79243784/116726512-0269fe00-a9a9-11eb-82fb-fde953578709.png)

Ahora nos aparecerán las siguientes opciones, seleccionaremos VNC.

![VNCMEDIUM](https://user-images.githubusercontent.com/79243784/116726547-0f86ed00-a9a9-11eb-9e95-eedd4d13adf6.png)

Confirmaremos que queremos habilitar el servidor VNC.

![VNCyesMEDIUM](https://user-images.githubusercontent.com/79243784/116726568-16156480-a9a9-11eb-84b7-574234f2e0af.png)

Volveremos al menú sudo raspi-config, ahora seleccionaremos "Display Options"

![DisplaYMEDIUM](https://user-images.githubusercontent.com/79243784/116726595-1e6d9f80-a9a9-11eb-84ea-64ac2ed54e24.png)

Ahora seleccionaremos D1 Resolution. Para configurar una resolución que no tenga problemas con nuestro equipo.

![RESOLUTIONmedium](https://user-images.githubusercontent.com/79243784/116726655-32190600-a9a9-11eb-8b1c-56fb42bbb700.png)


Seleccionaremos DMT Mode 85. La resolución 1280 x 720 es compatible con la mayoría de los equipos actuales, en caso de que no se vea muy bien en tu equipo intenta utilizar alguna de las demás opciones con menor resolución. 

![DTMresolutionMEDIUM](https://user-images.githubusercontent.com/79243784/116726729-4bba4d80-a9a9-11eb-8915-5e58d4d98941.png)

![RESOLUTIONokmediUM](https://user-images.githubusercontent.com/79243784/116726754-55dc4c00-a9a9-11eb-97ba-cd637bc9c66b.png)


Al confirmar nos preguntará si queremos reiniciar, mi recomendación es la opción "YES". Después de reiniciar estará lista nuestra Raspberry para poder ingresar por primera vez a el Escritorio.

![YESrebootMedium](https://user-images.githubusercontent.com/79243784/116726902-81f7cd00-a9a9-11eb-96dc-383bbc8f8908.png)

Tenemos que instalar VNC en nuestro ordenador, para descargar visite [VNC Download](https://www.realvnc.com/es/connect/download/viewer/), una vez instalado puede abrir el programa, ingresamos en la parte superior la IP de nuestra Raspberry.

![VNCmedium2](https://user-images.githubusercontent.com/79243784/116726967-96d46080-a9a9-11eb-85cf-00ba1f1bfa29.png)

Nos aparecerá la siguiente ventana donde ingresamos el nombre de usuario y contraseña de nuestra Raspberry Pi. Daremos en aceptar y nos mostrará el escritorio de Raspberry Pi.

![inicioVNCmedium](https://user-images.githubusercontent.com/79243784/116726987-9c31ab00-a9a9-11eb-82c1-cd3b402d6302.png)

Una vez ingresado desde nuestro ordenador Windows podremos ver el escritorio de nuestra Raspberry Pi remotamente, daremos clic en ok en la ventana warning y procederemos a seguir los siguientes pasos:
 
1.- Cuando inicie su Raspberry Pi por primera vez, aparecerá la aplicación Bienvenido a Raspberry Pi y lo guiará a través de la configuración inicial. Haga clic en Next para iniciar la configuración.

![inicioRaspMEDIUM](https://user-images.githubusercontent.com/79243784/116727044-abb0f400-a9a9-11eb-8f14-025c30ee7f29.png)

![NEXTmediuminicio](https://user-images.githubusercontent.com/79243784/116727522-4dd0dc00-a9aa-11eb-8f97-e13f60915045.png)

Configure su país, idioma y zona horaria, luego haga clic en Next nuevamente.

![countriraspbMEDIUM](https://user-images.githubusercontent.com/79243784/116727082-b8354c80-a9a9-11eb-80f4-93d92d54022d.png)

Nos dara la opcion de Ingresar una nueva contraseña para su Raspberry Pi, no es necesario cambiar la contraseña, de fábrica Raspberry tiene como usuario pi y contraseña raspberry, el cambio es solo por seguridad. y haga clic en Next.

![SETPASSWORDmedium](https://user-images.githubusercontent.com/79243784/116727123-c71bff00-a9a9-11eb-95f9-d4734d3a0522.png)

Nos dara la opcion de eliminar los bordes negros en una pantalla, como estamos utilizando un servidor remoto no podemos ver los bordes que normalente aparecerian si conectaramos nuestra Raspberry por HDMI asi que esta opcion la omitiremos y daremos click en Next.

![setupscreenMEDIUM](https://user-images.githubusercontent.com/79243784/116727147-cd11e000-a9a9-11eb-85de-854635d46cc1.png)

Nos permitirá conectarnos a otra red inalámbrica seleccionando su nombre, ingresando la contraseña (**Cambiar la red mientras estás en SSH o VNC hará que se cierre automáticamente la aplicación, las Raspberry tienen una IP dinamica que cambia cada con cara red nueva que se conecta, tendrás que ingresar la nueva IP de la red para volver a acceder remotamente**),continuaremos con la configuración haciendo clic en Next.

![NETWORKmedium](https://user-images.githubusercontent.com/79243784/116727183-d4d18480-a9a9-11eb-911a-eaf52de16e9d.png)

Nos aparecera la opcion de actualizar lo mas recomendable es dar en Next y dejar que el asistente busque actualizaciones del sistema operativo Raspberry Pi y las instale (esto puede llevar un poco de tiempo).

![updateMEDIUM](https://user-images.githubusercontent.com/79243784/116727213-ddc25600-a9a9-11eb-9055-ab4fb34cf48d.png)

Sí la actualización se ejecutó de manera exitosa nos aparecerá la siguiente ventana , en caso de que fallara lo mejor es seguir las indicaciones y después, por Putty en SSH ingresar los comandos:
 
1. sudo apt update
2. sudo apt full-upgrade
 
Si todo salió bien daremos click en Ok.

![readyMEDIUM](https://user-images.githubusercontent.com/79243784/116727267-f16dbc80-a9a9-11eb-85fc-ca4a39865bf6.png)

Haremos clic en Restart para finalizar la configuración.
 **Nota: Solo necesitará reiniciar si es necesario para completar una actualización.**

![REBOOTAGAINmedium](https://user-images.githubusercontent.com/79243784/116727306-fdf21500-a9a9-11eb-9145-cc3199afab0c.png)

Con estos pasos completados nuestra Raspberry ya está lista para que la utilicemos para nuestros proyectos. Ahora podrás ingresar por cualquiera de los métodos anteriores a tu Raspberry y crear con esta herramienta.
 
Sí quieres saber mas a cerca de como iniciar por primera vez en Raspberry visita su pagina oficial [Setting up Raspberry](https://projects.raspberrypi.org/en/projects/raspberry-pi-setting-up)
 
En caso de que te interese puedes revisar la guia de como instalar Visual Studio Code y Git en Raspberry Pi.

