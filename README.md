# Laravel Countries

[![License](https://poser.pugx.org/dariusiii/laravel-countries/license?format=flat-square)](https://packagist.org/packages/dariusiii/laravel-countries)
[![Total Downloads](https://poser.pugx.org/dariusiii/laravel-countries/downloads?format=flat-square)](https://packagist.org/packages/dariusiii/laravel-countries)
[![Latest Stable Version](https://poser.pugx.org/dariusiii/laravel-countries/v/stable?format=flat-square)](https://packagist.org/packages/dariusiii/laravel-countries)
[![Latest Unstable Version](https://poser.pugx.org/dariusiii/laravel-countries/v/unstable?format=flat-square)](https://packagist.org/packages/dariusiii/laravel-countries)


Laravel Countries is a bundle for Laravel, providing ISO 3166_2, 3166_3, currency, capitals and more for all countries.

This package has been forked from bhuvidya/laravel-countries.

## Installation

Add `dariusiii/laravel-countries` to your app:

    $ composer require "dariusiii/laravel-countries


## Configuration

You can elect to manage your own configuration. This is an optional step, it only contains the table name and does
not need to be altered. If the default table name `countries` suits you, leave it. Otherwise run the following command

    $ php artisan vendor:publish --provider='DariusIII\Countries\CountriesServiceProvider' --tag=config

The config file can then be found at `config/countries.php`.


## Migrations

The service provider automatically adds the package's migrations to your app.


## Seeding

There is a seeding module in the package. You can either run the seeder manually from the command line:

    $ php artisan db:seed --class='DariusIII\Countries\CountriesSeeder'

Otherwise you can add it to one of your app's database seeder files, probably `database/seeds/DatabaseSeeder.php`:

    use DariusIII\Countries\CountriesSeeder;

    /**  
     * Run the database seeds.
     *    
     * @return void 
     */ 
    public function run()
    {        
        ...
        $this->call(CountriesSeeder::class);
        ...
    }

