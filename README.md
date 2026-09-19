# Croquis del Deck

Planificador 3D del deck de la piscina. Sirve para probar reposeras, barra, comedor y sombrillas
antes de comprarlos, con las medidas reales del lugar y las sombras que corresponden a cada hora del día.

**Ver la app:** https://reneprieto10.github.io/croquis-deck/

## Cómo se usa

| Acción | Cómo |
|---|---|
| Girar la vista | Arrastra el fondo |
| Acercar | Rueda del mouse, o pellizco en el celular |
| Desplazar | Arrastra con el botón derecho, o con Shift |
| Mover un mueble | Arrástralo; se imanta cada 5 cm |
| Girar un mueble | Botones ⟲ / ⟳, tecla R, o Shift + arrastrar |
| Borrar | Tecla Suprimir o el botón Borrar |

Los botones **Vista de la foto** y **Aérea** llevan la cámara a dos puntos fijos. **Zonas** muestra en verde
dónde cabe un mueble dejando paso libre y en naranjo las franjas demasiado angostas. El control de
**hora del día** mueve el sol entre las 07:00 y las 20:00, que es lo que decide dónde conviene tomar sol.

La distribución se guarda en el navegador de cada persona, así que puedes cerrar y volver.

## Las medidas

No están inventadas: salen de una foto del patio, rectificada con fotogrametría. Se detectaron los bordes
del deck, de la piscina y del muro, se calculó el punto de fuga común y la distancia focal del lente, y la
escala se fijó con dos referencias que coinciden entre sí: el paso de las tablas del deck (14,5 cm) y la
altura de la cámara (1,50 m).

| Medida | Valor |
|---|---|
| Piscina | 4,4 × 9,6 m |
| Franja entre la piscina y el muro | 2,1 m |
| Franja entre la piscina y el pasto | 0,9 m |
| Fondo del deck, del muro al pasto | 7,4 m |
| Largo del deck | 15,5 m |
| Alto del muro de piedra | 1,25 m |

Margen de error de ±7%. La foto corta la piscina por la derecha, así que su largo y el largo total del deck
son mínimos, no valores exactos. Todas se editan en el panel lateral y la escena se rearma sola.

## Cómo está hecho

Un solo archivo `index.html`, sin compilación ni dependencias instaladas.

- [Babylon.js 7](https://github.com/BabylonJS/Babylon.js) (Apache-2.0) para el 3D, cargado desde jsDelivr.
- Cielo físico y agua con reflejo y refracción reales, sombras en cascada, oclusión ambiental y mapeo tonal ACES.
- Las texturas de madera, piedra, pasto y agua se generan por código al abrir la página, con sus mapas de
  normales. No hay imágenes externas salvo la foto de referencia, que va incrustada.

## Desarrollo

Abre `index.html` en el navegador. No hay nada que instalar.
