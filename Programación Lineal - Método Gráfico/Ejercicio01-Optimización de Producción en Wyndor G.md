# Optimización de Producción en Wyndor Glass Co.: Maximización de Beneficios

## Descripción de la Empresa

La empresa WYNDOR GLASS CO. produce productos de vidrio de alta calidad, incluyendo ventanas y puertas de vidrio. Tiene tres plantas de producción:
- **Planta 1**: Marcos de aluminio y herrajes.
- **Planta 2**: Marcos de madera.
- **Planta 3**: Producción de vidrio y ensamblaje de productos.

Debido a una disminución en las ganancias, la alta dirección ha decidido renovar la línea de productos de la empresa, eliminando los productos no rentables y liberando capacidad de producción para lanzar dos nuevos productos con gran potencial de ventas:
- 🚪 **Producto 1**: Una puerta de vidrio de 8 pies con marco de aluminio.
- 🪟 **Producto 2**: Una ventana de doble hoja de 4 x 6 pies con marco de madera.

El Producto 1 utiliza capacidad de producción en las Plantas 1 y 3, pero no en la Planta 2. El Producto 2 solo necesita las Plantas 2 y 3. La división de marketing concluyó que la empresa podría vender tanto de cualquiera de los productos como pudiera ser producido por estas plantas. Sin embargo, debido a que ambos productos compiten por la misma capacidad de producción en la Planta 3, no está claro cuál mezcla de los dos productos sería más rentable.

## Definición del Problema

Determinar las tasas de producción de los dos productos para maximizar el beneficio total, sujeto a las restricciones impuestas por las capacidades de producción limitadas disponibles en las tres plantas. Cada producto se producirá en lotes de 20, por lo que la tasa de producción se define como el número de lotes producidos por semana.

## Modelo de Programación Lineal

### Variables
- X₁ = Lotes semanales del Producto 1
- X₂ = Lotes semanales del Producto 2
- Z = Beneficio total semanal (miles $)

### Objetivo
Maximizar Z = 3X₁ + 5X₂

### Restricciones
- Planta 1 (marcos aluminio): X₁ ≤ 4
- Planta 2 (marcos madera): 2X₂ ≤ 12
- Planta 3 (vidrio/ensamblaje): 3X₁ + 2X₂ ≤ 18
- No negatividad: X₁, X₂ ≥ 0

### Datos Clave

| Producto | Ganancia/Lote | Planta 1 | Planta 2 | Planta 3 |
|----------|---------------|----------|----------|----------|
| 1: Puerta | $3,000 | 1h | 0h | 3h |
| 2: Ventana | $5,000 | 0h | 2h | 2h |
| **Capacidad** | | **4h** | **12h** | **18h** |

## Solución Gráfica

![Solución gráfica en GeoGebra](https://github.com/AvatarGaming/OperationalResearch/blob/main/Programaci%C3%B3n%20Lineal%20-%20M%C3%A9todo%20Gr%C3%A1fico/Imagen01.png?raw=true)

**Enlace a la solución**: [https://www.geogebra.org/graphing/x92wsx97](https://www.geogebra.org/graphing/x92wsx97)

### Región Factible

En la gráfica, la región factible está representada por el área sombreada en azul, formando un polígono con vértices en los puntos:

| Punto | Coordenadas | Descripción |
|-------|-------------|-------------|
| A | (0, 0) | Intersección de los ejes X₁ y X₂ |
| B | (0, 6) | Intersección de X₁ = 0 y X₂ = 6 |
| C | (2, 6) | Intersección de X₂ = 6 y 3X₁ + 2X₂ = 18 |
| D | (4, 3) | Intersección de X₁ = 4 y 3X₁ + 2X₂ = 18 |
| E | (4, 0) | Intersección de X₁ = 4 y X₂ = 0 |

### Evaluación en los Vértices

Para encontrar el punto óptimo, evaluamos la función objetivo en cada vértice:

| Vértice | Coordenadas | Valor de Z | Cálculo |
|---------|-------------|------------|---------|
| A | (0, 0) | 0 | Z(0,0) = 3(0) + 5(0) = 0 |
| B | (0, 6) | 30 | Z(0,6) = 3(0) + 5(6) = 30 |
| C | (2, 6) | 36 | Z(2,6) = 3(2) + 5(6) = 6 + 30 = 36 |
| D | (4, 3) | 27 | Z(4,3) = 3(4) + 5(3) = 12 + 15 = 27 |
| E | (4, 0) | 12 | Z(4,0) = 3(4) + 5(0) = 12 |

### 🏆 Solución Óptima

El punto C (2, 6) proporciona el valor máximo para la función objetivo: Z = 36 miles de dólares.

Por lo tanto, la solución óptima es:
- Producir 2 lotes del Producto 1 (puertas de vidrio) por semana
- Producir 6 lotes del Producto 2 (ventanas de doble hoja) por semana
- Generando un beneficio semanal de $36,000

### Verificación

Comprobamos que el punto (2, 6) cumple con todas las restricciones:
1. X₁ = 2 ≤ 4 ✓
2. 2X₂ = 2(6) = 12 ≤ 12 ✓
3. 3X₁ + 2X₂ = 3(2) + 2(6) = 6 + 12 = 18 ≤ 18 ✓
4. X₁ = 2 ≥ 0 ✓
5. X₂ = 6 ≥ 0 ✓

La solución (2, 6) es factible y óptima para este problema de programación lineal.