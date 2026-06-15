# Mapa interactivo de Italia por regiones - versión con visor interno

Este paquete contiene un mapa interactivo de Italia por regiones, preparado para publicación web y para su inserción en eTwinning/TwinSpace mediante `iframe`.

## Cambios principales de esta versión

- Los recursos ya no se enlazan como archivos descargables directos.
- Al pulsar el botón de idioma, el recurso se abre en una ventana interna superpuesta dentro de la propia página.
- Todos los recursos se han normalizado a PDF para facilitar su visualización en navegador.
- Las presentaciones PPTX y ODP recibidas se han convertido a PDF.
- El usuario puede cerrar el visor con el botón `Cerrar`, haciendo clic fuera de la ventana o pulsando la tecla `Esc`.
- Se mantiene la selección accesible por mapa, desplegable, teclado y panel lateral.

## Archivos incluidos

- `index.html`: mapa interactivo completo.
- `recursos/`: PDFs asociados a cada región.
- `insertar-en-etwinning.html`: fragmento de `iframe` para insertar el mapa en eTwinning/TwinSpace.
- `README.md`: este documento.

## Funcionamiento

1. El usuario selecciona una región en el mapa o en el desplegable.
2. El panel lateral muestra los recursos disponibles.
3. Al pulsar el botón de italiano, el PDF se abre dentro de una ventana interna.
4. El recurso no se abre como descarga directa.

## Importante sobre la descarga de archivos

Esta versión evita el enlace directo de descarga y presenta los documentos en un visor interno. No obstante, en cualquier sitio web público, si un archivo PDF está alojado en una URL accesible, un usuario técnicamente avanzado podría llegar a guardarlo desde el navegador o desde las herramientas del sistema. La solución implementada está orientada a evitar la descarga accidental y a mejorar la experiencia de uso en eTwinning, no a establecer una protección DRM.

## Publicación recomendada

1. Subir todos los archivos descomprimidos a un repositorio público de GitHub.
2. Activar GitHub Pages desde `Settings > Pages`.
3. Copiar la URL pública resultante.
4. Sustituir la URL de ejemplo en `insertar-en-etwinning.html`.
5. Insertar el `iframe` en TwinSpace/eTwinning.

## Fragmento de inserción

```html
<iframe
  src="https://TU-USUARIO.github.io/TU-REPOSITORIO/"
  width="100%"
  height="760"
  style="border:0; border-radius:18px; max-width:1120px; width:100%;"
  loading="lazy"
  allowfullscreen>
</iframe>
```

## Región pendiente

La Basilicata está incluida en el mapa y en el desplegable, pero no tiene recurso asociado porque no se ha recibido todavía el archivo correspondiente.
