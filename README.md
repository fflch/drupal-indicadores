1) Versão do php:

sudo update-alternatives --set php /usr/bin/php8.2
sudo update-alternatives --set phar /usr/bin/phar8.2
sudo update-alternatives --set phar.phar /usr/bin/phar.phar8.2

2) composer install

3) Instalar uma instância

./vendor/bin/drush site-install standard \
    --db-url=sqlite://sites/default/files/.ht.sqlite \
    --site-name="admin" \
    --site-mail="admin@localhost" \
    --account-name="admin" \
    --account-pass="admin" \
    --account-mail="admin@localhost" --yes
    
4) Sobe um server

./vendor/bin/drupal serve 0.0.0.0:8000 -vvv