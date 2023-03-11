# Laboratorio 1 - Robotica.
En este repositorio, se realiza el desarrollo del laboratorio 1 de la asignatura robotica por el profesor: Pedro Fabian Cardenas Herrera Dr.-Ing. Y el profesor:
Msc-Ing. Jhoan Sebastian Rodriguez Rodriguez

### Integrantes:
- Julian Felipe Medina Veira <jmedinave@unal.edu.co>
- Santiago Andres Gomez Pena <sagomezpe@unal.edu.co>
- Santiago Dleon Sanchez Romero <ssanchezro@unal.edu.co>

#### Introducción:
El laboratorio tiene como objetivo general lograr una familiarización con el manipulador industrial IRB 140 y el entorno virtual de trabajo RobotStudio.

#### Descripción:
En esta práctica se desarrollarán 3 ejes temáticos:
- **Rutina de robot:** El primer componente es la comprensión del flujo de programa en RAPID, comprender los tipos de movimientos MOVJ y MOVL, así como sus restricciones.
- **Herramienta:** El segundo es el diseño y construcción de una herramienta a usar con el robot. Con esta herramienta se podrá comprender el concepto de MTH de Tool y se podrá realizar el proceso de calibración tanto en software como con el robot real (TCP).
- **Calibración de herramientas:** Comparación del proceso de calibración de la herramienta usando el robot real y empleando Robotstudio.

#### Desarrollo:
##### Herramienta:
Como base del laboratorio, se debe fabricar una herramienta que cumpla el rol de portar un marcador convencional que realizará la escritura en el tablero de las iniciales de los integrantes del equipo. 
Para diseñar esta herramienta se tuvo encuenta los siguientes aspectos:
- Material resistente y de bajo costo.
- Debe contar con una inclinación respecto al suelo para evitar la singularidad del robot.
- debe ser de un tamaño razonable por dos motivos: el primero, debe tener la suficiente rigidez para soportar las cargas al cual esta sometido y evitar vibraciones. Segundo no debe ser muy grande con el fin que este tenga mayor maniobrabilidad.
El material y el metodo seleccionado para fabricación fue Impresión 3D en PLC.
#####  Herramienta:
El CAD de la herramienta se encuentra adjunto con el nombre  <a href="https://github.com/jmedinave/Lab-1-robotica/blob/main/PortaMarcador.rar">PortaMarcador.</a>

###### Vista preliminar:
![portaMarcador](https://user-images.githubusercontent.com/49196705/224438179-a45928cc-002a-44af-8f96-74b85692bff3.png)

###### Plano PortaMarcador:
![Plano portamarcador](https://user-images.githubusercontent.com/49196705/224438218-44e6d103-376a-48c7-b80e-e1791289638a.png)

Es importante destacar que la longitud del Marcador redimencionará la altura de la herramienta, se dispone de un resorte para amortiguar la carga y del mismo modo que las longitudes no sean un problema al momento de ensayar la herramienta en el manipulador.

##### Robot Studio:
Para la creación de las rutinas se diseñó el código considerando letras de tamaño 5cm x 2cm ubicando los puntos necesarios para seguir una trayectoria de acuerdo con el sistema de coordenadas que corresponde al plato de la herramienta.

Se creó un punto de trabajo en la esquina superior izquierda del texto, sobre el cual se colocó los puntos relativos a las letras y los desplazamientos en vacío entre cada letra y entre el punto home, esto con el fin de facilitar la creación de rutinas y el desplazamiento del texto para trabajar en otras posiciones y orientaciones.

Para el caso de la herramienta se ingresó un dato de herramienta con desplazamientos de z = -80 mm y x = 160 mm desde el sistema de coordenados general desde el punto del plato y en la posición de home, con el fin de asegurar una distancia constante sobre el uso de la calibración manual mediante el uso del flex-pendant.

Para el primer caso de escritura se utilizó el punto de trabajo con un desplazamiento de x = 500 mm con respecto a la base del robot, necesitando incrementar el valor de la coordenada z = 13 mm para evitar una colisión fuerte con el suelo por la orientación de la herramienta, mientras que para el segundo caso se utilizó un desplazamiento de x = 500 mm, y = -300 mm, z = 13 mm y con una rotación de -40° con respecto al eje z.

##### Código:
El archivo de Robot Studio se encuentra adjunto con el nombre  <a href="https://github.com/jmedinave/Lab-1-robotica/blob/main/InicialesRobotStudio.rar">código.</a>

##### Videos simulación

##### Videos practica en robots reales
Despues de la validación de las rutinas en el programa de RobotStudio se procedio a implementar el codigo en los robots reales del laboratorio.

Primero se ejecuto el codigo que permitiera dibujar las iniciales en la superficie relativamente horizontal, en el siguiente video se puede observar el resultado.

Por ultimo se ejecuto el codigo en donde el interes fue dibujar las mismas letras pero de manera rotada de tal forma que se tuviera que modificar la orientacion del workobject, en el siguiente video se puede observar el resultado.
