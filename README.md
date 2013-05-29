# JuliusBoilerplateBundle

Boilerplate (starter) bundle for Symfony2

## Enabling the bundle

Add following line in your `AppKernel.php` file to enable the bundle
```
// app/AppKernel.php
...
new Julius\BoilerplateBundle\JuliusBoilerplateBundle(),
```

## Declaring your routes

To declare your custom routes you can use `routing.yml` file situated in `./Resources/config`. Be sure to include this file in your main routing configuration.

### Example routing configuration
Your main configuration:
```
# app/config/routing.yml
JuliusBoilerplateBundle:
    resource: "@JuliusBoilerplateBundle/Resources/config/routing.yml"
```
Bundle routing configuration:
```
# Julius/BoilerplateBundle/Resources/config/routing.yml
JuliusBoilerplateBundle:
    resource: "@JuliusBoilerplateBundle/Resources/config/routing.yml"
```

## Asset management

If you need public access to your assets (images/stylesheets/javascripts etc.) place them under `./Resources/public` directory. The contents of this folder will be put inside `symfony-base-path/web/bundles/juliusboilerplate` after executing `php app/console assets:install` command.
