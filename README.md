# Proyecto ML Churn Telco

Proyecto de aprendizaje automatico para analizar churn de clientes Telco, limpiar el dataset, entrenar un pipeline base y guardar el modelo entrenado.

## Contenido

- `Proyecto_ML_Churn_Abel_Flores.ipynb`: notebook principal con carga de datos, limpieza, analisis exploratorio, entrenamiento y evaluacion.
- `Telco_customer_churn.csv`: dataset usado por el notebook.
- `pipeline_churn_telco.pkl`: pipeline entrenado y serializado con `joblib`.
- `requirements.txt`: dependencias necesarias para ejecutar el proyecto.

## Requisitos

Se recomienda usar un entorno virtual:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

## Uso

1. Abre `Proyecto_ML_Churn_Abel_Flores.ipynb`.
2. Selecciona el kernel de Python del entorno `.venv`.
3. Ejecuta todas las celdas.
4. Al finalizar, se genera o actualiza `pipeline_churn_telco.pkl`.

## Correcciones importantes

El dataset original usa nombres de columnas con espacios. El notebook crea alias para evitar errores comunes:

- `TotalCharges` se crea desde `Total Charges`.
- `Churn` se crea desde `Churn Label`.
- `ChurnTarget` se crea desde `Churn Value`.

Tambien se eliminan los registros donde `Total Charges` viene vacio antes del entrenamiento.

## Validacion

El notebook fue ejecutado de punta a punta con el entorno del proyecto:

- 15 celdas de codigo ejecutadas.
- 0 errores guardados en el notebook.
- `pipeline_churn_telco.pkl` carga correctamente y genera predicciones.
