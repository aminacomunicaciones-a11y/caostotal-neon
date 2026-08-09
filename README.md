# Caos Total: Neon — web pública

Página pública del juego **Caos Total: Neon** (Amina). Es la URL que va en
el campo **«Sitio web»** de la ficha de Google Play.

> **Nombre del estudio:** el nombre público es **«Amina»**, a secas. En la web no queda
> ni un «Amina Estudio». Ojo: el logo entregado (`Assets/Resources/Marca/AminaEstudio.png`)
> *dibuja* «AMINA ESTUDIO», así que el pie usa un rótulo de texto en vez del PNG. Cuando
> haya un logo redibujado solo con «AMINA», vuelve a ponerse como imagen.

> **Nada de promesas falsas.** La web **no** puede decir «sin compras», «sin registro»,
> «sin recopilar datos» ni «sin conexión»: el juego lleva compras dentro de la app
> (packs de Astros, con Unity Purchasing) y va a tener cuentas con recopilación de datos.
> Sí es cierto y sí se dice: descarga gratis y sin anuncios (no hay ningún SDK de
> publicidad en el proyecto).

**En vivo:** https://aminacomunicaciones-a11y.github.io/caostotal-neon/

## Qué hay aquí

| Fichero | Para qué |
|---|---|
| `index.html` | La página entera: HTML + CSS en un solo archivo, sin dependencias externas |
| `img/` | Capturas, icono, gráfico destacado y logo del estudio, ya optimizados para web |
| `robots.txt`, `sitemap.xml` | Para que Google la encuentre e indexe |

No hay scripts, ni fuentes externas, ni CDN, ni analítica: la página no hace ni una
sola petición fuera de este dominio. Igual que la [página legal](https://github.com/aminacomunicaciones-a11y/caostotal-legal).

## Cambio pendiente: cuando el juego salga en abierto

Ahora mismo los botones de descarga apuntan al alta de la **prueba cerrada**
(`play.google.com/apps/testing/...`), porque la ficha pública todavía responde 404.

Cuando el juego se publique, busca en `index.html` los dos `href` de
`apps/testing` y cámbialos por:

```
https://play.google.com/store/apps/details?id=com.caostotalgames.caostotal
```

Y ajusta el texto del sello («Prueba cerrada abierta en Google Play») y de la
sección de cierre.

## Pendiente: dominio propio (NO comprado)

Faussi valoró un dominio tipo `caostotalneon.com`. **No se ha comprado nada** — queda
como decisión suya, porque implica un gasto recurrente y todavía no está dado de alta
como autónomo.

Coste orientativo: **10–15 €/año** el `.com` en un registrador estándar
(Namecheap, Porkbun, Cloudflare Registrar), con privacidad de WHOIS incluida. Los
`.com` suelen tener el primer año más barato y renovar algo más caro; conviene mirar
el precio de **renovación**, no el de alta.

Si algún día se compra, GitHub Pages lo admite gratis: se añade un fichero `CNAME`
con el dominio, se apuntan los DNS a GitHub y la web sigue siendo la misma. La URL
actual de `github.io` seguiría funcionando como redirección.

## Publicar un cambio

GitHub Pages sirve la rama `main`. Cualquier `git push` a `main` republica la web
en un minuto o dos.

```bash
git add -A
git commit -m "Actualiza la web"
git push
```

## Las imágenes

La web lleva **exactamente 4 imágenes**, las que entregó Faussi el 2026-08-10
(5,8 MB de PNG → 212 KB de WebP):

| Fichero | Qué es | Dónde sale |
|---|---|---|
| `banner.webp` | Banner con el rótulo del juego y el pulpo mascota | La portada |
| `captura-combate.webp` | Combate contra la oleada, «la guerra neón ha llegado» | Galería |
| `captura-sombra.webp` | Selección de personaje: Sombra | Galería |
| `captura-luz.webp` | Ficha del esbirro Luz | Galería |

`og-caos-total-neon.jpg` se genera a partir del banner y solo se usa al compartir el
enlace. `icono.png` y `favicon.png` no se ven en la página: son el icono de la pestaña
y el de la pantalla de inicio.

Como el banner ya dibuja el nombre del juego, el `<h1>` va con la clase
`.oculto-visual`: sigue estando para Google y los lectores de pantalla, pero no se
repite en pantalla. **Si algún día se quita el banner, hay que volver a hacer visible
ese `<h1>`.**

Para añadir capturas nuevas: WebP calidad 82, 600 px de ancho las verticales y unos
700 px las más apaisadas. No se recortan: las pantallas de menú llevan texto de
interfaz y recortarlas se come información.
