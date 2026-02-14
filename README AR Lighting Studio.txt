AR Lighting Studio

Descripción

AR Lighting Studio es una aplicación web de Realidad Aumentada que permite previsualizar un set audiovisual con iluminación configurable. Utiliza A-Frame y AR.js para renderizar un entorno tridimensional anclado a un marcador físico (Hiro).

La aplicación permite modificar las dimensiones del set y ajustar un esquema clásico de iluminación de tres puntos en tiempo real.

Tecnologías utilizadas

A-Frame 1.4.2

AR.js

WebGL

HTML y JavaScript

Marcador Hiro

No requiere instalación de dependencias ni herramientas de compilación.

Requisitos

Dispositivo con cámara (computador o teléfono móvil)

Navegador moderno compatible con WebGL (Chrome recomendado)

Conexión mediante HTTPS o servidor local

Marcador Hiro impreso

El marcador Hiro puede descargarse desde el repositorio oficial de AR.js.

-Ejecución

Colocar el archivo index.html en una carpeta.

Iniciar un servidor local en esa carpeta, preferiblemente un live server desde Visual Studio Code

No abrir el archivo directamente con file://, ya que la cámara no funcionará.

-Funcionamiento general

La aplicación detecta el marcador Hiro mediante la cámara. Una vez reconocido, se genera un set virtual anclado al marcador.

El set incluye:

Un volumen tridimensional configurable.

Un piso con textura de referencia.

Tres paredes (posterior, izquierda y derecha).

Un objeto central intercambiable.

Sistema de iluminación de tres puntos.

Todo el contenido está contenido dentro de la entidad <a-marker> y se posiciona automáticamente respecto al marcador.

Control de dimensiones

El panel lateral permite modificar:

Ancho del set.

Alto del set.

Profundidad del set.

Al cambiar estos valores, se actualizan dinámicamente:

Dimensiones del volumen principal.

Posición vertical del volumen.

Tamaño del piso.

Posición y tamaño de las paredes.

La posición vertical del volumen se ajusta automáticamente en función de la altura seleccionada.

Sistema de iluminación

La escena incluye tres luces:

Key Light
Fill Light
Back Light

Cada luz permite modificar:

Intensidad.

Color.

Posición en los ejes X, Y y Z.

Las luces son de tipo Point Light y están representadas visualmente mediante una pequeña esfera emisiva que indica su ubicación dentro del set.

Los cambios se aplican en tiempo real.

Objetos de prueba

La aplicación incluye tres objetos intercambiables:

Esfera.

Cubo.

Cilindro.

Solo uno es visible a la vez. El botón "Change Object" permite alternar entre ellos.

Funciones adicionales

Reset Lights
Restablece dimensiones y parámetros de iluminación a los valores iniciales.

Show Volume
Activa o desactiva la visualización del volumen wireframe.

Alcance

La aplicación no realiza escaneo del entorno ni reconstrucción espacial. El volumen está anclado a un marcador fijo y no corresponde a medidas reales del espacio físico.

Su objetivo es servir como herramienta de apoyo para la comprensión espacial del comportamiento de la iluminación en un set audiovisual.