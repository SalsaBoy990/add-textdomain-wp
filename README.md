# add-textdomain-wp

Add textdomain for gettext functions (`__('', '')` etc.) to enable internationalization (i18n) for Wordpress plugins

Source of the code: wordpress-i18n
https://i18n.svn.wordpress.org/tools/trunk/add-textdomain.php

The `require`d php files for `add-textdomain.php` also included.

[More info...](https://codex.wordpress.org/I18n_for_WordPress_Developers)

## Install

Copy these files and the `pomo` folder to your `wp-content` folder of your WP site.


## Usage

Run example:
`php add-textdomain -i your-textdomain plugins/your-plugin-name/your-plugin-name.php`

After automatically adding textdomains, make a `.pot` file with wp cli:

`wp i18n make-pot plugins/your-plugin-name plugins/your-plugin-name/languages/your-textdomain.pot`

Create translation files (`.po` and `.mo`) with [Poedit](https://poedit.net/) or similar software.

Choose your own language. Translate the strings.

Name your translation files like this:
Example for Hungarian language:
`your-textdomain-hu_HU.po`

## Install WP CLI on Windows

1. Download [wp-cli.phar](https://raw.github.com/wp-cli/builds/gh-pages/phar/wp-cli.phar)
2. Create folder here: `C:\wp-cli`
3. Copy `wp-cli.phar` to that folder
4. Create a `wp.bat` file in that folder with the content:


  @ECHO OFF
  php "c:/wp-cli/wp-cli.phar" %*


5. Add PATH env variable: "C:\wp-cli"
6. Use wp in command line

See more at: https://make.wordpress.org/cli/handbook/guides/installing/

