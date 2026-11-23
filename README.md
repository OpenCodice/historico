# Histórico de las leyes mexicanas

El texto de cada ley después de cada una de sus reformas, desde 2006, un
archivo por artículo. Cada ley está en su propia rama y cada versión es un
commit, fechado el día de su publicación en el Diario Oficial de la Federación.

<!-- ramas -->
| Rama | Ley | Versiones | Periodo |
|---|---|---|---|
| [`cpeum`](../../tree/cpeum) | Constitución Política de los Estados Unidos Mexicanos | 75 | 2006-04-07 a 2026-10-07 |
| [`ccf`](../../tree/ccf) | Código Civil Federal | 14 | 2004-12-31 a 2025-11-14 |
| [`ccom`](../../tree/ccom) | Código de Comercio | 3 | 2018-03-28 a 2025-11-14 |
| [`cff`](../../tree/cff) | Código Fiscal de la Federación | 24 | 2006-07-18 a 2026-04-09 |
| [`cjm`](../../tree/cjm) | Código de Justicia Militar | 7 | 2005-06-29 a 2025-07-16 |
| [`lft`](../../tree/lft) | Ley Federal del Trabajo | 24 | 2006-01-17 a 2026-05-14 |
| [`lisr`](../../tree/lisr) | Ley del Impuesto sobre la Renta | 8 | 2013-12-11 a 2024-04-01 |
<!-- /ramas -->

```
git clone https://github.com/OpenCodice/historico && cd historico
git log origin/lft                        # las versiones de la LFT
git diff origin/lft~1 origin/lft          # qué cambió la última reforma
git log -p origin/cpeum -- cpeum/004.md   # la historia del artículo 4o. constitucional
```

## De dónde sale

La Cámara de Diputados publica cada ley en una sola dirección, que se
sobrescribe con cada reforma. Las versiones anteriores se recuperan de las
capturas de Wayback Machine de ese PDF, y cada commit dice de cuál salió
(`Fuente`), con su sha256. El texto lo extrae
[historico-extractor](https://github.com/OpenCodice/historico-extractor) con
los mismos extractores que mantienen el texto vigente; nada se edita a mano.

## Qué no es

- **No están todas las versiones.** Solo las que Wayback capturó (de la CPEUM,
  75 de las 103 fechas de reforma desde 2006; de la LFT, 24 de 29), y de ellas,
  las que pasan las compuertas. Un commit puede reunir más de una reforma.
- **No están todas las leyes.** Las ramas se van sumando por tandas; una ley
  cuya cadena no queda limpia no se publica.
- **No es el texto vigente.** Ese está en
  [constitucion-mexicana](https://github.com/OpenCodice/constitucion-mexicana) y
  [leyes-federales](https://github.com/OpenCodice/leyes-federales), y se
  mantiene al día cada semana.
- **Los hashes de una rama pueden cambiar.** Una rama se regenera cuando mejora
  un extractor o aparece una captura nueva. Para citar una versión, usa la rama
  y la fecha (`Publicacion`), no el hash.

Las notas de reforma al pie de cada artículo (en cursiva) son de la Cámara, y
las fue agregando y reescribiendo con los años: un artículo puede cambiar de
una versión a otra solo en sus notas.

Parte de [OpenCodice](https://github.com/OpenCodice). El texto legal es de
dominio público.
