![Titulo_github](https://github.com/Iranzubp/Grupo_2_IMH/blob/main/Dise%C3%B1o/T%C3%ADtulo.png)


## ¡Hola! 👋 

Somos un grupo de estudiantes del Master Dual Digital Manufacturing. Hemos realizado un proyecto de un robot de telepresencia en la asignatura de Tecnologías Industriales. A continuación dejamos unos links de interés:
  - [IMH] (https://www.imh.eus/es)
  - [Master Digital Manufacturing] (https://www.imh.eus/es/ingenieria-dual/master-industria-4-0)
  - [Web Robot] (https://iarakis.github.io/)
  - [Tareas Proyecto] (https://www.tactizity.com/iot)
  
## CAD y Prototipado 3D :straight_ruler: :triangular_ruler:

**La solución mecánica se diseñará en un programa de CAD a elección de los alumnos y dispondrá de los elementos necesarios para las funcionalidades anteriormente descritas, incluyendo la posibilida de controlar la inclinación del smartphone con un servomotor. Los componentes diseñados se imprimirán en una impresora 3D de IMH.**

Para llevar a cabo esta tarea se ha partido de unas piezas de CAD diseñadas digitalmente a las que se les ha hecho una modificación para poder incorporar el multisensor al robot. Mediante este dispositivo se obtienen las lecturas de los siguientes parámetros: temperatura, humedad, ruido, CO2 y TVOC. Hemos realizado la programación de este multisensor con el uso de Particle y Node-Red.

![Multisensor](https://github.com/Iranzubp/Grupo_2_IMH/blob/main/CAD%20y%20Prototipado%203D/Multisensor.PNG)
![CAD conjunto](https://github.com/Iranzubp/Grupo_2_IMH/blob/main/CAD%20y%20Prototipado%203D/CAD%20conjunto.png)

  
## Flujo y Visualización de Datos :computer: :bar_chart:

**En el proceso de fabricación de las piezas de plástico que componen el robot, la temperatura y humedad del proceso son parámetros clave. Esta tarea consiste en la realización de un flujo de datos en Node-Red para:**

**1-Visualizar una gráfica de los datos de temperatura y humedad.**

**2-Configurar un envío de alarma a tu email si se supera un valor del 70% de humedad.**

Con ayuda de Particle se ha realizado la programación correspondiente al Arduino que integra todos los sensores que recogen los datos ambientales del lugar en el que se encuentra el robot. A modo de ejemplo se muestra un fragmento del programa con extensión JSON así como una captura de otro fragmento del programa.

```js
void setup() {
	Serial.begin(9600); 
	pinMode(A2, INPUT);
	Serial.println("DHTxx test!");

Particle.variable("Temperatura", t);
Particle.variable("Humedad", h);
Particle.variable("CO2", co2);
Particle.variable("VOC", voc);
Particle.variable("Noise", n);
}
```

![Particle](https://github.com/Iranzubp/Grupo_2_IMH/blob/main/Flujo%20y%20Visualizacion%20de%20Datos/Particle.JPG)

Para llevar a cabo esta tarea se ha comenzado con el diseño del flujo en Node-Red considerando los diferentes datos conseguidos con el multisensor. Para mejorar la visualización de dichos datos en el dashboard se pueden ver una serie de gráficos acompañados de luces LED que indican el estado del dispositivo, así como unas notificaciones emergentes con recomendaciones. 

![Dashboard](https://github.com/Iranzubp/Grupo_2_IMH/blob/main/Flujo%20y%20Visualizacion%20de%20Datos/Dashboard.JPG)

Adicionalmente, en el menú de este dashboard, se tiene la opción de escaneo QR para probar la visualización de planos en realidad aumentada.

![QR](https://github.com/Iranzubp/Grupo_2_IMH/blob/main/Flujo%20y%20Visualizacion%20de%20Datos/Pantalla%20QR.png)


## Programación de Línea de Packaging :package: :wrench:

**Tras fabricar los robots de telepresecia, estos deben de ser enviados a su destino en lotes de diferente cantidad de unidades. El objetivo de esta tarea es programar una línea de clasificación por altura de cajas con robots. Para ello utilizaremos el software TIA PORTAL y FACTORY I/O.**

Se ha programado el sistema para comenzar su funcionamiento pulsando el botón de puesta en marcha. En función de la medida captada por el sensor de altura de las cajas, se dispone de tres clasificaciones: caja alta, caja baja o caja errónea. Con las dos primeras clasificaciones, el sistema sigue en marcha, mostrando una luz verde y separando las cajas bajas a la izquierda y las altas a la derecha, sumando una unidad al contador cada vez que una caja se desplaza a la izquierda o a la derecha. Con la clasificación de caja errónea, la cinta se para y se enciende una luz de alarma roja. Además, la cinta dispone de una seta de emergencia que permite parar el sistema de manera manual en caso de necesidad.

![Factory I_O](https://github.com/Iranzubp/Grupo_2_IMH/blob/main/Programacion%20de%20Linea%20de%20Packaging/Factory%20I_O.gif)


## Visualización con Tableau de Datos Ambientales :computer: :bar_chart:

Se ha empleado Tableau como herramienta de visualización que permite ver los datos ambientales del aula a través de una historia en la que se muestran los datos obtenidos por medio diferentes gráficas y mapas. En la historia, aparecen tres pestañas que permiten ver un enfoque global de los datos. La primera pestaña muestra los datos más relevantes de las condiciones ambientales. En las siguientes imágenes, se muestran gráficos que comparan el resto de datos obtenidos y enriquecen el análisis de las condiciones ambientales.

						https://public.tableau.com/profile/iranzu#!/vizhome/Grupo_2_IMH/Historia1?:showVizHome=no

![Tableau (1)](https://github.com/Iranzubp/Grupo_2_IMH/blob/main/Visualizacion%20con%20Tableau%20de%20Datos%20Ambientales/Tableau%20(1).png)
![Tableau (2)](https://github.com/Iranzubp/Grupo_2_IMH/blob/main/Visualizacion%20con%20Tableau%20de%20Datos%20Ambientales/Tableau%20(2).png)

## Webgrafía :link:  :space_invader:

- [3D Builder](https://www.3dnatives.com/es/3d-builder-software-gratuito-microsoft/)
- [Modelos 3D](https://www.thingiverse.com/)
- [Particle-Plataforma IoT](https://www.particle.io/)
- [Node-RED](https://nodered.org/)
- [Tableau-Software de analisis e inteligencia de negocio](https://www.tableau.com/es-es/why-tableau/what-is-tableau)
- [Factory IO-Simulador 3D](https://docs.factoryio.com/)


## Autores :black_nib: :black_nib:
- *Iranzu Barrado Pardo*
- *Laida Garcia Francisco*
- *Oihane Pizarro Barcena*
