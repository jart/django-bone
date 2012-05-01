.. -*-rst-*-

=============
 django-bone
=============

:name:        django-bone
:description: Generates Django Project Skeletons Simply and Properly
:copyright:   © 2011 Justine Alexandra Roberts Tunney
:license:     Licensed MIT


About
=====

django-bone = django + bootstrap + less + coffeescript + sphinx + south +
reversion + jquery + js/css minimization + debug-toolbar + gravatar +
pyflakes + pep8 + git + virtualenv + pip + tests

Starting a serious Django project? Not a newbie? Good. django-bone will save
you a few days worth of work by generating all the annoying boilerplate code
for you. One simple command is all you need to create a skeleton website with
all the infrastructure you'll need as your project grows.

Here's a screenshot of what you get:

![Django-Bone Screenshot](http://i.imgur.com/o0IHy.png)


Usage
=====

Here's how you use django-bone, assuming python/pip/virtualenv are installed::

    sudo ./install.sh
    cd /opt
    django-bone myapp

The following tools and libraries will also be configured:

- Twitter Bootstrap: The hippest way to make clean looking websites.

- lessc: Less is a very popular compiler that makes CSS easier to use by
  extending its syntax. Less is used by Twitter Bootstrap.

- coffeescript: Similar to Less, this is a compiler that gives javascript a
  more eloquent syntax that's easy to learn and requires far less typing.

- south: The standard for managing database schema changes and migrations.
  It's one of the best third party libraries available for Django and is so
  easy to use that I can't possibly imagine why you *wouldn't* want to use it.

- reversion: Allows you to enable version control on your models in the Django
  Admin.  The generated Article model (commented-out) serves as an example of
  how to use this.

- django-debug-toolbar: A very popular tool for debugging everything.  This
  will magically appear when in development mode.

- sphinx: Generates the prettiest documentation.  Inline autodoc style is used
  by the generated code.

- pip/virtualenv: The smartest way to install unstable Python software.

- jquery: Who doesn't use jquery?

- modernizr: Helps you use hip HTML5 features with cross browser support.

Django 1.4 is used with the following cool features configured:

- Time zone awareness
- The secure password hashing extension I wrote!
- Cross-site request forgery (CSRF) protection
- Browser-side session data storage (signed cookies)
- Internationalization (localization must be used explicitly)
- Static file framework
- Logging / error reporting system
- Memcached and cached template loading

Here's the files django-bone generates for you:

- ``README.rst``: A simple README file using RestructuredText markup.

- ``doc/index.rst``: Your main sphinx documentation page.

- ``setup.py``: All Python projects should have this!  Even if you don't want
  to put your program on the cheese shop.

- ``scripts/myapp``: Command that gets installed to your bin/ folder.  This
  replaces ``./manage.py --settings=myapp.settings``.

- ``scripts/myapp-dev``: Command that gets installed to your bin/ folder.
  This replaces ``./manage.py --settings=myapp.settings_dev``.

- ``.gitignore``: Preloaded with a list I've built over the years.

- ``conf/init.d/myapp``: This is a script for linux systems to automate
  starting/stopping the gunicorn backend webserver.

- ``conf/nginx/myapp.com.conf``: Shows you how to configure nginx to reverse
  proxy to your gunicorn server.

- ``myapp/urls.py``: A simple URL dispatcher.

- ``myapp/views.py``: Provides an index page view to get you started.

- ``myapp/models.py``: A placeholder for your database tables.

- ``myapp/middleware.py``: Some middleware classes that fix stuff.

- ``myapp/settings.py``: All my favorite production defaults!

- ``myapp/settings_dev.py``: DEBUG mode settings.  This overloads
  ``settings.py``.

- ``myapp/settings_local.py``: Overload settings ONLY for this install.

- ``myapp/tests.py``: Provides a few simple regression tests to make it easy
  for you to get you started with automated testing.  Only amateur software
  engineers forget to write tests so I figured you might want these.

- ``myapp/admin.py``: Gets you started customizing Django admin gui.

- ``myapp/management/commands/minify.py``: A happy js/css/png minify command.

- ``myapp/templates/myapp/base.html``: Master HTML5 template based on
  html5boilerplate.com

- ``myapp/templates/myapp/index.html``: Home page (overrides base.html)

- ``myapp/media/myapp/css/myapp.css``: Main CSS file based off normalize.css
  and html5boilerplate.com

- ``myapp/media/myapp/js/myapp.js``: Placeholder for your javascript code.

- ``myapp/templates/404.html``: Page not found page.

- ``myapp/templates/500.html``: Internal server error page.
