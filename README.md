# Alura Challenge Store – Análisis Comparativo de Tiendas

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![pandas](https://img.shields.io/badge/pandas-Data%20Analysis-150458?logo=pandas)
![NumPy](https://img.shields.io/badge/numpy-Numerical%20Computing-013243?logo=numpy)
![Matplotlib](https://img.shields.io/badge/matplotlib-Visualization-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## Índice

- [Descripcion](#descripcion)
- [Objetivo del Proyecto](#objetivo-del-proyecto)
- [Metodologia](#metodologia)
- [Resultados Principales](#resultados-principales)
- [Conclusiones](#conclusiones)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Como ejecutar el proyecto](#como-ejecutar-el-proyecto)

---

## Descripcion

Este proyecto corresponde al analisis exploratorio de datos del challenge **Alura Store Latam**.  

El objetivo es evaluar el rendimiento de cuatro tiendas utilizando metricas comerciales y construir un indice cuantitativo que permita clasificarlas de mejor a peor desempeño.

El analisis fue desarrollado en Jupyter Notebook utilizando Python y librerias de ciencia de datos.

---

## Objetivo del Proyecto

Determinar cual tienda presenta el menor rendimiento general considerando:

- Facturacion total  
- Volumen de ventas  
- Calificacion promedio  
- Costo promedio de envio  

Para ello se construyo un **Indice de Rendimiento Compuesto**, permitiendo una comparacion objetiva entre las tiendas.

---

## Metodologia

### 1. Analisis Exploratorio (EDA)

- Revision de estructura de datos  
- Validacion y limpieza  
- Visualizacion de metricas clave  

### 2. Normalizacion de Variables

Se utilizo normalizacion Min-Max para estandarizar las metricas.

Cuando mayor es mejor:

$$
X_{norm} = \frac{X - X_{min}}{X_{max} - X_{min}}
$$

Cuando menor es mejor (ej. costo de envio):

$$
X_{norm} = \frac{X_{max} - X}{X_{max} - X_{min}}
$$

### 3. Construccion del Indice

Se asignaron ponderaciones segun la importancia relativa de cada variable:

$$
Score = 0.4F + 0.3V + 0.2C + 0.1E
$$

Donde:

- F = Facturacion normalizada  
- V = Ventas normalizadas  
- C = Calificacion normalizada  
- E = Envio normalizado  

Finalmente se calculo la participacion porcentual de cada tienda sobre el total.

---

## Resultados Principales

- Tres tiendas presentan rendimiento similar (variacion aproximada de ±2%).  
- Una tienda muestra un rendimiento significativamente inferior con **6.4% del total**.  
- Dado que el equilibrio esperado seria 25% por tienda (4 tiendas), esta presenta una diferencia considerable respecto al promedio.  
- En terminos relativos, su rendimiento representa aproximadamente el 25.6% del rendimiento promedio esperado.  

El modelo permite identificar objetivamente la tienda con menor desempeño general.

---

## Conclusiones

El indice compuesto evidencia una diferencia estructural entre las tiendas evaluadas.

Mientras tres mantienen un comportamiento competitivo similar, una presenta un rendimiento considerablemente inferior segun las metricas analizadas.

Este resultado proporciona una base cuantitativa para la toma de decisiones estrategicas.

---

## Tecnologias Utilizadas

- Python  
- pandas  
- numpy  
- matplotlib  
- Jupyter Notebook  

---

## Como ejecutar el proyecto

```bash
git clone https://github.com/NULLPX-a/Alura-challenge-store.git
cd Alura-challenge-store
pip install pandas numpy matplotlib notebook
jupyter notebook
