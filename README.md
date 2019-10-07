## Docker for Laravel

1. Place this folder to subfolder in your project.
    For example: Project placed at `/home/user/Projects/app`. So clone this repo to subfolder `/home/user/Projects/app/.dev`
2. Check app name in `docker/nginx/core/nginx.conf` - `server_name app.test;` - by default. If need - change it.
3. Place in `hosts` file  - `127.0.0.1 app.test` (or other name from point 2)
4. Run docker - Enter to folder `.dev` and run docker - `docker-compose up -d`
5. Stop docker - Enter to folder `.dev` and run docker - `docker-compose down`
6. Install php dependencies - `docker-compose run --rm php-fpm composer install`
7. Install node dependencies - `docker-compose run --rm nodejs npm install`
8. Start npm script - `docker-compose run --rm nodejs npm run <script_name>`
9. Enter in php shell `docker exec -it php-fpm bash`

### Urls

- Application http://app.test:8080
- Adminer http://app.test:8081

### PHP details
Composer

Custom php.ini file - in `./docker/php/`. After change - rebuild image.

#### PHP Modules
- gd
- imagick
- intl
- iconv
- mbstring
- mysqli
- PDO
- PDO_mysql
- zip
- soap
- xsl