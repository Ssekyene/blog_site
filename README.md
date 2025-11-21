<h1 align=center>My Blog site</h1>
<p align=center><em>A blog site web application built with <strong>django</strong></em></p>
<p align=center>
    <a href=""><img src="https://img.shields.io/badge/Version-1.0.0-blue.svg" alt="Version"></a>
</p>

<p>Live Demo at <a href="r21.pythonanywhere.com">r21.pythonanywhere.com</a></p>

## Features
- Create Posts
- Edit and Update Posts
- Delete Posts
- View Blog Posts
- User Authentication (Basic)
- Basic Styling / Template
- Comment system (Basic)

## Installation
### 1. Clone the Repository
```
git clone https://github.com/Ssekyene/blog_site.git
cd blog_site
```
### 2. Create and Activate a Virtual Environment
#### On Linux / macOS
```
python3 -m venv myvenv
source venv/bin/activate
```
#### On Windows
```
python -m venv myvenv
venv\Scripts\activate
```

### 3. Install Project Dependencies

Make sure you're within the virtual environment eg `(myvenv) ~$ `

- Lets first have the latest `pip` version:
```
python -m pip install --upgrade pip
```

- Then install the required dependencies:

``` 

pip install -r requirements.txt
```

### 4. Set Up Environment Variables (Optional but for security purposes)
-  Create a random secret key in the terminal:

```
python -c 'from django.core.management.utils import get_random_secret_key; \
      print(get_random_secret_key())'
```

- Create a file `.env` at the root of your project and add the following property in it:

```
# Here, inside the single quotes, you can cut and paste the random key generated above eg
SECRET='3!0k#7ds5mp^-x$lqs2%le6v97h#@xopab&oj5y7d=hxe511jl'
```

- Then update the Django settings file ([`mysite/settings.py`](mysite/settings.py)) to inject this secret value:

```
import os

SECRET_KEY = os.getenv('SECRET')
```

### 5. Apply Database Migrations

The project currently uses **SQLite** by default. Just run:

```
python manage.py makemigrations
python manage.py migrate
```

### 6. Create a Superuser (Optional but Recommended)

For accessing the Django admin at `http://127.0.0.1:8000/admin/`:

```
python manage.py createsuperuser
```

### 7. Run the Development Server

Start the local server using:

```
python manage.py runserver
```
Then open the app in your browser at:

```
http://127.0.0.1:8000/
```

### 8. Additional Notes
- Default database is SQLite, stored in `db.sqlite3.`
- No extra configuration is required, basic configurations are done.

- Ensure your virtual environment is activated whenever running Django commands.

- If static files are required for production, run:

```
python manage.py collectstatic
```

## Acknowledgment
- [DjangoGirls Tutorial](https://tutorial.djangogirls.org/en/) --> For the guidance during the devlopment of the project
- [Bootstrap](https://getbootstrap.com/) --> For the icons used and minimal styles used