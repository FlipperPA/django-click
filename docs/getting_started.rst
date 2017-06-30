===============
Getting Started
===============

.. _installation:

Installation
============

Django Click can be installed from PyPI.

    pip install django-click

.. _your-first-command:

Your First Command
==================

Django Click allows you to use Click's rich feature set with your Django project. For example, the following code could be placed in `yourapp/management/commands/hello_world.py`:

.. code-block:: python

    import djclick as click

    @click.command()
    @click.argument('name')
    def command(name):
        click.secho('Hello, {}'.format(name), fg='red')

To call the command, use Django's `manage.py`:

.. code-block:: bash

    python manage.py hello_world Hal9000
