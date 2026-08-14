# Estructura Básica de un Documento **HTML**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Sitio Web</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Contenido visible -->
</body>
</html>
```

## 1. `<!DOCTYPE html>`

Esta declaración indica que el documento debe interpretarse usando el modo
estándar de HTML (Standards Mode). En HTML moderno esto corresponde al
estándar HTML5.

¡Ojo!, no le dice al navegador "usa HTML5" porque los navegadores actuales ya
implementan HTML vivo (Living Standard), sino:

> "Interpreta este documento con las reglas modernas."

Sin `<!DOCTYPE html>` muchos navegadores entran en Quirks Mode.
Quirks Mode significa:

> "Voy a comportarme como Internet Explorer de hace más de 20 años para mantener
> compatibilidad."

Eso puede romper:

* tamaños
* márgenes
* cajas (box model)
* CSS
* tablas

Por eso prácticamente siempre debe existir.

## 2. `<html lang="es">`

La etiqueta `<html>` representa la raíz o contenedor principal de un documento
HTML. Define el inicio y el final del documento y engloba todos los demás
elementos HTML, excepto la declaración `<!DOCTYPE html>`.

El atributo `lang` sirve para indicar en qué idioma está escrito el documento,
en el caso del ejemplo se usa el valor `es` indicando que el idioma es español.

Eso ayuda a:

* lectores de pantalla
* buscadores (SEO)
* traductores automáticos
* correctores ortográficos
* navegadores

Características:

* es el elemento raíz
* contiene absolutamente todo el documento
* solo puede existir uno
* normalmente tiene el atributo lang
* puede tener otros atributos globales (dir, class, id, etc.)

## 3. `<head>`

La etiqueta `<head>` en HTML conforma una sección esencial de un documento HTML
que contiene metadatos e información sobre el documento, pero no muestra
contenido visible directamente en la página web. Está ubicado entre las
etiquetas `<html>` y `<body>`.

### Funcionalidades principales del `<head>`

1. **Metadatos**:
    * Incluye información técnica como el conjunto de caracteres (`<meta charset="UTF-8">`), la descripción de la página (`<meta name="description" content="...">`), palabras clave, autor, etc.  
    * Metatags para viewport (útil en diseño responsivo):
         ```html
         <meta name="viewport" content="width=device-width, initial-scale=1.0">
         ```

2. **Título de la página**:  
   - Define el título que aparece en la pestaña del navegador:  
     ```html
     <title>Mi Página Web</title>
     ```

3. **Enlaces a recursos externos**:  
   - Hojas de estilo CSS:  
     ```html
     <link rel="stylesheet" href="estilos.css">
     ```  
   - Favicon (icono de la pestaña):  
     ```html
     <link rel="icon" href="favicon.ico">
     ```

4. **Scripts**:  
   - Aunque los scripts pueden ir en `<body>`, algunos se colocan en `<head>` (usando `defer` o `async` para no bloquear la carga).  

5. **Preconexiones y preloads**:  
   - Optimización de carga con:  
     ```html
     <link rel="preconnect" href="https://fonts.googleapis.com">  
     <link rel="preload" as="style" href="fuentes.css">
     ```

> [!NOTE]
> Elementos desglosados en: [01-head-elementos.md](./01-head-elementos.md).

### Diferencia con `<body>`:  
- **`<head>`**: Contiene información *sobre* el documento.  
- **`<body>`**: Contiene el contenido visible (texto, imágenes, etc.).
