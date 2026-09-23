# Perceptrón Simple desde Cero

Implementación pedagógica del **Perceptrón de Rosenblatt** (1958) programado desde cero con **NumPy y Matplotlib**, sin usar librerías de aprendizaje automático como scikit-learn.

## Descripción

El proyecto reproduce, en un notebook resuelto, la arquitectura matemática interna de una neurona artificial y su algoritmo de entrenamiento, aplicándola a dos problemas de clasificación linealmente separables (AND y OR) y a un problema no linealmente separable (XOR, el famoso contraejemplo de Minsky y Papert, 1969).

## Contenido del notebook

El notebook `perceptron_simple.ipynb` está estructurado según la guía de la práctica:

- **Parte 1 — Implementación**: clase `Perceptron` (inicialización en ceros, función de activación escalón de Heaviside, `predict` y algoritmo `fit` con regla de actualización de pesos y sesgo).
- **Parte 2 — Simulación**: entrenamiento con las compuertas AND, OR y XOR, incluyendo una comparación de tasas de aprendizaje (`eta = 0.01`, `0.1` y `0.5`).
- **Parte 3 — Visualización**: gráficas de convergencia (épocas vs. errores) y fronteras de decisión (`x2 = -(w1·x1 + b)/w2`) para cada compuerta.
- **Parte 4 — Cuestionario resuelto**:
  1. Análisis de convergencia en AND y OR y efecto de la tasa de aprendizaje.
  2. Explicación geométrica de por qué el Perceptrón falla en XOR (separabilidad lineal).
  3. Interpretación física de los pesos finales obtenidos para la compuerta AND.

## Resultados principales

| Compuerta | eta = 0.01 | eta = 0.1 | eta = 0.5 |
|-----------|------------|-----------|-----------|
| AND       | 6 épocas   | 4 épocas  | 6 épocas  |
| OR        | 4 épocas   | 4 épocas  | 4 épocas  |
| XOR       | no converge | no converge | no converge |

Para la compuerta AND (con `eta = 0.1`), los pesos finales son `w1 = 0.20`, `w2 = 0.10` y `b = -0.20`.

El Perceptrón de una sola capa es un **clasificador lineal**: solo puede resolver problemas linealmente separables. La verificación por fuerza bruta incluida en el notebook demuestra que la mejor recta posible sobre XOR comete al menos 1 error de 4 (exactitud máxima del 75%).

## Requisitos

- Python 3.9 o superior
- NumPy
- Matplotlib
- Jupyter Notebook

Instalación rápida:

```bash
pip install numpy matplotlib jupyter
```

## Uso

```bash
jupyter notebook perceptron_simple.ipynb
```

El notebook está resuelto y ejecutado de principio a fin; puede volver a ejecutarse como Kernel -> Restart & Run All sin errores.

## Licencia

Uso educativo.