# 🚀 Nombre de tu Proyecto

Este repositorio contiene el código para la prueba técnica. A continuación, se detallan las instrucciones para levantar el entorno de desarrollo, configurado para funcionar de manera óptima bajo WSL (Ubuntu en Windows).

---

## 🛠️ Pasos diarios para iniciar el entorno (Workflow en WSL)

Dado que los servicios de Linux se detienen al apagar Windows, sigue estos pasos cada vez que enciendas la computadora para retomar el trabajo:

1. Abre tu terminal de Ubuntu.

2. Navega a la carpeta del proyecto:
   ```bash
   cd ruta/hacia/el/proyecto (prueba_tecnica)
   ```
3. Abre el proyecto en Visual Studio Code:
   ```bash
   code .
   ```
4. En la terminal integrada de VS Code, levanta el servicio de PostgreSQL:
   ```bash
   sudo service postgresql start
   ```
5. Levanta el servidor web de Rails:
   ```bash
   rails server
   ```
6. Abre tu navegador web en Windows y visita: http://localhost:3000

---

## ⚙️ Requisitos del Sistema

* **Ruby:** 3.3.6
* **Framework:** Ruby on Rails
* **Base de datos:** PostgreSQL
* **Entorno:** Linux / macOS / WSL2 en Windows

## 🗄️ Configuración de la Base de Datos (Primera vez)

Asegúrate de tener el servicio de PostgreSQL corriendo y tu archivo `config/database.yml` configurado con tus credenciales. Luego ejecuta:

```bash
rails db:create
rails db:migrate
rails db:seed
```

## 🧪 Pruebas (Test Suite)

Para ejecutar la suite de pruebas del proyecto:

```bash
rails test
```