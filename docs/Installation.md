# Installation

!!! warning ""

    We recommend that you test the extensions on a test Magento installation before installing them on a live Magento installation.

Prior to installation, you may want to:

1. Back up your database.
2. Enable maintenance mode.

You can install the extension in the following ways:

1. [Install the extension using Composer](#install-the-extension-using-composer).
2. [Download package from the `My Downloadable Products` page](#download-package-from-the-my-downloadable-products-page).

## Install the extension using Composer
1. Log in to your Magento server as, or switch to, the file system owner.
2. Navigate to your Magento project directory.
3. If you have previously installed our extensions using this method, make sure that the repo.ecwhim.com repository exists in your composer.json file:
```json
"repositories": [
    "ecwhim": {
        "type": "composer",
        "url": "https://repo.ecwhim.com"
    }
]
```
Otherwise, run the following command:
```shell
composer config repositories.ecwhim composer https://repo.ecwhim.com
```
4. Get the latest version of the extension:
```shell
composer require <composer-name>
```
`composer-name` can be found in [`My Downloadable Products`](https://www.ecwhim.com/downloadable/customer/products/).
5. Enter your [authentication keys](#authentication-keys). Your public key is your username; your private key is your password.
6. [Enable the extension](#enable-the-extension).

## Download package from the `My Downloadable Products` page
1. Download the latest version of the package from the [`My Downloadable Products`](https://www.ecwhim.com/downloadable/customer/products/) page.
2. Extract the package in your Magento project directory.
3. [Enable the extension](#enable-the-extension).

## Enable the extension
1. Enable the extension:
```shell
php bin/magento module:enable Ecwhim_ModuleName
```
2. Register the extension:
```shell
php bin/magento setup:upgrade
```
3. Recompile your Magento project:
```shell
php bin/magento setup:di:compile
```
4. Deploy static view files (for production mode):
```shell
php bin/magento setup:static-content:deploy
```
5. Clean the cache:
```shell
php bin/magento cache:clean
```
6. Configure the extension in Admin as needed.

## Upgrade an extension
If you used the [Download package from the `My Downloadable Products` page](#download-package-from-the-my-downloadable-products-page) method:

1. Remove all files and directories that were provided in the current extension package.
2. [Reinstall the extension](#download-package-from-the-my-downloadable-products-page).

If you [installed using Composer](#install-the-extension-using-composer), run the following commands:
```shell
composer remove <composer-name>
composer require <composer-name>
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy
php bin/magento cache:clean
```
`composer-name` can be found in [`My Downloadable Products`](https://www.ecwhim.com/downloadable/customer/products/).

## Authentication keys
You can create and manage authentication keys in [`Access Keys`](https://www.ecwhim.com/customer/accessKeys/)