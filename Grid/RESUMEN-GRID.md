Grid Layout es un sistema de diseño bidimensional en CSS que permite distribuir elementos HTML en filas y columnas de manera eficiente y controlada. A diferencia de Flexbox, que trabaja mejor en un solo eje (horizontal o vertical), CSS Grid permite un control total sobre ambos ejes, lo que lo hace ideal para crear diseños más complejos y estructurados.

Conceptos Fundamentales:

Grid Container (Contenedor de rejilla): Es el elemento que se declara con la propiedad display: grid;. Este contenedor define el contexto del grid.

Grid Items (Elementos de rejilla): Son los elementos hijos directos del grid container. Estos se posicionan automáticamente o manualmente en las celdas del grid.

Unidades de Medida:

CSS Grid acepta diversas unidades de medida para definir el tamaño de filas y columnas:

px (píxeles): Medida fija, no responde a cambios en el tamaño del viewport.

% (porcentaje): Proporcional al tamaño del contenedor padre.

em / rem: Relativas al tamaño de fuente del elemento o del documento.

fr (fracción): Unidad exclusiva de CSS Grid que representa una fracción del espacio disponible. Por ejemplo, 1fr 2fr divide el espacio total en 3 partes, asignando 1 parte a la primera columna y 2 partes a la segunda.

auto: Ajusta automáticamente el tamaño según el contenido del elemento.

Grid Template Columns y Rows:

Estas propiedades definen explícitamente la estructura de la rejilla en cuanto a columnas y filas.

grid-template-columns: Define la cantidad y el tamaño de las columnas.

grid-template-rows: Define la cantidad y el tamaño de las filas.

Ejemplo:

.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: 100px auto;
}

Este código crea un grid con 3 columnas: la primera y la tercera ocupan 1 fracción del espacio cada una, mientras que la segunda ocupa el doble. La primera fila mide 100px y la segunda se ajusta al contenido.

Grid Areas (Áreas de Rejilla):

Una de las características más poderosas de CSS Grid es la posibilidad de nombrar áreas y colocarlas de forma semántica.

Se usa la propiedad grid-template-areas en el contenedor.

Luego se asignan estas áreas a los elementos con grid-area.

Ejemplo:

.container {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-template-rows: auto auto;
  grid-template-areas:
    "header header"
    "sidebar content";
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.content { grid-area: content; }

Este diseño crea un encabezado que ocupa ambas columnas, y luego dos elementos: un sidebar a la izquierda y contenido principal a la derecha.

Grid Layout ofrece un sistema robusto y flexible para construir interfaces web modernas, con herramientas potentes como las fracciones (fr), las áreas nombradas y la capacidad de definir de forma explícita el tamaño y posición de cada elemento dentro de la rejilla.
