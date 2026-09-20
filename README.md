# Análisis exploratorio y limpieza de datos agrícolas

## Descripción

Este proyecto presenta un análisis exploratorio y un proceso de limpieza de datos sobre estimaciones agrícolas de Argentina, utilizando Python y Pandas. El objetivo es preparar los datos para su análisis y obtener algunos indicadores relevantes sobre producción y rendimiento.

## Origen de los datos

El dataset contiene registros de estimaciones agrícolas correspondientes a distintos cultivos, provincias y departamentos de Argentina.

Los datos fueron obtenidos del portal oficial de datos abiertos de Argentina:

**Fuente:** [Estimaciones agrícolas - Datos Argentina](https://datos.gob.ar/dataset/estimaciones-agricolas/resource/2f3d94e1-9e58-5e51-a25d-d6c2bbc697fe)

El archivo fue utilizado en formato CSV para realizar el proceso de exploración, limpieza y análisis mediante Python y Pandas.

## Limpieza y preparación

El dataset inicial contenía 160.499 registros y 11 columnas. Durante el diagnóstico se detectaron 8 registros con valores faltantes en variables relacionadas con la ubicación geográfica.

Debido a que no existía información suficiente para determinar esos valores de forma confiable, se decidió eliminar dichos registros. También se verificó la ausencia de duplicados y se restableció el índice después de la eliminación.

Por último, se corrigieron los tipos de datos de `provincia_id` y `departamento_id`, convirtiéndolos de `float64` a `int`, ya que representan identificadores enteros.

## Análisis realizado

Se realizaron tres agrupaciones principales:

- Producción total por cultivo.
- Producción total por provincia.
- Rendimiento promedio por cultivo.

Estas operaciones permiten obtener una primera visión de la distribución de la producción y el rendimiento agrícola dentro del dataset.