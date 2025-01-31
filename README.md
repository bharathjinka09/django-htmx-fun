# django-htmx-fun

A small Django application to advertise the fun [htmx](//htmx.org) can bring you.

It implements a Single-Page-Application for writing a diary.

The entries in the diary database get lazy loaded (endless scrolling) via [hx-trigger="revealed"](https://htmx.org/attributes/hx-trigger/)

# Why I love htmx?

If you look into the past then one thing is clear: stateless has won. Nobody starts a new project with [Corba](https://en.wikipedia.org/wiki/Common_Object_Request_Broker_Architecture)
these days. Stateless http is the winner.

I don't understand why JavaScript based frontend frameworks seem to be the only way for new projects.

I want the client/browser to be SSS (simple, stupid and stateless).

I need to validate my data on the server anyway. So why should I validate them on the client?

The Django Forms library has all you need to write database focused applications.

Sending HTML fragements over the wire keeps my application simple.

There is just one thing which is outdated (although it is still perfectly fine). The need
for a full page refresh after submitting a form.

I want html pages with several small forms and I want to load and submit each of them 
individually. This does not mean I want to write a Single-Page-Application. There
are more colors than black and white. 

[Make web development fun again (Slides)](https://docs.google.com/presentation/d/1KHtEitL4O-EjbxrWdUk8oV9ciXcB39MLOA295QGqK28/edit#slide=id.p)

## Install

If you want to install my small htmx demo application:

```
python3 -m venv django-htmx-fun-env
cd django-htmx-fun-env
. bin/activate
pip install -e git+ssh://git@github.com/guettli/django-htmx-fun.git#egg=django_htmx_fun
```

## Run Database Migrations

```
manage.py migrate
```

## Start Webserver
```
manage.py runserver
```

Diary: http://127.0.0.1:8000/

## Admin
```
manage.py createsuperuser

```
Admin: http://127.0.0.1:8000/admin

## Screenshot

![diary-django-htmx](docs/diary-django-htmx.png)

In devtools you can see the lazy loading of the endless scrolling

... All this is possible without writing a single line of JavaScript :-)

## Pull Requests are welcome

You have an idea how to improve this example? Great! Just do it, provide a pull request and I will merge it.

## Podcast

[Podcast with the inventor of htmx](https://devmode.fm/episodes/dynamic-html-with-htmx/amp)

## Related

* [Güttli Django Tips](https://github.com/guettli/django-tips)
* [Güttli's opinionated Python Tips](https://github.com/guettli/python-tips)
* [Güttli working-out-loud](https://github.com/guettli/wol)


