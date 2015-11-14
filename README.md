Scala example with playframework and slick
==========================================
[![Build Status](https://travis-ci.org/kozlov-p-v/car-adverts.svg?branch=master)](https://travis-ci.org/kozlov-p-v/car-adverts)
[![Coverage Status](https://coveralls.io/repos/kozlov-p-v/car-adverts/badge.png?branch=master)](https://coveralls.io/r/kozlov-p-v/car-adverts)

# Car Adverts RESTful service
To run application just type "sbt run"

Application supports the following methods:
GET /adverts - list all adverts
GET /adverts/{id} - find by id
DELETE /adverts/{id} - delete by id
PUT /adverts/{id} - update (modify) existing advert
POST /adverts - create new advert

All adverts have the following fields:
 - id (UUID, required)
 - title (string, required)
 - fuel (string/enum, required)
 - price (integer, required)
 - new (boolean, required)
 - mileage (integer, optional) - only for used cars (new = false)
 - firstRegistration (local date, optional) - only for used cars (new = false)

Application uses H2 embedded database in-memory. No need to prepare anything.

