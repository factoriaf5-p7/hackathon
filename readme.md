# hackathon EVENTS

## Descripción

La empresa GAME-R-US©️ quiere probar nuevas utilidades en su web para ello os propone los siguientes retos. Cada reto tiene un valor sobre 5 puntos. El equipo que consiga más puntos será el ganador y recibirá una dulce recompensa!!!.

## Instrucciones

Cada equipo deberá hacer un commit por cada reto resuelto. Se contarán solo los commits dentro del repositorio de github.

## RETO 1: 5 PTOS.

Desarrolla el prototipo de un juego muy simple en JavaScript. Os proporcionan el código HTML i CSS, y tenéis que implementar las reglas siguientes:

El jugador tiene 3 segundos para hacer clic sobre el círculo de color rojo, que será seleccionado aleatoriamente.
Una vez que se haya agotado el tiempo el círculo se intercambia con otro.
Si se hace clic dentro del tiempo indicado muestra una alerta con el mensaje: “Has ganado”.

```css

  div>div {
    width: 100px;
    height: 100px;
    border: 1px solid red;
    display: inline-block;
    border-radius: 50px;
  }

  .target {
    background-color: red;
  }
```

```html
<div>
  <div id="1"></div>
  <div id="2"></div>
  <div id="3"></div>
</div>

<div>
  <div id="4"></div>
  <div id="5"></div>
  <div id="6"></div>
</div>

<div>
  <div id="7"></div>
  <div id="8"></div>
  <div id="9"></div>
</div>
```

**Nota**: *quizás necesites utilizar la propiedad className de un elemento*

**Tips:** El motor del juego es una función con un temporizador setTimeout que llamaría recursivamente a la misma función cada 3s.

## RETO 2: 3 PTOS

Crea un sistema de detección que permita cambiar el color de un elemento según la tecla que se presione:

Tecla R: red
Tecla Y: yellow
Tecla W: white
Os proporcionan el siguiente código HTML i CSS:

```css

  div {
    width: 100px;
    height: 100px;
    border: 1px solid black;
  }

  .white {
    background-color: white;
  }

  .red {
    background-color: red;
  }

  .yellow {
    background-color: yellow;
  }
```

```html
<div id="tests" tabindex=1></div>
```

Notas:

Fijaos que se ha utilizado el atributo `tabindex=1`: eso permite que el elemento div sea seleccionable y sea capaz de detectar los eventos del teclado.
Para acceder a las clases que dan estilo a un elemento de HTML se utiliza la propiedad `className` del elemento. Esta propiedad contiene una cadena de texto que puede ser modificada para reemplazar las clases, añadir nuevas o eliminarlas. Por tanto, para cambiar el color del contenedor sólo hace falta reemplazar el `className` del elemento por el que corresponda.

## RETO 3: 2 PTOS

Crea un formulario de contacto preparado para añadir un sistema de validación propio que se activará cuando se envíe el formulario.

Sólo necesitan una función que muestre una alerta, que será sustituida por el código de validación en una fase posterior. El código proporcionado és el seguiente:

```html
<form id="contacte" method="post">
    <label>Nombre:<input type="text" name="name"/></label><br>
    <label>Correo:<input type="text" name="mail"/></label><br>
    <label>Mensaje:</label><br><textarea name="message"></textarea><br>
    <button>Enviar</button>
</form>
```

## RETO 4: 2 PTOS

En este caso GAME-R-US ©️ quiere añadir un reproductor de audio en su sitio web y necesitan poder controlar que cuando se pausa una canción se muestre un mensaje personalizado. Es decir, tenéis que desarrollar un sistema que muestre una alerta cuando se pause la canción que se está reproduciendo. El código proporcionado es el siguiente:

```html
<audio id="reproductor" controls src = "https://bcncodes.surge.sh/Batty-McFaddin-slower.mp3"></audio>
```

## RETO 5: 3 PTOS

Se pide desarrollar un sistema para controlar los cambios en el almacenamiento de datos local. Se tiene que detectar que cuando se produzca un cambio en el almacenamiento (localstorage) se muestre un aviso en el resto de pestañas abiertas.
Para hacer las pruebas sólo se necesita implementar el código necesario para detectar el evento y que muestre una alerta. Podemos utilizar el siguiente código para guardar los datos en el almacen:

```javascript
let addButton = document.getElementById('addButton');

addButton.addEventListener('click', function() {
  localStorage.setItem(keywordElement.value, valElement.value);
});
```

y el código HTML es el siguiente:

```html
<input placeholder="Introduce una clave" id="keyword"/><input placeholder="Introduce un valor" id="value"/><button id="addButton">Add</button>
```

Nota: la detección de cambios en el almacén de datos no se dispara en la pestaña donde se producen los cambios!!!!
