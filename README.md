<img src="http://i.imgur.com/gKXJr5j.png" alt="Ultracore PHP 7 MVC Framework Logo" />

PHP 7 framework for building killer MVC web apps and APIs.

Designed and maintained by Nathaniel Sabanski. Open source under the MIT license.

## Features

* Fully automatic URL routing to contoller methods.
* Add new pages and API endpoints with ease.
* Autoloader with sub-directory traversal.
* Tiny codebase for easy security audits.
* Pure PDO database with wrapper to handle configuration.
* Fully commented codebase with PHPUnit test suite.
* Apache or nginx.

## Requirements

* PHP 7+.
* Apache 2+ ('''mod_rewrite''' enabled) or nginx.

## Usage Notes

1. Development and production configurations can be set in '''/system/config/Config.class.php'''

2. Optionally, PHPUnit is used to run the tests.

3. If using nginx, enable routing by using a server rule to route to '''index.php'''. This is achieved in Apache using '''mod_rewrite''' and the .htaccess file.

## License

This project is licensed under the MIT License. This means you can use and modify it for free in private or commercial projects.

