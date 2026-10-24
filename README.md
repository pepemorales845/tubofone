# Tubófone

Sitio estático para https://tubofone.srv2031686.hstgr.cloud

Copiar al docroot de nginx (igual que atelier / landings):

- index.html
- favicon.svg
- assets/routes-C1d2tNUk.js
- assets/styles-Dg6wH5VB.css
- assets/index-VSW1y7za.js

`assets/index-VSW1y7za.js` pesa 431963 bytes.
sha256: e3ffc490e24c989fca724b4534b675722e7e2a6afe30f30dc7e826f4201f0031

El mismo JS está partido en `js-parts/` (195 trozos de ~3 KB, base64) por si un conector no acepta el archivo de 432 KB. No hace falta usarlo si el `.js` de assets está.

Para reconstruir desde los trozos (cada grupo pXX se descodifica aparte; no juntes todo el base64 de golpe):

```
mkdir -p assets
for g in p00 p01 p02 p03 p04 p05 p06 p07 p08 p09 p10 p11 p12 p13 p14 p15 p16 p17 p18 p19 p20 p21; do
  cat js-parts/${g}-s*.b64 | tr -d '\n' | base64 -d
done > assets/index-VSW1y7za.js
```

El resultado tiene que medir 431963 bytes y el sha256 de arriba.

El título visible es Tubófone. No publiques hasta que esas cinco URLs respondan 200:

- https://tubofone.srv2031686.hstgr.cloud/
- https://tubofone.srv2031686.hstgr.cloud/favicon.svg
- https://tubofone.srv2031686.hstgr.cloud/assets/index-VSW1y7za.js
- https://tubofone.srv2031686.hstgr.cloud/assets/routes-C1d2tNUk.js
- https://tubofone.srv2031686.hstgr.cloud/assets/styles-Dg6wH5VB.css
