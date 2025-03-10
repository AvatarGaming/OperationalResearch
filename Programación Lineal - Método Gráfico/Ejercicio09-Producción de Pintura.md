# 🏭 Problema de Programación Lineal: Producción de Pintura

## 📝 Planteamiento del Problema

Una fábrica produce dos tipos de pintura (X e Y) utilizando dos componentes principales (A y B). La administración desea determinar la cantidad óptima de cada tipo de pintura que debe producir diariamente para maximizar sus beneficios.

### 💰 Datos Económicos
| Tipo de Pintura | Beneficio por Tonelada |
|:--------------:|:----------------------:|
| Pintura X | £50 |
| Pintura Y | £60 |

### 🧪 Requisitos de Componentes
| Tipo de Pintura | Componente A (toneladas) | Componente B (toneladas) |
|:--------------:|:------------------------:|:------------------------:|
| Pintura X | 4 | 5 |
| Pintura Y | 6 | 4 |

### 📦 Disponibilidad Diaria de Componentes
| Componente | Disponibilidad Máxima (toneladas/día) |
|:----------:|:-------------------------------------:|
| A | 24 |
| B | 20 |

## ⚙️ Formulación Matemática

### Variables de Decisión
- X = Toneladas de pintura X a producir por día
- Y = Toneladas de pintura Y a producir por día

### Función Objetivo

Maximizar el beneficio total:
$$\text{Maximizar}: Z(x,y) = 50X + 60Y \tag{1}$$

### Restricciones

1. Limitación del componente A:
   $$4X + 6Y \leq 24 \tag{2}$$

2. Limitación del componente B:
   $$5X + 4Y \leq 20 \tag{3}$$

3. Restricciones de no negatividad:
   $$X \geq 0 \tag{4}$$
   $$Y \geq 0 \tag{5}$$

## 🧮 Resolución Gráfica

Utilizando GeoGebra, hemos representado gráficamente el problema donde la región factible está sombreada en azul:

El problema se puede visualizar en GeoGebra mediante el siguiente enlace:
[Ver solución gráfica en GeoGebra](https://www.geogebra.org/graphing/u8qcmsvn)

![Solución gráfica](![alt text](image.png))


La región factible está definida por la intersección de las restricciones, formando un polígono convexo con los siguientes vértices:

| Punto | Coordenadas | Descripción |
|:-----:|:-----------:|:------------|
| A | (0, 0) | Intersección de $x = 0$ y $y = 0$ |
| B | (0, 4) | Intersección de $x = 0$ y $4X + 6Y = 24$ |
| C | (12/7, 20/7) | Intersección de $4X + 6Y = 24$ y $5X + 4Y = 20$ |
| D | (4, 0) | Intersección de $5X + 4Y = 20$ y $y = 0$ |

## 💰 Evaluación de la Función Objetivo

Para encontrar el punto óptimo, evaluamos la función objetivo $Z(x,y) = 50X + 60Y$ en cada vértice:

| Punto | Coordenadas | Valor de Z |
|:-----:|:-----------:|:----------:|
| A | (0, 0) | 0 |
| B | (0, 4) | 240 |
| C | (12/7, 20/7) | 257.14 |
| D | (4, 0) | 200 |

## 🏆 Solución Óptima

El valor máximo de la función objetivo se alcanza en el punto C, donde:
- X = 12/7 ≈ 1.71 toneladas de pintura X
- Y = 20/7 ≈ 2.86 toneladas de pintura Y
- Beneficio máximo = 257.14 libras esterlinas

## 📈 Interpretación Geométrica

Como se observa en la imagen de GeoGebra, el punto C representa la intersección de las dos restricciones principales:
- $4X + 6Y = 24$ (restricción del componente A)
- $5X + 4Y = 20$ (restricción del componente B)

La optimización ocurre en este vértice porque al "empujar" la línea de la función objetivo (con pendiente constante) en la dirección de crecimiento, el último punto de contacto con la región factible es precisamente el punto C.

## 🔄 Verificación de la Solución

Comprobemos que el punto (12/7, 20/7) satisface las restricciones:

1. Restricción del componente A:
   $$4 \cdot \frac{12}{7} + 6 \cdot \frac{20}{7} = \frac{48}{7} + \frac{120}{7} = \frac{168}{7} = 24 \checkmark$$

2. Restricción del componente B:
   $$5 \cdot \frac{12}{7} + 4 \cdot \frac{20}{7} = \frac{60}{7} + \frac{80}{7} = \frac{140}{7} = 20 \checkmark$$

3. Restricciones de no negatividad:
   $$\frac{12}{7} > 0 \text{ y } \frac{20}{7} > 0 \checkmark$$

## 📝 Conclusión

Para maximizar el beneficio, la empresa debe producir:
- 12/7 toneladas (aproximadamente 1.71 toneladas) de pintura X
- 20/7 toneladas (aproximadamente 2.86 toneladas) de pintura Y

Esto generará un beneficio máximo de 257.14 libras esterlinas por día, utilizando completamente los recursos disponibles de los componentes A y B.

## 🌟 Observaciones

Este problema ilustra perfectamente cómo la programación lineal permite encontrar la asignación óptima de recursos limitados. La solución encontrada se ubica en un vértice de la región factible, lo que confirma el principio fundamental de la programación lineal: el valor óptimo de la función objetivo siempre se encuentra en uno de los vértices del polígono que forma la región factible.