You can use this as a start point for managing a WordPress install with git.

See '[Install and manage WordPress with Git](http://davidwinter.me/articles/2012/04/09/install-and-manage-wordpress-with-git/)' for more details.

## Setup

You can either run:

	rake

Or manually run:

	git submodule update --init

Then copy `wp-config-sample.php` to `wp-config.php`, update your database settings, and your default theme.

## Updating WordPress

You can use the Rake helper task to upgrade WordPress to a specific version:

	rake wordpress_update[3.7.1]
