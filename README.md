# [Django Admin Volt PRO](https://appseed.us/admin-dashboards/django-dashboard-volt-pro)

Modern template for **Django Admin Interface** coded on top of **[Volt Dashboard](https://django-volt-pro.appseed-srv1.com/)** (PRO version). Volt Pro is a premium Bootstrap 5 Admin Dashboard featuring over 800 components, 20 example pages and 10 fully customized plugin written in Vanilla Javascript. It is based on the latest version of Bootstrap.

> Originally coded by [Iman Karimi](https://github.com/imankarimi), actively supported by [AppSeed](https://appseed.us/) via Github (issues tracker) and [Discord](https://discord.gg/fZC6hup).

<br>

**Links & Resources**

- [Django Volt Dashboard PRO](https://appseed.us/admin-dashboards/django-dashboard-volt-pro) - Starter that uses the same UI Kit
- [Django Volt Dashboard PRO](https://django-volt-pro.appseed-srv1.com/) - LIVE Demo

<br />

## Why Django Admin Volt Professional?

- UI Kit: **Volt Dashboard** (PRO version) provided by **Themesberg**
- New fresh look
- Responsive mobile interface
- Useful admin home page
- Minimal template overriding
- Easy integration

<br />

![Django Admin Volt Professional - Template project for Django provided by AppSeed.](https://user-images.githubusercontent.com/51070104/137681083-49905174-a36f-4c8b-aec1-54439afccfbc.gif)

<br>

## Installation

```bash
$ pip install git+https://github.com/app-generator/priv-django-admin-volt-pro.git
# or
$ easy_install git+https://github.com/app-generator/priv-django-admin-volt-pro.git
```

* Add 'admin_volt' application to the INSTALLED_APPS setting of your Django project settings.py file (note it should be before 'django.contrib.admin'):

```python
INSTALLED_APPS = (
    'admin_volt.apps.AdminVoltConfig',
    'django.contrib.admin',
    # ...
)
```


* All programs you add in **INSTALLED_APPS** should look like this: **APP_NAME.apps.APP_NAMEConfig**.

> In this feature, we considered that each App can have its own icon, so we ask users to use this feature according to the method. Also in apps.py of each program according to the example add the icon field in the corresponding class. You can go **[here](https://fontawesome.com/v4.7/icons/)** to use more icons


```python
from django.apps import AppConfig

class APP_NAMEConfig(AppConfig):
    name = 'APP_NAME'
    icon = 'ICON_CLASS'  # for example: icon = 'fa fa-users'
```

* Make sure ``django.template.context_processors.request`` context processor is enabled in settings.py (Django 1.8+ way):

```python
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                # ...
                'django.template.context_processors.request',
                # ...
            ],
        },
    },
]
```

:warning: **Warning!!**
* Before Django 1.8 you should specify context processors different way. Also use ``django.core.context_processors.request`` instead of ``django.template.context_processors.request``.

```python
from django.conf import global_settings

TEMPLATE_CONTEXT_PROCESSORS = global_settings.TEMPLATE_CONTEXT_PROCESSORS + (
    'django.core.context_processors.request',
)
```

* Collect static if you are in production environment:

```bash
$ python manage.py collectstatic
```

* Clear your browser cache

<br />

## Screenshots

![Django Admin Volt PRO - Presentation Page.](https://user-images.githubusercontent.com/51070104/137681464-5fc865b6-8a69-4f85-be5a-e263540d6f96.png)

<br>

![Django Admin Volt PRO - Admin Users Page.](https://user-images.githubusercontent.com/51070104/137681552-2c1c6ec7-040f-4bba-998f-71fa5f4ed5d0.png)

<br>

![Django Admin Volt PRO - Admin Users Details.](https://user-images.githubusercontent.com/51070104/137681689-b0ecdc95-b795-4beb-a6ed-1e7a566f6180.png)

<br>

![Django Admin Volt PRO - Admin Users Details (permissions).](https://user-images.githubusercontent.com/51070104/137681789-25aa309a-96f8-44b5-878b-c0e646c2302e.png)

<br />

---
[Django Admin Volt PRO](https://appseed.us/admin-dashboards/django-dashboard-volt-pro) - Provided by **[AppSeed](https://appseed.us/)**
