# Volahoy

Landing de **Volahoy** — vuelos privados y vuelos de bautismo en la provincia de Córdoba, Argentina.
Sitio estático, sin build. La consulta termina en WhatsApp; no hay pagos ni reservas automáticas.

## Estructura

```
index.html      la landing completa (HTML + CSS + JS inline)
assets/         las 5 fotos (hero, card vuelo privado, card bautismo, experiencia, cierre)
vercel.json     cleanUrls + cache inmutable para /assets
robots.txt      / sitemap.xml
```

## Editar

**Número de WhatsApp** — una sola línea al inicio del `<script>` en `index.html`:

```js
var WA_NUMBER = "5493385593545";
```

**Precio** — aparece en tres lugares: la píldora del hero, la primera pregunta del FAQ y el
bloque JSON-LD del `<head>` (dos `Offer`, `price: "50"`).

**Fotos** — reemplazá los archivos de `assets/` manteniendo el nombre y la proporción
(16:9 para hero/experiencia/cierre, 3:4 para las dos cards). Si cambiás las dimensiones,
actualizá los atributos `width`/`height` del `<img>` correspondiente.

## Deploy

Push a `main`; Vercel publica solo.

```bash
git add -A && git commit -m "..." && git push
```

## Ver en local

```bash
python3 -m http.server 4000
```
