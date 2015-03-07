# NOOBS (New Out of Box Software)
#### Un instalador de sistemas operativos para Raspberry Pi facil de usar

NOOBS esta pensado para que el proceso de elegir un sistema operativo especifico para Raspberry Pi e instalarlo sea facil y sin hacer manualmente el procesod e gestionar imagenes de la memoria SD.

La ultima version de NOOBS, de caracter oficial, esta disponible para su descarga desde  http://downloads.raspberrypi.org/NOOBS_latest

Si desea informacion de versiones anteriores y listas de modificaciones a las mismas, sirvase entrar al siguiente enlace https://github.com/raspberrypi/noobs/releases

![alt text](http://downloads.raspberrypi.org/NOOBS/screenshots/os_installed.png "Interface NOOBS")

### Acerca de NOOBS 
NOOBS en el primet boot procedera a formatear su tarjeta SD, dejandole que elija cuales sistemas operativos instalara, en una lista con todas las opciones. Esta lista de sistemas operativos se genera automaticamente tanto de sistemas operativos disponibles localmente (i.e. los cuales esten dentro del directoro `/os` en su disco) como de aquellos disponibles desde nuestro repositorio remoto, lo cual exige una colección a internet cableada

Para que ud. tenga la version mas reciente de su sistema operativo el menu solamente muestra las ultimas actualizaciones de cada sistema operativo.

Para los siguientes boot es posible reemplazar facilmente su sistema operativo presionando la tecla SHIFT, la cual muestra la interfaz NOOBS y permite reinstalar comodamente su proximo sistema operativo.

La interfaz NOOBS interface entrega los siguientes servicios:
- <b>Install</b>: Ofrece instalar los sistemas operativos de la lista en su tarjeta SD. Si ud. cambia esta opcion elimina todo sistema operativo instalado previamente.
- <b>Edit Config</b>: Esta opcion abre un editor de texto para cambiar la cmdline y configurar asi el sistema operativo instalado.
- <b>Online Help</b>: [Si ud selecciona esta opcion necesita acceso a internet] Al elegir esta alternativa ud. abre un navegador que muestra el foro Raspberry Pi Forum ( http://www.raspberrypi.org/phpBB3/ ), el cual tiene informacion de ayuda y de utilidad para resolver problemas de facil acceso.
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

#### OS Boot Selector

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

There are two main use cases for which you may want to create a custom version of one of the standard OS releases that is suitable for installation via NOOBS:
- If you are a teacher wanting to easily deploy a custom OS release containing pre-defined set of packages and files onto a number of SD cards (e.g. to provision a class set of Raspberry Pi's or quickly restore a Raspberry Pi back to custom "factory" settings).
- If you want to be able to back up your existing installed packages and files so that any future OS re-install does not force you back to a clean install.

The following steps allow you to create a modified copy of one of the standard OS releases that contains your custom files, packages and settings.

1. Download a base version of NOOBS from http://downloads.raspberrypi.org/NOOBS_latest

2. Extract the NOOBS zipfile

3. Navigate to the `os` directory

4. Create a copy of the folder containing the OS release that you want to modify and rename it with a custom name.

5. Edit the following fields in the `os.json` file contained in the folder that you just created
  1. "name" - replace the name of the base OS with the name of your custom OS version
  2. "description" - replace the description of the standard OS install with one for your custom OS version

6. [Optional] Rename or replace the existing `<OS>.png` icon file with one matching the name of your custom OS version

7. [Optional] Replace the PNG image files in the `slides` and `slides_vga` directory with your own custom installer slides

8. Edit the following fields in the `partitions.json` file contained in the folder that you just created
  1. "partition_size_nominal" - replace the numerical value with the size of the paritions in your custom OS version
  2. "uncompressed_tarball_size" - replace the numerical value with the size of your filesystem tarballs when uncompressed

9. Replace the `.tar.xz` root and boot filesystem tarballs with copies created from your custom OS version (these instructions assume you're only using a single OS at a time with NOOBS - they won't work if you're running multiple OSes from a single SD card). The name of these tarballs needs to match the labels given in `partitions.json`.
  1. To create the root tarball you will need to run `tar -cvpf <label>.tar /* --exclude=proc/* --exclude=sys/* --exclude=dev/pts/*` from within the root filesystem of your custom OS version. You should then compress the resulting tarball with `xz -9 -e <label>.tar`.
  2. To create the boot tarball you will need to run `tar -cvpf <label>.tar .` at the root directory of the boot partition of your custom OS version. You should then compress the resulting tarball with `xz -9 -e <label>.tar`.

### How to change the default Language, Keyboard layout, Display mode or Boot Partition

Edit the `recovery.cmdline` file in the root NOOBS directory and append the following arguments where relevant:
- `lang=<two-letter language code>` (e.g. `lang=de` or `lang=en`)
- `keyboard=<two-letter layout code>` (e.g. `keyboard=de` or `keyboard=us`)
- `display=<display mode number>` (e.g. `display=1` or `display=3`)
- `partition=<partition_number>` (e.g. `partition=5`)

Note that these defaults will be overwritten by any changes made in the GUI to these settings.

### How to bypass the Recovery splashscreen and boot directly into a fixed partition

After you have installed your chosen OSes, add the following file to the root directory of NOOBS to force the indicated partition to be booted at power-on.

1. Add a text file named `autoboot.txt` to the root directory of NOOBS.

2. Add `boot_partition=<partition number>` to the file and save it to disk.

This will also prevent the splashscreen from being displayed at boot. The partition number can be found by running `sudo fdisk -l` the partition will be one of the FAT32 partitions `/dev/mmcblk0p5` would be partition 5. Note that once an `autoboot.txt` file is present, there's then no way to force the NOOBS GUI to display, until you delete (or rename) the `autoboot.txt` file.

===

## Troubleshooting

#### What to do if your SHIFT keypress isn't detected

Try pressing shift only when the grey splashscreen is displayed rather than holding it from boot up.

#### How to boot into "Safe Mode"

To boot into a basic busybox shell rather than launching the NOOBS GUI, you can *either*:

1. Append `rescueshell` to the argument list in the `recovery.cmdline` file which is found in the root NOOBS directory.

2. Insert a physical jumper between pins 5 & 6 of GPIO header P1. If you have external hardware or an addon board connected to the GPIO header, you may find that pin 5 is being pulled low and accidentally triggering "Safe Mode". To prevent this you can append `disablesafemode` to the argument list in the `recovery.cmdline` file which is found in the root NOOBS directory.

#### How to enable using the GPIO to trigger entering Recovery Mode

To force Recovery Mode to be entered on boot and to show the NOOBS interface, you normally press the `SHIFT` key during bootup. If you don't have a keyboard or the `SHIFT` keypress isn't being detected, you should complete the following steps to force the NOOBS interface to be displayed on boot:

1. Append `gpiotriggerenable` to the argument list in the `recovery.cmdline` file which is found in the root NOOBS directory.
2. Reboot

To force Recovery Mode being entered on boot, connect GPIO pin 3 on header P1 to GND (pin 25). If GPIO pin 3 remains unconnected then it will boot through to the installed OS as normal.

#### How to force Recovery Mode being entered on boot (overrides GPIO or keyboard input)

Alternatively, if you are unable to use either the GPIO or keyboard to trigger entering Recovery Mode, you can:

1. Append `forcetrigger` to the argument list in the `recovery.cmdline` file which is found in the root NOOBS directory.
2. Reboot

Note that with this option enabled, the Recovery Mode will be displayed <b>every</b> time you boot from your NOOBS card (until you edit `recovery.cmdline` again).

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
