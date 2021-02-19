# KDK Memcached Object Cache (v1.1 / Feb 2021)
Object cache driver for Memcached in WordPress.

Based on Memcached Redux with corrections for handling Memcached connections and an option to have multiple Memcached backends (defined as an array in wp-config.php).


## Installation

Download the repo from https://github.com/kodeka/kdk_memcached_object_cache/archive/master.zip and extract it.

Upload the object-cache.php file to your WordPress site's /wp-content/ folder.

Setup multiple Memcached backends by defining them in wp-config.php like so:

Example:
```
# Place in wp-config.php & adjust accordingly
function get_memcached_servers () {
    return array(
        '127.0.0.1:11211',
        '10.1.1.1:11211',
        'production.cache.amazonaws.com:11211'
    );
}
```

Any WordPress caching plugin that offers in-memory object caching (e.g. [WP Rocket](https://wp-rocket.me/)) can now utilize this object cache driver to store cache objects in Memcached backends.

Enjoy :)


## License & Credits

Maintained by Kodeka OÜ.

Big thanks to [Fotis Alexandrou](https://github.com/falexandrou) for patching and extending [Memcached Redux](https://wordpress.org/plugins/memcached-redux/) (which uses code from Scott Taylor, Ryan Boren, Denis de Bernardy, Matt Martz, Mike Schroder, Mika Epstein). Silence is not golden m/f.

Licensed under the GNU/GPL license (https://www.gnu.org/copyleft/gpl.html).

Copyright (c) 2018 - 2021 Kodeka OÜ. All rights reserved.
