# Tubófone

Sitio estático del juego para https://tubofone.srv2031686.hstgr.cloud

El JavaScript principal está partido en `js-parts/part-00.txt` ... `js-parts/part-26.txt`. En el VPS, antes de copiar al docroot:

```
mkdir -p assets
cat js-parts/part-00.txt js-parts/part-01.txt js-parts/part-02.txt js-parts/part-03.txt js-parts/part-04.txt js-parts/part-05.txt js-parts/part-06.txt js-parts/part-07.txt js-parts/part-08.txt js-parts/part-09.txt js-parts/part-10.txt js-parts/part-11.txt js-parts/part-12.txt js-parts/part-13.txt js-parts/part-14.txt js-parts/part-15.txt js-parts/part-16.txt js-parts/part-17.txt js-parts/part-18.txt js-parts/part-19.txt js-parts/part-20.txt js-parts/part-21.txt js-parts/part-22.txt js-parts/part-23.txt js-parts/part-24.txt js-parts/part-25.txt js-parts/part-26.txt > assets/index-VSW1y7za.js
```

El archivo juntado tiene que pesar 431963 bytes. Si no, no lo publiques.

Luego copia al docroot nginx, igual que atelier o landings, con `index.html` en la raíz:

- index.html
- favicon.svg
- assets/index-VSW1y7za.js
- assets/routes-C1d2tNUk.js
- assets/styles-Dg6wH5VB.css

Tiene que responder 200 por HTTPS:

- https://tubofone.srv2031686.hstgr.cloud/
- https://tubofone.srv2031686.hstgr.cloud/assets/index-VSW1y7za.js
- https://tubofone.srv2031686.hstgr.cloud/assets/routes-C1d2tNUk.js
- https://tubofone.srv2031686.hstgr.cloud/assets/styles-Dg6wH5VB.css

El título visible es Tubófone.
