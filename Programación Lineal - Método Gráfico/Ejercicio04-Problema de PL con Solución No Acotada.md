# Problema de Programación Lineal con Solución No Acotada

## 📊 Planteamiento del problema

Una empresa ha formulado el siguiente problema de programación lineal:

**Función objetivo (maximizar):** 
$$Z = 3X_1 + 5X_2$$

## 📝 Representación tabular de restricciones

| N° | Restricción | Descripción | Expresión matemática |
|:--:|-------------|-------------|----------------------|
| 1  | Restricción 1 | Producción mínima de $X_1$ | $X_1 \geq 5$ |
| 2  | Restricción 2 | Límite superior para $X_2$ | $X_2 \leq 10$ |
| 3  | Restricción 3 | Restricción combinada | $X_1 + 2X_2 \geq 10$ |
| 4  | Restricción 4 | No negatividad de $X_1$ | $X_1 \geq 0$ |
| 5  | Restricción 5 | No negatividad de $X_2$ | $X_2 \geq 0$ |

Nota: Las restricciones 4 y 5 son redundantes con la restricción 1 y las condiciones básicas del problema, pero se incluyen por completitud.



## 📈 Visualización gráfica

El problema se puede visualizar en GeoGebra mediante el siguiente enlace:
[Ver solución gráfica en GeoGebra](https://www.geogebra.org/graphing/zuumhfae)

![Solución gráfica](https://github.com/AvatarGaming/OperationalResearch/blob/main/Programaci%C3%B3n%20Lineal%20-%20M%C3%A9todo%20Gr%C3%A1fico/Imagen03.png?raw=true)

## 🔍 Región factible

La región factible está delimitada por los siguientes puntos de intersección:

| Punto | Coordenadas | Descripción |
|:-----:|:-----------:|-------------|
| A     | (5, 10)     | Intersección de las ecuaciones $X_1 = 5$ y $X_2 = 10$ |
| B     | (5, 2.5)    | Intersección de las ecuaciones $X_1 = 5$ y $X_1 + 2X_2 = 10$ |
| C     | (10, 0)     | Intersección de las ecuaciones $X_1 + 2X_2 = 10$ y $X_2 = 0$ |

La región se extiende indefinidamente hacia la derecha en el plano cartesiano, lo que indica una **solución no acotada** ⚠️.

## 📝 Evaluación de la función objetivo

Evaluamos la función objetivo $Z = 3X_1 + 5X_2$ en cada uno de los vértices de la región factible:

| Punto | Coordenadas | Cálculo | Valor de Z |
|:-----:|:-----------:|:-------:|:----------:|
| A     | (5, 10)     | $3(5) + 5(10) = 15 + 50$ | $Z(A) = 65$ |
| B     | (5, 2.5)    | $3(5) + 5(2.5) = 15 + 12.5$ | $Z(B) = 27.5$ |
| C     | (10, 0)     | $3(10) + 5(0) = 30 + 0$ | $Z(C) = 30$ |

## 🧮 Análisis de resultados

1. Entre los vértices analizados, el valor máximo de la función objetivo se alcanza en el punto A = (5, 10) con $Z = 65$.

2. La línea de nivel de la función objetivo (ec6: $3X_1 + 5X_2 = 65$) que pasa por el punto A muestra que:
   - Al moverse horizontalmente hacia la derecha (aumentando $X_1$), manteniendo $X_2 = 10$
   - Por cada unidad que aumenta $X_1$, el valor de Z aumenta en 3 unidades

3. Como la región factible se extiende infinitamente en la dirección positiva del eje $X_1$ y el coeficiente de $X_1$ en la función objetivo es positivo (3), el valor de Z puede crecer sin límite.

## 🚫 Problema de no acotamiento

El problema presenta una **solución no acotada** debido a tres factores clave:

1. La región factible se extiende infinitamente en dirección positiva del eje $X_1$
2. El coeficiente de $X_1$ en la función objetivo es positivo (3)
3. No existe una restricción superior para la variable $X_1$

## 🔧 Implicaciones prácticas

En aplicaciones reales, una solución no acotada indica que el modelo matemático está incompleto, ya que en la práctica:

- 🏭 Ninguna empresa dispone de recursos de producción infinitos
- 🛒 No existe demanda infinita para ningún producto
- 🧪 Los recursos materiales siempre son limitados

## ✅ Solución propuesta

Para obtener un modelo más realista, se debería reformular el problema añadiendo restricciones adicionales, como:

1. Una cota superior para $X_1$: $X_1 ≤ M$ donde M representa la capacidad máxima de producción
2. Restricciones de recursos: $aX_1 + bX_2 ≤ R$ donde R representa la disponibilidad de recursos
3. Restricciones de demanda máxima del mercado

Esto permitiría obtener una solución acotada que refleje mejor las condiciones del mundo real.