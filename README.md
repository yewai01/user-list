# user-list

### env setup
- 【CMD】docker compose up -d
- 【CMD】docker compose exec php bash
- 【CMD】cd ./user-list
- 【CMD】cp .env.example .env
- 【CMD】composer install
- 【CMD】php artisan key:generate
- 【CMD】php artisan migrate --seed
- 【Note】if permission error occurs, delete storage/logs/todaydate.log