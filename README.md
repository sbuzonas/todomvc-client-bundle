Getting Started With FancyGuyTodoMVCClientBundle
================================================

This bundle implements an API client interface in the style of [TodoMVC](http://todomvc.com) to
highlight best practices, defined by FancyGuy Technologies, in implementing a web client in PHP.

## Prerequisites

This bundle requires Symfony 2.1+.

## Installation

1. Download FancyGuyTodoMVCClientBundle using composer
2. Enable the bundle
3. Update the application routes

### Step 1: Download FancyGuyTodoMVCClientBundle using composer

Add FancyGuyTodoMVCClientBundle by running the command:

``` bash
$ composer require fancyguy/todomvc-client-bundle "1.0.x-dev"
```

Composer will install the bundle to the project's `vendor/fancyguy` directory.

### Step 2: Enable the bundle

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new FancyGuy\Bundle\FancyGuyTodoMVCClientBundle(),
    );
}
```

### Step 3: Update the application routes

``` yaml
# app/config/routing.yml
fancyguy_todomvc_client:
    resource: "@FancyGuyTodoMVCClientBundle/Controller/"
    type:     annotation
    prefix:   /client
```
