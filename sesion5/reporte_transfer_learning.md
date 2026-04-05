# Reporte: Transfer Learning
## ¿Qué es Transfer Learning?
El Transfer Learning es básicamente usar un modelo que ya fue entrenado antes para poder resolver otro problema. En vez de empezar desde cero, aprovechamos lo que el modelo ya sabe. Esto hace que el proceso sea mucho más rápido y eficiente. Lo que te podia llegar a tardar dias o semanas, lo podrias realizar en unas cuantas horas o incluso minutos ya que la informacion que tenias antes te servira para adaptarlo a una nueva situación, en lugar de aprender todo otra vez.

## ¿Qué modelo usaste?
Utilizamos el modelo MobileNetV2. Este modelo es una red neuronal convolucional optimizada para ser ligera y rápida, lo que
la hace ideal para dispositivos móviles o aplicaciones en tiempo real.
MobileNetV2 fue entrenado previamente con millones de imágenes, lo que le permite reconocer patrones visuales como formas, colores y texturas.

## Resultado de la predicción
Primero probamos con una imagen de un elefante descargada de internet. El modelo predijo correctamente "African elephant" con un porcentaje muy alto (más del 90%). Después también se podía probar con imágenes propias, y el modelo daba las 3 o 5 predicciones más probables. El modelo funcionó sin haber sido entrenado por nosotros.

## Parámetros congelados vs entrenables
En la parte de fine-tuning cargamos el modelo sin la capa final y congelamos todas sus capas. Luego agregamos una nueva cabeza clasificadora con capas Dense.
El resultado fue que más del 95% de los parámetros estaban congelados y solo un pequeño porcentaje (alrededor del 5%) era entrenable. Esto explica por qué el modelo puede adaptarse rápido usando pocos datos.

## Aplicación potencial
El Transfer Learning se puede usar para muchas cosas, como reconocimiento de objetos, clasificación de imágenes o incluso aplicaciones médicas. En pocas palabras, sirve cuando no tienes muchos datos y quieres aprovechar modelos ya entrenados.

## Dataset recolectado
En la sesión anterior hice un dataset sobre hábitos diarios.
Incluí datos como:
- horas de sueño
- entrenamiento
- tiempo de estudio
- uso de celular
- nivel de energía
- productividad
Este dataset luego lo usare para análisis con Pandas.

## Opinión personal
Lo más sorprendente de esta sesión fue ver cómo un modelo ya entrenado puede adaptarse tan rápido a un nuevo problema. Es impresionante que no sea necesario entrenar todo desde cero y aun así obtener buenos resultados.
