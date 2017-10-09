# A WordPress Plugin Developers VVV

This is an [auto-sitesetup](https://github.com/Varying-Vagrant-Vagrants/VVV/wiki/Auto-site-Setup) designed to be used with [Varying Vagrants Vagrant](https://github.com/Varying-Vagrant-Vagrants/VVV) for developing WordPress Plugins.

## To get started:

1. Clone this repo to your VVV/`www` folder
2. Update to a [release tag](https://github.com/patilswapnilv/wordpress-plugin-dev-vvv/releases) to keep stable
3. If your Vagrant is running, from the Vagrant directory run `vagrant halt` followed by `vagrant up --provision`.

Perhaps a cup of tea or coffee now? The provisioning may take a while.

Then you can visit [http://wp.plugin.dev](https://wp.plugin.dev) to start developing or reviewing themes.

## Dependencies

- [Varying Vagrants Vagrant](https://github.com/Varying-Vagrant-Vagrants/VVV) - [Installation guide](https://github.com/Varying-Vagrant-Vagrants/VVV#the-first-vagrant-up)
- [vagrant-hostsupdater](https://github.com/cogitatio/vagrant-hostsupdater) - Install with `vagrant plugin install vagrant-hostsupdater`

## What will happen?

- Install WordPress and import "Test Data" from [WP tests by Post Status](https://github.com/poststatus/wptest)
- Install a bunch of developer plugins you'll need
- Install any `.zip` plugin located in the root

## Credentials and Such

### Plugin Development

* Username: `admin`
* Password: `password`
* Login: [login](https://wp.plugin.dev/wp-admin)

### MySQL Root

* User: `root`
* Pass: `root`
* See: [Connecting to MySQL](https://github.com/varying-vagrant-vagrants/vvv/wiki/Connecting-to-MySQL) from your local machine

# Reviewing Themes

If you drop a plugin's `.zip` file into the root folder (not htdocs) provisioning will automatically install the theme ready for activation.

Yes, drop six zip files and all six plugins will install automagically.

## To start over (building another plugin):

You can do it the soft way using (I know it's long, Text Expander?) `vagrant ssh -c 'cd /home/vagrant/www/wordpress-plugindev-vvv/ && rm -Rf htdocs/ && sh vvv-init.sh'`. Or, you can do it the hard way `vagrant reload --provision` and get a cup of coffee.

_________________________

# Changelog

## 1.0

- The beginning
