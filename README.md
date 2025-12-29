# 🛎️ Hotel Bellhop Logistics Optimizer

### 📋 Descripción

Este proyecto surge de una necesidad real en la operación hotelera. Durante la entrega masiva de amenidades o regalos para grupos, la logística manual (en papel) solía ser ineficiente y desequilibrada.

Este script en Python automatiza la clasificación de habitaciones por **zonas geográficas (Norte, Sur y Pisos Altos)** y distribuye la carga de trabajo de forma equitativa entre los Bellboys disponibles, optimizando los desplazamientos y reduciendo el tiempo de entrega.

### 🛏️ Números de Habitación y Jerarquía de Pisos

* **Los números de habitación:** Están conformados por 4 digitos (ejemplo: `1405`).
* **La jerarquía de los pisos:** Del piso mas bajo al mas alto queda de la siguiente manera: P, L, M, 1, 2, 3, 4, 5, 6, 7, 8, 9

Para reconocer de manera inmediata a que piso corresponde cada habitación existe un patrón.
* **Piso P:** Habitaciones iniciadas con `11`.
* **Piso L:** Habitaciones iniciadas con `12`.
* **Piso M:** Habitaciones iniciadas con `14`.
* **Lógica pisos superiores:** A partir del piso `1` en adelante, el primer dígito indica el piso.

### 🏨 Lógica del Hotel (Estructura de Pantalón)

El hotel presenta una estructura particular que el script maneja automáticamente:

* **Pisos Bajos (P al 5):** Divididos en dos alas independientes.
* **Lado Norte:** Habitaciones terminadas en `01-24`.
* **Lado Sur:** Habitaciones terminadas en `25-40` (o superiores).


* **Pisos Altos (6 al 9):** Pisos unidos donde la entrega es lineal y de alta prioridad.

### 🛠️ Características Principales

1. **Entrada Dinámica:** Permite ingresar una lista de habitaciones desordenadas y el número de personal en turno mediante `input()`.
2. **Clasificación Inteligente:** Separa las habitaciones usando lógica de strings y tipos de datos.
3. **Ordenamiento Automático:** Organiza las entregas por piso para que el Bellboy siga una ruta lógica.
4. **Reparto Equitativo:** Utiliza un algoritmo de **Slicing** para asegurar que todos trabajen lo mismo, manejando los residuos de la división de forma que nadie se quede sin asignar.

### 🚀 Cómo usarlo

1. Ejecuta el script en una terminal de Python o Jupyter Notebook.
2. Cuando se te solicite, pega la lista de habitaciones separadas por comas (ejemplo: `1010, 1260, 7001, 1405`).
3. Ingresa el número de Bellboys trabajando.
4. ¡Listo! El sistema imprimirá una **Hoja de Asignación** clara para cada trabajador.

### 💻 Conceptos de Programación Aplicados

* **Funciones:** Modularización de la lógica de clasificación.
* **List Comprehensions:** Limpieza y transformación de datos de entrada.
* **Manejo de Listas:** Uso de `.sort()`, `.append()` y concatenación de listas.
* **Control de Flujo:** Estructuras `if/else` y bucles `for` con `range()`.
* **Matemáticas de Python:** Uso de la división de piso `//` para cálculos logísticos.

---

### 💡 Ideas para el futuro (Versión 2.0)

* Exportación automática a un archivo `.txt` o PDF para impresión rápida.
* Integración con una interfaz gráfica sencilla (GUI).
* Carga de datos directamente desde un archivo Excel de recepción.
