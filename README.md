# Prueba Técnica Wizz Life

API REST para gestión de tareas de equipo.

# Tecnologías
- Python
- Django REST Framework
- PostgreSQL
- JWT Authentication
- Docker

# Cómo ejecutar localmente

1. Clonar el repositorio
2. Crear entorno virtual: "python -m venv venv"
3. Activar entorno virtual: "venv\Scripts\activate"
4. Instalar dependencias: "pip install -r requirements.txt"
5. Configurar variables de base de datos en "settings.py"
6. Correr migraciones: "py manage.py migrate"
7. Iniciar servidor: "py manage.py runserver"

# Cómo levantar con Docker

1. Levantar contenedor: "docker build -t wizz_life ."
2. Correr contenedor: "docker run -p 8000:8000 wizz_life"

# Endpoints

1. POST | /signup/ | Registro de usuario | No |
2. POST | /signin/ | Login, devuelve token JWT | No |
3. GET | /tasks/ | Listar tareas | Sí |
4. POST | /tasks/ | Crear tarea | Sí |
5. GET | /tasks/{id}/ | Detalle de tarea | Sí |
6. PATCH | /tasks/{id}/ | Actualizar tarea | Sí |
7. DELETE | /tasks/{id}/ | Eliminar tarea | Sí |

# Decisiones técnicas
- Se usó Django REST Framework por conocimiento y facilidad para construir APIs REST.
- Autenticación con JWT mediante simplejwt.
- Modelo de usuario personalizado extendiendo AbstractUser para mayor flexibilidad y escalabilidad.
- Apps separadas (users, tasks) para mejor separación de responsabilidades y escalabilidad.
