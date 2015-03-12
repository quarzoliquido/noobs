# NOOBS (New Out of Box Software)
#### Instalador de sistemas operativos facil de usar para Raspberry Pi 

NOOBS esta pensado para que el proceso de elegir un sistema operativo especifico para Raspberry Pi e instalarlo sea facil y sin necesidad de gestionar a mano las imagenes de la memoria SD.

La ultima version de NOOBS, de caracter oficial, esta disponible para su descarga en el siguiente enlace  http://downloads.raspberrypi.org/NOOBS_latest

Si desea informacion de versiones anteriores y listas de modificaciones realizadas a las mismas, consulte el siguiente enlace https://github.com/raspberrypi/noobs/releases

![alt text](http://downloads.raspberrypi.org/NOOBS/screenshots/os_installed.png "Interface NOOBS")

### Acerca de NOOBS 
NOOBS en el primet boot procedera a formatear su tarjeta SD, dejandole que elija cuales Sistemas Operativos instalara de una lista con todas las opciones. Esta lista de Sistemas Operativos se genera automaticamente tanto de Sistemas Operativos que se hallan en su propia maquina (es decir, estan dentro del directorio `/os` en su disco) como de aquellos disponibles desde nuestro repositorio remoto, para lo cual es necesaria una conexión cableada a internet. 

Para que ud. disponga de la version mas reciente de su Sistema Operativo, en el menu solamente se desplegaran las ultimas actualizaciones de cada Sistema Operativo.

Para los siguientes boots es posible reemplazar facilmente su Sistema Operativo presionando la tecla SHIFT, la cual muestra la interfaz NOOBS y permite reinstalar comodamente su proximo Sistema Operativo.

La interfaz NOOBS entrega los siguientes servicios:
- <b>Install</b>: Ofrece instalar los sistemas operativos de la lista en su tarjeta SD. Si ud. cambia esta opcion, elimina todo sistema operativo instalado anteriormente.
- <b>Edit Config</b>: Esta opcion abre un editor de texto para cambiar la linea de comandos (cmdline) y configurar de esta manera el sistema operativo instalado.
- <b>Online Help</b>: [Si ud selecciona esta opcion necesita acceso a internet] Al elegir esta alternativa, ud. abre un navegador que muestra el foro Raspberry Pi ( http://www.raspberrypi.org/phpBB3/ ), el cual permite a los usuarios acceder facilmente a respuestas de utilidad para resolver inconvenientes.
- <b>Exit</b>: Esta es la salida de NOOBS y deja a su Raspberry Pi en el menu boot.
- <b>Language Selection</b>: Desde esta opcion puede cambiar el lenguaje en el que lee NOOBS.
- <b>Keyboard Layout Selection</b>: Aca puede elegir la distribucion del teclado a usar.
- <b>Display Mode Selection</b>: NOOBS tiene por omision salida al puerto de video HDMI en la resolucion que su monitor tenga seleccionada, incluso si no hay pantalla HDMI. If you do not see any output on your HDMI display or are using the composite output, press 1, 2, 3 or 4 on your keyboard to select HDMI preferred mode, HDMI safe mode, composite PAL mode or composite NTSC mode respectively.

Por favor, note que todas las configuraciones de usuario (language, keyboard layout, display mode) seran mantenidas entre un boot y otro e igualmente seran llevadas a los sistemas operativos existentes. Esto implica que si ud puede ver la interfaz NOOBS en su monitor, entonces podra igualmente ver la linea de comandos o la interfaz grafica de usuario de su sistema operativo. 

### Configuracion

Para configurar mediante NOOBS una tarjeta SD en blanco card necesita realizar las siguientes acciones:
- Primero, tiene que dar formato a una tarjeta SD de capacidad igual o superior a 4GB en el sistema de ficheros FAT (vea las instrucciones para realizar esto abajo)
- Segundo, tiene que descargar y extraer los archivos desde el archivo comprimido "zip" de NOOBS.
- Tercero, tiene que copiar los archivos extraidos en la tarjeta SD que ud. acaba de formatear, por ende, esos archivos estaran disponibles en el directorio root de la tarjeta SD.
<b> En algunos casos es posible extraer los archivos en una carpeta, si este es el caso por favor haga una copia entre los archivos habiendo entrado previamente dentro de la carpeta en vez de copiar la carpeta en si.</b>

Al hacer boot por primera vez la particion con el sistema de ficheros FAT de tipo "RECOVERY" sera cambiada al menor tamano posible y el menu mostrara una lista de sistemas operativos par instalar.

### Como darle formato con sistema de ficheros FAT a una tarjeta SD

Nosotros recomendamos a los usuarios de <b>Windows</b> formatear su tarjeta SD usando la SD Association's Formatting Tool, la cual esta lista para ser descargada en https://www.sdcard.org/downloads/formatter_4/ ud. necesitara configurar la opcion "FORMAT SIZE ADJUSTMENT" en "ON" dentro del menu "Options" para asegurar que se de formateo a la  tarjeta SD completa, en vez de una particion individual. Si desea mayor informacion e instrucciones para principiantes, abra la siguiente pagina http://www.raspberrypi.org/quick-start-guide

La herramienta "SD Association's Formatting Tool" tambien se encuentra disponible para los usuarios <b>Mac</b> ,si bien, la herramienta por omision llamada "OSX Disk Utility" tambien permite formatear el disco por completo, para lo cual solo requiere de elegir el volumen de la tarjeta SD card y seleccionar "Erase" con formato "MS-DOS").

Para usuarios <b>Linux</b> nosotros aconsejamos dar formato mediante `gparted` o a traves de la herramienta en linea de comandos conocida como `parted`). (Update: Norman Dunbar ha escrito el siguiente instructivo para dar formato siendo usuario de Linux: http://qdosmsq.dunbar-it.co.uk/blog/2013/06/noobs-for-raspberry-pi/ )

===

### Capturas de pantalla

#### Instalacion del Sistema Operativo

Elija la "checkbox" al lado del sistema operativo que desea instalar usando un mouse o teclado. Si usa teclado, presiones las teclas de flecha para cambiar entre sistemas operativos, luego cliquee el icono "Install" (o presione "i" en su teclado) para instalar el sistema operativo. Los iconos mostrados a la derecha de la lista los cuales indican el sistema operativo a instalar desde la tarjeta SD (con el icono SD correspondiente) o desde el repositorio en internet (vea el icono Ethernet correspondiente).

![alt text](http://downloads.raspberrypi.org/NOOBS/screenshots/os_selected.png "Elija los sistemas operativos a instalar")

#### Encuentre ayuda en la red a traves de su navegador

El navegador de internet incluido por omision conocido como "Arora" hace mucho mas facil encontrar apoyo en los foros de Raspberry Pi Forum, esto necesita de internet por medio de conexion cableada.

![alt text](http://downloads.raspberrypi.org/NOOBS/screenshots/browser.png "Ud. puede realizar una busqueda para recibir ayuda en los foros Raspberry Pi forums usando el navegador que ya se encuentra incluido")

#### Editor de archivo de configuracion 

Existe un editor de archivos de configuracion instalado por omision que hace posible cambiar los datos en el archivo correspondiente en el sistema operativo resaltado en la lista del menu. Con este editor ud. puede agregar "license keys" a distintos sistemas operativos instalados a traves de la misma interfaz.

Note que el modo de salida de video elegido por el usuario al presionar las teclas numericas del 1 al 4 , los cuales correspoden a HDMId, HDMI VGA, Composite PAL y Composite NTSC, el cual sera configurado automaticamente en el archivo de texto plano `config.txt` de sus sistemas operativos instalados, por lo anterior no necesitara preocuparse por cambios a mano de las configuraciones de su monitor.

![alt text](http://downloads.raspberrypi.org/NOOBS/screenshots/config_editor.png "Sencilla configuracion de cualquier sistema operativo instalado")

#### Diapositivas de la instalacion 

Ud. podra entender los primeros pasos de la instalacion viendo las diapositivas a continuacion.

![alt text](http://downloads.raspberrypi.org/NOOBS/screenshots/installer_slides.png "Ud. podra entender los primeros pasos de la instalacion viendo las diapositivas a continuacion.")

#### Seleccion de Sistema Operativo en el Boot 

Despues de que haya instalado varios sistemas operativos, puede elegir con cual hacer boot por medio de este menu. En NOOBS es posible mantener la seleccion de sistema operativo realizada por ud. automaticamente esperando hasta un maximo de 10 segundos.

Si hay solo un sistema operativo installado no se mostrara el selector de boot y el sistema operativo sera iniciado automaticamente.

![alt text](http://downloads.raspberrypi.org/NOOBS/screenshots/boot_select.png "Elija facilmente cual sistema operativo desea dar inicio entre una lista de los que ha instalado previamente")

==

## Uso para expertos y pedagogos

### Como instalar de manera automatizada un sistema operativo

Si ud. esta utilizando su Raspberry Pi sin un monitor puede instalar un sistema operativo en particular facilmente, mediante NOOBS. Siga los pasos enumerados a continuacion para configurar de manera automatizada y sin pedir que el usuario haga input alguno para instalar un sistema operativo especifico:

1. Sirvase copiar la carpeta del sistema operatvo a instalar en el direcorio `/os`, o si lo prefiere, elimine todos los otros sistemas operativos que existen en el directorio `/os` para que asi solo permanezca el sistema operativo de su preferencia.

2. Si el sistema operativo que ud. desea copiar tiene multiples "sabores" o distribuciones, edite el archivo  `flavours.json` de modo tal que solo este en el fichero la entrada relacionada con el "sabor" o distribucion que ud. va a instalar.

3. Existe un archivo `recovery.cmdline` en el directorio root de NOOBS, editelo y agregue  `silentinstall` a la lista de  argumentos.

Durante el  boot mediante tarjeta SD con una version modificada por ud mismo de NOOBS en su Raspberry Pi, la cual instalara de manera automatizada el sistema operativo de su eleccion y hara boot en el mismo apenas la instalacion haya culminado.

### Instrucciones para personalizar la version de su Sistema Operativo en Raspberry Pi

Hay dos situaciones puntuales en las cuales podria sentirse impulsado a crear una version personalizada de los sistemas operativos estandar que se encuentran dentro de las alternativas de NOOBS para su instalacion en una Raspberry Pi:
- Puede que ud. sea un pedagogo que busca personalizar comodamente un sistema operativo el cual contenga un conjunto predefinido de paquetes y archivos en una cantidad determinada de tarjetas SD, por ejemplo, para entregar a un grupo de estudiantes sus correspondientes Raspberry Pi o quiza llevar rapidamente de vuelta a las configuraciones de fabrica un numero especifico de Raspberry Pi.
- Existe la necesidad de respaldar sus paquetes previamente instalados asi como sus archivos antiguos para que cualquier Sistema Operativo que use en un futuro no le obligue a volver a instalar, configurar y copiar tanto el sistema operativo como sus datos personales.

Si ud sigue los pasos enumerados a continuacion podra tener una copia modificada de los sistemas operativos estandar, dicha copia modificada contendra sus propios datos, paquetes y configuraciones.

1. Necesita descargar una version "base" de NOOBS, la cual se encuentra disponible en http://downloads.raspberrypi.org/NOOBS_latest

2. Debera extraer el archivo NOOBS comprimido en formato Zip 

3. Ingrese a la carpeta `os` 

4. Tendra que hacer una copia de la arpeta con el Sistema Operativo que ud modificara y personalizara.

5. Sera necesario editar los campos requeridos en el archivo `os.json` que existe en el interior de la carpeta que ud acaba de crear. 
  1. "name" - Cambie este campo por el nombre del Sistema Operativo "base" por el nombre de su propia version
  2. "description" - Modifique la descripcion del sistema opertivo estandar OS e instalado previamente por la descripcion de su propia version del Sistema Operativo

6. [Opcional] Puede cambiar de nombre o reemplazar el icono previamente existente llamado `<OS>.png` con el icono de su propia version del Sistema Operativo

7. [Opcional] Es perfectamente posible tener sus propias diapositivas de instalacion, en ingles "installer slides" cambiando las imagenes en formato PNG dentro de los directorios `slides` y `slides_vga` 

8. Cambie los siguientes campos en el archivo `partitions.json` que se encuentra en la carpeta o directorio creado recientemente 
  1. "partition_size_nominal" - Cambie la cifra por el tamano de las particiones en su propia version del Sistema Operativo
  2. "uncompressed_tarball_size" - Edite la cifra con el tamano al descomprimir de los archivos "Tarball" de su sistema de archivos 

9. Hay dos archivos de tipo "Tarball" para el "root" y "boot", con extencion `.tar.xz`, cambielos por sus propias copias personalizadas con su Sistema Operativo personalizado. Estas instrucciones tienen detras de si el supuesto de que instalara solamente un Sistema Operativo con NOOBS, todo lo aconsejado sera inutil si ud desea ejecutar multiples Sistemas Operativos en una sola tarjeta SD. Hay etiquetas puntuales en el archivo `partitions.json`, las cuales deben coincidir con el nombre de sus archivos de tipo "Tarball".
  1. Necesitara ingresa al sistema de archivos root de su propio Sistema Operativo personalizado. Tiene que hacer un "Tarball" del "Root" mediante la siguiente sintaxis en la linea de comandos: `tar -cvpf <label>.tar /* --exclude=proc/* --exclude=sys/* --exclude=dev/pts/*`. Posteriormente sera necesario comprimir el "Tarball" con la sintaxis que mostramos a continuacion `xz -9 -e <label>.tar`, en la misma interfaz de texto.
  2. Ingrese al directorio "Root" de la particion "Boot" de la version personalizada de su propio Sistema Operativo. Dentro de aquella carpeta o directorio, ejecute la siguiente sintaxis para crear un archivo "Tarball" para su "Root": `tar -cvpf <label>.tar .` Sera necesario comprimir el archivo "Tarball" con la sintaxis `xz -9 -e <label>.tar`.

### Modificacion del lenguaje por omision, disposicion del teclado, resolucion del monitor o particion de boot

Sera necesario editar el siguiente archivo : 
`recovery.cmdline` 
El cual se encuentra ubicado en el directorio root de NOOBS. Debera agregar los siguientes argumentos donde sea requerido:
- `lang=<two-letter language code>` (por ejemplo: `lang=de` or `lang=en`)
- `keyboard=<two-letter layout code>` (por ejemplo: `keyboard=de` or `keyboard=us`)
- `display=<display mode number>` (por ejemplo `display=1` or `display=3`)
- `partition=<partition_number>` (por ejemplo `partition=5`)

Todas las configuraciones de fabrica son modificadas por cualquier cambio hecho desde la Interfaz Grafica de Usuario.

### Como pasar de la pantalla "Recovery splashscreen" para hacer boot en una particion puntual

Si desea lograr que una particion especifica arranque desde el proceso de boot en el inicio mismo, realice los siguientes pasos. Una vez instalados sus Sistemas Operativos, agregue el siguiente archivo dentro del directorio root de NOOBS.

1. Por favor, agregue un archivo de texto plano con el nombre de `autoboot.txt`, en el mismo directorio root de NOOBS.

2. En el archivo `autoboot.txt` edite con la variable `boot_partition=<partition number>`y almacene el texto con la variable mencionada.

Con las acciones a seguir evitará que sea mostrada la splashscreen dentro del boot. El numero de particion puede encontrarse al ejecutar la sintaxis `sudo fdisk -l`, dicha particion tiene que ser una de las particiones en formato FAT32, en el siguient ejemplo `/dev/mmcblk0p5` seria la particion 5. Note que una vez hallado un archivo `autoboot.txt`, no hay forma de mostrar la interfaz grafica de usuario propia de NOOBS, a no ser que ud mismo elimine o cambie de nombre al archivo `autoboot.txt`.

===

## Solucion de problemas

#### Que hacer si no es detectada la tecla SHIFT 

Ud puede probar presionar SHIFT cuando aparezca la "splashscreen" de color gris en vez de presionarla durante el boot.

#### Como hacer boot en "Modo a prueba de fallos"

Es posible hacer boot en una consola busybox en vez de lanzar la interfaz grafica NOOBS GUI, elija uno de ambas medidas:

1. Dentro del directorio o carpeta NOOBS ubique `recovery.cmdline`y agregue `rescueshell` a la lista de argumentos.

2. Entre los pins 5 & 6 debe insertar un jumper de cabecera GPIO P1. Si ud. tiene hardware externo o una placa conectada a la cabecera GPIO, puede que encuentre el pin 5 presionado y por ende, habilitando accidentalmente el "Modo a prueba de fallos". Para prevenir que esto ocurra agregue al archivo `recovery.cmdline` que se halla en el directorio root de NOOBS el argumento  `disablesafemode`.

#### Como habilitar el  "Recovery Mode" usando el GPIO 

Normalmente solo se requiere de presionar la tecla `SHIFT` para entrar al "Recovery Mode" al entrar al boot y mostrar la interfaz NOOBS. Si carece de teclado o la tecla `SHIFT` no es detectada, sera necesario seguir los siguientes pasos de manera tal que aparezca en el boot la interfaz grafica NOOBS:

1.Entre a la linea de comandos, situe el directorio root de NOOBS.  Elija el archivo `recovery.cmdline` y agregue  `gpiotriggerenable`.
2. Haga Reboot

Puede forzar el "Recovery Mode" cuando su Raspberry Pi esta en proceso de boot, tan solo conecte el pin 3 GPIO pin en la cabecera P1 a GND (pin 25). Si el Pin 3 GPIO pin se mantiene desconectado entonces el boot ocurrira hacia el Sistema Operativo instalado, de manera rutinaria.

#### Como forzar el "Recovery Mode" en el boot (sobreescribe GPIO o la entrada por teclado)

Para entrar al "Recovery Mode" ud. puede usar tanto el GPIO como el teclado, sera necesario hacer lo siguiente:

1. Dirijase al directorio root en NOOBS. Edite el archivo `recovery.cmdline` y agregue `forcetrigger` a la lista de argumentos.
2. Haga Reboot

Note que al habilitar esta opción tendra el "Recovery Mode" <b>cada vez</b> que haga boot desde su tarjeta SD con NOOBS, hasta que edite nuevamente el archivo `recovery.cmdline`.

#### How to disable using the keyboard to trigger entering Recovery Mode

In some rare cases, you may find that NOOBS incorrectly detects a `SHIFT` keypress from your keyboard regardless of the presence of user input. In such cases it may be helpful to disable using the keyboard to trigger Recovery Mode being entered.

To prevent a `SHIFT` keypress from entering Recovery Mode on boot (maybe you have a problematic keyboard which is erroneously triggering every time you boot), you can:

1. Append `keyboardtriggerdisable` to the argument list in the `recovery.cmdline` file which is found in the root NOOBS directory.
2. Reboot

#### How to change display output modes

By default, NOOBS will output over HDMI at your display’s preferred resolution, even if no HDMI display is connected. If you do not see any output on your HDMI display or are using the composite output, press 1, 2, 3 or 4 on your keyboard to select HDMI preferred mode, HDMI safe mode, composite PAL mode or composite NTSC mode respectively.

If you don't have a keyboard, you can still change the display mode used by NOOBS through editing the `recovery.cmdline` file in the root NOOBS directory prior to first boot and appending the following argument:
- `display=<display mode number>` (e.g. `display=1` or `display=3`)

===

## How to Rebuild NOOBS

Note that this will require a minimum of 6GB free disk space.

#### Get Build Dependencies

On Ubuntu:

`sudo apt-get install build-essential rsync texinfo libncurses-dev whois unzip`

#### Run Build Script

`./BUILDME.sh`

Buildroot will then build the software and all dependencies, putting the result in the `output` directory.

Buildroot by default compiles multiple files in parallel, depending on the number of CPU cores you have.

If your build machine does have a quad core CPU, but relatively little RAM, you may want
to lower the number to prevent swapping:
- `cd buildroot ; make menuconfig`
- "Build options" -> "Number of jobs to run simultaneously"

## How to run your Build

In order to setup an SD card with a newly built version of NOOBS, you will need to:
- Format an SD card that is 4GB or greater in size as FAT
- Replace the `/os` directory in `/output` with the copy contained in the release version of NOOBS (see above for download links)
- Copy the files in the `/output` directory onto the SD card

## About the Buildroot infrastructure

To add extra packages: `cd buildroot ; make menuconfig`

Recovery software packaging is in: `buildroot/package/recovery`

Kernel configuration used: `buildroot/kernelconfig-recovery`

Main differences with bcmrpi_defconfig:
- `CONFIG_BLK_DEV_INITRD=y` - initramfs support
- `CONFIG_INPUT_EVDEV=y` - evdev support built-in
- `CONFIG_USB_HID=y` - usb HID driver built-in
- All modules disabled.

## Modifying Qt source

Source is in the `recovery` folder.
Be aware that user interface screens will appear larger in Qt Creator then when deployed on the Pi, can
raise font sizes 2 points to compensate.

Several constants can be changed in `config.h`

Wrap code that calls Qt Embedded specific classes (such as QWSServer) between
```C
#ifdef Q_WS_QWS
```
and
```C
#endif
```
so that the project also compiles and can be tested under standard Qt.

## Adding/Updating Translations

References:

http://qt-project.org/doc/qt-4.8/i18n-source-translation.html

http://qt-project.org/doc/qt-4.8/linguist-manual.html

To set up a git pre-commit hook to automatically update the translation files, run the following commands in the project root:
- `chmod +x pre-commit-translation-update-hook.sh`
- `cp pre-commit-translation-update-hook.sh .git/hooks/pre-commit`

To add a new translation:
- Add to `recovery/recovery.pro` the following: `TRANSLATIONS += translation_<languagecode>.ts`
- Run `lupdate recovery/recovery.pro` which extracts strings from the source code and generates/updates the *.ts* files.
- The *.ts* can then be sent to the translator, opened in Qt Linguist and filled in.
- Add a line for the *.ts* file in to `recovery/icons.qrc`, but substitute *.ts* extension with *.qm* . This file contains a list
  of resource files that will be embedded into the application's executable during build.
- Add a flag icon for your language from http://www.famfamfam.com/lab/icons/flags/ flag icon collection or if it
  doesn't have the one you need, you may use some other small png icon for it. Copy the icon file to the `recovery/icons`
  folder and add a line for it into `recovery/icons.qrc` as well.


### Legal compliance

Copyright (c) 2013, Raspberry Pi
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
Neither the name of the Raspberry Pi Foundation nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

#### Third party licenses:

Recovery software directly links to:
- Qt libraries, available under LGPL and commercial license.

Currently used icon sets:
- http://www.fatcow.com/free-icons - Creative commons Attribution license
- http://www.famfamfam.com/lab/icons/flags - "These flag icons are available for free use for any purpose with no requirement for attribution."
- http://www.oxygen-icons.org/ - Available under Creative Common Attribution-ShareAlike 3.0 and LGPL license

Licenses of utility software build by buildroot:
Type `cd buildroot ; make legal-info` to generate a list, which will be available under `output/legal-info`.
