# Cammeras Backend

API sencilla en Django REST Framework para usuarios, roles y autenticación JWT.

- Documentación completa y pruebas en `/docs/` (Swagger UI) y `/redoc/`.
- Configuración por entorno (`.env`).
- Compatible con MySQL y PostgreSQL.

## Instalación

```zsh
git clone
cd back_cammeras
python -m venv env
source env/bin/activate  # o .\env\Scripts\activate en Windows
pip install -r requirements.txt
cp .env.example .env  # o crea tu .env
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Consulta `/docs/` para ver todos los endpoints, parámetros y respuestas.