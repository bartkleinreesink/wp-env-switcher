<p align="center"><picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://fabrikage.nl/assets/img/logo-alt.svg">
  <img alt="Fabrikage logo" src="https://fabrikage.nl/assets/img/logo.svg">
</picture></p>

# <p align="center">fabrikage/wp-env-switcher</p>

<p align="center">Use this package to add a menu item in your WordPress admin bar in which you can switch between environments. This is useful when you have a DTAP street and you want to quickly switch between your environments.</p>

\
&nbsp;

The library will compare your current URL with the environment URLs you have set in your environment variables. If the current URL matches one of the environment URLs, that environment will be marked as active. Other environments will show in the submenu.

## Requirements

Set the following `$_ENV` variables in your project:

```bash
URL_DEVELOPMENT='https://example.dev'
URL_TESTING='https://example.test'
URL_ACCEPTANCE='https://example.acceptance'
URL_PRODUCTION='https://example.com'
```

*Note: These variables are not required, but if you don't set them, the corresponding menu item will not show up.*

## Installation

Install the package using composer:

```bash
composer require fabrikage/wp-env-switcher
```

## Usage

Add the following code to your `functions.php`:

```php
\Fabrikage\WordPress\EnvSwitcher::enable();
```

If you want to enable the menu for specific users, pass an array with usernames:

```php
\Fabrikage\WordPress\EnvSwitcher::enable(['admin', 'other-user']);
```

