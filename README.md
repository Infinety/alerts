## Laravel 5.1 SweetAlert

Laravel package to use the javascript SweetAlert with Laravel Service Provider.
Simple package, but effective.

## Installation

````
composer require infinety/alerts *@dev
````

After install this package you have to set the service provider on your config/app.php file

````
Infinety\Alerts\AlertServiceProvider::class
````


Copy the required assets of SweetAlert to your public folder. Those assets would be place in the css and js respective directory.

````
php artisan vendor:publish --tag=alerts
````

Then in your master view add those styles and scripts. Put this style between the <head> </head> tags

````
<link rel="stylesheet" type="text/css" href="css/sweetalert.css">
````

Add the JS script before close your </body> tag.

````
<script src="js/sweetalert.js"></script>
````

Include the alerts view to your master view. Add this code right after set the JS script file.

````
@include('Alerts::alerts')
````

### Usage

On your controllers is a perfect place to use it, any way you can fire the alerts from jobs or events.

````
alert('Title', 'Message')


alert()->error('Title', 'Message')


alert()->success('Title', 'Message')


alert()->overlay('Title', 'Message')
````

### Issues

If you have any questions or issues, please open an Issue and I will look at this and look to fix as soon as possible.

### SweetAlert website

http://t4t5.github.io/sweetalert/

### Thanks
Special thanks to https://github.com/socieboy/alerts for this package but changed a few things and wanted to learn myself how to make this sort of package also, so Kudos to Socieboy :)
