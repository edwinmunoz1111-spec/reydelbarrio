# Página de puntos de venta · Torneo del Rey del Barrio

Archivos de esta carpeta (súbelos todos, sin carpetas intermedias):

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La página. Fuentes e íconos van dentro del archivo: no depende de servicios externos. |
| `logos-rey-del-barrio.jpg` | Franja de logos del encabezado (recortada de la pieza oficial). |
| `pieza-rey-del-barrio.jpg` | Pieza oficial completa, visible y descargable en la página. |
| `og-rey-del-barrio.jpg` | Imagen 1200×630 que WhatsApp muestra como vista previa del enlace. |

## Publicar gratis en GitHub Pages (10 minutos, desde el navegador)

1. Entra a github.com e inicia sesión (la cuenta gratuita sirve).
2. Botón **New repository** → nombre: `reydelbarrio` → marca **Public** → **Create repository**.
3. En el repositorio vacío: **uploading an existing file** → arrastra los 4 archivos → **Commit changes**.
4. **Settings → Pages** → en *Build and deployment*, Source: **Deploy from a branch** → Branch: **main** y carpeta **/(root)** → **Save**.
5. Espera 1 a 3 minutos. Tu dirección queda así: `https://TU-USUARIO.github.io/reydelbarrio/`
6. Abre `index.html` en GitHub → ícono del lápiz → reemplaza `TU-USUARIO` por tu usuario real en las 3 líneas marcadas como VISTA PREVIA → **Commit changes**. Sin esto, WhatsApp no muestra la imagen de vista previa.
7. Prueba: envíate el enlace por WhatsApp. Debe aparecer la tarjeta con la imagen y el título.

## Enlaces por canal (para saber de dónde llegan los jugadores)

Agrega al final de la dirección el canal. El mensaje que el jugador le manda a la tienda termina con un código distinto según el canal:

| Canal | Enlace | Código que ve la tienda |
|---|---|---|
| WhatsApp (difusión) | `https://TU-USUARIO.github.io/reydelbarrio/?o=wa` | RDB-WA |
| SMS | `https://TU-USUARIO.github.io/reydelbarrio/?o=sms` | RDB-SMS |
| Reenvío desde grupos (botón Compartir) | se agrega solo `?o=grupo` | RDB-GR |
| Sin parámetro | `https://TU-USUARIO.github.io/reydelbarrio/` | RDB-WEB |

Para el SMS, acorta el enlace `?o=sms` en tinyurl.com (gratis, con alias personalizado, por ejemplo `LlantasReyDelBarrio`). Si el alias está ocupado, prueba otro y actualiza la plantilla de SMS.

Para quitar el código del mensaje: en `index.html` busca `USAR_CODIGO = true` y cámbialo por `false`.

## Mantenimiento

- **Agregar una tienda:** copia un bloque `<article class="tienda">…</article>`, cambia nombre, contacto, número (formato 57 + celular) y enlace de mapa. Si es una localidad nueva, agrega también su botón en la fila de filtros (`data-zona`).
- **Retirar una tienda:** borra su bloque `<article>`.
- **Cambiar fechas:** busca `FIN` y `SORTEO` en el script final.
- Cada cambio se publica solo en 1 a 3 minutos.
