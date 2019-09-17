Flight Leverage
===============

Simple Middleman blog for Flight Leverage (Travel Hacking).

## Setup

* Configure a config/deploy.yml from config/deploy.yml.sample

## Just do this

  $ curl http://www.flightleverage.com/penguin

## Deploying

Hosting is handled by dokku as a static site with the [buildpack-nginx](https://github.com/dokku/buildpack-nginx) buildpack (specified in `.env`).

Configuration:

    NGINX_ROOT=build
