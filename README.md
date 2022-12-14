# Level0 OpenStreetMap Editor

[![Level0 logo made by Midgard](level0.png)](level0.svg)

This is a text-based in-browser editor for OSM data. See [its wiki page](http://wiki.openstreetmap.org/wiki/Level0) and [language guide](http://wiki.openstreetmap.org/wiki/Level0L).

## Installation

You will need PHP with `mod_gettext`.

* Clone this repo somewhere. Make `www` a document root directory. (In any case make sure to keep the location of the includes directory relative to the document root the same.)
* Set up HTTPS. It is necessary to protect your users from attacks that take over their account.
* Open [this link](https://www.openstreetmap.org/user/username/oauth_clients/new) and register your instance of Level0. It needs permissions for reading user details and modifying the map. The callback URL should be the base URL for your application with `?action=callback` appended. Example: `https://level0.example.org/?action=callback`
* Edit `config.php`, inserting the OAuth client ID and secret the OpenStreetMap website gives you.
* Create `data` directory and give writing permissions for it to web server process. Check path in `config.php`.
* Check path to document root in `locales/deploy_locales` and run it.

You're set: download some data in the editor and login to OSM.

Oh, one more thing: there will be a lot of `.base` files in the data directory. To clean them, run `crontab -e` and add this line (change path accordingly):

    0 * * * * find /var/www/level0/data -type f -mtime 1 -delete

## Translation

Localization strings are managed with [Transifex](https://www.transifex.com/projects/p/level0/). There are not many of them, please add a translation for your language when you have time.

## License and authors

Level0 is written by Ilya Zverev and published under WTFPL license.
Modifications by Midgard released under the same license.

The bundled [Leaflet library](https://leafletjs.com/) (in www/vendor/leaflet0.7.7) is licensed under its own license, included in [www/vendor/leaflet0.7.7/LICENSE](www/vendor/leaflet0.7.7/LICENSE).
