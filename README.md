Painel AdminLTE Angular 4 e API JWT Laravel 5.5 
============

Esse projeto teve origem através da série **[TJG Web](https://www.youtube.com/watch?v=qA5bwYfmAqE)**, onde ensina integrar um painel AdminLTE com Angular 4.4 e API JWT Laravel 5.5.

Laravel
------------

Acesse o site da documentação do **[laravel](https://laravel.com/docs/5.5/installation)** para mais informação sobre a instalação

Vá para o diretório Dashboard.

```bash
cd Dashboard
```

execute o **[composer](https://getcomposer.org/download/)** para fazer a instalação dos componentes:

```bash
composer install
```

edite o arquivo .env, configure o banco de dados e o segredo do jwt

```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=database_name
DB_USERNAME=database_username
DB_PASSWORD=database_password
```

Adicione a chave de acesso da api através do comando

```bash
php artisan jwt:generate
```

ou editando o arquivo .env manualmente

```bash
JWT_SECRET=key
```

Faça a migração das tabelas

```bash
php artisan migrate --seed
```

Se você instalou o PHP localmente e você gostaria de usar o servidor de desenvolvimento incorporado do PHP para atender seu aplicativo, você pode usar o comando do servidor Artisan. Este comando iniciará um servidor de desenvolvimento em :

```bash
http://localhost:8000
```
```bash
php artisan serve
```

Angular
------------

Instale o angular cli.
```bash
npm install -g @angular/cli
```

vá até o diretório web

```bash
cd web
```

```bash
npm install
```

Edite a url da api no arquivo ```src\environments\environments\environment.ts```

```bash
export const environment = {
  api_url: 'http://localhost'
};
```
