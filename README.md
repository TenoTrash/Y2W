# Y2W

Basado en el proyecto de https://github.com/obra/Youtube2Webpage

Y2W es un script en Perl para generar una página web a partir de un video de Youtube, basado en los subtítulos asociados a ese mismo video, junto a capturas del mismo.

./Y2W.pl project-name "videoURL" Lenguaje

Lenguaje es un código de dos letras que refleja el idioma del subtítulo, por ejemplo es, en, ch, etc

## Dependencias

* [yt-dlp](https://github.com/yt-dlp/yt-dlp)
* [ffmpeg](https://ffmpeg.org/)

## Uso

Para usarse, ejecute el script de Perl junto al nombre de la carpeta en donde se guardará el proyecto, la URL del video y el idioma

./Y2W.pl nombre-proyecto "https://www.youtube.com/watch?v=jNQXAC9IVRw" es

## Salida

Al ejecutar este script, se va a generar un repositorio con la siguiente estructura:

nombre-proyecto
├── images
│   └── (…).jpg
├── video.vtt
├── video.webm
├── index.html
└── styles.css

* index.html es la página web creada por este script.
* images contiene todas las capturas de pantalla, con un nombre tipo ```horas-minutos-segundos-milisegundos.jpg```.
* El archivo .vtt contiene los subtítulos.
* El archivo .webm contiene una copia del video en sí.
* El archivo style.css contiene los estilos de la página web.
