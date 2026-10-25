# Tortillería POS - canal de actualizaciones

Este repositorio público contiene solo los paquetes de actualización del POS. El código fuente se mantiene en otro repositorio.

La aplicación consulta el manifiesto aquí:

https://raw.githubusercontent.com/daniel21dev/pos-updates/main/update-manifest.json

No agregues bases SQLite, respaldos, sesiones de WhatsApp ni datos de clientes.

## Publicar una versión

1. Genera la entrega desde el proyecto fuente con `npm run release:windows:zip`.
2. En GitHub, crea un Release con una etiqueta como `v0.2.1`.
3. Adjunta el ZIP como `tortilleria-pos.zip` y publica el Release.
4. Publica el archivo `dist/update-manifest.json` en la rama `main` de este repositorio. Se actualizan la versión y las notas, mientras la URL del ZIP permanece estable.
5. Publica primero el Release y después el manifiesto para no anunciar una descarga que aún no existe.

El manifiesto incluye la plataforma, la arquitectura, la URL directa, el SHA-256 y una firma Ed25519. La clave privada de publicación debe mantenerse fuera de este repositorio.
