# Tubófone

Sitio estático del juego para https://tubofone.srv2031686.hstgr.cloud

El JavaScript principal va partido en `js-parts/` porque no cabía en un solo archivo. En el VPS, antes de copiar al docroot, júntalo:

```
mkdir -p assets
cat js-parts/part-00.txt js-parts/part-01.txt js-parts/part-02.txt js-parts/part-03.txt js-parts/part-04.txt js-parts/part-05.txt js-parts/part-06.txt js-parts/part-07.txt js-parts/part-08.txt > assets/index-VSW1y7za.js
```

Luego copia al docroot nginx, de la misma forma que atelier o landings, con `index.html` en la raíz:

- index.html
- favicon.svg
- assets/index-VSW1y7za.js (el archivo juntado, no las partes)
- assets/routes-C1d2tNUk.js
- assets/styles-Dg6wH5VB.css

Tiene que responder 200 por HTTPS:

- https://tubofone.srv2031686.hstgr.cloud/
- https://tubofone.srv2031686.hstgr.cloud/assets/index-VSW1y7za.js
- https://tubofone.srv2031686.hstgr.cloud/assets/routes-C1d2tNUk.js
- https://tubofone.srv2031686.hstgr.cloud/assets/styles-Dg6wH5VB.css

El título visible es Tubófone.
