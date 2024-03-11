## 1.Crea un nuevo proyecto de Laravel 7 llamado "actividad7".
Abre tu terminal y ejecuta el siguiente comando ==
composer create-project --prefer-dist laravel/laravel actividad7

## 2.Crea el proyecto Git y el repositorio en GitHub:
Primero, navega al directorio de tu proyecto == cd actividad7

## 3.Luego, inicializa un repositorio Git e incluye todos los archivos
git init,
"git add .",
git commit -m "Inicializar repositorio".

## 4.Después, ve a GitHub y crea un nuevo repositorio. Luego, sigue las instrucciones para agregar tu repositorio remoto a tu repositorio local:
git remote add origin <url_del_repositorio_github>
git branch -M main
git push -u origin main

## 5.Usando la consola Artisan, crea modelos, controladores y migraciones:
php artisan make:model Usuario -m

## 6.Controlador:
php artisan make:controller UsuarioController --resource

## 7.Define los atributos, claves primarias y claves externas en los archivos de migración:

Abre el archivo de migración generado en database/migrations y define los atributos y restricciones necesarios. Por ejemplo:
Schema::create('usuarios', function (Blueprint $table) {
    $table->id();
    $table->string('nombre');
    $table->string('email')->unique();
    // Añadir otras columnas según sea necesario
    $table->timestamps();
});

## 8.Crea tus relaciones en los modelos correspondientes:

Abre los modelos ubicados en app/Models y define las relaciones necesarias. Por ejemplo:
namespace App\Models;

use Illuminate\Database\Eloquent\Model;

class Usuario extends Model
{
    // Ejemplo de relación con otro modelo
    public function roles()
    {
        return $this->hasMany(Rol::class);
    }
}

## 9. Por ultimo Ejecuta tus migraciones:
php artisan migrate


## DIAGRAMA ER 
![Imagen de WhatsApp 2024-03-10 a las 17 09 48_d1f474f8](https://github.com/Lapituda/actividad7/assets/102392241/d2cb9920-2d11-466f-93fe-face20cc34af)


# TAREA 6

Descripción del Proyecto: [Descripción breve del proyecto]

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[WebReinvent](https://webreinvent.com/)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Jump24](https://jump24.co.uk)**
- **[Redberry](https://redberry.international/laravel/)**
- **[Active Logic](https://activelogic.com)**
- **[byte5](https://byte5.de)**
- **[OP.GG](https://op.gg)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
