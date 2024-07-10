### Project Setup

** To run project**
docker compose build
docker compose up

1. **Make and apply migrations:**

   ```sh
   python manage.py makemigrations
   python manage.py migrate
   ```

2. **Create a superuser to access the admin site:**
   ```sh
   python manage.py createsuperuser
   ```

### Running the Project

1. **Start the development server:**

   ```sh
   python manage.py runserver
   ```

2. **Test the endpoints:**

   - **Register a new user:**

     ```
     POST /api/register/
     {
       "username": "testuser",
       "email": "test@example.com",
       "password": "testpassword123"
     }
     ```

   - **Login:**

     ```
     POST /api/login/
     {
       "email": "test@example.com",
       "password": "testpassword123"
     }
     ```

   - **Logout:**

     ```
     POST /api/logout/
     ```

   - **Get or update user details:**
     ```
     GET /api/me/
     PATCH /api/me/
     {
       "username": "newusername"
     }
     ```
