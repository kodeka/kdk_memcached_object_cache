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

## License
GNU/GPL v2

## Authors
Fotis Alexandrou using code from Scott Taylor, Ryan Boren, Denis de Bernardy, Matt Martz, Mike Schroder, Mika Epstein.
