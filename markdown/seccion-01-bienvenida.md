# 📘 Sección 1 – Bienvenido a la Máquina

---

## 🧠 Objetivo de la Sección

Aprender qué es una computadora, cómo funciona la web y cómo escribir tu primer programa. Esta sección marca el inicio de tu camino como programador. Vas a instalar tus herramientas, entender cómo se comunican las computadoras, y escribir tu primer "Hola Mundo" como todo maestro del teclado.

---

## 🧰 Herramientas que vas a usar

* Visual Studio Code (editor de código)
* Git (control de versiones)
* Terminal (Command Prompt, PowerShell, o Bash)
* Navegador (Chrome o Firefox)

> Si no tienes alguno de estos, no te preocupes. En esta sección también aprenderás a instalarlos paso a paso.

---

## 💡 ¿Qué es una computadora?

Una computadora es una máquina que sigue instrucciones al pie de la letra. Todo lo que ves en la pantalla —videos, redes, juegos— es el resultado de miles de instrucciones ejecutándose a toda velocidad.

### Componentes básicos:

* **CPU**: el cerebro que procesa todo
* **RAM**: la memoria temporal, como tu libreta de apuntes
* **Disco Duro/SSD**: donde se guarda todo a largo plazo
* **Periféricos**: teclado, mouse, pantalla, conexión a internet

> 🧠 **Analogía**: Tu compu es como una cocina. El CPU es el chef, la RAM es la mesa, el disco es la alacena y el Internet es como pedir ingredientes por Uber Eats.

### 📝 Ejercicio

Dibuja un diagrama de una computadora con los elementos principales. Usa colores y pon ejemplos personales (por ejemplo: "mi compu tiene 8 GB de RAM")

---

## 🌐 ¿Cómo funciona la web?

Cuando visitas una página web, tu compu (cliente) le pide algo a otra compu (servidor). Este modelo se llama **cliente-servidor**.

```
[ Tú (cliente) ] <--- petición --- [ Servidor ]
                   ---> respuesta --->
```

Tu navegador manda una petición (como "muéstrame el perfil de mi compa") y el servidor responde con los archivos (HTML, CSS, JS).

✅ El navegador interpreta esos archivos.
✅ Cada clic puede generar nuevas peticiones.
✅ Esto pasa en milisegundos.

### 🎨 Actividad Visual

Haz un dibujo tipo historieta de tú navegando a una página web. ¿Qué le pides al servidor? ¿Qué te responde? ¿Cómo lo ves tú?

---

## 💻 Actividad 1: Tu primer Hola Mundo

1. Abre Visual Studio Code.
2. Crea una carpeta llamada `mi-primera-web`
3. Dentro, crea un archivo `index.html`
4. Pega este código:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Mi Primer Página</title>
  </head>
  <body>
    <h1>¡Hola, Mundo!</h1>
    <script>
      console.log("¡JavaScript también dice hola!");
    </script>
  </body>
</html>
```

5. Guárdalo y ábrelo con doble clic en tu navegador.
6. Abre la consola (clic derecho > Inspeccionar > Consola) y verás el mensaje de JS.

---

## 🎨 Actividad 2: Personaliza tu página

* Cambia el `<h1>` por tu nombre o frase favorita.
* Agrega una imagen usando:

```html
<img src="https://placekitten.com/300/200" />
```

* Agrega un párrafo con algo que te guste usando `<p>`
* Usa listas con `<ul>` y `<li>` para nombrar 3 cosas que te gustaría aprender.

---

## 🧪 Actividad 3: Experimenta con JavaScript

Dentro del mismo archivo `index.html`, abajo del `<script>`, escribe:

```js
alert("¡Bienvenido a mi sitio!");
```

* Vuelve a abrir el archivo y verás un mensaje emergente.
* Cambia el mensaje a algo distinto y prueba otra vez.

### Ahora crea una variable en JavaScript:

```js
const nombre = "Lupita";
console.log("Hola, " + nombre);
```

---

## 🧭 Mapa Mental Visual

```
Computadora
├── CPU (procesa)
├── RAM (guarda temporal)
├── Disco (guarda permanente)
└── Entradas/Salidas (teclado, red)

Web
├── Cliente (navegador)
├── Petición (GET, POST)
├── Servidor (responde)
└── Archivos (HTML, CSS, JS)
```

---

## 📋 Tarea Final de la Sección

* Escribe un resumen de lo que aprendiste.
* Guarda tu archivo y crea una carpeta de respaldo.
* Si sabes usar GitHub, sube ahí tu código. Si no, ¡no te preocupes! Aprende eso en otra sección.
* Dibuja o esquematiza el proceso de visitar una página web.

---

## ✅ Cierre de la Sección

Si llegaste hasta aquí, ya entendiste cómo piensa una computadora, qué pasa cuando visitas una página web y escribiste tu primer código. No es magia. Es lógica, instrucciones y muchas ganas.

Guarda tu archivo, siéntete orgulloso, y prepárate para la siguiente aventura: **hablar con la computadora usando JavaScript**.

🎉 ¡Nos vemos en la Sección 2!
