# Authentication System

#### Project Description
- Authentication system using PHP & Slim micro-framework
- YouTube [Link](https://www.youtube.com/playlist?list=PLfdtiltiRHWGKUvioJly40RJZchSG2-34)

#### Purpose:
- To understand and learn more about PHP

#### Timeline:
- Start: May 28, 2018
- End: still deciding if install php 7.1.3

#### Dependencies
- PHP 7.1.3 (for Illuminate Database to install)
- Slim ^2.6
- Slim-Views 0.1.3 (to use Twig template engine)
- Twig 1.18.1
- PHP Mailer 5.2.10 (to send email)
- Config 0.8.2
- Illuminate Database

#### For redirect to work:
- For 500 internal error, see: https://stackoverflow.com/a/31451383/6353682
- Make sure to run: sudo a2enmod rewrite
- Then add these lines on apache2.conf or sites-available/xxx.conf if enabled:

```
<Directory directory>
    Options Indexes FollowSymLinks
    AllowOverride All
    Require all granted
</Directory>
```
- where directory could be /var/www/ or the directory in your sites-available/xxx.conf

#### Create .htaccess (where index.php is located) and add these lines:

```
RewriteEngine On

RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^ index.php [QSA,L]
```

#### Credit:
- [Codecourse YouTube Channel](https://www.youtube.com/user/phpacademy/about)
