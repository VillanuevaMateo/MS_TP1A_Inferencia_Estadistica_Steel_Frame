# 📊 Trabajo Práctico: Estadística Descriptiva Aplicada a Steel Frame

## 🧪 Ejemplo 3: Análisis de Calidad en Paneles de Steel Frame

Este trabajo práctico tiene como objetivo aplicar técnicas de estadística descriptiva e inferencial al análisis de calidad de paneles de Steel Frame producidos por dos proveedores diferentes.

---

## 📁 Descripción del Dataset

El conjunto de datos contiene registros de **200 paneles de Steel Frame**, generados a partir de una muestra ajustada del dataset original de 240 observaciones. Las variables medidas incluyen:

- `espesor_mm`: Espesor del perfil (en milímetros).
- `resistencia_fluencia_MPa`: Resistencia a la fluencia del acero (en MPa).
- `recubrimiento_zinc_g_m2`: Cantidad de zinc en el recubrimiento (en g/m²).
- `U_W_m2K`: Valor de transmitancia térmica del panel (en W/m²·K).
- `cumple_requisito_U`: Indicador booleano que señala si el panel cumple con el requisito térmico (U ≤ 0.40).
- `proveedor`: Letra identificadora del proveedor (`A` o `B`).

---

## 🔍 Análisis Realizado

### 3.1 Estadística Descriptiva

- Se calculan la **media**, **mediana** y **desviación estándar** del espesor de los perfiles (`espesor_mm`).
- Se evalúa la dispersión y consistencia entre paneles, observando si los espesores son homogéneos o presentan alta variabilidad.

### 3.2 Prueba de Hipótesis para Resistencia

- **Hipótesis nula (H₀):** μ = 240 MPa  
- **Hipótesis alternativa (H₁):** μ < 240 MPa  
- Se realiza una **prueba t de una muestra** con nivel de significancia α = 0.05 para verificar si la resistencia media cumple con el estándar.

### 3.3 Comparación entre Proveedores

- Se comparan los espesores promedio entre los proveedores A y B mediante una **prueba t para dos muestras independientes**.
- Se evalúa si hay diferencias significativas en la media de `espesor_mm`, con justificación sobre si se asumen varianzas iguales o distintas.
- Se reporta el valor **p** y la conclusión estadística.

### 3.4 Proporciones de Cumplimiento

- Se calcula la proporción de paneles que cumplen con el requisito térmico (`U ≤ 0.40`) por proveedor.
- Se realiza una **prueba de diferencia de proporciones** para evaluar si la tasa de cumplimiento difiere significativamente entre A y B.

### 3.5 Modelo Predictivo

- Se construye una **regresión lineal simple** donde:
  - Variable dependiente: `resistencia_fluencia_MPa`
  - Variable independiente: `espesor_mm`
- Se presenta la **ecuación estimada**, se interpreta el efecto del espesor sobre la resistencia, y se evalúa el **coeficiente de determinación (R²)**.

---

## 🛠 Herramientas utilizadas

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- SciPy / Statsmodels

---

## 📌 Requisitos

Antes de ejecutar los scripts, asegúrate de tener instaladas las dependencias:

```bash
pip install pandas numpy matplotlib scipy
