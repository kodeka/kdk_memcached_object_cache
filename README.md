# WP Memcached Object Cache
Object cache driver for Memcached in WordPress.

Based on Memcached Redux with fixes for closing Memcached connections and an option to have multiple Memcached backends (defined as an array in wp-config.php).

## Install
Upload this file to your WordPress site's /wp-content/ folder.

Setup multiple Memcached backends by defining them in wp-config.

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

Any WordPress caching plugin that offers in-memory object caching (e.g. [W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/), [WP Rocket](https://wp-rocket.me/) etc.) can now utilize this object cache driver to store cache objects in Memcached backends.

Enjoy :)

## License
GNU/GPL v2

## Authors
Big thanks to [Fotis Alexandrou](https://github.com/falexandrou) for patching and extending [Memcached Redux](https://wordpress.org/plugins/memcached-redux/) (which uses code from Scott Taylor, Ryan Boren, Denis de Bernardy, Matt Martz, Mike Schroder, Mika Epstein). Silence is not golden m/f.
