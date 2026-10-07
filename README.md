# Weather App using Django

## Project Overview

This project is a Weather App developed using Django and Python. It allows users to search for the current weather of a city using the OpenWeather API.

## Features

- Search weather by city name
- Display current temperature
- Display humidity
- Display atmospheric pressure
- Display weather conditions
- Display weather icon
- Store recent searches
- Display the last 5 searches

## Technologies Used

- Python
- Django
- SQLite
- OpenWeather API
- HTML
- CSS

## Project Structure

```text
DjangoWeatherApp/
│
├── manage.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── weather/
│   ├── migrations/
│   │   └── 0001_initial.py
│   │
│   ├── templates/
│   │   └── main/
│   │       └── index.html
│   │
│   ├── apps.py
│   ├── models.py
│   ├── urls.py
│   └── views.py
│
└── weather_project/
    ├── asgi.py
    ├── settings.py
    ├── urls.py
    └── wsgi.py
```

### How to Run

### 1. Create a virtual environment

```bash
python -m venv venv
```

### Windows:

```bash
venv\Scripts\activate
```

### 2. Install the required packages

```bash
pip install -r requirements.txt
```

### 3. Apply migrations

```bash
python manage.py migrate
```

### 4. Add your OpenWeather API key

Open:

```text
weather/views.py
```

Set your API key:

```python
API_KEY = "your_api_key_here"
```

### 5. Start the server

```bash
python manage.py runserver
```

Open:

```text
http://127.0.0.1:8000/
```

### 6. Search for a city

Enter a city name such as:

```text
Delhi
```

The application displays the current weather information and stores the search in the database.

## How It Works

The user enters a city name and submits the form.

- **View:** `weather/views.py` handles the weather request and application logic.
- **Model:** `weather/models.py` stores the search history.
- **Template:** `weather/templates/main/index.html` displays the weather information.
- **URL:** `weather/urls.py` connects the URL to the view.
- **Database:** SQLite is used to store the search history.
- **API:** OpenWeather API provides the current weather data.

The application displays the city, temperature, humidity, pressure, weather conditions and weather icon. The five most recent searches are also displayed.

## Basic Demo

1. Start the Django development server.
2. Open the Weather App in the browser.
3. Enter a city name.
4. View the current weather information.
5. Search different cities.
6. View the five most recent searches.

## GitHub

The repository contains the complete Django project files, `README.md`, `requirements.txt` and `.gitignore`.

The virtual environment, `db.sqlite3` and generated `__pycache__` files are not uploaded to the repository.

