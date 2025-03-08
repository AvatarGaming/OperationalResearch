# EJERCICIO 02: Optimización de Mezcla de Alimentos: Ahorra Costos en Ozark Farms

Ozark Farms consume diariamente un mínimo de 800 lb de un alimento especial, el cual es una mezcla de maíz y soya con las siguientes composiciones:

| Forraje | Proteína | Fibra | Costo ($/lb) |
|---------|----------|-------|--------------|
| Maíz    | 0.09     | 0.02  | 0.30         |
| Soya    | 0.60     | 0.06  | 0.90         |

Las necesidades dietéticas del alimento especial son un mínimo de 30% de proteína y un máximo de 5% de fibra. El objetivo es determinar la mezcla diaria de alimento a un costo mínimo.

Las variables de decisión del modelo son:
- $X_1$ = libras de maíz en la mezcla diaria
- $X_2$ = libras de soya en la mezcla diaria

El objetivo es minimizar el costo diario total (en dólares) de la mezcla de alimento, es decir,

$$\text{Minimizar } z = 0.3X_1 + 0.9X_2$$

Las restricciones representan la cantidad diaria de la mezcla y las necesidades dietéticas. Ozark Farms requiere un mínimo de 800 lb de alimento al día, es decir,

$$X_1 + X_2 \geq 800$$

La cantidad de proteína contenida en $X_1$ libras de maíz y en $X_2$ libras de soya es $(0.09X_1 + 0.6X_2)$ lb.
Esta cantidad debe ser al menos igual al 30% de la mezcla de alimentos total $(X_1 + X_2)$ lb, es decir,

$$0.09X_1 + 0.60X_2 \geq 0.3(X_1 + X_2)$$

Asimismo, la necesidad de fibra de 5% máximo se representa como sigue:

$$0.02X_1 + 0.06X_2 \leq 0.05(X_1 + X_2)$$

Las restricciones se simplifican cambiando los términos en $X_1$ y $X_2$ al lado izquierdo de cada desigualdad, con sólo una constante del lado derecho. El modelo completo es:

## Modelo Matemático de Programación Lineal

$$\text{Minimizar } z = 0.3X_1 + 0.9X_2$$

Sujeto a:
$$X_1 + X_2 \geq 800$$
$$0.21X_1 - 0.30X_2 \leq 0$$
$$0.03X_1 - 0.01X_2 \geq 0$$
$$X_1 \geq 0$$
$$X_2 \geq 0$$


# 📊 Optimización de Mezcla de Alimentos en Ozark Farms

## 🎯 Objetivo
Minimizar el costo diario de alimentación mientras se cumplen los requisitos nutricionales.

## 📋 Datos de Forrajes
| Forraje | 🌱 Proteína | 📏 Fibra | 💰 Costo ($/lb) |
|:-------:|:-----------:|:--------:|:---------------:|
| 🌽 Maíz  | 0.09        | 0.02     | 0.30            |
| 🌱 Soya  | 0.60        | 0.06     | 0.90            |

## ⚖️ Restricciones Dietéticas
- Consumo mínimo: 800 libras diarias
- Contenido proteico: mínimo 30%
- Contenido de fibra: máximo 5%

## 🧮 Modelo Matemático
- Variables: $X_1$ = libras de maíz, $X_2$ = libras de soya

### Función Objetivo:
$$\text{Min } z = 0.3X_1 + 0.9X_2$$

### Restricciones:
1. Cantidad mínima: $X_1 + X_2 \geq 800$
2. Proteína mínima: $0.09X_1 + 0.60X_2 \geq 0.3(X_1 + X_2)$  
   Simplificada: $-0.21X_1 + 0.30X_2 \geq 0$ o $0.21X_1 - 0.30X_2 \leq 0$
3. Fibra máxima: $0.02X_1 + 0.06X_2 \leq 0.05(X_1 + X_2)$  
   Simplificada: $0.03X_1 - 0.01X_2 \geq 0$
4. No negatividad: $X_1, X_2 \geq 0$

## 💡 Interpretación
Este problema utiliza programación lineal para determinar la mezcla óptima de ingredientes que:
- Reduce al mínimo los costos de alimentación
- Satisface las necesidades nutricionales del ganado
- Cumple con la demanda diaria de alimento

La solución se puede obtener mediante métodos gráficos o herramientas como Excel Solver o POM QM.

## 📊 Solución Gráfica del Problema

### 🔍 Visualización en GeoGebra

![Solución gráfica en GeoGebra](https://github.com/AvatarGaming/OperationalResearch/blob/main/Programaci%C3%B3n%20Lineal%20-%20M%C3%A9todo%20Gr%C3%A1fico/Imagen02.png?raw=true)

[📊 Ver solución interactiva en GeoGebra](https://www.geogebra.org/graphing/nqmgmtwy)

### 📝 Interpretación del Método Gráfico

#### Restricciones del Problema

En el gráfico se representan todas las restricciones del problema:

| Restricción | Descripción matemática | Interpretación |
|:-----------:|:----------------------:|:---------------|
| a | $x + y \geq 800$ | Cantidad mínima de alimento (800 lb) |
| b | $0.21x - 0.3y \leq 0$ | Requerimiento mínimo de proteína (30%) |
| c | $0.03x - 0.01y \geq 0$ | Límite máximo de fibra (5%) |
| d | $x \geq 0$ | No negatividad para maíz |
| e | $y \geq 0$ | No negatividad para soya |
| f | Región factible (área sombreada) | Conjunto de todas las soluciones posibles |

#### 📈 Rectas Principales

El gráfico muestra las siguientes ecuaciones:
- **ec1**: $x + y = 800$ (línea naranja) - Cantidad mínima de alimento
- **ec2**: $0.21x - 0.3y = 0$ (línea azul claro) - Límite de proteína
- **ec3**: $0.03x - 0.01y = 0$ (línea gris) - Límite de fibra
- **ec4**: $x = 0$ (línea verde) - Eje vertical
- **ec5**: $0.3x + 0.9y = 437.647$ (línea roja) - Función objetivo óptima

### 🎯 Puntos Críticos

#### Vértices de la Región Factible
- **Punto A** = $(200, 600)$ - Intersección de ec3 y ec1
- **Punto B** = $(470.59, 329.41)$ - Intersección de ec2 y ec1

#### 💰 Evaluación de la Función Objetivo

La función objetivo es: $Z(x,y) = 0.3x + 0.9y$

| Punto | Coordenadas | Valor de Z | 
|:-----:|:-----------:|:----------:|
| A | $(200, 600)$ | $Z(A) = 600$ |
| B | $(470.59, 329.41)$ | $Z(B) = 437.65$ |

### 🏆 Solución Óptima

La solución óptima se encuentra en el punto B:
- $X_1$ (Maíz) ≈ 470.59 libras
- $X_2$ (Soya) ≈ 329.41 libras
- Costo mínimo = $437.65

## 💡 Análisis Final

1. La región factible está delimitada por las restricciones de cantidad mínima de alimento, proteína mínima y fibra máxima.
2. El punto óptimo se encuentra en la intersección de las restricciones de cantidad mínima (ec1) y proteína mínima (ec2).
3. La restricción activa de fibra máxima (ec3) no afecta a la solución óptima.
4. La mezcla óptima contiene aproximadamente 60% de maíz y 40% de soya.

