# Cooklist

Cooklist is a recipe-sharing and meal-planning application built with Django. Users can share recipes, plan meals, and create shopping lists. This README file documents the setup and deployment process of the application on Heroku, based on the actions taken to address deployment issues.

## Table of Contents

- Project Setup
- Dependencies
- Environment Variables
- Procfile
- Deployment on Heroku
- Troubleshooting
- Credits

## Project Setup

1. Clone the repository and navigate to the project directory.
2. Set up a virtual environment and activate it.
3. Install dependencies listed in the requirements file.
4. Create the profiles app within the Django project.

## Dependencies

Ensure the following packages are installed and listed in your requirements file:

asgiref version 3.8.1, dj-rest-auth version 6.0.0, Django version 5.1.2, django-allauth version 65.0.2, django-cors-headers version 4.4.0, djangorestframework version 3.15.2, sqlparse version 0.5.1, tzdata version 2024.2.

To install any missing packages, update the requirements file accordingly.

## Environment Variables

For deployment, ensure the following environment variables are set:

The Django Secret Key, replacing it with your own secret key. The database URL, which is automatically set by Heroku for PostgreSQL. Set the debug variable to false for production.

Environment variables can be set in the Heroku dashboard or using the Heroku CLI.

## Procfile

Create a Procfile in the root directory with a command to run the Gunicorn server, pointing to the correct Django WSGI application file.

## Deployment on Heroku

1. Log in to Heroku.
2. Create a new Heroku application.
3. Add the PostgreSQL add-on to the Heroku application.
4. Push code to Heroku.
5. Run migrations on the Heroku database.
6. Create a superuser to access the Django admin.

## Troubleshooting

If a Module Not Found error occurs, for example, for the `corsheaders` or `requests` package, ensure it is listed in the requirements file and install it. Additionally, verify the application structure and that Heroku environment variables are correctly configured.

## Credits

This project was developed as part of the Full Stack Software Development Diploma. Additional resources include documentation from Django, Heroku, and various open-source libraries utilized within the project.
