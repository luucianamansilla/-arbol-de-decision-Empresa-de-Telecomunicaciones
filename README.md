# 🌳 Árbol de Decisión: Empresa de Telecomunicaciones

## 📌 Descripción del proyecto

Este proyecto consiste en la aplicación de un **árbol de decisión** para analizar el comportamiento de clientes de una empresa de telecomunicaciones y predecir si aceptarán una oferta comercial.

Para realizar el análisis, se utiliza un conjunto de datos de 10 clientes, considerando las siguientes características:

- **Edad:** edad del cliente.
- **Uso de datos (GB):** consumo de datos móviles.
- **Tiene línea fija:** indica si el cliente cuenta con una línea fija.
- **Aceptó oferta:** variable objetivo que indica si el cliente aceptó la oferta comercial.

El objetivo es identificar qué característica permite clasificar mejor a los clientes según su respuesta a la oferta.

## 🎯 Objetivos

- Analizar un conjunto de datos de clientes.
- Calcular la entropía inicial del conjunto.
- Calcular la ganancia de información de cada atributo.
- Comparar los atributos para seleccionar la mejor variable de división.
- Construir e interpretar el árbol de decisión.
- Aplicar las reglas obtenidas a nuevos casos.

## 📊 Conjunto de datos

El conjunto de datos utilizado contiene 10 registros.

| ID | Edad | Uso de datos (GB) | Tiene línea fija | Aceptó oferta |
|---:|---:|---:|:---:|:---:|
| 1 | 24 | 2.5 | No | No |
| 2 | 38 | 6.0 | Sí | Sí |
| 3 | 29 | 3.0 | No | No |
| 4 | 45 | 8.0 | Sí | Sí |
| 5 | 52 | 7.5 | Sí | Sí |
| 6 | 33 | 4.0 | No | No |
| 7 | 41 | 5.5 | Sí | Sí |
| 8 | 27 | 2.0 | No | No |
| 9 | 36 | 6.5 | Sí | Sí |
| 10 | 31 | 3.5 | No | No |

## 🧮 Metodología

Para determinar el atributo más adecuado para construir el árbol, se utilizan dos conceptos fundamentales:

**1. Entropía**

Mide el grado de incertidumbre o impureza de un conjunto de datos. Cuanto menor sea su valor, más homogénea será la clasificación.

**2. Ganancia de información**

Permite medir cuánto disminuye la entropía al dividir los datos según un atributo. El atributo con mayor ganancia de información se selecciona como raíz del árbol.

La entropía inicial del conjunto es de **1 bit**, ya que existen cinco clientes que aceptaron la oferta y cinco que la rechazaron.

## 📈 Resultados

Los atributos evaluados presentan los siguientes resultados:

| Atributo | Entropía ponderada | Ganancia de información |
|---|---:|---:|
| Tiene línea fija | 0.0000 | 1.0000 |
| Uso de datos | 0.4000 | 0.6000 |
| Edad | 0.5510 | 0.4490 |

El atributo **«Tiene línea fija»** obtiene la mayor ganancia de información, con un valor de **1.0000 bit**. Por este motivo, se selecciona como raíz del árbol de decisión.

## 🌳 Árbol de decisión obtenido

La clasificación final se puede representar mediante las siguientes reglas:

- **Tiene línea fija = Sí:** se predice que el cliente aceptará la oferta.
- **Tiene línea fija = No:** se predice que el cliente rechazará la oferta.

Ambas ramas clasifican correctamente los registros del conjunto utilizado, por lo que no es necesario realizar nuevas divisiones.

## 🔎 Ejemplos de predicción

**Caso A**

- Edad: 40 años.
- Uso de datos: 5 GB.
- Tiene línea fija: Sí.
- **Predicción:** aceptará la oferta.

**Caso B**

- Edad: 25 años.
- Uso de datos: 2 GB.
- Tiene línea fija: No.
- **Predicción:** rechazará la oferta.

## ✅ Conclusión

El análisis muestra que la variable **«Tiene línea fija»** es la más relevante para clasificar a los clientes dentro del conjunto de datos estudiado. Su ganancia de información de 1.0000 permite separar los registros en dos grupos homogéneos.

El ejercicio permite comprender cómo la entropía y la ganancia de información ayudan a seleccionar atributos para construir árboles de decisión.

👨‍🎓 Información académica

Trabajo práctico: Árbol de Decisión - Empresa de Telecomunicaciones
Materia: Procesamiento de Aprendizaje Automático
Alumna: Luciana Mansilla
Docente: Yanina Scudero
Fecha: 23 de septiembre de 2026

