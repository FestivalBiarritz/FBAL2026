# FBAL — App de programación

## Qué es esto
Mini-app web (PWA) con la programación del festival, favoritos, stands, redes sociales y la ficha de detalle (foto/descripción/video) de cada película o concierto.

## Archivos
- index.html → toda la app
- manifest.json → permite "instalar" la app en el celular
- sw.js → funcionamiento offline
- icons/ → íconos de la app (ya con un recorte del cartel real)
- assets/header-strip.jpg → la franja del cartel real que aparece en el header

## Cómo cambiar la imagen del header por otra parte del cartel (o el cartel final)
1. Sustituye el archivo assets/header-strip.jpg por la nueva imagen, manteniendo el mismo nombre (o cambia el nombre y ajústalo en index.html, en la etiqueta `<img src="assets/header-strip.jpg">`)
2. Lo ideal es una imagen apaisada (mucho más ancha que alta), sin texto importante en los bordes, porque se recorta automáticamente

## Cómo agregar foto y video real a cada película/concierto
Busca `const events = [...]` en index.html. Cada actividad de cine/música que ya tiene `descFr`/`descEs` muestra una ficha al tocarla. Para agregar el video:
- Si es de YouTube: copia el ID del video (en la URL, lo que va después de `watch?v=`) y ponlo en el campo `video:"ESE_ID"` de esa actividad
- Mientras no haya video, la ficha muestra "Foto y video à venir" automáticamente

## Cómo publicar cambios
Cada vez que edites y subas los archivos a GitHub (botón "Edit" o "Upload files" en el repositorio), Vercel vuelve a publicar la app automáticamente en 30-60 segundos. No hay que hacer nada más.
