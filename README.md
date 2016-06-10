# Codeigniter-Database-Environment
Manage your database environment in codeigniter

- Copy database.php into your project config folder

- Manage your environment by edit this line
```php
$db_env = array(
	'development' => 'default', //In case development
	'production' => 'production' //In case production
);
```

- Config your environment case
```php
'hostname' => '', // Your host name
'username' => '', // Your DB username
'password' => '', // Your DB password
'database' => '', // Your DB name
```

- Config the environment by edit index.php in your project
```php
define('ENVIRONMENT', isset($_SERVER['CI_ENV']) ? $_SERVER['CI_ENV'] : 'development');
```

Then when your call `$this->db` thie environment will switch as you config.
