# 📘 Sección 4 – El Cerebro del Backend

---

## 🧠 Objetivo de la Sección

Comprender qué es un servidor, cómo funciona Node.js y Express, y construir tu primera API REST que responda a peticiones desde el navegador o desde tu frontend.

---

## 🛠️ Herramientas que usarás

* Node.js (JavaScript en el servidor)
* Express.js (framework para crear APIs)
* Postman o navegador para hacer peticiones
* Editor de código (VSCode)
* Terminal

---

## 📄 Conceptos Clave

### ¿Qué es un servidor?

Un servidor es una computadora que está esperando a recibir peticiones y responder con datos. Las páginas web, apps y juegos online se conectan con servidores todo el tiempo.

> 🧠 *Piensa en el servidor como un mesero digital. Le haces un pedido (petición HTTP) y él te trae el platillo (respuesta con datos).*

### Peticiones HTTP

* `GET` → pedir información
* `POST` → enviar información
* `PUT` → actualizar información
* `DELETE` → borrar información

---

## 💻 Actividad 1: Tu primer servidor con Node.js

1. Abre VSCode y una terminal
2. Crea una carpeta llamada `mi-api`
3. Ejecuta esto para iniciar un proyecto:

```bash
npm init -y
```

4. Instala Express:

```bash
npm install express
```

5. Crea un archivo llamado `index.js` y escribe esto:

```js
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => {
  res.send('Hola desde el backend!')
})

app.listen(port, () => {
  console.log(`Servidor escuchando en http://localhost:${port}`)
})
```

6. Corre el servidor:

```bash
node index.js
```

7. Abre tu navegador y ve a `http://localhost:3000`

---

## 🎓 Actividad 2: Agrega más rutas a tu API

Modifica tu `index.js` para que responda a diferentes rutas:

```js
app.get('/saludo', (req, res) => {
  res.send('Hola programador!')
```
