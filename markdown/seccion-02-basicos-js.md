# 📘 Sección 2 – Aprende a Hablar Código

---

## 🧠 Objetivo de la Sección

Aprender los fundamentos del lenguaje de programación JavaScript: variables, funciones, ciclos, y estructuras de datos. Vas a escribir código que piensa, que repite tareas, y que reacciona a tus decisiones. Esta sección es el primer paso real para volverte un programador.

---

## 📈 Conceptos Clave

### 🔢 Variables: Guardando información

Una variable es una cajita donde guardas un valor.

```js
let nombre = "Lupita";
const edad = 19;
```

* `let` permite cambiar el valor.
* `const` es una variable que no cambia.

### ⚙️ Funciones: Bloques reutilizables

Una función es un conjunto de instrucciones con nombre propio.

```js
function saludar(nombre) {
  console.log("Hola, " + nombre);
}

saludar("Luis");
```

### ⟳ Ciclos: Repetir sin copiar y pegar

```js
for (let i = 1; i <= 5; i++) {
  console.log("Repetición " + i);
}
```

Los ciclos automatizan tareas repetitivas. Puedes hacer listas, tablas, animaciones y más.

---

## 📊 Estructuras de Datos

### 🛋️ Arreglos

```js
const frutas = ["manzana", "plátano", "sandía"];
console.log(frutas[1]); // plátano
```

### 🔹 Objetos

```js
const persona = {
  nombre: "Pedro",
  edad: 28,
  ciudad: "Monterrey"
};

console.log(persona.nombre);
```

### 🧩 Mapas (nivel intermedio)

```js
const mapa = new Map();
mapa.set("clave", "valor");
console.log(mapa.get("clave"));
```

---

## 📚 Actividad 1: Mini Calculadora

1. Crea un archivo `calculadora.html`
2. Agrega un formulario con dos inputs numéricos y botones para sumar, restar, multiplicar y dividir.
3. Escribe funciones en JavaScript que hagan las operaciones.

```html
<input type="number" id="a">
<input type="number" id="b">
<button onclick="sumar()">+</button>
<p id="resultado"></p>

<script>
  function sumar() {
    const a = Number(document.getElementById("a").value);
    const b = Number(document.getElementById("b").value);
    document.getElementById("resultado").innerText = a + b;
  }
</script>
```

---

## 🎮 Actividad 2: Mini Quiz Interactivo

1. Crea un archivo `quiz.html`
2. Escribe 3 preguntas y botones de respuesta.
3. Usa condiciones (`if`) para decir si está bien o mal.

```html
<p>¿Cuál es la capital de México?</p>
<button onclick="verificar('CDMX')">CDMX</button>
<button onclick="verificar('Guadalajara')">Guadalajara</button>
<p id="feedback"></p>

<script>
  function verificar(respuesta) {
    if (respuesta === "CDMX") {
      document.getElementById("feedback").innerText = "¡Correcto!";
    } else {
      document.getElementById("feedback").innerText = "Intenta otra vez.";
    }
  }
</script>
```

---

## 📓 Tarea Final de la Sección

* Crea un archivo que combine todo: inputs, funciones y resultados.
* Usa una estructura de objeto para guardar preguntas y respuestas.
* Escribe 3 funciones nuevas de utilidad.
* Guarda todo como `reto-seccion-2.html`

---

## ✅ Cierre de la Sección

Ya sabes declarar variables, escribir funciones, usar ciclos, y construir estructuras de datos como arreglos y objetos. Eso es TODO lo que necesitas para hacer programas reales.

Lo que sigue es **hacer que tu código interactúe con la página**, darle vida, y controlar eventos. Eso lo ves en la siguiente sección: **Hazlo Moverse**.
