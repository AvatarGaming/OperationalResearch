# Ejercicio 04: Ejemplo de un Problema de Programación Lineal con Solución No Acotada

## Planteamiento del problema

Una empresa ha formulado el siguiente problema de programación lineal (LP):

**Maximizar beneficio:** 
$$Z = 3X_1 + 5X_2$$

**Sujeto a:**
$$X_1 \geq 5$$
$$X_2 \leq 10$$
$$X_1 + 2X_2 \geq 10$$
$$X_1, X_2 \geq 0$$

## Análisis del problema

Debido a que este es un problema de maximización y la región factible se extiende infinitamente hacia la derecha, se presenta una situación de **no acotamiento** o una **solución no acotada** ⚠️.

Esto implica que el problema ha sido formulado incorrectamente. Sería maravilloso que la empresa pudiera producir un número infinito de unidades de $X_1$ (¡con un beneficio de $\$3$ cada una!), pero obviamente ninguna empresa tiene:

- 🏭 Recursos infinitos disponibles
- 📊 Demanda infinita de productos

## Representación tabular

| Restricción | Descripción | Expresión matemática |
|-------------|-------------|----------------------|
| Restricción 1 | Producción mínima de $X_1$ | $X_1 \geq 5$ |
| Restricción 2 | Límite superior para $X_2$ | $X_2 \leq 10$ |
| Restricción 3 | Restricción combinada | $X_1 + 2X_2 \geq 10$ |
| No negatividad | Variables no negativas | $X_1, X_2 \geq 0$ |

# Análisis de un Problema de Programación Lineal con Solución No Acotada

## Interpretación gráfica del problema

![Gráfico de Programación Lineal en GeoGebra](https://www.geogebra.org/graphing/zuumhfae)

```html
<img src="https://www.geogebra.org/graphing/zuumhfae" alt="Gráfico de Programación Lineal en GeoGebra">
```

## Planteamiento del problema

Se presenta un problema de programación lineal con la siguiente formulación:

**Función objetivo (maximizar):** 
$$Z(x,y) = 3x + 5y$$

**Sujeto a las restricciones:**
$$x \geq 5 \quad \text{(ec1)}$$
$$y \leq 10 \quad \text{(ec2)}$$
$$x + 2y \geq 10 \quad \text{(ec3)}$$
$$x \geq 0 \quad \text{(ec4)}$$
$$y \geq 0 \quad \text{(ec5)}$$

## Región factible

La región factible está delimitada por los puntos de intersección:
- Punto A = (5, 10) → Intersección de ec1 y ec2
- Punto B = (5, 2.5) → Intersección de ec3 y ec1
- Punto C = (10, 0) → Intersección de ec3 y ec5

La región factible se extiende indefinidamente hacia el lado derecho del gráfico (valores de $x$ crecientes), lo que indica una solución **no acotada** ⚠️.

## Evaluación de la función objetivo

La función objetivo ha sido evaluada en los vértices de la región factible:

| Punto | Coordenadas | Valor de $Z = 3x + 5y$ |
|-------|-------------|------------------------|
| A     | (5, 10)     | $Z(A) = 65$            |
| B     | (5, 2.5)    | $Z(B) = 27.5$          |
| C     | (10, 0)     | $Z(C) = 30$            |

## Análisis de resultados

1. El valor máximo de la función objetivo en los vértices se encuentra en el punto A = (5, 10) con $Z = 65$.

2. Sin embargo, dado que la región se extiende infinitamente hacia la derecha y el coeficiente de $x$ en la función objetivo es positivo (3), el valor de $Z$ puede aumentar sin límite al incrementar el valor de $x$.

3. La línea de nivel de la función objetivo (`ec6: 3x + 5y = 65`) que pasa por el punto A muestra que al moverse hacia la derecha (aumentando $x$), manteniendo $y = 10$, se pueden encontrar valores cada vez mayores para $Z$.

## Conclusión

🔍 Este problema presenta una **solución no acotada** porque:

- La región factible se extiende infinitamente en la dirección positiva del eje $x$.
- El coeficiente de $x$ en la función objetivo es positivo (3).
- No hay restricciones superiores para la variable $x$.

En aplicaciones prácticas, esto indicaría que el modelo matemático está incompleto, ya que en situaciones reales:

- 🏭 Las empresas tienen capacidades de producción limitadas
- 🛒 Los mercados tienen demanda finita
- 🧪 Los recursos disponibles son limitados

Para obtener una solución realista, se debería reformular el problema añadiendo restricciones adicionales, como una cota superior para $x$.