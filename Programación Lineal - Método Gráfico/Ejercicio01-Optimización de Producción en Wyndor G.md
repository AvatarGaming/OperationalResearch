# Optimización de Producción en Wyndor Glass Co.: Maximización de Beneficios en un Entorno de Restricciones de Capacidad

## Descripción de la Empresa

La empresa WYNDOR GLASS CO. produce productos de vidrio de alta calidad, incluyendo ventanas y puertas de vidrio. Tiene tres plantas de producción:
- **Planta 1**: Marcos de aluminio y herrajes.
- **Planta 2**: Marcos de madera.
- **Planta 3**: Producción de vidrio y ensamblaje de productos.

Debido a una disminución en las ganancias, la alta dirección ha decidido renovar la línea de productos de la empresa, eliminando los productos no rentables y liberando capacidad de producción para lanzar dos nuevos productos con gran potencial de ventas:
- **Producto 1**: Una puerta de vidrio de 8 pies con marco de aluminio.
- **Producto 2**: Una ventana de doble hoja de 4 x 6 pies con marco de madera.

El Producto 1 utiliza capacidad de producción en las Plantas 1 y 3, pero no en la Planta 2. El Producto 2 solo necesita las Plantas 2 y 3. La división de marketing concluyó que la empresa podría vender tanto de cualquiera de los productos como pudiera ser producido por estas plantas. Sin embargo, debido a que ambos productos compiten por la misma capacidad de producción en la Planta 3, no está claro cuál mezcla de los dos productos sería más rentable. Por lo tanto, se ha formado un equipo de Investigación Operativa (IO) para estudiar esta cuestión.

## Definición del Problema

El equipo de IO comenzó discutiendo con la alta dirección para identificar los objetivos de la gestión para el estudio, lo que llevó a desarrollar la siguiente definición del problema: Determinar cuáles deberían ser las tasas de producción de los dos productos para maximizar el beneficio total, sujeto a las restricciones impuestas por las capacidades de producción limitadas disponibles en las tres plantas. (Cada producto se producirá en lotes de 20, por lo que la tasa de producción se define como el número de lotes producidos por semana). Se permite cualquier combinación de tasas de producción que cumpla con estas restricciones, incluyendo producir ninguno de un producto y tanto como sea posible del otro.

## Datos Necesarios

El equipo de IO identificó los datos que necesitaban recopilar:

a) Número de horas de tiempo de producción disponible por semana en cada planta para estos nuevos productos. (La mayor parte del tiempo en estas plantas ya está comprometido con productos actuales, por lo que la capacidad disponible para los nuevos productos es bastante limitada).

b) Número de horas de tiempo de producción utilizado en cada planta por cada lote producido de cada nuevo producto.

c) Beneficio por lote producido de cada nuevo producto. (El beneficio por lote producido fue elegido una medida apropiada después de que el equipo concluyó que el beneficio incremental de cada lote adicional producido sería aproximadamente constante sin importar el número total de lotes producidos. Debido a que no se incurrirán en costos sustanciales para iniciar la producción y el marketing de estos nuevos productos, el beneficio total de cada uno es aproximadamente este beneficio por lote producido multiplicado por el número de lotes producidos).

## Recopilación de Datos

Obtener estimaciones razonables de estas cantidades requirió la ayuda del personal clave en varias unidades de la empresa. El personal de la división de fabricación proporcionó los datos en la primera categoría mencionada. Desarrollar estimaciones para la segunda categoría de datos requirió algo de análisis por parte de los ingenieros de fabricación involucrados en el diseño de los procesos de producción para los nuevos productos. Analizando los datos de costos de estos mismos ingenieros y la división de marketing, junto con una decisión de precios de la división de marketing, el departamento de contabilidad desarrolló estimaciones para la tercera categoría.

## Resumen de Datos

El equipo de IO reconoció inmediatamente que esto era un problema de programación lineal del tipo clásico de mezcla de productos, y luego procedieron a formular el modelo matemático correspondiente.

## Formulación del Problema de Programación Lineal

La definición del problema indica que las decisiones a tomar son el número de lotes de los respectivos productos que se producirán por semana para maximizar su beneficio total. Por lo tanto, para formular el modelo matemático (programación lineal) para este problema, definamos:

- $X_1$ = número de lotes del Producto 1 producidos por semana.
- $X_2$ = número de lotes del Producto 2 producidos por semana.
- $Z$ = beneficio total por semana (en miles de dólares) de la producción de estos dos productos.

El objetivo es elegir los valores de $X_1$ y $X_2$ para maximizar $Z=3X_1+5X_2$, sujeto a las restricciones impuestas por las capacidades de producción limitadas disponibles en las tres plantas.

## Restricciones

a) **Planta 1**: Cada lote del Producto 1 utiliza 1 hora de tiempo de producción por semana, mientras que solo hay 4 horas disponibles. Esto se expresa matemáticamente por la desigualdad: $X_1 \leq 4$.

b) **Planta 2**: Cada lote del Producto 2 utiliza 2 horas de tiempo de producción por semana, mientras que solo hay 12 horas disponibles. Esto se expresa como: $2X_2 \leq 12$.

c) **Planta 3**: El número de horas de tiempo de producción usado por semana en la Planta 3 por $X_1$ y $X_2$ es: $3X_1+2X_2$. La restricción de la Planta 3 es entonces: $3X_1+2X_2 \leq 18$.

d) Finalmente, dado que las tasas de producción no pueden ser negativas, es necesario restringir las variables de decisión a ser no negativas: $X_1 \geq 0, X_2 \geq 0$.

# Planteamiento del Ejercicio.

## Contexto
Wyndor Glass Co. busca maximizar beneficios con dos nuevos productos:
- 🚪 **Producto 1**: Puerta de vidrio con marco de aluminio
- 🪟 **Producto 2**: Ventana de doble hoja con marco de madera

## Variables
- $X_1$ = Lotes semanales del Producto 1
- $X_2$ = Lotes semanales del Producto 2
- $Z$ = Beneficio total semanal (miles $)

## Modelo de Programación Lineal
**Objetivo**: Maximizar $Z = 3X_1 + 5X_2$

**Restricciones**:
- Planta 1 (marcos aluminio): $X_1 \leq 4$
- Planta 2 (marcos madera): $2X_2 \leq 12$
- Planta 3 (vidrio/ensamblaje): $3X_1 + 2X_2 \leq 18$
- No negatividad: $X_1, X_2 \geq 0$

## Datos Clave

| Producto | Ganancia/Lote | Planta 1 | Planta 2 | Planta 3 |
|----------|---------------|----------|----------|----------|
| 1: Puerta | $3,000 | 1h | 0h | 3h |
| 2: Ventana | $5,000 | 0h | 2h | 2h |
| **Capacidad** | | **4h** | **12h** | **18h** |

El problema puede resolverse mediante métodos gráficos o usando herramientas como Excel Solver, POM QM, LINGO, R o Python para determinar la combinación óptima de productos que maximice el beneficio total.



# Solución del Problema de Wyndor Glass Co. por Método Gráfico

## 📊 Visualización Gráfica en GeoGebra

<iframe src="https://www.geogebra.org/graphing/x92wsx97?embed" width="800" height="1500" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

**Enlace a la solución**: [https://www.geogebra.org/graphing/x92wsx97](https://www.geogebra.org/graphing/x92wsx97)

## 📝 Restricciones del Problema

El modelo matemático presenta las siguientes restricciones:

1. $X_1 \leq 4$ (límite de capacidad Planta 1)
2. $2X_2 \leq 12$ → $X_2 \leq 6$ (límite de capacidad Planta 2)
3. $3X_1 + 2X_2 \leq 18$ (límite de capacidad Planta 3)
4. $X_1 \geq 0$ (no negatividad)
5. $X_2 \geq 0$ (no negatividad)

## 🔍 Región Factible

En la gráfica de GeoGebra, la región factible está representada por el área sombreada en azul, formando un polígono con vértices en los puntos:

| Punto | Coordenadas | Descripción |
|-------|-------------|-------------|
| A | (0, 0) | Intersección de los ejes $X_1$ y $X_2$ |
| B | (0, 6) | Intersección de $X_1 = 0$ y $X_2 = 6$ |
| C | (2, 6) | Intersección de $X_2 = 6$ y $3X_1 + 2X_2 = 18$ |
| D | (4, 3) | Intersección de $X_1 = 4$ y $3X_1 + 2X_2 = 18$ |
| E | (4, 0) | Intersección de $X_1 = 4$ y $X_2 = 0$ |

## 💹 Función Objetivo

La función objetivo a maximizar es $Z = 3X_1 + 5X_2$ (en miles de dólares). En la herramienta GeoGebra, esta función se representa como $Z(x,y) = 3x + 5y$

## 📈 Evaluación en los Vértices

Para encontrar el punto óptimo, evaluamos la función objetivo en cada uno de los vértices:

| Vértice | Coordenadas | Valor de Z | Cálculo |
|---------|-------------|------------|---------|
| A | (0, 0) | 0 | $Z(0,0) = 3(0) + 5(0) = 0$ |
| B | (0, 6) | 30 | $Z(0,6) = 3(0) + 5(6) = 30$ |
| C | (2, 6) | 36 | $Z(2,6) = 3(2) + 5(6) = 6 + 30 = 36$ |
| D | (4, 3) | 27 | $Z(4,3) = 3(4) + 5(3) = 12 + 15 = 27$ |
| E | (4, 0) | 12 | $Z(4,0) = 3(4) + 5(0) = 12$ |

## 🏆 Solución Óptima

Según los valores calculados, el punto C (2, 6) proporciona el valor máximo para la función objetivo: $Z = 36$ miles de dólares.

Por lo tanto, la solución óptima es:
- Producir 2 lotes del Producto 1 (puertas de vidrio) por semana
- Producir 6 lotes del Producto 2 (ventanas de doble hoja) por semana
- Generando un beneficio semanal de $36,000

## 🔄 Verificación

Comprobamos que el punto (2, 6) cumple con todas las restricciones:
1. $X_1 = 2 \leq 4$ ✓
2. $2X_2 = 2(6) = 12 \leq 12$ ✓
3. $3X_1 + 2X_2 = 3(2) + 2(6) = 6 + 12 = 18 \leq 18$ ✓
4. $X_1 = 2 \geq 0$ ✓
5. $X_2 = 6 \geq 0$ ✓

La solución (2, 6) es factible y óptima para este problema de programación lineal.