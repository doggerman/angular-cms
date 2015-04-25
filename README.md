angular-cms
===========

[![Build Status](https://travis-ci.org/rmatil/angular-cms.svg?branch=master)](https://travis-ci.org/rmatil/angular-cms)
[![Codacy Badge](https://www.codacy.com/project/badge/29fc1a82158346ddb42cd13cdde3a163)](https://www.codacy.com)

Angular CMS is a simple Content Management System (CMS) which is based on the structure of a [Slim Application](https://github.com/codeguy/Slim). The content managamenet itself is implemented as a single page application with AngularJS.

![ScreenShot](/web/media/overview.png)

Installation
============
As of now, you have to clone the repo via git.

Once downloaded, use composer in the root folder to install required dependencies: `composer install`.
In `web/cms/` run `bower install` to download all required frontend packages.

To minify all assets, run `gulp` in the project root folder.

After download, set up the connection to your database in `config/yaml/parameters.yml`. Furthermore, you can setup the credentials for a mailserver which gets used for sending emails for user registration purposes.

Generate the database schema using `vendor/bin/doctrine orm:schema-tool:create` in the root folder of this application.

You also may want to change the locale used for this application, which you can do in this file 
[here](https://github.com/rmatil/angular-cms/tree/v0.1/setup.php#L39). 
Additionally, you can change the path to the media directory for uploaded files [here](https://github.com/rmatil/angular-cms/tree/v0.1/setup.php#L35) and [here](https://github.com/rmatil/angular-cms/tree/v0.1/setup.php#L36). It might be necessary to give your webserver write permissions on this folder.

Login to backend
================
As of now, you have to generate a user entry in the database. Use `sha512` as hash algorithm for field `passwordHash`.
Navigate in your browser to `your-webserver/login` to login with specified username and password.

Registration Endpoint
=====================
Registration endpoint is specified at `api/registration/:token`



