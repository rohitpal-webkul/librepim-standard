# **LibrePIM – Community-Maintained Fork of the Akeneo PIM Community Edition**

Welcome to **LibrePIM**, an independent and community-driven fork of the **Akeneo PIM Community Edition**.
LibrePIM aims to provide long-term maintenance, stability, and compatibility for teams relying on the open-source PIM ecosystem.

LibrePIM focuses on:

* Security updates and bug fixes
* Performance and dependency improvements
* Community contributions and transparency
* A familiar and compatible migration path from Akeneo PIM Community Edition

This repository helps you create a new PIM project based on LibrePIM.

---

## **Contributing & Development**

Development happens in the main repository:
🔗 [https://github.com/libre-pim/librepim-dev](https://github.com/libre-pim/librepim-dev)

If you would like to contribute:

* Fork [https://github.com/libre-pim/librepim-dev](https://github.com/libre-pim/librepim-dev)
* Submit a pull request with your changes
* Open issues or feature requests here: [https://github.com/libre-pim/librepim-dev/issues](https://github.com/libre-pim/librepim-dev/issues)

Community participation is welcome and appreciated.

---

# **Installation Instructions**

## Development Installation with Docker

### **Requirements**

* Docker 19+
* docker-compose ≥ 1.24
* make

### **Create a project and start LibrePIM**

Run the following commands in an **empty directory**:

```bash
docker run -u www-data -v $(pwd):/srv/pim -w /srv/pim --rm akeneo/pim-php-dev:8.1 \
    php /usr/local/bin/composer create-project --prefer-dist \
    libre-pim/librepim-standard /srv/pim "master"
```

```bash
make
```

LibrePIM will be available at:
➡️ **[http://localhost:8080/](http://localhost:8080/)**
Default credentials: **admin / admin**

To stop the PIM:

```
make down
```

---

## **Installation Without Docker**

```bash
php /usr/local/bin/composer create-project --prefer-dist \
    libre-pim/librepim-standard /srv/pim "master"
```

Configure `.env` with your MySQL and Elasticsearch credentials.

Then run:

```
NO_DOCKER=true make
```

For more details, refer to the Akeneo installation guide:
[https://docs.akeneo.com/master/install_pim](https://docs.akeneo.com/master/install_pim)

---

# **Migrating from Akeneo PIM Community Edition**

LibrePIM maintains compatibility with Akeneo PIM CE, allowing for a smooth migration.
A migration guide will be available in the documentation.

---

# **Upgrade Instructions**

LibrePIM currently follows the Akeneo CE upgrade workflow.

For upgrade details, see:
[https://docs.akeneo.com/master/migrate_pim/index.html](https://docs.akeneo.com/master/migrate_pim/index.html)

---

# **Changelog**

You can view the changelog here:
[https://github.com/libre-pim/librepim-dev](https://github.com/libre-pim/librepim-dev)

---

# **Support & Community**

* **Development Repository:** [https://github.com/libre-pim/librepim-dev](https://github.com/libre-pim/librepim-dev)
* **Issue Tracker:** [https://github.com/libre-pim/librepim-dev/issues](https://github.com/libre-pim/librepim-dev/issues)
* **Standard Edition:** [https://github.com/libre-pim/librepim-standard](https://github.com/libre-pim/librepim-standard)

---

# **License**

LibrePIM is licensed under the **Open Software License 3.0 (OSL-3.0)**.
See `LICENSE.txt` for details.

---

# **About Akeneo**

LibrePIM is independently developed and originates from the openly licensed
**Akeneo PIM Community Edition (OSL-3.0)**.

For more information about Akeneo, visit:
[https://www.akeneo.com/](https://www.akeneo.com/)
 
