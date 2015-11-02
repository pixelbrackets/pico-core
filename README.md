Pico
====

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://scrutinizer-ci.com/g/theshka/Pico/build-status/LICENSE)
[![Version](https://img.shields.io/badge/version-1.0-lightgrey.svg)](https://github.com/picocms/Pico/releases/latest)
[![Build Status](https://scrutinizer-ci.com/g/theshka/Pico/badges/build.png?b=master)](https://scrutinizer-ci.com/g/theshka/Pico/build-status/master)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/theshka/Pico/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/theshka/Pico/?branch=master)

Pico is a stupidly simple, blazing fast, flat file CMS. See http://picocms.org/ for more info.

<!--flippa verify-->
[![I Love Open Source](http://www.iloveopensource.io/images/logo-lightbg.png)](http://www.iloveopensource.io/projects/524c55dcca7964c617000756)

Install
-------

You can install Pico either using a pre-bundled release or with composer. Pico requires PHP 5.3+

#### Using a pre-bundled release

Just [download the latest Pico release][LatestRelease] and upload all files to the `httpdocs` directory (e.g. `/var/www/html`) of your server.

#### Composer

###### Step 1 - for users
[Download the *source code* of Picos latest release][LatestRelease], upload all files to the `httpdocs` directory (e.g. `/var/www/html`) of your server and navigate to the upload directory using a shell.

###### Step 1 - for developers
Open a shell and navigate to the desired install directory of Pico within the `httpdocs` directory (e.g. `/var/www/html`) of your server. You can now clone Picos Git repository as follows:
```shell
$ git clone https://github.com/picocms/Pico.git .
```
Please note that this gives you the current development version of Pico, what is likely *unstable* and *not ready for production use*!

###### Step 2
Download [composer][] and run it with the `install` option:
```shell
$ curl -sS https://getcomposer.org/installer | php
$ php composer.phar install
```

Upgrade
-------

Upgrading Pico is very easy: You just have to replace all of Picos files - that's it! Nevertheless you should *always* create a backup of your Pico installation before upgrading.

Pico follows [Semantic Versioning 2.0][SemVer] and uses version numbers like `MAJOR`.`MINOR`.`PATCH`. When we update...

- the `PATCH` version (e.g. `1.0.0` to `1.0.1`), we made backwards-compatible bug fixes. It's then sufficient to extract [Picos latest release][LatestRelease] to your existing installation directory and overwriting all files.
- the `MINOR` version (e.g. `1.0` to `1.1`), we added functionality in a backwards-compatible manner, but anyway recommend you to "install" Pico newly. Backup all of your files, empty your installation directory and install Pico as elucidated above. You can then copy your `config/config.php` and `content` directory without any change. If applicable, you can also copy the folder of your custom theme within the `themes` directory. Provided that you're using plugins, also copy all of your plugins from the `plugins` directory.
- the `MAJOR` version (e.g. `1.0` to `2.0`), a appropriate upgrade tutorial will be provided.

Upgrading Pico 0.8 or 0.9 to Pico 1.0 is a special case. The new `PicoDeprecated` plugin ensures backwards compatibility, so you basically can follow the above upgrade instructions as if we updated the `MINOR` version. However, we recommend you to take some further steps to confine the neccessity of `PicoDeprecated` as far as possible. For more information about what has changed with Pico 1.0 and a step-by-step upgrade tutorial, please refer to the [upgrade page of our website][UpgradeNotes].

Run
---

You have nothing to consider specially, simply navigate to your Pico install using your favourite web browser. Picos default contents will explain how to use your brand new, stupidly simple, blazing fast, flat file CMS.

#### You don't have a web server?
Starting with PHP 5.4 the easiest way to try Pico is using [the built-in web server of PHP][PHPServer]. Please note that PHPs built-in web server is for development and testing purposes only!

###### Step 1
Navigate to Picos installation directory using a shell.

###### Step 2
Start PHPs built-in web server:
```shell
$ php -S 127.0.0.1:8080
```

###### Step 3
Access Pico from <http://localhost:8080>.

Getting Help
------------

You can read the [Wiki][] if you are looking for examples and read the inline-docs for more development information.

If you find a bug please report it on the issues page, but remember to include as much detail as possible, and what someone can do to re-create the issue.

Issues with plugins should be reported on the offending plugins homepage, same goes for themes.

Contributing
------------

You want to contribute to Pico? We really appreciate that! You can help making Pico better by [contributing code][PullRequests] or [reporting issues][Issues], but please take note of our [contribution guidelines][ContributionGuidelines]. In general you can contribute in four different areas:

1. Issues: You have a problem with Pico? Please don't hesitate to create a new [Issue][Issues] on GitHub! Concerning problems with plugins or themes, please refer to the website of the developer of this plugin or theme.
2. Plugins & Themes: You're a plugin developer or theme designer? We love you guys! You can find tons of information about how to develop plugins and themes at http://picocms.org/plugin-dev.html. If you have created a plugin or theme, please add it to our [Wiki][], either on the [plugins][WikiPlugins] or [themes page][WikiThemes]. Maybe we will then promote your plugin or theme on [our website][OfficialPlugins] as officially supported!
3. Documentation: We always appreciate people improving our documentation. You can either improve the [inline user docs][InlineUserDocs] or the more extensive [user docs on our website][WebsiteUserDocs]. You can also improve the [docs for plugin and theme developers][WebsiteDevDocs]. Simply fork Pico from https://github.com/picocms/Pico, change the Markdown files and open a [pull request][PullRequests].
4. Picos Core: The supreme discipline is to work on Picos Core. Your contribution should help *every* Pico user to have a better experience with Pico. If this is the case, fork Pico from https://github.com/picocms/Pico and open a [pull request][PullRequests]. We look forward to your contribution!

[LatestRelease]: https://github.com/picocms/Pico/releases/latest
[composer]: https://getcomposer.org/
[SemVer]: http://semver.org
[UpgradeNotes]: http://picocms.org/upgrade.html
[PHPServer]: http://php.net/manual/en/features.commandline.webserver.php
[PullRequests]: https://github.com/picocms/Pico/pulls
[Issues]: https://github.com/picocms/Pico/issues
[ContributionGuidelines]: https://github.com/picocms/Pico/blob/master/CONTRIBUTING.md
[Wiki]: https://github.com/picocms/Pico/wiki
[WikiPlugins]: https://github.com/picocms/Pico/wiki/Pico-Plugins
[WikiThemes]: https://github.com/picocms/Pico/wiki/Pico-Themes
[OfficialPlugins]: http://picocms.org/plugins.html
[InlineUserDocs]: https://github.com/picocms/Pico/blob/master/content-sample/index.md
[WebsiteUserDocs]: https://github.com/picocms/Pico/tree/gh-pages/_docs
[WebsiteDevDocs]: https://github.com/picocms/Pico/tree/gh-pages/_plugin-dev
