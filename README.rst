.. role:: bash(code)
   :language: bash

Jack Bower
==========

Installing frontend Django dependencies via bower.

Installation
------------

To get the latest stable release from PyPi

.. code-block:: bash

    $ pip install jack-bower

Add ``bower`` to your ``INSTALLED_APPS``

.. code-block:: python

    INSTALLED_APPS = (
        ...,
        'bower',
    )


Usage
-----

Use :bash:`./manage.py bower_init <app_name>` to bootstrap an app with
a ``bower.json``. Add your dependencies to it:

.. code-block:: javascript

    {
        "dependencies": {
            "backbone": "1.0.0",
            "underscore": "1.4.4"
        }
    }

Then just run :bash:`./manage.py bower_install` and it'll install all the
dependencies in all the ``INSTALLED_APPS`` apps that has a
``bower.json``. Add a ``.bowerrc`` file in your project root to control where
packages are installed.
