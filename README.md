# 📊 Challenge 2 - Análisis de Evasión de Clientes | TelecomX LATAM

## 📌 Descripción
Análisis exploratorio de datos (EDA) para identificar los factores que 
influyen en la evasión de clientes (Churn) de TelecomX, empresa de 
telecomunicaciones latinoamericana. El objetivo es entender el comportamiento 
de los clientes y generar insights estratégicos para reducir la cancelación del servicio.

---

## 🗂️ Archivos del Repositorio

| Archivo | Descripción |
|---|---|
| `Challenge2_TelecomX_LATAM.ipynb` | Notebook principal con todo el análisis |
| `TelecomX_Data.json` | Dataset fuente en formato JSON |
| `TelecomX_diccionario.md` | Diccionario de variables del dataset |

---

## 🔧 Tecnologías Utilizadas
- **Python 3**
- **Pandas** — manipulación y limpieza de datos
- **Matplotlib / Seaborn** — visualizaciones estáticas con valores visibles
- **Plotly Express** — visualizaciones interactivas

---

## 📋 Etapas del Análisis

1. **Extracción** — Datos obtenidos desde una API en formato JSON anidado
2. **Limpieza** — Normalización con `pd.json_normalize()`, conversión de tipos, eliminación de nulos y duplicados
3. **EDA Categórico** — Distribución de evasión por género, tipo de contrato, método de pago y tipo de internet
4. **EDA Numérico** — Boxplots de tiempo de contrato, valor mensual, total cobrado y cuentas diarias
5. **Correlación** — Matriz de correlación entre variables numéricas y la evasión
6. **Informe Final** — Conclusiones e insights estratégicos con recomendaciones

---

## 🔍 Principales Hallazgos

- **26.6%** de los 7,043 clientes cancelaron el servicio
- Clientes con contrato **mensual**: 1,655 cancelaciones vs **anual**: 166 y **bienal**: 48
- Clientes que se van llevan en promedio **10 meses** vs **38 meses** los que se quedan
- El **cheque electrónico** concentra 1,071 cancelaciones — más del triple que otros métodos
- Usuarios de **fibra óptica** evaden más (1,297) que los de DSL (459)
- `tiempo_contrato` es la variable con mayor correlación con la evasión (**-0.35**)
- Clientes que se van pagan en promedio **$79.7/mes** vs **$64.5** los que se quedan

---

## 💡 Recomendaciones Estratégicas

1. **Incentivar contratos anuales o bienales** con descuentos para reducir evasión mensual
2. **Programa de retención en los primeros 12 meses** — período crítico de cancelaciones
3. **Revisar precio y calidad del servicio de fibra óptica** — alta evasión pese a ser premium
4. **Investigar el perfil de clientes con cheque electrónico** — fuertemente asociado a evasión
5. **Desarrollar modelo predictivo de Churn** usando: `tipo_contrato`, `tiempo_contrato`, 
   `valor_mensual` y `tipo_internet` como variables principales

---

## 🚀 Instrucciones para Ejecutar el Notebook

### Opción 1 — Google Colab (recomendado)
1. Abre el archivo `Challenge2_TelecomX_LATAM.ipynb` en Google Colab
2. Ve a **Runtime > Run all** (`Ctrl + F9`)
3. El notebook descarga automáticamente los datos desde la API

### Opción 2 — Local
```bash
# 1. Clona el repositorio
git clone https://github.com/rluzav/challenge2-telecomx.git

# 2. Instala las dependencias
pip install pandas matplotlib seaborn plotly

# 3. Ejecuta el notebook
jupyter notebook Challenge2_TelecomX_LATAM.ipynb
```
---
## 👤 Autor
**rluzav**  
Challenge realizado como parte del programa de formación en Data Science — Alura LATAM 🚀
