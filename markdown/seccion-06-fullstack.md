# 📘 Sección 6 – Fusión Full-stack

---

## 🧠 Objetivo de la Sección

Aprender a conectar el frontend con el backend usando `fetch`, peticiones HTTP y el formato JSON. Vas a construir una pequeña app con autenticación simple y un bloc de notas personal.

---

## 🧰 Herramientas que vas a usar

- HTML + JS (Frontend)
- Node.js + Express (Backend)
- Base de datos PostgreSQL o SQLite
- `fetch()` (para hacer peticiones desde el navegador)
- JSON (formato para enviar/recibir datos)

---

## 🔌 ¿Qué significa “Full-stack”?

Una app **Full-stack** tiene:

- **Frontend**: lo que ves en pantalla (HTML, CSS, JS)
- **Backend**: código que corre en el servidor (Express, Node.js)
- **Base de Datos**: donde se guarda la información (PostgreSQL)

> Cuando conectas los tres, ya puedes crear una app funcional completa. 🧠✨

---

## 📬 ¿Qué es una petición HTTP?

Una forma en que el navegador y el servidor se comunican. Las más comunes:

- `GET`: obtener información  
- `POST`: enviar información  
- `PUT`: actualizar  
- `DELETE`: borrar  

Y los datos van en formato **JSON**, así:

```json
{
  "usuario": "lupita",
  "nota": "No olvidar practicar JavaScript"
}
````

---

## 🛠️ Actividad 1: Conecta el Frontend con Fetch

Crea un archivo `frontend.html`:

```html
<h2>Bloc de Notas</h2>
<input id="nota" placeholder="Escribe tu nota" />
<button onclick="guardarNota()">Guardar</button>

<script>
  function guardarNota() {
    const texto = document.getElementById('nota').value;

    fetch('http://localhost:3000/notas', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ nota: texto })
    })
    .then(res => res.text())
    .then(data => alert(data));
  }
</script>
```

---

## 🛠️ Actividad 2: Recibe la petición en tu servidor

Crea la ruta en tu backend `notas.js`:

```js
import express from 'express';
import db from './db.js';

const router = express.Router();

router.post('/notas', async (req, res) => {
  const { nota } = req.body;
  await db.query('INSERT INTO notas (contenido) VALUES ($1)', [nota]);
  res.send('Nota guardada correctamente');
});

router.get('/notas', async (req, res) => {
  const resultado = await db.query('SELECT * FROM notas');
  res.json(resultado.rows);
});

export default router;
```

Y en tu `server.js` asegúrate de usar:

```js
app.use(express.json()); // para que lea JSON
app.use('/notas', notasRouter);
```

---

## 🧪 Actividad 3: App de Login Básico

Simula un login sin base de datos todavía:

### HTML

```html
<h2>Login</h2>
<input id="usuario" placeholder="Usuario" />
<input id="password" type="password" placeholder="Contraseña" />
<button onclick="login()">Entrar</button>

<script>
  function login() {
    const usuario = document.getElementById('usuario').value;
    const password = document.getElementById('password').value;

    fetch('http://localhost:3000/login', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ usuario, password })
    })
    .then(res => res.json())
    .then(data => alert(data.mensaje));
  }
</script>
```

### Backend

```js
app.post('/login', (req, res) => {
  const { usuario, password } = req.body;

  if (usuario === 'admin' && password === '1234') {
    res.json({ mensaje: 'Bienvenido, admin' });
  } else {
    res.json({ mensaje: 'Credenciales incorrectas' });
  }
});
```

---

## 🎯 Desafío Final: App Bloc de Notas Completa

Tu reto es crear una app donde:

* El usuario pueda “loguearse”
* Una vez dentro, vea sus notas guardadas
* Pueda crear nuevas notas
* Todo usando `fetch`, rutas y base de datos

---

## ✅ Cierre de la Sección

> ¡Felicidades! Ya sabes cómo unir todas las piezas para tener una aplicación que se comunica entre el navegador, el servidor y la base de datos. Esto ya es nivel pro.

Prepárate, porque lo que viene ahora es... **¡construir tu primer videojuego web!**

```

---

¿Quieres que el siguiente también lo prepare ya en este mismo formato para el juego tipo Snake o Clicker?
```
