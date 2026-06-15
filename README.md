# Mapa interactivo de Italia por regiones

Este paquete contiene un mapa interactivo de Italia preparado para integrarse en una página web o en un proyecto eTwinning/TwinSpace mediante `iframe`.

## Archivos principales

- `index.html`: mapa interactivo completo.
- `recursos/`: carpeta con los PDF, PPTX y ODP asociados a las regiones.
- `insertar-en-etwinning.html`: ejemplo de código `iframe` para insertar el mapa en eTwinning/TwinSpace.

## Regiones incluidas

- Calabria — `recursos/calabria.pptx`
- Emilia Romagna — `recursos/emilia-romagna.pdf`
- L’Abruzzo — `recursos/abruzzo.pdf`
- La Basilicata — pendiente de archivo
- La Puglia — `recursos/puglia.odp`
- Campania — `recursos/campania.pptx`
- Lazio — `recursos/lazio.pptx`
- Molise — `recursos/molise.pptx`
- Liguria — `recursos/liguria.pdf`
- Lombardia — `recursos/lombardia.pdf`
- Marche — `recursos/marche.pptx`
- Piemonte — `recursos/piemonte.pptx`
- Sicilia — `recursos/sicilia.pdf`
- Toscana — `recursos/toscana.pptx`
- Trentino — `recursos/trentino.pdf`
- Veneto — `recursos/veneto.pptx`

## Funcionamiento

1. El usuario pulsa una región coloreada del mapa o la selecciona en el desplegable.
2. El panel lateral muestra los recursos asociados.
3. El botón de italiano abre el archivo recibido para esa región.
4. Los botones de español e inglés aparecen como pendientes porque no se han recibido recursos en esos idiomas.

## Publicación recomendada para eTwinning

1. Publica el contenido completo de esta carpeta en una URL pública HTTPS, por ejemplo GitHub Pages, Netlify o la web del centro.
2. Abre `insertar-en-etwinning.html`.
3. Sustituye `https://TU-USUARIO.github.io/TU-REPOSITORIO/` por la URL real del mapa.
4. Inserta ese `iframe` en la página del proyecto eTwinning/TwinSpace.

## Nota técnica

El mapa carga la geometría de las regiones italianas desde el repositorio público `openpolis/geojson-italy`, archivo `limits_IT_regions.geojson`. Si la plataforma en la que se inserta bloquea GitHub, el selector de regiones seguirá funcionando, pero el mapa no podrá dibujarse. Para una versión completamente autónoma se puede incrustar el GeoJSON dentro del propio `index.html`.
