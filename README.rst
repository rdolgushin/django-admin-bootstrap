Fat-free django-admin-bootstrap
===============================

Differences from original django-admin-bootstrap
------------------------------------------------

- No annoying spinner overlay
- Hidden-but-jumping-on-every-page-reload sidebar is fixed
- No CSS transitions
- No default branding

Screenshots
-----------

.. image:: https://raw.githubusercontent.com/rdolgushin/django-admin-bootstrap/master/screenshots/screenshot.png
    :target: https://github.com/rdolgushin/django-admin-bootstrap/tree/master/screenshots
    :alt: See Screenshots

`More screenshots <https://github.com/rdolgushin/django-admin-bootstrap/tree/master/screenshots>`_

Installation
------------

    $ pip install git+https://github.com/rdolgushin/django-admin-bootstrap

Settings:

.. code-block:: python

    INSTALLED_APPS = (
        # ...
        'bootstrap_admin', # always before django.contrib.admin
        'django.contrib.admin',      
        # ...   
    )

    # For Sidebar Menu (List of apps and models) (RECOMMENDED)
    from django.conf import global_settings
    TEMPLATE_CONTEXT_PROCESSORS = global_settings.TEMPLATE_CONTEXT_PROCESSORS + (
        'django.core.context_processors.request',
    )
    BOOTSTRAP_ADMIN_SIDEBAR_MENU = True
