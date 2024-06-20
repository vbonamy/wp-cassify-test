Development and testing environment for WP-CASSIFY - A WordPress CAS plugin
============================

This project provides a development and testing environment for the WP-CASSIFY plugin with a docker-compose file that sets up 
 * a WordPress instance with the WP-CASSIFY plugin installed
 * a MariaDB database
 * an Apereo CAS server
 * with an OpenLDAP server

The same docker-compose provides also 
 * a selenium chrome node
 * and a selenium runner that runs the tests

The tests are edited with Selenium IDE.
There are two tests:
 * one that make the install of wordpress and the plugin and a simple configuration of the plugin (wp-cassify)
 * one that make the login with CAS on wordpress

## Usage

To launch all the dockers, included the selenium tests, simply run:
```
docker compose up
```

## Requirements

You have to install the last version of docker.

For debian for example, see the [official documentation](https://docs.docker.com/engine/install/debian/#install-using-the-repository)

## Github Actions

The project is also configured to run the tests on Github Actions. The workflow is defined in the file `.github/workflows/docker-selenium-tests.yml`.