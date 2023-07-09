# Project name and introduction

Home Automation setup

Homeserver simulates temperature and humidity data and exposing the data to the API. Back end server retrieves data from the API, front end provides data to the client. 

# Prerequisites

Python 3.x
Flask
flask-cors
Axios

# Installation & execution -

## Servers

1. Install the required dependencies:

pip install -r requirements.txt

2. Set up the configuration file:

Open `config.json` and update the temperature and humidity ranges as needed.

3. Run the Servers:

    ./service.sh 


4. The homeserver API will be available at `http://localhost:5004`

    ### API Endpoints

    GET /data

    Returns simulated sensor data for temperature and humidity.

    Example response:

    {"Temperature": "29.59°C", "Humidity": "59.7%"}


    The backend server API will be available at `http://localhost:5002`

    ### API Endpoints

    GET /collect-data

    Returns sensor data for temperature and humidity from home server

    Example response:

    {"Temperature": "29.59°C", "Humidity": "59.7%"}


## Front end 

Front end retrieves the data from back end. 

1. cd frontend
   npm start

2. The application will be available at http://localhost:3000/


# Layout 

assignment/
├── backend
│   ├── __init__.py
│   └── app.py
│   └── view.py
│   └── tests
|        └── __init__.py
|        └──backendtest.py
├── homeserver
│   ├── __init__.py
│   │   ├── app.py
│   │   ├── view.py
│   │   └── config.json
|        └── tests
|           └── __init__.py
|           └──backendtest.py
├── frontend
├── package.json
├── package-lock.json
├── .gitignore
├── README.md
└── service.sh
└── setup.py

