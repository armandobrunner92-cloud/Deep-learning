# Deep Learning - Vibe Coding

Colección de aplicaciones de inteligencia artificial desarrolladas en **Google Colab** con la técnica de *vibe coding*: el código se generó con asistencia de una IA a partir de prompts. Cada aplicación incluye una interfaz web hecha con **Gradio**.

**Autor:** Armando

## Contenido

| # | Trabajo | Archivo | Qué hace |
|---|---------|---------|----------|
| 1 | Red RNN: audio, manuscritos y traducción | [app_transcripcion_rnn.ipynb](app_transcripcion_rnn.ipynb) | Transcribe audios e imágenes de texto manuscrito (OCR con red CRNN) y traduce entre español, inglés, francés y alemán. |
| 2 | Red GAN: generación de imágenes | [app_gan_imagenes.ipynb](app_gan_imagenes.ipynb) | Entrena una DCGAN con MNIST y genera imágenes aleatorias nuevas. |
| 3 | Transformers: análisis de sentimientos | [app_sentimientos_transformers.ipynb](app_sentimientos_transformers.ipynb) | Clasifica el sentimiento de textos o archivos `.txt`/`.csv` con modelos Transformer multilingües. |
| 4 | Procesamiento de imágenes | [app_fotos_animales_bd.ipynb](app_fotos_animales_bd.ipynb) | Identifica animales en fotografías con CLIP y guarda el análisis en una base de datos con una tabla de características de animales. |
| 5 | Procesamiento de sonidos | [app_audios_comentarios_bd.ipynb](app_audios_comentarios_bd.ipynb) | Transcribe audios de comentarios de productos, detecta el sentimiento y guarda likes/dislikes y el análisis en la base de datos. |
| 6 | Procesamiento de textos | [app_textos_comentarios_bd.ipynb](app_textos_comentarios_bd.ipynb) | Analiza comentarios de productos escritos (o en CSV) y guarda sentimiento, estadísticas y palabras clave en la base de datos. |
| 7 | Procesamiento de PDF | [app_pdf_resumen_bd.ipynb](app_pdf_resumen_bd.ipynb) | Extrae el texto de PDF, genera un resumen y guarda el análisis en la base de datos. |
| 8 | Procesamiento de videos | [app_videos_resumen_bd.ipynb](app_videos_resumen_bd.ipynb) | Transcribe el audio de videos, genera un resumen, analiza las imágenes y guarda todo en la base de datos. |

## Tecnologías

- **Lenguaje:** Python
- **Modelos:** Whisper, EasyOCR (CRNN), MarianMT, XLM-RoBERTa, CLIP, DCGAN propia en PyTorch
- **Librerías:** PyTorch, Hugging Face Transformers, OpenCV, pypdf, pandas, Pillow, NumPy
- **Base de datos:** SQLite
- **Interfaz:** Gradio

## Cómo ejecutar

1. Abrir el notebook en [Google Colab](https://colab.research.google.com) (Archivo > Subir cuaderno, o abrirlo desde GitHub).
2. Activar la GPU: Entorno de ejecución > Cambiar tipo de entorno > T4.
3. Ejecutar las celdas en orden.
4. La última celda de cada notebook abre la interfaz de Gradio con un enlace público (`gradio.live`). Conviene abrirlo en una pestaña nueva del navegador.

## Notas

- Los modelos se descargan automáticamente la primera vez que se ejecuta cada notebook.
- Las bases de datos (`.db`) y las carpetas con archivos subidos se crean al ejecutar. En Colab se borran al cerrar la sesión; cada notebook explica cómo guardarlas en Google Drive.
- Los datos de las tablas de ejemplo son inventados y solo sirven para probar.
