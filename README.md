Soporte de Huarya para instalar Scratch 2 

Este paquete agrega dependencias desde i386 para poder instalar Scratch 2.
Scratch esta hecho con Adobe Air, éste último solo funciona en 32Bits y **no
tiene** soporte oficial de Adobe.

Tenga en cuenta que tanto Air como Scratch 2 son **sofware privativo** ya que no 
es posible en principio acceder al código fuente.

¿Cómo usar este paquete?

Este paquete está pensado para ser instalado en arquitecturas amd64.
Por lo tanto debe agregar la arquitetura i386 al gestor de paquetes dpkg para
poder instalar las dependencias de 32bits en su sistema de 64bits. 
Es lo que en debian se denomina como multiarch.

    sudo dpkg --add-architecture i386
  
    sudo apt-get update
  
    sudo apt-get install huayra-scratch-multiarch

Hay 2 librerías libhal1 y libhal-storge1 que fueron agregadas al repositorio
de Huayra porque ésta aplicacion las necesita para poder realizar la instalación.

Ambas son obsoletas en debian ya que HAL fué reemplazada por UDEV y otras herramientas
por lo tanto no deberían usarse mas.

Una vez que pudo instalar éste paquete, puede seguir las instruciones del sitio
de Scratch para su instalación.

Primero bajar e instalar Adobe Air:

    wget http://airdownload.adobe.com/air/lin/download/2.6/AdobeAIRInstaller.bin

Instalación:

    chmod +x AdobeAIRInstaller.bin
    ./AdobeAIRInstaller.bin
    
Luego bajar Scratch 2:
  
    wget https://scratch.mit.edu/scratchr2/static/sa/Scratch-440.air
  
Finalmente instalarlo con la herramienta "Adobe Air Application Installer" que debería estar en su menu de accesorios.

De acuerdo a la Ley de Murphy tienen grandes chances de que Scratch2 funcione! 



