# Festival BAL — App de programación

## Qué es esto
Una mini-app web (PWA) con la programación del festival, favoritos, stands y enlaces (redes, playlist, tickets BilletWeb).

## Archivos
- index.html → toda la app (estructura, estilos y lógica)
- manifest.json → permite "instalar" la app en el celular
- sw.js → hace que funcione offline una vez cargada
- icons/ → íconos provisionales (cambiar cuando tengamos el logo oficial)

## Cómo editar la programación
Abre index.html, busca la sección `const events = [...]` y agrega/edita actividades siguiendo el mismo formato. Lo mismo para `const stands = [...]`.

## Cómo publicarlo (sin terminal, sin código)
1. Crea un repositorio en GitHub (gratis) y sube esta carpeta completa arrastrando los archivos desde el navegador.
2. En Vercel, "Add New Project" → "Import" → selecciona ese repositorio de GitHub.
3. Deja la configuración por default (no es un framework, es estático) y dale "Deploy".
4. Vercel te da una URL tipo bal-app.vercel.app — ábrela en tu celular y verás la opción de "añadir a pantalla de inicio".
