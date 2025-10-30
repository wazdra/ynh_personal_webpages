# Personal Webpages for YunoHost

[![Integration level](https://dash.yunohost.org/integration/example.svg)](https://dash.yunohost.org/appci/app/example)
[![Install Example app with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=example)

*[Lire ce readme en français.](./README_fr.md)*

> *This package allows you to install Example app quickly and simply on a YunoHost server.
If you don't have YunoHost, please consult [the guide](https://yunohost.org/#/install) to learn how to install it.*

## Overview

Serve static personal webpages for each SSH-enabled user under /people/~username. Content is read from /home/USERNAME/public_html and served by Nginx without PHP.

### Features

* URL scheme: /PATH/~username (default path: /people)
* Static files only (no PHP/CGI), no symlinks, dotfiles hidden (except .well-known)
* Users upload via SFTP to ~/public_html
* Public access by default


**Shipped version:** 0.1.0~ynh1

**Demo:** <https://demo.example.com>

## Screenshots

![Screenshot of Example app](./doc/screenshots/example.jpg)

## Disclaimers / important information

* Limitations in v1:
  * Only serves users in SSH group; multi-domain mapping is not yet implemented (served on chosen domain/path).
  * No quotas. No directory listing. Large files allowed.
  * Backups include Nginx config, data_dir structure, and provisioning helper; user content remains in home directories.

## Documentation and resources

* Official app website: <https://example.com>
* Official user documentation: <https://yunohost.org/apps>
* Official admin documentation: <https://yunohost.org/packaging_apps>
* Upstream app code repository: <https://some.forge.com/example/example>
* YunoHost documentation for this app: <https://yunohost.org/app_example>
* Report a bug: <https://github.com/YunoHost-Apps/example_ynh/issues>

## Developer info

Please send your pull request to the [testing branch](https://github.com/YunoHost-Apps/example_ynh/tree/testing).

To try the testing branch, please proceed like that.

``` bash
sudo yunohost app install https://github.com/YunoHost-Apps/example_ynh/tree/testing --debug
or
sudo yunohost app upgrade example -u https://github.com/YunoHost-Apps/example_ynh/tree/testing --debug
```

**More info regarding app packaging:** <https://yunohost.org/packaging_apps>
