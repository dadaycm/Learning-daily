## Laravel cheat sheet

## Laravel 5 Faker tutorial  

http://www.tutorials.kode-blog.com/laravel-5-faker-tutorial

Faker can be used to generate the following data types

Numbers
Lorem text
Person i.e. titles, names, gender etc.
Addresses
Phone numbers
Companies
Text
DateTime
Internet i.e. domains, URLs, emails etc.
User Agents
Payments i.e. MasterCard
Colour
Files
Images
uuid
Barcodes
Miscellaneous

```
Route::get('/customers',function(){
    $faker = Faker\Factory::create();

    $limit = 10;

    for ($i = 0; $i < $limit; $i++) {
        $faker->name . ', Email Address: ' . $faker->unique()->email . ', Contact No' . $faker->phoneNumber . '<br>';
    }
});

```

## Vue.js
