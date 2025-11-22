# Fullstack Django + ReactJS

Aplicación web full-stack desarrollada con Django (backend) y React (frontend).

## 🚀 Tecnologías

### Backend
- Django
- Django REST Framework
- Python

### Frontend
- React
- JavaScript/TypeScript

### API Endpoints
## Autenticación

POST /api/user/register/ - Registrar usuario
POST /api/token/ - Obtener tokens JWT
POST /api/token/refresh/ - Refrescar access token

## Notas (Requieren autenticación)
GET /api/notes/ - Listar notas del usuario
POST /api/notes/ - Crear nueva nota
DELETE /api/notes/delete/:id/ - Eliminar nota

## 📋 Requisitos Previos

- Python 3.8+
- Node.js 14+
- npm o yarn

## 🔧 Instalación

### 1. Clonar el repositorio

```bash
git clone <repository-url>
cd fullstack-django-reactjs

# backend

cd backend

# Crear y activar entorno virtual
python -m venv venv

# Windows
venv\Scripts\activate
# Linux/Mac
source venv/bin/activate

# Instalar dependencias
pip install django djangorestframework djangorestframework-simplejwt django-cors-headers psycopg2-binary python-dotenv

# Crear archivo .env
# Agregar las siguientes variables:
# DB_NAME=tu_base_de_datos
# DB_USER=tu_usuario
# DB_PWD=tu_contraseña
# DB_HOST=localhost
# DB_PORT=5432

# Ejecutar migraciones
python manage.py migrate

# Crear superusuario
python manage.py createsuperuser

# Iniciar servidor
python manage.py runserver

# frontend
cd frontend

# Instalar dependencias
npm install

# Crear archivo .env (opcional)
# VITE_API_URL=http://localhost:8000

# Iniciar servidor de desarrollo
npm run dev