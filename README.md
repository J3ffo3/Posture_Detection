# Universidad Peruana de Ciencias Aplicadas

## INFORME TRABAJO FINAL

### CURSO
PROCESAMIENTO DE IMÁGENES

### DOCENTE
CARLOS FERNANDO MONTOYA CUBAS

### CARRERA
CIENCIAS DE LA COMPUTACIÓN

### SECCIÓN
CC61

### ALUMNOS

| CÓDIGO     | NOMBRES Y APELLIDOS                      |
|------------|------------------------------------------|
| U202118258 | Iam Anthony Marcelo Alvarez Orellana     |
| U20211d574 | Fabiana Nayeli Mallma Villanueva         |
| U202124269 | Jeffrey Ulises Diaz Villanueva           |

**JUNIO 2024**

---

## Tabla de Contenido

1. [Introducción](#introducción)
2. [Problemática](#problemática)
3. [Motivación](#motivación)
4. [Objetivos](#objetivos)
5. [Potencial solución](#potencial-solución)
6. [Desarrollo](#desarrollo)
7. [Conclusiones](#conclusiones)
8. [Recomendaciones](#recomendaciones)
9. [Bibliografía](#bibliografía)
10. [Anexo](#anexo)

---

## Introducción

En la era digital actual, el tiempo que los jóvenes y estudiantes pasan frente a la computadora ha aumentado considerablemente. Esta situación ha traído consigo numerosas ventajas, como la facilidad para realizar trabajos académicos y buscar información de manera rápida y eficiente. Sin embargo, este incremento en el uso de dispositivos electrónicos también ha generado una problemática significativa: el descuido de la salud postural.

Por ello, como grupo, proponemos como solución una aplicación de monitoreo postural que, mediante el uso de la cámara web, pueda alertar al usuario si adopta una postura incorrecta mientras está frente al monitor. Esta solución utilizará conceptos aprendidos en el curso de procesamiento de imágenes, como la segmentación de imágenes y el seguimiento de objetos, entre otros. Además, serán implementados en el lenguaje de programación Python y utilizando librerías de procesamiento de imágenes como OpenCV.

---

## Problemática

El uso prolongado de ordenadores y dispositivos móviles es fundamental entre los estudiantes universitarios de carreras de ingeniería, como ciencias de la computación, ingeniería de software y afines en Lima, Perú. Esta situación ha generado diversas preocupaciones en cuanto a los riesgos para la salud asociados a esta actividad, como fatiga ocular y trastornos musculoesqueléticos. Los estudiantes de estas disciplinas tienden a pasar largas horas frente a sus ordenadores debido a la demanda de sus cursos, que requieren programación, desarrollo de software y otras actividades intensivas en el uso de la computadora.

Según Hodelín Hodelín, de los Reyes García, Hurtado Cumbá y Batista Salmon (2016), pasar mucho tiempo frente a una pantalla puede provocar varios problemas de salud, como fatiga ocular, síndrome del ojo seco y trastornos musculoesqueléticos, incluyendo dolores de espalda y cuello. Estos problemas surgen especialmente cuando los usuarios no toman descansos regulares ni adoptan posturas ergonómicas adecuadas. Además, la tensión constante en los ojos y la postura estática pueden llevar a una disminución del rendimiento académico y afectar la calidad de vida de los estudiantes.

Por otra parte, el uso de dispositivos electrónicos móviles también ha sido identificado como un factor que contribuye al incremento de afecciones físicas entre los estudiantes. Hidalgo Cajo, Hidalgo Cajo, Mayacela Alulema y Hidalgo Cajo (2019) señalan que el uso excesivo de estos dispositivos está relacionado con problemas posturales y dolores musculares, debido a la postura encorvada que a menudo adoptan los usuarios. Este comportamiento se ha observado con frecuencia en entornos universitarios, quienes utilizan sus dispositivos móviles tanto para el estudio como para el entretenimiento.

Según este contexto, se propone el desarrollo de una aplicación que monitorea la postura mediante el uso de la cámara web, con el objetivo de mitigar estos riesgos al promover prácticas más saludables y posturas correctas durante el uso prolongado de dispositivos electrónicos. También se busca mejorar el rendimiento académico al reducir distracciones y controlar los tiempos de descanso en la rutina de estudio o trabajo.

---

## Motivación

La motivación detrás de este proyecto surge de nuestra propia experiencia como estudiantes de Ciencias de la Computación y usuarios frecuentes de computadoras y dispositivos electrónicos móviles, somos conscientes de los desafíos que enfrentamos en términos de salud debido al uso prolongado de estas tecnologías. Hemos experimentado personalmente la fatiga ocular, los dolores musculares y otros problemas relacionados con la postura, también el tiempo prolongado que invertimos frente a la pantalla.

Además, hemos observado que esta problemática no se limita a nuestra experiencia personal, sino que es común entre nuestros compañeros de carrera y otros estudiantes universitarios de las diferentes facultades. La creciente dependencia de la tecnología en la educación y el trabajo ha aumentado la necesidad de abordar estos problemas de salud de manera efectiva.

Consideramos que desarrollar una aplicación que monitorea la postura y promueve hábitos saludables frente a la pantalla no solo beneficiará a los estudiantes universitarios de Ciencias de la Computación, sino también a una amplia gama de usuarios que enfrentan desafíos similares en su vida diaria.

---

## Objetivos

### Objetivo General

Desarrollar una aplicación que monitoree la postura de los estudiantes mediante el uso de la cámara web en tiempo real.

### Objetivos Específicos

- Reducir los riesgos para la salud de los estudiantes que utilizan dispositivos electrónicos de manera prolongada.
- Diseñar una aplicación como recurso de apoyo para corregir la postura de los estudiantes.

---

## Potencial solución

### Técnicas a utilizar

- **Detección de bordes y segmentación**:
  - **Aplicación**: Utilizaremos técnicas de detección de bordes para identificar la silueta del alumno en la imagen captada por la cámara. Esto permitirá segmentar la región del cuerpo del alumno y centrarnos en el análisis de su postura.

- **Analizar la postura y la geometría**:
  - **Aplicación**: Como siguiente paso, emplearemos transformaciones geométricas para analizar la alineación de las partes del cuerpo del alumno (por ejemplo, espalda, cuello, hombros). Implementando este algoritmo, podremos calcular los ángulos entre las distintas partes del cuerpo para determinar si la postura es adecuada o inadecuada.

- **Reconocer y clasificar patrones**:
  - **Aplicación**: Después de aplicar las transformaciones geométricas, implementaremos técnicas de aprendizaje automático para clasificar las posturas detectadas como buenas o malas. Entrenaremos un modelo capaz de identificar automáticamente patrones asociados a malas posturas basándose en una base de datos previamente etiquetada.

- **Mejora de imágenes**:
  - **Aplicación**: Antes del entrenamiento del modelo, aplicaremos técnicas de mejora de imágenes para optimizar la calidad de las imágenes en el dataset. Esto facilitará el proceso de entrenamiento del modelo y garantizará la detección precisa de detalles relevantes para la evaluación de la postura, como la posición de la columna vertebral o la alineación de los hombros. Del mismo modo, implementaremos mejoras de imagen en los videos durante las pruebas.

- **Seguimiento de objetos y análisis temporal**:
  - **Aplicación**: Con el modelo entrenado, implementaremos técnicas de seguimiento de objetos para monitorizar el movimiento y la evolución de la postura del alumno en tiempo real. Esto proporcionará información continua sobre la postura mientras el alumno trabaja.

### Herramientas a utilizar

- Para el desarrollo de nuestro proyecto de Trabajo Final sobre la detección de postura para el monitoreo de una correcta postura, utilizaremos Python con bibliotecas como OpenCV para el procesamiento de imágenes y TensorFlow o PyTorch para las técnicas de aprendizaje automático. Para garantizar una correcta ejecución, realizaremos pruebas en Google Colab y Visual Studio.
- Para gestionar el flujo de trabajo y las dependencias del proyecto, utilizaremos herramientas como Git para el control de versiones y GitHub para la colaboración en línea. También utilizaremos Visual Studio Code como entorno de desarrollo integrado (IDE), por su flexibilidad y su amplio soporte de extensiones.
- Para garantizar la calidad de los datos, utilizaremos un conjunto de datos adecuado, buscando en plataformas como Kaggle y Hugging Face, que nos proporcionarán datos bien etiquetados y relevantes para nuestro objetivo.
- Además, integraremos herramientas especializadas como Mediapipe y OpenPose para el análisis avanzado de la postura y la detección de puntos corporales clave. Estas herramientas nos aportarán precisión y eficacia en la detección y el seguimiento de la postura de los alumnos.
- Finalmente, crearemos un prototipo de aplicación capaz de acceder a la cámara del dispositivo, capturar imágenes en tiempo real y analizar la postura utilizando las técnicas mencionadas anteriormente.

---

## Desarrollo

### Proyecto: [https://github.com/J3ffo3/Posture_Detection.git](https://github.com/J3ffo3/Posture_Detection.git)

### Primer paso: Preparación de los datos

En primer lugar, realizamos la búsqueda de un dataset adecuado para nuestro proyecto. Buscábamos un dataset que contuviera imágenes de personas en buenas y malas posturas. Cada imagen debía tener su correspondiente etiqueta, indicando los keypoints de cada persona en la imagen y especificando si la postura era buena o mala.

Encontramos el dataset ideal en la página Roboflow.com, bajo el nombre "human_pose". Este dataset estaba organizado de manera que facilitaba el entrenamiento de un modelo de reconocimiento de poses utilizando YOLOv8-Pose. Las imágenes estaban acompañadas de etiquetas que indicaban las ubicaciones de los keypoints, junto con su clase: 0 (mala postura) o 1 (buena postura).

Encontramos el dataset ideal en la página Roboflow.com, bajo el nombre "human_pose". Este dataset estaba organizado de manera que facilitaba el entrenamiento de un modelo de reconocimiento de poses utilizando YOLOv8-Pose. Las imágenes estaban acompañadas de etiquetas que indicaban las ubicaciones de los keypoints, junto con su clase: 0 (mala postura) o 1 (buena postura).

Para asegurar la calidad y consistencia en el entrenamiento del modelo, procesamos las imágenes del dataset para que todas tuvieran una resolución de 640x640 píxeles, tal como se requiere para entrenar el modelo de YOLOv8-Pose. Este preprocesamiento de las imágenes garantizó que nuestro modelo recibiera datos de alta calidad y consistentes, lo que es crucial para lograr un rendimiento óptimo en la detección de posturas.

Este dataset cumplía con los requisitos necesarios para el entrenamiento de nuestro modelo, proporcionando una base sólida para el desarrollo de un sistema eficiente de detección de posturas. El link de este dataset está anexado al final del informe.

### Segundo paso: Entrenamiento del modelo en Visual Studio con la librería de Ultralytics

Con los datos listos para el entrenamiento, procedimos a instalar las librerías necesarias en nuestro entorno de Python en Visual Studio. Primero, instalamos la librería de Ultralytics para poder entrenar nuestro modelo. Además, instalamos la librería MediaPipe para poder comparar los resultados obtenidos por esta librería con los de nuestro modelo.

MediaPipe ayuda a detectar posturas configurando una función sobre ángulos entre ciertos puntos clave para determinar si una postura es buena o mala. Sin embargo, no trabaja con un modelo de reconocimiento propiamente dicho, sino que utiliza operaciones matemáticas para calcular los ángulos entre los puntos clave detectados (como el oído, el hombro y la cadera en vista de perfil).

Nuestro objetivo es entrenar un modelo que automatice este proceso utilizando reconocimiento de imágenes en video, como YOLOv8-Pose. Entrenamos el modelo para que detecte si una persona está en buena o mala postura con una entrada de video de una persona de perfil (nuestro público objetivo son los estudiantes).

A continuación, mostramos imágenes de cada parte de este paso para ilustrar el proceso de entrenamiento del modelo.
- Importamos la librería de Ultralytics y comenzamos el entrenamiento utilizando un modelo preentrenado de YOLOv8m-pose. Este modelo preentrenado nos proporciona una base sólida, ya que ha sido previamente entrenado en un conjunto de datos diverso y puede reconocer poses humanas con precisión.
- Luego iniciamos el entrenamiento, proporcionándole el archivo .yaml, que contiene la ubicación de todas las imágenes con sus etiquetas en sus respectivas carpetas. Configuramos el entrenamiento para 30 épocas, con un tamaño de batch de 6 para evitar saturar la memoria RAM. Además, aseguramos que todas las imágenes estuvieran redimensionadas a 640x640 píxeles.
Resultados del entrenamiento, 
Análisis:
- El modelo muestra una mayor precisión y recall para la clase "good" (buena postura) en comparación con la clase "bad" (mala postura). Esto sugiere que el modelo detecta mejor las buenas posturas que las malas.

- La precisión global (mAP50) es razonablemente alta para ambas clases, pero mAP50-95, que es una medida más rigurosa, es inferior, lo que indica que el modelo tiene más dificultades para detectar correctamente las posturas en escenarios más variados.

- El tiempo de inferencia es aceptable para aplicaciones en tiempo real, con un total de unos 47,5 ms por imagen (incluyendo pre y post procesamiento).

- Estos resultados indican que el modelo tiene un buen rendimiento global, sobre todo en la detección de posturas correctas, y es adecuado para aplicaciones de control postural en tiempo real, por ejemplo para estudiantes sentados en sus pupitres.

### Tercer paso: Implementación del modelo
Una vez entrenado el modelo, lo implementamos en un script de Python para la detección de poses en tiempo real. Para ello, utilizamos OpenCV para capturar el vídeo en directo, el modelo YOLOv8 para la detección de poses y MediaPipe para analizar el ángulo de las articulaciones.

El código del entrenamiento del modelo y su implementación se encuentra disponible en nuestro repositorio de GitHub y en Google Colab (enlaces anexados en los anexos del informe, en la parte final).

A continuación, una breve explicación de lo que hace la implementación del modelo:
1. Carga del modelo: Se carga el modelo YOLOv8 para la detección de objetos y se inicializa MediaPipe para la detección de posturas.
2. Procesamiento de detecciones: Se procesan las detecciones de YOLOv8 y se dibujan los cuadros alrededor de los objetos detectados.
3. Análisis de posturas: Se procesan las detecciones de MediaPipe para detectar puntos clave en el cuerpo y calcular el ángulo del cuello.
4. Visualización: Se muestran las posturas detectadas y se resalta si hay una mala postura.
5. Interacción: Se muestra la ventana con las detecciones y se cierra si se presiona la tecla 'q'.
Para un mayor detalle sobre el funcionamiento, hemos subido un video explicativo a Google Drive, cuyo enlace también se encuentra anexado al final del documento.

## Conclusiones

### Precisión y Recall del Modelo:
- Nuestro modelo desarrollado muestra una mayor precisión y recall para la clase "good" (buena postura) en comparación con la clase "bad" (mala postura). Esto indica que el modelo identifica mejor las posturas correctas que las incorrectas.
- La precisión global (mAP50) es razonablemente alta para ambas clases, lo que indica un rendimiento sólido del modelo en general. Sin embargo, la medida mAP50-95, que evalúa la precisión en múltiples umbrales, es inferior. Esto implica que el modelo encuentra dificultades para detectar posturas en escenarios más variados y con diferentes grados de precisión.

### Aplicabilidad y Eficacia:
- Los resultados del modelo indican que es adecuado para su uso en aplicaciones de control postural en tiempo real, especialmente para estudiantes sentados en sus pupitres. La capacidad del modelo para detectar correctamente las buenas posturas puede servir como una herramienta eficaz para corregir y mantener una postura adecuada, reduciendo así los riesgos para la salud asociados con el uso prolongado de dispositivos electrónicos.

## Recomendaciones

### Mejora de la Detección de Malas Posturas:
- Dado que el modelo muestra un rendimiento inferior en la detección de malas posturas, recomendamos aumentar el entrenamiento del modelo con más ejemplos de malas posturas. Esto podría incluir datos adicionales y más variados que representan diferentes tipos de malas posturas.
### Evaluación Continua y Retroalimentación:
- Implementar un sistema de evaluación continua donde el modelo reciba retroalimentación constante sobre su rendimiento. Esto puede incluir la incorporación de un módulo de aprendizaje en línea que permita al modelo mejorar continuamente basado en nuevas entradas y correcciones.
### Interfaz de Usuario y Usabilidad:
- Diseñar una interfaz de usuario intuitiva y amigable que permita a los estudiantes y profesores interactuar fácilmente con la aplicación. Proporcionar alertas y sugerencias en tiempo real sobre la postura, además de ofrecer informes periódicos que ayuden a los estudiantes a mejorar su postura de manera proactiva.

## Bibliografía

- Hodelín Hodelín, Y., de los Reyes García, Z. L., Hurtado Cumbá, G., & Batista Salmon, M. (2016). Riesgos sobre tiempo prolongado frente a un ordenador. Universidad de Ciencias Médicas, Guantánamo, Cuba. Recuperado de https://www.redalyc.org/journal/5517/551762874018/551762874018.pdf [22/06/2024]

- Hidalgo Cajo, B. G., Hidalgo Cajo, D. P., Mayacela Alulema, A., & Hidalgo Cajo, I. M. (2019). El uso de dispositivos electrónicos móviles y su impacto en el incremento de afecciones en los estudiantes universitarios. Universidad Nacional de Chimborazo, Escuela Superior Politécnica de Chimborazo. Recuperado de https://revistasdigitales.upec.edu.ec/index.php/sathiri/article/view/906 [22/06/2024]

- Vikas Gupta. (2021, Junio). Human Pose Estimation using Keypoint RCNN in PyTorch. https://learnopencv.com/human-pose-estimation-using-keypoint-rcnn-in-pytorch/ [23/06/2024]

- Vikas Gupta. (2019, Febrero). Pose Detection comparison : wrnchAI vs OpenPose. https://learnopencv.com/pose-detection-comparison-wrnchai-vs-openpose/ [23/06/2024]

- TensorFlow. (2023, Diciembre). Estimación de poses.
https://www.tensorflow.org/lite/examples/pose_estimation/overview?hl=es
	[24/06/2024]

- Gabriela Solano. (2021, Mayo). Como instalar MEDIAPIPE | Python.
https://omes-va.com/como-instalar-mediapipe-python/
[24/06/2024]

## Anexo

- Link del video funcionalidad del proyecto: https://drive.google.com/drive/folders/1cbPKQl7cKOisAJQrUrXprLHeJx_HbxJU?usp=sharing

- Link del dataset utilizado:
https://universe.roboflow.com/ai-yeodd/human_pose-yndai/dataset/4

- Link del notebook en Google Colab - Training:
https://colab.research.google.com/drive/1jqaizcKnv9sP5Rs06fBkLOn4nq4YOH27?usp=sharing

- Link del notebook en Google Colab - Posture Detection:
https://colab.research.google.com/drive/1pJcx9VsjnVvquqL6r7397ig-fHa_-251?usp=sharing

- Link del GitHub del proyecto:
https://github.com/J3ffo3/Posture_Detection.git

- Link de la PPT en Canva: https://www.canva.com/design/DAGJMNTeZo0/nIOqpYAX79IjCNSqcuxaYA/edit?utm_content=DAGJMNTeZo0&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

