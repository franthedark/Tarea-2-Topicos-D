# Tarea-2-Topicos-D
Este repositorio contiene una serie de cuadernos de Jupyter que documentan el flujo de trabajo completo de un proyecto de Machine Learning, desde la exploración inicial de los datos hasta la evaluación final del modelo. El proyecto utiliza el conjunto de datos **NSL-KDD**, un estándar en la investigación de sistemas de detección de intrusiones en red (IDS).

## Estructura de Carpetas Recomendada

Para que los notebooks funcionen correctamente (especialmente los scripts de carga de datos), se recomienda organizar el repositorio de la siguiente manera:

```
/
├── notebooks/
│   ├── 6_Visualizacion_conjunto_datos.ipynb
│   ├── 7_División_del_conjunto_datos.ipynb
│   ├── 8_Preparación_del_conjunto_datos.ipynb
│   ├── 9_Creación_de_Transformadores_y_Pipelines.ipynb
│   └── 10_Evaluación_de_resultados.ipynb
├── datasets/
│   ├── KDDTrain+.csv           # Archivo de entrenamiento principal
│   └── KDDTest+.csv            # Archivo de prueba
└── README.md
```

---

## Descripción de los Notebooks

Los cuadernos deben ejecutarse en orden secuencial, ya que cada uno construye sobre los resultados o conceptos del anterior:

### 1. [6] Visualización del conjunto de datos
Se realiza el **Análisis Exploratorio de Datos (EDA)**. Aquí aprendemos a cargar los datos sin cabeceras, asignar nombres a las columnas y entender la distribución de las clases (tráfico normal vs. ataques) mediante gráficas y matrices de correlación.

### 2. [7] División del conjunto de datos
Se enfoca en la metodología de particionado. Se implementa el **muestreo estratificado (Stratified Sampling)** para garantizar que los subconjuntos de entrenamiento y prueba sean representativos de la población original, evitando sesgos en el modelo.

### 3. [8] Preparación del conjunto de datos
Fase de **limpieza y preprocesamiento**. Se tratan los valores faltantes (imputación), se escalan los valores numéricos mediante `RobustScaler` y se transforman las variables categóricas (como protocolos de red) a numéricas usando `OneHotEncoder`.

### 4. [9] Creación de Transformadores y Pipelines personalizados
Se introduce la **automatización del flujo de trabajo**. Se crean clases personalizadas y `Pipelines` de Scikit-Learn para encapsular todas las transformaciones en un solo objeto, facilitando la reproducibilidad y evitando la "fuga de datos" (data leakage).

### 5. [10] Evaluación de resultados
Fase final de validación. Se analizan métricas de rendimiento más allá de la precisión simple, incluyendo la **Matriz de Confusión**, el **F1 Score** y la **Curva ROC**, para asegurar que el modelo detecte eficazmente las anomalías en la red.

---

## Requisitos Técnicos

Para ejecutar estos cuadernos, necesitarás un entorno de Python 3.x con las siguientes librerías:

* **Pandas:** Manipulación de estructuras de datos.
* **NumPy:** Operaciones numéricas.
* **Matplotlib / Seaborn:** Visualización de datos.
* **Scikit-Learn:** Algoritmos de ML, preprocesamiento y evaluación.

---

## Cómo empezar

1. Clona este repositorio.
2. Asegúrate de colocar los archivos del dataset NSL-KDD en la carpeta `/datasets`.
3. Abre Jupyter Notebook o Google Colab y comienza por el cuaderno número **6**.
