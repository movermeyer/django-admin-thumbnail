django_admin_thumbnail
======================
This is a package developed to help you with ImageField visualization in your ModelAdmin. It automatically creates user friendly thumbnail for any ImageField you choose to put in your list_display.

All you have to do is to switch from *ModelAdmin* to *ThumbAdmin* subclass. It's super easy to use:

.. contents::

Usage
-----

Insert **admin_thumbnail** to the end of your INSTALLED_APPS in settings.py::

    INSTALLED_APPS = (
        ...
        'admin_thumbnail',
        ...
    )

Now, your ModelAdmin must look like this::

    from models import ModelExample
    from admin_thumbnail.thumb_admin import ThumbAdmin
    from django.contrib import admin

    class ModelExampleAdmin(ThumbAdmin):
        list_display = ('a_image_field',)

    admin.register(ModelExample, ModelExampleAdmin)

Yes! It's THAT simple!

Requirements
------------
* `Django 1.4+ <http://pypi.python.org/pypi/Django/1.4>`_
* `sorl.thumbnail 11.12+ <http://pypi.python.org/pypi/sorl-thumbnail/11.12>`_
* `PIL 1.1.6+ <http://pypi.python.org/pypi/PIL/1.1.6>`_

Installation
------------
Install using pip::

    pip install django-admin-thumbnail

Check This Out
--------------
1. `GitHub Repository <https://github.com/fjcaetano/django_admin_thumbnail>`_
2. `Owner website <http://flaviocaetano.com>`_
3. `PyPi package <http://pypi.python.org/pypi/django_admin_thumbnail/0.1>`_


Contact
==============
If you have any comments, ideas questions, feedback, etcetera, email me and we'll be in touch. I'm `flavio@vieiracaetano.com <mailto:flavio@vieiracaetano.com>`_
