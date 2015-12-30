docker run -p 80:80 --link mysql57:mysql -d --name php701 -v YOUR_APP_PATH:/var/www/html -v ~/Workspace/Docker/php7/config/apache:/etc/apache2/sites-enabled hhzz/php7
docker exec php701 bash -c "cd YOUR_APP_PATH && php artisan migraet"
docker exec php701 bash -c "cd YOUR_APP_PATH && php artisan db:seed"
