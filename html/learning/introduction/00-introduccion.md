# **HTML** (HyperText Markup Language)

Es un *lenguaje de marcado* utilizado para estructurar documentos que
serán analizados ([parsed](https://developer.mozilla.org/es/docs/Glossary/Parse "MDN Parse (análisis sintáctico)")) e interpretados por el navegador para construir
la página web. Para ello, **HTML** utiliza **elementos**, cuya estructura se
define mediante **etiquetas**.

Por ejemplo:

```html
<p>Hola mundo</p>
```

En este ejemplo, `<p>` es la etiqueta de apertura, `Hola mundo` es el contenido,
`</p>` es la etiqueta de cierre y todo el conjunto `<p>Hola mundo</p>`
constituye un elemento **HTML**.

Ejemplo desglosado por partes:

```html
<p>Hola mundo</p>
 │      │      │
 │      │      └────── Etiqueta de cierre
 │      └───────────── Contenido
 └──────────────────── Etiqueta de apertura

 <p>Hola mundo</p>
└─────────────────┘
        └─────── Elemento
```

Los elementos también pueden contener atributos, que proporcionan información
adicional o permiten configurar determinadas características del elemento.

```html
<a href="https://example.com">Visitar sitio</a>
```

En este caso, href es un atributo y "<https://example.com>" es su valor.

De forma general, podemos representar un elemento HTML de la siguiente manera:

```html
<etiqueta atributo="valor">contenido</etiqueta>
```

---

> Es importante comprender la diferencia entre los componentes de un documento
> HTML, ya que suelen confundirse entre sí al comenzar a aprender este lenguaje.

## 1. Empecemos con un documento HTML completo

Mira este ejemplo:

```html
<!DOCTYPE html>
<html lang="es">
  <head>                          
    <title>Mi página de ejemplo</title>
  </head>

  <body>
    <h1 class="title">Bienvenido</h1>
  
    <p>No te preocupes si aún no conoces el significado de cada elemento que ves.</p>
  
    <p>Si comprendes los fundamentos, el resto será mucho más fácil.</p>
  </body>
</html>
```

Podemos pensar que el documento está formado por piezas que se relacionan entre sí:

```text
Documento HTML
│
└── Elemento <html>
    │
    ├── Elemento <head>
    │   └── Elemento <title>
    │       └── Contenido: "Mi página de ejemplo"
    │
    └── Elemento <body>
        │
        ├── Elemento <h1>
        │   ├── Atributo: class
        │   ├── Valor: "title"
        │   └── Contenido: "Bienvenido"
        │
        ├── Elemento <p>
        │   └── Contenido: "No te preocupes si aún no conoces el
        │                   significado de cada elemento que ves."
        │
        └── Elemento <p>
            └── Contenido: "Si comprendes los fundamentos, el resto
                            será mucho más fácil."
```

Ahora vamos **concepto por concepto**.

---

## 2. Documento HTML

El **documento HTML** es el archivo completo.

Por ejemplo:

```text
index.html
```

Y dentro puede existir todo esto:

```html
<!DOCTYPE html>
<html>
  <head>
    ...
  </head>

  <body>
    ...
  </body>
</html>
```

Es decir:

> **Documento HTML = todo el documento que contiene la estructura de la página.**

No es una etiqueta ni un elemento específico.

---

## 3. Elemento

Un **elemento HTML** es una unidad estructural del documento.

Por ejemplo:

```html
<h1>Título</h1>
```

Todo eso constituye **un elemento**.

Otro:

```html
<p>Estoy aprendiendo HTML.</p>
```

También es un elemento.

Y otro:

```html
<body>
  ...
</body>
```

También.

Una forma sencilla de recordarlo:

> **Elemento = una pieza de la estructura HTML.**

---

# 4. Etiqueta

Aquí viene una distinción importante.

En:

```html
<h1>Título</h1>
```

tenemos dos etiquetas:

```text
<h1>               </h1>
  ↑                  ↑
apertura           cierre
```

La etiqueta indica **qué tipo de elemento estamos creando**.

En este caso:

```html
<h1>
```

indica un encabezado de nivel 1.

Y:

```html
</h1>
```

indica dónde termina ese elemento.

Por tanto:

```html
<h1>Título</h1>
│  │        │
│  │        └── Etiqueta de cierre
│  └─────────── Contenido
└────────────── Etiqueta de apertura
```

Mientras que:

```html
<h1>Título</h1>
└──────────────┘
        └──────── Elemento completo
```

## ⚠️ Una precisión importante

En conversaciones informales muchas personas dicen:

> "`<h1>Hola mundo</h1>` es una etiqueta."

Pero técnicamente es mejor decir:

> "`<h1>` es una etiqueta y
> `<h1>Hola mundo</h1>` es un elemento."

Esta distinción te será útil más adelante.

---

# 5. Contenido

El **contenido** es lo que se encuentra dentro del elemento.

Por ejemplo:

```html
<h1>Título</h1>
```

Tenemos:

```html
<h1>Título</h1>
└─────────────┘
   contenido
```

El contenido es:

```text
Hola mundo
```

Otro ejemplo:

```html
<p>Estoy aprendiendo HTML.</p>
```

Contenido:

```text
Estoy aprendiendo HTML.
```

Pero hay una particularidad interesante: **el contenido no necesariamente tiene que ser texto**.

Podemos tener:

```html
<div>
  <h1>Hola</h1>
  <p>Bienvenido.</p>
</div>
```

Aquí el contenido de `<div>` está compuesto por **otros elementos HTML**.

> Esto nos lleva directamente a la idea del árbol DOM (más adelante lo veremos).

---

# 6. Atributo

Ahora agreguemos un atributo:

```html
<h1 class="title">Hola mundo</h1>
```

Tenemos:

```text
<h1 class="title">
     │      │
     │      └── valor
     │
     └── atributo
```

Más concretamente:

```text
class = "title"
  │        │
  │        └── valor
  └────────── atributo
```

El atributo proporciona **información adicional al elemento** o modifica/configura determinados aspectos de su comportamiento.

Por ejemplo:

```html
<a href="https://example.com">
  Visitar sitio
</a>
```

Aquí:

```text
href
 ↓
atributo

"https://example.com"
 ↓
valor
```

---

# 7. Ahora juntemos todo

Observa este elemento:

```html
<a href="https://example.com">Visitar sitio</a>
```

Podemos descomponerlo así:

```text
<a href="https://example.com">Visitar sitio</a>
│  │      │                    │
│  │      │                    └── Contenido
│  │      └─────────────────────── Valor
│  └────────────────────────────── Atributo
└───────────────────────────────── Etiqueta
```

Y:

```text
<a href="https://example.com">Visitar sitio</a>
└──────────────────────────────────────────────┘
                    Elemento
```

Entonces:

| Concepto | Ejemplo |
|---|---|
| Documento | `index.html` |
| Elemento | `<a href="...">Visitar sitio</a>` |
| Etiqueta | `<a>` / `</a>` |
| Atributo | `href` |
| Valor | `"https://example.com"` |
| Contenido | `Visitar sitio` |

---

## 8. La jerarquía completa

Ahora podemos representar la relación:

```text
DOCUMENTO HTML
│
├── ELEMENTO
│   │
│   ├── ETIQUETA
│   │
│   ├── ATRIBUTO
│   │   └── VALOR
│   │
│   └── CONTENIDO
│
├── ELEMENTO
│   │
│   ├── ETIQUETA
│   └── CONTENIDO
│
└── ELEMENTO
```

Pero **ojo con algo**: esto no significa que todo elemento tenga necesariamente atributos, contenido de texto o incluso etiqueta de cierre.

Por ejemplo:

```html
<img src="foto.jpg" alt="Un paisaje">
```

Es un elemento `img`, tiene atributos:

```text
src → "foto.jpg"
alt → "Un paisaje"
```

pero **no tiene contenido de texto ni etiqueta de cierre** como `<p>texto</p>`.

---

# 9. ¿Y por qué todo esto importa?

Porque HTML no es simplemente:

> "texto con etiquetas".

HTML describe una **estructura jerárquica**.

Por ejemplo:

```html
<body>
  <main>
    <h1>Mi página</h1>

    <p>Bienvenido.</p>
  </main>
</body>
```

Puede representarse como:

```text
body
└── main
    ├── h1
    │   └── "Mi página"
    │
    └── p
        └── "Bienvenido."
```

Y esto es prácticamente la idea fundamental del **DOM (Document Object Model)**.

El navegador toma el HTML y construye una representación en memoria parecida a ese árbol:

```text
Document
└── html
    ├── head
    └── body
        └── main
            ├── h1
            └── p
```

---

## 🧠 Qué deberías llevarte

No intentes memorizar simplemente la lista. Piensa en **niveles**:

```text
DOCUMENTO
    ↓
ELEMENTOS
    ↓
ETIQUETAS ────┐
              │
ATRIBUTOS ── VALORES
              │
           CONTENIDO
```

Y especialmente recuerda esta diferencia:

> **Etiqueta:** `<p>`  
> **Elemento:** `<p>Hola</p>`  
> **Atributo:** `class`  
> **Valor:** `"texto"`  
> **Contenido:** `Hola`

Si entiendes esto, ya tienes una base conceptual bastante buena para pasar de **HTML → DOM → CSS → JavaScript**. 🚀
