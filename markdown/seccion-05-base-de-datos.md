# 📘 Sección 5 – La Bóveda de Datos

---

## 🧠 Objetivo de la Sección

Aprender qué es una base de datos, cómo funciona y cómo conectar tu backend para guardar y leer información usando SQL. Vas a instalar PostgreSQL (o SQLite), escribir tus primeros comandos y construir una conexión real con Node.js.

---

## 🧰 Herramientas que vas a usar

- PostgreSQL o SQLite (base de datos)
- Node.js + Express (ya instalados de secciones anteriores)
- Librería `pg` para conectarse a PostgreSQL

---

## 💾 ¿Qué es una base de datos?

Una base de datos es un sistema que guarda, organiza y permite consultar información de manera eficiente. Imagínala como un Excel con superpoderes, hecho para que los programas guarden y busquen datos sin errores.

### Tipos comunes

- **SQL (relacional)**: PostgreSQL, MySQL, SQLite  
- **NoSQL (documento/clave-valor)**: MongoDB, Redis  

> 🧠 *Ejemplo:* Una app de tareas necesita guardar tus tareas con campos como `nombre`, `fecha`, `completado`. Todo eso vive en una base de datos.

---

## 🧪 Actividad 1: Instala PostgreSQL

- Descarga desde: [https://www.postgresql.org/download/](https://www.postgresql.org/download/)
- Instala y recuerda tu contraseña
- Abre la terminal e ingresa a la consola:

```bash
psql -U postgres
````

* Crea una base de datos:

```sql
CREATE DATABASE tareasdb;
```

---

## 🧪 Actividad 2: Crea tu tabla de tareas

Dentro de `psql`, escribe:

```sql
CREATE TABLE tareas (
  id SERIAL PRIMARY KEY,
  titulo TEXT NOT NULL,
  completado BOOLEAN DEFAULT false
);
```

Verifica que existe:

```sql
\d tareas
```

Agrega datos:

```sql
INSERT INTO tareas (titulo) VALUES ('Aprender PostgreSQL');
```

---

## 🔗 Conecta tu backend a la base de datos

Instala el cliente de PostgreSQL:

```bash
npm install pg
```

Crea un archivo `db.js`:

```js
import pkg from 'pg';
const { Pool } = pkg;

const pool = new Pool({
  user: 'postgres',
  host: 'localhost',
  database: 'tareasdb',
  password: 'tu_contraseña',
  port: 5432,
});

export default pool;
```

---

## 🛠️ Usa la conexión en tu API

En `routes/tareas.js`:

```js
import express from 'express';
import db from './db.js';

const router = express.Router();

router.get('/tareas', async (req, res) => {
  const result = await db.query('SELECT * FROM tareas');
  res.json(result.rows);
});

router.post('/tareas', async (req, res) => {
  const { titulo } = req.body;
  await db.query('INSERT INTO tareas (titulo) VALUES ($1)', [titulo]);
  res.status(201).send('Tarea creada');
});

export default router;
```

---

## 🎮 Actividad Final: Construye tu CRUD

1. Agrega rutas para editar y borrar tareas
2. Usa `UPDATE` y `DELETE` en SQL
3. Agrega validaciones (no campos vacíos)
4. Prueba usando Postman o una app frontend simple

---

## ✅ Cierre de la Sección

> Ya aprendiste a crear, consultar y modificar datos reales desde tu backend. Eso es lo que hacen apps como Instagram, Gmail o cualquier servicio moderno.

¡Tienes el poder de construir tu propia base de datos ahora! 🎉

Siguiente parada: **Conectar todo para tener tu primera app full-stack.**

```

---

¿Te gustaría que también agreguemos visuales tipo ERD (diagramas de tablas y relaciones) o quieres pasar directo a la Sección 6?
```
