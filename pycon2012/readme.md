![lunch](https://github.com/tylerball/confnotes/raw/master/pycon2012/pycon.jpg)

What I learned at PyCon
=======================

* In [Stormy Peters' Keynote][peters] on how to keep users in control of their experience online, she said:

> "Learning something new is equal to a 20% raise"

Continous Deployment
--------------------

[David Cramer's talk][cramer] from [Disqus](http://disqus.com/welcome/) on continuous deployment had a lot of great ideas in it
about iterating quickly on your projects:

* automated tests, peer review > test suite on the build > deploy
* Develop features incrementally, release frequently, smaller doses of QA
* You don't need to test the full stack in every environment
* local development should be dead simple. clone and make. will do pip install
  automatically.
* need to test dependencies? use vagrant with the same configuration service you're using
  for production. e.g. puppet or chef
* [Phabricator](http://phabricator.org/) a code review and ticketing tool built by

Facebook that is in early release, but looks promising.

Django forms
------------

Nathan Yergler of EventBrite [talk on django form processing][yergler].

* [django-crispy-forms](https://github.com/maraujop/django-crispy-forms) gives you
greater flexibility for the HTML output of your form, including built in Twitter
Bootstrap templates

Testing and Django
------------------

[Carl Meyer on testing][meyer].

### testing models

* [django factory\_boy](https://github.com/dnerdy/factory_boy) a tool that makes adding
  fixtures for your model tests really easy
* don't create data you don't need for a test
* he shows some examples of using [mock](http://www.voidspace.org.uk/python/mock/), which
  looks cool

### testing views

* Write less view code, use things like selenium for interface testing

Fabric
------

Ricardo Kikner's talk on [Using fabric to standardizw the development process][kirkner]
wasn't the most eloquent, and his examples weren't as good as some of the fabric scripts
I've seen around the net but it gave a good foundation and the right philosophy.

* Developers should be able to issue one command to set up their development environment
and one command to deploy to the server.
* fabric can contain commands for all the common, repetitive tasks that we do. Remember
  DRY?

More cool talks
---------------

* [Parsing horrible things with Python](http://pyvideo.org/video/708/parsing-horrible-things-with-python)
* [A Noob Speaks to Noobs][noobs] walked in at the end of this one, but it contains some good advice about getting set up on a server with Django.
* [Stop Writing Classes](http://pyvideo.org/video/880/stop-writing-classes)

[peters]:http://pyvideo.org/video/625/keynote-stormy-peters-mozilla-corporation
[cramer]:http://pyvideo.org/video/655/practicing-continuous-deployment
[yergler]:http://youtu.be/Wh9a0obtQUQ
[meyer]:http://pyvideo.org/video/699/testing-and-django
[kirkner]:http://pyvideo.org/video/677/using-fabric-to-standardize-the-development-proce
[noobs]:http://pyvideo.org/video/628/a-noob-speaks-to-noobs-your-first-site-in-the-cl
