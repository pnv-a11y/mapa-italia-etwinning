# Mapa interactivo de España con visor interno

Este paquete contiene una versión del mapa interactivo de España preparada para integrarse en una página web o en eTwinning/TwinSpace mediante `iframe`.

## Archivos incluidos

- `index.html`: mapa interactivo de España por comunidades autónomas.
- `insertar-en-etwinning.html`: fragmento `iframe` para incrustar el mapa cuando esté publicado en una URL HTTPS.
- `recursos/pendiente.html`: pantalla provisional que se muestra cuando todavía no hay recurso definitivo.

## Funcionamiento

1. El usuario selecciona una comunidad autónoma en el mapa o desde el desplegable.
2. El panel lateral muestra tres botones: español, italiano e inglés.
3. Al pulsar un botón se abre una ventana interna dentro del propio mapa.
4. Como aún no hay recursos definitivos, se muestra una página provisional de “recurso pendiente”.

## Cómo añadir recursos reales

Se recomienda convertir las presentaciones a PDF antes de subirlas, porque los navegadores muestran los PDF dentro del visor con más estabilidad que los archivos `.pptx` u `.odp`.

Ejemplo: para Andalucía puede crear esta estructura:

```text
recursos/
└── andalucia/
    ├── es.pdf
    ├── it.pdf
    └── en.pdf
```

Después, en `index.html`, busque el bloque `resourcesByCommunity` y cambie:

```js
es: { url: "./recursos/pendiente.html", type: "Pendiente", available: false }
```

por:

```js
es: { url: "./recursos/andalucia/es.pdf", type: "PDF", available: true }
```

Haga lo mismo para italiano e inglés cuando existan recursos.

## Publicación en GitHub Pages

1. Descomprima el ZIP.
2. Suba a GitHub el contenido descomprimido, no el ZIP.
3. Active GitHub Pages desde `Settings > Pages`.
4. Use la URL pública generada en el archivo `insertar-en-etwinning.html`.

## Nota técnica

El mapa carga la geometría de comunidades autónomas desde un GeoJSON público. Si se desea una versión completamente autónoma, puede descargarse el GeoJSON y cambiar la variable `geojsonUrl` en `index.html` por una ruta local.


## Versión corregida

Esta versión mantiene Canarias en un recuadro inferior independiente. La proyección principal reserva una franja específica para el archipiélago, por lo que Canarias no se superpone con Andalucía ni con ninguna otra comunidad autónoma.

El mapa conserva el visor interno para recursos PDF. Mientras no existan recursos definitivos, los botones muestran una pantalla provisional. Cuando se incorporen los materiales, se recomienda guardarlos en `recursos/<comunidad>/<idioma>.pdf` y actualizar las rutas en `index.html`.
