# WooCommerce Order Tables
Managed WooCommerce plugin for Liquid Web.

## Background & Purpose
WooCommerce even with CRUD classes in core, still uses a custom post type for orders. By moving orders to use a custom table in the site database, will improve store orders performance.

### Here's how

WooCommerce saves more than 40 custom fields per order— including those from plugins— inside the wp_postmeta table. If your store gets ~40 per day, that's 1600 rows (40 * 40) added to the postmeta table in a day. 

In one month that number can be 48,000 new rows (1600 * 30) added to your postmeta table. The more rows in a table the longer it will take for a query to execute. WooCommerce Order Tables creates a new table for WooCommerce orders which would cut that number tremendously by making each custom field into a column so that 1 order = 1 row.

## Installation
This plugin uses a Composer autoloader. If you are working with code from the `master` branch in a development environment, the autoloader needs to be generated in order for the plugin to work. After cloning this repository, run `composer install` in the root directory of the plugin.

The packaged version of this plugin, which is available in [releases](https://github.com/liquidweb/WooCommerce-Order-Tables/releases), contains the autoloader. This means that end users should not need to worry about running the `composer install` command to get things working. Just grab the latest release and go, but be sure to backup your database first!


