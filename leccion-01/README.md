# Lección 1: ¿Qué es una página web y cómo mostramos texto en pantalla?

## 1. Concepto base (HTML)
- **Página web**: un documento de texto con instrucciones (HTML) que el navegador interpreta para mostrar contenido.
- **HTML** (*HyperText Markup Language*): lenguaje de marcas con “etiquetas” que le dicen al navegador qué es cada parte (títulos, párrafos, botones, etc.).

## 2. Ejemplo HTML puro (muy simple)
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mi primera página</title>
  </head>
  <body>
    <h1>Hola mundo</h1>
    <p>Este es mi primer texto en la web.</p>
  </body>
</html>
```
**Explicación rápida de las etiquetas usadas:**
- `<!DOCTYPE html>`: indica al navegador que es un documento HTML5.
- `<html>`: raíz de todo el documento.
- `<head>`: contiene meta-información (título, configuraciones), no se ve directamente.
- `<title>`: texto que aparece en la pestaña del navegador.
- `<body>`: todo lo que se muestra en pantalla.
- `<h1>`: encabezado principal (título grande).
- `<p>`: párrafo de texto.

## 3. Traducción a JSX
JSX es una sintaxis que se parece a HTML pero vive dentro de JavaScript.
```jsx
<h1>Hola mundo</h1>
<p>Este es mi primer texto en la web.</p>
```
**Nota:** En JSX ya no usamos `<!DOCTYPE>`, `<html>`, `<head>`, `<body>`. React “se encarga” de dónde insertar esto en la página real.

## 4. Uso dentro de un componente React
Un componente funcional es una función que devuelve JSX:
```jsx
// Un componente muy simple
function App() {
  return (
    <div>
      <h1>Hola mundo</h1>
      <p>Este es mi primer texto en la web.</p>
    </div>
  );
}

export default App;
```

## 5. Explicación línea por línea
- `function App() { ... }`: defines una función llamada `App`. En React, cada componente es una función (con mayúscula inicial).
- `return ( ... )`: lo que devuelves es JSX; React lo convierte en HTML real en el navegador.
- `<div> ... </div>`: contenedor genérico en HTML; en React lo usamos para agrupar elementos.
- `<h1>Hola mundo</h1>`: título principal.
- `<p>Este es mi primer texto en la web.</p>`: un párrafo de texto.
- `export default App;`: permite que otros archivos usen este componente.

## 6. Resumen corto
- HTML describe la estructura de una página mediante etiquetas.
- JSX se parece a HTML, pero está dentro de JavaScript y es lo que usamos en React.
- Un componente React es una función que devuelve JSX y React se encarga de mostrarlo en pantalla.

## 7. Ejercicio guiado
1. Crea un archivo `App.jsx`.
2. Escribe un componente funcional que devuelva:
   ```jsx
   <div>
     <h1>Tu nombre en grande</h1>
     <p>Una frase corta que te describa</p>
   </div>
   ```
3. Asegúrate de exportarlo con `export default App;`.
4. Imagina que React lo “inyecta” en la página: verías tu nombre como título y tu frase debajo como párrafo.

Cuando te sientas cómodo con esto, seguimos con la Lección 2: HTML mínimo (div, h1, p, button).
