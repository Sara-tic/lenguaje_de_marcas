# Chuleta Flex y Grid

## Dónde escribir

- **Grupo de botones del menú:** `nav ul`
- **Grupo de tarjetas:** `.platos` (o el nombre de la caja que las envuelve en el HTML)
- **Galería:** `.galeria`
- **Cabecera:** `header`
- **Pie:** `footer`
- **Página entera:** `body`
- **Una sola cosa** (un botón, una tarjeta, una foto): su nombre, por ejemplo `nav li:last-child` o `.galeria div:first-child`
- **Si el grupo no existe en el CSS:** lo creas en una línea nueva, fuera de las llaves de otro.
- **Todo va dentro de las llaves**, junto al `display: flex` o `display: grid`. Ejemplo:

```css
.platos { display: flex; gap: 16px; justify-content: center; }
```

---

## Menú (en `nav ul`)

- **En fila:** `display: flex;`
- **Separados:** `gap: 8px;`
- **Al centro:** `justify-content: center;`
- **A la derecha:** `justify-content: flex-end;`
- **Repartidos de lado a lado** (el primero pegado a la izquierda y el último a la derecha): `justify-content: space-between;`
- **Repartidos con el mismo espacio en todos lados:** `justify-content: space-evenly;`
- **En vertical (uno debajo de otro):** `flex-direction: column;`
- **Al revés:** `flex-direction: row-reverse;`
- **Solo el último botón a la derecha:** en `nav li:last-child` pones `margin-left: auto;`
- **Si tenía `inline-block` en `nav li`:** bórralo.

---

## Tarjetas (en `.platos`)

- **En fila:** `display: flex; gap: 16px;`
- **Todas igual de anchas:** en `.platos article` pones `flex: 1;` y borras `inline-block` y `width`.
- **Una el doble de ancha:** en esa tarjeta, `flex: 2;` (las demás con `flex: 1;`)
- **Una debajo de otra:** `display: flex; flex-direction: column;`
- **Que bajen de línea si no caben:** `flex-wrap: wrap;`
- **Alineadas arriba, sin estirarse:** `align-items: flex-start;`
- **Centradas en vertical:** `align-items: center;`
- **Centradas en la página:** `justify-content: center;`
- **Una sola distinta:** en esa tarjeta, `align-self: center;`

---

## Centrar algo en medio de una caja (en `header` o la caja que sea)

- **En horizontal y vertical:** `display: flex; justify-content: center; align-items: center; height: 220px;`
- **Título y subtítulo uno encima del otro:** añade `flex-direction: column;`
- **Solo en horizontal:** `display: flex; justify-content: center;`
- **Solo en vertical:** `display: flex; align-items: center; height: 220px;`
- **Solo centrar las letras** (esto no es flex): `text-align: center;`
- **Sin `height` no centra en vertical.**

---

## Galería (en `.galeria`)

- **3 columnas iguales:** `display: grid; grid-template-columns: repeat(3, 1fr);`
- **2 columnas:** `grid-template-columns: repeat(2, 1fr);`
- **4 columnas:** `grid-template-columns: repeat(4, 1fr);`
- **La segunda el doble:** `grid-template-columns: 1fr 2fr;`
- **La del medio más ancha:** `grid-template-columns: 1fr 2fr 1fr;`
- **Una fija y otra el resto:** `grid-template-columns: 200px 1fr;`
- **Hueco entre fotos:** `gap: 12px;`
- **Primera foto más ancha:** `.galeria div:first-child { grid-column: span 2; }`
- **Primera foto más alta:** `.galeria div:first-child { grid-row: span 2; }`
- **Última foto más ancha:** `.galeria div:last-child { grid-column: span 2; }`
- **Que ocupe toda la fila** (si hay 3 columnas): `grid-column: span 3;`
- **Elegir una foto concreta:** `.galeria div:nth-child(3)` es la tercera.

---

## Página con menú lateral (en `body`)

- **Dividir la página:** `display: grid; grid-template-columns: 220px 1fr; grid-template-rows: auto 1fr auto; min-height: 100vh;`
- **Dibujar las zonas:** `grid-template-areas: "menu cabecera" "menu contenido" "menu pie";`
- **Menú a la derecha:** `grid-template-columns: 1fr 220px;` y `grid-template-areas: "cabecera menu" "contenido menu" "pie menu";`
- **Cabecera y pie de lado a lado:** `grid-template-areas: "cabecera cabecera" "menu contenido" "pie pie";`
- **Decir dónde va cada parte** (líneas nuevas, debajo del `body`):

```css
nav    { grid-area: menu; }
header { grid-area: cabecera; }
main   { grid-area: contenido; }
footer { grid-area: pie; }
```

- **Menú en vertical:** en `nav ul` pones `flex-direction: column;`
- **Quitar el empujón del último botón:** en `nav li:last-child` pones `margin-left: 0;`

---

## Pie (en `footer`)

- **Textos en fila y separados:** `display: flex; justify-content: space-between;`

---

## Ojo

- Es `:` y no `=`.
- Cada línea acaba en `;`.
- Cada grupo lleva `{` al abrir y `}` al cerrar.
- No borres la línea del nombre (`.platos article {`), o todo sale en rojo.
- El archivo tiene que llamarse igual que en el HTML (`estilos.css`).
- Después de cada cambio: **Control+S** y **F5**.
- **¿Flex o grid?** Una fila de cosas: flex. Filas y columnas: grid.
