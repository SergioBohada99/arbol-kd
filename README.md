# Análisis de Tarifas y Clasificación con Árbol KD

Este proyecto implementa un árbol KD (k-dimensional) para clasificar tarifas de energía eléctrica en Colombia, utilizando datos abiertos del portal oficial [Datos Abiertos Colombia](https://www.datos.gov.co/).

Se ha realizado un preprocesamiento, transformación de clases con base en percentiles y visualización jerárquica interactiva del árbol.

---

## 📁 Datos

El conjunto de datos proviene del archivo:

**Tarifas_y_Costos_de_Energía_Eléctrica_para_el_Mercado_Regulado_20250429.csv**

Cada fila representa los costos del servicio eléctrico para el mercado regulado, con atributos como:

- Costo de compra de energía (`Costo Compra (Gm,i)`)
- Transporte (`STN`, `SDL`)
- Comercialización (`CVm,i,j`)
- Pérdidas y restricciones (`PRn,m`, `Rm`)
- Costo fijo mensual
- Costo total (`COT`)
- Costo unitario total (`CU Total`, convertido a clase 0, 1 o 2)

---

## 🎯 Objetivo

1. Clasificar los costos energéticos (`CU Total`) en tres clases:

   - Clase 0 → Bajo
   - Clase 1 → Medio
   - Clase 2 → Alto

2. Construir un árbol KD utilizando los atributos numéricos restantes para dividir recursivamente los ejemplos en función de su valor.

3. Visualizar el árbol KD de forma jerárquica e interactiva con PyVis.

---

## 🧠 ¿Qué es un Árbol KD?

Un árbol KD divide recursivamente los datos usando distintos atributos como ejes de división, alternando entre ellos (X₀, X₁, ...), usando la mediana como punto de corte. Esto permite particionar el espacio en regiones y encontrar estructuras o vecinos cercanos de forma eficiente.

---

## 📊 Visualización

El árbol se visualiza en un archivo HTML interactivo:

```bash
arbol_kd.html
```
