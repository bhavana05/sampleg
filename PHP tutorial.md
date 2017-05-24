# PHP INSTALLATION IN UBUNTU 

#### What is PHP?

 PHP is a open source, interpreted and object-oriented scripting language i.e. executed at server side. It is used to develop web applications (an application i.e. executed at server side and generates dynamic page).

* PHP is a server side scripting language.

* PHP is an interpreted language, i.e. there is no need for compilation.

* PHP is an object-oriented language.

* PHP is an open-source scripting language.

* PHP is simple and easy to learn language.

* PHP runs on various platforms (Windows, Linux, Unix, Mac OS X, etc).

#### Main features of PHP:


1. Performance: Script written in PHP executes much faster then those scripts written in other languages such as JSP & ASP.

2. Open Source Software: PHP source code is free available on the web, you can developed all the version of PHP according to your requirement without paying any cost.

3. Platform Independent: PHP are available for WINDOWS, MAC, LINUX & UNIX operating system. A PHP application developed in one OS can be easily executed in other OS also.

4. Compatibility: PHP is compatible with almost all local servers used today like Apache, IIS etc.

5. Embedded: PHP code can be easily embedded within HTML tags and script.

First, we need to update our local package index to make sure we have a fresh list of the available packages. Then we can install the necessary components.

```$ sudo apt-get update```

* #### Step-1:Installing PHP 5.6

To install PHP, first you need to install Apache and MySql.
Now download php using the below commands.
```
$ sudo add-apt-repository ppa:ondrej/php
$ sudo apt-get update
$ sudo apt-get install -y php5.6 php5.6-mcrypt php5.6-gd
```
#### What is Apache2?

 Apache is the most popular Web server software. It enables a computer to host one or more websites that can be accessed over the Internet using a Web browser. Most Apache installations include a URL rewriting module called "mod_rewrite," which has become a common way for webmasters to create custom URLs.

* #### Step-2:Installing Apache2

To install Apache2, use the following command

```$ apt-get install apache2 libapache2-mod-php5```

#### What is MySQL?

 MySQL is a fast, easy-to-use RDBMS being used for many small and big businesses. It handles a large subset of the functionality of the most expensive and powerful database packages.

1. MySQL uses a standard form of the well-known SQL data language.

2. MySQL works on many operating systems and with many languages including PHP, PERL, C, C++, JAVA, etc.

3. MySQL works very quickly and works well even with large data sets.

4. MySQL is very friendly to PHP, the most appreciated language for web development.

* #### Step-3:Installing MySQL

To install MySql, use the below command

```$ apt-get install mysql-server php5.6-mysql```

If there is any error in connecting MySql to PHP:

* Check if etc/mysql.my.cnf file has [mysqld] line.

If mbstring missing error occurs:

* Then follow the below command
```$sudo apt-get install php-mbstring```
 
#### What is Composer?

Composer is not a package Manager.It is a tool for dependency management in PHP. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you.

* #### Step-4:Installing Composer
Install by using following commands
```
$ curl -sS https://getcomposer.org/installer | php
$ sudo mv composer.phar /usr/local/bin/composer
$ sudo chmod +x /usr/local/bin/composer
```

#### What is Laravel?

Laravel is a free, open-source PHP web framework, created for the development of web applications following the model–view–controller (MVC) architectural pattern. Some of the features of Laravel are a modular packaging system with a dedicated dependency manager, different ways for accessing relational databases, utilities that aid in application deployment and maintenance.

* #### Step-5:Installing Laravel

Now download laravel using composer.

```
$ cd /var/www
$ git clone https://github.com/laravel/laravel.git
```

Navigate to Laravel code directory and use composer to install all dependencies required for Laravel framework.

```
$ cd /var/www/laravel
$ sudo composer install
```

Dependencies installation will take some time. After than set proper permissions on files.

```
$ chown -R www-data.www-data /var/www/laravel
$ chmod -R 755 /var/www/laravel
$ chmod -R 777 /var/www/laravel/app/storage
```

* #### Step-6:Set Encryption Key

Now set the 32 bit long random number encryption key, which used by the Illuminate encrypter service.

```$ php artisan key:generate```

Output may look like this: Application key [uOHTNu3Au1Kt7Uloyr2Py9blU0J5XQ75] set successfully.

Now edit config/app.php configuration file and update above generated application key as followings. Also make sure cipher is set properly.

'key' => env('APP_KEY', 'uOHTNu3Au1Kt7Uloyr2Py9blU0J5XQ75'),

'cipher' => 'AES-256-CBC',

* #### Step-7:local Development Server

 You have PHP installed locally and you would like to use PHP's built-in development server to serve your application, you may use the serve Artisan command. This command will start a development server at http://localhost:8000:

```$ php artisan serve```

