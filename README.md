## saasdb

Fast, efficient and useful Query Builder and PDO Class for #PHP

[![Total Downloads](https://poser.pugx.org/kolayentegre/saas-db-pdo/d/total.svg)](https://packagist.org/packages/kolayentegre/saas-db-pdo)
[![Latest Stable Version](https://poser.pugx.org/kolayentegre/saas-db-pdo/v/stable.svg)](https://packagist.org/packages/kolayentegre/saas-db-pdo)
[![Latest Unstable Version](https://poser.pugx.org/kolayentegre/saas-db-pdo/v/unstable.svg)](https://packagist.org/packages/kolayentegre/saas-db-pdo)
[![License](https://poser.pugx.org/kolayentegre/saas-db-pdo/license.svg)](https://packagist.org/packages/kolayentegre/saas-db-pdo)

## Install

composer.json file:
```json
{
    "require": {
        "kolayentegre/saas-db-pdo": "^1"
    }
}
```
after run the install command.
```
$ composer install
```

OR run the following command directly.

```
$ composer require kolayentegre/saas-db-pdo
```

## Example Usage
```php
require 'vendor/autoload.php';

$config = [
	'host'		=> 'localhost',
	'driver'	=> 'mysql',
	'database'	=> 'test',
	'username'	=> 'root',
	'password'	=> '',
	'charset'	=> 'utf8',
	'collation'	=> 'utf8_general_ci',
	'prefix'	 => ''
];

$db = new \klas\saasdb($config);

$records = $db->table('users')
		->select('id, name, surname, age')
		->where('age', '>', 18)
		->orderBy('id', 'desc')
		->limit(20)
		->getAll();

var_dump($records);
```

## Docs
Documentation page: [PDOx Docs][doc-url]


## Licence
[MIT Licence][mit-url]

## Contributing

1. Fork it ( https://github.com/kolayentegre/pdo-saas/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [Others](https://github.com/klasvento/pdo-saas/graphs/contributors)

[mit-url]: http://opensource.org/licenses/MIT
[doc-url]: https://github.com/klasvento/pdo-saas/blob/master/DOCS.md

