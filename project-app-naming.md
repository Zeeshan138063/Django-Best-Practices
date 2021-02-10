1) #### Application Naming.
`Modules should have short, all-lowercase names. Underscores can be used in the module name if it improves readability. 
 Python packages should also have short, all-lowercase names, although the use of underscores is discouraged.`
* my_django_app
* my-django-app   ```**Not allowed syntactically**```
* mydjangoapp  ```**Recommended solution**```

[This image help you to understand](https://github.com/Zeeshan138063/Django-Best-Practices/blob/main/screenshot-www.reddit.com-2021.02.10-13_48_24.png)

2) ####  [Project Naming](https://forum.djangoproject.com/t/project-naming-conventions/339/12).
```
rene@rene-desktop tmp % cd myproject
rene@rene-desktop myproject % ./manage.py startapp myapp
rene@rene-desktop myproject % tree
.
├── manage.py
├── myapp
│   ├── admin.py
│   ├── apps.py
│   ├── __init__.py
│   ├── migrations
│   │   └── __init__.py
│   ├── models.py
│   ├── tests.py
│   └── views.py
└── myproject
    ├── __init__.py
    ├── settings.py
    ├── urls.py
    └── wsgi.py

```
`I know that some people dislike having two nested directories with the same name (myproject/myproject). 
 In this case, I recommend to rename the outer myproject directory. You can do this without having to adjust any import paths 
 (only the inner myproject directory is a Python package). If the outer myproject directory also is the repository root, 
 it is even possible for each developer to use their own local name without interfering with others:
`
```
git clone https://example.org/myproject my-preferred-name
cd my-preferred-name
# ...
```
