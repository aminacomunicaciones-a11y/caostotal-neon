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

Salen del proyecto de Unity (`Preview/StoreShots`, `Preview/Ficha`,
`Assets/Resources/Marca`) y se reducen a WebP con el guion que las generó
(11,8 MB → 286 KB). Si se cambian las capturas de la ficha, conviene volver a
pasarlas por el mismo redimensionado (540 px de ancho, WebP calidad 80).
