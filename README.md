# Exposición: Objetos predefinidos de JavaScript

## 1. ¿Qué es JavaScript?

JavaScript es un lenguaje de programación que se usa principalmente para agregar interactividad a las páginas web. Por ejemplo, permite mostrar mensajes, realizar cálculos, consultar la fecha y modificar el contenido de una página.

En esta exposición veremos 11 herramientas: `Number`, `Math`, `Boolean`, `Date`, intervalos de tiempo, `String`, `Location`, `Navigator`, `Document`, `Window` y `Frame`.

## 2. JavaScript puro y HTML

**JavaScript puro**, también llamado *Vanilla JavaScript*, significa usar JavaScript sin instalar librerías o frameworks adicionales.

- **HTML** organiza el contenido de la página.
- **JavaScript** realiza operaciones y puede cambiar el contenido.
- Algunas herramientas, como `Location`, `Navigator`, `Document`, `Window` y los `Frame`, pertenecen al entorno del navegador, no al núcleo del lenguaje ECMAScript.

## 3. Ejemplos de cada tema

### 1. Number

Sirve para convertir valores a números y trabajar con cantidades.

```javascript
let numero = Number("10");
console.log(numero + 5); // Muestra 15
```

### 2. Math

Incluye funciones matemáticas, como calcular una raíz cuadrada.

```javascript
let raiz = Math.sqrt(25);
console.log(raiz); // Muestra 5
```

### 3. Boolean

Representa un valor verdadero (`true`) o falso (`false`).

```javascript
let esMayor = Boolean(10 > 5);
console.log(esMayor); // Muestra true
```

### 4. Date

Permite consultar la fecha y la hora.

```javascript
let fecha = new Date();
console.log(fecha); // Muestra la fecha y hora actuales
```

### 5. Intervalos de tiempo

`setInterval()` repite una función cada cierto tiempo. El tiempo se indica en milisegundos; 2000 milisegundos equivalen a 2 segundos.

```javascript
let intervalo = setInterval(function() {
    console.log("Han pasado 2 segundos");
}, 2000);

// Para detenerlo cuando sea necesario:
// clearInterval(intervalo);
```

### 6. String

Sirve para guardar y manipular texto.

```javascript
let nombre = String("Carlos");
console.log(nombre.toUpperCase()); // Muestra CARLOS
```

### 7. Location

Permite consultar la dirección web actual.

```javascript
console.log(location.href); // Muestra la URL actual
```

### 8. Navigator

Permite consultar información del navegador, como el idioma configurado.

```javascript
console.log(navigator.language); // Por ejemplo, es-CO
```

### 9. Document

Representa el documento HTML y permite modificar su contenido.

```javascript
document.getElementById("resultado").textContent = "Hola, mundo";
```

Este ejemplo necesita que exista en el HTML un elemento con `id="resultado"`.

### 10. Window

Representa la ventana o pestaña del navegador. Por ejemplo, permite mostrar una alerta.

```javascript
window.alert("Bienvenidos a mi ejemplo");
```

### 11. Frame (iframe)

Un `iframe` permite mostrar otra página o documento dentro de la página actual. Cada marco tiene su propio contexto de ventana.

```html
<iframe id="marco" src="about:blank"></iframe>

<script>
    let marco = document.getElementById("marco");
    console.log(marco.contentWindow);
</script>
```

En este ejemplo se consulta la ventana del marco interno. El acceso a su contenido puede estar limitado por las reglas de seguridad del navegador.

## 4. Ejemplo completo para ejecutar

Guarda el siguiente código en un archivo llamado `index.html`. Incluye HTML para mostrar los resultados y JavaScript puro para trabajar con los temas de la exposición.


<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Objetos predefinidos de JavaScript</title>
</head>
<body>
    <h1>Objetos predefinidos de JavaScript</h1>
    <p id="resultado"></p>

    <iframe id="marco" src="about:blank" title="Marco de ejemplo"></iframe>

    <script>
        // 1. Number: convierte texto a número
        let numero = Number("10");

        // 2. Math: calcula la raíz cuadrada
        let raiz = Math.sqrt(25);

        // 3. Boolean: guarda un valor verdadero o falso
        let respuesta = Boolean(true);

        // 4. Date: obtiene la fecha y hora actuales
        let fecha = new Date();

        // 5. Intervalo: muestra un mensaje cada 2 segundos
        let intervalo = setInterval(function() {
            console.log("Han pasado 2 segundos");
        }, 2000);

        // 6. String: guarda un texto
        let nombre = String("Carlos");

        // 7. Location: obtiene la dirección de la página
        let direccion = location.href;

        // 8. Navigator: obtiene el idioma del navegador
        let idioma = navigator.language;

        // 9. Document: muestra los resultados en la página
        document.getElementById("resultado").innerHTML =
            "Number: " + numero + "<br>" +
            "Math (raíz cuadrada de 25): " + raiz + "<br>" +
            "Boolean: " + respuesta + "<br>" +
            "Date: " + fecha + "<br>" +
            "String: " + nombre.toUpperCase() + "<br>" +
            "Location: " + direccion + "<br>" +
            "Navigator (idioma): " + idioma;

        // 10. Window: muestra una alerta
        window.alert("Bienvenidos a mi ejemplo");

        // 11. Frame: consulta la ventana del iframe
        let marco = document.getElementById("marco");
        console.log("Ventana del frame:", marco.contentWindow);
    </script>
</body>
</html>
```

## 5. ¿Cómo ejecutar el ejemplo?

1. Abre Visual Studio Code.
2. Crea un archivo llamado `index.html`.
3. Copia el ejemplo completo y guarda el archivo.
4. Abre `index.html` en un navegador, como Chrome.
5. Cierra el mensaje de bienvenida.
6. Los resultados aparecerán en la página.
7. Para ver los mensajes del intervalo y la información del `Frame`, presiona `F12` y abre la pestaña **Console**.

## 6. Resumen de los 11 temas

| Tema | ¿Para qué sirve? |
|---|---|
| `Number` | Convertir y trabajar con números. |
| `Math` | Realizar operaciones matemáticas. |
| `Boolean` | Representar valores verdaderos o falsos. |
| `Date` | Trabajar con fechas y horas. |
| `setInterval()` | Repetir una función cada cierto tiempo. |
| `String` | Guardar y manipular texto. |
| `Location` | Consultar o cambiar la dirección de la página. |
| `Navigator` | Consultar información del navegador. |
| `Document` | Leer y modificar el contenido HTML. |
| `Window` | Trabajar con la ventana o pestaña del navegador. |
| `Frame` | Trabajar con marcos internos creados con `iframe`. |

## 7. Conclusión para la exposición

Los objetos y las herramientas predefinidas de JavaScript facilitan muchas tareas comunes. Algunos sirven para hacer cálculos y manejar datos, mientras que otros permiten interactuar con el navegador y modificar una página web. Al usarlos juntos, podemos crear páginas más dinámicas sin instalar librerías adicionales.

## 8. Frase corta para decir en clase

“Este ejemplo está hecho con JavaScript puro y HTML. HTML muestra la estructura de la página y JavaScript utiliza sus objetos y herramientas para hacer cálculos, mostrar la fecha, consultar el navegador y cambiar el contenido de la página.”
