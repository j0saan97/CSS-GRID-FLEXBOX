RESUMEN DE CSS GRID
-------------------

1. ¿QUÉ ES GRID?
   - Sistema de diseño bidimensional para organizar contenido en filas y columnas.
   - Permite distribuir elementos fácilmente en layouts complejos y responsivos.

2. PROPIEDADES PRINCIPALES DEL CONTENEDOR (display: grid)
   - display: grid;
   - grid-template-columns: define columnas (ej: 1fr 2fr 1fr);
   - grid-template-rows: define filas (ej: 100px auto);
   - grid-template-areas: define zonas por nombre;
   - gap: espacio entre filas/columnas;
   - justify-items / align-items: alineación del contenido interno;

3. PROPIEDADES DEL ELEMENTO HIJO
   - grid-area: nombre del área definida en grid-template-areas;
   - grid-column / grid-row: posición explícita (inicio / fin);
   - justify-self / align-self: alineación del ítem individual;

4. FUNCIONES UTILES
   - fr: fracción del espacio disponible;
   - repeat(): repite valores (ej: repeat(3, 1fr));
   - minmax(): define rangos (ej: minmax(200px, 1fr));
   - auto-fit / auto-fill: para grids adaptables;

5. MEDIA QUERIES (RESPONSIVE)
   - Permiten cambiar la estructura grid según el ancho de la pantalla.
   - Ejemplo:
     @media (max-width: 768px) {
       grid-template-columns: 1fr;
     }

6. VENTAJAS DE GRID
   - Ideal para layouts completos (cabecera, contenido, sidebar, footer).
   - Más control que Flexbox en estructuras 2D.
   - Buena legibilidad y mantenimiento del código.

7. RECURSO RÁPIDO PARA ÁREAS
   Ejemplo:

   .container {
     display: grid;
     grid-template-areas:
       "header header"
       "sidebar main"
       "footer footer";
     grid-template-columns: 200px 1fr;
     grid-template-rows: 60px 1fr 40px;
   }

   .header  { grid-area: header; }
   .sidebar { grid-area: sidebar; }
   .main    { grid-area: main; }
   .footer  { grid-area: footer; }
