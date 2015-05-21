# Drushenv

A command line tool to manage local drush installations, similar to [rbenv](https://github.com/sstephenson/rbenv) or [phpenv](https://github.com/phpenv/phpenv).

Build with https://github.com/mislav/everyenv

---

# Installation

This will get you going with the latest version of drushenv and make it
easy to fork and contribute any changes back upstream.

1. Check out drushenv into `~/.drushenv`.

    ~~~ sh
    $ git clone https://github.com/webflo/drushenv.git ~/.drushenv
    ~~~

2. Add `~/.drushenv/bin` to your `$PATH` for access to the `drushenv`
   command-line utility.

    ~~~ sh
    $ echo 'export PATH="$HOME/.drushenv/bin:$PATH"' >> ~/.bash_profile
    ~~~

    **Ubuntu Desktop note**: Modify your `~/.bashrc` instead of `~/.bash_profile`.

    **Zsh note**: Modify your `~/.zshrc` file instead of `~/.bash_profile`.

3. Add `drushenv init` to your shell to enable shims and autocompletion.

    ~~~ sh
    $ echo 'eval "$(drushenv init -)"' >> ~/.bash_profile
    ~~~

    _Same as in previous step, use `~/.bashrc` on Ubuntu, or `~/.zshrc` for Zsh._

4. Restart your shell so that PATH changes take effect. (Opening a new
   terminal tab will usually do it.) Now check if drushenv was set up:

    ~~~ sh
    $ type drushenv
    #=> "drushenv is a function"
    ~~~

# Installing Drush Versions

Drushenv ships with a handy command to install various drush version with composer.

**tl;dr**

```
# Installs the latest stable version of Drush 7.
drushenv install 7 '~7.0'

# Installs the latest dev version of Drush 8.
drushenv install 8 '~8.0@dev'
```

The first argument is local drush version alias in `~/.drushenv/versions`, the second argument is a composer version constaint for `drush/drush`.

---

Build with https://github.com/mislav/everyenv
