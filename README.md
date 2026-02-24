# 🚀 Rails Postgres App

Este repositorio contiene el código para el desarrollo del proyecto. El entorno está configurado para funcionar de manera óptima bajo **WSL2 (Ubuntu en Windows)**, utilizando PostgreSQL como motor de base de datos.

---

## 🛠️ Pasos diarios para iniciar el entorno (Workflow en WSL)

Dado que los servicios de Linux se detienen al apagar Windows, sigue estos pasos cada vez que inicies una sesión de trabajo:

1. **Abre tu terminal de Ubuntu.**

2. **Navega a la carpeta del proyecto:**
```bash
cd ~/rails-postgres-app
```

3. **Abre el proyecto en Visual Studio Code:**
```bash
code .
```

4. **En la terminal integrada de VS Code, levanta el servicio de PostgreSQL:**
```bash
sudo service postgresql start
```

5. **Levanta el servidor web de Rails:**
```bash
rails server
```

6. **Accede desde el navegador (en Windows):**

Abre: http://localhost:3000

---

## ⚙️ Requisitos del Sistema

- Ruby: 3.3.6
- Framework: Ruby on Rails 8.x
- Base de datos: PostgreSQL 16+
- Entorno: WSL2 (Ubuntu 24.04 recomendado)

---

## 🗄️ Configuración de la Base de Datos

El proyecto utiliza dos bases de datos principales:

- rails_postgres_app_development
- rails_postgres_app_test

Si es la primera vez que configuras el proyecto o has reseteado el entorno, ejecuta:

```bash
rails db:create   # Crea las bases de datos definidas en database.yml
rails db:migrate  # Aplica las migraciones de las tablas
rails db:seed     # (Opcional) Carga datos de prueba iniciales
```

---

## 👁️ Visualización de Datos (VS Code)

Para ver las tablas de forma visual sin salir del editor:

1. Instala la extensión "Database Client"
2. Conecta con los siguientes parámetros:

- Host: localhost
- User: postgres
- Pass: 990113
- Port: 5432

---

## Comandos Rápidos (Cheat Sheet)

Generadores

- Crear un Scaffold (CRUD completo):
```bash
rails g scaffold Nombre modelo:string precio:decimal
```

- Crear un Modelo:
```bash
rails g model Nombre atributo:tipo
```

- Crear un Controlador:
```bash
rails g controller Nombres index show
```

Base de Datos

- Crear Migración:
```bash
rails g migration AddFieldToTable field:string
```

- Deshacer última migración:
```bash
rails db:rollback
```

- Estado de migraciones:
```bash
rails db:migrate:status
```

Consola y Pruebas

- Consola interactiva:
```bash
rails c
```

- Ejecutar pruebas:
```bash
rails test
```

---

Notas: adapta las rutas y credenciales según tu entorno local y las variables de `config/database.yml` si usas usuarios/puertos/contraseñas distintos.