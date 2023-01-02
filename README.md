# ML model classification application

The repository provides implementation of endpoints for prediction of iris species.

Technologies used:
- endpoint
    - fastapi
    - postgres
    - sqlalchemy
- model training
    - jupyter notebook
    - scikit-learn
    - numpy
    - pandas
    - joblib

## Model training + Endpoint diagram
![Model diagram](/images/diagram.png "Model diagram")

## Launch options
![Launch](/images/launch.png "Launch options")

### 0. Project setup
1. [Download postgres application](https://www.postgresql.org/download/)
2. Open postgres application and create the password to access the database
3. Create .env file in the repo folder according to the template_env.txt
4. Place the .env file in the repo folder and copy it to fastapi/dbms.
5. Kill the processes running on localhost:5432 by running ```sudo kill -9 `sudo lsof -t -i:5432```
6. Make sure ```*.env``` is added to gitignore!

### 1. Docker
1. Open Docker application
2. Open terminal
    - Download postgres docker version by running ```docker pull postgres```
    - Run postgres and set up all the necessary 
    - Go to the root folder = deepsenseai
    - Run command ```docker build -t deepsenseai .```
    - Go to fastapi folder (root folder isn't sufficient!)
    - Run command ```docker compose up```
    - Make use of a local endpoint ```localhost:8000```!
    - Remarks:
        - make sure docker application is running
        - you may get an error after ```docker compose up``` (it's because postgres runs asynchrounsly for some reason)
        - if so run ```docker compose up``` again and you should access the endpoint

### 2. Terminal
1. Open postgres application and enter the password
2. Open terminal
    - Go to fastapi folder
    - Run command ```uvicorn main:app --host 0.0.0.0 --port 8000"```
    - Make use of a local endpoint ```localhost:8000```!






