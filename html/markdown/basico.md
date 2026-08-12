# HTML: Guía Completa para Principiantes
## 🎓 Nivel Básico - De Cero a Desarrollador Web

## 📚 Tabla de Contenidos

1. [Introducción a HTML](#1-introducción-a-html)
2. [Anatomía de un Documento HTML](#2-anatomía-de-un-documento-html)
3. [Etiquetas de Texto Básicas](#3-etiquetas-de-texto-básicas)
4. [Enlaces e Imágenes](#4-enlaces-e-imágenes)
5. [Listas en HTML](#5-listas-en-html)
6. [Tablas Básicas](#6-tablas-básicas)
7. [Formularios Básicos](#7-formularios-básicos)
8. [Elementos Semánticos Básicos](#8-elementos-semánticos-básicos)
9. [Atributos Comunes](#9-atributos-comunes)
10. [Buenas Prácticas y Validación](#10-buenas-prácticas-y-validación)

---

## 1. Introducción a HTML

### ¿Qué es HTML?

**HTML** (HyperText Markup Language) es el lenguaje de marcado estándar para crear páginas web. No es un lenguaje de programación, sino un lenguaje de marcado que define la estructura del contenido.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mi Primera Página</title>
</head>
<body>
    <h1>¡Hola Mundo!</h1>
    <p>Esta es mi primera página web.</p>
</body>
</html>
```

### Conceptos Fundamentales

**Elementos HTML**: Los bloques de construcción de las páginas web
- **Etiquetas**: Palabras clave entre `<` y `>` 
- **Atributos**: Información adicional sobre elementos
- **Contenido**: Lo que se muestra al usuario

**Jerarquía HTML**:
- **Elementos padres**: Contienen otros elementos
- **Elementos hijos**: Están contenidos dentro de otros
- **Elementos hermanos**: Están al mismo nivel

---

## 2. Anatomía de un Documento HTML

### Estructura Básica

```html
<!DOCTYPE html>
<!-- Declara el tipo de documento -->
<html lang="es">
<!-- Elemento raíz, lang define el idioma -->
<head>
    <!-- Información sobre el documento -->
    <meta charset="UTF-8">
    <!-- Codificación de caracteres -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Responsive design -->
    <title>Título de la Página</title>
    <!-- Título en la pestaña del navegador -->
    <link rel="stylesheet" href="estilos.css">
    <!-- Enlace a hoja de estilos -->
</head>
<body>
    <!-- Contenido visible de la página -->
    <h1>Bienvenido</h1>
    <p>Contenido de la página.</p>
    <script src="script.js"></script>
    <!-- Enlace a JavaScript -->
</body>
</html>
```

### Partes Esenciales Explicadas

#### 1. DOCTYPE
```html
<!DOCTYPE html>
```
- Siempre debe ser la primera línea
- Indica al navegador que es HTML5
- No es una etiqueta HTML, es una declaración

#### 2. Elemento `<html>`
```html
<html lang="es">
```
- Contenedor de toda la página
- Atributo `lang` importante para accesibilidad y SEO

#### 3. Sección `<head>`
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Página</title>
</head>
```

**Metadatos importantes**:
- `charset="UTF-8"`: Soporta caracteres internacionales
- `viewport`: Hace la página responsive en móviles
- `title`: Aparece en pestañas y resultados de búsqueda

#### 4. Sección `<body>`
```html
<body>
    <!-- Todo el contenido visible -->
</body>
```

---

## 3. Etiquetas de Texto Básicas

### Encabezados (Headings)

```html
<h1>Encabezado Principal (Solo uno por página)</h1>
<h2>Subtítulo Nivel 2</h2>
<h3>Subtítulo Nivel 3</h3>
<h4>Subtítulo Nivel 4</h4>
<h5>Subtítulo Nivel 5</h5>
<h6>Subtítulo Nivel 6</h6>
```

**Importante**:
- `h1` es el más importante, `h6` el menos
- No se usan para tamaño, sino para jerarquía
- Mejoran SEO y accesibilidad

### Párrafos y Formato de Texto

```html
<!-- Párrafo básico -->
<p>Este es un párrafo normal.</p>

<!-- Salto de línea -->
<p>Primera línea<br>Segunda línea</p>

<!-- Línea horizontal -->
<hr>

<!-- Texto en negrita -->
<p>Texto <strong>importante</strong> o <b>destacado</b>.</p>

<!-- Texto en cursiva -->
<p>Texto <em>énfasis</em> o <i>itálica</i>.</p>

<!-- Texto subrayado -->
<p>Texto <u>subrayado</u>.</p>

<!-- Texto tachado -->
<p>Texto <s>eliminado</s> o <del>tachado</del>.</p>

<!-- Texto subíndice y superíndice -->
<p>H<sub>2</sub>O (subíndice)</p>
<p>E = mc<sup>2</sup> (superíndice)</p>

<!-- Texto preformateado -->
<pre>
    Este texto
    mantiene
    los espacios
    y saltos de línea
</pre>

<!-- Código -->
<p>Para imprimir en Python: <code>print("Hola")</code></p>

<!-- Texto de teclado -->
<p>Presiona <kbd>Ctrl + S</kbd> para guardar</p>

<!-- Texto de muestra -->
<p>La salida es: <samp>Error 404</samp></p>

<!-- Variable -->
<p>La fórmula es: <var>x</var> = <var>y</var> + 2</p>

<!-- Cita corta -->
<p>Dijo: <q>Esto es una cita corta</q></p>

<!-- Cita larga -->
<blockquote>
    Esto es una cita larga que puede tener múltiples párrafos.
    Normalmente se indenta visualmente.
</blockquote>

<!-- Abreviaturas -->
<p>
    <abbr title="HyperText Markup Language">HTML</abbr>
    es el lenguaje de la web.
</p>

<!-- Dirección -->
<address>
    Contacto: <a href="mailto:ejemplo@email.com">ejemplo@email.com</a><br>
    Calle Falsa 123, Ciudad
</address>

<!-- Cita de título de obra -->
<p>
    Mi libro favorito es <cite>El Principito</cite>
    de Antoine de Saint-Exupéry.
</p>
```

### Diferencias importantes:

| Etiqueta | Uso recomendado | Ejemplo |
|----------|-----------------|---------|
| `<strong>` | Texto importante semánticamente | **Advertencia:** No tocar |
| `<b>` | Texto en negrita sin importancia semántica | Término en <b>negrita</b> |
| `<em>` | Texto con énfasis | Realmente <em>necesitas</em> esto |
| `<i>` | Texto en itálica técnico/idiomático | <i>Eureka!</i> dijo Arquímedes |

---

## 4. Enlaces e Imágenes

### Enlaces (Hyperlinks)

```html
<!-- Enlace básico -->
<a href="https://www.ejemplo.com">Visitar Ejemplo</a>

<!-- Enlace con título (tooltip) -->
<a href="https://www.ejemplo.com" title="Ir a Ejemplo">Ejemplo</a>

<!-- Enlace que se abre en nueva pestaña -->
<a href="https://www.ejemplo.com" target="_blank">Abrir en nueva pestaña</a>

<!-- Enlace a correo electrónico -->
<a href="mailto:contacto@ejemplo.com">Enviar correo</a>

<!-- Enlace para llamar (móviles) -->
<a href="tel:+34123456789">Llamar al 123 456 789</a>

<!-- Enlace a sección de la misma página -->
<a href="#seccion2">Ir a Sección 2</a>
<h2 id="seccion2">Sección 2</h2>

<!-- Enlace a archivo -->
<a href="documento.pdf" download>Descargar PDF</a>

<!-- Enlace con relación -->
<a href="pagina.html" rel="nofollow">Enlace no seguido</a>

<!-- Enlace vacío (placeholder) -->
<a href="#">Enlace temporal</a>
```

#### Tipos de rutas:

```html
<!-- Ruta absoluta (URL completa) -->
<a href="https://www.misitio.com/carpeta/pagina.html">Absoluta</a>

<!-- Ruta relativa desde la misma carpeta -->
<a href="pagina.html">Relativa misma carpeta</a>

<!-- Ruta relativa a subcarpeta -->
<a href="blog/articulo.html">Subcarpeta</a>

<!-- Ruta relativa a carpeta superior -->
<a href="../contacto.html">Carpeta superior</a>

<!-- Ruta relativa a raíz del sitio -->
<a href="/imagenes/logo.png">Desde raíz</a>
```

### Imágenes

```html
<!-- Imagen básica -->
<img src="imagen.jpg" alt="Descripción de la imagen">

<!-- Imagen con dimensiones -->
<img src="imagen.jpg" alt="Descripción" width="300" height="200">

<!-- Imagen con título (tooltip) -->
<img src="imagen.jpg" alt="Descripción" title="Título de la imagen">

<!-- Imagen responsiva -->
<img src="imagen.jpg" alt="Descripción" style="max-width: 100%; height: auto;">

<!-- Imagen con fuente múltiple (srcset) -->
<img src="imagen-pequeña.jpg" 
     srcset="imagen-grande.jpg 1200w, imagen-mediana.jpg 800w"
     sizes="(max-width: 600px) 480px, 800px"
     alt="Descripción">

<!-- Imagen como enlace -->
<a href="imagen-grande.jpg">
    <img src="imagen-miniatura.jpg" alt="Ver imagen grande">
</a>

<!-- Figura con leyenda -->
<figure>
    <img src="diagrama.jpg" alt="Diagrama del proceso">
    <figcaption>Figura 1: Diagrama del proceso de trabajo</figcaption>
</figure>
```

#### Atributo `alt` (texto alternativo):
- **Obligatorio** para accesibilidad
- Describe la imagen si no se puede cargar
- Importante para SEO
- Vacío (`alt=""`) para imágenes decorativas

**Ejemplos correctos**:
```html
<!-- Informativa -->
<img src="grafico.jpg" alt="Gráfico de ventas 2023: crecimiento del 15%">

<!-- Decorativa -->
<img src="separador.jpg" alt="">

<!-- Funcional -->
<img src="boton-buscar.jpg" alt="Buscar">

<!-- Compleja -->
<img src="mapa.jpg" alt="Mapa de la ciudad con ubicación del hotel marcada en rojo">
```

---

## 5. Listas en HTML

### Listas Desordenadas (unordered lists)

```html
<ul>
    <li>Primer elemento</li>
    <li>Segundo elemento</li>
    <li>Tercer elemento</li>
</ul>

<!-- Con diferentes marcadores -->
<ul style="list-style-type: disc;">   <!-- Por defecto -->
    <li>Elemento con punto</li>
</ul>

<ul style="list-style-type: circle;">
    <li>Elemento con círculo</li>
</ul>

<ul style="list-style-type: square;">
    <li>Elemento con cuadrado</li>
</ul>

<ul style="list-style-type: none;">
    <li>Elemento sin marcador</li>
</ul>
```

### Listas Ordenadas (ordered lists)

```html
<ol>
    <li>Primer paso</li>
    <li>Segundo paso</li>
    <li>Tercer paso</li>
</ol>

<!-- Diferentes tipos de numeración -->
<ol type="1">   <!-- Por defecto -->
    <li>Números (1, 2, 3)</li>
</ol>

<ol type="A">
    <li>Letras mayúsculas (A, B, C)</li>
</ol>

<ol type="a">
    <li>Letras minúsculas (a, b, c)</li>
</ol>

<ol type="I">
    <li>Números romanos mayúsculas (I, II, III)</li>
</ol>

<ol type="i">
    <li>Números romanos minúsculas (i, ii, iii)</li>
</ol>

<!-- Empezar desde un número específico -->
<ol start="10">
    <li>Elemento 10</li>
    <li>Elemento 11</li>
</ol>

<!-- Lista inversa -->
<ol reversed>
    <li>Tercer elemento</li>
    <li>Segundo elemento</li>
    <li>Primer elemento</li>
</ol>
```

### Listas de Definición (definition lists)

```html
<dl>
    <dt>HTML</dt>
    <dd>Lenguaje de marcado para crear páginas web</dd>
    
    <dt>CSS</dt>
    <dd>Lenguaje para estilizar páginas web</dd>
    
    <dt>JavaScript</dt>
    <dd>Lenguaje de programación para interactividad web</dd>
</dl>
```

### Listas Anidadas

```html
<ul>
    <li>Frutas
        <ul>
            <li>Manzanas</li>
            <li>Naranjas</li>
            <li>Plátanos</li>
        </ul>
    </li>
    <li>Verduras
        <ul>
            <li>Zanahorias</li>
            <li>Brócoli</li>
            <li>Espinacas</li>
        </ul>
    </li>
    <li>Lácteos
        <ol>
            <li>Leche</li>
            <li>Queso</li>
            <li>Yogur</li>
        </ol>
    </li>
</ul>
```

### Listas con Elementos Complejos

```html
<ul>
    <li>
        <h3>Título del elemento</h3>
        <p>Descripción detallada del elemento.</p>
        <a href="#">Enlace relacionado</a>
    </li>
    <li>
        <img src="icono.jpg" alt="Icono">
        <strong>Elemento importante</strong>
        <span>Información adicional</span>
    </li>
</ul>
```

---

## 6. Tablas Básicas

### Estructura Básica de una Tabla

```html
<table>
    <tr>  <!-- Table Row (fila) -->
        <th>Encabezado 1</th>  <!-- Table Header (celda de encabezado) -->
        <th>Encabezado 2</th>
        <th>Encabezado 3</th>
    </tr>
    <tr>
        <td>Dato 1</td>  <!-- Table Data (celda de datos) -->
        <td>Dato 2</td>
        <td>Dato 3</td>
    </tr>
    <tr>
        <td>Dato 4</td>
        <td>Dato 5</td>
        <td>Dato 6</td>
    </tr>
</table>
```

### Tabla Completa con Todas las Partes

```html
<table>
    <!-- Caption: Título de la tabla -->
    <caption>Horario de Clases</caption>
    
    <!-- Encabezado de la tabla -->
    <thead>
        <tr>
            <th>Hora</th>
            <th>Lunes</th>
            <th>Martes</th>
            <th>Miércoles</th>
            <th>Jueves</th>
            <th>Viernes</th>
        </tr>
    </thead>
    
    <!-- Cuerpo de la tabla -->
    <tbody>
        <tr>
            <th>8:00 - 9:00</th>
            <td>Matemáticas</td>
            <td>Historia</td>
            <td>Matemáticas</td>
            <td>Ciencias</td>
            <td>Educación Física</td>
        </tr>
        <tr>
            <th>9:00 - 10:00</th>
            <td>Español</td>
            <td>Matemáticas</td>
            <td>Español</td>
            <td>Historia</td>
            <td>Música</td>
        </tr>
    </tbody>
    
    <!-- Pie de la tabla -->
    <tfoot>
        <tr>
            <th>Total Horas</th>
            <td>2</td>
            <td>2</td>
            <td>2</td>
            <td>2</td>
            <td>2</td>
        </tr>
    </tfoot>
</table>
```

### Tablas con Celdas Combinadas

```html
<table border="1">
    <tr>
        <th colspan="2">Nombre Completo</th>  <!-- Combina 2 columnas -->
        <th>Edad</th>
    </tr>
    <tr>
        <td>María</td>
        <td>García</td>
        <td>25</td>
    </tr>
    <tr>
        <td>Juan</td>
        <td>Pérez</td>
        <td rowspan="2">30</td>  <!-- Combina 2 filas -->
    </tr>
    <tr>
        <td>Ana</td>
        <td>López</td>
    </tr>
</table>
```

### Tablas con Estructura Compleja

```html
<table>
    <colgroup>
        <col style="background-color: #f0f0f0;">  <!-- Estilo para columna 1 -->
        <col span="2" style="background-color: #e0e0e0;">  <!-- Columnas 2 y 3 -->
    </colgroup>
    
    <thead>
        <tr>
            <th scope="col">Producto</th>  <!-- scope ayuda a accesibilidad -->
            <th scope="col">Precio</th>
            <th scope="col">Stock</th>
        </tr>
    </thead>
    
    <tbody>
        <tr>
            <th scope="row">Laptop</th>  <!-- Encabezado de fila -->
            <td>$999</td>
            <td>15</td>
        </tr>
        <tr>
            <th scope="row">Tablet</th>
            <td>$299</td>
            <td>30</td>
        </tr>
    </tbody>
</table>
```

### Tabla Responsiva Básica

```html
<div style="overflow-x: auto;">  <!-- Contenedor para scroll horizontal -->
    <table style="min-width: 600px;">
        <!-- Tabla ancha que necesita scroll en móviles -->
        <tr>
            <th>Producto</th>
            <th>Descripción</th>
            <th>Precio</th>
            <th>Descuento</th>
            <th>Precio Final</th>
            <th>Disponibilidad</th>
        </tr>
        <tr>
            <td>Laptop XYZ</td>
            <td>Laptop de 15 pulgadas, 8GB RAM</td>
            <td>$999</td>
            <td>10%</td>
            <td>$899</td>
            <td>En stock</td>
        </tr>
    </table>
</div>
```

---

## 7. Formularios Básicos

### Estructura Básica de un Formulario

```html
<form action="/procesar.php" method="POST">
    <!-- Campos del formulario aquí -->
    <input type="submit" value="Enviar">
</form>
```

### Métodos de Envío

```html
<!-- GET: Datos visibles en URL (para búsquedas) -->
<form action="/buscar" method="GET">
    <input type="text" name="q" placeholder="Buscar...">
    <input type="submit" value="Buscar">
</form>
<!-- Resultado: /buscar?q=termino+busqueda -->

<!-- POST: Datos ocultos (para formularios sensibles) -->
<form action="/registro" method="POST">
    <!-- Campos de registro -->
    <input type="submit" value="Registrarse">
</form>
```

### Elementos de Formulario

#### Campos de Texto

```html
<!-- Texto simple -->
<label for="nombre">Nombre:</label>
<input type="text" id="nombre" name="nombre" placeholder="Escribe tu nombre">

<!-- Texto con valor por defecto -->
<input type="text" name="ciudad" value="Madrid">

<!-- Texto requerido -->
<input type="text" name="email" required>

<!-- Texto con patrón (regex) -->
<input type="text" name="codigo" pattern="[A-Z]{3}[0-9]{3}" 
       title="3 letras mayúsculas y 3 números">

<!-- Texto con longitud máxima -->
<input type="text" name="mensaje" maxlength="200">

<!-- Texto con sugerencias -->
<input type="text" name="pais" list="paises">
<datalist id="paises">
    <option value="España">
    <option value="México">
    <option value="Argentina">
    <option value="Colombia">
</datalist>

<!-- Área de texto multilínea -->
<label for="comentario">Comentario:</label>
<textarea id="comentario" name="comentario" rows="4" cols="50">
Texto por defecto
</textarea>
```

#### Contraseñas

```html
<label for="password">Contraseña:</label>
<input type="password" id="password" name="password">

<!-- Mostrar/ocultar contraseña -->
<input type="password" id="pass" name="pass">
<button type="button" onclick="mostrarPass()">👁️</button>

<script>
function mostrarPass() {
    const pass = document.getElementById('pass');
    pass.type = pass.type === 'password' ? 'text' : 'password';
}
</script>
```

#### Opciones Únicas (Radio Buttons)

```html
<fieldset>
    <legend>Selecciona tu género:</legend>
    
    <input type="radio" id="masculino" name="genero" value="masculino">
    <label for="masculino">Masculino</label><br>
    
    <input type="radio" id="femenino" name="genero" value="femenino">
    <label for="femenino">Femenino</label><br>
    
    <input type="radio" id="otro" name="genero" value="otro">
    <label for="otro">Otro</label>
</fieldset>

<!-- Con selección por defecto -->
<input type="radio" id="si" name="suscripcion" value="si" checked>
<label for="si">Sí, suscribirme</label>
```

#### Opciones Múltiples (Checkboxes)

```html
<fieldset>
    <legend>Intereses (selecciona varios):</legend>
    
    <input type="checkbox" id="deportes" name="intereses" value="deportes">
    <label for="deportes">Deportes</label><br>
    
    <input type="checkbox" id="musica" name="intereses" value="musica">
    <label for="musica">Música</label><br>
    
    <input type="checkbox" id="lectura" name="intereses" value="lectura">
    <label for="lectura">Lectura</label>
</fieldset>
```

#### Listas Desplegables (Select)

```html
<!-- Selección simple -->
<label for="pais">País:</label>
<select id="pais" name="pais">
    <option value="">Selecciona un país</option>
    <option value="es">España</option>
    <option value="mx">México</option>
    <option value="ar">Argentina</option>
</select>

<!-- Selección múltiple -->
<label for="deportes">Deportes favoritos:</label>
<select id="deportes" name="deportes" multiple size="4">
    <option value="futbol">Fútbol</option>
    <option value="baloncesto">Baloncesto</option>
    <option value="tenis">Tenis</option>
    <option value="natacion">Natación</option>
</select>

<!-- Grupos de opciones -->
<label for="coche">Coche:</label>
<select id="coche" name="coche">
    <optgroup label="Alemán">
        <option value="audi">Audi</option>
        <option value="bmw">BMW</option>
        <option value="mercedes">Mercedes</option>
    </optgroup>
    <optgroup label="Japonés">
        <option value="toyota">Toyota</option>
        <option value="honda">Honda</option>
        <option value="nissan">Nissan</option>
    </optgroup>
</select>
```

#### Campos Especializados

```html
<!-- Email (validación automática) -->
<input type="email" name="correo" placeholder="usuario@ejemplo.com">

<!-- Número -->
<input type="number" name="edad" min="0" max="120" step="1" value="25">

<!-- Rango (slider) -->
<input type="range" name="volumen" min="0" max="100" value="50">

<!-- Fecha -->
<input type="date" name="nacimiento">

<!-- Hora -->
<input type="time" name="hora">

<!-- Color -->
<input type="color" name="color_favorito" value="#ff0000">

<!-- URL -->
<input type="url" name="sitio_web" placeholder="https://ejemplo.com">

<!-- Teléfono -->
<input type="tel" name="telefono" pattern="[0-9]{9}">

<!-- Archivo -->
<input type="file" name="archivo" accept=".pdf,.jpg,.png">

<!-- Oculto -->
<input type="hidden" name="token" value="abc123">
```

#### Botones

```html
<!-- Botón de envío -->
<input type="submit" value="Enviar Formulario">
<button type="submit">Enviar</button>

<!-- Botón de reset -->
<input type="reset" value="Limpiar Formulario">

<!-- Botón normal -->
<button type="button" onclick="alert('Hola')">Click Me</button>

<!-- Botón con imagen -->
<button type="submit">
    <img src="icono-enviar.png" alt="Enviar">
    Enviar
</button>
```

### Formulario Completo de Ejemplo

```html
<form action="/registro" method="POST">
    <fieldset>
        <legend>Información Personal</legend>
        
        <div>
            <label for="nombre">Nombre completo:*</label>
            <input type="text" id="nombre" name="nombre" required>
        </div>
        
        <div>
            <label for="email">Correo electrónico:*</label>
            <input type="email" id="email" name="email" required>
        </div>
        
        <div>
            <label for="telefono">Teléfono:</label>
            <input type="tel" id="telefono" name="telefono">
        </div>
        
        <div>
            <label>Género:</label>
            <input type="radio" id="m" name="genero" value="M">
            <label for="m">Masculino</label>
            
            <input type="radio" id="f" name="genero" value="F">
            <label for="f">Femenino</label>
        </div>
    </fieldset>
    
    <fieldset>
        <legend>Preferencias</legend>
        
        <div>
            <label for="pais">País:</label>
            <select id="pais" name="pais">
                <option value="">Selecciona...</option>
                <option value="es">España</option>
                <option value="mx">México</option>
                <option value="ar">Argentina</option>
            </select>
        </div>
        
        <div>
            <label>Intereses:</label>
            <input type="checkbox" id="tech" name="intereses" value="tech">
            <label for="tech">Tecnología</label>
            
            <input type="checkbox" id="sports" name="intereses" value="sports">
            <label for="sports">Deportes</label>
            
            <input type="checkbox" id="music" name="intereses" value="music">
            <label for="music">Música</label>
        </div>
        
        <div>
            <label for="mensaje">Mensaje:</label>
            <textarea id="mensaje" name="mensaje" rows="4"></textarea>
        </div>
    </fieldset>
    
    <div>
        <button type="submit">Registrarse</button>
        <button type="reset">Limpiar</button>
    </div>
</form>
```

---

## 8. Elementos Semánticos Básicos

### ¿Qué es HTML Semántico?

**HTML semántico** significa usar las etiquetas HTML que mejor describen el significado del contenido, no solo su apariencia.

```html
<!-- NO semántico -->
<div id="header">
    <div class="menu">...</div>
</div>

<!-- SEMÁNTICO -->
<header>
    <nav>...</nav>
</header>
```

### Elementos Semánticos Principales

#### 1. `<header>` - Cabecera
```html
<header>
    <h1>Nombre del Sitio</h1>
    <p>Eslogan o descripción breve</p>
    <nav>
        <a href="/">Inicio</a>
        <a href="/nosotros">Nosotros</a>
        <a href="/contacto">Contacto</a>
    </nav>
</header>
```

#### 2. `<nav>` - Navegación
```html
<nav>
    <ul>
        <li><a href="/">Inicio</a></li>
        <li><a href="/productos">Productos</a>
            <ul>
                <li><a href="/productos/laptops">Laptops</a></li>
                <li><a href="/productos/tablets">Tablets</a></li>
            </ul>
        </li>
        <li><a href="/contacto">Contacto</a></li>
    </ul>
</nav>
```

#### 3. `<main>` - Contenido Principal
```html
<main>
    <h1>Artículo Principal</h1>
    <p>Contenido más importante de la página...</p>
</main>
```

#### 4. `<article>` - Artículo Independiente
```html
<article>
    <header>
        <h2>Título del Artículo</h2>
        <p>Publicado el <time datetime="2024-01-15">15 de Enero 2024</time></p>
    </header>
    
    <p>Contenido del artículo...</p>
    
    <footer>
        <p>Escrito por: Autor</p>
    </footer>
</article>
```

#### 5. `<section>` - Sección Temática
```html
<section>
    <h2>Nuestros Servicios</h2>
    <article>
        <h3>Diseño Web</h3>
        <p>Descripción del servicio...</p>
    </article>
    <article>
        <h3>Marketing Digital</h3>
        <p>Descripción del servicio...</p>
    </article>
</section>
```

#### 6. `<aside>` - Contenido Relacionado
```html
<aside>
    <h3>Artículos Relacionados</h3>
    <ul>
        <li><a href="#">Artículo relacionado 1</a></li>
        <li><a href="#">Artículo relacionado 2</a></li>
    </ul>
</aside>

<!-- También para barras laterales -->
<aside>
    <h3>Sidebar</h3>
    <p>Publicidad o contenido adicional...</p>
</aside>
```

#### 7. `<footer>` - Pie de Página
```html
<footer>
    <p>&copy; 2024 Mi Sitio Web. Todos los derechos reservados.</p>
    <address>
        Contacto: <a href="mailto:info@misitio.com">info@misitio.com</a>
    </address>
    <nav>
        <a href="/privacidad">Política de Privacidad</a>
        <a href="/terminos">Términos de Uso</a>
    </nav>
</footer>
```

#### 8. `<figure>` y `<figcaption>` - Figuras
```html
<figure>
    <img src="grafico.jpg" alt="Gráfico de crecimiento">
    <figcaption>Figura 1: Crecimiento anual de la empresa</figcaption>
</figure>

<figure>
    <pre>
        <code>
function saludar() {
    console.log("Hola Mundo");
}
        </code>
    </pre>
    <figcaption>Código 1: Función de saludo en JavaScript</figcaption>
</figure>
```

### Estructura Semántica Completa

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Blog Personal</title>
</head>
<body>
    <!-- Cabecera del sitio -->
    <header>
        <h1>Mi Blog Personal</h1>
        <p>Reflexiones sobre tecnología y desarrollo web</p>
        
        <!-- Navegación principal -->
        <nav>
            <ul>
                <li><a href="/">Inicio</a></li>
                <li><a href="/blog">Blog</a></li>
                <li><a href="/proyectos">Proyectos</a></li>
                <li><a href="/contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>
    
    <!-- Contenido principal -->
    <main>
        <!-- Artículo principal -->
        <article>
            <header>
                <h2>Aprendiendo HTML5 Semántico</h2>
                <p>
                    Publicado el 
                    <time datetime="2024-01-20">20 de Enero, 2024</time>
                    por <strong>Carlos Rodríguez</strong>
                </p>
            </header>
            
            <!-- Sección de introducción -->
            <section>
                <h3>Introducción</h3>
                <p>HTML semántico es fundamental para el desarrollo web moderno...</p>
            </section>
            
            <!-- Sección de ejemplos -->
            <section>
                <h3>Ejemplos Prácticos</h3>
                <p>Veamos algunos ejemplos de elementos semánticos...</p>
                
                <figure>
                    <img src="estructura-semantica.jpg" 
                         alt="Diagrama de estructura semántica HTML">
                    <figcaption>Estructura semántica típica de una página web</figcaption>
                </figure>
            </section>
            
            <!-- Pie del artículo -->
            <footer>
                <p>Categorías: <a href="/categoria/html">HTML</a>, 
                   <a href="/categoria/web">Desarrollo Web</a></p>
                <p>Etiquetas: #HTML5 #Semántica #Web</p>
            </footer>
        </article>
        
        <!-- Barra lateral -->
        <aside>
            <section>
                <h3>Sobre el Autor</h3>
                <p>Carlos es desarrollador web con 10 años de experiencia...</p>
            </section>
            
            <section>
                <h3>Artículos Populares</h3>
                <ul>
                    <li><a href="#">Introducción a CSS Grid</a></li>
                    <li><a href="#">JavaScript Moderno</a></li>
                </ul>
            </section>
        </aside>
    </main>
    
    <!-- Pie de página -->
    <footer>
        <p>&copy; 2024 Mi Blog Personal. Todos los derechos reservados.</p>
        <address>
            Contacto: <a href="mailto:contacto@miblog.com">contacto@miblog.com</a>
        </address>
        <nav>
            <a href="/privacidad">Privacidad</a> |
            <a href="/terminos">Términos</a> |
            <a href="/sitemap">Mapa del Sitio</a>
        </nav>
    </footer>
</body>
</html>
```

---

## 9. Atributos Comunes

### Atributos Globales (funcionan en todas las etiquetas)

```html
<!-- id - Identificador único -->
<div id="header">...</div>

<!-- class - Clase para agrupar elementos -->
<p class="destacado importante">Texto</p>
<p class="destacado">Otro texto</p>

<!-- style - Estilos en línea -->
<p style="color: blue; font-size: 16px;">Texto azul</p>

<!-- title - Información adicional (tooltip) -->
<a href="#" title="Más información sobre esto">Enlace</a>

<!-- data-* - Datos personalizados -->
<div data-id="123" data-categoria="libros">Producto</div>

<!-- aria-* - Atributos para accesibilidad -->
<button aria-label="Cerrar menú">X</button>

<!-- tabindex - Orden de tabulación -->
<input type="text" tabindex="1">
<button tabindex="2">Enviar</button>

<!-- contenteditable - Permite edición -->
<div contenteditable="true">Puedes editar este texto</div>

<!-- hidden - Oculta el elemento -->
<p hidden>Este texto no es visible</p>

<!-- draggable - Permite arrastrar -->
<div draggable="true">Arrástrame</div>

<!-- spellcheck - Corrección ortográfica -->
<textarea spellcheck="true">Texto con corrección</textarea>

<!-- translate - Indica si traducir -->
<p translate="no">Don't translate this</p>

<!-- dir - Dirección del texto -->
<p dir="ltr">Texto izquierda a derecha</p>
<p dir="rtl">نص من اليمين إلى اليسار</p>

<!-- lang - Idioma del contenido -->
<p lang="en">This is English text</p>
<p lang="fr">Ceci est du texte français</p>
```

### Atributos Específicos

#### Para Enlaces (`<a>`)
```html
<a href="https://ejemplo.com" 
   target="_blank"
   rel="noopener noreferrer"
   download="archivo.pdf"
   hreflang="en"
   type="application/pdf">
    Enlace
</a>
```

#### Para Imágenes (`<img>`)
```html
<img src="imagen.jpg" 
     alt="Descripción"
     width="300"
     height="200"
     loading="lazy"
     decoding="async"
     crossorigin="anonymous">
```

#### Para Formularios
```html
<input type="text"
       name="usuario"
       value="valor inicial"
       placeholder="Escribe algo..."
       required
       readonly
       disabled
       maxlength="100"
       minlength="2"
       pattern="[A-Za-z]+"
       autocomplete="on"
       autofocus
       size="30">
```

### Atributos de Eventos

```html
<!-- Eventos de ratón -->
<button onclick="alert('¡Hola!')">Click</button>
<button onmouseover="this.style.color='red'"
        onmouseout="this.style.color='black'">
    Pasa el ratón
</button>

<!-- Eventos de teclado -->
<input onkeydown="console.log('Tecla presionada')"
       onkeyup="console.log('Tecla soltada')">

<!-- Eventos de formulario -->
<form onsubmit="return validarFormulario()"
      onreset="console.log('Formulario limpiado')">
    <!-- Campos -->
</form>

<!-- Eventos de foco -->
<input onfocus="this.style.background='yellow'"
       onblur="this.style.background='white'">

<!-- Eventos de carga -->
<img onload="console.log('Imagen cargada')"
     onerror="console.log('Error cargando imagen')"
     src="imagen.jpg">

<body onload="inicializarPagina()"
      onunload="guardarDatos()">
```

---

## 10. Buenas Prácticas y Validación

### 1. Estructura Correcta del Documento

**✅ CORRECTO:**
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Título Correcto</title>
</head>
<body>
    <h1>Título Principal</h1>
    <!-- Contenido -->
</body>
</html>
```

**❌ INCORRECTO:**
```html
<!-- Sin DOCTYPE -->
<!-- Sin charset -->
<!-- Título en body -->
```

### 2. Indentación y Formato

```html
<!-- ✅ Correcto -->
<body>
    <header>
        <h1>Título</h1>
        <nav>
            <ul>
                <li><a href="#">Enlace</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <article>
            <h2>Artículo</h2>
            <p>Párrafo</p>
        </article>
    </main>
</body>

<!-- ❌ Incorrecto -->
<body><header><h1>Título</h1>
<nav><ul><li><a href="#">Enlace</a></li></ul>
</nav></header><main><article>
<h2>Artículo</h2><p>Párrafo</p></article>
</main></body>
```

### 3. Uso Correcto de Etiquetas

```html
<!-- ✅ Semántico -->
<header>
    <h1>Logo</h1>
    <nav>...</nav>
</header>

<!-- ❌ No semántico -->
<div class="header">
    <div class="logo">Logo</div>
    <div class="menu">...</div>
</div>

<!-- ✅ Jerarquía correcta -->
<h1>Título Principal</h1>
<h2>Subtítulo</h2>
<h3>Sub-subtítulo</h3>

<!-- ❌ Jerarquía incorrecta -->
<h3>Título Principal</h3>
<h1>Subtítulo</h1>
<h2>Sub-subtítulo</h2>
```

### 4. Accesibilidad Básica

```html
<!-- ✅ Accesible -->
<img src="grafico.jpg" alt="Gráfico de ventas mensuales">
<label for="nombre">Nombre:</label>
<input type="text" id="nombre" name="nombre">
<button aria-label="Cerrar ventana">X</button>

<!-- ❌ No accesible -->
<img src="grafico.jpg">
<input type="text" name="nombre">
<div onclick="cerrar()">X</div>

<!-- ✅ Contraste adecuado -->
<p style="color: #000; background: #fff;">Texto legible</p>

<!-- ❌ Contraste pobre -->
<p style="color: #ccc; background: #fff;">Texto difícil de leer</p>
```

### 5. Validación HTML

#### Validación Manual
1. **Estructura**: Verificar etiquetas abiertas/cerradas
2. **Atributos**: Comprobar atributos obligatorios
3. **Anidamiento**: Confirmar jerarquía correcta
4. **Semántica**: Usar etiquetas apropiadas

#### Herramientas de Validación
- **W3C Validator**: https://validator.w3.org/
- **HTMLHint**: Extensión para editores de código
- **Lighthouse**: Herramienta de Chrome DevTools

#### Errores Comunes a Evitar

```html
<!-- ❌ Etiquetas sin cerrar -->
<p>Texto sin cerrar
<div>Div sin cerrar

<!-- ❌ Atributos mal escritos -->
<imput type="text">  <!-- "input" mal escrito -->
<img scr="foto.jpg"> <!-- "src" mal escrito -->

<!-- ❌ Anidamiento incorrecto -->
<p>Texto <div>Div dentro de párrafo</div></p>

<!-- ❌ Atributos duplicados -->
<input type="text" type="password">

<!-- ❌ Caracteres especiales sin escape -->
<p>El precio es 10 < 20</p>  <!-- Usar &lt; -->

<!-- ✅ Corregido -->
<p>Texto sin cerrar</p>
<div>Div sin cerrar</div>

<input type="text">
<img src="foto.jpg">

<p>Texto</p>
<div>Div después de párrafo</div>

<input type="text">

<p>El precio es 10 &lt; 20</p>
```

### 6. SEO Básico

```html
<!-- ✅ Buen SEO -->
<head>
    <title>Mi Empresa - Servicios de Desarrollo Web</title>
    <meta name="description" content="Empresa especializada en desarrollo web con 10 años de experiencia">
    <meta name="keywords" content="desarrollo web, HTML, CSS, JavaScript">
    <link rel="canonical" href="https://www.miempresa.com">
</head>
<body>
    <h1>Servicios de Desarrollo Web</h1>
    <h2>Diseño Responsive</h2>
    <p>Creación de sitios web adaptables a todos los dispositivos...</p>
</body>

<!-- ❌ SEO pobre -->
<head>
    <title>Página 1</title>
</head>
<body>
    <h3>Título Principal</h3>
    <div>Texto importante aquí</div>
</body>
```

### 7. Rendimiento

```html
<!-- ✅ Optimizado -->
<img src="imagen.jpg" 
     alt="Descripción" 
     width="300" 
     height="200"
     loading="lazy">

<script src="script.js" defer></script>
<link rel="stylesheet" href="estilos.css">

<!-- ❌ No optimizado -->
<img src="imagen-muy-grande.jpg" alt="">
<script src="script.js"></script> <!-- Bloqueante -->
```

### 8. Compatibilidad entre Navegadores

```html
<!-- ✅ Compatible -->
<input type="text" placeholder="Escribe aquí">

<!-- Con fallback -->
<video controls>
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    <p>Tu navegador no soporta video HTML5</p>
</video>

<!-- Polyfill para IE -->
<!--[if IE]>
    <script src="html5shiv.js"></script>
<![endif]-->
```

### 9. Mantenibilidad

```html
<!-- ✅ Fácil de mantener -->
<!-- Header principal -->
<header class="main-header">
    <h1 class="site-title">Mi Sitio</h1>
    <!-- Navegación principal -->
    <nav class="main-nav" aria-label="Navegación principal">
        <ul>
            <li><a href="/">Inicio</a></li>
            <li><a href="/servicios">Servicios</a></li>
        </ul>
    </nav>
</header>

<!-- ❌ Difícil de mantener -->
<header><h1>Mi Sitio</h1><div><ul><li><a href="#">Inicio</a></li></ul></div></header>
```

### Checklist de Buenas Prácticas

- [ ] DOCTYPE HTML5 presente
- [ ] Charset UTF-8 definido
- [ ] Viewport configurado para responsive
- [ ] Título único y descriptivo
- [ ] Estructura semántica correcta
- [ ] Encabezados con jerarquía adecuada
- [ ] Todas las imágenes tienen atributo `alt`
- [ ] Formularios tienen etiquetas `label`
- [ ] Enlaces tienen texto descriptivo
- [ ] Código indentado correctamente
- [ ] Atributos entre comillas
- [ ] Validación W3C pasa sin errores
- [ ] Compatibilidad con navegadores antiguos verificada
- [ ] Metadatos SEO básicos presentes
- [ ] Favicon configurado
- [ ] Scripts al final del body o con `defer`

---

## 🎓 Ejercicios Prácticos

### Ejercicio 1: Página Personal Básica
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi Página Personal</title>
</head>
<body>
    <!-- Crear:
    1. Título principal con tu nombre
    2. Foto tuya con descripción
    3. Lista de hobbies
    4. Tabla con información personal
    5. Formulario de contacto
    6. Enlaces a redes sociales
    -->
</body>
</html>
```

### Ejercicio 2: Receta de Cocina
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Receta de Paella</title>
</head>
<body>
    <!-- Crear:
    1. Nombre del plato
    2. Imagen de la paella
    3. Lista de ingredientes
    4. Pasos numerados para preparación
    5. Tabla con información nutricional
    6. Sección de comentarios con formulario
    -->
</body>
</html>
```

### Ejercicio 3: Blog Simple
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi Blog</title>
</head>
<body>
    <!-- Crear estructura semántica:
    1. Header con título y navegación
    2. Main con varios artículos
    3. Cada artículo con título, fecha y contenido
    4. Aside con información del autor
    5. Footer con información de contacto
    6. Formulario de suscripción
    -->
</body>
</html>
```

## 📚 Recursos Adicionales

### Herramientas
- **Editores**: VS Code, Sublime Text, Atom
- **Validadores**: W3C Validator, HTMLHint
- **Referencias**: MDN Web Docs, W3Schools

### Próximos Pasos
1. **CSS Básico**: Aprender a estilizar tu HTML
2. **JavaScript Intro**: Agregar interactividad
3. **Responsive Design**: Hacer sitios para móviles
4. **Formularios Avanzados**: Validación y envío
5. **Accesibilidad Web**: Hacer sitios para todos

### Consejos Finales
- **Practica diariamente**: Crea páginas reales
- **Inspecciona sitios web**: Aprende de otros
- **Valida tu código**: Corrige errores temprano
- **Usa semántica**: Mejora SEO y accesibilidad
- **Mantén simple**: Empieza con lo básico

---

## 🎯 ¡Felicidades!

Has completado la **Guía Básica de HTML**. Ahora puedes:

✅ Crear páginas web básicas con estructura correcta  
✅ Usar etiquetas HTML apropiadamente  
✅ Crear formularios funcionales  
✅ Implementar tablas y listas  
✅ Entender HTML semántico  
✅ Validar y mantener código limpio  

**¿Listo para el siguiente nivel?** En la guía intermedia aprenderás:
- HTML5 APIs avanzadas
- Formularios complejos
- Integración con CSS y JavaScript
- Técnicas de accesibilidad
- Optimización y rendimiento

**¡Sigue practicando y construyendo proyectos!** 🚀 
