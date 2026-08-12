# HTML

**HTML** (HyperText Markup Language) es un lenguaje de marcado utilizado
para estructurar documentos que serán interpretados por un navegador web.
**HTML** permite definir qué representa cada parte del documento mediante
elementos, los cuales se escriben utilizando etiquetas.

Por ejemplo:

```html
<p>Hola mundo</p>
```

En este ejemplo, `<p>` es la etiqueta de apertura, Hola mundo es el contenido,
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
