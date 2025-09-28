# Credit Card Fraud Detection Dataset
## Predicción de Fraude en Transacciones de Tarjeta de Crédito

### Trabajo Final - Big Data, Machine Learning & Econometrics
**Universidad Torcuato Di Tella**  
**Profesor:** Gabriel Martos Venturini  
**Período:** 2025

---

## Descripción del Dataset

Este repositorio contiene el dataset utilizado para el análisis comparativo de técnicas de Machine Learning versus métodos econométricos tradicionales en la predicción de fraude en transacciones de tarjeta de crédito.

### Características del Dataset
- **Observaciones:** 1,296,675 transacciones
- **Variables:** 24 variables (temporal, geoespacial, demográfica, transaccional)
- **Período temporal:** 2019-2020
- **Variable objetivo:** `is_fraud` (clasificación binaria)
- **Tamaño:** 354 MB (almacenado via Git LFS)

### Variables Principales
| Categoría | Variables |
|-----------|-----------|
| **Temporales** | `trans_date_trans_time`, `unix_time` |
| **Transaccionales** | `amt`, `merchant`, `category` |
| **Demográficas** | `first`, `last`, `gender`, `dob`, `job` |
| **Geoespaciales** | `lat`, `long`, `merch_lat`, `merch_long` |
| **Objetivo** | `is_fraud` (0=legítima, 1=fraude) |

## Fuente Original

**Dataset primario:** [Kaggle - Credit Card Transactions Dataset](https://www.kaggle.com/datasets/priyamchoksi/credit-card-transactions-dataset)  
**Autor original:** priyamchoksi  
**Licencia:** Disponible para uso académico y educativo

## Metodología del Proyecto

Este dataset forma parte de un análisis académico que implementa:

1. **Análisis Exploratorio** - Caracterización de patrones de fraude
2. **Feature Engineering** - Variables derivadas temporales y geoespaciales  
3. **Benchmarking Econométrico** - Modelos logísticos tradicionales
4. **Machine Learning** - Ridge/Lasso, Random Forest, SVM, KNN, Redes Neuronales
5. **Evaluación Comparativa** - Trade-off interpretabilidad vs. capacidad predictiva

## Estructura del Repositorio

```
├── data/
│   └── raw/
│       └── credit_card_transactions.csv    # Dataset principal (Git LFS)
├── README.md                               # Documentación
├── LICENSE                                 # Licencia MIT
└── .gitattributes                         # Configuración Git LFS
```

## Uso del Dataset

### Carga en R
```r
# Carga directa desde GitHub
url_dataset <- "https://raw.githubusercontent.com/DrDarioDiaz/credit-card-fraud-detection-ml/main/data/raw/credit_card_transactions.csv"
data <- read.csv(url_dataset)

# Verificación
cat("Dataset cargado:", nrow(data), "observaciones,", ncol(data), "variables\n")
```

### Carga en Python
```python
import pandas as pd

# Carga directa desde GitHub
url_dataset = "https://raw.githubusercontent.com/DrDarioDiaz/credit-card-fraud-detection-ml/main/data/raw/credit_card_transactions.csv"
data = pd.read_csv(url_dataset)

print(f"Dataset cargado: {data.shape[0]} observaciones, {data.shape[1]} variables")
```

## Consideraciones Técnicas

- **Git LFS requerido** para clonar el repositorio completo
- **Conexión a internet necesaria** para carga directa via URL
- **Memoria RAM recomendada:** Mínimo 2GB para procesamiento completo

## Citación Académica

Si utiliza este dataset en trabajos académicos, cite apropiadamente:

```
Díaz, D. (2025). Credit Card Fraud Detection Dataset. 
Trabajo Final Big Data, ML & Econometrics. 
Universidad Torcuato Di Tella. 
https://github.com/DrDarioDiaz/credit-card-fraud-detection-ml
```

## Uso Académico y Ético

- **Propósito educativo:** Dataset disponible para investigación y aprendizaje
- **Datos sintéticos:** El dataset contiene información simulada, no datos reales de clientes
- **Reproducibilidad:** Versionado para garantizar resultados reproducibles
- **Integridad académica:** Cite apropiadamente el uso de este repositorio

## Contacto

**Repositorio mantenido por:** [Su Nombre]  
**Institución:** Universidad Torcuato Di Tella  
**Curso:** Big Data, Machine Learning & Econometrics  
**Año académico:** 2025

---

## Licencia

Este proyecto está bajo la Licencia MIT - vea el archivo [LICENSE](LICENSE) para detalles.

## Disclaimer

Este dataset se proporciona "tal como está" para fines educativos. Los datos son sintéticos y no representan información real de clientes o transacciones financieras.
