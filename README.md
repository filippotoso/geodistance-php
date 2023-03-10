# Geodistance
A simple & minimal geodistance php library to calculate geo distance between two points (latitude, longitude) using [Harvesine formula](https://www.wikiwand.com/en/Haversine_formula)

## Installation

``` bash
composer require 0x13a/geodistance-php
```

## Usage

```php
<?php

require_once __DIR__ . '/vendor/autoload.php';

use function Geodistance\centimeters;
use function Geodistance\feet;
use function Geodistance\kilometers;
use function Geodistance\miles;
use function Geodistance\meters;
use function Geodistance\yards;
use Geodistance\Location;

$new_york          = new Location(40.7128, 74.0059);
$los_angeles       = new Location(34.0522, 118.2437);
$decimal_precision = 3;

echo kilometers($new_york, $los_angeles); // 3936
echo miles($new_york, $los_angeles, $decimal_precision); // 2445.564
echo yards($new_york, $los_angeles); // 4304181
echo feet($new_york, $los_angeles); // 12912543
echo centimeters($new_york, $los_angeles); // 393575500
echo meters($new_york, $los_angeles); // 3935755

```

## License

Geodistance PHP is licensed under the MIT license. See [License File](LICENSE) for more information.

## Release info

This package disappeared from Github the 20th January, 2023, so I cloned it. 
I added the FilippoToso prefix to the namespace to avoid naming collisions.