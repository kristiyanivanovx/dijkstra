# Dijkstra's algorithm in PHP
[![Build Status](https://travis-ci.org/taniko/dijkstra.svg?branch=master)](https://travis-ci.org/taniko/dijkstra)
---

Fork of [taniko/dijkstra](https://github.com/taniko/dijkstra), extended to suit my needs.
## Installation
```sh
composer require taniko/dijkstra
```

```
"repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/kristiyanivanovx/dijkstra"
        }
    ],
```

## Usage
```php
$graph = Taniko\Dijkstra\Graph::create();
$graph
    ->add('s', 'a', 1)
    ->add('s', 'b', 2)
    ->add('a', 'b', 2)
    ->add('a', 'c', 4)
    ->add('b', 'c', 2)
    ->add('b', 'd', 5)
    ->add('c', 'd', 1)
    ->add('c', 't', 3)
    ->add('d', 't', 1);
$route = $graph->search('s', 't'); // ['s', 'b', 'c', 'd', 't']
$cost  = $graph->cost($route);     // 6.0
```
