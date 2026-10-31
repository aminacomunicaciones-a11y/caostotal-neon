# Caos Total Neon — web pública

Página pública del juego **Caos Total Neon**, de **Aminan**. Es la URL que va en
el campo **«Sitio web»** de la ficha de Google Play.

> **Nombre de la marca: «Aminan».** A secas, y con **N al final**. Confirmado por
> Faussi el 2026-08-18. Todas estas variantes son **incorrectas** y no deben volver a
> aparecer: *Amin&#97;*, *Amin&#97;n Juegos*, *Amin&#97; Juegos*, *Amin&#97; Estudio*.
> El nombre va en el `<title>`, en las meta, en el Open Graph, en los datos
> estructurados, en la portada y en el pie.
>
> ⚠️ **Una cadena lleva la grafía vieja y NO se puede tocar**, porque es una
> dirección real y romperla rompe la web: el dominio
> `aminacomunicaciones-a11y.github.io`.
>
> El buzón de contacto es **`aminansoporte@gmail.com`** desde el 6-sep-2026, el mismo
> que usan las páginas legales y la ficha de Play. El viejo `amina.comunicaciones@…`
> ya no aparece en la web.
>
> Regla al escribir el pie: **la palabra «estudio» no puede aparecer en pantalla**
> (Faussi no es un estudio). La frase de debajo se lee pegada al rótulo, así que
> conviene releerlas juntas antes de cambiar cualquiera de las dos.
>
> El logo redibujado llegó el 2026-08-20: `img/logo-aminan.png` (copia de
> `Assets/Resources/Marca/AminanEstudio.png` del proyecto de Unity) ya pone «AMINAN»
> bien escrito, y el pie lo usa como imagen. El rótulo de texto que había antes ya no está.

> **Nada de promesas falsas.** La web **no** puede decir «sin compras», «sin registro»,
> «sin recopilar datos», «sin conexión» **ni «sin anuncios»**: el juego lleva compras
> dentro de la app (packs de Astros, con Unity Purchasing), cuentas con recopilación de
> datos y, desde el 29-ago-2026, anuncios de Google AdMob (intersticial al final de la
> partida y vídeo voluntario para doblar la Esencia). Sí es cierto y sí se dice:
> descarga gratis. El apartado «Claro desde el principio» que hablaba de todo esto lo
> retiró Faussi entero el 6-sep-2026.

> **La historia** (sección `#historia`, abajo del todo, 6-sep-2026): un mundo de
> magos arrasado por una invasión alienígena, y los magos que se vengan atacando los
> mundos de los aliens mundo a mundo. Está redactada por Claude sobre la sinopsis de
> Faussi; si el juego cambia el trasfondo, este texto va detrás.

**En vivo:** https://aminacomunicaciones-a11y.github.io/caostotal-neon/

## Qué hay aquí

| Fichero | Para qué |
|---|---|
| `index.html` | La página entera: HTML + CSS en un solo archivo, sin dependencias externas |
| `img/` | Capturas, icono del juego (pestaña), gráfico destacado y logo de la marca, ya optimizados para web |
| `robots.txt`, `sitemap.xml` | Para que Google la encuentre e indexe |

No hay scripts, ni fuentes externas, ni CDN, ni analítica: la página no hace ni una
sola petición fuera de este dominio. Igual que la [página legal](https://github.com/aminacomunicaciones-a11y/caostotal-legal).

## El juego ya está en Google Play (10-sep-2026)

Salió en abierto el 10-sep-2026. En la tienda se llama **«Caos Total Neon: Supervivencia»**.
Los avisos de que el juego aún no había salido se quitaron; los dos botones «Descargar en Google Play»
(portada y sección de cierre) y el JSON-LD (`installUrl`, `sameAs`, `offers.url`, con
`availability` `InStock`) apuntan a la ficha pública:

```
https://play.google.com/store/apps/details?id=com.caostotalgames.caostotal
```

El icono del botón es un triángulo de «play» genérico, **no** el logotipo de Google Play.

## SEO: el nombre y las seis palabras

El nombre es **«Caos Total Neon»**, sin dos puntos entre «Total» y «Neon». Esa grafía
vieja se retiró y el 10-sep-2026 Google todavía tenía guardado el título antiguo: no
puede volver a aparecer en ningún sitio de la web (título, meta, Open Graph, JSON-LD,
textos, comentarios). La única forma con dos puntos que vale es el nombre de la tienda,
«Caos Total Neon: Supervivencia».

El `<title>` (31-oct-2026) empieza por el nombre exacto y sigue con el de la tienda:
«Caos Total Neon: Supervivencia — juego gratis para Android | Aminan». La meta `description` lleva las seis:
**Caos Total Neon, supervivencia, oleadas, roguelike, magos, Android**. Si se
reescriben, que no se caiga ninguna.

Páginas del dominio a 10-sep-2026: la portada (`/`), esta web (`/caostotal-neon/`, una
sola página) y las legales (`/caostotal-legal/`: `index`, `privacidad`, `condiciones`,
`borrar-datos`). Los dos sitemaps (`/sitemap.xml` y `/caostotal-neon/sitemap.xml`)
recogen la portada y esta web; las legales no están en ninguno.

## Google Search Console

Propiedad de **prefijo de URL**: `https://aminacomunicaciones-a11y.github.io/caostotal-neon/`.
Valen los dos métodos, porque GitHub Pages sirve la raíz de `main` tal cual:

- **Etiqueta HTML (el que se usa):** la `<meta name="google-site-verification">` va en el
  `<head>` de `index.html`, justo debajo del `viewport`. El token es de la **cuenta** de
  Google, no de la propiedad: si Search Console enseña el mismo `content`, ya está puesto.
  Si enseña otro (otra cuenta), se **añade** una segunda línea debajo; la vieja no se borra.
- **Fichero HTML:** el `googleXXXX.html` que da Google se deja en la **raíz de este repo**
  (junto a `index.html`) y queda en `…/caostotal-neon/googleXXXX.html`. Jekyll lo copia
  tal cual porque no lleva cabecera YAML.

Una vez verificada: enviar el sitemap `https://aminacomunicaciones-a11y.github.io/caostotal-neon/sitemap.xml`
y pedir indexación de la portada en «Inspección de URL».

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

La web lleva **exactamente 5 imágenes**: las 4 que entregó Faussi el 2026-08-10
(5,8 MB de PNG → 212 KB de WebP) más el logotipo AMINAN del 2026-08-20:

| Fichero | Qué es | Dónde sale |
|---|---|---|
| `banner.webp` | Banner con el rótulo del juego y el pulpo mascota | La portada |
| `captura-menu.webp` | Menú principal, mapa 1 Bosque de Silicio | Galería |
| `captura-jefe-laseres.webp` | Jefe bajo fuego cruzado, arena roja | Galería |
| `captura-jefe-enjambre.webp` | Jefa medusa rodeada de esbirros | Galería |
| `logo-aminan.png` | El logotipo AMINAN de neón (el mismo del juego) | El pie |

> ⚠️ **Ninguna imagen puede llevar la marca de agua de Gemini.** Las tres capturas de
> la galería se cambiaron el 2026-08-10 justo por eso: dos de las anteriores traían el
> icono de IA en una esquina. Antes de subir una imagen nueva, mírale las cuatro
> esquinas ampliadas. El banner está comprobado y limpio.

`og-caos-total-neon.jpg` se genera a partir del banner y solo se usa al compartir el
enlace. `favicon.ico`, `icon-16/32/48/96/192/512.png` y `apple-touch-icon.png` son el
**icono del juego** (el bicho azul de `Assets/CharacterArt/icono_wikivampiro.png`, el
mismo que sale en el móvil), recortado del marco negro y con esquinas redondeadas.
Desde el 6-sep-2026 sustituyen a la A de Aminan en la pestaña, y `icon-192.png` se
ve también en la sección de la historia.

> ⚠️ **El icono que Google pinta en los resultados NO sale de aquí.** Google solo
> admite un favicon por dominio y lo lee de la portada raíz
> (`aminacomunicaciones-a11y.github.io/favicon.ico`, repo `amina-raiz`). Por eso el
> mismo juego de iconos está también allí. Si se cambia el icono, hay que cambiarlo
> en los dos repos.

El `<h1>` va visible debajo del banner desde el 31-oct-2026, aunque el banner ya dibuje
el nombre: es la señal más clara para Google de cómo se llama la página.

Las cifras de la web (8 magos, 18 armas, 18 fusiones, 6 mapas y 6 jefes) salen de
`NeonCharacterCatalog`, `GameManager.NeonKit`, `GameManager.NeonFusions` y `MapCatalog`
del juego (rama `horno`), a 31-oct-2026. Si el juego cambia, estas van detrás.

Para añadir capturas nuevas: WebP calidad 82, 600 px de ancho las verticales y unos
700 px las más apaisadas. No se recortan: las pantallas de menú llevan texto de
interfaz y recortarlas se come información.
