# Drupal 8 Migrate

A quickstart project for Drupal 8 migrations.

## Requirements

- [Composer](https://getcomposer.org/), [Install Composer Globally](https://getcomposer.org/doc/00-intro.md#globally)
- A Drupal 7 Source site. (The site to be upgraded.)
- A Drupal 8 Target site. (The site to upgrade to.)

## Getting Started

- Backup the Drupal 7 source site and setup a copy locally.
- Setup the Drupal 8 target site locally also. 
  - **Note:** _Do not add any content or otherwise to the D8 site or it will be lost in the migration process._

###  Install Drupal 8 with Composer

Run the following command to install a Drupal 8 site with dependencies managed by Composer.

    composer create-project drupal-composer/drupal-project:8.x-dev some-dir --no-interaction

**Note:** _This composer create-project process will take several minutes to complete._

### Enable Drupal 8 Migration Modules

The following modules need to be enabled in order to perform a migration.

- Mirate 
- Migrate Drupal
- Migrate Drupal UI

### Run Upgrade Migration Checks

- Visit http://source7.local/upgrade and enter the Drupal 7 Source site's database connection settings.
- Run the upgrade migration check if the connection to the DB was successful.
  - Check DB connection settings in settings.php on the Drupal 7 site if connection fails.
  - See Known Issues below for DB issues inside container tools like DDEV.


## Known Issues

- Database connection issues in DDEV.
  - A VM seems to work much better for DB connection compatibility.
