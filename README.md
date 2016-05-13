<img src="http://i.imgur.com/Blqx0N2.png" alt="Ultracore PHP 7 MVC Template Logo" />

PHP 7 MVC template for building lean web apps and APIs.

Designed and maintained by Nathaniel Sabanski. Open source under the MIT license.

[![Build Status](https://travis-ci.org/gnat/ultracore.svg?branch=master)](https://travis-ci.org/gnat/ultracore)

## Features

* Automatic URL routing to contollers.
* Add new pages and API endpoints with ease.
* Tiny codebase for easy security audits.
* Autoloader with sub-directory traversal.
* PDO database wrapper.
* Fully commented codebase, with PHPUnit tests.
* Apache or nginx.

## Requirements

* PHP 7+.
* Apache 2+ or nginx.

## Example Page (http://localhost/example)

Create **system/controllers/Example.class.php** with the following code:

```php
<?php
namespace Ultracore;

class Example extends Controller
{
	function Default() 
	{
		echo "Hello World!";
		exit();
	}
}
```

## Example REST API Endpoint (http://localhost/timestamp)

Create **system/controllers/Timestamp.class.php** with the following code:

```php
<?php
namespace Ultracore;

// Returns current Unix timestamp as JSON.
class Timestamp extends Controller
{
	function Default() 
	{
		$output = array("Timestamp" => time());
		$output = json_encode($output);
		$this->View('json');
		echo $output;
		exit();
	}
}
```

## Usage Notes

1. Development and production configurations can be set in **/system/config/Config.class.php**

2. Optionally, PHPUnit is used to run the tests.

## If using Apache

Enable **mod_rewrite** and add **AllowOverride All** to your site configuration. This will enable routing using the included .htaccess file. 

```
<Directory "/var/www">
	AllowOverride All
</Directory>
```

## If using nginx

Enable routing by creating a location rule set to **index.php** inside your server configuration.

```
location / {
	index index.html index.php;
}
```

## Keywords

Framework, Model View Controller, PHP 7 Compatible, PHP 7+, router, fast, simple, lean.

## License

This project is licensed under the MIT License. This means you can use and modify it for free in private or commercial projects.
