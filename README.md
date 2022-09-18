<div align="center">

# ***My Django Exploration***
[![marwanmusa github](https://img.shields.io/badge/GitHub-marwanmusa-181717.svg?style=flat&logo=github)](https://github.com/marwanmusa)

![logo django](https://avatars.githubusercontent.com/u/27804?s=200&v=4)
</div>

---

# What does “Django” mean, and how do we pronounce it?
Django is named after [Django Reinhardt](https://en.wikipedia.org/wiki/Django_Reinhardt), a jazz manouche guitarist from the 1930s to early 1950s. To this day, he’s considered one of the best guitarists of all time. Django is pronounced JANG-oh. Rhymes with FANG-oh. The “D” is silent. We can hear this [audio](https://www.red-bean.com/~adrian/django_pronunciation.mp3) how to pronounce it right.

Django is a high-level python-based free and open-source web framework that follows the model-view-template(MVT) architectural pattern. As of now, the framework is maintained by Django Software Foundation (DSF), an independent organization based in the US and established as a 501(c)(3) non-benefit.

It was created in the fall of 2003 when the web programmers at the Lawrence Journal-World newspaper, Adrian Holovaty and Simon Willson. Began using python to build applications. Two years later, in July of 2005, it was released to the public under a BSD license. Later, in June 2008, the fledgling Django Software Foundation(DSF) took over the development of Django.

<br>

# Who’s behind this?
Django was originally developed at World Online, the web department of a newspaper in Lawrence, Kansas, USA. Django’s now run by an international [team of volunteers](https://www.djangoproject.com/foundation/teams/).

<br>

# List of popular firms using Django
> **PBS**<br>
> **Instagram**<br>
> **Mozilla**<br>
> **The Washington Times**<br>
> **Disqus, Bitbucket**<br>
> **NextDoor**<br>

<br>

# What are the features of Django?
- SEO Optimized
- Extremely fast
- Fully loaded framework that comes along with *authentications*, *content administrations*, *RSS feeds*, etc
- Very secure thereby helping developers avoid common *security mistakes* such as cross-site request forgery (csrf), clickjacking, cross-site scripting, etc
- It is exceptionally `scalable` which in turn helps meet the heaviest traffic demands
- Immensely `versatile` which allows us to `develop` any kind of websites

<br>

# Advantages of using Django
- Rich Ecosystem: It comes with numerous third-party apps which can be easily integrated as per the requirements of the project.
- Maturity:  Django has been in use for over a decade. In the time frame, a lot of features are added and enhanced to make it a Robust framework. Apart from that, there are a large number of developers who are using Django.
- Admin panel: Django provides an admin dashboard that we can use to do basic CRUD operations over the models.
- Plugins: Allow programmers to add various features to applications and leave sufficient space for customization.
- Libraries: Due to the large development community there is an ample number of libraries for every task.
- ORM: It helps us with working with data in a more object-oriented way.

<br>

# Django Architecture
Django follows the MVT (Model View Template) pattern which is based on the Model View Controller architecture. It’s slightly different from the MVC pattern as it maintains its own conventions, so, the controller is handled by the framework itself. The template is a presentation layer. It is an HTML file mixed with Django Template Language (DTL). The developer provides the model, the view, and the template then maps it to a URL, and finally, Django serves it to the user.
<div align="center">

![mvt django](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/10/mvt.png)
</div>
<br>

# How do I get started with Django?
1. [Download the code](https://www.djangoproject.com/download/).
2. Install Django (I followed this [installation guide](https://docs.djangoproject.com/en/4.1/intro/install/))
3. Walk through the [tutorial](https://docs.djangoproject.com/en/4.1/intro/tutorial01/).
4. Check out the rest of the [documentation](https://docs.djangoproject.com/en/4.1/)

##  *Installing Django*
You may have readed it from the [installation guide](https://docs.djangoproject.com/en/4.1/intro/install/), but if you haven't already installed it, then just open your `terminal/command prompt` and type

```bash
$ python -m pip install Django # to install
$ python -m django --version # to check version
```

## *Creating a project*
```bash
$ django-admin startproject mysite
```
`Note : We’ll need to avoid naming projects after built-in Python or Django components. In particular, this means we should avoid using names like django (which will conflict with Django itself) or test (which conflicts with a built-in Python package).`


`Where should this code live? : If our background is in plain old PHP (with no use of modern frameworks), we’re probably used to putting code under the web server’s document root (in a place such as` **`/var/www`**`). With Django, we don’t do that. It’s not a good idea to put any of this Python code within our web server’s document root, because it risks the possibility that people may be able to view our code over the web. That’s not good for security. Put the code in some directory `**`outside`**` of the document root, such as `**`/home/mycode`**`.`

Let’s look at what **`startproject`** created:
```py
mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
```

These files are:
- The outer **`mysite/`** root directory is a container for our project. Its name doesn’t matter to Django; we can rename it to anything you like.
- **`manage.py`**: A command-line utility that lets us interact with this Django project in various ways. You can read all the details about **`manage.py`** in [django-admin and manage.py](https://docs.djangoproject.com/en/4.1/ref/django-admin/).
- The inner **`mysite/`** directory is the actual Python package for our project. Its name is the Python package name we’ll need to use to import anything inside it (e.g. **`mysite.urls`**).
- **`mysite/__init__.py`**: An empty file that tells Python that this directory should be considered a Python package. If you’re a Python beginner, read [more about packages](https://docs.python.org/3/tutorial/modules.html#tut-packages) in the official Python docs.
- **`mysite/settings.py`**: Settings/configuration for this Django project. [Django settings](https://docs.djangoproject.com/en/4.1/topics/settings/) will tell us all about how settings work.
- **`mysite/urls.py`**: The URL declarations for this Django project; a “table of contents” of our Django-powered site. We can read more about URLs in [URL dispatcher](https://docs.djangoproject.com/en/4.1/topics/settings/).
- **`mysite/asgi.py`**: An entry-point for ASGI-compatible web servers to serve our project. See [How to deploy with ASGI for more details](https://docs.djangoproject.com/en/4.1/howto/deployment/asgi/).
- **`mysite/wsgi.py`**: An entry-point for WSGI-compatible web servers to serve our project. See [How to deploy with WSGI for more details](https://docs.djangoproject.com/en/4.1/howto/deployment/wsgi/).

## *The development server*
Let’s verify our Django project works. In the outer mysite directory, run the following commands:
```bash
$ python manage.py runserver
```
We’ll see the following output on the command line:
```bash
Performing system checks...

System check identified no issues (0 silenced).

You have unapplied migrations; your app may not work properly until they are applied.
Run 'python manage.py migrate' to apply them.

September 13, 2022 - 15:50:53
Django version 4.1, using settings 'mysite.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```
`Note : Ignore the warning about unapplied database migrations for now; we’ll deal with the database shortly.`

*Changing the port:*
```bash
# By default, the runserver command starts the development server on the internal IP at port 8000.

$ python manage.py runserver 8080 
# If we want to change the server’s port, pass it as a command-line argument. For instance, this command starts the server on port 8080.

$ python manage.py runserver 0:8000 
# If we want to change the server’s IP, pass it along with the port. For example, to listen on all available public IPs (which is useful if we're running Vagrant or want to show off our work on other computers on the network)
```
`0 is a shortcut for 0.0.0.0. Full docs for the development server can be found in the `[runserver](https://docs.djangoproject.com/en/4.1/ref/django-admin/#django-admin-runserver)` reference.`

## *Creating the app*
Now that our environment – a “project” – is set up, we’re set to start doing work.

Each application we write in Django consists of a Python package that follows a certain convention. Django comes with a utility that automatically generates the basic directory structure of an app, so we can focus on writing code rather than creating directories.

> **Projects vs. apps**
>
> What’s the difference between a project and an app? An app is a web application that does something – e.g., a blog system, a database of public records or a small poll app. A project is a collection of configuration and apps for a particular website. A project can contain multiple apps. An app can be in multiple projects.

Our apps can live anywhere on our Python path. In this tutorial, we’ll create our poll app in the same directory as the manage.py file so that it can be imported as its own top-level module, rather than a submodule of mysite.

To create app, make sure we’re in the same directory as manage.py and type this command:
```bash
$ python manage.py startapp polls # that 'polls' app name is just for example, you can change it on your own app
```

That’ll create a directory polls, which is laid out like this:
```py
polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
```
This directory structure will house the poll application.

<br>

# What Python version can I use with Django?


| Django version | Python versions |
| --- | --- |
| 2.2 | 3.5, 3.6, 3.7, 3.8 (added in 2.2.8), 3.9 (added in 2.2.17) |
| 3.1 | 3.6, 3.7, 3.8, 3.9 (added in 3.1.3) |
| 3.2 | 3.6, 3.7, 3.8, 3.9, 3.10 (added in 3.2.9) |
| 4.0, 4.1 | 	3.8, 3.9, 3.10 |

For each version of Python, only the latest micro release (A.B.C) is officially supported. We can find the latest micro version for each series on the [Python download page](https://www.python.org/downloads/).

<br>

# What Python version should I use with Django?
Since newer versions of Python are often faster, have more features, and are better supported, the latest version of Python 3 is recommended.

We don’t lose anything in Django by using an older release, but can't take advantage of the improvements and optimizations in newer Python releases. Third-party applications for use with Django are free to set their own version requirements.

<br>

# What is models on Django?
A model is the single, definitive source of information about our data. It contains the essential fields and behaviors of the data we’re storing. Generally, each model maps to a single database table. They are defined in `app/models.py`. <br>
The basics :
- Each model is a Python class that subclasses **django.db.models.Model**.
- Each attribute of the model represents a database field.
- With all of this, Django gives us an automatically-generated database-access API; see [Making queries](https://docs.djangoproject.com/en/4.1/topics/db/queries/). <br>
`Example:`
```py
from django.db import models
class SampleModel(models.Model):
    field1 = models.CharField(max_length = 50)
    field2 = models.IntegerField()
    class Meta:
        db_table = “sample_model”
```
Every model inherits from **`django.db.models.Model`**

Our example has 2 attributes (1 char and 1 integer field), those will be in the table fields.

The `metaclass` helps us set things like available permissions, singular and plural versions of the name, associated database table name, whether the model is abstract or not, etc.

<br>

# What are views in Django?
>A view function, or “view” for short, is simply a `Python function` that takes a **`web request`** and returns a **`web response`**. This response can be HTML contents of a *web page*, or a *redirect*, or a *404 error*, or an *XML document*, or an *image*, etc. <br>
`Example:`
```py
from django.http import HttpResponse
def sample_function(request):
 return HttpResponse(“Welcome to Django”)
```
There are two types of views:

- **`Function-Based Views`**: In this, we import our view as a function.
- **`Class-based Views`**: It’s an object-oriented approach.

<br>

# What are templates in Django?
**`Django’s template`** layer `renders` the information to be presented to the user in a *designer-friendly* format. Using templates, we can generate `HTML` dynamically. The HTML consists of both `static` as well as `dynamic` parts of the content. We can have any number of templates depending on the requirement of our project. It is also fine to have none of them. <br> Django has its own template system called the `Django template language` (DTL). Regardless of the backend, we can also load and render templates using `Django’s standard admin`.

<br>

# What is Django ORM?
This ORM (an acronym for Object Relational Mapper) enables us to interact with databases in a more pythonic way like we can avoid writing raw queries, it is possible to retrieve, save, delete and perform other operations over the database without ever writing any SQL query. It works as an abstraction layer between the models and the database.

<br>

# Define static files and explain their uses?
Websites generally need to serve additional files such as images. Javascript or CSS. In Django, these files are referred to as “static files”, Apart from that Django provides django.contrib.staticfiles to manage these static files.

<br>

# What is Django Rest Framework(DRF)?
Django Rest Framework is an open-source framework based upon Django which lets us create RESTful APIs rapidly.

<br>

# What is django-admin and manage.py and explain its commands?
django-admin is Django’s command-line utility for administrative tasks. In addition to this, a manage.py file is also automatically created in each Django project. Not only does it perform the same purpose as the django-admin but it also sets the DJANGO_SETTINGS_MODULE environment variable to point to the project's settings.py file.

- **`django-admin help`** - used to display usage information and a list of the commands provided by each application.
- **`django-admin version`** - used to check the Django version.
- **`django-admin check`** - used to inspect the entire Django project for common problems.
- **`django-admin compilemessages`** - Compiles .po files created by makemessages to .mo files for use with the help of built-in gettext support.
- **`django-admin createcachetable`** - Creates the cache tables for use in the database cache backend.
- **`django-admin dbshell`** - Runs the command-line client for the database engine specified in the ENGINE setting(s), with the connection parameters (USER, PASSWORD, DB_NAME, USER etc.) specified settings file.
- **`django-admin diffsettings`** - Shows the difference between the existing settings file and Django’s default settings.
- **`django-admin dumpdata`** - Used to the dumpdata from the database.
- **`django-admin flush`** - Flush all values from the database and also re-executes any post-synchronization handlers specified in the code.
- **`django-admin inspectdb`** - It generates django models from the existing database tables.
- **`django-admin loaddata`** - loads the data into the database from the fixture file.
- **`django-admin makemessages`** - Used for translation purpose and it generates a message file too.
- **`django-admin makemigrations`** - Generates new migrations as per the changes detected to our models.
- **`django-admin migrate`** - Executes SQL commands after which the database state with the current set of models and migrations are synchronized.
- **`django-admin runserver`** - Starts a light-weight Web server on the local machine for development. The default server runs on port 8000 on the IP address 127.0.0.1. We can pass a custom IP address and port number explicitly if we want.
- **`django-admin sendtestemail`** - This is used to confirm email sending through Django is working by sending a test email to the recipient(s) specified.
- **`django-admin shell`** - Starts the Python interactive interpreter.
- **`django-admin showmigrations`** - Shows all migrations present in the project.
- **`django-admin sqlflush`** - Prints the SQL statements that would be executed for the flush command mentioned above.
- **`django-admin sqlmigrate`** - Prints the SQL statement for the named migration.
- **`django-admin sqlsequencereset`** - output the SQL queries for resetting sequences for the given app name(s).
- **`django-admin squashmigrations`** - Squashes a range of migrations for a particular app_label.
- **`django-admin startapp`** - Creates a new Django app for the given app name within the current directory or at the given destination.
- **`django-admin startproject`** - Creates a new Django project directory structure for the given project name within the current directory or at the given destination.
- **`django-admin test`** - Runs tests for all installed apps.
- **`django-admin testserver`** - Runs a Django development server (which is also executed via the runserver command) using data from the given fixture(s).
- **`django-admin changepassword`** - offers a method to change the user's password.
- **`django-admin createsuperuser`** - Creates a user account with all permissions(also known as superuser account).
- **`django-admin remove_stale_contenttypes`** - removes stale content types (from deleted models) in our database.
- **`django-admin clearsessions`** - Can be used to clean out expired sessions or as a cron job.

<br>

# What is Jinja templating?
Jinja Templating is a very popular templating engine for Python, the latest version is Jinja2. <br>
Some of its features are:
- **`Sandbox Execution`** - This is a sandbox (or a protected) framework for automating the testing process
- **`HTML Escaping`** - It provides automatic HTML Escaping as <, >, & characters have special values in templates and if using a regular text, these symbols can lead to XSS Attacks which Jinja deals with automatically.
- **`Template Inheritance`**
- **`Generates HTML templates`** much faster than `default engine`
- **`Easier to debug`** as compared to the default engine.

<br>

# What are Django URLs?
**`URLs`** are one of the most important parts of a web application and **Django** provides us with an elegant way to design our own custom URLs with help of its module known as **`URLconf`** (URL Configuration). The basic functionality of this python module is we can design our own URLs in Django in the way we like and then map them to the python function (**`View function`**). These URLs can be `static` as well as `dynamic`. These URLs as present in the **`urls.py`** where they are matched with the equivalent `view function`. <br>
Basic syntax:
```python
from django.urls import path
from . import views
urlpatterns = [
   path('data/2020/', views.data_2020),
   path('data/<int:year>/', views.data_year)
]
```

<br>

# What is the difference between a project and an app in Django?
In simple words Project is the entire Django application and an app is a module inside the project that deals with one specific use case. 
For eg, payment system(app) in the eCommerce app(Project).

<br>

# What are different model inheritance styles in the Django?
- **`Abstract Base Class Inheritance`**: Used when we only need the `parent class` to hold information that we don’t want to write for each `child model`.
- **`Multi-Table Model Inheritance`**:  Used when we are subclassing an existing model and need each model to have its own table in the database.
- **`Proxy Model Inheritance`**:  Used when we want to retain the model's field while altering the python level functioning of the model.

<br>

# What are Django Signals?
Whenever there is a modification in a model, we may need to trigger some actions. 
Django provides an elegant way to handle these in the form of signals. The signals are the utilities that allow us to associate events with actions. We can implement these by developing a function that will run when a signal calls it.<br>

**`List of built-in signals in the models:`**
| Signals | Description |
| --- | --- |
| django.db.models.pre_init & django.db.models.post_init | Sent before or after a models’s _init_() method is called |
| django.db.models.signals.pre_save & django.db.models.signals.post_save | Sent before or after a model’s save() method is called |
| django.db.models.signals.pre_delete & django.db.models.signals.post_delete | Sent before or after a models’ delete() method or queryset delete() method is called |
| django.db.models.signals.m2m_changed | 	Sent when a ManyToManyField is changed |
| django.core.signals.request_started & django.core.signals.request_finished | 	Sent when an HTTP request is started or finished |

<br>

# Explain the caching strategies in the Django?
Caching refers to the technique of storing the output results when they are processed initially so that next time when the same results are fetched again, instead of processing again those already stored results can be used, which leads to faster accessing as well us less resource utilization. Django provides us with a robust cache system that is able to store dynamic web pages so that these pages don’t need to be evaluated again for each request.

**`Some of the caching strategies in Django are listed below:`**
| Strategy | Description |
| --- | --- |
| Memcached | A memory-based cache server is the fastest and most efficient |
| FileSystem Caching | Values of the cache are stored as separate files in a serialized order |
| Local-memory Caching | This is used as the default cache strategy by Django if we haven’t set anything. It is per-process as well as thread-safe. |
| Database Caching | Cache data will be stored in the database and works very well if we have a fast and well-indexed DB server. |

<br>

# Explain user authentication in Django?
Django comes with a built-in user authentication system, which handles objects like users, groups, user-permissions, and few cookie-based user sessions. Django User authentication not only authenticates the user but also authorizes him.<br>

**`The system consists and operates on these objects:`**
- Users
- Permissions
- Groups
- Password Hashing System
- Forms Validation
- A pluggable backend system

<br>

# How to connect Django project to the database?
Django comes with a default database which is SQLite. To connect our project to this database, use the following commands:
- **`python manage.py migrate`** (*migrate command looks at the INSTALLED_APPS settings and creates database tables accordingly*)
- **`python manage.py makemigrations`** (*tells Django we have created/changed our models*)
- **`python manage.py sqlmigrate <name of the app followed by the generated id> `**(*sqlmigrate takes the migration names and returns their SQL*)

<br>

# How to configure static files?
Ensure that **`django.contrib.staticfiles`** is added to **`INSTALLED_APPS`**. In the settings file, define **`STATIC_URL`** for ex.

```python
STATIC_URL = 'static/'
```
In Django templates, use the static template tag to create the URL for the given relative path using the configured **`STATICFILES_STORAGE`**.
```html
{% load static %}
<img src="{% static 'my_sample/abcxy.jpg' %}" alt="ABC image">
```
Store the static files in a folder called **`static`** in the app. For example **`my_sample/static/my_sample/abcxy.jpg`**

<br>

# Explain Django Response lifecycle?
Whenever a request is made to a web page, Django creates an HttpRequest object that contains metadata about the request. After that Django loads the particular view, passing the HttpRequest as the first argument to the view function. Each view will be returning an HttpResponse object.
On the big picture following steps occur when a request is received by Django:
1. First of the Django **`settings.py`** file is loaded which also contain various middleware classes (**MIDDLEWARES**)
2. The middlewares are also executed in the order in which they are mentioned in the **MIDDLEWAREST**
3. From here on the request is now moved to the URL Router, who simply gets the URL path from the request and tries to map with our given URL paths in the **`urls.py`**. 
4. As soon as it has mapped, it will call the equivalent view function, from where an equivalent response is generated
5. The response also passes through the response **`middlewares`** and send back to the **`client/browser`**.

<br>

# What databases are supported by Django?
PostgreSQL and MySQL, SQLite and Oracle. Apart from these, Django also supports databases such as ODBC, Microsoft SQL Server, IBM DB2, SAP SQL Anywhere, and Firebird using third-party packages. Note: Officially Django doesn’t support any no-SQL databases.

# What's the use of a session framework?
Using the session framework, we can easily store and retrieve arbitrary data based on the pre-site-visitors. It stores data on the server-side and takes care of the process of sending and receiving cookies. These cookies just consist of a session ID, not the actual data itself unless we explicitly use a cookie-based backend.

<br>

# What’s the use of Middleware in Django?
**`Middleware`** is something that executes between the `request` and `response`. In simple words, we can say it **`acts as a bridge`** between the `request` and `response`. Similarly In Django when a request is made it moves through middlewares to views and data is passed through middleware as a response.

<br>

# What is context in the Django?
**`Context`** is a `dictionary mapping` template variable name given to Python objects in Django. This is the general name, but you can give any other name of your choice if you want.

<br>

# What is django.shortcuts.render function?
When a view function returns a webpage as HttpResponse instead of a simple string, we use render(). **`Render function`** is a `shortcut function` that lets the developer easily pass the data dictionary with the template. This function then `combines` the template with a data dictionary via `templating engine`. Finally, this render() returns as HttpResponse with the rendered text, which is the data returned by models. Thus, Django render() bypasses most of the developer’s work and lets him use different template engines.<br>
The basic syntax:<br>
```python
render(request, template_name, context=None, content_type=None, status=None, using=None)
```
The request is the parameter that generates the response. The template name is the HTML template used, whereas the context is a dict of the data passed on the page from the python. We can also specify the content type, the status of the data we passed, and the render we are returning.

<br>

# What’s the significance of the settings.py file?
As the name suggests this file **`stores the configurations`** or **`settings`** of our Django project, like database configuration, backend engines, middlewares, installed applications, main URL configurations, static file addresses, templating engines, main URL configurations, security keys, allowed hosts, and much more.

<br>

# How to view all items in the Model?
```python
ModelName.objects.all()
```

<br>

# How to filter items in the Model?
```python
ModelName.objects.filter(field_name=”term”)
```

<br>

# How to use file-based sessions?
To use the same, we need to set the **`SESSION_ENGINE`** settings to "**`django.contrib.sessions.backends.file`**"

<br>

# What is mixin?
**`Mixin`** is a type of **`multiple inheritances`** wherein we can combine `behaviors` and `attributes` of more than one parent class. It provides us with an excellent way to *reuse code* from multiple classes. One drawback of using these **`mixins`** is that it becomes difficult to analyze what a class is doing and which methods to override in case of its code being too scattered between multiple classes.

<br>

# What is Django Field Class?
'**`Field`**' refers to an abstract class that represents a **`column in the database table`**. 
The Field class is just a subclass of **`RegisterLookupMixin`**. In Django, these fields are used to create database tables (**`db_types()`**) which are used to map Python types to the database using **`get_prep_value()`** and the other way round using **`from_db_value()`** method. Therefore, fields are fundamental pieces in different Django APIs such as `models` and `querysets`.

<br>

# Why is permanent redirection not a good option?
**`Permanent redirection`** is used only when we don’t want to lead **visitors** to the `old URLs`. The response of the permanent redirections is cached by the browser so when we try to redirect to something else it will cause **`issues`**. Since this is a *browser-side operation* if our user wants to move to a new page it will load the *same page*.

<br>

# Difference between Django OneToOneField and ForeignKey Field?
Both of them are of the **`most common types`** of fields used in Django. The only difference between these two is that ForeignKey field consists of **`on_delete option`** along with a model’s class because it’s used for **`many-to-one relationships`** while on the other hand, the OneToOneField, only carries out a **`one-to-one relationship`** and requires only the model’s class.

<br>

# How can we combine multiple QuerySets in a View?
Initially, Concatenating QuerySets into lists is believed to be the easiest approach. Here’s an example of how to do that:
```python
from itertools import chain
result_list = list(chain(model1_list, model2_list, model3_list))
```

<br>

# How to get a particular item in the Model?
```python
ModelName.objects.get(id=”term”)
```
`Note: If there are no results that match the query, get() will raise a `**`DoesNotExist`**`  exception. If more than one item matches the given get() query. In this case, it’ll raise  `**`MultipleObjectsReturned`**`, which is also an attribute of the model class itself.`

<br>

# How to obtain the SQL query from the queryset?
```python
print(queryset.query)
```
<br>

# Give the exception classes present in Django.
Django uses its own exceptions as well as those present in Python. Django core exceptions are present in `django.core.exceptions` class some of which are mentioned in the table below:

**`Some of the caching strategies in Django are listed below:`**
| Exception | Description |
| --- | --- |
| **AppRegistryNotReady** | Raised when we try to use our models before the app loading process (initializes the ORM) is completed. |
| **ObjectDoesNotExist** | This is the base class for `DoesNotExist` exceptions |
| **EmptyResultSet** | This exception may be raised if a query won’t return any result |
| **FieldDoesNotExist** | This exception is raised by a model’s `_meta.get_field()` function in case the requested field does not exist |
| **MultipleObjectsReturned** | This is raised by a query if multiple objects are returned and only one object was expected |

<br>

# Does the Django framework scale?
*Yes*. Hardware is much cheaper when compared to the development time and this is why Django is designed to make full use of any amount of hardware that we can provide it. Django makes use of a “**`shared-nothing`**” architecture meaning we can add hardware at any level i.e `database servers`, `caching servers` or `Web/ application servers`.

<br>

# Is Django a CMS?
Django is not a `CMS (content-management-system)`. It is just a `Web framework`, a tool that allows us to `build websites`.

<br>

# Is Django better than Flask?
Django is a `framework` that allows us to build **large projects**. On the other hand, Flask is used to build **smaller websites** but flask is much `easier to learn and use` compared to Django. Django is a `full-fledged framework` and `no third-party packages are required`. Flask is more of a `lightweight framework` that allows us to install third-party tools as and how we like. So, the answer to this question basically `depends on the user’s need` and in case the need is very heavy, the answer is definitely, ***Django***.

<br>

# An Example of a Django view.
A view in Django either returns an `HttpResponse` or raises an `exception` such as `Http404`. HttpResponse contains the objects that consist of the content that is to be rendered to the user.

**`Example:`**
```python
from django.http import HttpResponse
def hello_world(request):
    html = "<h1>Hello World!</h1>"
    return HttpResponse(html)
```

<br>

# What is `csrf_token`?
The `csrf_token` is used for protection against `Cross-Site Request Forgeries`. This kind of attack takes place when a malicious website consists of a `link`, some JavaScript or a form whose aim is to perform some action on our website by using the login credentials of a genuine user.