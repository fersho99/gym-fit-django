# Gym Fit API

Backend del gimnasio Gym Fit con Django, Django REST Framework y JWT.
Unidad 3, Práctica 4 de Desarrollo Web Integral.

## Instalación

```bash
python -m venv venv
./venv/Scripts/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

## Endpoints principales

| Ruta | Descripción |
| --- | --- |
| `/swagger/` | Documentación interactiva de la API |
| `/admin/` | Panel de administración |
| `POST /api/v1/auth/token/` | Login con email y contraseña; devuelve los tokens |
| `POST /api/v1/auth/token/refresh/` | Renueva el token de acceso |
| `GET /api/v1/auth/me/` | Datos personales del usuario del token |
| `/api/v1/users/` | CRUD de usuarios, solo para administradores |

En Swagger, usa **Authorize** y escribe `Bearer <token de acceso>`. El token de acceso dura 30 minutos.

## Pruebas

```bash
python manage.py test
```
