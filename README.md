# ¿Cuánto vale tu trabajo?

### Salario mínimo y desigualdad en 38 países europeos

Un análisis exploratorio de datos (EDA) sobre si el salario mínimo realmente protege a los trabajadores europeos. Comparamos lo que dice tu nómina con lo que realmente puedes comprar, y analizamos cómo la vivienda, la desigualdad de género y la pobreza laboral afectan a los trabajadores con salario mínimo.

**[Explorar la web interactiva](https://cuantovaletutrabajo.lovable.app)**

---

### [H1: El salario nominal engaña](https://cuantovaletutrabajo.lovable.app)

* Comparación del salario mínimo en euros (EUR) vs poder adquisitivo real (PPS) en 27 países de la UE
* 21 de 27 países cambian de posición en el ranking al ajustar por coste de vida
* Rumanía sube 8 posiciones: 703 EUR equivalen a 1.105 PPS. Irlanda baja 8
* **Keywords**: Pearson, PPS, Eurostat, scatter plot, ranking
* **Resultado**: **Validada** (r = 0.945, p < 0.001)

---

### [H2: Subir el SM es política de género](https://cuantovaletutrabajo.lovable.app)

* Análisis de la relación entre salario mínimo y brecha salarial de género
* Test con datos panel (344 obs): r = -0.299, p < 0.001. Test snapshot (2014): p = 0.58
* La correlación existe pero está confundida por tendencias temporales
* **Keywords**: Brecha de género, correlación temporal, panel vs snapshot
* **Resultado**: **Parcialmente validada**

---

### [H3: Con el SM no se paga el alquiler](https://cuantovaletutrabajo.lovable.app)

* Comparación de velocidades de crecimiento: salario mínimo vs precios de vivienda (2015-2024)
* En 8 de 10 países la vivienda crece más rápido que el salario
* Portugal: vivienda +124% vs salario +61%. Solo España y Rumanía son excepciones
* **Keywords**: Índice de vivienda, crecimiento porcentual, emancipación
* **Resultado**: **Validada** (por crecimiento, no por correlación)

---

### [H4: Tener empleo no te saca de pobre](https://cuantovaletutrabajo.lovable.app)

* El 8,6% de los trabajadores europeos son pobres a pesar de tener empleo
* Desempleo y pobreza laboral son problemas diferentes (r = 0.287)
* Luxemburgo: SM más alto de Europa pero 13,5% de pobreza laboral
* **Keywords**: Working poor, pobreza laboral, calidad del empleo
* **Resultado**: **Validada** (r = -0.245, p < 0.001)

---

### [H5: La Gen Z trabaja más para vivir peor](https://cuantovaletutrabajo.lovable.app)

* En 27 de 28 países el salario real (descontando inflación) ha subido desde 2008
* Pero combinado con H3 (vivienda sube más), la capacidad de emancipación ha bajado
* Europa Occidental prácticamente estancada: Bélgica +3,8% en 16 años
* **Keywords**: Inflación, HICP, salario real, deflactación, Gen Z
* **Resultado**: **Refutada** (pero cierta en experiencia vivida: H3+H5)

---

## Dataset final

`dataset_europa_final.csv`: **1.016 filas x 12 columnas** | 38 países | 1999-2026

## Tecnologías

Python, Pandas, NumPy, Plotly Express, SciPy (Pearson), Matplotlib, Seaborn, Requests (API Eurostat), Lovable (web)

## Estructura del repositorio

```
src/
  data/
    dataset_europa_final.csv
    salario_minimo.tsv
    pib_percapita.tsv
    precios_vivienda.tsv
    gini.tsv
    brecha_genero.tsv
  notebooks/
    EDA_Andoni.ipynb
    EDA_Hipotesis.ipynb
  utils/
    eurostat_api.py
  main.ipynb
docs/
  Memoria_Proyecto_EDA.pdf
  presentacion_final.pptx
  Guia_Rapida_EDA.pdf
  Guia_Completa_EDA.pdf
README.md
```

## Autor

Andoni Olaso - Data Science Bootcamp, 2026
