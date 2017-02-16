# Google Cloud Storage Bucket Browser

## Description
This is a simple web-based application to browse the contents of a bucket from the GCS upon user authentication.

It was built using the [Google PHP cloud client library](https://github.com/GoogleCloudPlatform/google-cloud-php) and [jstree](https://github.com/vakata/jstree).

The [storage-metabucket-javascript](https://github.com/GoogleCloudPlatform/storage-metabucket-javascript) and [storage-getting-started-php](https://github.com/GoogleCloudPlatform/storage-getting-started-php) projects were used as a starting point.

This build was tested in PHP version 7.1 using the official PHP docker image [php:7.1-apache](https://hub.docker.com/_/php/)

## Prerequisites:
[google-cloud-php](https://github.com/GoogleCloudPlatform/google-cloud-php)

```
$ composer require google/cloud
```

[thephpleague/oauth2-google](https://github.com/thephpleague/oauth2-google)

```
$ composer require league/oauth2-google
```

## Running the application using Docker:
Run the following command in the project directory:
docker run -d -p 80:80 --name &lt;my-apache-php-app&gt; -v "$PWD":/var/www/html php:7.1-apache

And the web app will be deployed in the host mapped to port 80.

## Deploying authentication
Rename conf.demo.php to conf.php and fill in with your credentials information with oauth credentials previously created on
