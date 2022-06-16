## PDOx
```
 _____  _____   ____       
 |  __ \|  __ \ / __ \      
 | |__) | |  | | |  | |_  __
 |  ___/| |  | | |  | \ \/ /
 | |    | |__| | |__| |>  <
 |_|    |_____/ \____//_/\_\
```
Fast, efficient and useful Query Builder and PDO Class for #PHP

[![Total Downloads](https://poser.pugx.org/klasvento/pdo-saas/d/total.svg)](https://packagist.org/packages/klasvento/pdo-saas)
[![Latest Stable Version](https://poser.pugx.org/klasvento/pdo-saas/v/stable.svg)](https://packagist.org/packages/klasvento/pdo-saas)
[![Latest Unstable Version](https://poser.pugx.org/klasvento/pdo-saas/v/unstable.svg)](https://packagist.org/packages/klasvento/pdo-saas)
[![License](https://poser.pugx.org/klasvento/pdo-saas/license.svg)](https://packagist.org/packages/klasvento/pdo-saas)

## Install

composer.json file:
```json
{
    "require": {
        "klasvento/pdo-saas": "^1"
    }
}
```
after run the install command.
```
$ composer install
```

OR run the following command directly.

```
$ composer require klasvento/pdo-saas
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

$db = new \Buki\Pdox($config);

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

1. Fork it ( https://github.com/klasvento/pdo-saas/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [Others](https://github.com/klasvento/pdo-saas/graphs/contributors)

[mit-url]: http://opensource.org/licenses/MIT
[doc-url]: https://github.com/klasvento/pdo-saas/blob/master/DOCS.md

