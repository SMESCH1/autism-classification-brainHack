# Autism Classification — BrainHack

<p align="center">
  <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-1.x-F7931E?logo=scikitlearn&logoColor=white">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white">
  <img alt="Jupyter" src="https://img.shields.io/badge/Jupyter-notebooks-F37626?logo=jupyter&logoColor=white">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-blue">
</p>

> Unsupervised clustering (**KMeans**) and supervised classification (**Logistic Regression**) on neuroimaging-derived features for **autism spectrum disorder (ASD)**, developed during a BrainHack workshop.

🇬🇧 English below · 🇪🇸 Versión en español primero.

---

## 🇪🇸 Resumen

Proyecto de machine learning desarrollado durante un BrainHack (workshop colaborativo de neurociencia computacional) cuyo objetivo es clasificar sujetos en dos grupos (control vs. condición del espectro autista) a partir de features extraídas de neuroimágenes.

### Lo que hay en este repo

| Notebook | Qué hace |
|----------|----------|
| `final_analysis.ipynb` | Pipeline completo: EDA, preprocesamiento, clustering no supervisado (KMeans con `n_clusters=2`) y clasificación supervisada (Logistic Regression). |
| `Clasificador_Autismo_Brainhack.ipynb` | Versión anterior / exploratoria del clasificador. |
| `BasesDeDatos/1_Intro_DBs/intro_sql.ipynb` | Notebook de soporte sobre acceso a las bases de datos del workshop. |

### Stack
scikit-learn · pandas · numpy · matplotlib · jupyter

### Resultados principales
- **KMeans (k=2)** sobre features estandarizadas: separa parcialmente las clases en el espacio latente, pero no de forma limpia (la condición no es linealmente separable solo con clustering no supervisado).
- **Logistic Regression** entrenada con `random_state=3` sobre el split de entrenamiento.
- Métricas detalladas y matriz de confusión en el notebook.

> ⚠️ **Limitación importante:** dado el tamaño del dataset y la naturaleza de la tarea, los resultados son **exploratorios**, no clínicos. El objetivo del workshop era pedagógico.

### Cómo correr
```bash
pip install -r requirements.txt
jupyter lab final_analysis.ipynb
```

### Autor
**Sebastián Mesch Henriques** — [@SMESCH1](https://github.com/SMESCH1)
Desarrollado en el contexto de **BrainHack**.

---

## 🇬🇧 Summary

Machine learning project developed during a **BrainHack** (collaborative computational neuroscience workshop). The goal is to classify subjects into two groups (control vs. autism spectrum condition) using features derived from neuroimaging data.

### What's in this repo

| Notebook | What it does |
|----------|--------------|
| `final_analysis.ipynb` | Full pipeline: EDA, preprocessing, unsupervised clustering (KMeans, `n_clusters=2`), and supervised classification (Logistic Regression). |
| `Clasificador_Autismo_Brainhack.ipynb` | Earlier exploratory version of the classifier. |
| `BasesDeDatos/1_Intro_DBs/intro_sql.ipynb` | Support notebook on accessing the workshop databases. |

### Stack
scikit-learn · pandas · numpy · matplotlib · jupyter

### Key findings
- **KMeans (k=2)** on standardized features partially separates the two classes in latent space — but not cleanly, since the condition is not linearly separable from clustering alone.
- **Logistic Regression** trained on `random_state=3` over the train split.
- Detailed metrics and confusion matrix in the notebook.

> ⚠️ **Important caveat:** given dataset size and task nature, results are **exploratory, not clinical**. The workshop goal was pedagogical.

### How to run
```bash
pip install -r requirements.txt
jupyter lab final_analysis.ipynb
```

### Suggested `requirements.txt`
```
scikit-learn>=1.3
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
jupyter>=1.0
```

### Author
**Sebastián Mesch Henriques** — [@SMESCH1](https://github.com/SMESCH1)
Developed in the context of **BrainHack**.

### License
MIT — see `LICENSE`.
