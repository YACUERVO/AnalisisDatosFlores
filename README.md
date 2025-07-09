# 🌸 Análisis Estadístico de Flores por Especie (Python)

Este proyecto realiza un análisis estadístico básico (promedio y desviación estándar) de características florales, agrupadas por especie, usando programación orientada a objetos en Python. Es ideal como ejercicio introductorio al manejo de datos, clases y funciones estadísticas.

---

## 📌 Características Analizadas

Cada flor se describe mediante las siguientes características:

- Longitud del sépalo
- Ancho del sépalo
- Longitud del pétalo
- Ancho del pétalo
- Especie (nombre)

---

## 🧠 Objetivo del Proyecto

1. Agrupar flores por especie.
2. Calcular:
   - Promedio de cada característica.
   - Desviación estándar de cada característica.
3. Presentar un análisis estructurado por especie.

---

## 🛠️ Estructura del Proyecto

- `Flor`: clase que calcula estadísticas para un conjunto de flores.
- `agrupar_por_especie()`: función que agrupa los datos por especie.
- `main.py` o archivo de prueba: contiene datos de ejemplo y ejecución del análisis.

---

## 🧪 Ejemplo de uso

```python
from flor import Flor
from agrupador import agrupar_por_especie

# Lista de flores: 4 características + especie (último elemento)
datos = [
    [5.1, 3.5, 1.4, 0.2, 'Iris-setosa'],
    [4.9, 3.0, 1.4, 0.2, 'Iris-setosa'],
    [7.0, 3.2, 4.7, 1.4, 'Iris-versicolor']
]

# Agrupar por especie
grupos = agrupar_por_especie(datos)

# Analizar cada grupo
for especie, caracteristicas in grupos.items():
    flor = Flor(
        caracteristicas['Longitud_sepalo'],
        caracteristicas['ancho_sepalo'],
        caracteristicas['longitud_petalo'],
        caracteristicas['ancho_petalo']
    )
    print(f"\n📊 Análisis para {especie}")
    print(flor.analisis())

