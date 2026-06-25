# FBAL — App de programación

## Qué hay en esta versión
- Splash inicial con el cartel del festival (aparece y desaparece solo)
- Página de Inicio (Accueil): aftermovie 2025, redes sociales, sitio web, playlist, botón para ir al programa
- Programa con filtros por día/categoría, duración y hora de salida calculada
- Ficha de detalle (foto/descripción/video) en cada película o concierto, con botón de billetería
- Favoritos (itinerario personal)
- Stands con ficha de detalle y link a redes sociales
- Sección Infos: hashtag, goodies, billetería

## Archivos
- index.html → toda la app
- manifest.json → instalación en el celular
- sw.js → funcionamiento offline
- icons/ → íconos de la app (personajes reales del cartel)
- assets/header-strip.jpg → franja de personajes en el header
- assets/affiche-full.jpg → cartel completo usado en el splash de apertura

## Cómo cambiar el link de billetería
Busca `billetweb.fr/festival-biarritz-amerique-latine-2026` en index.html — aparece en 2 lugares (pestaña Infos y el botón dentro de cada ficha de película/concierto). Cámbialo en ambos si llega a cambiar.

## Cómo agregar video/foto a una película o concierto
En `const events = [...]`, cada actividad tiene un campo `video`. Pon ahí el ID de YouTube (lo que va después de `watch?v=` en la URL). Mientras no haya video, se muestra "Foto y video à venir" automáticamente.

## Cómo agregar redes sociales a un stand
En `const stands = [...]`, cada stand tiene un campo `social`. Pon ahí el link de Instagram (o lo que sea) de ese stand. Mientras esté en `null`, el botón dice "Redes próximamente" y no es clicable.

## Cómo cambiar el aftermovie
Busca `9ZaVxVQamcM` en index.html (es el ID del video de YouTube) y sustitúyelo por el ID del video que quieras usar.

## Ideas para seguir personalizando (cuando haya tiempo)
- Mapa visual del village con los stands ubicados espacialmente
- Notificaciones push reales (cambios de horario, recordatorios)
- Compartir una actividad o el itinerario de favoritos por WhatsApp/redes
- Modo oscuro / claro
- Detectar automáticamente el idioma del teléfono al abrir la app
- Botón "agregar a mi calendario" en cada favorito
- Contador de cuenta atrás para el inicio del festival
- Sección de equipo/jurado (Prix des Biarrots) con fotos y bios
- Encuesta rápida de satisfacción al final del festival

## Cómo publicar cambios
Sube los archivos modificados a GitHub (botón "Add file" → "Upload files", reemplaza lo que ya existe). Vercel vuelve a publicar la app sola en 30-60 segundos.
