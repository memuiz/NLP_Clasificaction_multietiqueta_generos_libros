# Proyecto NLP - Clasificación de libros según género literario

El desarrollo del siguiente trabajo consite en la clasificación miltietiqueta de libros en sus respectivos géneros dada la sinopsis de estos. Bajo este objetivo obtendremos los datos mediante recopilación automática de la web OpenLibrary, aplicaremos técnicas de limpieza y normalización de texto además de probar distintas metodologías de clasificación con modelos propios y modelos pre-entrenados.

Contenidos:
  - Libros_raw.csv : datos en bruto extraídos a partir de webscraping
  - Libros_filtrado.csv : datos limpios procesados
  - embeddings_limpio.npy y embeddings_sentences_transformers.npy: contienen los embeddings realizados, se pueden cargar para ejecutar los modelos u observar las proyección sin necesidad de generarlo cada vez, con el objetivo de reducir el tiempo de ejecución.
  - ProyectoNLP.ipynb : Notebook que contiene el código empleado
  - ProyectoNLP_memoria.pdf : Memoria del trabajo
  - ProyectoNLP_presentacion.pdf : Presentación del trabajo

Requirements:
Para la elaboración del proyecto se ha hecho uso de Google Collab donde, sobre el entorno habitual, se han instalado adicionalmente otras librerías, que se pueden ver en el notebook de código ejecutado.

Pasos:
1- WebScraping: OpenLibrary API
Recolección de datos de la página web de reseñas de libros llamada “OpenLibrary”. Esta nos proporciona una API que nos permitirá descargar conjuntos de descripciones de libros en formato .json para agilizar el proceso, obteniendo título, descripción y género de las obras.

2- Tratamiento de datos y preprocesado
Limpieza del dataset realizando pasos como la eliminación de contenido no relevante, normalización del texto, lematizado y otros. Agrupamiento de géneros. Seguidamente aplicaremos algunas técnicas de extracción de características como BoW, TFIDF y obtención de embeddings.

3-Modelo propio de clasificación
Construir un modelo propio de clasificación de género, empleando funciones disponibles en la librería scikit-learn, entrenándolo a partir de las características extraídas anteriormente mencionadas: Bag of Words, TF-IDF y embeddings (Bert y Sentence embeddings).

4-Modelo pre-entrenado
Fine-tuning de tres formas distintas para adaptarlo a nuestro problema de clasificación a partir del texto limpio pero sin preprocesado.


