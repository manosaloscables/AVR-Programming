Código y Ejemplos de "Make: AVR Programming"
==============================================

Bienvenidos!
--------

Aquí encontrarás todo el código (y más) para el libro de Maker Media
 [Make: AVR Programming](http://shop.oreilly.com/product/0636920028161.do).

Las diferencias principales entre este repositorio y el original son:

1. El código original está orientado al microcontrolador ATmega168 y sus variantes, mientras que el código en este repositorio está adaptado al attiny45 20PU.
2. Este repositorio está en español.

ADVERTENCIA! Este es un trabajo en proceso y no está terminado.


Getting Started
---------------

* Primero, descargar los contenidos de este repositorio en tu disco duro. La manera más fácil es con el botón "Download ZIP" que se encuentra en la parte superior derecha de esta página web. Extrae los contenidos del archivo zip a tu conveniencia. (Eres libre de clonar el repositorio si usas Git.)

* La mayoría de los proyectos comparten un set común de definiciones de pines y una librerial serial USART común y simple en el directorio **AVR-Programing-Library**. Los archivos make que se incluyen dependen por defecto de esta estructura del directorio, por ello no muevas las carpetas a menos que también cambies la ruta hacia los archivos incluídos en el archivo make.
  
* If you're using the Arduino IDE, you'll want to copy the **AVR-Programming-Library** directory
  into your **sketchbook/libraries** folder.  If you don't know where this is, you can find out in the 
  "File...Settings" dialog within Arduino.  Now you can link your code to use this library simply
  using "Sketch...Import Library" and selecting the library from the the menu.

* Now you will be set to open the code, edit it, and flash it into the AVR following the directions
  in the book.
  
  
Repo Layout
-----------

All of the project code is organized by the chapters in the book.  So if
you're looking for an example of some SPI code, see the "Chapter16_SPI" folder for 
SPI-related projects.  That's obvious.

But a bunch of the projects are interesting in addition to the topic covered in
the chapter.  For instance, "Chapter05_Serial-IO" includes a project that uses
the serial communication between your desktop computer and the AVR to turn your
computer keyboard into a musical keyboard that plays notes generated on the
AVR, turning it into a serial-port-controlled organ.  You wouldn't think to 
go looking in the Serial I/O chapter unles you were following along in the book. 

So for an overview all the projects, the file [allProjectsList](https://github.com/hexagon5un/AVR-Programming/blob/master/allProjectsList) lists them all out by name.  

setupProject
------------

If you'd like a blank template to start writing your own AVR code, 
have a look in the **setupProject** directory that I've included here. Inside, you'll find 
**main.c** and **main.h** files that are essentially blank and ready to go.  **main.c** 
makes use of my simple USART library, which is also included an linked in by the **Makefile**. 
In short, you could copy this directory, rename files, and start using it in your own projects.

But you don't have to do that manually.  Running *python setupProject.py
myProjectName* will create a directory called **myProjectName** for you, copy
the blank main files, renaming them as appropriate, and set up the Makefile
accordingly.  All that's left for you to do is the hard part -- actually
coding.  

If you use this setup a lot, you'll want to personalize the **Makefile** and
the two **main** files to suit your own preferences.  That way, whenever you
start up a new project, it'll include a customized **Makefile** that has your
programmer, chip type, and favorite baud rate already set.   

Finally, if you like to map out your pin definitions in macro definitions, run
*python createPinDefines.py*.  The program will ask you what you'd like to call
each pin macro (e.g. "LED0") and then which pin on the AVR you'd like to
associate with it (e.g. "PB1").  When you're done entering your pin layout,
it'll create a "pinDefines.h" file with (I hope) nicely-named macros.  Move
this file into the right directory, and include it in your code.  Calling
LED0_SET_HIGH will turn your LED on.


More!
-----

You've read the book, you've built the projects, you've worked through the code.
But still you hunger for more projects, more examples, more, more, more!
If I may toot my own horn, you should visit [LittleHacks.org](http://littlehacks.org)
where I blog about whatever microcontroller projects I'm currently up to.  

In particular, if you're reading
 [Make: AVR Programming](http://shop.oreilly.com/product/0636920028161.do), and
you're interested in fully-elaborated versions of the projects with more
photos, videos, and explanation than could fit in a book, head on over to
 [LittleHacks.org's AVR-Programming Section](http://littlehacks.org/AVR-Programming).  

Once you've exhausted all of these resources, you should *definitely* head over
to [The Cornell University ECE 4760 Final
Projects](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/)
list page.  It's an awe-inspiring collection of applications, and sure to spark
some creative thoughts.  It's all well-documented and there's tons of source
code in C.  [Professor Land's links section]
(http://people.ece.cornell.edu/land/courses/ece4760/#links) is also top-notch,
and his lectures on YouTube are also worth a look if you're getting serious
about this whole AVR deal.  






