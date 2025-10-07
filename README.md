# Django + React (Function-Based Views Example)

This is a minimal project showing how to connect **Django (backend)** and **React (frontend)**.

## Backend (Django)
1. Install dependencies:
   ```bash
   pip install django djangorestframework django-cors-headers
   ```

2. Run migrations:
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

3. Create a superuser (optional):
   ```bash
   python manage.py createsuperuser
   ```

4. Start the server:
   ```bash
   python manage.py runserver
   ```

Your API is now live at: `http://127.0.0.1:8000/api/products/`

## Frontend (React + Vite)
1. Go to `frontend/` and install dependencies:
   ```bash
   npm install
   ```

2. Start the React dev server:
   ```bash
   npm run dev
   ```

3. Open browser at: `http://127.0.0.1:5173`

## How It Works
- Django serves the API endpoint using a **function-based view** (`product_list`).
- React fetches this data with **Axios** and displays it.

## Notes
- Ensure both backend (`8000`) and frontend (`5173`) are running.
- `django-cors-headers` is enabled for all origins in development.
- Adjust `CORS_ALLOW_ALL_ORIGINS` in `backend/settings.py` for production.

## Next Steps
- Add more models and views.
- Protect APIs with authentication (JWT).
- Deploy Django + React together on a single server (e.g., using Nginx + Gunicorn).
