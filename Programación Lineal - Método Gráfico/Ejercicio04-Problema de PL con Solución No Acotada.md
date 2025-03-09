# Análisis de un Problema de Programación Lineal con Solución No Acotada

## 📊 Planteamiento del problema

Una empresa ha formulado el siguiente problema de programación lineal:

**Función objetivo (maximizar):** 
$$Z = 3X_1 + 5X_2$$

**Restricciones:**
$$X_1 \geq 5$$
$$X_2 \leq 10$$
$$X_1 + 2X_2 \geq 10$$
$$X_1, X_2 \geq 0$$

## 📈 Representación gráfica

La solución puede visualizarse en GeoGebra: [Ver gráfico interactivo](https://www.geogebra.org/graphing/zuumhfae)

![Gráfico de Programación Lineal](https://github.com/AvatarGaming/OperationalResearch/blob/main/Programaci%C3%B3n%20Lineal%20-%20M%C3%A9todo%20Gr%C3%A1fico/Imagen03.png?raw=true)

## 🔍 Análisis de la región factible

La región factible está delimitada por tres puntos importantes:

| Punto | Coordenadas | Descripción |
|-------|-------------|-------------|
| A     | (5, 10)     | Intersección de $X_1 = 5$ y $X_2 = 10$ |
| B     | (5, 2.5)    | Intersección de $X_1 = 5$ y $X_1 + 2X_2 = 10$ |
| C     | (10, 0)     | Intersección de $X_1 + 2X_2 = 10$ y $X_2 = 0$ |

La región factible se extiende indefinidamente hacia la derecha del plano, lo que indica una **solución no acotada** ⚠️.

## 📝 Evaluación de la función objetivo

Calculando el valor de la función objetivo en cada vértice:

| Punto | Coordenadas | Valor de $Z = 3X_1 + 5X_2$ | Cálculo |
|-------|-------------|----------------------------|---------|
| A     | (5, 10)     | 65                         | $3(5) + 5(10) = 15 + 50 = 65$ |
| B     | (5, 2.5)    | 27.5                       | $3(5) + 5(2.5) = 15 + 12.5 = 27.5$ |
| C     | (10, 0)     | 30                         | $3(10) + 5(0) = 30 + 0 = 30$ |

## ⚠️ Diagnóstico de solución no acotada

Este problema presenta una **solución no acotada** por las siguientes razones:

1. La región factible se extiende infinitamente en la dirección positiva del eje $X_1$
2. El coeficiente de $X_1$ en la función objetivo es positivo (3)
3. No hay restricciones superiores para la variable $X_1$

## 🧮 Comportamiento de la función objetivo

Si analizamos el comportamiento en la dirección de crecimiento:
- Partiendo del punto A (5,10) con $Z=65$
- Si aumentamos $X_1$ mientras mantenemos $X_2=10$:
  - Para $X_1=100$: $Z = 3(100) + 5(10) = 300 + 50 = 350$
  - Para $X_1=1000$: $Z = 3(1000) + 5(10) = 3000 + 50 = 3050$

Esto demuestra que $Z$ puede crecer ilimitadamente.

## 🏭 Implicaciones prácticas

La solución no acotada indica que el modelo matemático está incompleto, ya que en situaciones reales:

- 🏭 Las empresas tienen capacidades de producción limitadas
- 🛒 Los mercados tienen demanda finita
- 🧪 Los recursos disponibles son limitados

## 🔧 Corrección del modelo

Para obtener una solución realista, se debería reformular el problema añadiendo restricciones adicionales, como:

$$X_1 \leq 100 \text{ (capacidad máxima de producción)}$$

O bien incluir costos fijos que limiten la ventaja de incrementar $X_1$ indefinidamente.

## 📘 Conclusión

Este ejercicio ilustra la importancia de definir correctamente las restricciones en un problema de programación lineal. Un modelo que produce una solución no acotada generalmente carece de restricciones que reflejen las limitaciones físicas, económicas o logísticas del mundo real.