# PrecioIGTF

Calculadora web para comercios en Venezuela que cobran en dólares y facturan en bolívares.
Recibe el monto final que paga el cliente en USD y la tasa del día, y devuelve el monto que
hay que ingresar en la máquina fiscal para que, después de sumar el IVA (16 %) y el IGTF
(3 %), el total cuadre con lo cobrado.

**Pruébala:** https://odjaramillo.github.io/precioigtf/

## Cómo calcula

Partiendo del monto final en USD:

| Paso | Fórmula |
| :--- | :--- |
| Subtotal + IVA | `monto final / 1,03` |
| IGTF | `(subtotal + IVA) × 0,03` |
| Precio sin IVA | `(subtotal + IVA) / 1,16` |
| IVA | `precio sin IVA × 0,16` |
| Monto a ingresar en la máquina fiscal (Bs) | `(subtotal + IVA) × tasa del día` |

Cada resultado se muestra en bolívares y se redondea a dos decimales.

## Stack

HTML, JavaScript sin frameworks y Bulma para los estilos. Se publica con GitHub Pages.

## Contexto

Es de 2022 y fue uno de mis primeros proyectos. La lógica completa vive en
[`script.js`](script.js).
