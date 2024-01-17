# Aplicación para inferencia del modelo de segmentación semantica en video VGG-Unet
<p align="justify"> En este repositorio se tiene los archivos .ipynb para ser ejecutados en Google Colab y siguiendo el link https://drive.google.com/drive/folders/1poLxrX4AD2HyrKVipEzJMxONQHqrbKs_?usp=sharing se puede encontrar el modelo y el video para realizar la inferencia del modelo. Todo el proceso fue realizado por medio del Framework Keras Tensorflow.
  
El archivo **Dataset.ipynb** permite extraer imágenes y etiquetas para entrenar el modelo de segmentación somática. Construido a partir del Dataset de Microsft COCO filtrada con los objetos de interés como (Background, Vaso, Laptop, Persona) por medio de FifthyOne que es una herramienta de código abierto que permite construir datasets a partir de otros dataset, filtrando la cantidad de imágenes y los objetos de interés.

El archivo **Entrenamiento.ipynb** permite realizar el entrenamiento del modelo de segmentación. Descarga el dataset filtrado con **Dataset.ipynb** por medio de la plataforma Roboflow y lo usa para realizar la construcción del modelo VGG 16 como encoder o backbone y Unet como decoder. Ambos modelos constituyen la arquitectura de red neuronal que permite entrenar el modelo de segmentación somática. 

El archivo **InferenceVideo.ipynb** por medio de un video de entrada en este caso se utilizó el almacenado en el enlace anteriormente mencionado el nombre es **"_import_61ea45b28b2592.20292381.mov"** se predice la segmentación por medio del modelo también almacenado en el mismo enlace que tiene el nombre de **"semasegUltimate.keras"**. El script genera un archivo de video de extensión .mp4 listo para ser descargado y visto de forma local con las etiquetas y sus colores asociados. En el link esta el archivo generado.
</p>

![alt text](https://divamgupta.com/assets/images/posts/imgseg/image6.png?style=centerme)*Encoder-Decoder with skip connections.*
