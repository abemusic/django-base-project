# README

This project was heavily influenced by the django-twoscoops-project that can
be found at https://github.com/twoscoops/django-twoscoops-project

## Getting Started

You'll need to setup your virtual environment first, and I recommend using
[virtualenvwrapper]. So, go ahead ahead and create your virtual environment

```bash
    # First create your project directory:
    mkdir foobar && cd foobar

    # And then make your virtual environment
    mkvirtualenv foobar
    
    # The virtual environment will already be activated, but in the 
    # future to switch to this environment you'll need to do
    workon foobar
    
    # Install django into your virtual environment
    pip install django==1.5.1
    
```

When starting a new Django project, use the --template and --extension args
to django-admin.py. For example, to create a new project called `foobar` you
can do something like this:

```bash
    django-admin.py startproject \
      --template=https://github.com/abemusic/django-base-project/archive/master.zip \
      --extension=py,rst,html foobar .
```
    
This basically tells django to create a new project called `foobar` in the 
current directory and use a project template from the zip file on github. 
The extension argument instructs django to treat any files with the .py, .rst, 
and .html extension as templates and render them with a particular context. 
For example, the HTML files might reference a variable called `{{ project_name }}`, 
and django would render that as `foobar` in this case. For more information on 
starting a new project or app using templates, see the documentation at 
https://docs.djangoproject.com/en/dev/ref/django-admin/#startproject-projectname-destination


[virtualenvwrapper]: https://bitbucket.org/dhellmann/virtualenvwrapper
