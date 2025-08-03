# 📘 Sección 3 – Haz que se Mueva

---

## 🧠 Objetivo de la Sección

Aprenderás a hacer que tu página web cobre vida. Vamos a manipular el contenido con JavaScript, reaccionar a eventos como clics y tecleos, y darle estilo usando CSS. Esta sección te permite transformar una página estática en una experiencia interactiva.

---

## 🛠 Herramientas necesarias

* Tu navegador favorito
* Visual Studio Code
* Archivos HTML, CSS y JS

---

## 💡 Concepto Clave: El DOM

El **DOM** (Document Object Model) es como el esqueleto vivo de tu página. Cada etiqueta HTML se convierte en un "nodo" que puedes modificar desde JavaScript.

> 🔎 Piensa en el DOM como un árbol. Puedes moverte entre ramas (elementos), cortar hojas (borrarlos), o pintar ramas (modificarlos).

### Ejemplo:

```html
<h1 id="titulo">Hola</h1>
<script>
  const t = document.getElementById("titulo");
  t.innerText = "Hola desde JS";
</script>
```

---

## 🌈 Estilos con CSS

CSS (Cascading Style Sheets) permite que tu página se vea bonita. Puedes cambiar colores, tamaños, posiciones y mucho más.

### Ejemplo:

```html
<style>
  body { background: #f0f0f0; font-family: sans-serif; }
  h1 { color: tomato; }
</style>
```

---

## ✨ Eventos: Dale vida a tu sitio

Puedes escuchar cosas como:

* Clics (`onclick`)
* Tecleos (`onkeydown`)
* Movimiento del mouse

### Ejemplo:

```html
<button id="btn">Haz clic</button>
<script>
  document.getElementById("btn").onclick = function() {
    alert("¡Clic detectado!");
  };
</script>
```

---

## 🚀 Actividad 1: Interactúa con el DOM

1. Crea un archivo `dom.html`
2. Agrega un `h2` con un ID y un botón
3. Al hacer clic en el botón, cambia el texto del `h2`

```html
<h2 id="saludo">Hola, visitante</h2>
<button onclick="document.getElementById('saludo').innerText = 'Hola, hacker'">
  Cambiar texto
</button>
```

---

## 🎨 Actividad 2: Estilo Dinámico

1. Agrega una hoja de estilos interna
2. Al hacer clic en un botón, cambia el color de fondo de la página

```html
<script>
  function cambiarColor() {
    document.body.style.backgroundColor = "#222";
  }
</script>
<button onclick="cambiarColor()">Modo oscuro</button>
```

---

## 🔮 Actividad 3: Mini Clicker Game

1. Crea una variable `let puntos = 0`
2. Muestra un botón y un contador
3. Cada clic suma 1 punto

```html
<p>Has hecho <span id="contador">0</span> clics</p>
<button onclick="sumar()">Haz clic</button>
<script>
  let puntos = 0;
  function sumar() {
    puntos++;
    document.getElementById("contador").innerText = puntos;
  }
</script>
```

---

## 📚 Proyecto de Cierre: To-Do List Interactiva
