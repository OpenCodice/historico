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
| [`cmpp`](../../tree/cmpp) | Código Militar de Procedimientos Penales | 4 | 2018-06-21 a 2025-11-14 |
| [`cnpp`](../../tree/cnpp) | Código Nacional de Procedimientos Penales | 8 | 2014-03-05 a 2025-11-28 |
| [`laam`](../../tree/laam) | Ley de Ascensos de la Armada de México | 3 | 2004-06-25 a 2025-12-17 |
| [`laassp`](../../tree/laassp) | Ley de Adquisiciones, Arrendamientos y Servicios del Sector Público | 1 | 2025-04-16 a 2025-04-16 |
| [`laat`](../../tree/laat) | Ley de Ayuda Alimentaria para los Trabajadores | 1 | 2011-01-17 a 2011-01-17 |
| [`lac`](../../tree/lac) | Ley de Aviación Civil | 9 | 2006-07-05 a 2025-11-14 |
| [`laem`](../../tree/laem) | Ley que crea la Agencia Espacial Mexicana | 1 | 2010-07-30 a 2010-07-30 |
| [`laero`](../../tree/laero) | Ley de Aeropuertos | 8 | 2006-07-05 a 2025-11-14 |
| [`lagra`](../../tree/lagra) | Ley Agraria | 12 | 1993-07-09 a 2025-11-14 |
| [`lamn`](../../tree/lamn) | Ley de Amnistía | 2 | 2020-04-22 a 2024-06-14 |
| [`lamni`](../../tree/lamni) | Ley de Amnistía | 1 | 1994-01-22 a 1994-01-22 |
| [`lamp`](../../tree/lamp) | Ley de Amparo, Reglamentaria de los artículos 103 y 107 de la Constitución Política de los Estados Unidos Mexicanos | 10 | 2013-04-02 a 2025-10-16 |
| [`lan`](../../tree/lan) | Ley de Aguas Nacionales | 11 | 2004-04-29 a 2025-12-11 |
| [`lansi`](../../tree/lansi) | Ley de la Agencia Nacional de Seguridad Industrial y de Protección al Medio Ambiente del Sector Hidrocarburos | 3 | 2014-08-11 a 2022-05-11 |
| [`lapp`](../../tree/lapp) | Ley de Asociaciones Público Privadas | 6 | 2012-01-16 a 2025-11-14 |
| [`larcp`](../../tree/larcp) | Ley de Asociaciones Religiosas y Culto Público | 5 | 2006-04-24 a 2025-11-14 |
| [`larefam`](../../tree/larefam) | Ley de Ascensos y Recompensas del Ejército, Fuerza Aérea y Guardia Nacional | 1 | 2025-07-16 a 2025-07-16 |
| [`lasoc`](../../tree/lasoc) | Ley de Asistencia Social | 10 | 2004-09-02 a 2024-04-01 |
| [`latime`](../../tree/latime) | Ley Sobre la Aprobación de Tratados Internacionales en Materia Económica | 1 | 2004-09-02 a 2004-09-02 |
| [`lbio`](../../tree/lbio) | Ley de Biocombustibles | 1 | 2025-03-18 a 2025-03-18 |
| [`lbm`](../../tree/lbm) | Ley del Banco de México | 4 | 2000-12-31 a 2014-01-10 |
| [`lbogm`](../../tree/lbogm) | Ley de Bioseguridad de Organismos Genéticamente Modificados | 3 | 2005-03-18 a 2022-05-11 |
| [`lcacsam`](../../tree/lcacsam) | Ley para la Comprobación, Ajuste y Cómputo de Servicios de la Armada de México | 2 | 2004-06-14 a 2009-06-12 |
| [`lcacsefam`](../../tree/lcacsefam) | Ley para la Comprobación, Ajuste y Cómputo de Servicios en el Ejército y Fuerza Aérea Mexicanos | 3 | 2006-02-09 a 2024-05-03 |
| [`lce`](../../tree/lce) | Ley de Comercio Exterior | 3 | 2006-01-24 a 2026-05-01 |
| [`lcec`](../../tree/lcec) | Ley de Cámaras Empresariales y sus Confederaciones | 1 | 2019-04-12 a 2019-04-12 |
| [`lcid`](../../tree/lcid) | Ley de Cooperación Internacional para el Desarrollo | 1 | 2020-11-06 a 2020-11-06 |
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
