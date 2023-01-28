# ultimate-systems

## prerequisites

- php 8.1

## deployment

`git  clone https://github.com/takdzwiedz/ultimate-systems/`

`cd ultimate-systems`

`composer-install`

configure `.env file with your local database`
and execute

`php bin/console make:migration`

`$ php bin/console doctrine:migrations:migrate`

launch local server

`symfony server:start --port-8080`

## Authentication

### 1. Main authorisation is on branch name 'main'

`git checkout main`

open browser and got o `127.0.0.1:8080/api/doc` to see available routes

### 2. Proto JWT authorisation on early stage is on branch 'jwt'

`git checkout jwt`

`php bin/console lexik:jwt:generate-keypair`

and try route `/api/login_check` to get JWT Token
use  JWT Token to access `/api/admin`