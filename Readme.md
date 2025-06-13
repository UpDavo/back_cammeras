# Cammeras Backend

Backend en Django + Django REST Framework para gestión de usuarios, roles y autenticación JWT. Incluye documentación automática de la API y estructura lista para crecer.

---

## Características principales

- Autenticación JWT (SimpleJWT)
- Gestión de usuarios y roles
- Permisos personalizados
- Documentación automática en `/docs/` (Swagger UI) y `/redoc/`
- Estructura modular y escalable
- Configuración por entorno (`.env`)
- Compatible con MySQL y PostgreSQL

---

## Instalación rápida

1. Clona el repositorio y entra a la carpeta:
   ```zsh
git clone <tu-repo-url>
cd back_cammeras
```
2. Crea y activa un entorno virtual:
   ```zsh
python -m venv env
source env/bin/activate  # Mac/Linux
# o
.\env\Scripts\activate  # Windows
```
3. Instala dependencias:
   ```zsh
pip install -r requirements.txt
```
4. Configura tu archivo `.env`:
   ```env
SECRET_KEY=tu-clave
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
DB_NAME=cammeras
DB_USER=usuario
DB_PASSWORD=contraseña
DB_HOST=localhost
DB_PORT=3306
```
5. Aplica migraciones:
   ```zsh
python manage.py migrate
```
6. Crea un superusuario:
   ```zsh
python manage.py createsuperuser
```
7. Ejecuta el servidor:
   ```zsh
python manage.py runserver
```

---

## Endpoints principales

| Método | Endpoint           | Descripción                  |
|--------|--------------------|------------------------------|
| POST   | /auth/login/       | Login de usuario             |
| POST   | /auth/register/    | Registro de usuario          |
| POST   | /auth/logout/      | Logout de usuario            |
| GET    | /auth/user/        | Perfil usuario autenticado   |
| GET    | /auth/users-list/  | Listar usuarios (admin)      |
| CRUD   | /auth/roles/       | Gestión de roles             |
| CRUD   | /auth/permissions/ | Gestión de permisos          |
| GET    | /docs/             | Documentación Swagger UI     |
| GET    | /redoc/            | Documentación ReDoc          |

---

## Documentación automática

- Accede a la documentación interactiva en `/docs/` (Swagger UI) o `/redoc/`.
- El esquema OpenAPI está disponible en `/schema/`.

---

## Tecnologías

- Django 5+
- Django REST Framework
- drf-spectacular (OpenAPI/Swagger)
- SimpleJWT
- MySQL o PostgreSQL

---

## Autor

Desarrollado por Anthony Villegas