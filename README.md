# ## Laboratorio 1 - Robotica.
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
El CAD de la herramienta se encuentra adjunto con el nombre PortaMarcador.

###### Vista preliminar:
![portaMarcador](https://user-images.githubusercontent.com/49196705/224438179-a45928cc-002a-44af-8f96-74b85692bff3.png)

###### Plano PortaMarcador:
![Plano portamarcador](https://user-images.githubusercontent.com/49196705/224438218-44e6d103-376a-48c7-b80e-e1791289638a.png)

Es importante destacar que la longitud del Marcador redimencionará la altura de la herramienta, se dispone de un resorte para amortiguar la carga y del mismo modo que las longitudes no sean un problema al momento de ensayar la herramienta en el manipulador.


