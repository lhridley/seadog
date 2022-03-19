## Introduction

The Sea Dog suite of modules allows you to turn Drupal into a Digitao Ocean asset management system.

This modules interacts with the Digital Ocean API v2.  The documentation for that API can be found at:

* https://docs.digitalocean.com/reference/api/

The functionality of this module depends on the following:

* PHP 8.1 or higher
* Drupal 9.4 or higher
* The Key module (https://www.drupal.org/project/key)
* The "DigitalOcean API v2 client for PHP

### Getting started

1. Set up a Personal Access token with `read` and `write` scopes on your Digital Ocean account.
1. Add your PAT from step 1 to an environment variable for your Drupal environment.
1. Include the module via Composer so that all third party dependencies are included.
1. Enable the module.

#### Personal Access Token

In order for Sea Dog to interact with the Digital Ocean API, you need to confgiure a Personal Access Token with both `read` and `write` scopes.  You can set an expiration date n the token if you wish; this is a good security practice in general.

#### Environment Variable housing PAT

Once you set up the PAT with the proper scopes, create an environment variable called SEADOG_PAT in the environment where your Drupal project will be running, and enable the module.

#### Include the module via Composer

Execute `composer require drupal/seadog` to include the module as part of your project.

#### Enable the module

On your running Drupal installation, execute `drush pm:enable seadog -y`
