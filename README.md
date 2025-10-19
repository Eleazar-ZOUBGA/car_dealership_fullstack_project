# Setting-up of the project : 
cd server/
pip install virtualenv
virtualenv djangoenv
source djangoenv/bin/activate

# Install the necessary python packages : 
python3 -m pip install -U -r requirements.txt

# Perform the migrations to create necessary tables
python3 manage.py makemigrations

# Run migration to activate models for th app
python3 manage.py migrate

# Start he local development server
python3 manage.py runserver

# To create a superuser : 
python3 manage.py createsuperuser

# To launch the database's server : 
cd server/database
docker build . -t nodeapp
docker-compose up