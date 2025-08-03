# 🎮 Sección 7 – Sube de Nivel con un Mini-Juego

---

## 🧠 Objetivo de la Sección

Construir un videojuego sencillo en el navegador usando JavaScript puro. Aprenderás el concepto del **game loop**, cómo manejar el estado del juego, y cómo crear interactividad básica. ¡Aquí tu código ya se vuelve divertido!

---

## 🎯 ¿Por qué hacer un videojuego?

- Porque es **divertido**
- Porque ejercitas **DOM**, **eventos**, **lógica**, **diseño visual**
- Porque aprendes a **pensar en estados** y reacciones del usuario

> Si puedes hacer un juego, puedes hacer cualquier app interactiva. Es un entrenamiento completo del cerebro coder.

---

## 🕹️ Conceptos Clave

### 🔄 Game Loop

Un bucle que se repite cada cierto tiempo y actualiza lo que pasa en pantalla:

```js
function loop() {
  actualizar();
  dibujar();
  requestAnimationFrame(loop);
}

loop(); // inicia el juego
````

### 🧠 Estado del juego

Guarda toda la información actual del juego en variables:

```js
let posicionJugador = { x: 5, y: 5 };
let puntos = 0;
let juegoTerminado = false;
```

Cada acción del jugador modifica ese estado, y cada "frame" del juego lo dibuja con base en ese estado.

---

## 🧪 Actividad Guiada: Juego de Memorama

Un juego clásico para ejercitar DOM, lógica y memoria.

### 🧰 HTML básico

```html
<div id="tablero"></div>

<script src="memorama.js"></script>
```

### 🎮 JavaScript básico

```js
const emojis = ['🍕', '🍕', '🎮', '🎮', '🐱', '🐱'];
let seleccionadas = [];
let bloqueadas = [];

function mezclar(array) {
  return array.sort(() => 0.5 - Math.random());
}

function dibujarTablero() {
  const tablero = document.getElementById('tablero');
  tablero.innerHTML = '';

  emojis.forEach((emoji, i) => {
    const carta = document.createElement('button');
    carta.textContent = seleccionadas.includes(i) || bloqueadas.includes(i) ? emoji : '❓';
    carta.onclick = () => seleccionar(i);
    tablero.appendChild(carta);
  });
}

function seleccionar(indice) {
  if (bloqueadas.includes(indice) || seleccionadas.includes(indice)) return;

  seleccionadas.push(indice);
  if (seleccionadas.length === 2) {
    const [i1, i2] = seleccionadas;
    if (emojis[i1] === emojis[i2]) {
      bloqueadas.push(i1, i2);
    }
    setTimeout(() => {
      seleccionadas = [];
      dibujarTablero();
    }, 1000);
  }
  dibujarTablero();
}

mezclar(emojis);
dibujarTablero();
```

🎉 ¡Ya tienes un mini-memorama funcional!

---

## 💡 Alternativa: Snake Clásico (Extra)

Si quieres un reto más visual y dinámico, intenta hacer el juego de la serpiente (Snake). Empieza dibujando con `<canvas>` y moviendo la serpiente con las flechas del teclado.

---

## 🧭 Sugerencias Visuales

* Usa emojis como sprites
* Dibuja tu propio diseño del juego antes de programarlo
* Agrega sonidos con `Audio()` para más realismo

---

## 🧰 Herramientas Opcionales

* `<canvas>` para dibujar juegos con píxeles
* `setInterval()` o `requestAnimationFrame()` para animaciones
* Sonidos `.mp3` con `<audio>` o JavaScript

---

## ✅ Desafío Final de la Sección

* Mejora el juego (puntuación, cronómetro, niveles)
* Crea tu propio estilo con CSS
* Publica tu juego en GitHub Pages o Netlify
* Rétate a ti mismo/a: ¿puedes hacer el juego sin copiar código?

---

## 🏁 Cierre de la Sección

> Crear un juego es una de las mejores formas de aprender a programar. Si llegaste hasta aquí, ya puedes crear experiencias interactivas y dinámicas. Ahora sí, estás hablando el idioma del navegador como un pro.

Prepárate: en la siguiente sección... ¡vas a construir tu primer proyecto real de principio a fin!

```

---

¿Quieres que prepare también la **Sección 8: Proyecto Final** con la misma estructura?
```
