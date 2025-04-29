# Tarea_BBDD_JP

## 1.Transformación y limipieza de los datos

Al tratarse de una tabla profesional, no necesitamos de una gran limpieza, los procesos realizados han sido:

### 1.1 Reducir cantidad de columnas

La tabla original contiene 84 columnas, un número excesivo para realizar el ejercicio, por lo que la reduzco a 16 columnas

### 1.2 Cambiar nombre columnas

Cambiamos el nombre de las columnas a uno mucho más amigable

### 1.3 Traducir una columna de inglés a español

Para trabajar más cómodamente con los datos, hay una columna que guarda datos en inglés por lo que la pasamos a español con un método bruto pero con buenos resultados, con ifs anidados

Creamos la columna “metodo_descubrimiento”, con la fórmula:

    =SI([@discoverymethod]="Radial Velocity";"Velocidad Radial";SI([@discoverymethod]="Imaging";"Imagen";SI([@discoverymethod]="Eclipse Timing Variations";"Variaciones de tiempo de eclipse";SI([@discoverymethod]="Transit";"Tránsito";SI([@discoverymethod]="Transit Timing Variations";"Variaciones de tiempo de tránsito";SI([@discoverymethod]="Astrometry";"Astrometría";SI([@discoverymethod]="Microlensing";"Microlente";SI([@discoverymethod]="Disk Kinematics";"Cinemática de disco";SI([@discoverymethod]="Orbital Brightness Modulation";"Modulación de brillo orbital";SI([@discoverymethod]="Pulsation Timing Variations";"Variaciones de tiempo en pulso";SI([@discoverymethod]="Pulsar Timing";"Tiempo entre pulsos";"Error en traducción"))))))))))) 
Esta fórmula sirve bien ya que no son muchos posibles datos y no cambian frecuentemente en el tiempo

### 1.4 Formato fecha aaaa en columna fecha_descubrimiento

Ajustamos el formato a uno personalizado para el año en el que se descubren los planetas

## 2. Análisis descriptivo de los datos
Por lo que entiendo en este apartado debo explicar de qué se tratan los datos analizados;
Se recogen datos publicados por la NASA recogidos desde 1992 hasta 2025 acerca de información relacionada con sistemas planetarios
Un sistema planetario está formado por una estrella central o varias, y distintos objetos orbitando a su alrededor. Nuestro sistema planetario es el sistema solar y está formado por el Sol, los diferentes planetas y una multitud de cuerpos menores.

Se recoge información como:

    • Nombre de planeta y sistemas
    • Número de estrellas y planetas en el sistema
    • Método de descubrimiento
    • Instalación donde se descubrió
    • Fecha del descubrimiento
    • Información de las órbitas (No usadas)
    • Masa,medida y distancia de los planetas
    • Temperaturas estrellas
    
## 3.Dashboard
![image](https://github.com/user-attachments/assets/6f3e0ee6-1d65-41dc-86e6-a6482dcfbfa3)


## 4. Informe explicativo del análisis
Gracias al análisis podemos observar que la tecnología mayormente usada para nuevos descubrimientos es el tránsito, que gracias a los filtros hemos podido ver que se empieza a usar cada vez más a partir de 2010

También podemos observar que la instalación KELT-SOUTH es con diferencia la que más descubrimientos ha aportado, al menos a nuestro registro

Datos en 2005:
![image](https://github.com/user-attachments/assets/c61b8a79-fd38-4eae-89fd-40a23aeceb1b)


Datos en 2024:
![image](https://github.com/user-attachments/assets/54c06571-2f5e-4f0c-9afe-1df2a05bee71)


2005
- 36 planetas
- 46 estrellas
- 11362 tamaño en tierras de promedio
- 325… parsecs desde la tierra
- Tecnología más usada: Velocidad Radial

2024
- 250 planetas (+214)
- 274 estrellas (+228)
- 6478 tamaño en tierras de promedio (ahora podemos encontrar planetas más pequeños y máss lejos)
- 766… parsecs desde la tierra (doble de distancia)
- Tecnología más usada: Tránsito















