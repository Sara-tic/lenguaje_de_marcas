# UD0 – Actividad 1

## Ejercicio 1

Crea un archivo de texto llamado `textos.txt`:

```html
<h1>Texto grande</h1>
<h3>Texto pequeño</h3>
```

Ábrelo con un navegador. Cámbialo de nombre por `textos.html`. Vuélvelo a abrir con el navegador.
¿Qué conclusiones sacas de tu observación?

### Conclusión

La conclusión es que cuando abrimos el archivo en el navegador como `.txt`, aparece en texto plano (nos aparecen directamente las etiquetas con toda la información). Y cuando lo abrimos en el navegador como `.html`, ahí es cuando el navegador interpreta las etiquetas y sí que nos pone los textos en los distintos tamaños que nosotros hemos puesto.

---

## Ejercicio 2

Completar el documento con al menos tres módulos de DAM. Archivo: `ud0_act1/DAM.sgml`

**Vocabulario:** `dam`, `modulo`, `titulo`, `contenido`, `unidad`

**Reglas:**
- `dam` contiene varios `modulo`.
- Un `modulo` tiene un `titulo` y un `contenido`.
- `contenido` tiene varias `unidad`.
- Todas las unidades están dentro de un `contenido`.
- Las unidades son texto simple.
- Detrás de una `unidad` solo puede ir otra `unidad` o el fin de `contenido`.
- Detrás de un `modulo` solo puede ir otro `modulo` o el fin de `dam`.

```xml
<dam>
  <modulo>
    <titulo>Lenguaje de Marcas</titulo>
    <contenido>
      <unidad>Introducción</unidad>
      <unidad>HTML</unidad>
      <unidad>CSS</unidad>
      <unidad>XML</unidad>
      <unidad>Sistemas de gestión de la información</unidad>
    </contenido>
  </modulo>
  <modulo>
    <titulo>Programación</titulo>
    <contenido>
      <unidad>Introducción a la programación</unidad>
      <unidad>Variables y tipos de datos</unidad>
      <unidad>Estructuras de control</unidad>
      <unidad>Programación orientada a objetos</unidad>
    </contenido>
  </modulo>
  <modulo>
    <titulo>Bases de Datos</titulo>
    <contenido>
      <unidad>Sistemas de almacenamiento</unidad>
      <unidad>Modelo entidad-relación</unidad>
      <unidad>Modelo relacional</unidad>
      <unidad>Lenguaje SQL</unidad>
    </contenido>
  </modulo>
  <modulo>
    <titulo>Sistemas Informáticos</titulo>
    <contenido>
      <unidad>Hardware</unidad>
      <unidad>Sistemas operativos</unidad>
      <unidad>Redes</unidad>
    </contenido>
  </modulo>
  <modulo>
    <titulo>Entornos de Desarrollo</titulo>
    <contenido>
      <unidad>Desarrollo de software</unidad>
      <unidad>Uso de entornos de desarrollo (IDE)</unidad>
      <unidad>Pruebas y depuración</unidad>
      <unidad>Control de versiones</unidad>
    </contenido>
  </modulo>
</dam>
```

---

## Ejercicio 3

Documento SGML propio con los datos de **PAÍSES DEL MUNDO**. Archivo: `ud0_act1/PAISES.sgml`

**Vocabulario:** `paises`, `continente`, `nombre`, `pais`, `capital`, `idioma`, `poblacion`, `moneda`

**Reglas:**
- `paises` contiene varios `continente`.
- Un `continente` tiene un `nombre` y uno o varios `pais`.
- Un `pais` tiene, en este orden: `nombre`, `capital`, uno o varios `idioma`, `poblacion` y `moneda`.
- Todos los elementos de un `pais` son texto simple.
- Detrás de un `idioma` solo puede ir otro `idioma` o `poblacion`.
- Detrás de un `pais` solo puede ir otro `pais` o el fin de `continente`.
- Detrás de un `continente` solo puede ir otro `continente` o el fin de `paises`.

```xml
<paises>
  <continente>
    <nombre>Europa</nombre>
    <pais>
      <nombre>España</nombre>
      <capital>Madrid</capital>
      <idioma>Español</idioma>
      <poblacion>48 millones</poblacion>
      <moneda>Euro</moneda>
    </pais>
    <pais>
      <nombre>Francia</nombre>
      <capital>París</capital>
      <idioma>Francés</idioma>
      <poblacion>68 millones</poblacion>
      <moneda>Euro</moneda>
    </pais>
  </continente>
  <continente>
    <nombre>África</nombre>
    <pais>
      <nombre>Marruecos</nombre>
      <capital>Rabat</capital>
      <idioma>Árabe</idioma>
      <idioma>Amazigh</idioma>
      <poblacion>37 millones</poblacion>
      <moneda>Dírham</moneda>
    </pais>
    <pais>
      <nombre>Egipto</nombre>
      <capital>El Cairo</capital>
      <idioma>Árabe</idioma>
      <poblacion>107 millones</poblacion>
      <moneda>Libra egipcia</moneda>
    </pais>
  </continente>
  <continente>
    <nombre>América</nombre>
    <pais>
      <nombre>México</nombre>
      <capital>Ciudad de México</capital>
      <idioma>Español</idioma>
      <poblacion>130 millones</poblacion>
      <moneda>Peso mexicano</moneda>
    </pais>
  </continente>
  <continente>
    <nombre>Asia</nombre>
    <pais>
      <nombre>Japón</nombre>
      <capital>Tokio</capital>
      <idioma>Japonés</idioma>
      <poblacion>124 millones</poblacion>
      <moneda>Yen</moneda>
    </pais>
  </continente>
</paises>
```

---

## Ejercicio 4

Dar estructura y significado semántico a la información de los libros. Archivo: `ud0_act1/LIBROS.sgml`

**Vocabulario:** `libreria`, `libro`, `titulo`, `formato`, `isbn`, `autor`, `paginas`, `editorial`, `anyo`, `idioma`, `sinopsis`

**Reglas:**
- `libreria` contiene varios `libro`.
- Un `libro` tiene, en este orden: `titulo`, `formato`, `isbn`, `autor`, `paginas` (opcional), `editorial`, `anyo` (opcional), `idioma` (opcional) y `sinopsis` (opcional).
- `formato` solo puede tener el valor *Papel* o *Ebook*.
- `isbn` es un número de 13 cifras.
- `paginas` y `anyo` son números; el resto de elementos son texto simple.
- Detrás de un `libro` solo puede ir otro `libro` o el fin de `libreria`.

```xml
<libreria>
  <libro>
    <titulo>Falcó</titulo>
    <formato>Papel</formato>
    <isbn>9788420419688</isbn>
    <autor>Arturo Pérez-Reverte</autor>
    <paginas>296</paginas>
    <editorial>Alfaguara</editorial>
    <idioma>Castellano</idioma>
  </libro>
  <libro>
    <titulo>Todo Alatriste</titulo>
    <formato>Ebook</formato>
    <isbn>9788420425528</isbn>
    <autor>Arturo Pérez-Reverte</autor>
    <editorial>Alfaguara</editorial>
    <idioma>Castellano</idioma>
  </libro>
  <libro>
    <titulo>Hombres buenos</titulo>
    <formato>Papel</formato>
    <isbn>9788466329804</isbn>
    <autor>Arturo Pérez-Reverte</autor>
    <editorial>Punto de Lectura</editorial>
    <anyo>2024</anyo>
    <sinopsis>La heroica aventura de quienes se atrevieron a cambiar el mundo con libros. En tiempos de oscuridad siempre hubo hombres buenos que lucharon para llevar las luces y el progreso. Y otros que procuraron impedirlo.</sinopsis>
  </libro>
</libreria>
```
