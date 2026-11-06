# Práctica Deep Learning – Redes GAN (Semana 11)

**Estudiante:** Ruby Dayana Cárdenas Gómez
**Docente:** Paul Alexander Díaz Montaña
**Curso:** Inteligencia Artificial – Conceptos · Universidad de Cundinamarca

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RubyDayana/redes-gan/blob/main/GAN_FashionMNIST_RubyCardenas.ipynb)

## Descripción
Práctica en la que se entrenan dos redes generativas adversarias (GAN) sobre el conjunto **Fashion-MNIST** (60.000 imágenes de prendas, 28×28) y se comparan:

1. **GAN densa (MLP):** capas totalmente conectadas, como la propuesta original de Goodfellow et al. (2014).
2. **DCGAN:** capas convolucionales, según Radford et al. (2016).

Las dos redes usan los mismos datos e hiperparámetros: 10 épocas, lote de 128, Adam (lr = 0,0002, β₁ = 0,5) y ruido de 100 dimensiones. Lo único que cambia es la arquitectura.

## Contenido del cuaderno
1. Carga y normalización de Fashion-MNIST
2. Definición del generador y del discriminador (MLP y DCGAN)
3. Entrenamiento adversarial
4. Curvas de pérdida y de salida del discriminador
5. Evolución de las imágenes generadas por época
6. Evaluación con IS y FID adaptados (clasificador CNN entrenado con imágenes reales)
7. Interpolación en el espacio latente

## Resultados principales
| Modelo | IS ↑ | FID ↓ | Tiempo (CPU) |
|---|---|---|---|
| Imágenes reales (referencia) | 7,68 | 0,41 | – |
| GAN densa | 4,17 | 29,41 | 1,3 min |
| DCGAN | 5,32 | 8,45 | 18,8 min |

La DCGAN genera prendas más nítidas y cercanas a las reales (FID 3,5 veces menor), a cambio de un mayor costo computacional.


