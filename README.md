# family-board

## Setup / File structure
### family-board | family-board/backend | family-board/frontend/project-x
##### family-board_base repo contains root files (docker-compose), backend and frontend are two separate repos because heroku needs two separate repos / two apps
### You can create a local (non-git) folder and only copy the docker-compose.yaml manually from here. Inside this folder, you can run:
#### Backend
##### git clone git@github.com:ydaetwyler/familyboard-backend.git backend
#### Frontend
##### git clone git@github.com:ydaetwyler/familyboard-frontend.git frontend/project-x

### Root env (for docker) / local setup
#### Path: .env
##### DOCKER_ENV=dev
##### APP_SERVER_PORT=4000
##### APP_CLIENT_PORT=3000

### Backend env / local setup
#### Path: backend/.env
##### MONGO_URI="" -> Mongo DB Atlas (cloud) => https://www.mongodb.com/cloud/atlas/register
##### NODE_ENV="development"
##### PORT=4000
##### SECRET_KEY="" -> Secret for encryption
##### FRONT_BASE_URL="http://localhost:3000"
##### MAIL_PW="" -> Mail account pw (you may change the email sender in the code - ToDo: Email address env)
##### PASSWORD="" -> Secret for encryption (must be 32 characters)

### Frontend env / local setup
#### Path: frontend/project-x/.env.development.local
##### REACT_APP_BASE_URL="http://localhost:4000/dashboard"
##### REACT_APP_SUBSCRIBE_URL="ws://localhost:4000/dashboard"
##### REACT_APP_OPENWEATHER_KEY="" -> Openweathermap API => https://openweathermap.org/api

### Ready?
#### docker-compose up -d
##### Happy codding :)

### Logs
#### You'll find logs in your DB
#### & you can log with docker
##### docker-compose logs -t -f server
##### docker-compose logs -t -f client
