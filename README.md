# Prueba 2026

Proyecto de entrenamiento en Google Colab para crear un detector de botellas listo para Android.

## Notebook principal

El archivo `PRUEBA2026.ipynb` prepara un dataset YOLO en `.zip`, valida imagenes y etiquetas `.txt`, divide los datos en entrenamiento, validacion y prueba, entrena un modelo EfficientDet-Lite1 con TensorFlow Lite Model Maker y exporta modelos `.tflite` para Android.

## Uso basico

1. Abrir `PRUEBA2026.ipynb` en Google Colab.
2. Activar GPU en `Entorno de ejecucion > Cambiar tipo de entorno de ejecucion`.
3. Ejecutar la celda 1 para crear el entorno Python 3.9 compatible con TensorFlow Lite Model Maker.
4. Subir el `.zip` con imagenes y etiquetas YOLO en la celda 2.
5. Ejecutar las celdas restantes para crear el script, entrenar y descargar el paquete Android.

El notebook usa un entorno Python 3.9 separado porque `tflite-model-maker==0.4.3` depende de `scann==1.2.6`, que no está disponible para Python 3.10/3.11 en Colab.

## Resultado

El notebook descarga un paquete `efficientdet_lite1_botellas_android.zip` con:

- modelo Float16 para usar con GPU Delegate;
- modelo INT8 para probar en CPU;
- `labels.txt`;
- `data.yaml`;
- CSV de anotaciones;
- resultados de evaluacion;
- archivo de informacion del modelo.
