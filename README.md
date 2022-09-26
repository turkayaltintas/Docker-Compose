# Docker Multi Project

@turkayaltintas

### Eklentiler
- [Laravel User Permisson Plugin](https://spatie.be/docs/laravel-permission/v5/installation-laravel)

### Yeni bir bilgisayarda kurulum yapıldığında ->
- docker-compose up -d

### Docker Bilgiler
- docker ps -> çalışan containerları listeler
- docker-compose up -d --build -> docker-compose.yml dosyasındaki değişiklikleri uygular
- docker-compose down -> çalışan containerları durdurur
- docker-compose exec php-apache /bin/bash -> php-apache containerına giriş yapar

### Console
- composer install
- composer update
- php artisan migrate

### Dikkat Edilmesi Gereken Konular
```
    npm install i PhpStorm da boşa yapma bir işe yaramıyor.
    .env` de database düzenlemelerini yap.
    Terminal`'den proje içerisinde composer update yap.
    php artisan serve` ile projeyi çalıştır.
```

## Docker Start Containers
 İlgili parametreler:
```
docker-compose up -d --build
```
<img height="250" src="https://i.hizliresim.com/9coqhfs.png"/>

### Set up the Laravel application ###
To set up the Laravel application, initiate a container in the php-apache container with the command below.
```
docker-compose exec php-apache /bin/bash
```
This opens a CLI in the php-apache container. Create the Laravel application using the following command.
```
composer create-project laravel/laravel .
```

### http://localhost:8080/  ###
