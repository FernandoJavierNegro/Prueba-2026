# Prueba 2026

Proyecto de entrenamiento en Google Colab para crear un detector de botellas listo para Android.

## Notebook principal

El archivo `PRUEBA2026.ipynb` prepara un dataset YOLO en `.zip`, valida imagenes y etiquetas `.txt`, divide los datos en entrenamiento, validacion y prueba, entrena un modelo EfficientDet-Lite1 con TensorFlow Lite Model Maker y exporta modelos `.tflite` para Android.

## Uso basico

1. Abrir `PRUEBA2026.ipynb` en Google Colab.
2. Activar GPU en `Entorno de ejecucion > Cambiar tipo de entorno de ejecucion`.
3. Ejecutar la celda de instalacion.
4. Reiniciar la sesion de Colab cuando termine la instalacion.
5. Ejecutar el resto del notebook y subir el `.zip` con imagenes y etiquetas YOLO.

## Resultado

El notebook descarga un paquete `efficientdet_lite1_botellas_android.zip` con:

- modelo Float16 para usar con GPU Delegate;
- modelo INT8 para probar en CPU;
- `labels.txt`;
- `data.yaml`;
- CSV de anotaciones;
- resultados de evaluacion;
- archivo de informacion del modelo.
