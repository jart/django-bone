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

Starting a new Django project?  django-bone will save you a day's
worth of work by generating all the annoying boilerplate code for you.
One simple command is all that's needed to set up everything you'd
expect from a bona-fide python project: standard source code layout,
setup.py, sphinx documentation, unit tests, version control,
virtualenv, db migrations, nginx config, init.d file, jquery,
deployment scripts, pretty css, etc.


Usage
=====

Installation::

    sudo cp -a django-bone /usr/local/bin
    sudo chmod go+rwt /opt  # let people create *NEW* files in /opt

Create a new project::

    cd /opt
    django-bone myapp
    cd myapp/myapp
    source ../bin/activate
    myapp-dev runserver

Your project will be configured to use the following tools/libraries:

- south: The standard for managing database schema changes and
  migrations.  It's one of the best third party libraries available
  for Django and is so easy to use that I can't possibly imagine why
  you *wouldn't* want to use it.

- django-debug-toolbar: A very popular tool for debugging everything.
  This will magically appear when in development mode.

- virtualenv: Excellent and very popular tool for compartmentalizing
  python software installations.

- pip: The successor of easy_install.

- sphinx: The standard for documentation.

Here are the files django-bone generates for you:

- ``README.rst``: A simple README file using RestructuredText markup.

- ``doc/index.rst``: Your main sphinx documentation page.

- ``setup.py``: All Python projects should have this!  Even if you
  don't want to put your program on the cheese shop.

- ``scripts/myapp``: Command that gets installed to your bin/ folder.
  This replaces ``./manage.py --settings=myapp.settings``.

- ``scripts/myapp-dev``: Command that gets installed to your bin/
  folder.  This replaces ``./manage.py --settings=myapp.settings_dev``.

- ``.gitignore``: Preloaded with a list I've built over the years.

- ``conf/init.d/myapp``: This is a script for linux systems to
  automate starting/stopping the gunicorn backend webserver.

- ``conf/nginx/myapp.com.conf``: Shows you how to configure nginx to
  reverse proxy to your gunicorn server.

- ``myapp/urls.py``: A simple URL dispatcher.

- ``myapp/views.py``: Provides an index page view to get you started.

- ``myapp/models.py``: A placeholder for your database tables.

- ``myapp/middleware.py``: Some middleware classes that fix stuff.

- ``myapp/settings.py``: All my favorite production defaults!

- ``myapp/settings_dev.py``: DEBUG mode settings.  This overloads
  ``settings.py``.

- ``myapp/settings_local.py``: Overload settings ONLY for this install.

- ``myapp/tests.py``: Provides a few simple regression tests to make
  it easy for you to get you started with automated testing.  If you
  don't write tests, now's the time to start because not doing so is
  irresponsible engineering.

- ``myapp/admin.py``: Gets you started customizing Django admin gui.

- ``myapp/media/myapp/js/jquery.min.js``: How could we live without it?

- ``myapp/media/myapp/css/myapp.js``: A basic stylesheet.

- ``myapp/media/myapp/img/favicon.png``: Anarchist symbolism.

- ``myapp/templates/myapp/base.html``: Master HTML file.

- ``myapp/templates/myapp/index.html``: Home page that overrides base.html.

- ``myapp/templates/404.html``: Page not found page.

- ``myapp/templates/500.html``: Internal server error page.

- ``myapp/management/commands/example.py``: Example subcommand.
