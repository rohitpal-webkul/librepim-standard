LibrePIM - Official Akeneo PIM Community Edition Fork
======================================================

Welcome to LibrePIM - A Community-Driven Fork of Akeneo PIM

**LibrePIM** is an official community fork of Akeneo PIM Community Edition, dedicated to providing:
- Security patches and bug fixes
- Performance improvements
- Community-driven development
- Easy migration path from Akeneo PIM Community Edition

This repository is used to create a new PIM project based on LibrePIM (forked from Akeneo PIM).

### Contributing & Development

For development and feature requests, please visit: https://github.com/libre-pim/librepim-dev

If you want to contribute to LibrePIM, you can fork the repository https://github.com/libre-pim/librepim-dev and submit a pull request.

To report issues or suggest improvements, please use: https://github.com/libre-pim/librepim-dev/issues

Installation instructions
-------------------------

### Development Installation with Docker

## Requirements
 - Docker 19+
 - docker-compose >= 1.24
 - make

## Creating a project and starting the PIM
The following steps will install LibrePIM in the current directory (must be empty) and launch it from there:

```bash
$ docker run -u www-data -v $(pwd):/srv/pim -w /srv/pim --rm akeneo/pim-php-dev:8.1 \
    php /usr/local/bin/composer create-project --prefer-dist \
    libre-pim/librepim-standard /srv/pim "master"
```
```
$ make

```

The PIM will be available on http://localhost:8080/, with `admin/admin` as default credentials.

To shutdown your PIM: `make down`

### Installation without Docker


```bash
$ php /usr/local/bin/composer create-project --prefer-dist libre-pim/librepim-standard /srv/pim "master"
```

You will need to change the `.env` file to configure the access to your MySQL and ES server.

Once done, you can run:

```
$ NO_DOCKER=true make
```

For more details, please follow https://docs.akeneo.com/master/install_pim

### Migrating from Akeneo PIM Community Edition

If you're currently using Akeneo PIM Community Edition and want to migrate to LibrePIM, the process is straightforward as LibrePIM maintains compatibility with Akeneo PIM Community Edition. Please refer to the migration guide in the documentation.

Upgrade instructions
--------------------

To upgrade LibrePIM to a newer version, please follow the Akeneo upgrade guide:
https://docs.akeneo.com/master/migrate_pim/index.html

LibrePIM maintains compatibility with Akeneo PIM upgrades, so you can use the official Akeneo upgrade instructions.

Changelog
---------
You can check out the changelog files in https://github.com/libre-pim/librepim-dev.

### Support & Community

- **Development Repository**: https://github.com/libre-pim/librepim-dev
- **Issue Tracker**: https://github.com/libre-pim/librepim-dev/issues
- **Standard Edition**: https://github.com/libre-pim/librepim-standard

### License

LibrePIM is licensed under the Open Software License 3.0 (OSL-3.0). See LICENCE.txt for more information.

### About Akeneo

LibrePIM is a fork of Akeneo PIM Community Edition. For more information about Akeneo, visit https://www.akeneo.com/
