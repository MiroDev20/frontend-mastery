# Elementos en `<head>` Desglosados

## 1. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### ¿Qué es `<meta>`?

La etiqueta `<meta>` sirve para proporcionar **metadatos**.

Los metadatos son información **sobre** el documento, pero **no forman parte del contenido visible**.

Por ejemplo:

- codificación de caracteres
- descripción para buscadores
- autor
- configuración de dispositivos móviles
- palabras clave

La mayoría de las etiquetas `<meta>` no tienen etiqueta de cierre porque son
elementos vacíos.

---

### Desglose completo

#### `<meta>`

Es la etiqueta.

Le dice al navegador:

> "Voy a darte información adicional sobre esta página."

---

#### `name="viewport"`

Aquí aparece un atributo.

```
name
```

Su función es indicar **qué tipo de información** estamos configurando.

En este caso:

```
viewport
```

El viewport es el área visible de la página dentro del navegador.

Imagina esto:

```txt
  Pantalla del celular
+----------------------+
|                      |
|                      |
|    Área visible      |
|     (viewport)       |
|                      |
+----------------------+
```

El navegador necesita saber cómo debe calcular ese espacio.

---

#### `content="..."`

El atributo `content` contiene el valor asociado al `name`.

Aquí contiene dos configuraciones.

```txt
width=device-width
initial-scale=1.0
```

---

##### Primera configuración

```txt
width=device-width
```

Se divide así:

```txt
width
=
device-width
```

###### width

Significa:

> "El ancho del viewport será..."

---

###### device-width

Significa:

> "...el ancho real del dispositivo."

Si el teléfono mide 390 píxeles CSS:

```txt
viewport = 390px
```

Si la tablet mide 820 px:

```txt
viewport = 820px
```

Si es un monitor grande:

```txt
viewport = ancho del monitor
```

Sin esta configuración, algunos navegadores móviles simulan una pantalla mucho
más ancha (por ejemplo, unos 980 px CSS) para mostrar sitios antiguos, haciendo
que la página aparezca muy pequeña.

---

##### Segunda configuración

```txt
initial-scale=1.0
```

También se divide.

```txt
initial-scale
=
1.0
```

---

###### initial-scale

Indica el nivel de zoom inicial.

---

```txt
1.0 → 100%    No hay zoom.
```

**Ejemplos:**

```txt
0.5 → 50%
```

---

```txt
2.0 → 200%
```

---

#### Resumen

```txt
<meta>                 → información adicional
```

```txt
name="viewport"        → configuración del área visible
```

```txt
width=device-width     → usar el ancho real del dispositivo
```

```txt
initial-scale=1.0      → comenzar sin zoom
```

---

## 2. `<title>Mi Página Web</title>`

```html
<title>Mi Página Web</title>
```

### ¿Qué hace?

Define el título del documento.

No aparece dentro de la página.

Se muestra en:

- la pestaña del navegador
- los marcadores
- el historial
- normalmente el título que muestran los buscadores

---

### Desglose

```txt
<title>          → Abre el elemento.
```

---

```txt
Mi Página Web    → Es el contenido.
```

---

```txt
</title>         → Cierra el elemento.
```

---

### Resultado

En la pestaña del navegador aparecería algo como:

```txt
────────────────────
 Mi Página Web
────────────────────
```

---

## 3. `<link rel="stylesheet" href="estilos.css">`

```html
<link rel="stylesheet" href="estilos.css">
```

### ¿Qué es `<link>`?

La etiqueta `<link>` sirve para enlazar recursos externos con el documento HTML.

Por ejemplo:

- CSS
- iconos
- fuentes
- relaciones entre páginas

No muestra nada por sí misma.

---

### Desglose

#### `<link>`

Etiqueta para crear un enlace a un recurso.

---

#### `rel`

Significa:

```txt
relationship
```

o

> relación.

Indica:

> "¿Qué relación tiene este archivo con el documento?"

---

#### `rel="stylesheet"`

Indica:

> "Este archivo es una hoja de estilos CSS."

Entonces el navegador sabe:

```txt
Debo descargar este archivo
↓

Interpretarlo como CSS
↓

Aplicar los estilos
```

---

#### `href`

Significa:

```txt
Hypertext Reference
```

Es la dirección del recurso.

---

#### `"estilos.css"`

Es el archivo CSS.

```txt
estilos.css
```

podría contener:

```css
body {
    background: black;
}
```

---

## Flujo completo

```
HTML

↓

<link>

↓

estilos.css

↓

El navegador descarga el CSS

↓

Lo interpreta

↓

Lo aplica
```

---

## 4. `<link rel="icon" href="favicon.ico">`

```html
<link rel="icon" href="favicon.ico">
```

Es prácticamente la misma estructura.

---

### `rel="icon"`

Le dice al navegador:

> "Este archivo representa el icono del sitio."

---

### `href`

Indica dónde está el icono.

```txt
favicon.ico
```

Normalmente es un archivo pequeño.

Puede ser:

```txt
.ico
.png
.svg
```

---

### ¿Dónde aparece?

En la pestaña.

```txt
🟦 Mi Página
```

También en:

- favoritos
- historial
- marcadores
- algunas pantallas de inicio en móviles

---

## 5. `<link rel="preconnect" href="https://fonts.googleapis.com">`

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
```

Esta etiqueta está relacionada con el **rendimiento** de la página.

---

### ¿Qué hace `preconnect`?

Cuando el navegador descarga un archivo de otro servidor, normalmente realiza varios pasos:

```txt
Buscar el servidor (DNS)

↓

Abrir la conexión (TCP)

↓

Negociar una conexión segura (TLS/HTTPS)

↓

Solicitar el archivo
```

Cada paso consume tiempo.

Con `preconnect`, el navegador puede adelantar parte de ese trabajo antes de necesitar el recurso.

---

### `rel="preconnect"`

Significa:

> "Conéctate desde ahora a este servidor porque más adelante probablemente lo necesitaré."

---

### `href`

```txt
https://fonts.googleapis.com
```

Ese es el servidor desde donde se descargan las hojas de estilo de Google Fonts.

---

### Sin preconnect

```txt
Necesito una fuente

↓

Abrir conexión

↓

Esperar

↓

Descargar
```

---

### Con preconnect

```txt
Abrir conexión antes

↓

Cuando llegue el momento

↓

Descargar inmediatamente
```

---

## 6. `<link rel="preload" as="style" href="fuentes.css">`

```html
<link rel="preload" as="style" href="fuentes.css">
```

También busca mejorar el rendimiento, pero de una forma distinta.

---

### ¿Qué significa `preload`?

Le dice al navegador:

> "Este archivo será importante. Descárgalo cuanto antes."

---

### Desglose

#### `rel="preload"`

Indica una descarga anticipada.

---

#### `as="style"`

El atributo `as` especifica el tipo de recurso.

En este caso:

```txt
style        → quiere decir CSS
```

Otros valores comunes son:

```html
as="script"  → JavaScript
```

```html
as="image"   → Imagen
```

```html
as="font"    → Fuente
```

---

### `href`

Es el archivo que debe descargarse.

```txt
fuentes.css
```

---

### ¿Por qué indicar `as`?

El navegador usa esta información para:

- asignar la prioridad adecuada de descarga,
- aplicar reglas de caché correctas,
- enviar encabezados apropiados en la petición.

---

### Comparación entre `preconnect` y `preload`

| Característica | `preconnect` | `preload` |
|----------------|--------------|-----------|
| ¿Descarga archivos? | ❌ No | ✅ Sí |
| ¿Abre la conexión antes? | ✅ Sí | Puede hacerlo como parte de la descarga |
| ¿Acelera la primera conexión? | ✅ Sí | Indirectamente |
| ¿Sirve para recursos importantes? | Indirectamente | ✅ Sí |
| Ejemplo | Conectarse a `fonts.googleapis.com` | Descargar `fuentes.css` de inmediato |

## Relación entre todos estos elementos

Todos colaboran para que la página se muestre correctamente y con buen rendimiento:

```txt
<head>
│
├── <meta>   → Configura el comportamiento del navegador (por ejemplo, el viewport).
├── <title>  → Define el título de la página.
├── <link rel="stylesheet"> → Carga la hoja de estilos CSS.
├── <link rel="icon"> → Define el icono del sitio (favicon).
├── <link rel="preconnect"> → Prepara una conexión temprana con un servidor externo.
└── <link rel="preload"> → Descarga de forma anticipada un recurso importante.
```

Puedes observar un patrón útil para aprender HTML: muchas etiquetas del `<head>`
utilizan **atributos con responsabilidades bien definidas**. En los ejemplos
anteriores, `href` siempre indica **dónde está el recurso**, mientras que `rel`
indica **qué relación tiene ese recurso con el documento**, y `as` (cuando
aparece) indica **de qué tipo de recurso se trata**. Comprender el propósito de
cada atributo hace mucho más fácil recordar las distintas etiquetas.
